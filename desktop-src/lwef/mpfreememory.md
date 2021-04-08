---
title: MpFreeMemory, fonction (MpClient. h)
description: Libère de la mémoire pour le gestionnaire de protection contre les programmes malveillants.
ms.assetid: D0B43AE5-756F-4E86-B8A5-8268A41901BC
keywords:
- Fonctionnalités d’environnement Windows hérités de la fonction MpFreeMemory
topic_type:
- apiref
api_name:
- MpFreeMemory
api_location:
- MpClient.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a15a2845b034a3aa739b1ba2f33a023b742b4b22
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741012"
---
# <a name="mpfreememory-function"></a><span data-ttu-id="9d329-104">MpFreeMemory fonction)</span><span class="sxs-lookup"><span data-stu-id="9d329-104">MpFreeMemory function</span></span>

<span data-ttu-id="9d329-105">Libère de la mémoire pour le gestionnaire de protection contre les programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="9d329-105">Frees memory for the malware protection manager.</span></span> <span data-ttu-id="9d329-106">Toutes les mémoires tampons allouées et renvoyées par les fonctions de protection contre les programmes malveillants doivent être libérées par l’appelant à l’aide de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="9d329-106">All buffers allocated and returned by malware protection functions must be freed by the caller using this function.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d329-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9d329-107">Syntax</span></span>


```C++
void WINAPI MpFreeMemory(
  _In_ PVOID pMemory
);
```



## <a name="parameters"></a><span data-ttu-id="9d329-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9d329-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d329-109">*pMemory* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9d329-109">*pMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9d329-110">Type : **pVoid**</span><span class="sxs-lookup"><span data-stu-id="9d329-110">Type: **PVOID**</span></span>

<span data-ttu-id="9d329-111">Pointeur vers la mémoire allouée par une fonction de protection contre les programmes malveillants.</span><span class="sxs-lookup"><span data-stu-id="9d329-111">A pointer to memory allocated by a malware protection function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d329-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="9d329-112">Return value</span></span>

<span data-ttu-id="9d329-113">Cette fonction ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="9d329-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d329-114">Notes</span><span class="sxs-lookup"><span data-stu-id="9d329-114">Remarks</span></span>

<span data-ttu-id="9d329-115">Pour faciliter la gestion de la mémoire pour les clients, le gestionnaire de protection contre les programmes malveillants définit également des macros pour libérer la mémoire associée aux différentes structures renvoyées par les fonctions de protection contre les programmes malveillants</span><span class="sxs-lookup"><span data-stu-id="9d329-115">To facilitate memory management for clients, the malware protection manager also defines macros to free memory associated with various structures returned by malware protection functions.</span></span> <span data-ttu-id="9d329-116">Les macros suivantes sont définies dans le fichier d’en-tête mpmemfree. h :</span><span class="sxs-lookup"><span data-stu-id="9d329-116">The following macros are defined in the header file mpmemfree.h:</span></span>



| <span data-ttu-id="9d329-117">Nom</span><span class="sxs-lookup"><span data-stu-id="9d329-117">Name</span></span>                            | <span data-ttu-id="9d329-118">Description</span><span class="sxs-lookup"><span data-stu-id="9d329-118">Description</span></span>                                                                      |
|---------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="9d329-119">MPRESOURCE \_ informations \_ gratuites</span><span class="sxs-lookup"><span data-stu-id="9d329-119">MPRESOURCE\_INFO\_FREE</span></span>          | <span data-ttu-id="9d329-120">Libère des [**\_ informations MPRESOURCE**](mpresource-info.md)allouées.</span><span class="sxs-lookup"><span data-stu-id="9d329-120">Frees an allocated [**MPRESOURCE\_INFO**](mpresource-info.md).</span></span>                  |
| <span data-ttu-id="9d329-121">MPTHREAT \_ informations \_ gratuites</span><span class="sxs-lookup"><span data-stu-id="9d329-121">MPTHREAT\_INFO\_FREE</span></span>            | <span data-ttu-id="9d329-122">Libère des [**\_ informations MPTHREAT**](mpthreat-info.md)allouées.</span><span class="sxs-lookup"><span data-stu-id="9d329-122">Frees an allocated [**MPTHREAT\_INFO**](mpthreat-info.md).</span></span>                      |
| <span data-ttu-id="9d329-123">MPTHREAT \_ \_ informations localisées \_ gratuites</span><span class="sxs-lookup"><span data-stu-id="9d329-123">MPTHREAT\_LOCALIZED\_INFO\_FREE</span></span> | <span data-ttu-id="9d329-124">Libère des [**\_ \_ informations localisées MPTHREAT**](mpthreat-localized-info.md)allouées.</span><span class="sxs-lookup"><span data-stu-id="9d329-124">Frees an allocated [**MPTHREAT\_LOCALIZED\_INFO**](mpthreat-localized-info.md).</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="9d329-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9d329-125">Requirements</span></span>



| <span data-ttu-id="9d329-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9d329-126">Requirement</span></span> | <span data-ttu-id="9d329-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="9d329-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9d329-128">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d329-128">Minimum supported client</span></span><br/> | <span data-ttu-id="9d329-129">Applications de \[ Bureau Windows 8 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9d329-129">Windows 8 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="9d329-130">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9d329-130">Minimum supported server</span></span><br/> | <span data-ttu-id="9d329-131">Applications de bureau Windows Server 2012 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9d329-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="9d329-132">En-tête</span><span class="sxs-lookup"><span data-stu-id="9d329-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d329-133"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d329-133"><dt>MpClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="9d329-134">DLL</span><span class="sxs-lookup"><span data-stu-id="9d329-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9d329-135"><dt>MpClient.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9d329-135"><dt>MpClient.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d329-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9d329-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d329-137">**MpErrorMessageFormat**</span><span class="sxs-lookup"><span data-stu-id="9d329-137">**MpErrorMessageFormat**</span></span>](mperrormessageformat.md)
</dt> <dt>

[<span data-ttu-id="9d329-138">**\_informations MPRESOURCE**</span><span class="sxs-lookup"><span data-stu-id="9d329-138">**MPRESOURCE\_INFO**</span></span>](mpresource-info.md)
</dt> <dt>

[<span data-ttu-id="9d329-139">**\_informations MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="9d329-139">**MPTHREAT\_INFO**</span></span>](mpthreat-info.md)
</dt> <dt>

[<span data-ttu-id="9d329-140">**\_informations localisées \_ MPTHREAT**</span><span class="sxs-lookup"><span data-stu-id="9d329-140">**MPTHREAT\_LOCALIZED\_INFO**</span></span>](mpthreat-localized-info.md)
</dt> </dl>

 

 





