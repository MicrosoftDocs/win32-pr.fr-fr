---
description: 'En savoir plus sur : structure JET_DBID'
title: Structure JET_DBID
TOCTitle: JET_DBID structure
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_DBID
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_dbid(v=EXCHG.10)
ms:contentKeyID: 39515255
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_DBID
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_DBID
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bc26dc58eb4377b24af36f830b96bc3f146237c1b0f419901d7eb106de84a3ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119112258"
---
# <a name="jet_dbid-structure"></a>Structure JET_DBID

Un JET_DBID contient le descripteur de la base de données. Un descripteur de base de données est utilisé pour gérer le schéma d’une base de données. Il peut également être utilisé pour gérer les tables à l’intérieur de cette base de données.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Structure JET_DBID _
    Implements IEquatable(Of JET_DBID), IFormattable
'Usage
Dim instance As JET_DBID
```

``` csharp
public struct JET_DBID : IEquatable<JET_DBID>, 
    IFormattable
```

## <a name="thread-safety"></a>Sécurité des threads

Tout membre statique public (Shared en Visual Basic) de ce type est thread-safe. Tous les membres de l'instance ne sont pas garantis comme étant thread-safe.

## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Membres JET_DBID](./jet-dbid-members.md)

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
