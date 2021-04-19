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
# <a name="temptablegrbit-enumeration"></a><span data-ttu-id="bddf8-103">Énumération TempTableGrbit</span><span class="sxs-lookup"><span data-stu-id="bddf8-103">TempTableGrbit enumeration</span></span>

<span data-ttu-id="bddf8-104">Options de création de table temporaire.</span><span class="sxs-lookup"><span data-stu-id="bddf8-104">Options for temporary table creation.</span></span>

<span data-ttu-id="bddf8-105">Cette énumération a un attribut [FlagsAttribute](/dotnet/api/system.flagsattribute) qui permet une combinaison au niveau du bit de ses valeurs membres.</span><span class="sxs-lookup"><span data-stu-id="bddf8-105">This enumeration has a [FlagsAttribute](/dotnet/api/system.flagsattribute) attribute that allows a bitwise combination of its member values.</span></span>

<span data-ttu-id="bddf8-106">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="bddf8-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="bddf8-107">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="bddf8-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="bddf8-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bddf8-108">Syntax</span></span>

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

## <a name="members"></a><span data-ttu-id="bddf8-109">Membres</span><span class="sxs-lookup"><span data-stu-id="bddf8-109">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="bddf8-110">Nom du membre</span><span class="sxs-lookup"><span data-stu-id="bddf8-110">Member name</span></span></th>
<th><span data-ttu-id="bddf8-111">Description</span><span class="sxs-lookup"><span data-stu-id="bddf8-111">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="bddf8-112">Aucune</span><span class="sxs-lookup"><span data-stu-id="bddf8-112">None</span></span></td>
<td><span data-ttu-id="bddf8-113">Options par défaut.</span><span class="sxs-lookup"><span data-stu-id="bddf8-113">Default options.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="bddf8-114">Indexée</span><span class="sxs-lookup"><span data-stu-id="bddf8-114">Indexed</span></span></td>
<td><span data-ttu-id="bddf8-115">Cette option demande que la table temporaire soit suffisamment flexible pour permettre l’utilisation de JetSeek pour rechercher des enregistrements par clé d’index.</span><span class="sxs-lookup"><span data-stu-id="bddf8-115">This option requests that the temporary table be flexible enough to permit the use of JetSeek to lookup records by index key.</span></span> <span data-ttu-id="bddf8-116">Si cette fonctionnalité n’est pas nécessaire, il est préférable de ne pas la demander.</span><span class="sxs-lookup"><span data-stu-id="bddf8-116">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="bddf8-117">Si cette fonctionnalité n’est pas demandée, le gestionnaire de tables temporaire peut être en mesure de choisir une stratégie de gestion de la table temporaire qui entraîne une amélioration des performances.</span><span class="sxs-lookup"><span data-stu-id="bddf8-117">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="bddf8-118">Unique</span><span class="sxs-lookup"><span data-stu-id="bddf8-118">Unique</span></span></td>
<td><span data-ttu-id="bddf8-119">Cette option demande que les enregistrements avec des clés d’index dupliquées soient supprimés du jeu final d’enregistrements dans la table temporaire.</span><span class="sxs-lookup"><span data-stu-id="bddf8-119">This option requests that records with duplicate index keys be removed from the final set of records in the temporary table.</span></span> <span data-ttu-id="bddf8-120">Avant Windows Server 2003, le moteur de base de données supposait toujours que cette option était appliquée en raison du fait que tous les index cluster doivent également être une clé primaire et doivent donc être uniques.</span><span class="sxs-lookup"><span data-stu-id="bddf8-120">Prior to Windows Server 2003, the database engine always assumed this option to be in effect due to the fact that all clustered indexes must also be a primary key and thus must be unique.</span></span> <span data-ttu-id="bddf8-121">À compter de Windows Server 2003, il est désormais possible de créer une table temporaire qui ne supprime pas les doublons quand l’option <a href="dn351284(v=exchg.10).md">ForwardOnly</a> est également spécifiée.</span><span class="sxs-lookup"><span data-stu-id="bddf8-121">As of Windows Server 2003, it is now possible to create a temporary table that does NOT remove duplicates when the <a href="dn351284(v=exchg.10).md">ForwardOnly</a> option is also specified.</span></span> <span data-ttu-id="bddf8-122">Il n’est pas possible de savoir quels doublons seront remportés et quels doublons seront ignorés en général.</span><span class="sxs-lookup"><span data-stu-id="bddf8-122">It is not possible to know which duplicate will win and which duplicates will be discarded in general.</span></span> <span data-ttu-id="bddf8-123">Toutefois, quand l’option ErrorOnDuplicateInsertion est demandée, le premier enregistrement avec une clé d’index donnée à insérer dans la table temporaire est toujours gagnant.</span><span class="sxs-lookup"><span data-stu-id="bddf8-123">However, when the ErrorOnDuplicateInsertion option is requested then the first record with a given index key to be inserted into the temporary table will always win.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="bddf8-124">Peut être mise à jour</span><span class="sxs-lookup"><span data-stu-id="bddf8-124">Updatable</span></span></td>
<td><span data-ttu-id="bddf8-125">Cette option demande que la table temporaire soit suffisamment flexible pour permettre la modification ultérieure des enregistrements qui ont été insérés précédemment.</span><span class="sxs-lookup"><span data-stu-id="bddf8-125">This option requests that the temporary table be flexible enough to allow records that have previously been inserted to be subsequently changed.</span></span> <span data-ttu-id="bddf8-126">Si cette fonctionnalité n’est pas nécessaire, il est préférable de ne pas la demander.</span><span class="sxs-lookup"><span data-stu-id="bddf8-126">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="bddf8-127">Si cette fonctionnalité n’est pas demandée, le gestionnaire de tables temporaire peut être en mesure de choisir une stratégie de gestion de la table temporaire qui entraîne une amélioration des performances.</span><span class="sxs-lookup"><span data-stu-id="bddf8-127">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="bddf8-128">Défilement</span><span class="sxs-lookup"><span data-stu-id="bddf8-128">Scrollable</span></span></td>
<td><span data-ttu-id="bddf8-129">Cette option demande que la table temporaire soit suffisamment flexible pour permettre l’analyse des enregistrements dans un ordre et une direction arbitraires à l’aide de <a href="dn292217(v=exchg.10).md">JetMove (JET_SESID, JET_TABLEID, Int32, MoveGrbit)</a>.</span><span class="sxs-lookup"><span data-stu-id="bddf8-129">This option requests that the temporary table be flexible enough to allow records to be scanned in arbitrary order and direction using <a href="dn292217(v=exchg.10).md">JetMove(JET_SESID, JET_TABLEID, Int32, MoveGrbit)</a>.</span></span> <span data-ttu-id="bddf8-130">Si cette fonctionnalité n’est pas nécessaire, il est préférable de ne pas la demander.</span><span class="sxs-lookup"><span data-stu-id="bddf8-130">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="bddf8-131">Si cette fonctionnalité n’est pas demandée, le gestionnaire de tables temporaire peut être en mesure de choisir une stratégie de gestion de la table temporaire qui entraîne une amélioration des performances.</span><span class="sxs-lookup"><span data-stu-id="bddf8-131">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="bddf8-132">SortNullsHigh</span><span class="sxs-lookup"><span data-stu-id="bddf8-132">SortNullsHigh</span></span></td>
<td><span data-ttu-id="bddf8-133">Cette option demande que les valeurs de colonne clé NULL soient triées plus près de la fin de l’index que les valeurs de colonne clé non NULL.</span><span class="sxs-lookup"><span data-stu-id="bddf8-133">This option requests that NULL key column values sort closer to the end of the index than non-NULL key column values.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="bddf8-134">ForceMaterialization</span><span class="sxs-lookup"><span data-stu-id="bddf8-134">ForceMaterialization</span></span></td>
<td><span data-ttu-id="bddf8-135">Cette option force le gestionnaire de tables temporaires à abandonner toute tentative de choix d’une stratégie astucieuse pour la gestion de la table temporaire qui entraîne des performances améliorées.</span><span class="sxs-lookup"><span data-stu-id="bddf8-135">This option forces the temporary table manager to abandon any attempt to choose a clever strategy for managing the temporary table that will result in enhanced performance.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="bddf8-136">ErrorOnDuplicateInsertion</span><span class="sxs-lookup"><span data-stu-id="bddf8-136">ErrorOnDuplicateInsertion</span></span></td>
<td><span data-ttu-id="bddf8-137">Cette option demande que toute tentative d’insertion d’un enregistrement avec la même clé d’index qu’un enregistrement précédemment inséré échouera immédiatement avec <a href="hh564840(v=exchg.10).md">KeyDuplicate</a>.</span><span class="sxs-lookup"><span data-stu-id="bddf8-137">This option requests that any attempt to insert a record with the same index key as a previously inserted record will immediately fail with <a href="hh564840(v=exchg.10).md">KeyDuplicate</a>.</span></span> <span data-ttu-id="bddf8-138">Si cette option n’est pas demandée, un doublon peut être détecté immédiatement et échouer ou peut être supprimé en mode silencieux ultérieurement selon la stratégie choisie par le moteur de base de données pour implémenter la table temporaire en fonction de la fonctionnalité demandée.</span><span class="sxs-lookup"><span data-stu-id="bddf8-138">If this option is not requested then a duplicate may be detected immediately and fail or may be silently removed later depending on the strategy chosen by the database engine to implement the temporary table based on the requested functionality.</span></span> <span data-ttu-id="bddf8-139">Si cette fonctionnalité n’est pas nécessaire, il est préférable de ne pas la demander.</span><span class="sxs-lookup"><span data-stu-id="bddf8-139">If this functionality it not required then it is best to not request it.</span></span> <span data-ttu-id="bddf8-140">Si cette fonctionnalité n’est pas demandée, le gestionnaire de tables temporaire peut être en mesure de choisir une stratégie de gestion de la table temporaire qui entraîne une amélioration des performances.</span><span class="sxs-lookup"><span data-stu-id="bddf8-140">If this functionality is not requested then the temporary table manager may be able to choose a strategy for managing the temporary table that will result in improved performance.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="bddf8-141">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bddf8-141">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="bddf8-142">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="bddf8-142">Reference</span></span>

[<span data-ttu-id="bddf8-143">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="bddf8-143">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

[<span data-ttu-id="bddf8-144">ForwardOnly</span><span class="sxs-lookup"><span data-stu-id="bddf8-144">ForwardOnly</span></span>](./server2003grbits.forwardonly-field.md)

[<span data-ttu-id="bddf8-145">IntrinsicLVsOnly</span><span class="sxs-lookup"><span data-stu-id="bddf8-145">IntrinsicLVsOnly</span></span>](./windows7grbits.intrinsiclvsonly-field.md)
