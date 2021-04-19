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
ms.openlocfilehash: edeaef8144fe6e13674ec6d3dfcb8adf7522e148
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529372"
---
# <a name="jet_prep-enumeration"></a><span data-ttu-id="3fac7-103">Énumération JET_prep</span><span class="sxs-lookup"><span data-stu-id="3fac7-103">JET_prep enumeration</span></span>

<span data-ttu-id="3fac7-104">Types de mise à jour pour JetPrepareUpdate.</span><span class="sxs-lookup"><span data-stu-id="3fac7-104">Update types for JetPrepareUpdate.</span></span>

<span data-ttu-id="3fac7-105">**Espace de noms :**  [Microsoft. ISAM. esent. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="3fac7-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="3fac7-106">**Assembly :**  Microsoft. ISAM. esent. Interop (en Microsoft.Isam.Esent.Interop.dll)</span><span class="sxs-lookup"><span data-stu-id="3fac7-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="3fac7-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3fac7-107">Syntax</span></span>

``` vb
'Declaration
Public Enumeration JET_prep
'Usage
Dim instance As JET_prep
```

``` csharp
public enum JET_prep
```

## <a name="members"></a><span data-ttu-id="3fac7-108">Membres</span><span class="sxs-lookup"><span data-stu-id="3fac7-108">Members</span></span>

<table>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="3fac7-109">Nom du membre</span><span class="sxs-lookup"><span data-stu-id="3fac7-109">Member name</span></span></th>
<th><span data-ttu-id="3fac7-110">Description</span><span class="sxs-lookup"><span data-stu-id="3fac7-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td></td>
<td><span data-ttu-id="3fac7-111">Insérer</span><span class="sxs-lookup"><span data-stu-id="3fac7-111">Insert</span></span></td>
<td><span data-ttu-id="3fac7-112">Cet indicateur force le curseur à préparer une insertion d’un nouvel enregistrement.</span><span class="sxs-lookup"><span data-stu-id="3fac7-112">This flag causes the cursor to prepare for an insert of a new record.</span></span> <span data-ttu-id="3fac7-113">Toutes les données sont initialisées à l’État par défaut de l’enregistrement.</span><span class="sxs-lookup"><span data-stu-id="3fac7-113">All the data is initialized to the default state for the record.</span></span> <span data-ttu-id="3fac7-114">Si la table comporte une colonne à incrémentation automatique, une nouvelle valeur est affectée à cet enregistrement, que la mise à jour réussisse ou non, échoue ou est annulée.</span><span class="sxs-lookup"><span data-stu-id="3fac7-114">If the table has an auto-increment column, then a new value is assigned to this record regardless of whether the update ultimately succeeds, fails or is cancelled.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="3fac7-115">Replace</span><span class="sxs-lookup"><span data-stu-id="3fac7-115">Replace</span></span></td>
<td><span data-ttu-id="3fac7-116">Cet indicateur force le curseur à préparer un remplacement de l’enregistrement en cours.</span><span class="sxs-lookup"><span data-stu-id="3fac7-116">This flag causes the cursor to prepare for a replace of the current record.</span></span> <span data-ttu-id="3fac7-117">Si la table contient une colonne version, la colonne version est définie sur la valeur suivante dans sa séquence.</span><span class="sxs-lookup"><span data-stu-id="3fac7-117">If the table has a version column, then the version column is set to the next value in its sequence.</span></span> <span data-ttu-id="3fac7-118">Si cette mise à jour ne se termine pas, la valeur de la version dans l’enregistrement n’est pas affectée.</span><span class="sxs-lookup"><span data-stu-id="3fac7-118">If this update does not complete, then the version value in the record will be unaffected.</span></span> <span data-ttu-id="3fac7-119">Un verrou de mise à jour est appliqué à l’enregistrement pour empêcher d’autres sessions de mettre à jour cet enregistrement avant la fin de cette session.</span><span class="sxs-lookup"><span data-stu-id="3fac7-119">An update lock is taken on the record to prevent other sessions from updating this record before this session completes.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="3fac7-120">Annuler</span><span class="sxs-lookup"><span data-stu-id="3fac7-120">Cancel</span></span></td>
<td><span data-ttu-id="3fac7-121">Cet indicateur Force JetPrepareUpdate à annuler la mise à jour pour ce curseur.</span><span class="sxs-lookup"><span data-stu-id="3fac7-121">This flag causes JetPrepareUpdate to cancel the update for this cursor.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="3fac7-122">ReplaceNoLock</span><span class="sxs-lookup"><span data-stu-id="3fac7-122">ReplaceNoLock</span></span></td>
<td><span data-ttu-id="3fac7-123">Cet indicateur est similaire à JET_prepReplace, mais aucun verrou n’est pris pour empêcher d’autres sessions de mettre à jour cet enregistrement.</span><span class="sxs-lookup"><span data-stu-id="3fac7-123">This flag is similar to JET_prepReplace, but no lock is taken to prevent other sessions from updating this record.</span></span> <span data-ttu-id="3fac7-124">Au lieu de cela, cette session peut recevoir des JET_errWriteConflict lorsqu’elle appelle JetUpdate pour terminer la mise à jour.</span><span class="sxs-lookup"><span data-stu-id="3fac7-124">Instead, this session may receive JET_errWriteConflict when it calls JetUpdate to complete the update.</span></span></td>
</tr>
<tr class="odd">
<td></td>
<td><span data-ttu-id="3fac7-125">InsertCopy</span><span class="sxs-lookup"><span data-stu-id="3fac7-125">InsertCopy</span></span></td>
<td><span data-ttu-id="3fac7-126">Cet indicateur force le curseur à préparer une insertion d’une copie de l’enregistrement existant.</span><span class="sxs-lookup"><span data-stu-id="3fac7-126">This flag causes the cursor to prepare for an insert of a copy of the existing record.</span></span> <span data-ttu-id="3fac7-127">Il doit y avoir un enregistrement actif si cette option est utilisée.</span><span class="sxs-lookup"><span data-stu-id="3fac7-127">There must be a current record if this option is used.</span></span> <span data-ttu-id="3fac7-128">L’état initial du nouvel enregistrement est copié à partir de l’enregistrement en cours.</span><span class="sxs-lookup"><span data-stu-id="3fac7-128">The initial state of the new record is copied from the current record.</span></span> <span data-ttu-id="3fac7-129">Les valeurs longues qui sont stockées hors enregistrement sont virtuellement copiées.</span><span class="sxs-lookup"><span data-stu-id="3fac7-129">Long values that are stored off-record are virtually copied.</span></span></td>
</tr>
<tr class="even">
<td></td>
<td><span data-ttu-id="3fac7-130">InsertCopyDeleteOriginal</span><span class="sxs-lookup"><span data-stu-id="3fac7-130">InsertCopyDeleteOriginal</span></span></td>
<td><span data-ttu-id="3fac7-131">Cet indicateur force le curseur à préparer une insertion du même enregistrement, ainsi qu’une suppression ou l’enregistrement d’origine.</span><span class="sxs-lookup"><span data-stu-id="3fac7-131">This flag causes the cursor to prepare for an insert of the same record, and a delete or the original record.</span></span> <span data-ttu-id="3fac7-132">Il est utilisé dans les cas où la clé primaire a été modifiée.</span><span class="sxs-lookup"><span data-stu-id="3fac7-132">It is used in cases in which the primary key has changed.</span></span></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="3fac7-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="3fac7-133">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="3fac7-134">Informations de référence</span><span class="sxs-lookup"><span data-stu-id="3fac7-134">Reference</span></span>

[<span data-ttu-id="3fac7-135">Espace de noms Microsoft. ISAM. esent. Interop</span><span class="sxs-lookup"><span data-stu-id="3fac7-135">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
