---
description: 'En savoir plus sur : énumération JET_prep'
title: Énumération JET_prep
TOCTitle: JET_prep enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.JET_prep
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.jet_prep(v=EXCHG.10)
ms:contentKeyID: 39510193
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.JET_prep.Replace
- Microsoft.Isam.Esent.Interop.JET_prep.InsertCopy
- Microsoft.Isam.Esent.Interop.JET_prep.Cancel
- Microsoft.Isam.Esent.Interop.JET_prep.Insert
- Microsoft.Isam.Esent.Interop.JET_prep.InsertCopyDeleteOriginal
- Microsoft.Isam.Esent.Interop.JET_prep
- Microsoft.Isam.Esent.Interop.JET_prep.ReplaceNoLock
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.JET_prep.InsertCopyDeleteOriginal
- Microsoft.Isam.Esent.Interop.JET_prep.ReplaceNoLock
- Microsoft.Isam.Esent.Interop.JET_prep
- Microsoft.Isam.Esent.Interop.JET_prep.Cancel
- Microsoft.Isam.Esent.Interop.JET_prep.InsertCopy
- Microsoft.Isam.Esent.Interop.JET_prep.Insert
- Microsoft.Isam.Esent.Interop.JET_prep.Replace
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0246114eef784fea2fc145f7cab737c815c17626fc2580b33aa6d09229418066
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118765053"
---
# <a name="jet_prep-enumeration"></a>Énumération JET_prep

Types de mise à jour pour JetPrepareUpdate.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
Public Enumeration JET_prep
'Usage
Dim instance As JET_prep
```

``` csharp
public enum JET_prep
```

## <a name="members"></a>Membres

<table>
<thead>
<tr class="header">
<th></th>
<th>Nom du membre</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td>Insérer</td>
<td>Cet indicateur force le curseur à préparer une insertion d’un nouvel enregistrement. Toutes les données sont initialisées à l’État par défaut de l’enregistrement. Si la table comporte une colonne à incrémentation automatique, une nouvelle valeur est affectée à cet enregistrement, que la mise à jour réussisse ou non, échoue ou est annulée.</td>
</tr>
<tr class="even">
<td></td>
<td>Replace</td>
<td>Cet indicateur force le curseur à préparer un remplacement de l’enregistrement en cours. Si la table contient une colonne version, la colonne version est définie sur la valeur suivante dans sa séquence. Si cette mise à jour ne se termine pas, la valeur de la version dans l’enregistrement n’est pas affectée. Un verrou de mise à jour est appliqué à l’enregistrement pour empêcher d’autres sessions de mettre à jour cet enregistrement avant la fin de cette session.</td>
</tr>
<tr class="odd">
<td></td>
<td>Annuler</td>
<td>Cet indicateur Force JetPrepareUpdate à annuler la mise à jour pour ce curseur.</td>
</tr>
<tr class="even">
<td></td>
<td>ReplaceNoLock</td>
<td>Cet indicateur est similaire à JET_prepReplace, mais aucun verrou n’est pris pour empêcher d’autres sessions de mettre à jour cet enregistrement. Au lieu de cela, cette session peut recevoir des JET_errWriteConflict lorsqu’elle appelle JetUpdate pour terminer la mise à jour.</td>
</tr>
<tr class="odd">
<td></td>
<td>InsertCopy</td>
<td>Cet indicateur force le curseur à préparer une insertion d’une copie de l’enregistrement existant. Il doit y avoir un enregistrement actif si cette option est utilisée. L’état initial du nouvel enregistrement est copié à partir de l’enregistrement en cours. Les valeurs longues qui sont stockées hors enregistrement sont virtuellement copiées.</td>
</tr>
<tr class="even">
<td></td>
<td>InsertCopyDeleteOriginal</td>
<td>Cet indicateur force le curseur à préparer une insertion du même enregistrement, ainsi qu’une suppression ou l’enregistrement d’origine. Il est utilisé dans les cas où la clé primaire a été modifiée.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
