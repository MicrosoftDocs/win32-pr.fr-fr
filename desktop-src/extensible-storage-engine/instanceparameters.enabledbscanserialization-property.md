---
description: 'En savoir plus sur : InstanceParameters. EnableDBScanSerialization, propriété'
title: InstanceParameters. EnableDBScanSerialization, propriété
TOCTitle: 'EnableDBScanSerialization property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.EnableDBScanSerialization
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.enabledbscanserialization(v=EXCHG.10)
ms:contentKeyID: 55103555
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.EnableDBScanSerialization
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_EnableDBScanSerialization
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_EnableDBScanSerialization
- Microsoft.Isam.Esent.Interop.InstanceParameters.EnableDBScanSerialization
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c514218b43d1f291abc01d384cdb47f339163cc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318749"
---
# <a name="instanceparametersenabledbscanserialization-property"></a>InstanceParameters. EnableDBScanSerialization, propriété

Obtient ou définit une valeur indiquant si la sérialisation de la maintenance de la base de données est activée pour les bases de données qui partagent le même disque.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Property EnableDBScanSerialization As Boolean
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Boolean

value = instance.EnableDBScanSerialization

instance.EnableDBScanSerialization = value
```

``` csharp
public bool EnableDBScanSerialization { get; set; }
```

#### <a name="property-value"></a>Valeur de la propriété

Type : [System. Boolean](/dotnet/api/system.boolean)  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[InstanceParameters, classe](./instanceparameters-class.md)

[Membres InstanceParameters](./instanceparameters-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
