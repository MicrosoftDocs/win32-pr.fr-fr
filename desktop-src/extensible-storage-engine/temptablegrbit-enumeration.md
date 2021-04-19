---
description: 'En savoir plus sur : énumération TempTableGrbit'
title: Énumération TempTableGrbit
TOCTitle: TempTableGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.TempTableGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.temptablegrbit(v=EXCHG.10)
ms:contentKeyID: 39515065
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.TempTableGrbit
- Microsoft.Isam.Esent.Interop.TempTableGrbit.ErrorOnDuplicateInsertion
- Microsoft.Isam.Esent.Interop.TempTableGrbit.None
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Unique
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Updatable
- Microsoft.Isam.Esent.Interop.TempTableGrbit.SortNullsHigh
- Microsoft.Isam.Esent.Interop.TempTableGrbit.ForceMaterialization
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Indexed
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Scrollable
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.TempTableGrbit.ErrorOnDuplicateInsertion
- Microsoft.Isam.Esent.Interop.TempTableGrbit.None
- Microsoft.Isam.Esent.Interop.TempTableGrbit
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Indexed
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Updatable
- Microsoft.Isam.Esent.Interop.TempTableGrbit.ForceMaterialization
- Microsoft.Isam.Esent.Interop.TempTableGrbit.SortNullsHigh
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Scrollable
- Microsoft.Isam.Esent.Interop.TempTableGrbit.Unique
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 79247bac6e8d3bda9d1aeac4d19b7af894201a57
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515016"
---
# <a name="temptablegrbit-enumeration"></a>Énumération TempTableGrbit

Options de création de table temporaire.

Cette énumération a un attribut [FlagsAttribute](/dotnet/api/system.flagsattribute) qui permet une combinaison au niveau du bit de ses valeurs membres.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration TempTableGrbit
'Usage
Dim instance As TempTableGrbit
```

``` csharp
[FlagsAttribute]
public enum TempTableGrbit
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
<td>Aucune</td>
<td>Options par défaut.</td>
</tr>
<tr class="even">
<td></td>
<td>Indexée</td>
<td>Cette option demande que la table temporaire soit suffisamment flexible pour permettre l’utilisation de JetSeek pour rechercher des enregistrements par clé d’index. Si cette fonctionnalité n’est pas nécessaire, il est préférable de ne pas la demander. Si cette fonctionnalité n’est pas demandée, le gestionnaire de tables temporaire peut être en mesure de choisir une stratégie de gestion de la table temporaire qui entraîne une amélioration des performances.</td>
</tr>
<tr class="odd">
<td></td>
<td>Unique</td>
<td>Cette option demande que les enregistrements avec des clés d’index dupliquées soient supprimés du jeu final d’enregistrements dans la table temporaire. Avant Windows Server 2003, le moteur de base de données supposait toujours que cette option était appliquée en raison du fait que tous les index cluster doivent également être une clé primaire et doivent donc être uniques. À compter de Windows Server 2003, il est désormais possible de créer une table temporaire qui ne supprime pas les doublons quand l’option <a href="dn351284(v=exchg.10).md">ForwardOnly</a> est également spécifiée. Il n’est pas possible de savoir quels doublons seront remportés et quels doublons seront ignorés en général. Toutefois, quand l’option ErrorOnDuplicateInsertion est demandée, le premier enregistrement avec une clé d’index donnée à insérer dans la table temporaire est toujours gagnant.</td>
</tr>
<tr class="even">
<td></td>
<td>Peut être mise à jour</td>
<td>Cette option demande que la table temporaire soit suffisamment flexible pour permettre la modification ultérieure des enregistrements qui ont été insérés précédemment. Si cette fonctionnalité n’est pas nécessaire, il est préférable de ne pas la demander. Si cette fonctionnalité n’est pas demandée, le gestionnaire de tables temporaire peut être en mesure de choisir une stratégie de gestion de la table temporaire qui entraîne une amélioration des performances.</td>
</tr>
<tr class="odd">
<td></td>
<td>Défilement</td>
<td>Cette option demande que la table temporaire soit suffisamment flexible pour permettre l’analyse des enregistrements dans un ordre et une direction arbitraires à l’aide de <a href="dn292217(v=exchg.10).md">JetMove (JET_SESID, JET_TABLEID, Int32, MoveGrbit)</a>. Si cette fonctionnalité n’est pas nécessaire, il est préférable de ne pas la demander. Si cette fonctionnalité n’est pas demandée, le gestionnaire de tables temporaire peut être en mesure de choisir une stratégie de gestion de la table temporaire qui entraîne une amélioration des performances.</td>
</tr>
<tr class="even">
<td></td>
<td>SortNullsHigh</td>
<td>Cette option demande que les valeurs de colonne clé NULL soient triées plus près de la fin de l’index que les valeurs de colonne clé non NULL.</td>
</tr>
<tr class="odd">
<td></td>
<td>ForceMaterialization</td>
<td>Cette option force le gestionnaire de tables temporaires à abandonner toute tentative de choix d’une stratégie astucieuse pour la gestion de la table temporaire qui entraîne des performances améliorées.</td>
</tr>
<tr class="even">
<td></td>
<td>ErrorOnDuplicateInsertion</td>
<td>Cette option demande que toute tentative d’insertion d’un enregistrement avec la même clé d’index qu’un enregistrement précédemment inséré échouera immédiatement avec <a href="hh564840(v=exchg.10).md">KeyDuplicate</a>. Si cette option n’est pas demandée, un doublon peut être détecté immédiatement et échouer ou peut être supprimé en mode silencieux ultérieurement selon la stratégie choisie par le moteur de base de données pour implémenter la table temporaire en fonction de la fonctionnalité demandée. Si cette fonctionnalité n’est pas nécessaire, il est préférable de ne pas la demander. Si cette fonctionnalité n’est pas demandée, le gestionnaire de tables temporaire peut être en mesure de choisir une stratégie de gestion de la table temporaire qui entraîne une amélioration des performances.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)

[ForwardOnly](./server2003grbits.forwardonly-field.md)

[IntrinsicLVsOnly](./windows7grbits.intrinsiclvsonly-field.md)
