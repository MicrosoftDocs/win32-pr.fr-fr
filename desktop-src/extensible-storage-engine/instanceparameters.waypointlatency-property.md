---
description: 'En savoir plus sur : InstanceParameters. WaypointLatency, propriété'
title: InstanceParameters. WaypointLatency, propriété
TOCTitle: 'WaypointLatency property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.WaypointLatency
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.waypointlatency(v=EXCHG.10)
ms:contentKeyID: 55103325
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.WaypointLatency
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_WaypointLatency
- Microsoft.Isam.Esent.Interop.InstanceParameters.WaypointLatency
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_WaypointLatency
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b0e52100247a438d442d134bc3f31313b7da72df04591c44b1e6d70e159d0b7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118076642"
---
# <a name="instanceparameterswaypointlatency-property"></a>InstanceParameters. WaypointLatency, propriété

Obtient ou définit le nombre de journaux pour lesquels esent diffère le vidage de base de données. Cela peut être utilisé pour augmenter la capacité de récupération de base de données en cas de perte de fichiers journaux. pris en charge sur Windows 7 et les autres. ignoré sur Windows XP, Windows server 2003, Windows Vista et Windows server 2008.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Property WaypointLatency As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.WaypointLatency

instance.WaypointLatency = value
```

``` csharp
public int WaypointLatency { get; set; }
```

#### <a name="property-value"></a>Valeur de la propriété

Type : [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[InstanceParameters, classe](./instanceparameters-class.md)

[Membres InstanceParameters](./instanceparameters-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
