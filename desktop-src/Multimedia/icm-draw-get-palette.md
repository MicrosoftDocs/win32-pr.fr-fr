---
title: Message ICM_DRAW_GET_PALETTE (VFW. h)
description: Le message de la \_ palette de dessin ICM \_ \_ demande à un pilote de rendu de retourner une palette.
ms.assetid: 02a9df7d-e0b9-4bde-9cda-c36d2a10a23c
keywords:
- Message ICM_DRAW_GET_PALETTE Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DRAW_GET_PALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a03f3658d2a2653f940e18e9b82b7cc3d7690ad2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032475"
---
# <a name="icm_draw_get_palette-message"></a><span data-ttu-id="b2c7b-104">Message d’extraction de la \_ \_ \_ palette ICM</span><span class="sxs-lookup"><span data-stu-id="b2c7b-104">ICM\_DRAW\_GET\_PALETTE message</span></span>

<span data-ttu-id="b2c7b-105">Le message de la **\_ \_ \_ palette de dessin ICM** demande à un pilote de rendu de retourner une palette.</span><span class="sxs-lookup"><span data-stu-id="b2c7b-105">The **ICM\_DRAW\_GET\_PALETTE** message requests a rendering driver to return a palette.</span></span>


```C++
ICM_DRAW_GET_PALETTE 
wParam = 0; 
lParam = 0; 
```



## <a name="return-value"></a><span data-ttu-id="b2c7b-106">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="b2c7b-106">Return Value</span></span>

<span data-ttu-id="b2c7b-107">Le pilote doit retourner l’un des éléments suivants : un descripteur de la palette utilisée, **null** s’il n’a pas de handle à retourner, ou ICERR non \_ pris en charge s’il ne prend pas en charge les palettes.</span><span class="sxs-lookup"><span data-stu-id="b2c7b-107">The driver should return one of the following: a handle of the palette being used, **NULL** if it doesn't have a handle to return, or ICERR\_UNSUPPORTED if it doesn't support palettes.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2c7b-108">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b2c7b-108">Requirements</span></span>



| <span data-ttu-id="b2c7b-109">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b2c7b-109">Requirement</span></span> | <span data-ttu-id="b2c7b-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="b2c7b-110">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b2c7b-111">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b2c7b-111">Minimum supported client</span></span><br/> | <span data-ttu-id="b2c7b-112">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b2c7b-112">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b2c7b-113">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b2c7b-113">Minimum supported server</span></span><br/> | <span data-ttu-id="b2c7b-114">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b2c7b-114">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b2c7b-115">En-tête</span><span class="sxs-lookup"><span data-stu-id="b2c7b-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2c7b-116"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2c7b-116"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2c7b-117">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b2c7b-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2c7b-118">Gestionnaire de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="b2c7b-118">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="b2c7b-119">Messages de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="b2c7b-119">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





