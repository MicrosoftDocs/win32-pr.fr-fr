---
description: La fonction GetNPPEtypeSapFilter récupère le filtre ETYPE/SAP à partir d’un objet BLOB donné.
ms.assetid: c4891eff-ab2d-43ff-8d2b-3aa299570c0a
title: GetNPPEtypeSapFilter, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetNPPEtypeSapFilter
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 5359332d96fb85343300c5def12070c812bd99d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535719"
---
# <a name="getnppetypesapfilter-function"></a><span data-ttu-id="6b002-103">GetNPPEtypeSapFilter fonction)</span><span class="sxs-lookup"><span data-stu-id="6b002-103">GetNPPEtypeSapFilter function</span></span>

<span data-ttu-id="6b002-104">La fonction **GetNPPEtypeSapFilter** récupère le filtre ETYPE/SAP à partir d’un objet BLOB donné.</span><span class="sxs-lookup"><span data-stu-id="6b002-104">The **GetNPPEtypeSapFilter** function retrieves the Etype/Sap filter from a given BLOB.</span></span>

## <a name="syntax"></a><span data-ttu-id="6b002-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6b002-105">Syntax</span></span>


```C++
DWORD GetNPPEtypeSapFilter(
  _In_  HBLOB  hBlob,
  _Out_ WORD   *pnSaps,
  _Out_ WORD   *pnEtypes,
  _Out_ LPBYTE *ppSapTable,
  _Out_ LPWORD *ppEtypeTable,
  _Out_ DWORD  *pFilterFlags,
  _Out_ HBLOB  hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="6b002-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6b002-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6b002-107">*hBlob* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6b002-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6b002-108">Handle de l’objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="6b002-108">Handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="6b002-109">*pnSaps* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6b002-109">*pnSaps* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b002-110">Pointeur vers le nombre de protocoles renvoyés dans la table SAP.</span><span class="sxs-lookup"><span data-stu-id="6b002-110">Pointer to the returned number of protocols in the SAP table.</span></span>

</dd> <dt>

<span data-ttu-id="6b002-111">*pnEtypes* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6b002-111">*pnEtypes* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b002-112">Pointeur vers le nombre retourné de ETYPE dans la table ETYPE.</span><span class="sxs-lookup"><span data-stu-id="6b002-112">Pointer to the returned number of Etypes in the Etype table.</span></span>

</dd> <dt>

<span data-ttu-id="6b002-113">*ppSapTable* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6b002-113">*ppSapTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b002-114">Pointeur vers la table SAP retournée.</span><span class="sxs-lookup"><span data-stu-id="6b002-114">Pointer to the returned SAP table.</span></span>

</dd> <dt>

<span data-ttu-id="6b002-115">*ppEtypeTable* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6b002-115">*ppEtypeTable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b002-116">Pointeur vers la table ETYPE retournée.</span><span class="sxs-lookup"><span data-stu-id="6b002-116">Pointer to the returned Etype table.</span></span>

</dd> <dt>

<span data-ttu-id="6b002-117">*pFilterFlags* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6b002-117">*pFilterFlags* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b002-118">Pointeur vers les indicateurs de filtre retournés.</span><span class="sxs-lookup"><span data-stu-id="6b002-118">Pointer to the returned filter flags.</span></span>

</dd> <dt>

<span data-ttu-id="6b002-119">*hErrorBlob* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6b002-119">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6b002-120">Handle vers un objet BLOB d’erreur, qui spécifie l’emplacement dans l’objet BLOB d’origine où l’erreur (le cas échéant) s’est produite.</span><span class="sxs-lookup"><span data-stu-id="6b002-120">Handle to an error BLOB, which specifies the location in the original BLOB where the error (if any) occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6b002-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6b002-121">Return value</span></span>

<span data-ttu-id="6b002-122">Si la fonction réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="6b002-122">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="6b002-123">Si la fonction échoue, la valeur de retour est une valeur NMERR qui indique l’erreur.</span><span class="sxs-lookup"><span data-stu-id="6b002-123">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="6b002-124">Notes</span><span class="sxs-lookup"><span data-stu-id="6b002-124">Remarks</span></span>

<span data-ttu-id="6b002-125">Les informations ETYPE/SAP sont stockées dans la catégorie de **configuration** de la section **propriétaire** NPP.</span><span class="sxs-lookup"><span data-stu-id="6b002-125">The Etype/Sap information is stored in the **Config** category of the NPP **Owner** section.</span></span>

## <a name="requirements"></a><span data-ttu-id="6b002-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6b002-126">Requirements</span></span>



| <span data-ttu-id="6b002-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6b002-127">Requirement</span></span> | <span data-ttu-id="6b002-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="6b002-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6b002-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6b002-129">Minimum supported client</span></span><br/> | <span data-ttu-id="6b002-130">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6b002-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="6b002-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6b002-131">Minimum supported server</span></span><br/> | <span data-ttu-id="6b002-132">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6b002-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6b002-133">En-tête</span><span class="sxs-lookup"><span data-stu-id="6b002-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="6b002-134"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="6b002-134"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="6b002-135">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6b002-135">Library</span></span><br/>                  | <dl> <span data-ttu-id="6b002-136"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6b002-136"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="6b002-137">DLL</span><span class="sxs-lookup"><span data-stu-id="6b002-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6b002-138"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6b002-138"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6b002-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6b002-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6b002-140">SetNPPEtypeSapFilter</span><span class="sxs-lookup"><span data-stu-id="6b002-140">SetNPPEtypeSapFilter</span></span>](setnppetypesapfilter.md)
</dt> </dl>

 

 




