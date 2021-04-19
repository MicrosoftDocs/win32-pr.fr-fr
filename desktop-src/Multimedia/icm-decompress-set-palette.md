---
title: Message ICM_DECOMPRESS_SET_PALETTE (VFW. h)
description: Le \_ message de palette DÉcompresser les DÉcompresses \_ \_ spécifie une palette pour un pilote de décompression vidéo à utiliser s’il est décompressé dans un format qui utilise une palette. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro ICDecompressSetPalette.
ms.assetid: 269d01f9-b7c8-40e4-abdb-24dd0c9cc18d
keywords:
- Message ICM_DECOMPRESS_SET_PALETTE Windows Multimedia
topic_type:
- apiref
api_name:
- ICM_DECOMPRESS_SET_PALETTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f2bbbf1b09b8c5954a2149edd16cb213a08fb3a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511584"
---
# <a name="icm_decompress_set_palette-message"></a><span data-ttu-id="090a5-105">\_ \_ Message de palette de DÉcompression ICM \_</span><span class="sxs-lookup"><span data-stu-id="090a5-105">ICM\_DECOMPRESS\_SET\_PALETTE message</span></span>

<span data-ttu-id="090a5-106">Le message de **\_ \_ \_ palette décompresser les décompresses** spécifie une palette pour un pilote de décompression vidéo à utiliser s’il est décompressé dans un format qui utilise une palette.</span><span class="sxs-lookup"><span data-stu-id="090a5-106">The **ICM\_DECOMPRESS\_SET\_PALETTE** message specifies a palette for a video decompression driver to use if it is decompressing to a format that uses a palette.</span></span> <span data-ttu-id="090a5-107">Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ICDecompressSetPalette**](/windows/desktop/api/Vfw/nf-vfw-icdecompresssetpalette) .</span><span class="sxs-lookup"><span data-stu-id="090a5-107">You can send this message explicitly or by using the [**ICDecompressSetPalette**](/windows/desktop/api/Vfw/nf-vfw-icdecompresssetpalette) macro.</span></span>


```C++
ICM_DECOMPRESS_SET_PALETTE 
wParam = (DWORD_PTR) (LPVOID) lpbiPalette; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="090a5-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="090a5-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="090a5-109"><span id="lpbiPalette"></span><span id="lpbipalette"></span><span id="LPBIPALETTE"></span>*lpbiPalette*</span><span class="sxs-lookup"><span data-stu-id="090a5-109"><span id="lpbiPalette"></span><span id="lpbipalette"></span><span id="LPBIPALETTE"></span>*lpbiPalette*</span></span>
</dt> <dd>

<span data-ttu-id="090a5-110">Pointeur vers une structure [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) dont la table des couleurs contient les couleurs à utiliser si possible.</span><span class="sxs-lookup"><span data-stu-id="090a5-110">Pointer to a [**BITMAPINFOHEADER**](/previous-versions//dd183376(v=vs.85)) structure whose color table contains the colors that should be used if possible.</span></span> <span data-ttu-id="090a5-111">Vous pouvez spécifier zéro pour utiliser l’ensemble de couleurs de sortie par défaut.</span><span class="sxs-lookup"><span data-stu-id="090a5-111">You can specify zero to use the default set of output colors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="090a5-112">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="090a5-112">Return Value</span></span>

<span data-ttu-id="090a5-113">Retourne ICERR \_ OK si le pilote de décompression peut décompresser des images de manière précise dans la palette suggérée à l’aide de l’ensemble de couleurs à mesure qu’elles sont organisées dans la palette.</span><span class="sxs-lookup"><span data-stu-id="090a5-113">Returns ICERR\_OK if the decompression driver can precisely decompress images to the suggested palette using the set of colors as they are arranged in the palette.</span></span> <span data-ttu-id="090a5-114">Retourne ICERR \_ non pris en charge dans le cas contraire.</span><span class="sxs-lookup"><span data-stu-id="090a5-114">Returns ICERR\_UNSUPPORTED otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="090a5-115">Notes</span><span class="sxs-lookup"><span data-stu-id="090a5-115">Remarks</span></span>

<span data-ttu-id="090a5-116">Ce message ne doit pas affecter la décompression déjà en cours ; au lieu de cela, les couleurs transmises à l’aide de ce message doivent être retournées en réponse à l’avenir de la [**\_ décompression \_ \_ ICM**](icm-decompress-get-format.md) , de l’extraction des messages de la [**\_ \_ \_ palette**](icm-decompress-get-palette.md) .</span><span class="sxs-lookup"><span data-stu-id="090a5-116">This message should not affect decompression already in progress; rather, colors passed using this message should be returned in response to future [**ICM\_DECOMPRESS\_GET\_FORMAT**](icm-decompress-get-format.md) and [**ICM\_DECOMPRESS\_GET\_PALETTE**](icm-decompress-get-palette.md) messages.</span></span> <span data-ttu-id="090a5-117">Les couleurs sont renvoyées au pilote de décompression dans un prochain message de [**\_ \_ début**](icm-decompress-begin.md) de décompression ICM.</span><span class="sxs-lookup"><span data-stu-id="090a5-117">Colors are sent back to the decompression driver in a future [**ICM\_DECOMPRESS\_BEGIN**](icm-decompress-begin.md) message.</span></span>

<span data-ttu-id="090a5-118">Ce message est principalement utilisé lorsqu’un pilote décompresse des images à l’écran et qu’une autre application qui utilise une palette est au premier plan, forçant le pilote de décompression à s’adapter à un ensemble de couleurs étranger.</span><span class="sxs-lookup"><span data-stu-id="090a5-118">This message is used primarily when a driver decompresses images to the screen and another application that uses a palette is in the foreground, forcing the decompression driver to adapt to a foreign set of colors.</span></span>

## <a name="requirements"></a><span data-ttu-id="090a5-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="090a5-119">Requirements</span></span>



| <span data-ttu-id="090a5-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="090a5-120">Requirement</span></span> | <span data-ttu-id="090a5-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="090a5-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="090a5-122">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="090a5-122">Minimum supported client</span></span><br/> | <span data-ttu-id="090a5-123">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="090a5-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="090a5-124">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="090a5-124">Minimum supported server</span></span><br/> | <span data-ttu-id="090a5-125">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="090a5-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="090a5-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="090a5-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="090a5-127"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="090a5-127"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="090a5-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="090a5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="090a5-129">Gestionnaire de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="090a5-129">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="090a5-130">Messages de compression vidéo</span><span class="sxs-lookup"><span data-stu-id="090a5-130">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

