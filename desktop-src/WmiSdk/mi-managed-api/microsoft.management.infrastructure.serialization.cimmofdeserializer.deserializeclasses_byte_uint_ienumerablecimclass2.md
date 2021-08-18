---
description: 'En savoir plus sur : méthode CimMofDeserializer. DeserializeClasses (Byte [], UInt32, IEnumerable <CimClass> , OnClassNeeded, GetIncludedFileContent)'
title: Méthode CimMofDeserializer. DeserializeClasses (Byte [], UInt32, IEnumerable (CimClass), OnClassNeeded, GetIncludedFileContent) (Microsoft. Management. infrastructure. Serialization)
TOCTitle: CimMofDeserializer.DeserializeClasses method (Byte[], UInt32, IEnumerable(CimClass), OnClassNeeded, GetIncludedFileContent) (Microsoft.Management.Infrastructure.Serialization)
ms:assetid: M:Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeClasses(System.Byte[],System.UInt32@,System.Collections.Generic.IEnumerable{Microsoft.Management.Infrastructure.CimClass},Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.OnClassNeeded,Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.GetIncludedFileContent)
ms.date: 11/14/2019
mtps_version: v=VS.85
dev_langs:
- csharp
- c++
- fsharp
- vb
api_location:
- Microsoft.Management.Infrastructure.dll
api_name:
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeClasses
api_type:
- Assembly
topic_type:
- apiref
product_family_name: VS
ms.topic: reference
ms.openlocfilehash: 7c09374b19c6e845dbac674b3b8c3e694ae9513c290acb90e1f8a7d5974dab49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119131091"
---
# <a name="cimmofdeserializerdeserializeclasses-method-byteuint32ienumerablecimclass-onclassneeded-getincludedfilecontent"></a>Méthode CimMofDeserializer. DeserializeClasses (Byte \[ \] , UInt32, IEnumerable \<CimClass\> , OnClassNeeded, GetIncludedFileContent)

Désérialise les classes CIM en fonction des données sérialisées, d’une collection de classes CIM parentes et de rappels.

**Espace de noms :**   [Microsoft. Management. infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))  
**Assembly :**  Microsoft. Management. infrastructure (en Microsoft.Management.Infrastructure.dll)  

## <a name="syntax"></a>Syntaxe

``` csharp
public IEnumerable<CimClass> DeserializeClasses(
    byte[] serializedData,
    ref uint offset,
    IEnumerable<CimClass> classes,
    OnClassNeeded onClassNeededCallback,
    GetIncludedFileContent getIncludedFileCallback
)
```

``` c++
public:
IEnumerable<CimClass^>^ DeserializeClasses(
    array<unsigned char>^ serializedData,
    unsigned int% offset,
    IEnumerable<CimClass^>^ classes,
    OnClassNeeded^ onClassNeededCallback,
    GetIncludedFileContent^ getIncludedFileCallback
)
```

``` fsharp
member DeserializeClasses : 
        serializedData:byte[] *
        offset:uint32 byref *
        classes:IEnumerable<CimClass> *
        onClassNeededCallback:OnClassNeeded *
        getIncludedFileCallback:GetIncludedFileContent -> IEnumerable<CimClass>
```

``` vb
Public Function DeserializeClasses (
    serializedData As Byte(),
    ByRef offset As UInteger,
    classes As IEnumerable(Of CimClass),
    onClassNeededCallback As OnClassNeeded,
    getIncludedFileCallback As GetIncludedFileContent
) As IEnumerable(CimClass)
```

#### <a name="parameters"></a>Paramètres

  - serializedData  
    Type : [System. Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]
    
    Mémoire tampon qui contient les données sérialisées.

<!-- end list -->

  - offset  
    Type : [System. UInt32](/dotnet/api/system.uint32?view=netframework-4.8)
    
    Offset d’octet à l’emplacement où commencer la lecture des données. Lorsque la méthode est retournée, le décalage pointe vers l’octet suivant après les classes désérialisées.

<!-- end list -->

  - Classes  
    Type : [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\>
    
    Cache facultatif de classes CIM parentes.

<!-- end list -->

  - onClassNeededCallback  
    Type : [OnClassNeeded](microsoft.management.infrastructure.serialization.cimmofdeserializer.onclassneeded.md)
    
    Fonction de rappel utilisée pour fournir un objet de classe demandé pendant la désérialisation.

<!-- end list -->

  - getIncludedFileCallback  
    Type : [GetIncludedFileContent](microsoft.management.infrastructure.serialization.cimmofdeserializer.getincludedfilecontent.md)
    
    Fonction de rappel utilisée pour fournir le contenu de la mémoire tampon d’un fichier spécifié.

#### <a name="return-value"></a>Valeur retournée

Type : [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimClass](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))\>

Interface [IEnumerable \<T\> ](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) qui peut être utilisée pour énumérer les classes CIM.

## <a name="see-also"></a>Voir aussi

[CimClass, classe](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832269(v=vs.85))  
[Espace de noms Microsoft. Management. infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))
