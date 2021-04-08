---
description: Retourne une valeur qui représente les fonctionnalités du matériel de tablette.
ms.assetid: 68936dab-3df4-42c4-9945-bcd525c996f3
title: 'ITablet :: GetHardwareCaps, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet.GetHardwareCaps
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: 5ada3ad58699952bac5458ddd079abaf84f63bf2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867722"
---
# <a name="itabletgethardwarecaps-method"></a><span data-ttu-id="6731e-103">ITablet :: GetHardwareCaps, méthode</span><span class="sxs-lookup"><span data-stu-id="6731e-103">ITablet::GetHardwareCaps method</span></span>

<span data-ttu-id="6731e-104">Retourne une valeur qui représente les fonctionnalités du matériel de tablette.</span><span class="sxs-lookup"><span data-stu-id="6731e-104">Returns a value that represents the capabilities of the tablet hardware.</span></span>

## <a name="syntax"></a><span data-ttu-id="6731e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6731e-105">Syntax</span></span>


```C++
HRESULT GetHardwareCaps(
  [out] DWORD *pdwCaps
);
```



## <a name="parameters"></a><span data-ttu-id="6731e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6731e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6731e-107">*pdwCaps* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="6731e-107">*pdwCaps* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6731e-108">Indicateurs binaires qui représentent les fonctionnalités du matériel de tablette.</span><span class="sxs-lookup"><span data-stu-id="6731e-108">Bit flags that represent the capabilities of the tablet hardware.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6731e-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6731e-109">Return value</span></span>

<span data-ttu-id="6731e-110">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="6731e-110">This method can return one of these values.</span></span>



| <span data-ttu-id="6731e-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="6731e-111">Return code</span></span>                                                                            | <span data-ttu-id="6731e-112">Description</span><span class="sxs-lookup"><span data-stu-id="6731e-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="6731e-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6731e-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="6731e-114">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="6731e-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="6731e-115"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="6731e-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="6731e-116">Une erreur non spécifiée s'est produite.</span><span class="sxs-lookup"><span data-stu-id="6731e-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6731e-117">Notes</span><span class="sxs-lookup"><span data-stu-id="6731e-117">Remarks</span></span>

<span data-ttu-id="6731e-118">Le paramètre *pdwCaps* est un jeu d’indicateurs binaires qui décrivent les fonctionnalités matérielles de Tablet PC.</span><span class="sxs-lookup"><span data-stu-id="6731e-118">The *pdwCaps* parameter is a set of bit flags that describe tablet hardware capabilities.</span></span> <span data-ttu-id="6731e-119">Le tableau suivant décrit ces indicateurs.</span><span class="sxs-lookup"><span data-stu-id="6731e-119">The following table describes these flags.</span></span>



| <span data-ttu-id="6731e-120">Nom de l’indicateur</span><span class="sxs-lookup"><span data-stu-id="6731e-120">Flag Name</span></span>                         | <span data-ttu-id="6731e-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="6731e-121">Value</span></span>                 | <span data-ttu-id="6731e-122">Description</span><span class="sxs-lookup"><span data-stu-id="6731e-122">Description</span></span>                                                                                                                    |
|-----------------------------------|-----------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6731e-123">THWC \_ intégré</span><span class="sxs-lookup"><span data-stu-id="6731e-123">THWC\_INTEGRATED</span></span><br/>       | <span data-ttu-id="6731e-124">0x00000001</span><span class="sxs-lookup"><span data-stu-id="6731e-124">0x00000001</span></span><br/> | <span data-ttu-id="6731e-125">Indique que l’affichage et le digitaliseur partagent la même surface.</span><span class="sxs-lookup"><span data-stu-id="6731e-125">Indicates that the display and digitizer share the same surface.</span></span><br/>                                                    |
| <span data-ttu-id="6731e-126">THWC \_ CSR \_ doit \_ toucher</span><span class="sxs-lookup"><span data-stu-id="6731e-126">THWC\_CSR\_MUST\_TOUCH</span></span><br/> | <span data-ttu-id="6731e-127">0x00000002</span><span class="sxs-lookup"><span data-stu-id="6731e-127">0x00000002</span></span><br/> | <span data-ttu-id="6731e-128">Indique que le curseur doit être dans un contact physique avec l’appareil pour signaler la position.</span><span class="sxs-lookup"><span data-stu-id="6731e-128">Indicates that the cursor must be in physical contact with the device to report position.</span></span><br/>                           |
| <span data-ttu-id="6731e-129">\_proximité THWC \_</span><span class="sxs-lookup"><span data-stu-id="6731e-129">THWC\_HARD\_PROXIMITY</span></span><br/>  | <span data-ttu-id="6731e-130">0x00000004</span><span class="sxs-lookup"><span data-stu-id="6731e-130">0x00000004</span></span><br/> | <span data-ttu-id="6731e-131">Indique que l’appareil peut générer des événements lorsque le curseur entre en entrée et en quittant la plage de détection physique.</span><span class="sxs-lookup"><span data-stu-id="6731e-131">Indicates that the device can generate events when the cursor is entering and leaving the physical detection range.</span></span><br/> |
| <span data-ttu-id="6731e-132">THWC \_ PHYSID \_ CSR</span><span class="sxs-lookup"><span data-stu-id="6731e-132">THWC\_PHYSID\_CSRS</span></span><br/>     | <span data-ttu-id="6731e-133">0x00000008</span><span class="sxs-lookup"><span data-stu-id="6731e-133">0x00000008</span></span><br/> | <span data-ttu-id="6731e-134">Indique que l’appareil peut identifier de manière unique le curseur actif dans le matériel.</span><span class="sxs-lookup"><span data-stu-id="6731e-134">Indicates that the device can uniquely identify the active cursor in hardware.</span></span><br/>                                      |



 

## <a name="requirements"></a><span data-ttu-id="6731e-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6731e-135">Requirements</span></span>



| <span data-ttu-id="6731e-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6731e-136">Requirement</span></span> | <span data-ttu-id="6731e-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="6731e-137">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6731e-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6731e-138">Minimum supported client</span></span><br/> | <span data-ttu-id="6731e-139">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6731e-139">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="6731e-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6731e-140">Minimum supported server</span></span><br/> | <span data-ttu-id="6731e-141">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="6731e-141">None supported</span></span><br/>                                                              |
| <span data-ttu-id="6731e-142">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="6731e-142">Library</span></span><br/>                  | <dl> <span data-ttu-id="6731e-143"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6731e-143"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6731e-144">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6731e-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6731e-145">**Interface ITablet**</span><span class="sxs-lookup"><span data-stu-id="6731e-145">**ITablet Interface**</span></span>](itablet.md)
</dt> </dl>

 

 




