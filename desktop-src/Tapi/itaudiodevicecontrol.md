---
description: L’interface ITAudioDeviceControl expose des méthodes qui permettent à une application d’obtenir et de définir des paramètres pour le contrôle d’un périphérique audio.
ms.assetid: 9a557cb2-acad-406c-9a87-18cbe96e8a9f
title: Interface ITAudioDeviceControl (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 589bf50ee219f200a81aed7057b7755f203b2275
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543302"
---
# <a name="itaudiodevicecontrol-interface"></a><span data-ttu-id="bb310-103">Interface ITAudioDeviceControl</span><span class="sxs-lookup"><span data-stu-id="bb310-103">ITAudioDeviceControl interface</span></span>

<span data-ttu-id="bb310-104">\[ Cette interface n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="bb310-104">\[ This interface is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="bb310-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="bb310-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="bb310-106">L’interface **ITAudioDeviceControl** expose des méthodes qui permettent à une application d’obtenir et de définir des paramètres pour le contrôle d’un périphérique audio.</span><span class="sxs-lookup"><span data-stu-id="bb310-106">The **ITAudioDeviceControl** interface exposes methods that enable an application to get and set parameters for control of an audio device.</span></span>

<span data-ttu-id="bb310-107">Cette interface est implémentée par le [MSP ipconf](ipconf-msp.md) et le [MSP H323](h323-msp.md).</span><span class="sxs-lookup"><span data-stu-id="bb310-107">This interface is implemented by the [IPConf MSP](ipconf-msp.md) and the [H323 MSP](h323-msp.md).</span></span> <span data-ttu-id="bb310-108">Il est exposé lorsqu’un appel utilise ces fournisseurs de services ou un fournisseur de services tiers qui implémente cette interface.</span><span class="sxs-lookup"><span data-stu-id="bb310-108">It is exposed when a call uses these service providers or a third party service provider that implements this interface.</span></span> <span data-ttu-id="bb310-109">Pour obtenir un pointeur vers l’interface **ITAudioDeviceControl** , appelez **QueryInterface** sur l’interface [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) qui contrôle le périphérique audio correspondant au flux.</span><span class="sxs-lookup"><span data-stu-id="bb310-109">To obtain a pointer to the **ITAudioDeviceControl** interface, call **QueryInterface** on the [**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream) interface that controls the audio device corresponding to the stream.</span></span> <span data-ttu-id="bb310-110">Le type de média de l’interface **ITStream** doit être audio pour que l’interface **ITAudioDeviceControl** soit exposée.</span><span class="sxs-lookup"><span data-stu-id="bb310-110">The media type of the **ITStream** interface must be audio for the **ITAudioDeviceControl** interface to be exposed.</span></span>

## <a name="members"></a><span data-ttu-id="bb310-111">Membres</span><span class="sxs-lookup"><span data-stu-id="bb310-111">Members</span></span>

<span data-ttu-id="bb310-112">L’interface **ITAudioDeviceControl** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="bb310-112">The **ITAudioDeviceControl** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="bb310-113">**ITAudioDeviceControl** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="bb310-113">**ITAudioDeviceControl** also has these types of members:</span></span>

-   [<span data-ttu-id="bb310-114">Méthodes</span><span class="sxs-lookup"><span data-stu-id="bb310-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="bb310-115">Méthodes</span><span class="sxs-lookup"><span data-stu-id="bb310-115">Methods</span></span>

<span data-ttu-id="bb310-116">L’interface **ITAudioDeviceControl** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="bb310-116">The **ITAudioDeviceControl** interface has these methods.</span></span>



| <span data-ttu-id="bb310-117">Méthode</span><span class="sxs-lookup"><span data-stu-id="bb310-117">Method</span></span>                                              | <span data-ttu-id="bb310-118">Description</span><span class="sxs-lookup"><span data-stu-id="bb310-118">Description</span></span>                                                                                             |
|:----------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bb310-119">**Télécharger**</span><span class="sxs-lookup"><span data-stu-id="bb310-119">**Get**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_call)          | <span data-ttu-id="bb310-120">Obtient la valeur d’une [propriété de périphérique audio](audiodeviceproperty.md)donnée.</span><span class="sxs-lookup"><span data-stu-id="bb310-120">Gets the value of a given [audio device property](audiodeviceproperty.md).</span></span><br/>                  |
| [<span data-ttu-id="bb310-121">**GetRange**</span><span class="sxs-lookup"><span data-stu-id="bb310-121">**GetRange**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_terminal) | <span data-ttu-id="bb310-122">Obtient la plage de valeurs valides pour une [propriété de périphérique audio](audiodeviceproperty.md)donnée.</span><span class="sxs-lookup"><span data-stu-id="bb310-122">Gets the range of valid values for a given [audio device property](audiodeviceproperty.md).</span></span><br/> |
| [<span data-ttu-id="bb310-123">**Définissez**</span><span class="sxs-lookup"><span data-stu-id="bb310-123">**Set**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_error)         | <span data-ttu-id="bb310-124">Définit la valeur d’une [propriété de périphérique audio](audiodeviceproperty.md)donnée.</span><span class="sxs-lookup"><span data-stu-id="bb310-124">Sets the value of a given [audio device property](audiodeviceproperty.md).</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="bb310-125">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bb310-125">Requirements</span></span>



| <span data-ttu-id="bb310-126">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bb310-126">Requirement</span></span> | <span data-ttu-id="bb310-127">Valeur</span><span class="sxs-lookup"><span data-stu-id="bb310-127">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bb310-128">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="bb310-128">TAPI version</span></span><br/> | <span data-ttu-id="bb310-129">Nécessite TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="bb310-129">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="bb310-130">En-tête</span><span class="sxs-lookup"><span data-stu-id="bb310-130">Header</span></span><br/>       | <dl> <span data-ttu-id="bb310-131"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="bb310-131"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="bb310-132">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="bb310-132">Library</span></span><br/>      | <dl> <span data-ttu-id="bb310-133"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bb310-133"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="bb310-134">DLL</span><span class="sxs-lookup"><span data-stu-id="bb310-134">DLL</span></span><br/>          | <dl> <span data-ttu-id="bb310-135"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bb310-135"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb310-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bb310-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb310-137">MSP IPConf</span><span class="sxs-lookup"><span data-stu-id="bb310-137">IPConf MSP</span></span>](ipconf-msp.md)
</dt> </dl>

 

