# QT
QT 4.4.3 with Visual Studio 2015

Add C:\Qt\4.4.3\bin to path variable

cd C:\Qt\4.4.3

configure.exe -debug -no-webkit -no-vcproj -no-phonon -no-phonon-backend

/c/QT/4.4.3/src/3rdparty/clucene/src/CLucene/config/CompilerMsvc.h

12,13d11
< #define _SILENCE_STDEXT_HASH_DEPRECATION_WARNINGS 1
< 
123c121
< //typedef double float_t;
---
> typedef double float_t;

/c/QT/4.4.3/src/3rdparty/clucene/src/CLucene/debug/lucenebase.h

61,62c61
<     //virtual ~LuceneBase(){};
< 	virtual ~LuceneBase()noexcept(false){};
---
>     virtual ~LuceneBase(){};

/c/QT/4.4.3/src/3rdparty/clucene/src/CLucene/index/MultiReader.h

105c105
< 	~MultiTermPositions()noexcept(false){};
---
> 	~MultiTermPositions() {};

/c/QT/4.4.3/src/3rdparty/clucene/src/CLucene/index/SegmentHeader.h

85c85
< 	~SegmentTermPositions()noexcept(false);
---
> 	~SegmentTermPositions();


/c/QT/4.4.3/src/3rdparty/clucene/src/CLucene/index/TermVector.h

368c368
< 	~SegmentTermPositionVector()noexcept(false);
---
> 	~SegmentTermPositionVector();


/c/QT/4.4.3/src/3rdparty/clucene/src/CLucene/util/VoidMap.h

222c222
< 	typename _compare,
---
> 	typename _Compare,
226c226
< 	CL_NS_STD(map)<_kt,_vt, _compare>,
---
> 	CL_NS_STD(map)<_kt,_vt, _Compare>,
229,230c229,230
< 	typedef typename CL_NS_STD(map)<_kt,_vt,_compare> _base;
< 	typedef __CLMap<_kt, _vt, CL_NS_STD(map)<_kt,_vt, _compare>,
---
> 	typedef typename CL_NS_STD(map)<_kt,_vt,_Compare> _base;
> 	typedef __CLMap<_kt, _vt, CL_NS_STD(map)<_kt,_vt, _Compare>,


/c/QT/4.4.3/src/corelib/arch/qatomic_windows.h

232c232
< //#  ifndef _M_IX86
---
> #  ifndef _M_IX86
243,244c243,244
< //#  else
< //#    define _InterlockedCompareExchangePointer(a,b,c) \
---
> #  else
> #    define _InterlockedCompareExchangePointer(a,b,c) \
246,250c246,250
< //#    define _InterlockedExchangePointer(a, b) \
< //        _InterlockedExchange(reinterpret_cast<volatile long *>(a), long(b))
< //#    define _InterlockedExchangeAddPointer(a,b) \
< //        _InterlockedExchangeAdd(reinterpret_cast<volatile long *>(a), long(b))
< //#  endif
---
> #    define _InterlockedExchangePointer(a, b) \
>         _InterlockedExchange(reinterpret_cast<volatile long *>(a), long(b))
> #    define _InterlockedExchangeAddPointer(a,b) \
>         _InterlockedExchangeAdd(reinterpret_cast<volatile long *>(a), long(b))
> #  endif
286c286
< //#ifndef _M_IX86
---
> #ifndef _M_IX86
288,290c288,290
< //#else
< //                                              (long)  
< //#endif
---
> #else
>                                               (long)  
> #endif


/c/QT/4.4.3/src/corelib/io/qfsfileengine_win.cpp

38,39d37
< #define PATH_MAX 4096
< 


