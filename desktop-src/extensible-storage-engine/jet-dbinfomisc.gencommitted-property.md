---
description: 'En savoir plus sur : propriété JET_DBINFOMISC. genCommitted'
title: JET_DBINFOMISC. genCommitted, propriété
TOCTitle: 'genCommitted property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.genCommitted
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfomisc.gencommitted(v=EXCHG.10)
ms:contentKeyID: 39513072
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.genCommitted
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.genCommitted
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.get_genCommitted
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.set_genCommitted
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: a40612c535bed3bbfe345add1fd922b65e450fd7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526097"
---
# <a name="jet_dbinfomiscgencommitted-property"></a>JET_DBINFOMISC. genCommitted, propriété

Obtient la génération de journal maximale validée dans la base de données. En général, génération de journal en cours.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Property genCommitted As Integer
    Get
    Friend Set
'Usage
Dim instance As JET_DBINFOMISC
Dim value As Integer

value = instance.genCommitted
```

``` csharp
public int genCommitted { get; internal set; }
```

#### <a name="property-value"></a>Valeur de la propriété

Type : [System. Int32](/dotnet/api/system.int32)  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe JET_DBINFOMISC](./jet-dbinfomisc-class.md)

[Membres JET_DBINFOMISC](./jet-dbinfomisc-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
