---
description: 'En savoir plus sur : structure JET_BKLOGTIME'
title: Structure JET_BKLOGTIME
TOCTitle: JET_BKLOGTIME structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_BKLOGTIME
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_bklogtime(v=EXCHG.10)
ms:contentKeyID: 39512194
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_BKLOGTIME
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_BKLOGTIME
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b718254082095592f097097500d2690be320dd63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114070"
---
# <a name="jet_bklogtime-structure"></a>Structure JET_BKLOGTIME

Décrit une date/heure à laquelle une sauvegarde s’est produite.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
<SerializableAttribute> _
Public Structure JET_BKLOGTIME _
    Implements IEquatable(Of JET_BKLOGTIME), IJET_LOGTIME,  _
    INullableJetStruct
'Usage
Dim instance As JET_BKLOGTIME
```

``` csharp
[SerializableAttribute]
public struct JET_BKLOGTIME : IEquatable<JET_BKLOGTIME>, 
    IJET_LOGTIME, INullableJetStruct
```

## <a name="thread-safety"></a>Sécurité des threads

Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe. Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Membres JET_BKLOGTIME](./jet-bklogtime-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
