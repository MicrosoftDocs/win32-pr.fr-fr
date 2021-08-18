---
description: 'En savoir plus sur : structure JET_RECSIZE'
title: Structure de JET_RECSIZE (Microsoft. ISAM. esent. Interop. Vista)
TOCTitle: JET_RECSIZE structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.jet_recsize(v=EXCHG.10)
ms:contentKeyID: 39509765
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.JET_RECSIZE
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 58ac34dd551b38dc6179bbe1448d0b96e09073fff4ce716ac6efaf74037c0f3e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119107455"
---
# <a name="jet_recsize-structure"></a>Structure JET_RECSIZE

Utilisé par [JetGetRecordSize (JET_SESID, JET_TABLEID, JET_RECSIZE, GetRecordSizeGrbit)](./vistaapi.jetgetrecordsize-method.md) pour retourner des informations sur les exigences d’utilisation d’un enregistrement dans l’espace de données utilisateur, le nombre de colonnes définies, le nombre de valeurs et l’espace de charge de structure d’enregistrement esent.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
<SerializableAttribute> _
Public Structure JET_RECSIZE _
    Implements IEquatable(Of JET_RECSIZE)
'Usage
Dim instance As JET_RECSIZE
```

``` csharp
[SerializableAttribute]
public struct JET_RECSIZE : IEquatable<JET_RECSIZE>
```

## <a name="thread-safety"></a>Sécurité des threads

Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe. Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Membres JET_RECSIZE](./jet-recsize-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop. Vista](./microsoft.isam.esent.interop.vista-namespace.md)
