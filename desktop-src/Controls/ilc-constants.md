---
title: Indicateurs de création de la liste d’images (shlobj. h)
description: Jeu d’indicateurs de bits qui spécifie le type de liste d’images à créer. Ce paramètre peut être une combinaison des valeurs suivantes, mais il ne peut inclure qu’une seule des \_ valeurs de couleur ILC. Utilisé par ImageList \_ Create et IImageList2 Initialize.
ms.assetid: DFEB1934-DB7F-4151-97F9-DDB2BCCC782A
topic_type:
- apiref
api_name:
- ILC_MASK
- ILC_COLOR
- ILC_COLORDDB
- ILC_COLOR4
- ILC_COLOR8
- ILC_COLOR16
- ILC_COLOR24
- ILC_COLOR32
- ILC_PALETTE
- ILC_MIRROR
- ILC_PERITEMMIRROR
- ILC_ORIGINALSIZE
- ILC_HIGHQUALITYSCALE
api_location:
- Shlobj.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f27f9a83c119b8e201ba41c002bf7c166ba3e4dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465042"
---
# <a name="image-list-creation-flags"></a><span data-ttu-id="3e36a-105">Indicateurs de création de la liste d’images</span><span class="sxs-lookup"><span data-stu-id="3e36a-105">Image List Creation Flags</span></span>

<span data-ttu-id="3e36a-106">Jeu d’indicateurs de bits qui spécifie le type de liste d’images à créer.</span><span class="sxs-lookup"><span data-stu-id="3e36a-106">The set of bit flags that specifies the type of image list to create.</span></span> <span data-ttu-id="3e36a-107">Ce paramètre peut être une combinaison des valeurs suivantes, mais il ne peut inclure qu’une seule des \_ valeurs de couleur ILC.</span><span class="sxs-lookup"><span data-stu-id="3e36a-107">This parameter can be a combination of the following values, but it can include only one of the ILC\_COLOR values.</span></span> <span data-ttu-id="3e36a-108">Utilisé par [**ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) et [**IImageList2 :: Initialize**](/windows/desktop/api/Commoncontrols/nf-commoncontrols-iimagelist2-initialize).</span><span class="sxs-lookup"><span data-stu-id="3e36a-108">Used by [**ImageList\_Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) and [**IImageList2::Initialize**](/windows/desktop/api/Commoncontrols/nf-commoncontrols-iimagelist2-initialize).</span></span>



| <span data-ttu-id="3e36a-109">Constante/valeur</span><span class="sxs-lookup"><span data-stu-id="3e36a-109">Constant/value</span></span>                                                                                                                                                                                                                                     | <span data-ttu-id="3e36a-110">Description</span><span class="sxs-lookup"><span data-stu-id="3e36a-110">Description</span></span>                                                                                                                                                                                  |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ILC_MASK"></span><span id="ilc_mask"></span><dl> <span data-ttu-id="3e36a-111"><dt>**ILC \_ Masquer**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="3e36a-111"><dt>**ILC\_MASK**</dt> <dt>0x00000001</dt></span></span> </dl>                                     | <span data-ttu-id="3e36a-112">Utilisez un masque.</span><span class="sxs-lookup"><span data-stu-id="3e36a-112">Use a mask.</span></span> <span data-ttu-id="3e36a-113">La liste d’images contient deux bitmaps, dont l’un est une bitmap monochrome utilisée comme masque.</span><span class="sxs-lookup"><span data-stu-id="3e36a-113">The image list contains two bitmaps, one of which is a monochrome bitmap used as a mask.</span></span> <span data-ttu-id="3e36a-114">Si cette valeur n’est pas incluse, la liste d’images contient une seule bitmap.</span><span class="sxs-lookup"><span data-stu-id="3e36a-114">If this value is not included, the image list contains only one bitmap.</span></span><br/>      |
| <span id="ILC_COLOR"></span><span id="ilc_color"></span><dl> <span data-ttu-id="3e36a-115"><dt>**ILC \_ COULEUR**</dt> <dt>0x00000000</dt></span><span class="sxs-lookup"><span data-stu-id="3e36a-115"><dt>**ILC\_COLOR**</dt> <dt>0x00000000</dt></span></span> </dl>                                  | <span data-ttu-id="3e36a-116">Utilisez le comportement par défaut si aucun des autres \_ indicateurs ILC COLORx n’est spécifié.</span><span class="sxs-lookup"><span data-stu-id="3e36a-116">Use the default behavior if none of the other ILC\_COLORx flags is specified.</span></span> <span data-ttu-id="3e36a-117">En règle générale, la valeur par défaut est ILC \_ color4, mais pour les anciens pilotes d’affichage, la valeur par défaut est ILC \_ COLORDDB.</span><span class="sxs-lookup"><span data-stu-id="3e36a-117">Typically, the default is ILC\_COLOR4, but for older display drivers, the default is ILC\_COLORDDB.</span></span><br/> |
| <span id="ILC_COLORDDB"></span><span id="ilc_colorddb"></span><dl> <span data-ttu-id="3e36a-118"><dt>**ILC \_ COLORDDB**</dt> <dt>0x000000FE</dt></span><span class="sxs-lookup"><span data-stu-id="3e36a-118"><dt>**ILC\_COLORDDB**</dt> <dt>0x000000FE</dt></span></span> </dl>                         | <span data-ttu-id="3e36a-119">Utilisez une image bitmap dépendante de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="3e36a-119">Use a device-dependent bitmap.</span></span><br/>                                                                                                                                                    |
| <span id="ILC_COLOR4"></span><span id="ilc_color4"></span><dl> <span data-ttu-id="3e36a-120"><dt>**ILC \_ COLOR4**</dt> <dt>0x00000004</dt></span><span class="sxs-lookup"><span data-stu-id="3e36a-120"><dt>**ILC\_COLOR4**</dt> <dt>0x00000004</dt></span></span> </dl>                               | <span data-ttu-id="3e36a-121">Utilisez une section DIB (Device-Independent Bitmap) 4 bits (16 couleurs) comme bitmap de la liste d’images.</span><span class="sxs-lookup"><span data-stu-id="3e36a-121">Use a 4-bit (16-color) device-independent bitmap (DIB) section as the bitmap for the image list.</span></span><br/>                                                                                  |
| <span id="ILC_COLOR8"></span><span id="ilc_color8"></span><dl> <span data-ttu-id="3e36a-122"><dt>**ILC \_ COLOR8**</dt> <dt>0x00000008</dt></span><span class="sxs-lookup"><span data-stu-id="3e36a-122"><dt>**ILC\_COLOR8**</dt> <dt>0x00000008</dt></span></span> </dl>                               | <span data-ttu-id="3e36a-123">Utilisez une section DIB 8 bits.</span><span class="sxs-lookup"><span data-stu-id="3e36a-123">Use an 8-bit DIB section.</span></span> <span data-ttu-id="3e36a-124">Les couleurs utilisées pour la table de couleurs sont les mêmes que celles de la palette de demi-teintes.</span><span class="sxs-lookup"><span data-stu-id="3e36a-124">The colors used for the color table are the same colors as the halftone palette.</span></span><br/>                                                                        |
| <span id="ILC_COLOR16"></span><span id="ilc_color16"></span><dl> <span data-ttu-id="3e36a-125"><dt>**ILC \_ COLOR16**</dt> <dt>0x00000010</dt></span><span class="sxs-lookup"><span data-stu-id="3e36a-125"><dt>**ILC\_COLOR16**</dt> <dt>0x00000010</dt></span></span> </dl>                            | <span data-ttu-id="3e36a-126">Utilisez une section DIB 16 bits (32/64 bits).</span><span class="sxs-lookup"><span data-stu-id="3e36a-126">Use a 16-bit (32/64k-color) DIB section.</span></span><br/>                                                                                                                                          |
| <span id="ILC_COLOR24"></span><span id="ilc_color24"></span><dl> <span data-ttu-id="3e36a-127"><dt>**ILC \_ COLOR24**</dt> <dt>0x00000018</dt></span><span class="sxs-lookup"><span data-stu-id="3e36a-127"><dt>**ILC\_COLOR24**</dt> <dt>0x00000018</dt></span></span> </dl>                            | <span data-ttu-id="3e36a-128">Utilisez une section DIB de 24 bits.</span><span class="sxs-lookup"><span data-stu-id="3e36a-128">Use a 24-bit DIB section.</span></span><br/>                                                                                                                                                         |
| <span id="ILC_COLOR32"></span><span id="ilc_color32"></span><dl> <span data-ttu-id="3e36a-129"><dt>**ILC \_ COLOR32**</dt> <dt>0x00000020</dt></span><span class="sxs-lookup"><span data-stu-id="3e36a-129"><dt>**ILC\_COLOR32**</dt> <dt>0x00000020</dt></span></span> </dl>                            | <span data-ttu-id="3e36a-130">Utilisez une section DIB 32 bits.</span><span class="sxs-lookup"><span data-stu-id="3e36a-130">Use a 32-bit DIB section.</span></span><br/>                                                                                                                                                         |
| <span id="ILC_PALETTE"></span><span id="ilc_palette"></span><dl> <span data-ttu-id="3e36a-131"><dt>**ILC \_ PALETTE**</dt> <dt>0x00000800</dt></span><span class="sxs-lookup"><span data-stu-id="3e36a-131"><dt>**ILC\_PALETTE**</dt> <dt>0x00000800</dt></span></span> </dl>                            | <span data-ttu-id="3e36a-132">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="3e36a-132">Not implemented.</span></span><br/>                                                                                                                                                                  |
| <span id="ILC_MIRROR"></span><span id="ilc_mirror"></span><dl> <span data-ttu-id="3e36a-133"><dt>**ILC \_ MIROIR**</dt> <dt>0x00002000</dt></span><span class="sxs-lookup"><span data-stu-id="3e36a-133"><dt>**ILC\_MIRROR**</dt> <dt>0x00002000</dt></span></span> </dl>                               | <span data-ttu-id="3e36a-134">Mettre en miroir les icônes contenues si le processus est mis en miroir</span><span class="sxs-lookup"><span data-stu-id="3e36a-134">Mirror the icons contained, if the process is mirrored</span></span><br/>                                                                                                                            |
| <span id="ILC_PERITEMMIRROR"></span><span id="ilc_peritemmirror"></span><dl> <span data-ttu-id="3e36a-135"><dt>**ILC \_ PERITEMMIRROR**</dt> <dt>0x00008000</dt></span><span class="sxs-lookup"><span data-stu-id="3e36a-135"><dt>**ILC\_PERITEMMIRROR**</dt> <dt>0x00008000</dt></span></span> </dl>          | <span data-ttu-id="3e36a-136">Fait en sorte que le code de mise en miroir reflète chaque élément lors de l’insertion d’un ensemble d’images, par opposition à la bande entière.</span><span class="sxs-lookup"><span data-stu-id="3e36a-136">Causes the mirroring code to mirror each item when inserting a set of images, versus the whole strip.</span></span><br/>                                                                             |
| <span id="ILC_ORIGINALSIZE"></span><span id="ilc_originalsize"></span><dl> <span data-ttu-id="3e36a-137"><dt>**ILC \_ ORIGINALSIZE**</dt> <dt>0x00010000</dt></span><span class="sxs-lookup"><span data-stu-id="3e36a-137"><dt>**ILC\_ORIGINALSIZE**</dt> <dt>0x00010000</dt></span></span> </dl>             | <span data-ttu-id="3e36a-138">**Windows Vista et versions ultérieures.**</span><span class="sxs-lookup"><span data-stu-id="3e36a-138">**Windows Vista and later.**</span></span> <span data-ttu-id="3e36a-139">ImageList doit accepter des images Set plus petites et appliquer la taille d’origine en fonction de l’image ajoutée.</span><span class="sxs-lookup"><span data-stu-id="3e36a-139">Imagelist should accept smaller than set images and apply original size based on image added.</span></span><br/>                                                        |
| <span id="ILC_HIGHQUALITYSCALE"></span><span id="ilc_highqualityscale"></span><dl> <span data-ttu-id="3e36a-140"><dt>**ILC \_ HIGHQUALITYSCALE**</dt> <dt>0x00020000</dt></span><span class="sxs-lookup"><span data-stu-id="3e36a-140"><dt>**ILC\_HIGHQUALITYSCALE**</dt> <dt>0x00020000</dt></span></span> </dl> | <span data-ttu-id="3e36a-141">**Windows Vista et versions ultérieures.**</span><span class="sxs-lookup"><span data-stu-id="3e36a-141">**Windows Vista and later.**</span></span> <span data-ttu-id="3e36a-142">Réservé.</span><span class="sxs-lookup"><span data-stu-id="3e36a-142">Reserved.</span></span><br/>                                                                                                                                            |



## <a name="requirements"></a><span data-ttu-id="3e36a-143">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3e36a-143">Requirements</span></span>



| <span data-ttu-id="3e36a-144">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3e36a-144">Requirement</span></span> | <span data-ttu-id="3e36a-145">Valeur</span><span class="sxs-lookup"><span data-stu-id="3e36a-145">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3e36a-146">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e36a-146">Minimum supported client</span></span><br/> | <span data-ttu-id="3e36a-147">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3e36a-147">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="3e36a-148">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3e36a-148">Minimum supported server</span></span><br/> | <span data-ttu-id="3e36a-149">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3e36a-149">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3e36a-150">En-tête</span><span class="sxs-lookup"><span data-stu-id="3e36a-150">Header</span></span><br/>                   | <dl> <span data-ttu-id="3e36a-151"><dt>Shlobj. h</dt></span><span class="sxs-lookup"><span data-stu-id="3e36a-151"><dt>Shlobj.h</dt></span></span> </dl> |



 

 





