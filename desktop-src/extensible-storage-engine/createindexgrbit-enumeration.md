---
description: 'En savoir plus sur : énumération CreateIndexGrbit'
title: Énumération CreateIndexGrbit
TOCTitle: CreateIndexGrbit enumeration
ms:assetid: T:Microsoft.Isam.Esent.Interop.CreateIndexGrbit
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.createindexgrbit(v=EXCHG.10)
ms:contentKeyID: 39511957
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexUnversioned
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreFirstNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexUnique
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexDisallowNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexPrimary
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.None
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexSortNullsHigh
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreAnyNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexLazyFlush
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexEmpty
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreNull
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexEmpty
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.None
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreFirstNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreAnyNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexLazyFlush
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexUnversioned
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexSortNullsHigh
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexDisallowNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexIgnoreNull
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexPrimary
- Microsoft.Isam.Esent.Interop.CreateIndexGrbit.IndexUnique
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4e7a03a077262485533e29690215be1468987e50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106536661"
---
# <a name="createindexgrbit-enumeration"></a>Énumération CreateIndexGrbit

Options pour JetCreateIndex.

Cette énumération a un attribut [FlagsAttribute](/dotnet/api/system.flagsattribute) qui permet une combinaison au niveau du bit de ses valeurs membres.

**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)  
**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)

## <a name="syntax"></a>Syntaxe

``` vb
'Declaration
<FlagsAttribute> _
Public Enumeration CreateIndexGrbit
'Usage
Dim instance As CreateIndexGrbit
```

``` csharp
[FlagsAttribute]
public enum CreateIndexGrbit
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
<td>IndexUnique</td>
<td>Les entrées d’index en double (clés) ne sont pas autorisées. Cette méthode est appliquée quand JetUpdate est appelé, et non lorsque JetSetColumn est appelé.</td>
</tr>
<tr class="odd">
<td></td>
<td>IndexPrimary</td>
<td>L’index est un index principal (cluster). Chaque table doit avoir un seul index primaire. Si aucun index primaire n’est défini explicitement sur une table, le moteur de base de données crée son propre index primaire.</td>
</tr>
<tr class="even">
<td></td>
<td>IndexDisallowNull</td>
<td>Aucune des colonnes sur lesquelles l’index est créé ne peut contenir une valeur NULL.</td>
</tr>
<tr class="odd">
<td></td>
<td>IndexIgnoreNull</td>
<td>N’ajoutez pas d’entrée d’index pour une ligne si toutes les colonnes indexées ont la valeur NULL.</td>
</tr>
<tr class="even">
<td></td>
<td>IndexIgnoreAnyNull</td>
<td>N’ajoutez pas d’entrée d’index pour une ligne si l’une des colonnes indexées a la valeur NULL.</td>
</tr>
<tr class="odd">
<td></td>
<td>IndexIgnoreFirstNull</td>
<td>N’ajoutez pas d’entrée d’index pour une ligne si la première colonne indexée a la valeur NULL.</td>
</tr>
<tr class="even">
<td></td>
<td>IndexLazyFlush</td>
<td>Spécifie que les opérations d’index seront journalisées tardivement. JET_bitIndexLazyFlush n’affecte pas le paresse des mises à jour de données. Si les opérations d’indexation sont interrompues par l’arrêt du processus, la récupération logicielle peut toujours être en mesure d’obtenir la base de données à un état cohérent, mais l’index n’est peut-être pas présent.</td>
</tr>
<tr class="odd">
<td></td>
<td>IndexEmpty</td>
<td>N’essayez pas de créer l’index, car toutes les entrées ont la valeur NULL. Grbit doit également spécifier JET_bitIgnoreAnyNull lorsque JET_bitIndexEmpty est passé. Il s’agit d’une amélioration des performances. Par exemple, si une nouvelle colonne est ajoutée à une table, un index est créé sur cette colonne nouvellement ajoutée, tous les enregistrements de la table sont analysés même s’ils ne sont jamais ajoutés à l’index. La spécification de JET_bitIndexEmpty ignore l’analyse de la table, ce qui peut prendre un certain temps.</td>
</tr>
<tr class="even">
<td></td>
<td>IndexUnversioned</td>
<td>Rend la création d’index visible pour les autres transactions. Normalement, une session dans une transaction ne peut pas voir une opération de création d’index dans une autre session. Cet indicateur peut être utile si une autre transaction est susceptible de créer le même index, de sorte que la deuxième index-Create échoue simplement au lieu de provoquer potentiellement des opérations de base de données inutiles. La deuxième transaction peut ne pas être en mesure d’utiliser l’index immédiatement. L’opération de création d’index doit être terminée pour pouvoir être utilisée. La session ne doit pas être actuellement dans une transaction pour créer un index sans informations de version.</td>
</tr>
<tr class="odd">
<td></td>
<td>IndexSortNullsHigh</td>
<td>Si vous spécifiez cet indicateur, les valeurs NULL sont triées après les données de toutes les colonnes de l’index.</td>
</tr>
</tbody>
</table>


## <a name="see-also"></a>Voir aussi

#### <a name="reference"></a>Informations de référence

[Espace de noms Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)
