---
title: IMAGELISTSTATEFLAGS (commctrl. h)
description: Les indicateurs suivants sont passés à la méthode IImageList Draw dans le membre fState de IMAGELISTDRAWPARAMS.
ms.assetid: a22b4acf-c290-44b2-9216-b006d0326236
topic_type:
- apiref
api_name:
- ILS_NORMAL
- ILS_GLOW
- ILS_SHADOW
- ILS_SATURATE
- ILS_ALPHA
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fea580294f54b6e2fc5c3e5b6aee1119811c22e8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032695"
---
# <a name="imageliststateflags"></a><span data-ttu-id="b43d9-103">IMAGELISTSTATEFLAGS</span><span class="sxs-lookup"><span data-stu-id="b43d9-103">IMAGELISTSTATEFLAGS</span></span>

<span data-ttu-id="b43d9-104">Les indicateurs suivants sont passés à la méthode [**IImageList ::D RAW**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-draw) dans le membre **fState** de [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams).</span><span class="sxs-lookup"><span data-stu-id="b43d9-104">The following flags are passed to the [**IImageList::Draw**](/windows/desktop/api/CommonControls/nf-commoncontrols-iimagelist-draw) method in the **fState** member of [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams).</span></span>



| <span data-ttu-id="b43d9-105">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="b43d9-105">Constant/value</span></span>                                                                                                                                                                                                             | <span data-ttu-id="b43d9-106">Description</span><span class="sxs-lookup"><span data-stu-id="b43d9-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                   |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ILS_NORMAL"></span><span id="ils_normal"></span><dl> <span data-ttu-id="b43d9-107"><dt>**Ils \_ NORMAL**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="b43d9-107"><dt>**ILS\_NORMAL**</dt> <dt>0x00000000</dt></span></span> </dl>       | <span data-ttu-id="b43d9-108">L’état de l’image n’est pas modifié.</span><span class="sxs-lookup"><span data-stu-id="b43d9-108">The image state is not modified.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                   |
| <span id="ILS_GLOW"></span><span id="ils_glow"></span><dl> <span data-ttu-id="b43d9-109"><dt>**Ils \_ ÉCLAT**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="b43d9-109"><dt>**ILS\_GLOW**</dt> <dt>0x00000001</dt></span></span> </dl>             | <span data-ttu-id="b43d9-110">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="b43d9-110">Not supported.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="ILS_SHADOW"></span><span id="ils_shadow"></span><dl> <span data-ttu-id="b43d9-111"><dt>**Ils \_ OMBRE**</dt> <dt></dt> dépendante</span><span class="sxs-lookup"><span data-stu-id="b43d9-111"><dt>**ILS\_SHADOW**</dt> <dt>0x00000002</dt></span></span> </dl>       | <span data-ttu-id="b43d9-112">Non pris en charge.</span><span class="sxs-lookup"><span data-stu-id="b43d9-112">Not supported.</span></span> <br/>                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="ILS_SATURATE"></span><span id="ils_saturate"></span><dl> <span data-ttu-id="b43d9-113"><dt>**Ils \_ SATURATION**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="b43d9-113"><dt>**ILS\_SATURATE**</dt> <dt>0x00000004</dt></span></span> </dl> | <span data-ttu-id="b43d9-114">Réduit la saturation de la couleur de l’icône à des nuances de gris.</span><span class="sxs-lookup"><span data-stu-id="b43d9-114">Reduces the color saturation of the icon to grayscale.</span></span> <span data-ttu-id="b43d9-115">Cela affecte uniquement les images 32bpp.</span><span class="sxs-lookup"><span data-stu-id="b43d9-115">This only affects 32bpp images.</span></span> <br/>                                                                                                                                                                                                                                                                                            |
| <span id="ILS_ALPHA"></span><span id="ils_alpha"></span><dl> <span data-ttu-id="b43d9-116"><dt>**Ils \_ ALPHA**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="b43d9-116"><dt>**ILS\_ALPHA**</dt> <dt>0x00000008</dt></span></span> </dl>          | <span data-ttu-id="b43d9-117">Alpha fusionne l’icône.</span><span class="sxs-lookup"><span data-stu-id="b43d9-117">Alpha blends the icon.</span></span> <span data-ttu-id="b43d9-118">La fusion alpha contrôle le niveau de transparence d’une icône, en fonction de la valeur de son canal alpha.</span><span class="sxs-lookup"><span data-stu-id="b43d9-118">Alpha blending controls the transparency level of an icon, according to the value of its alpha channel.</span></span> <span data-ttu-id="b43d9-119">La valeur du canal alpha est indiquée par le membre **Frame** dans la méthode [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams) .</span><span class="sxs-lookup"><span data-stu-id="b43d9-119">The value of the alpha channel is indicated by the **frame** member in the [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams) method.</span></span> <span data-ttu-id="b43d9-120">Le canal alpha peut être compris entre 0 et 255, 0 étant complètement transparent, et 255 entièrement opaque.</span><span class="sxs-lookup"><span data-stu-id="b43d9-120">The alpha channel can be from 0 to 255, with 0 being completely transparent, and 255 being completely opaque.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="b43d9-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b43d9-121">Requirements</span></span>



| <span data-ttu-id="b43d9-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b43d9-122">Requirement</span></span> | <span data-ttu-id="b43d9-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="b43d9-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b43d9-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b43d9-124">Minimum supported client</span></span><br/> | <span data-ttu-id="b43d9-125">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b43d9-125">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="b43d9-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b43d9-126">Minimum supported server</span></span><br/> | <span data-ttu-id="b43d9-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b43d9-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="b43d9-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="b43d9-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="b43d9-129"><dt>Commctrl. h</dt></span><span class="sxs-lookup"><span data-stu-id="b43d9-129"><dt>Commctrl.h</dt></span></span> </dl> |



 

