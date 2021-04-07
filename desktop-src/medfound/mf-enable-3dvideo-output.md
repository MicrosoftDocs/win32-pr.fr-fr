---
description: Spécifie la manière dont une transformation de Media Foundation (MFT) doit générer un flux vidéo stéréoscopique 3D.
ms.assetid: AA75A2FB-DEAC-44E9-93E9-4AC2D9F03B39
title: Attribut MF_ENABLE_3DVIDEO_OUTPUT (Mftransform. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fd0123a574ec74ed4aa9fa0aea3b2cabecbb29da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863590"
---
# <a name="mf_enable_3dvideo_output-attribute"></a><span data-ttu-id="0db4a-103">\_Activer l' \_ attribut de \_ sortie 3DVIDEO MF</span><span class="sxs-lookup"><span data-stu-id="0db4a-103">MF\_ENABLE\_3DVIDEO\_OUTPUT attribute</span></span>

<span data-ttu-id="0db4a-104">Spécifie la manière dont une transformation de Media Foundation (MFT) doit générer un flux vidéo stéréoscopique 3D.</span><span class="sxs-lookup"><span data-stu-id="0db4a-104">Specifies how a Media Foundation transform (MFT) should output a 3D stereoscopic video stream.</span></span>

## <a name="data-type"></a><span data-ttu-id="0db4a-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="0db4a-105">Data type</span></span>

<span data-ttu-id="0db4a-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="0db4a-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="0db4a-107">Notes</span><span class="sxs-lookup"><span data-stu-id="0db4a-107">Remarks</span></span>

<span data-ttu-id="0db4a-108">La valeur de l’attribut est un membre de l’énumération [**MF3DVideoOutputType**](/windows/desktop/api/mftransform/ne-mftransform-mf3dvideooutputtype) .</span><span class="sxs-lookup"><span data-stu-id="0db4a-108">The value of the attribute is a member of the [**MF3DVideoOutputType**](/windows/desktop/api/mftransform/ne-mftransform-mf3dvideooutputtype) enumeration.</span></span>

<span data-ttu-id="0db4a-109">Cet attribut s’applique uniquement si la table MFT retourne la **valeur true** pour l’attribut [ \_ \_ 3DVIDEO de prise en charge MFT](mft-support-3dvideo.md) .</span><span class="sxs-lookup"><span data-stu-id="0db4a-109">This attribute applies only if the MFT returns **TRUE** for the [MFT\_SUPPORT\_3DVIDEO](mft-support-3dvideo.md) attribute.</span></span>

<span data-ttu-id="0db4a-110">Pour récupérer ou définir cet attribut, appelez [**IMFTransform :: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) pour récupérer le magasin d’attributs global de la table MFT.</span><span class="sxs-lookup"><span data-stu-id="0db4a-110">To get or set this attribute call [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) to get the global attribute store of the MFT.</span></span>

## <a name="requirements"></a><span data-ttu-id="0db4a-111">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0db4a-111">Requirements</span></span>



| <span data-ttu-id="0db4a-112">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0db4a-112">Requirement</span></span> | <span data-ttu-id="0db4a-113">Valeur</span><span class="sxs-lookup"><span data-stu-id="0db4a-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0db4a-114">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0db4a-114">Minimum supported client</span></span><br/> | <span data-ttu-id="0db4a-115">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="0db4a-115">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="0db4a-116">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0db4a-116">Minimum supported server</span></span><br/> | <span data-ttu-id="0db4a-117">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="0db4a-117">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="0db4a-118">En-tête</span><span class="sxs-lookup"><span data-stu-id="0db4a-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="0db4a-119"><dt>Mftransform. h</dt></span><span class="sxs-lookup"><span data-stu-id="0db4a-119"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0db4a-120">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0db4a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0db4a-121">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0db4a-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




