---
description: 'En savoir plus sur : méthode CimMofDeserializer. Create (String, UInt32)'
title: CimMofDeserializer.Create, méthode (String, UInt32) (Microsoft.Management.Infrastructure.Serialization)
TOCTitle: CimMofDeserializer.Create method (String, UInt32) (Microsoft.Management.Infrastructure.Serialization)
ms:assetid: M:Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.Create(System.String,System.UInt32)
ms.date: 11/13/2019
mtps_version: v=VS.85
f1_keywords:
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.Create
- Microsoft::Management::Infrastructure::.Serialization::CimMofDeserializer::Create
dev_langs:
- CSharp
- C++
- VB
- FSharp
api_location:
- Microsoft.Management.Infrastructure.dll
api_name:
- Microsoft.Management.Infrastructure.Serialization.CimMofDeserializer.Create
api_type:
- Assembly
topic_type:
- apiref
product_family_name: VS
ms.topic: reference
ms.openlocfilehash: e8a89c628abcc9fa9b8ac54d75493c8a385ef64bddd257bd3dc193b7e04c71aa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050667"
---
# <a name="cimmofdeserializercreate-method-string-uint32"></a>CimMofDeserializer. Create, méthode (String, UInt32)

Crée et initialise un désérialiseur personnalisé, selon le format et les indicateurs spécifiés.

**Espace de noms :**   [Microsoft. Management. infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))  
**Assembly :**  Microsoft. Management. infrastructure (en Microsoft.Management.Infrastructure.dll)  

## <a name="syntax"></a>Syntaxe

``` csharp
public static CimMofDeserializer Create(
    string format,
    uint flags
)
```

``` c++
public:
static CimMofDeserializer^ Create(
    String^ format,
    unsigned int flags
)
```

``` fsharp
static member Create : 
        format:string *
        flags:uint32 -> CimMofDeserializer
```

``` vb
Public Shared Function Create (
    format As String,
    flags As UInteger
) As CimMofDeserializer
```

#### <a name="parameters"></a>Paramètres

  - format  
    Type : [System. String](/dotnet/api/system.string?view=netframework-4.8)
    
    Format de sérialisation. Seul « MI_XML » est pris en charge.

<!-- end list -->

  - flags  
    Type : [System. UInt32](/dotnet/api/system.uint32?view=netframework-4.8)
    
    Indicateurs de sérialisation. Doit être égal à 0.

#### <a name="return-value"></a>Valeur retournée

Type : [Microsoft. Management. infrastructure. Serialization. CimMofDeserializer](microsoft.management.infrastructure.serialization.cimmofdeserializer.md)

Objet de désérialiseur nouvellement créé.

## <a name="see-also"></a>Voir aussi

[CimMofDeserializer, classe](microsoft.management.infrastructure.serialization.cimmofdeserializer.md) 
 [Espace de noms Microsoft. Management. infrastructure. Serialization](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832966(v=vs.85))
