---
description: Retourne le type de périphérique matériel que l’objet tablette représente, par exemple Mouse, Pen ou Touch.
ms.assetid: 693cb45f-958d-42e2-a3ee-a7cfcc72e5c3
title: 'ITablet2 :: GetDeviceKind, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITablet2.GetDeviceKind
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: f20b1fe6a5a48196f6b3adc5982f2596d93f0863
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106519367"
---
# <a name="itablet2getdevicekind-method"></a><span data-ttu-id="cd57c-103">ITablet2 :: GetDeviceKind, méthode</span><span class="sxs-lookup"><span data-stu-id="cd57c-103">ITablet2::GetDeviceKind method</span></span>

<span data-ttu-id="cd57c-104">Retourne le type de périphérique matériel que l’objet tablette représente, par exemple Mouse, Pen ou Touch.</span><span class="sxs-lookup"><span data-stu-id="cd57c-104">Returns the type of hardware device the tablet object represents such as mouse, pen or touch.</span></span>

## <a name="syntax"></a><span data-ttu-id="cd57c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="cd57c-105">Syntax</span></span>


```C++
HRESULT GetDeviceKind(
  [out] TABLET_DEVICE_KIND *pKind
);
```



## <a name="parameters"></a><span data-ttu-id="cd57c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="cd57c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cd57c-107">*pKind* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="cd57c-107">*pKind* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cd57c-108">Valeur d’énumération qui indique le type de tablette, par exemple la souris, le stylet ou le toucher.</span><span class="sxs-lookup"><span data-stu-id="cd57c-108">Enumeration value that indicates the type of tablet such as mouse, pen or touch.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cd57c-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="cd57c-109">Return value</span></span>

<span data-ttu-id="cd57c-110">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="cd57c-110">This method can return one of these values.</span></span>



| <span data-ttu-id="cd57c-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="cd57c-111">Return code</span></span>                                                                            | <span data-ttu-id="cd57c-112">Description</span><span class="sxs-lookup"><span data-stu-id="cd57c-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="cd57c-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="cd57c-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="cd57c-114">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="cd57c-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="cd57c-115"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="cd57c-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="cd57c-116">Une erreur non spécifiée s'est produite.</span><span class="sxs-lookup"><span data-stu-id="cd57c-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="cd57c-117">Notes</span><span class="sxs-lookup"><span data-stu-id="cd57c-117">Remarks</span></span>

<span data-ttu-id="cd57c-118">Cette interface et cette méthode ont été introduites dans Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="cd57c-118">This interface and method were introduced in Windows Vista.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd57c-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="cd57c-119">Requirements</span></span>



| <span data-ttu-id="cd57c-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="cd57c-120">Requirement</span></span> | <span data-ttu-id="cd57c-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="cd57c-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="cd57c-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cd57c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="cd57c-123">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="cd57c-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="cd57c-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="cd57c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="cd57c-125">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="cd57c-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="cd57c-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="cd57c-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="cd57c-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cd57c-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd57c-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="cd57c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd57c-129">**Interface ITablet2**</span><span class="sxs-lookup"><span data-stu-id="cd57c-129">**ITablet2 Interface**</span></span>](itablet2.md)
</dt> <dt>

[<span data-ttu-id="cd57c-130">**\_Énumération de type d’appareil tablette \_**</span><span class="sxs-lookup"><span data-stu-id="cd57c-130">**TABLET\_DEVICE\_KIND Enumeration**</span></span>](tablet-device-kind.md)
</dt> <dt>

[<span data-ttu-id="cd57c-131">**Interface ITablet**</span><span class="sxs-lookup"><span data-stu-id="cd57c-131">**ITablet Interface**</span></span>](itablet.md)
</dt> </dl>

 

 




