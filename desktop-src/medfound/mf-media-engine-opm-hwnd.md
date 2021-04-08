---
description: Spécifie une fenêtre pour le moteur multimédia qui applique des protections de sortie Protection Manager (OPM).
ms.assetid: E5271D72-FE16-4D28-9BBA-1440C7CE0921
title: Attribut MF_MEDIA_ENGINE_OPM_HWND (Mfmediaengine. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d60dd38f4f9eaca3e4eefbf84142c1509463f9b9
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103953377"
---
# <a name="mf_media_engine_opm_hwnd-attribute"></a><span data-ttu-id="36917-103">Attribut de HWND de l’un des \_ Media \_ Engines \_ OPM \_</span><span class="sxs-lookup"><span data-stu-id="36917-103">MF\_MEDIA\_ENGINE\_OPM\_HWND attribute</span></span>

<span data-ttu-id="36917-104">Spécifie une fenêtre pour le moteur multimédia qui applique des protections de [sortie Protection Manager](output-protection-manager.md) (OPM).</span><span class="sxs-lookup"><span data-stu-id="36917-104">Specifies a window for the Media Engine to apply [Output Protection Manager](output-protection-manager.md) (OPM) protections.</span></span>

## <a name="data-type"></a><span data-ttu-id="36917-105">Type de données</span><span class="sxs-lookup"><span data-stu-id="36917-105">Data type</span></span>

<span data-ttu-id="36917-106">**HWND** stocké comme **UINT64**</span><span class="sxs-lookup"><span data-stu-id="36917-106">**HWND** stored as **UINT64**</span></span>

## <a name="remarks"></a><span data-ttu-id="36917-107">Notes</span><span class="sxs-lookup"><span data-stu-id="36917-107">Remarks</span></span>

<span data-ttu-id="36917-108">Cet attribut est utilisé avec la méthode [**IMFMediaEngineClassFactory :: CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) pour initialiser le moteur multimédia.</span><span class="sxs-lookup"><span data-stu-id="36917-108">This attribute is used with the [**IMFMediaEngineClassFactory::CreateInstance**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance) method to initialize the Media Engine.</span></span>

<span data-ttu-id="36917-109">Pour activer les protections OPM pour la lecture vidéo, l’application doit effectuer l’une des opérations suivantes :</span><span class="sxs-lookup"><span data-stu-id="36917-109">To enable OPM protections for video playback, the application must do one of the following:</span></span>

-   <span data-ttu-id="36917-110">Définissez l' [attribut \_ \_ HWND de \_ lecture \_ du moteur multimédia MF](mf-media-engine-playback-hwnd.md) lors de la création du moteur multimédia.</span><span class="sxs-lookup"><span data-stu-id="36917-110">Set the [MF\_MEDIA\_ENGINE\_PLAYBACK\_HWND](mf-media-engine-playback-hwnd.md) attribute when creating the Media Engine.</span></span>
-   <span data-ttu-id="36917-111">Définissez l' \_ attribut du \_ \_ HWND OPM Media Engine \_ pour la création du moteur multimédia.</span><span class="sxs-lookup"><span data-stu-id="36917-111">Set the MF\_MEDIA\_ENGINE\_OPM\_HWND attribute when creating the Media Engine.</span></span>
-   <span data-ttu-id="36917-112">Appelez [**IMFMediaEngineProtectedContent :: SetOPMWindow**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineprotectedcontent-setopmwindow) à tout moment après avoir créé le moteur multimédia, mais avant d’afficher le contenu protégé.</span><span class="sxs-lookup"><span data-stu-id="36917-112">Call [**IMFMediaEngineProtectedContent::SetOPMWindow**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineprotectedcontent-setopmwindow) at any point after creating the Media Engine, but before protected content is displayed.</span></span>

## <a name="requirements"></a><span data-ttu-id="36917-113">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="36917-113">Requirements</span></span>



| <span data-ttu-id="36917-114">Condition requise</span><span class="sxs-lookup"><span data-stu-id="36917-114">Requirement</span></span> | <span data-ttu-id="36917-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="36917-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="36917-116">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36917-116">Minimum supported client</span></span><br/> | <span data-ttu-id="36917-117">Applications Windows 8 \[ Desktop Apps \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="36917-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="36917-118">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="36917-118">Minimum supported server</span></span><br/> | <span data-ttu-id="36917-119">Applications de bureau Windows Server 2012 \[ \| apps UWP\]</span><span class="sxs-lookup"><span data-stu-id="36917-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                                |
| <span data-ttu-id="36917-120">En-tête</span><span class="sxs-lookup"><span data-stu-id="36917-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="36917-121"><dt>Mfmediaengine. h</dt></span><span class="sxs-lookup"><span data-stu-id="36917-121"><dt>Mfmediaengine.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36917-122">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="36917-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36917-123">Liste alphabétique des attributs Media Foundation</span><span class="sxs-lookup"><span data-stu-id="36917-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="36917-124">Attributs du moteur multimédia</span><span class="sxs-lookup"><span data-stu-id="36917-124">Media Engine Attributes</span></span>](media-engine-attributes.md)
</dt> </dl>

 

 




