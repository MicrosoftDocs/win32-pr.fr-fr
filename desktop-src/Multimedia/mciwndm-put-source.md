---
title: Message MCIWNDM_PUT_SOURCE (VFW. h)
description: Le \_ \_ message source MCIWNDM place redéfinit les coordonnées du rectangle source utilisé pour le rognage des images d’un fichier AVI lors de la lecture. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro MCIWndPutSource.
ms.assetid: cff95139-0302-4db3-bf2e-559e75257e85
keywords:
- Message MCIWNDM_PUT_SOURCE Windows Multimedia
topic_type:
- apiref
api_name:
- MCIWNDM_PUT_SOURCE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5407f420b8def6dda9795e87eb68943c9373b143
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103739813"
---
# <a name="mciwndm_put_source-message"></a><span data-ttu-id="2e387-105">MCIWNDM \_ Placer le \_ message source</span><span class="sxs-lookup"><span data-stu-id="2e387-105">MCIWNDM\_PUT\_SOURCE message</span></span>

<span data-ttu-id="2e387-106">Le **message \_ \_ source MCIWNDM place** redéfinit les coordonnées du rectangle source utilisé pour le rognage des images d’un fichier AVI lors de la lecture.</span><span class="sxs-lookup"><span data-stu-id="2e387-106">The **MCIWNDM\_PUT\_SOURCE** message redefines the coordinates of the source rectangle used for cropping the images of an AVI file during playback.</span></span> <span data-ttu-id="2e387-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**MCIWndPutSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndputsource) .</span><span class="sxs-lookup"><span data-stu-id="2e387-107">You can send this message explicitly or by using the [**MCIWndPutSource**](/windows/desktop/api/Vfw/nf-vfw-mciwndputsource) macro.</span></span>


```C++
MCIWNDM_PUT_SOURCE 
wParam = 0; 
lParam = (LPARAM) (LPRECT) prc; 
```



## <a name="parameters"></a><span data-ttu-id="2e387-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2e387-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e387-109"><span id="prc"></span><span id="PRC"></span>*République*</span><span class="sxs-lookup"><span data-stu-id="2e387-109"><span id="prc"></span><span id="PRC"></span>*prc*</span></span>
</dt> <dd>

<span data-ttu-id="2e387-110">Pointeur vers une structure [Rect](/previous-versions//ms536136(v=vs.85)) contenant les coordonnées du rectangle source.</span><span class="sxs-lookup"><span data-stu-id="2e387-110">Pointer to a [RECT](/previous-versions//ms536136(v=vs.85)) structure containing the coordinates of the source rectangle.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e387-111">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="2e387-111">Return Value</span></span>

<span data-ttu-id="2e387-112">Retourne zéro en cas de réussite ou une erreur.</span><span class="sxs-lookup"><span data-stu-id="2e387-112">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e387-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2e387-113">Requirements</span></span>



| <span data-ttu-id="2e387-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2e387-114">Requirement</span></span> | <span data-ttu-id="2e387-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="2e387-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="2e387-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e387-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2e387-117">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2e387-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="2e387-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2e387-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2e387-119">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2e387-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="2e387-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="2e387-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2e387-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e387-121"><dt>Vfw.h</dt></span></span> </dl> |



 

