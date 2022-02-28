# Exceptions
## Built-in Exception variable

- type(e).__name__ -> give the exception name
- dir(e) ->  related methods
- e.args -> print tuple of args

## Built-in Exceptions

### Base classes
|Exception|Detail|
|-|-|
| BaseException| The base class for all built-in exceptions |
| Exception | All built-in, non-system-exiting exceptions are derived from this class. All user-defined exceptions should also be derived from this class. |
| ArithmeticError | The base class for those built-in exceptions that are raised for various arithmetic errors: **OverflowError, ZeroDivisionError, FloatingPointError**. |
| BufferError | Raised when a [buffer](https://docs.python.org/3/c-api/buffer.html#bufferobjects) related operation cannot be performed |
| LookupError | The base class for the exceptions that are raised when a key or index used on a mapping or sequence is invalid: [IndexError](https://docs.python.org/3/library/exceptions.html#IndexError), [KeyError](https://docs.python.org/3/library/exceptions.html#KeyError). This can be raised directly by [codecs.lookup()](https://docs.python.org/3/library/codecs.html#codecs.lookup) |

### `Concrete exceptions `
|Exception|Detail|
|-|-|
| AssertionError | Raised when an [assert](https://docs.python.org/3/reference/simple_stmts.html#assert) statement fails. |
| AttributeError | Raised when an attribute reference (see Attribute references) or assignment fails. |
| EOFError | Raised when the input() function hits an end-of-file condition (EOF) without reading any data. |
| FloatingPointError | Not currently used. |
| GeneratorExit | Raised when a [generator](https://docs.python.org/3/glossary.html#term-generator) or [coroutine](https://docs.python.org/3/glossary.html#term-coroutine) is closed; see generator.close() and coroutine.close(). It directly inherits from BaseException instead of Exception since it is technically not an error. |
| ImportError | Raised when the import statement has troubles trying to load a module. Also raised when the “from list” in `from ... import `has a name that cannot be found. |
| ModuleNotFoundError | A subclass of ImportError which is raised by import when a module could not be located. It is also raised when None is found in sys.modules. |
| IndexError | Raised when a sequence subscript is out of range. (Slice indices are silently truncated to fall in the allowed range; if an index is not an integer, TypeError is raised.) |
| **KeyError** | Raised when a mapping (dictionary) key is not found in the set of existing keys. |
| KeyboardInterrupt | Raised when the user hits the interrupt key (normally **Control-C or Delete**). During execution, a check for interrupts is made regularly. |
| MemoryError | Raised when an operation runs out of memory but the situation may still be rescued (by deleting some objects). |
| NameError | Raised when a local or global name is not found. This applies only to unqualified names. The associated value is an error message that includes the name that could not be found. |
| NotImplementedError | This exception is derived from RuntimeError. In user defined base classes, abstract methods should raise this exception when they require derived classes to override the method, or while the class is being developed to indicate that the real implementation still needs to be added. |
| [OSError](https://docs.python.org/3/library/exceptions.html#OSError) | This exception is raised when a system function returns a system-related error, including I/O failures such as “file not found” or “disk full” (not for illegal argument types or other incidental errors). |
| OverflowError | Raised when the result of an arithmetic operation is too large to be represented. This cannot occur for integers (which would rather raise MemoryError than give up). However, for historical reasons, OverflowError is sometimes raised for integers that are outside a required range. Because of the lack of standardization of floating point exception handling in C, most floating point operations are not checked. |
| RecursionError |  It is raised when the interpreter detects that the maximum recursion depth (see [sys.getrecursionlimit()](https://docs.python.org/3/library/sys.html#sys.getrecursionlimit)) is exceeded. |
| ReferenceError | This exception is raised when a weak reference proxy, created by the weakref.proxy() function, is used to access an attribute of the referent after it has been garbage collected. For more information on weak references, see the [weakref](https://docs.python.org/3/library/weakref.html#module-weakref) module. |
| RuntimeError | Raised when an error is detected that doesn’t fall in any of the other categories. The associated value is a string indicating what precisely went wrong. |
| [StopIteration](https://docs.python.org/3/library/exceptions.html#StopIteration) | - |
| [StopAsyncIteration](https://docs.python.org/3/library/exceptions.html#StopAsyncIteration) | - |
| [SyntaxError](https://docs.python.org/3/library/exceptions.html#SyntaxError) | - |
| TabError | - |
| IndentationError | - |
| SystemError | Raised when the interpreter finds an internal error, but the situation does not look so serious to cause it to abandon all hope. The associated value is a string indicating what went wrong (in low-level terms). |
| SystemExit     | - |
| SystemExit | - |
| UnboundLocalError | Raised when a reference is made to a local variable in a function or method, but no value has been bound to that variable. This is a subclass of NameError. |
| [UnicodeError](https://docs.python.org/3/library/exceptions.html#UnicodeError) | - |
| ValueError | - |
| ZeroDivisionError | - |
| WindowsError | - |

### OS exceptions
|Exception|Detail|
|-|-|
| BlockingIOError | Raised when an operation would block on an object (e.g. socket) set for non-blocking operation. Corresponds to errno EAGAIN, EALREADY, EWOULDBLOCK and EINPROGRESS. |
| ChildProcessError | Raised when an operation on a child process failed. Corresponds to errno ECHILD. |
| ConnectionError |     A base class for connection-related issues.    Subclasses are BrokenPipeError, ConnectionAbortedError, ConnectionRefusedError and ConnectionResetError. |
| BrokenPipeError | A subclass of ConnectionError, raised when trying to write on a pipe while the other end has been closed, or trying to write on a socket which has been shutdown for writing. Corresponds to errno EPIPE and ESHUTDOWN. |
| ConnectionAbortedError | A subclass of ConnectionError, raised when a connection attempt is aborted by the peer. Corresponds to errno ECONNABORTED. |
| ConnectionRefusedError | - |
| ConnectionResetError | - |
| FileExistsError | Raised when trying to create a file or directory which already exists. Corresponds to *errno* `EEXIST`. |
| FileNotFoundError | Raised when a file or directory is requested but doesn’t exist. Corresponds to errno `ENOENT` |
| InterruptedError | Raised when a system call is interrupted by an incoming signal. Corresponds to errno `EINTR.` |
| IsADirectoryError | Raised when a file operation (such as os.remove()) is requested on a directory. |
| NotADirectoryError | Raised when a directory operation (such as os.listdir()) is requested on something which is not a directory |
| PermissionError | Raised when trying to run an operation without the adequate access rights - for example filesystem permissions. Corresponds to errno EACCES and EPERM. |
| ProcessLookupError | Raised when a given process doesn’t exist. Corresponds to errno ESRCH |

