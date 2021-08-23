---
description: 'En savoir plus sur : InstanceParameters. EnableIndexChecking, propriété'
title: InstanceParameters. EnableIndexChecking, propriété
TOCTitle: 'EnableIndexChecking property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.EnableIndexChecking
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.enableindexchecking(v=EXCHG.10)
ms:contentKeyID: 55103567
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.EnableIndexChecking
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_EnableIndexChecking
- Microsoft.Isam.Esent.Interop.InstanceParameters.EnableIndexChecking
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_EnableIndexChecking
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0f48e4058741ab69677d62f7441cb6181e0783900d69eaff9cec73aa6bb46eb7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119834368"
---
# <a name="instanceparametersenableindexchecking-property"></a>InstanceParameters. EnableIndexChecking, propriété

Obtient ou définit une valeur indiquant si [JetAttachDatabase (JET_SESID, String, AttachDatabaseGrbit)](./api.jetattachdatabase-method.md) doit vérifier les index qui ont été générés à l’aide d’une version antérieure de la bibliothèque NLS dans le système d’exploitation.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Property EnableIndexChecking As Boolean
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Boolean

value = instance.EnableIndexChecking

instance.EnableIndexChecking = value
```

``` csharp
public bool EnableIndexChecking { get; set; }
```

#### <a name="property-value"></a>Valeur de la propriété

Type : [System. Boolean](/dotnet/api/system.boolean)  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[InstanceParameters, classe](./instanceparameters-class.md)

[Membres InstanceParameters](./instanceparameters-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
