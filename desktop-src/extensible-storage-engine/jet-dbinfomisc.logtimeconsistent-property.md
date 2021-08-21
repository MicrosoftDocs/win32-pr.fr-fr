---
description: 'En savoir plus sur : propriété JET_DBINFOMISC. logtimeConsistent'
title: JET_DBINFOMISC. logtimeConsistent, propriété
TOCTitle: 'logtimeConsistent property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.logtimeConsistent
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbinfomisc.logtimeconsistent(v=EXCHG.10)
ms:contentKeyID: 39513228
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.logtimeConsistent
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.logtimeConsistent
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.get_logtimeConsistent
- Microsoft.Isam.Esent.Interop.JET_DBINFOMISC.set_logtimeConsistent
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c7f8a8db663dca151d1d2e8e46512ee44fe97074f906ae657af3e1fa2803bbda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118486211"
---
# <a name="jet_dbinfomisclogtimeconsistent-property"></a>JET_DBINFOMISC. logtimeConsistent, propriété

Obtient l’heure à laquelle la base de données a été rendue cohérente. Cette valeur est null si la base de données est incohérente.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Property logtimeConsistent As JET_LOGTIME
    Get
    Friend Set
'Usage
Dim instance As JET_DBINFOMISC
Dim value As JET_LOGTIME

value = instance.logtimeConsistent
```

``` csharp
public JET_LOGTIME logtimeConsistent { get; internal set; }
```

#### <a name="property-value"></a>Valeur de la propriété

Type : [Microsoft.ISAM.esent.Interop.JET_LOGTIME](./jet-logtime-structure2.md)  

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe JET_DBINFOMISC](./jet-dbinfomisc-class.md)

[Membres JET_DBINFOMISC](./jet-dbinfomisc-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
