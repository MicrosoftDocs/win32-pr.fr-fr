---
description: Valeur indiquant si une image a été capturée à l’aide de l’éclairage infrarouge (active Infrared).
ms.assetid: D84772C8-902F-4302-8288-0430892A1896
title: Attribut MF_CAPTURE_METADATA_FRAME_ILLUMINATION (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb9aa60b5e921e99ac4f4c56cb4643af8389aa91
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514212"
---
# <a name="mf_capture_metadata_frame_illumination-attribute"></a><span data-ttu-id="a4b02-103">\_Attribut d' \_ \_ éclairage de trame de métadonnées de capture MF \_</span><span class="sxs-lookup"><span data-stu-id="a4b02-103">MF\_CAPTURE\_METADATA\_FRAME\_ILLUMINATION attribute</span></span>

<span data-ttu-id="a4b02-104">\[Certaines informations relatives aux produits précommercialisés peuvent être substantiellement modifiées avant leur commercialisation.</span><span class="sxs-lookup"><span data-stu-id="a4b02-104">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a4b02-105">Microsoft ne donne aucune garantie, expresse ou implicite, concernant les informations fournies ici.\]</span><span class="sxs-lookup"><span data-stu-id="a4b02-105">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a4b02-106">Valeur indiquant si une image a été capturée à l’aide de l’éclairage infrarouge (active Infrared).</span><span class="sxs-lookup"><span data-stu-id="a4b02-106">A value indicating whether a frame was captured using active infrared (IR) illumination.</span></span>

## <a name="data-type"></a><span data-ttu-id="a4b02-107">Type de données</span><span class="sxs-lookup"><span data-stu-id="a4b02-107">Data type</span></span>

<span data-ttu-id="a4b02-108">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="a4b02-108">**UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="a4b02-109">Notes</span><span class="sxs-lookup"><span data-stu-id="a4b02-109">Remarks</span></span>

<span data-ttu-id="a4b02-110">Cet attribut est un masque de masque.</span><span class="sxs-lookup"><span data-stu-id="a4b02-110">This attribute is a bitmask.</span></span> <span data-ttu-id="a4b02-111">Il s’agit d’une valeur de bit de 64 pour la compatibilité descendante.</span><span class="sxs-lookup"><span data-stu-id="a4b02-111">It is a 64 bit value for backward compatibility.</span></span>

<span data-ttu-id="a4b02-112">L’éclairage actif est lorsqu’un appareil a un émetteur de lumière proche de la caméra IR émettant un faisceau de lumière pour éclairer la scène, émettant généralement une lumière IR pour ne pas perturber les yeux humains.</span><span class="sxs-lookup"><span data-stu-id="a4b02-112">Active illumination is when a device has a light emitter close to the IR camera emitting a beam of light to illuminate the scene, typically emitting IR light so it won’t disturb human eyes.</span></span> <span data-ttu-id="a4b02-113">Affectez la valeur (valeur & 0x1) ! = 0 si le frame a été capturé quand l’éclairage actif était activé et défini (valeur & 0x1) = = 0 si l’éclairage actif était désactivé.</span><span class="sxs-lookup"><span data-stu-id="a4b02-113">Set value to (value & 0x1) != 0 if frame was captured when active illumination was on and set (value & 0x1) == 0 if active illumination was off.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4b02-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a4b02-114">Requirements</span></span>



| <span data-ttu-id="a4b02-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a4b02-115">Requirement</span></span> | <span data-ttu-id="a4b02-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="a4b02-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a4b02-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a4b02-117">Minimum supported client</span></span><br/> | <span data-ttu-id="a4b02-118">Applications de bureau Windows 10, version 1709 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a4b02-118">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a4b02-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a4b02-119">Minimum supported server</span></span><br/> | <span data-ttu-id="a4b02-120">Windows Server, version 1709, \[ applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a4b02-120">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                      |
| <span data-ttu-id="a4b02-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="a4b02-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4b02-122"><dt>Mfapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4b02-122"><dt>Mfapi.h</dt></span></span> </dl> |



 

 




