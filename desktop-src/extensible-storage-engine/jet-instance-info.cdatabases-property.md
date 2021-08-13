---
description: 'En savoir plus sur : propriété JET_INSTANCE_INFO. cDatabases'
title: JET_INSTANCE_INFO. cDatabases, propriété
TOCTitle: 'cDatabases property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.cDatabases
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_instance_info.cdatabases(v=EXCHG.10)
ms:contentKeyID: 55103699
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.cDatabases
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.set_cDatabases
- Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.get_cDatabases
- Microsoft.Isam.Esent.Interop.JET_INSTANCE_INFO.cDatabases
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: fd24092d039bc7cfc1c32a48068e1a5e3694c57dc42e7754998d06abe298cc14
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118765708"
---
# <a name="jet_instance_infocdatabases-property"></a>JET_INSTANCE_INFO. cDatabases, propriété

Obtient le nombre de bases de données attachées à l’instance de base de données.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Property cDatabases As Integer
    Get
    Private Set
'Usage
Dim instance As JET_INSTANCE_INFO
Dim value As Integer

value = instance.cDatabases
```

``` csharp
public int cDatabases { get; private set; }
```

#### <a name="property-value"></a>Valeur de la propriété

Type : [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe JET_INSTANCE_INFO](./jet-instance-info-class.md)

[Membres JET_INSTANCE_INFO](./jet-instance-info-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
