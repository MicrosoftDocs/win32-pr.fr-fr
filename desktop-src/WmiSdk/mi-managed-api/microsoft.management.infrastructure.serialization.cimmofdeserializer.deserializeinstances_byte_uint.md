---
description: 'En savoir plus sur : méthode CimMofDeserializer. DeserializeInstances (Byte [], UInt32)'
title: Méthode CimMofDeserializer. DeserializeInstances (Byte [], UInt32) (Microsoft. Management. infrastructure. Serialization)
TOCTitle: CimMofDeserializer.DeserializeInstances method (Byte[], UInt32) (Microsoft.Management.Infrastructure.Serialization)
ms:assetid: M:Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeInstances(System.Byte[],System.UInt32@)
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
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.DeserializeInstances
api_type:
- Assembly
topic_type:
- apiref
product_family_name: VS
ms.topic: reference
ms.openlocfilehash: c44270429dc81c64d26b5e2512686bde97ac7851235eab01ebd545aae762e0ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118317328"
---
# <a name="cimmofdeserializerdeserializeinstances-method-byteuint32"></a>Méthode CimMofDeserializer. DeserializeInstances (Byte \[ \] , UInt32)

Désérialise les instances CIM en fonction des données sérialisées.

**Espace de noms :**   [Microsoft. Management. infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))  
**Assembly :**  Microsoft. Management. infrastructure (en Microsoft.Management.Infrastructure.dll)  

## <a name="syntax"></a>Syntaxe

``` csharp
public IEnumerable<CimInstance> DeserializeInstances(
    byte[] serializedData,
    ref uint offset
)
```

``` c++
public:
IEnumerable<CimInstance^>^ DeserializeInstances(
    array<unsigned char>^ serializedData,
    unsigned int% offset
)
```

``` fsharp
member DeserializeInstances : 
        serializedData:byte[] *
        offset:uint32 byref -> IEnumerable<CimInstance>
```

``` vb
Public Function DeserializeInstances (
    serializedData As Byte(),
    ByRef offset As UInteger
) As IEnumerable(CimInstance)
```

#### <a name="parameters"></a>Paramètres

  - serializedData  
    Type : [System. Byte](/dotnet/api/system.byte?view=netframework-4.8)\[\]
    
    Mémoire tampon qui contient les données sérialisées.

<!-- end list -->

  - offset  
    Type : [System. UInt32](/dotnet/api/system.uint32?view=netframework-4.8)
    
    Offset d’octet à l’emplacement où commencer la lecture des données. Lorsque la méthode est retournée, le décalage pointe vers l’octet suivant après les instances désérialisées.

#### <a name="return-value"></a>Valeur retournée

Type : [System. Collections. Generic. IEnumerable](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8)\<[CimInstance](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))\>

Interface [IEnumerable \<T\> ](/dotnet/api/system.collections.generic.ienumerable-1?view=netframework-4.8) qui peut être utilisée pour énumérer les classes CIM.

## <a name="see-also"></a>Voir aussi

[CimInstance, classe](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336(v=vs.85))  
[Espace de noms Microsoft. Management. infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))
