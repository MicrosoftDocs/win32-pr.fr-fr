---
description: 'En savoir plus sur : fonction JetSetCursorFilter'
title: JetSetCursorFilter fonction)
TOCTitle: JetSetCursorFilter Function
ms:assetid: 3cea5beb-2cf8-4053-8e7f-7b8645580ef0
ms:mtpsurl: https://msdn.microsoft.com/library/JJ835040(v=EXCHG.10)
ms:contentKeyID: 49894662
ms.date: 04/11/2016
ms.topic: reference
dev_langs:
- c++
api_name:
- JetSetCursorFilter
topic_type:
- apiref
- kbArticle
api_type:
- DLLExport
api_location:
- ESENT.DLL
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ad589fecb190ad0f0676325b78adc7c96028a3fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112518"
---
# <a name="jetsetcursorfilter-function"></a><span data-ttu-id="27922-103">JetSetCursorFilter fonction)</span><span class="sxs-lookup"><span data-stu-id="27922-103">JetSetCursorFilter Function</span></span>


<span data-ttu-id="27922-104">_**S’applique à :** Windows | Serveur Windows_</span><span class="sxs-lookup"><span data-stu-id="27922-104">_**Applies to:** Windows | Windows Server_</span></span>

<span data-ttu-id="27922-105">La fonction **JetSetCursorFilter** définit un tableau de filtres simples pour la fonction [JetMove](./jetmove-function.md) .</span><span class="sxs-lookup"><span data-stu-id="27922-105">The **JetSetCursorFilter** function sets an array of simple filters for the [JetMove](./jetmove-function.md) function.</span></span>

<span data-ttu-id="27922-106">La fonction **JetSetCursorFilter** a été introduite dans le système d’exploitation Windows 8.</span><span class="sxs-lookup"><span data-stu-id="27922-106">The **JetSetCursorFilter** function was introduced in the Windows 8 operating system.</span></span>

``` c++
JET_ERR JET_API JetSetCursorFilter(
  __in          JET_SESID sesid,
  __in          JET_TABLEID tableid,
  __in_ecount(cFilters)  JET_INDEX_COLUMN* rgFilters,
  __in          DWORD cFilters,
  __in          JET_GRBIT grbit
);
```

### <a name="parameters"></a><span data-ttu-id="27922-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="27922-107">Parameters</span></span>

<span data-ttu-id="27922-108">*sesid*</span><span class="sxs-lookup"><span data-stu-id="27922-108">*sesid*</span></span>

<span data-ttu-id="27922-109">Contexte de la session de base de données à utiliser pour l’appel d’API.</span><span class="sxs-lookup"><span data-stu-id="27922-109">The database session context to use for the API call.</span></span>

<span data-ttu-id="27922-110">*TableID*</span><span class="sxs-lookup"><span data-stu-id="27922-110">*tableid*</span></span>

<span data-ttu-id="27922-111">Curseur à positionner.</span><span class="sxs-lookup"><span data-stu-id="27922-111">The cursor to position.</span></span>

<span data-ttu-id="27922-112">*rgFilters*</span><span class="sxs-lookup"><span data-stu-id="27922-112">*rgFilters*</span></span>

<span data-ttu-id="27922-113">Filtres d’enregistrements simples.</span><span class="sxs-lookup"><span data-stu-id="27922-113">The simple record filters.</span></span>

<span data-ttu-id="27922-114">*cFilters*</span><span class="sxs-lookup"><span data-stu-id="27922-114">*cFilters*</span></span>

<span data-ttu-id="27922-115">Nombre de filtres.</span><span class="sxs-lookup"><span data-stu-id="27922-115">The number of filters.</span></span>

<span data-ttu-id="27922-116">*grbit*</span><span class="sxs-lookup"><span data-stu-id="27922-116">*grbit*</span></span>

<span data-ttu-id="27922-117">Groupe de bits qui spécifie zéro, une ou plusieurs des options de déplacement énumérées dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="27922-117">A group of bits that specifies zero or more of the move options listed in the following table.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="27922-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="27922-118">Value</span></span></p></th>
<th><p><span data-ttu-id="27922-119">Signification</span><span class="sxs-lookup"><span data-stu-id="27922-119">Meaning</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="27922-120">Aucun</span><span class="sxs-lookup"><span data-stu-id="27922-120">None</span></span></p></td>
<td><p><span data-ttu-id="27922-121">Option par défaut.</span><span class="sxs-lookup"><span data-stu-id="27922-121">Default option.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="return-value"></a><span data-ttu-id="27922-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="27922-122">Return value</span></span>

<span data-ttu-id="27922-123">Cette fonction retourne le type de données [JET_ERR](./jet-err.md) avec l’un des codes de retour énumérés dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="27922-123">This function returns the [JET_ERR](./jet-err.md) data type with one of the return codes listed in the following table.</span></span> <span data-ttu-id="27922-124">Pour plus d’informations sur les erreurs ESE (Extensible Storage Engine) possibles, consultez [Erreurs du moteur de stockage extensible](./extensible-storage-engine-errors.md) et [paramètres de gestion des erreurs](./error-handling-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="27922-124">For more information about the possible Extensible Storage Engine (ESE) errors, see [Extensible Storage Engine Errors](./extensible-storage-engine-errors.md) and [Error Handling Parameters](./error-handling-parameters.md).</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="27922-125">Code de retour</span><span class="sxs-lookup"><span data-stu-id="27922-125">Return code</span></span></p></th>
<th><p><span data-ttu-id="27922-126">Description</span><span class="sxs-lookup"><span data-stu-id="27922-126">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="27922-127">JET_errSuccess</span><span class="sxs-lookup"><span data-stu-id="27922-127">JET_errSuccess</span></span></p></td>
<td><p><span data-ttu-id="27922-128">L’opération s’est terminée avec succès.</span><span class="sxs-lookup"><span data-stu-id="27922-128">The operation completed successfully.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="requirements"></a><span data-ttu-id="27922-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="27922-129">Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="27922-130"><strong>Client</strong></span><span class="sxs-lookup"><span data-stu-id="27922-130"><strong>Client</strong></span></span></p></td>
<td><p><span data-ttu-id="27922-131">Requiert Windows 8.</span><span class="sxs-lookup"><span data-stu-id="27922-131">Requires Windows 8.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27922-132"><strong>Serveur</strong></span><span class="sxs-lookup"><span data-stu-id="27922-132"><strong>Server</strong></span></span></p></td>
<td><p><span data-ttu-id="27922-133">Requiert Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="27922-133">Requires Windows Server 2012.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27922-134"><strong>En-tête</strong></span><span class="sxs-lookup"><span data-stu-id="27922-134"><strong>Header</strong></span></span></p></td>
<td><p><span data-ttu-id="27922-135">Déclaré dans esent. h.</span><span class="sxs-lookup"><span data-stu-id="27922-135">Declared in Esent.h.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="27922-136"><strong>Bibliothèque</strong></span><span class="sxs-lookup"><span data-stu-id="27922-136"><strong>Library</strong></span></span></p></td>
<td><p><span data-ttu-id="27922-137">Utilisez ESENT. lib.</span><span class="sxs-lookup"><span data-stu-id="27922-137">Use ESENT.lib.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="27922-138"><strong>DLL</strong></span><span class="sxs-lookup"><span data-stu-id="27922-138"><strong>DLL</strong></span></span></p></td>
<td><p><span data-ttu-id="27922-139">Requiert ESENT.dll.</span><span class="sxs-lookup"><span data-stu-id="27922-139">Requires ESENT.dll.</span></span></p></td>
</tr>
</tbody>
</table>


#### <a name="see-also"></a><span data-ttu-id="27922-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="27922-140">See also</span></span>

[<span data-ttu-id="27922-141">JetMove</span><span class="sxs-lookup"><span data-stu-id="27922-141">JetMove</span></span>](./jetmove-function.md)  
[<span data-ttu-id="27922-142">JET_ERR</span><span class="sxs-lookup"><span data-stu-id="27922-142">JET_ERR</span></span>](./jet-err.md)
