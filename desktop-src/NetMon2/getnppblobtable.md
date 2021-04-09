---
description: La fonction GetNPPBlobTable récupère une table d’objets BLOB NPP qui représente les cartes réseau du Registre sur l’ordinateur local.
ms.assetid: 9e61faf5-1f06-40b5-bf47-f258ffb5151a
title: GetNPPBlobTable, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPBlobTable
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 883493215aaac0fa2568baec69232b379b8aa808
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866266"
---
# <a name="getnppblobtable-function"></a><span data-ttu-id="d7bc6-103">GetNPPBlobTable fonction)</span><span class="sxs-lookup"><span data-stu-id="d7bc6-103">GetNPPBlobTable function</span></span>

<span data-ttu-id="d7bc6-104">La fonction **GetNPPBlobTable** récupère une table d’objets BLOB NPP qui représente les cartes réseau du Registre sur l’ordinateur local.</span><span class="sxs-lookup"><span data-stu-id="d7bc6-104">The **GetNPPBlobTable** function retrieves an NPP BLOB table that represents the register NICs on the local computer.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7bc6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d7bc6-105">Syntax</span></span>


```C++
DWORD GetNPPBlobTable(
  _In_  HBLOB       hFilterBlob,
  _Out_ PBLOB_TABLE *ppBlobTable
);
```



## <a name="parameters"></a><span data-ttu-id="d7bc6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d7bc6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7bc6-107">*hFilterBlob* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d7bc6-107">*hFilterBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7bc6-108">Handle vers un objet BLOB de filtre qui limite les objets BLOB NPP renvoyés dans la table.</span><span class="sxs-lookup"><span data-stu-id="d7bc6-108">Handle to a filter BLOB that limits the NPP BLOBs returned in the table.</span></span>

</dd> <dt>

<span data-ttu-id="d7bc6-109">*ppBlobTable* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d7bc6-109">*ppBlobTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7bc6-110">Pointeur vers une structure de [ \_ table d’objets BLOB](blob-table.md) qui contient au moins un pointeur d’objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="d7bc6-110">Pointer to a [BLOB\_TABLE](blob-table.md) structure that contains at least one BLOB pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7bc6-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d7bc6-111">Return value</span></span>

<span data-ttu-id="d7bc6-112">Si la fonction réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="d7bc6-112">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="d7bc6-113">Si la fonction échoue, la valeur de retour est l’un des codes d’erreur suivants :</span><span class="sxs-lookup"><span data-stu-id="d7bc6-113">If the function is unsuccessful, the return value is one of the following error codes:</span></span>



| <span data-ttu-id="d7bc6-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="d7bc6-114">Return code</span></span>                                                                                                | <span data-ttu-id="d7bc6-115">Description</span><span class="sxs-lookup"><span data-stu-id="d7bc6-115">Description</span></span>                                                            |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d7bc6-116"><dt>**NMERR \_ aucune \_ \_ dll NPP**</dt></span><span class="sxs-lookup"><span data-stu-id="d7bc6-116"><dt>**NMERR\_NO\_NPP\_DLL**</dt></span></span> </dl>         | <span data-ttu-id="d7bc6-117">Aucune dll n’a été trouvée dans le répertoire NPP.</span><span class="sxs-lookup"><span data-stu-id="d7bc6-117">No DLLs were found in the NPP directory.</span></span><br/>                    |
| <dl> <span data-ttu-id="d7bc6-118"><dt>**NMERR \_ aucune \_ \_ dll NPP \_ valide**</dt></span><span class="sxs-lookup"><span data-stu-id="d7bc6-118"><dt>**NMERR\_NO\_VALID\_NPP\_DLLS**</dt></span></span> </dl> | <span data-ttu-id="d7bc6-119">Aucune des dll du répertoire NPP n’était des dll NPP valides.</span><span class="sxs-lookup"><span data-stu-id="d7bc6-119">None of the DLLs in the NPP directory were valid NPP DLLs.</span></span><br/>  |
| <dl> <span data-ttu-id="d7bc6-120"><dt>**NMERR \_ aucun \_ \_ NPPS correspondant**</dt></span><span class="sxs-lookup"><span data-stu-id="d7bc6-120"><dt>**NMERR\_NO\_MATCHING\_NPPS**</dt></span></span> </dl>   | <span data-ttu-id="d7bc6-121">Les objets BLOB NPP ont été découverts, mais aucun n’a passé le test de filtre.</span><span class="sxs-lookup"><span data-stu-id="d7bc6-121">NPP BLOBs were discovered, but none passed the filter test.</span></span><br/> |
| <dl> <span data-ttu-id="d7bc6-122"><dt>**NMERR \_ hors \_ \_ Mémo**</dt></span><span class="sxs-lookup"><span data-stu-id="d7bc6-122"><dt>**NMERR\_OUT\_OF\_MEMOR**</dt></span></span> </dl>       | <span data-ttu-id="d7bc6-123">Moniteur réseau n’a pas pu allouer de mémoire.</span><span class="sxs-lookup"><span data-stu-id="d7bc6-123">Network Monitor was not able to allocate memory.</span></span><br/>            |



 

## <a name="remarks"></a><span data-ttu-id="d7bc6-124">Notes</span><span class="sxs-lookup"><span data-stu-id="d7bc6-124">Remarks</span></span>

<span data-ttu-id="d7bc6-125">L’objet BLOB nommé par *hFilterBlob* peut également être un objet BLOB spécial.</span><span class="sxs-lookup"><span data-stu-id="d7bc6-125">The BLOB named by *hFilterBlob* can also be a special BLOB.</span></span>

<span data-ttu-id="d7bc6-126">Si vous affectez la **valeur true** à l’indicateur dans l’objet blob de filtres, la table d’objets BLOB retournée peut également inclure des objets BLOB spéciaux.</span><span class="sxs-lookup"><span data-stu-id="d7bc6-126">If you set the flag in the filter BLOB to **TRUE**, the returned BLOB table can also include special BLOBs .</span></span>

<span data-ttu-id="d7bc6-127">Si l’objet BLOB nommé par *hFilterBlob* est un objet BLOB spécial, l’interface utilisateur de moniteur réseau tente de la traiter.</span><span class="sxs-lookup"><span data-stu-id="d7bc6-127">If the BLOB named by *hFilterBlob* is a special BLOB, the Network Monitor UI will attempt to process it.</span></span> <span data-ttu-id="d7bc6-128">Par exemple, supposons qu’un appel précédent retourne un objet BLOB spécial du NPP distant.</span><span class="sxs-lookup"><span data-stu-id="d7bc6-128">For example, suppose that a previous call returns a special BLOB from the remote NPP.</span></span> <span data-ttu-id="d7bc6-129">L’application insère la balise requise, le nom de l’ordinateur \_ .</span><span class="sxs-lookup"><span data-stu-id="d7bc6-129">The application inserts the required tag, MACHINE\_NAME.</span></span> <span data-ttu-id="d7bc6-130">Le Finder transmet ensuite cet objet BLOB au NPP distant, qui retourne ensuite une table des objets BLOB NPP associés au nom de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="d7bc6-130">The finder then passes this BLOB to the remote NPP, which then returns a table of the NPP BLOBs associated with the machine name.</span></span>

<span data-ttu-id="d7bc6-131">Pour détruire tous les objets BLOB retournés et la table BLOB, l’appelant est chargé d’appeler la fonction **DestroyBlob** .</span><span class="sxs-lookup"><span data-stu-id="d7bc6-131">To destroy all returned BLOBs and the BLOB table, the caller is responsible for calling the **DestroyBlob** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7bc6-132">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d7bc6-132">Requirements</span></span>



| <span data-ttu-id="d7bc6-133">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d7bc6-133">Requirement</span></span> | <span data-ttu-id="d7bc6-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="d7bc6-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7bc6-135">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7bc6-135">Minimum supported client</span></span><br/> | <span data-ttu-id="d7bc6-136">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d7bc6-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="d7bc6-137">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7bc6-137">Minimum supported server</span></span><br/> | <span data-ttu-id="d7bc6-138">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d7bc6-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d7bc6-139">En-tête</span><span class="sxs-lookup"><span data-stu-id="d7bc6-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7bc6-140"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7bc6-140"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="d7bc6-141">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d7bc6-141">Library</span></span><br/>                  | <dl> <span data-ttu-id="d7bc6-142"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d7bc6-142"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="d7bc6-143">DLL</span><span class="sxs-lookup"><span data-stu-id="d7bc6-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7bc6-144"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7bc6-144"><dt>Npptools.dll</dt></span></span> </dl> |



 

 




