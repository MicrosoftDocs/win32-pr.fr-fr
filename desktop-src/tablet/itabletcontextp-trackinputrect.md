---
description: Met à jour les coordonnées du mappage de l’emplacement des fenêtres dans le digitaliseur de tablette.
ms.assetid: 2984b87b-620e-4e5d-a3cc-4c3f4c89bae3
title: 'ITabletContextP :: TrackInputRect, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletContextP.TrackInputRect
api_type:
- COM
api_location:
- Wisptis.exe
- Wisptis.exe.dll
ms.openlocfilehash: 4529263b81933651db35b88262b11e979d39e6f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528335"
---
# <a name="itabletcontextptrackinputrect-method"></a><span data-ttu-id="53cf0-103">ITabletContextP :: TrackInputRect, méthode</span><span class="sxs-lookup"><span data-stu-id="53cf0-103">ITabletContextP::TrackInputRect method</span></span>

<span data-ttu-id="53cf0-104">Met à jour les coordonnées du mappage de l’emplacement des fenêtres dans le digitaliseur de tablette.</span><span class="sxs-lookup"><span data-stu-id="53cf0-104">Updates the tablet digitizer to window location mapping coordinates.</span></span>

## <a name="syntax"></a><span data-ttu-id="53cf0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="53cf0-105">Syntax</span></span>


```C++
HRESULT TrackInputRect(
  [out] RECT *prcInput
);
```



## <a name="parameters"></a><span data-ttu-id="53cf0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="53cf0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53cf0-107">*prcInput* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="53cf0-107">*prcInput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="53cf0-108">Nouveau rectangle de la fenêtre d’entrée après la mise à jour du mappage entre les coordonnées de la fenêtre et du digitaliseur.</span><span class="sxs-lookup"><span data-stu-id="53cf0-108">The new input window rectangle after updating the mapping between the window and digitizer coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53cf0-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="53cf0-109">Return value</span></span>

<span data-ttu-id="53cf0-110">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="53cf0-110">This method can return one of these values.</span></span>



| <span data-ttu-id="53cf0-111">Code de retour</span><span class="sxs-lookup"><span data-stu-id="53cf0-111">Return code</span></span>                                                                            | <span data-ttu-id="53cf0-112">Description</span><span class="sxs-lookup"><span data-stu-id="53cf0-112">Description</span></span>                               |
|----------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <span data-ttu-id="53cf0-113"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="53cf0-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="53cf0-114">Opération réussie.</span><span class="sxs-lookup"><span data-stu-id="53cf0-114">Success.</span></span><br/>                       |
| <dl> <span data-ttu-id="53cf0-115"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="53cf0-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="53cf0-116">Une erreur non spécifiée s'est produite.</span><span class="sxs-lookup"><span data-stu-id="53cf0-116">An unspecified error occurred.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="53cf0-117">Notes</span><span class="sxs-lookup"><span data-stu-id="53cf0-117">Remarks</span></span>

<span data-ttu-id="53cf0-118">Appelez cette méthode chaque fois que l’emplacement de la fenêtre à l’écran change.</span><span class="sxs-lookup"><span data-stu-id="53cf0-118">Call this method anytime the location of the window on the screen changes.</span></span>

## <a name="requirements"></a><span data-ttu-id="53cf0-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="53cf0-119">Requirements</span></span>



| <span data-ttu-id="53cf0-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="53cf0-120">Requirement</span></span> | <span data-ttu-id="53cf0-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="53cf0-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="53cf0-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53cf0-122">Minimum supported client</span></span><br/> | <span data-ttu-id="53cf0-123">Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="53cf0-123">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="53cf0-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="53cf0-124">Minimum supported server</span></span><br/> | <span data-ttu-id="53cf0-125">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="53cf0-125">None supported</span></span><br/>                                                              |
| <span data-ttu-id="53cf0-126">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="53cf0-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="53cf0-127"><dt>Wisptis.exe</dt></span><span class="sxs-lookup"><span data-stu-id="53cf0-127"><dt>Wisptis.exe</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53cf0-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="53cf0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53cf0-129">**Interface ITabletContextP**</span><span class="sxs-lookup"><span data-stu-id="53cf0-129">**ITabletContextP Interface**</span></span>](itabletcontextp.md)
</dt> </dl>

 

 




