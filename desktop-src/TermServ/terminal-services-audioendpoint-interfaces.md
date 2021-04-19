---
title: Services Bureau à distance les interfaces AudioEndpoint
description: Les interfaces suivantes sont utilisées avec l’API AudioEndpoint.
ms.assetid: 615c2d03-c2fb-46f8-aa78-064f8e7b6064
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de520571c99bf84472760e8a1ca28a52a1d6c32e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510200"
---
# <a name="remote-desktop-services-audioendpoint-interfaces"></a><span data-ttu-id="99640-103">Services Bureau à distance les interfaces AudioEndpoint</span><span class="sxs-lookup"><span data-stu-id="99640-103">Remote Desktop Services AudioEndpoint Interfaces</span></span>

<span data-ttu-id="99640-104">Les interfaces suivantes sont utilisées avec l’API AudioEndpoint.</span><span class="sxs-lookup"><span data-stu-id="99640-104">The following interfaces are used with the AudioEndpoint API.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="99640-105">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="99640-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="99640-106">**IAudioDeviceEndpoint**</span><span class="sxs-lookup"><span data-stu-id="99640-106">**IAudioDeviceEndpoint**</span></span>](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiodeviceendpoint)
</dt> <dd>

<span data-ttu-id="99640-107">Initialise un objet de point de terminaison d’appareil et obtient les fonctionnalités de l’appareil qu’il représente.</span><span class="sxs-lookup"><span data-stu-id="99640-107">Initializes a device endpoint object and gets the capabilities of the device that it represents.</span></span>

</dd> <dt>

[<span data-ttu-id="99640-108">**IAudioEndpoint**</span><span class="sxs-lookup"><span data-stu-id="99640-108">**IAudioEndpoint**</span></span>](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpoint)
</dt> <dd>

<span data-ttu-id="99640-109">Fournit des informations au moteur audio sur un point de terminaison audio.</span><span class="sxs-lookup"><span data-stu-id="99640-109">Provides information to the audio engine about an audio endpoint.</span></span> <span data-ttu-id="99640-110">Cette interface est implémentée par un point de terminaison audio.</span><span class="sxs-lookup"><span data-stu-id="99640-110">This interface is implemented by an audio endpoint.</span></span>

</dd> <dt>

[<span data-ttu-id="99640-111">**IAudioEndpointControl**</span><span class="sxs-lookup"><span data-stu-id="99640-111">**IAudioEndpointControl**</span></span>](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointcontrol)
</dt> <dd>

<span data-ttu-id="99640-112">Contrôle l’état du flux d’un point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="99640-112">Controls the stream state of an endpoint.</span></span>

</dd> <dt>

[<span data-ttu-id="99640-113">**IAudioEndpointRT**</span><span class="sxs-lookup"><span data-stu-id="99640-113">**IAudioEndpointRT**</span></span>](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointrt)
</dt> <dd>

<span data-ttu-id="99640-114">Obtient la différence entre les positions actuelles de lecture et d’écriture dans la mémoire tampon du point de terminaison.</span><span class="sxs-lookup"><span data-stu-id="99640-114">Gets the difference between the current read and write positions in the endpoint buffer.</span></span>

</dd> <dt>

[<span data-ttu-id="99640-115">**IAudioInputEndpointRT**</span><span class="sxs-lookup"><span data-stu-id="99640-115">**IAudioInputEndpointRT**</span></span>](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt)
</dt> <dd>

<span data-ttu-id="99640-116">Obtient la mémoire tampon d’entrée pour chaque passe de traitement.</span><span class="sxs-lookup"><span data-stu-id="99640-116">Gets the input buffer for each processing pass.</span></span>

</dd> <dt>

[<span data-ttu-id="99640-117">**IAudioOutputEndpointRT**</span><span class="sxs-lookup"><span data-stu-id="99640-117">**IAudioOutputEndpointRT**</span></span>](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt)
</dt> <dd>

<span data-ttu-id="99640-118">Obtient la mémoire tampon de sortie pour chaque passe de traitement.</span><span class="sxs-lookup"><span data-stu-id="99640-118">Gets the output buffer for each processing pass.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="99640-119">Notes</span><span class="sxs-lookup"><span data-stu-id="99640-119">Remarks</span></span>

<span data-ttu-id="99640-120">L’API Services Bureau à distance AudioEndpoint est destinée à être utilisée dans Bureau à distance scénarios ; ce n’est pas le cas pour les applications clientes.</span><span class="sxs-lookup"><span data-stu-id="99640-120">The Remote Desktop Services AudioEndpoint API is for use in Remote Desktop scenarios; it is not for client applications.</span></span>

 

 




