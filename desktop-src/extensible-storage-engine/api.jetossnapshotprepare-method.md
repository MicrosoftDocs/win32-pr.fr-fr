---
description: 'En savoir plus sur : méthode API. JetOSSnapshotPrepare'
title: API. JetOSSnapshotPrepare, méthode
TOCTitle: 'JetOSSnapshotPrepare method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotPrepare(Microsoft.Isam.Esent.Interop.JET_OSSNAPID@,Microsoft.Isam.Esent.Interop.SnapshotPrepareGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetossnapshotprepare(v=EXCHG.10)
ms:contentKeyID: 55100779
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotPrepare
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetOSSnapshotPrepare
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d6e863c13ee46267e18133afc825e9362acfe44d58b64b22bc5105ab8c164bfe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117902959"
---
# <a name="apijetossnapshotprepare-method"></a>API. JetOSSnapshotPrepare, méthode

Commence les préparations pour une session d’instantané. Une session d’instantané est un intervalle de temps dans lequel le moteur n’émet pas d’e/s d’écriture sur le disque, de sorte que le moteur peut participer à une session d’instantané de volume (lorsqu’il est piloté par un enregistreur d’instantané).

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Shared Sub JetOSSnapshotPrepare ( _
    <OutAttribute> ByRef snapshot As JET_OSSNAPID, _
    grbit As SnapshotPrepareGrbit _
)
'Usage
Dim snapshot As JET_OSSNAPID
Dim grbit As SnapshotPrepareGrbitApi.JetOSSnapshotPrepare(snapshot, _
    grbit)
```

``` csharp
public static void JetOSSnapshotPrepare(
    out JET_OSSNAPID snapshot,
    SnapshotPrepareGrbit grbit
)
```

#### <a name="parameters"></a>Paramètres

  - instantané  
    Type : [Microsoft.ISAM.esent.Interop.JET_OSSNAPID](./jet-ossnapid-structure.md)  
    
    Retourne l’ID de la session d’instantané.

<!-- end list -->

  - grbit  
    Type : [Microsoft. ISAM. esent. Interop. SnapshotPrepareGrbit](./snapshotpreparegrbit-enumeration.md)  
    
    Options d’instantané.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Classe d’API](./api-class.md)

[Membres d’API](./api-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
