---
title: Exemples de Tracelogging C/C++
description: Cette rubrique contient des exemples Tracelogging C/C++.
ms.assetid: FB0A29B9-D1F7-4F13-AA75-5963A0699F7A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8f85a9ba4aca2da7405a908beb5cebbb2ef7be59422ea1d3706a83257e30106
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118041750"
---
# <a name="cc-tracelogging-examples"></a>Exemples de Tracelogging C/C++

Cette rubrique contient des exemples Tracelogging C/C++.

> [!IMPORTANT]
> Liez advapi32. lib lors de la compilation de ces exemples.

 

-   [Consigner les types de données intrinsèques](#log-intrinsic-data-types)
-   [Champs d’événement de nom](#name-event-fields)
-   [Niveau de détail des événements de journal](#log-event-verbosity-level)
-   [Mots clés des événements de journal](#log-event-keywords)
-   [Données d’événement de tableau de journaux](#log-array-event-data)
-   [Données d’événement de structure de journal](#log-structure-event-data)

### <a name="log-intrinsic-data-types"></a>Consigner les types de données intrinsèques

Cet exemple montre comment enregistrer des types de données intrinsèques, tels que des entiers, des valeurs booléennes, etc.


```C++
void TraceLoggingSample::BasicDataTypes()
{
    UINT8 u8 = 200;
    INT32 i32 = -2000000000;
    UINT32 u32 = 4000000000;
    INT64 i64 = 9000000000000000000;
    float f32 = 3.14f;
    BOOL b = TRUE;
    bool bcpp = true;

    /*
    The following four "NumericValues" events are equivalent (except where noted) ...
    */

    TraceLoggingWrite(
        g_hMyComponentProvider,
        "NumericValues",
        TraceLoggingUInt8(u8, "UINT8"),
        TraceLoggingInt32(i32, "INT32"),
        TraceLoggingUInt32(u32, "UINT32"),
        TraceLoggingHexUInt32(u32, "UINT32"),
        TraceLoggingInt64(i64, "INT64"),
        TraceLoggingFloat32(f32, "float"),
        TraceLoggingBool(b, "BOOL"),
        TraceLoggingBoolean(bcpp, "bool (C++)")
        );

    /*
    same as ...
    */

    TraceLoggingWrite(
        g_hMyComponentProvider,
        "NumericValues",
        TraceLoggingUInt8(200, "UINT8"),
        TraceLoggingInt32(-2000000000, "INT32"),
        TraceLoggingUInt32(4000000000, "UINT32"),
        TraceLoggingHexUInt32(4000000000, "UINT32"),
        TraceLoggingInt64(9000000000000000000, "INT64"),
        TraceLoggingFloat32(3.14f, "float"),
        TraceLoggingBool(TRUE, "BOOL"),
        TraceLoggingBoolean(true, "bool (C++)")
        );

    /*
    same as ...
    */

#ifdef __cplusplus

    /*
    TraceLoggingValue() automatically determines the value type (C++ only)
    */

    TraceLoggingWrite(
        g_hMyComponentProvider,
        "NumericValues",
        TraceLoggingValue(u8, "UINT8"),
        TraceLoggingValue(i32, "INT32"),
        TraceLoggingValue(u32, "UINT32"),
        TraceLoggingValue(u32, "UINT32"),
        TraceLoggingValue(i64, "INT64"),
        TraceLoggingValue(f32, "float"),
        TraceLoggingValue(b, "BOOL"),         // This will be evaluated as INT32, not as BOOL
        TraceLoggingValue(bcpp, "bool (C++)") 
        );

    TraceLoggingWrite(
        g_hMyComponentProvider,
        "NumericValues",
        TraceLoggingValue((BYTE)200, "UINT8"),
        TraceLoggingValue(-2000000000, "INT32"),
        TraceLoggingValue(4000000000, "UINT32"),
        TraceLoggingValue(4000000000, "UINT32"),    // This one won't show up as hex. TraceLoggingValue will use default out types
        TraceLoggingValue(9000000000000000000, "INT64"),
        TraceLoggingValue(3.14f, "float"),
        TraceLoggingValue((BOOL)TRUE, "BOOL"),      // This will be evaluated as INT32, not as BOOL
        TraceLoggingValue((bool)true, "bool (C++)") 
        );

#endif


    /*
    Strings and chars
    */

    TraceLoggingWrite(
        g_hMyComponentProvider,
        "Strings and Chars",
        TraceLoggingString("String1", "String (char)"),
        TraceLoggingWideString(L"LString2", "String (wide char)"),
        TraceLoggingChar('A', "Single char")
        );


    /*
    Other types
    */

    /*
    NOTE: In C, a GUID, FILETIME, or SYSTEMTIME value parameter must be an l-value.
    */

    INT_PTR iptr = 1234;
    UINT_PTR uptr = 4321;
    FILETIME ft;
    SYSTEMTIME st;
    SID const sid1 = { SID_REVISION, 1, 5, { 6 } };
    static const GUID s_TestGuid = { 0x3970f9cf, 0x2c0c, 0x4f11, { 0xb1, 0xcc, 0xe3, 0xa1, 0xe9, 0x95, 0x88, 0x33 } };

    GetSystemTime(&st);
    GetSystemTimeAsFileTime(&ft);

    TraceLoggingWrite(
        g_hMyComponentProvider,
        "Other Types",
        TraceLoggingGuid(s_TestGuid, "GUID"),
        TraceLoggingSystemTime(st, "Current Time (FILETIME)"),
        TraceLoggingPointer((LPCVOID)&iptr, "void*"),
        TraceLoggingSid(&sid1, "SID")
        TraceLoggingIntPtr(iptr, "INT_PTR"),
        TraceLoggingUIntPtr(uptr, "UINT_PTR")
        );
}
```



### <a name="name-event-fields"></a>Champs d’événement de nom

L’exemple montre comment nommer des champs d’événement.


```C++
void TraceLoggingSample::NamingData()
{
    UINT32 Cat = 0xCA7;

    /*
    Each of the following four events are equivalent:
    */

    /*
    TraceLogging uses the symbol to automatically name the field "Cat"
    and assign it the value contained in the variable Cat (0xCA7).
    */

    TraceLoggingWrite(
        g_hMyComponentProvider,
        "Cat1",
        TraceLoggingUInt32(Cat) 
        );

    TraceLoggingWrite(
        g_hMyComponentProvider,
        "Cat2",
        TraceLoggingValue(Cat)  
        );


    /*
    Use a different symbol for the value of the event's "Cat" field.  
    */
    
    UINT32 Tiger = Cat;
    
    /*
    Now we need to explicitly name the datum or we will have events with a 
    different field name ("Tiger").
    */

    TraceLoggingWrite(
        g_hMyComponentProvider,
        "Tiger",
        TraceLoggingUInt32(Tiger, "Cat")
        );

    TraceLoggingWrite(
        g_hMyComponentProvider,
        "Cat3",
        TraceLoggingValue(Tiger, "Cat")
        );
};
```



### <a name="log-event-verbosity-level"></a>Niveau de détail des événements de journal

Cet exemple montre comment enregistrer des événements par niveau de détail.


```C++
#include <winmeta.h> // for WINEVENT_LEVEL_* definitions
void TraceLoggingSample::LevelsAndKeywords()
{
    /*
    Verbosity levels and event keywords must be compile-time constants.

    TraceLoggingLevel accepts values 0-255
    TraceLoggingKeyword accepts values 0 to UINT64_MAX

    See winmeta.h for predefined verbosity levels and reserved keyword values.
    */

    PCWSTR MyName = L"Joe";
    INT16 MyRank = 99;
    ULONG MySerialNumber = 12345;

    /*
    The following is only logged when session verbosity level is 
    WINEVENT_LEVEL_VERBOSE (5) or higher ...  
    */

    TraceLoggingWrite(
        g_hMyComponentProvider,
        "Levels",
        TraceLoggingLevel(WINEVENT_LEVEL_VERBOSE),
        TraceLoggingWideString(MyName, "Name"),
        TraceLoggingInt16(MyRank, "Rank"),
        TraceLoggingUInt32(MySerialNumber, "Serial Number")
        );

    /*
    TraceLoggingWrite will not complain if TraceLoggingLevel is invoked more than once.  
    However, only the last level will be used.  
    The following event is only logged at WINEVENT_LEVEL_VERBOSE or higher...
    */

    TraceLoggingWrite(
        g_hMyComponentProvider,
        "Levels",
        TraceLoggingLevel(WINEVENT_LEVEL_CRITICAL),
        TraceLoggingLevel(WINEVENT_LEVEL_VERBOSE),
        TraceLoggingWideString(MyName, "Name"),
        TraceLoggingInt16(MyRank, "Rank"),
        TraceLoggingUInt32(MySerialNumber, "Serial Number")
        );
}
```



### <a name="log-event-keywords"></a>Enregistrer les mots clés des événements

Cet exemple montre comment définir des mots clés d’événement. Le filtrage des événements peut être effectué par niveau et par mot clé. Par exemple, les événements d’achèvement de scénario ou les événements d’échec peuvent être regroupés sous des mots clés séparés afin que vous puissiez filtrer facilement ces événements.


```C++
void TraceLoggingSample::CombineKeywords()
{
    /*
    Keywords can be combined using multiple TraceLoggingKeyword() macros ...
    */

    #define MY_PROVIDER_KEYWORD_BLUE    0x1
    #define MY_PROVIDER_KEYWORD_YELLOW  0x2
    #define MY_PROVIDER_KEYWORD_GREEN   (MY_PROVIDER_KEYWORD_BLUE | MY_PROVIDER_KEYWORD_YELLOW) 

    PCWSTR Status = L"Feeling a bit green";

    /*
    These events are equivalent...
    */

    TraceLoggingWrite(
        g_hProvider,
        "Keywords",
        TraceLoggingKeyword(MY_PROVIDER_KEYWORD_GREEN),
        TraceLoggingValue(Status, "Current Status")
        );

    TraceLoggingWrite(
        g_hProvider,
        "Keywords",
        TraceLoggingKeyword(MY_PROVIDER_KEYWORD_BLUE | MY_PROVIDER_KEYWORD_YELLOW),
        TraceLoggingValue(Status, "Current Status")
        );

    TraceLoggingWrite(
        g_hProvider,
        "Keywords",
        TraceLoggingKeyword(MY_PROVIDER_KEYWORD_BLUE),
        TraceLoggingKeyword(MY_PROVIDER_KEYWORD_YELLOW),
        TraceLoggingValue(Status, "Current Status")
        );
}
```



### <a name="log-array-event-data"></a>Données d’événement de tableau de journaux

Cet exemple montre comment enregistrer des tableaux en tant que données d’événement.


```C++
void TraceLoggingSample::Arrays()
{
    INT32 IntValsFixed[5] = {20, 21, 22, 23, 24};
    UINT cIntVals = 5;
    INT32* IntValsVar = new INT32[cIntVals];

    VERIFY_IS_NOT_NULL(IntValsVar);
    memcpy(IntValsVar, IntValsFixed, sizeof(IntValsFixed));


    /*
    Variable size arrays
    */

    TraceLoggingWrite(
        g_hMyComponentProvider,
        "Variable Size Arrays",
        TraceLoggingInt32Array(IntValsVar, (UINT16)cIntVals, "Variable size int array"), 
        TraceLoggingInt32Array(IntValsVar, 5, "Variable size int array")  
        );


    /*
    Fixed size arrays

    Fixed size array macros use the "FixedArray" suffix.
    The absence of the suffix indicates a variable sized array.
    */

    TraceLoggingWrite(
        g_hMyComponentProvider,
        "Constant Size Arrays", 
        TraceLoggingInt32FixedArray(IntValsFixed, _countof(IntValsFixed), "Constant size int array")      
        );

    delete [] IntValsVar;
}
```



### <a name="log-structure-event-data"></a>Données d’événement de structure de journal

Cet exemple montre comment enregistrer des données d’événement de structure.


```C++
void TraceLoggingSample::Structs()
{
    WIN32_FIND_DATA FindData;
    HANDLE hFind = FindFirstFile(".", &FindData);

    VERIFY_IS_TRUE(hFind != INVALID_HANDLE_VALUE);

    /*
    TraceLoggingStruct defines a group of related fields in an event.
    The first parameter, which must be a compile-time constant, indicates
    the number of subsequent fields that are to be considered part of the 
    struct.
    */

    TraceLoggingWrite(
        g_hMyComponentProvider,
        "FindFirstFile",
        TraceLoggingStruct(5, "FileData"),                           
            TraceLoggingString(FindData.cFileName, "Name"),   
            TraceLoggingUInt32(FindData.dwFileAttributes, "Attributes"),              
            TraceLoggingFileTime(FindData.ftCreationTime, "CreateTime"),              
            TraceLoggingUInt32(FindData.nFileSizeHigh, "SizeHigh"),              
            TraceLoggingUInt32(FindData.nFileSizeLow, "SizeLow"),
        TraceLoggingPointer(hFind, "Result")
        );

    /*
    ... or ...
    */

#define LogWin32FindData(fd) \
    TraceLoggingStruct(5, "FileData"), \
    TraceLoggingString(((fd).cFileName), "Name"), \
    TraceLoggingUInt32(((fd).dwFileAttributes), "Attributes"), \
    TraceLoggingFileTime(((fd).ftCreationTime), "CreateTime"), \
    TraceLoggingUInt32(((fd).nFileSizeHigh), "SizeHigh"), \
    TraceLoggingUInt32(((fd).nFileSizeLow), "SizeLow")

    TraceLoggingWrite(
        g_hMyComponentProvider,
        "FindFirstFile",
        LogWin32FindData(FindData),
        TraceLoggingPointer(hFind, "Result")
        );

    FindClose(hFind);
}
```



### <a name="how-to-fix-tracelogging-cc-build-errors"></a>Comment corriger les erreurs de build TraceLogging C/C++

Erreur de build

``` syntax
Linker error:
Error   2       error LNK2001: unresolved external symbol __imp__EventSetInformation@20 App.xaml.obj    PrintPreview
Error   3       error LNK2001: unresolved external symbol __imp__EventRegister@16       App.xaml.obj    PrintPreview
```

Correction

Corrigez cette erreur en liant advapi32. lib dans votre projet.

 

 




