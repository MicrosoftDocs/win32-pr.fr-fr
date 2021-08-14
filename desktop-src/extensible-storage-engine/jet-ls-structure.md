---
description: 'En savoir plus sur : structure JET_LS'
title: Structure JET_LS
TOCTitle: JET_LS structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_LS
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_ls(v=EXCHG.10)
ms:contentKeyID: 39510760
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_LS
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_LS
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 1fa85ea0f3117d6f4f9c0c9102f21f2fb1f626f8c115144998c1a4c94c300626
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118765085"
---
# <a name="jet_ls-structure"></a>Structure JET_LS

Stockage local pour un handle ESENT. Utilisé par [JetGetLS (JET_SESID, JET_TABLEID, JET_LS, LsGrbit)](./api.jetgetls-method.md) et [JetSetLS (JET_SESID, JET_TABLEID, JET_LS, LsGrbit)](./api.jetsetls-method.md).

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Structure JET_LS _
    Implements IEquatable(Of JET_LS), IFormattable
'Usage
Dim instance As JET_LS
```

``` csharp
public struct JET_LS : IEquatable<JET_LS>, 
    IFormattable
```

## <a name="thread-safety"></a>Sécurité des threads

Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe. Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Membres JET_LS](./jet-ls-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
