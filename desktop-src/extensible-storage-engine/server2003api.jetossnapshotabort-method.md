---
description: 'En savoir plus sur : méthode Server2003Api. JetOSSnapshotAbort'
title: Méthode Server2003Api. JetOSSnapshotAbort (Microsoft. ISAM. esent. Interop. Server2003)
TOCTitle: 'JetOSSnapshotAbort method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetOSSnapshotAbort(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,Microsoft.Isam.Esent.Interop.Server2003.SnapshotAbortGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.server2003.server2003api.jetossnapshotabort(v=EXCHG.10)
ms:contentKeyID: 55104209
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetOSSnapshotAbort
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Server2003.Server2003Api.JetOSSnapshotAbort
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 6ca7633ce07468c7c516988e7e048b6c9673bc3ed685bbee35a4f5f094a59db3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119780219"
---
# <a name="server2003apijetossnapshotabort-method"></a>Méthode Server2003Api. JetOSSnapshotAbort

Notifie le moteur qu’il peut reprendre des opérations d’e/s normales après la fin d’une période de blocage avec un instantané ayant échoué.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Shared Sub JetOSSnapshotAbort ( _
    snapid As JET_OSSNAPID, _
    grbit As SnapshotAbortGrbit _
)
'Usage
Dim snapid As JET_OSSNAPID
Dim grbit As SnapshotAbortGrbitServer2003Api.JetOSSnapshotAbort(snapid, _
    grbit)
```

``` csharp
public static void JetOSSnapshotAbort(
    JET_OSSNAPID snapid,
    SnapshotAbortGrbit grbit
)
```

#### <a name="parameters"></a>Paramètres

  - snapid  
    Type : [Microsoft.ISAM.esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)  
    
    Identificateur de la session d’instantané.

<!-- end list -->

  - grbit  
    Type : [Microsoft. ISAM. esent. Interop. Server2003. SnapshotAbortGrbit](./snapshotabortgrbit-enumeration.md)  
    
    Options pour cet appel.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Server2003Api, classe](./server2003api-class.md)

[Membres Server2003Api](./server2003api-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop. Server2003](./microsoft.isam.esent.interop.server2003-namespace.md)
