---
description: 'En savoir plus sur : propriété InstanceParameters. MaxSessions'
title: InstanceParameters. MaxSessions, propriété
TOCTitle: 'MaxSessions property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.MaxSessions
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.maxsessions(v=EXCHG.10)
ms:contentKeyID: 55103557
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxSessions
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.MaxSessions
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_MaxSessions
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_MaxSessions
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2294a8de2e3603a638607efad5baaa6af6c1ec17
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126914668"
---
# <a name="instanceparametersmaxsessions-property"></a>InstanceParameters. MaxSessions, propriété

Obtient ou définit le nombre de ressources de sessions réservées pour cette instance. Une ressource de session correspond directement à un JET_SESID.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Property MaxSessions As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.MaxSessions

instance.MaxSessions = value
```

``` csharp
public int MaxSessions { get; set; }
```

#### <a name="property-value"></a>Valeur de la propriété

Type : [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[InstanceParameters, classe](./instanceparameters-class.md)

[Membres InstanceParameters](./instanceparameters-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
