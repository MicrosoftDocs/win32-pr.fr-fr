---
description: Définit le filtre ETYPE/SAP de l’objet BLOB.
ms.assetid: cd659c93-3415-4737-b848-936e80318544
title: SetNPPEtypeSapFilter, fonction (NetMon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SetNPPEtypeSapFilter
api_type:
- DllExport
api_location:
- Npptools.dll
ms.openlocfilehash: 14657536e09b65912afa1715c296663d8d1916b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318961"
---
# <a name="setnppetypesapfilter-function"></a><span data-ttu-id="79e90-103">SetNPPEtypeSapFilter fonction)</span><span class="sxs-lookup"><span data-stu-id="79e90-103">SetNPPEtypeSapFilter function</span></span>

<span data-ttu-id="79e90-104">La fonction **SetNPPEtypeSapFilter** définit le filtre ETYPE/SAP de l’objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="79e90-104">The **SetNPPEtypeSapFilter** function sets the BLOB Etype/Sap filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="79e90-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="79e90-105">Syntax</span></span>


```C++
DWORD SetNPPEtypeSapFilter(
  _In_  HBLOB  hBlob,
  _In_  WORD   nSaps,
  _In_  WORD   nEtypes,
  _In_  LPBYTE lpSapTable,
  _In_  LPWORD lpEtypeTable,
  _In_  DWORD  FilterFlags,
  _Out_ HBLOB  hErrorBlob
);
```



## <a name="parameters"></a><span data-ttu-id="79e90-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="79e90-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="79e90-107">*hBlob* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="79e90-107">*hBlob* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79e90-108">Handle de l’objet BLOB.</span><span class="sxs-lookup"><span data-stu-id="79e90-108">A handle to the BLOB.</span></span>

</dd> <dt>

<span data-ttu-id="79e90-109">*nSaps* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="79e90-109">*nSaps* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79e90-110">Nombre de SAP.</span><span class="sxs-lookup"><span data-stu-id="79e90-110">The number of SAPs.</span></span>

</dd> <dt>

<span data-ttu-id="79e90-111">*nEtypes* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="79e90-111">*nEtypes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79e90-112">Nombre de ETYPE dans la table ETYPE en cours de définition.</span><span class="sxs-lookup"><span data-stu-id="79e90-112">The number of Etypes in the Etype table being set.</span></span>

</dd> <dt>

<span data-ttu-id="79e90-113">*lpSapTable* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="79e90-113">*lpSapTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79e90-114">Pointeur vers la table SAP qui est définie.</span><span class="sxs-lookup"><span data-stu-id="79e90-114">A pointer to the SAP table that is set.</span></span>

</dd> <dt>

<span data-ttu-id="79e90-115">*lpEtypeTable* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="79e90-115">*lpEtypeTable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79e90-116">Pointeur vers la table ETYPE qui est définie.</span><span class="sxs-lookup"><span data-stu-id="79e90-116">A pointer to the Etype table that is set.</span></span>

</dd> <dt>

<span data-ttu-id="79e90-117">*FilterFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="79e90-117">*FilterFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="79e90-118">Indicateurs de filtre définis.</span><span class="sxs-lookup"><span data-stu-id="79e90-118">The filter flags that are set.</span></span>

</dd> <dt>

<span data-ttu-id="79e90-119">*hErrorBlob* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="79e90-119">*hErrorBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="79e90-120">Handle d’un objet BLOB d’erreurs qui spécifie à quel endroit de l’objet BLOB d’origine l’erreur (le cas échéant) s’est produite.</span><span class="sxs-lookup"><span data-stu-id="79e90-120">The handle to an error BLOB that specifies where in the original BLOB the error (if any) occurred.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="79e90-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="79e90-121">Return value</span></span>

<span data-ttu-id="79e90-122">Si la fonction réussit, la valeur de retour est NMERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="79e90-122">If the function is successful, the return value is NMERR\_SUCCESS.</span></span>

<span data-ttu-id="79e90-123">Si la fonction échoue, la valeur de retour est une valeur NMERR qui indique l’erreur.</span><span class="sxs-lookup"><span data-stu-id="79e90-123">If the function is unsuccessful, the return value is a NMERR value that indicates the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="79e90-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="79e90-124">Requirements</span></span>



| <span data-ttu-id="79e90-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="79e90-125">Requirement</span></span> | <span data-ttu-id="79e90-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="79e90-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="79e90-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="79e90-127">Minimum supported client</span></span><br/> | <span data-ttu-id="79e90-128">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="79e90-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="79e90-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="79e90-129">Minimum supported server</span></span><br/> | <span data-ttu-id="79e90-130">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="79e90-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="79e90-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="79e90-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="79e90-132"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="79e90-132"><dt>Netmon.h</dt></span></span> </dl>     |
| <span data-ttu-id="79e90-133">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="79e90-133">Library</span></span><br/>                  | <dl> <span data-ttu-id="79e90-134"><dt>Npptools. lib</dt></span><span class="sxs-lookup"><span data-stu-id="79e90-134"><dt>Npptools.lib</dt></span></span> </dl> |
| <span data-ttu-id="79e90-135">DLL</span><span class="sxs-lookup"><span data-stu-id="79e90-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="79e90-136"><dt>Npptools.dll</dt></span><span class="sxs-lookup"><span data-stu-id="79e90-136"><dt>Npptools.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79e90-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="79e90-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79e90-138">GetNPPEtypeSapFilter</span><span class="sxs-lookup"><span data-stu-id="79e90-138">GetNPPEtypeSapFilter</span></span>](getnppetypesapfilter.md)
</dt> </dl>

 

 




