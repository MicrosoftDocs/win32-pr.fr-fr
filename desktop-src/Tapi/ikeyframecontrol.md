---
description: L’interface IKeyFrameControl est implémentée par le MSP H. 323 et n’est disponible que sur les objets de flux H. 323.
ms.assetid: 68cb1df1-f7fa-447a-8ea5-80dc1e802760
title: Interface IKeyFrameControl (H323priv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c326c6a492777d7c41ae450a1c502c343aeb8cb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540328"
---
# <a name="ikeyframecontrol-interface"></a><span data-ttu-id="ae679-103">Interface IKeyFrameControl</span><span class="sxs-lookup"><span data-stu-id="ae679-103">IKeyFrameControl interface</span></span>

<span data-ttu-id="ae679-104">\[**IKeyFrameControl** n’est pas disponible pour une utilisation dans Windows Vista, windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="ae679-104">\[**IKeyFrameControl** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="ae679-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="ae679-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="ae679-106">L’interface **IKeyFrameControl** est implémentée par le [MSP h. 323](h323-msp.md) et n’est disponible que sur les objets de flux h. 323.</span><span class="sxs-lookup"><span data-stu-id="ae679-106">The **IKeyFrameControl** interface is implemented by the [H.323 MSP](h323-msp.md) and is available only on H.323 stream objects.</span></span> <span data-ttu-id="ae679-107">Cette interface expose des méthodes qui permettent la création et la manipulation de terminaux qui peuvent communiquer entre des clients H323 et SDP.</span><span class="sxs-lookup"><span data-stu-id="ae679-107">This interface exposes methods that enable creation and manipulation of terminals that can communicate between H323 and SDP clients.</span></span> <span data-ttu-id="ae679-108">Il a deux méthodes qui permettent à l’application de demander au point de terminaison distant de mettre à jour l’image vidéo avec une image clé.</span><span class="sxs-lookup"><span data-stu-id="ae679-108">It has two methods that allow the application to ask the remote endpoint to update the video image with a keyframe.</span></span>

## <a name="members"></a><span data-ttu-id="ae679-109">Membres</span><span class="sxs-lookup"><span data-stu-id="ae679-109">Members</span></span>

<span data-ttu-id="ae679-110">L’interface **IKeyFrameControl** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="ae679-110">The **IKeyFrameControl** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ae679-111">**IKeyFrameControl** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="ae679-111">**IKeyFrameControl** also has these types of members:</span></span>

-   [<span data-ttu-id="ae679-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ae679-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ae679-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="ae679-113">Methods</span></span>

<span data-ttu-id="ae679-114">L’interface **IKeyFrameControl** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="ae679-114">The **IKeyFrameControl** interface has these methods.</span></span>



| <span data-ttu-id="ae679-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="ae679-115">Method</span></span>                                                                  | <span data-ttu-id="ae679-116">Description</span><span class="sxs-lookup"><span data-stu-id="ae679-116">Description</span></span>                                                                                 |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ae679-117">**PeriodicUpdatePicture**</span><span class="sxs-lookup"><span data-stu-id="ae679-117">**PeriodicUpdatePicture**</span></span>](ikeyframecontrol-periodicupdatepicture.md) | <span data-ttu-id="ae679-118">Configure un minuteur dans le flux qui demandera régulièrement des mises à jour d’images.</span><span class="sxs-lookup"><span data-stu-id="ae679-118">Configures a timer in the stream that will ask for picture updates periodically.</span></span><br/> |
| [<span data-ttu-id="ae679-119">**UpdatePicture**</span><span class="sxs-lookup"><span data-stu-id="ae679-119">**UpdatePicture**</span></span>](ikeyframecontrol-updatepicture.md)                 | <span data-ttu-id="ae679-120">Demande à l’expéditeur vidéo de mettre à jour l’image.</span><span class="sxs-lookup"><span data-stu-id="ae679-120">Asks the video sender to update the picture.</span></span><br/>                                     |



 

## <a name="requirements"></a><span data-ttu-id="ae679-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ae679-121">Requirements</span></span>



| <span data-ttu-id="ae679-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ae679-122">Requirement</span></span> | <span data-ttu-id="ae679-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="ae679-123">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ae679-124">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="ae679-124">TAPI version</span></span><br/> | <span data-ttu-id="ae679-125">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="ae679-125">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="ae679-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="ae679-126">Header</span></span><br/>       | <dl> <span data-ttu-id="ae679-127"><dt>H323priv. h</dt></span><span class="sxs-lookup"><span data-stu-id="ae679-127"><dt>H323priv.h</dt></span></span> </dl> |
| <span data-ttu-id="ae679-128">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="ae679-128">Library</span></span><br/>      | <dl> <span data-ttu-id="ae679-129"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ae679-129"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="ae679-130">DLL</span><span class="sxs-lookup"><span data-stu-id="ae679-130">DLL</span></span><br/>          | <dl> <span data-ttu-id="ae679-131"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ae679-131"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="ae679-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ae679-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae679-133">MSP H323</span><span class="sxs-lookup"><span data-stu-id="ae679-133">H323 MSP</span></span>](h323-msp.md)
</dt> </dl>

 

