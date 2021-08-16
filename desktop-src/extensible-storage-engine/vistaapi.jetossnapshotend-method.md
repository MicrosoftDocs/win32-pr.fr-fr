---
description: 'En savoir plus sur : méthode VistaApi. JetOSSnapshotEnd'
title: Méthode VistaApi. JetOSSnapshotEnd (Microsoft. ISAM. esent. Interop. Vista)
TOCTitle: 'JetOSSnapshotEnd method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotEnd(Microsoft.Isam.Esent.Interop.JET_OSSNAPID,Microsoft.Isam.Esent.Interop.Vista.SnapshotEndGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaapi.jetossnapshotend(v=EXCHG.10)
ms:contentKeyID: 55104196
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotEnd
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaApi.JetOSSnapshotEnd
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f8aa385dbba241a631bc7bc29c5ca7905c4a609f6eb2231a984b4c0e9d1db8eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119106816"
---
# <a name="vistaapijetossnapshotend-method"></a>Méthode VistaApi. JetOSSnapshotEnd

Notifie le moteur que la session d’instantané s’est terminée.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Shared Sub JetOSSnapshotEnd ( _
    snapshot As JET_OSSNAPID, _
    grbit As SnapshotEndGrbit _
)
'Usage
Dim snapshot As JET_OSSNAPID
Dim grbit As SnapshotEndGrbitVistaApi.JetOSSnapshotEnd(snapshot, _
    grbit)
```

``` csharp
public static void JetOSSnapshotEnd(
    JET_OSSNAPID snapshot,
    SnapshotEndGrbit grbit
)
```

#### <a name="parameters"></a>Paramètres

  - instantané  
    Type : [Microsoft.ISAM.esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)  
    
    Identificateur de la session d’instantané.

<!-- end list -->

  - grbit  
    Type : [Microsoft. ISAM. esent. Interop. Vista. SnapshotEndGrbit](./snapshotendgrbit-enumeration.md)  
    
    Options de fin d’instantané.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[VistaApi, classe](./vistaapi-class.md)

[Membres VistaApi](./vistaapi-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)
