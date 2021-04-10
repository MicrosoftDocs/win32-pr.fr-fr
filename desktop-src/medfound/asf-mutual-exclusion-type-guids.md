---
description: Les GUID suivants définissent les types de l’objet d’exclusion mutuelle pour les flux ASF (Advanced Systems Format).
ms.assetid: 3db8eebd-2e26-4c77-8f66-7d08436c9e42
title: GUID de type d’exclusion mutuelle ASF (Wmcontainer. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a6fedc766e26c35bb967054a704b732ca03e8a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201183"
---
# <a name="asf-mutual-exclusion-type-guids"></a><span data-ttu-id="a7902-103">GUID de type d’exclusion mutuelle ASF</span><span class="sxs-lookup"><span data-stu-id="a7902-103">ASF Mutual Exclusion Type GUIDs</span></span>

<span data-ttu-id="a7902-104">Les GUID suivants définissent les types de l’objet d’exclusion mutuelle pour les flux ASF (Advanced Systems Format).</span><span class="sxs-lookup"><span data-stu-id="a7902-104">The following GUIDs define the types for the mutual exclusion object for Advanced Systems Format (ASF) streams.</span></span>



| <span data-ttu-id="a7902-105">Constante</span><span class="sxs-lookup"><span data-stu-id="a7902-105">Constant</span></span>                                                                                                                                                                                                                                              | <span data-ttu-id="a7902-106">Description</span><span class="sxs-lookup"><span data-stu-id="a7902-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFASFMutexType_Language"></span><span id="mfasfmutextype_language"></span><span id="MFASFMUTEXTYPE_LANGUAGE"></span><dl> <span data-ttu-id="a7902-107"><dt>**\_Langue MFASFMutexType**</dt></span><span class="sxs-lookup"><span data-stu-id="a7902-107"><dt>**MFASFMutexType\_Language**</dt></span></span> </dl>                 | <span data-ttu-id="a7902-108">Les flux sont mutuellement exclusifs par langue.</span><span class="sxs-lookup"><span data-stu-id="a7902-108">The streams are mutually exclusive by language.</span></span> <span data-ttu-id="a7902-109">Ce type d’exclusion mutuelle est similaire à celui des pistes audio sur un DVD.</span><span class="sxs-lookup"><span data-stu-id="a7902-109">This type of mutual exclusion is similar to the audio tracks on a DVD.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="MFASFMutexType_Bitrate"></span><span id="mfasfmutextype_bitrate"></span><span id="MFASFMUTEXTYPE_BITRATE"></span><dl> <span data-ttu-id="a7902-110"><dt>**\_Débit binaire MFASFMutexType**</dt></span><span class="sxs-lookup"><span data-stu-id="a7902-110"><dt>**MFASFMutexType\_Bitrate**</dt></span></span> </dl>                     | <span data-ttu-id="a7902-111">Les flux sont mutuellement exclusifs par vitesse de transmission.</span><span class="sxs-lookup"><span data-stu-id="a7902-111">The streams are mutually exclusive by bit rate.</span></span> <span data-ttu-id="a7902-112">Ce type d’exclusion mutuelle est également appelé exclusion de la vitesse de transmission multiple (MBR).</span><span class="sxs-lookup"><span data-stu-id="a7902-112">This type of mutual exclusion is also called multiple bit rate (MBR) exclusion.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                        |
| <span id="MFASFMutexType_Presentation"></span><span id="mfasfmutextype_presentation"></span><span id="MFASFMUTEXTYPE_PRESENTATION"></span><dl> <span data-ttu-id="a7902-113"><dt>**\_Présentation MFASFMutexType**</dt></span><span class="sxs-lookup"><span data-stu-id="a7902-113"><dt>**MFASFMutexType\_Presentation**</dt></span></span> </dl> | <span data-ttu-id="a7902-114">Les flux sont mutuellement exclusifs par présentation.</span><span class="sxs-lookup"><span data-stu-id="a7902-114">The streams are mutually exclusive by presentation.</span></span> <span data-ttu-id="a7902-115">Ce type peut être utilisé pour de nombreux scénarios, mais il ne doit être utilisé que lorsque le contenu est identique, mais qu’il prend une forme différente.</span><span class="sxs-lookup"><span data-stu-id="a7902-115">This type can be used for many scenarios, but it should only be used when the content is the same but takes a different form.</span></span> <span data-ttu-id="a7902-116">Par exemple, deux flux contenant la même vidéo, l’un mis en forme pour remplir l’écran et l’autre qui conserve les proportions d’un grand écran d’origine, doivent être rendus mutuellement exclusifs à l’aide de ce type.</span><span class="sxs-lookup"><span data-stu-id="a7902-116">For example, two streams containing the same video, one formatted to fill the screen and the other maintaining the original widescreen aspect ratio, should be made mutually exclusive by using this type.</span></span> <span data-ttu-id="a7902-117">Un autre exemple est l’affichage de flux contenant des vidéos de la même scène à partir de différents angles.</span><span class="sxs-lookup"><span data-stu-id="a7902-117">Another example is streams containing video of the same scene shot from different angles.</span></span><br/> |
| <span id="MFASFMutexType_Unknown"></span><span id="mfasfmutextype_unknown"></span><span id="MFASFMUTEXTYPE_UNKNOWN"></span><dl> <span data-ttu-id="a7902-118"><dt>**MFASFMutexType \_ inconnu**</dt></span><span class="sxs-lookup"><span data-stu-id="a7902-118"><dt>**MFASFMutexType\_Unknown**</dt></span></span> </dl>                     | <span data-ttu-id="a7902-119">Les flux s’excluent mutuellement en fonction de critères personnalisés.</span><span class="sxs-lookup"><span data-stu-id="a7902-119">The streams are mutually exclusive based on custom criteria.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                           |



## <a name="requirements"></a><span data-ttu-id="a7902-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a7902-120">Requirements</span></span>



| <span data-ttu-id="a7902-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a7902-121">Requirement</span></span> | <span data-ttu-id="a7902-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="a7902-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7902-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a7902-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a7902-124">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a7902-124">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a7902-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a7902-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a7902-126">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a7902-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a7902-127">En-tête</span><span class="sxs-lookup"><span data-stu-id="a7902-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="a7902-128"><dt>Wmcontainer. h</dt></span><span class="sxs-lookup"><span data-stu-id="a7902-128"><dt>Wmcontainer.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7902-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a7902-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7902-130">**IMFASFMutualExclusion :: GetType**</span><span class="sxs-lookup"><span data-stu-id="a7902-130">**IMFASFMutualExclusion::GetType**</span></span>](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-gettype)
</dt> <dt>

[<span data-ttu-id="a7902-131">**IMFASFMutualExclusion::SetType**</span><span class="sxs-lookup"><span data-stu-id="a7902-131">**IMFASFMutualExclusion::SetType**</span></span>](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-settype)
</dt> <dt>

[<span data-ttu-id="a7902-132">Constantes Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a7902-132">Media Foundation Constants</span></span>](media-foundation-constants.md)
</dt> </dl>

 

 




