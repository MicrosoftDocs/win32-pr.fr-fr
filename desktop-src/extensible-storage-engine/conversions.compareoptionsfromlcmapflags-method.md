---
description: 'En savoir plus sur : conversions. CompareOptionsFromLCMapFlags, méthode'
title: Conversions. CompareOptionsFromLCMapFlags, méthode
TOCTitle: 'CompareOptionsFromLCMapFlags method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Conversions.CompareOptionsFromLCMapFlags(System.UInt32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.conversions.compareoptionsfromlcmapflags(v=EXCHG.10)
ms:contentKeyID: 55100975
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Conversions.CompareOptionsFromLCMapFlags
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Conversions.CompareOptionsFromLCMapFlags
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bfe3a65c52d23ee335a81560775f0063b8ca81a10cc43c1787e353a5b803eed4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117901845"
---
# <a name="conversionscompareoptionsfromlcmapflags-method"></a>Conversions. CompareOptionsFromLCMapFlags, méthode

Les indicateurs fournis pour LCMapFlags, les transforment en options de comparaison. Les options inconnues sont ignorées.

Cette API n’est pas conforme CLS. 

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Function CompareOptionsFromLCMapFlags ( _
    lcmapFlags As UInteger _
) As CompareOptions
'Usage
Dim lcmapFlags As UInteger
Dim returnValue As CompareOptions

returnValue = Conversions.CompareOptionsFromLCMapFlags(lcmapFlags)
```

``` csharp
[CLSCompliantAttribute(false)]
public static CompareOptions CompareOptionsFromLCMapFlags(
    uint lcmapFlags
)
```

#### <a name="parameters"></a>Paramètres

  - lcmapFlags  
    Type : [System. UInt32](/dotnet/api/system.uint32)  
    
    Indicateurs LCMapString.

#### <a name="return-value"></a>Valeur retournée

Type : [System. Globalization. CompareOptions](/dotnet/api/system.globalization.compareoptions)  
CompareOptions décrivant les indicateurs (connus).  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Conversions (classe)](./conversions-class.md)

[Conversions, membres](./conversions-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
