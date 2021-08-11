---
description: 'En savoir plus sur : structure JET_SIGNATURE'
title: Structure JET_SIGNATURE
TOCTitle: JET_SIGNATURE structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_SIGNATURE
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_signature(v=EXCHG.10)
ms:contentKeyID: 39511048
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_SIGNATURE
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_SIGNATURE
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e0f9c6508f3901d9755b3a244f88eb948959164918278f067ee6f6d25fefd3e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118253413"
---
# <a name="jet_signature-structure"></a>Structure JET_SIGNATURE

La structure JET_SIGNATURE contient des informations qui identifient de façon unique une séquence de base de données ou de fichier journal.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
<SerializableAttribute> _
Public Structure JET_SIGNATURE _
    Implements IEquatable(Of JET_SIGNATURE)
'Usage
Dim instance As JET_SIGNATURE
```

``` csharp
[SerializableAttribute]
public struct JET_SIGNATURE : IEquatable<JET_SIGNATURE>
```

## <a name="thread-safety"></a>Sécurité des threads

Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe. Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Membres JET_SIGNATURE](./jet-signature-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
