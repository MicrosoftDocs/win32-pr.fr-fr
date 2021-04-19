---
description: 'En savoir plus sur : structure JET_CONDITIONALCOLUMN'
title: Structure JET_CONDITIONALCOLUMN
TOCTitle: JET_CONDITIONALCOLUMN Structure
ms:assetid: 2ca6b4ba-0dc4-47d5-b072-324e5a381d0d
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269214(v=EXCHG.10)
ms:contentKeyID: 32765517
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 27d0add64adeb7b609e84d6102a06230df55ebbf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531813"
---
# <a name="jet_conditionalcolumn-structure"></a><span data-ttu-id="d523c-103">Structure JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="d523c-103">JET_CONDITIONALCOLUMN Structure</span></span>


<span data-ttu-id="d523c-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="d523c-104">_**Applies to:** Windows | Windows Server_</span></span>

## <a name="jet_conditionalcolumn-structure"></a><span data-ttu-id="d523c-105">Structure JET_CONDITIONALCOLUMN</span><span class="sxs-lookup"><span data-stu-id="d523c-105">JET_CONDITIONALCOLUMN Structure</span></span>

<span data-ttu-id="d523c-106">La structure **JET_CONDITIONALCOLUMN** définit la manière dont l’indexation conditionnelle est effectuée pour un index donné.</span><span class="sxs-lookup"><span data-stu-id="d523c-106">The **JET_CONDITIONALCOLUMN** structure defines how conditional indexing is performed for a given index.</span></span> <span data-ttu-id="d523c-107">Un index conditionnel contient une entrée d’index uniquement pour les lignes qui correspondent à la condition spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d523c-107">A conditional index contains an index entry for only those rows that match the specified condition.</span></span> <span data-ttu-id="d523c-108">Toutefois, la colonne conditionnelle ne fait pas partie de la clé de l’index, elle contrôle uniquement la présence de l’entrée d’index.</span><span class="sxs-lookup"><span data-stu-id="d523c-108">However, the conditional column is not part of the index's key, it only controls the presence of the index entry.</span></span>

```cpp
    typedef struct tagJET_CONDITIONALCOLUMN {
      unsigned long cbStruct;
      tchar* szColumnName;
      JET_GRBIT grbit;
    } JET_CONDITIONALCOLUMN;
```

### <a name="members"></a><span data-ttu-id="d523c-109">Membres</span><span class="sxs-lookup"><span data-stu-id="d523c-109">Members</span></span>

<span data-ttu-id="d523c-110">**cbStruct**</span><span class="sxs-lookup"><span data-stu-id="d523c-110">**cbStruct**</span></span>

<span data-ttu-id="d523c-111">Ce champ doit être initialisé à sizeof (JET_CONDITIONALCOLUMN), en octets.</span><span class="sxs-lookup"><span data-stu-id="d523c-111">This field must be initialized to sizeof( JET_CONDITIONALCOLUMN ), in bytes.</span></span>

<span data-ttu-id="d523c-112">**szColumnName**</span><span class="sxs-lookup"><span data-stu-id="d523c-112">**szColumnName**</span></span>

<span data-ttu-id="d523c-113">Nom de la colonne qui contient les données sur lesquelles le moteur de base de données indexe conditionnellement la ligne.</span><span class="sxs-lookup"><span data-stu-id="d523c-113">The name of the column that contains the data on which the database engine is conditionally indexing the row.</span></span>

<span data-ttu-id="d523c-114">**Grbit** Groupe de bits qui fournit les options pour l’index conditionnel.</span><span class="sxs-lookup"><span data-stu-id="d523c-114">**grbit** A group of bits that gives the options for the conditional index.</span></span> <span data-ttu-id="d523c-115">Le passage de valeurs zéro ou d’une valeur de logique **ou** Ed n’est pas valide pour **JET_CONDITIONALCOLUMN**.</span><span class="sxs-lookup"><span data-stu-id="d523c-115">Passing in zero or logically-**OR** ed values is not valid for **JET_CONDITIONALCOLUMN**.</span></span> <span data-ttu-id="d523c-116">Le champ de bits doit correspondre exactement à l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="d523c-116">The bit field must be exactly one of the following:</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d523c-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="d523c-117">Value</span></span></p></th>
<th><p><span data-ttu-id="d523c-118">Signification</span><span class="sxs-lookup"><span data-stu-id="d523c-118">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d523c-119">JET_bitIndexColumnMustBeNull</span><span class="sxs-lookup"><span data-stu-id="d523c-119">JET_bitIndexColumnMustBeNull</span></span></p></td>
<td><p><span data-ttu-id="d523c-120">La colonne spécifiée par le paramètre <em>szColumnName</em> doit avoir la valeur null pour qu’une entrée d’index d’une ligne donnée apparaisse dans cet index.</span><span class="sxs-lookup"><span data-stu-id="d523c-120">The column specified by the <em>szColumnName</em> parameter must be NULL for an index entry for a given row to appear in this index.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d523c-121">JET_bitIndexColumnMustBeNonNull</span><span class="sxs-lookup"><span data-stu-id="d523c-121">JET_bitIndexColumnMustBeNonNull</span></span></p></td>
<td><p><span data-ttu-id="d523c-122">La colonne spécifiée par le paramètre <em>szColumnName</em> doit être non null pour une entrée d’index afin qu’une ligne donnée apparaisse dans cet index.</span><span class="sxs-lookup"><span data-stu-id="d523c-122">The column specified by the <em>szColumnName</em> parameter must be non-NULL for an index entry in order for a given row to appear in this index.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="remarks"></a><span data-ttu-id="d523c-123">Notes</span><span class="sxs-lookup"><span data-stu-id="d523c-123">Remarks</span></span>

<span data-ttu-id="d523c-124">Un index conditionnel contient une entrée d’index uniquement pour les lignes qui correspondent à la condition spécifiée.</span><span class="sxs-lookup"><span data-stu-id="d523c-124">A conditional index contains an index entry for only those rows that match the specified condition.</span></span> <span data-ttu-id="d523c-125">Par exemple, une colonne peut être nommée « marquée » et lorsqu’une ligne est marquée, la colonne est définie sur une valeur non NULL.</span><span class="sxs-lookup"><span data-stu-id="d523c-125">For example, a column could be named "Marked", and when a row is marked, the column is set to a non-NULL value.</span></span> <span data-ttu-id="d523c-126">Un JET_bitIndexColumnMustBeNonNull index conditionnel sur cette colonne affiche toutes les lignes marquées, et un index conditionnel JET_bitIndexColumnMustBeNull affiche les lignes qui ne sont pas marquées.</span><span class="sxs-lookup"><span data-stu-id="d523c-126">A JET_bitIndexColumnMustBeNonNull conditional index on this column will show all rows that are marked, and a JET_bitIndexColumnMustBeNull conditional index will show rows that are not marked.</span></span> <span data-ttu-id="d523c-127">Il s’agit également d’un moyen pratique d’effectuer une suppression d’indicateur et un index de garbage collection.</span><span class="sxs-lookup"><span data-stu-id="d523c-127">This is also a convenient way to perform a flag deletion and garbage collecting index.</span></span>

### <a name="requirements"></a><span data-ttu-id="d523c-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d523c-128">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d523c-129"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="d523c-129"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="d523c-130">Nécessite Windows Vista, Windows XP ou Windows 2000 professionnel.</span><span class="sxs-lookup"><span data-stu-id="d523c-130">Requires Windows Vista, Windows XP, or Windows 2000 Professional.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d523c-131"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="d523c-131"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="d523c-132">Requiert Windows Server 2008, Windows Server 2003 ou Windows 2000 Server.</span><span class="sxs-lookup"><span data-stu-id="d523c-132">Requires Windows Server 2008, Windows Server 2003, or Windows 2000 Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d523c-133"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="d523c-133"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="d523c-134">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="d523c-134">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d523c-135"><strong>Unicode</strong></span><span class="sxs-lookup"><span data-stu-id="d523c-135"><strong>Unicode</strong></span></span></p></td>
<td><p><span data-ttu-id="d523c-136">Implémenté comme <strong>JET_CONDITIONALCOLUMN_W</strong> (Unicode) et <strong>JET_CONDITIONALCOLUMN_A</strong> (ANSI).</span><span class="sxs-lookup"><span data-stu-id="d523c-136">Implemented as <strong>JET_CONDITIONALCOLUMN_W</strong> (Unicode) and <strong>JET_CONDITIONALCOLUMN_A</strong> (ANSI).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a><span data-ttu-id="d523c-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d523c-137">See Also</span></span>

[<span data-ttu-id="d523c-138">JET_GRBIT</span><span class="sxs-lookup"><span data-stu-id="d523c-138">JET_GRBIT</span></span>](./jet-grbit.md)  
[<span data-ttu-id="d523c-139">JET_INDEXCREATE</span><span class="sxs-lookup"><span data-stu-id="d523c-139">JET_INDEXCREATE</span></span>](./jet-indexcreate-structure.md)
