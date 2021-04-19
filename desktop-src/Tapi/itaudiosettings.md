---
description: L’interface ITAudioSettings expose des méthodes qui permettent à une application d’obtenir et de définir des paramètres pour le contrôle d’un périphérique audio.
ms.assetid: 56607024-255d-4d1b-9ca0-6086eff7b7b2
title: Interface ITAudioSettings (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eaf2566c7438dbcd14cdacee46cc4d5ec4166731
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525602"
---
# <a name="itaudiosettings-interface"></a><span data-ttu-id="9aac8-103">Interface ITAudioSettings</span><span class="sxs-lookup"><span data-stu-id="9aac8-103">ITAudioSettings interface</span></span>

<span data-ttu-id="9aac8-104">\[ Cette interface n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="9aac8-104">\[ This interface is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="9aac8-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="9aac8-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="9aac8-106">L’interface **ITAudioSettings** expose des méthodes qui permettent à une application d’obtenir et de définir des paramètres pour le contrôle d’un périphérique audio.</span><span class="sxs-lookup"><span data-stu-id="9aac8-106">The **ITAudioSettings** interface exposes methods that allow an application to get and set parameters for control of an audio device.</span></span>

<span data-ttu-id="9aac8-107">Cette interface est implémentée par le [MSP ipconf](ipconf-msp.md) et le [MSP H323](h323-msp.md).</span><span class="sxs-lookup"><span data-stu-id="9aac8-107">This interface is implemented by the [IPConf MSP](ipconf-msp.md) and the [H323 MSP](h323-msp.md).</span></span> <span data-ttu-id="9aac8-108">Elle est exposée uniquement lorsqu’un appel utilise ces fournisseurs de services.</span><span class="sxs-lookup"><span data-stu-id="9aac8-108">It is exposed only when a call uses these service providers.</span></span>

## <a name="members"></a><span data-ttu-id="9aac8-109">Membres</span><span class="sxs-lookup"><span data-stu-id="9aac8-109">Members</span></span>

<span data-ttu-id="9aac8-110">L’interface **ITAudioSettings** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="9aac8-110">The **ITAudioSettings** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="9aac8-111">**ITAudioSettings** a également les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="9aac8-111">**ITAudioSettings** also has these types of members:</span></span>

-   [<span data-ttu-id="9aac8-112">Méthodes</span><span class="sxs-lookup"><span data-stu-id="9aac8-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9aac8-113">Méthodes</span><span class="sxs-lookup"><span data-stu-id="9aac8-113">Methods</span></span>

<span data-ttu-id="9aac8-114">L’interface **ITAudioSettings** possède ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="9aac8-114">The **ITAudioSettings** interface has these methods.</span></span>



| <span data-ttu-id="9aac8-115">Méthode</span><span class="sxs-lookup"><span data-stu-id="9aac8-115">Method</span></span>                                              | <span data-ttu-id="9aac8-116">Description</span><span class="sxs-lookup"><span data-stu-id="9aac8-116">Description</span></span>                                                                                                |
|:----------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9aac8-117">**Télécharger**</span><span class="sxs-lookup"><span data-stu-id="9aac8-117">**Get**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_call)          | <span data-ttu-id="9aac8-118">Obtient la valeur d’une [propriété de paramètre audio](audiosettingsproperty.md)donnée.</span><span class="sxs-lookup"><span data-stu-id="9aac8-118">Gets the value of a given [audio setting property](audiosettingsproperty.md).</span></span><br/>                  |
| [<span data-ttu-id="9aac8-119">**GetRange**</span><span class="sxs-lookup"><span data-stu-id="9aac8-119">**GetRange**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_terminal) | <span data-ttu-id="9aac8-120">Obtient la plage de valeurs valides pour une [propriété de paramètre audio](audiosettingsproperty.md)donnée.</span><span class="sxs-lookup"><span data-stu-id="9aac8-120">Gets the range of valid values for a given [audio setting property](audiosettingsproperty.md).</span></span><br/> |
| [<span data-ttu-id="9aac8-121">**Définissez**</span><span class="sxs-lookup"><span data-stu-id="9aac8-121">**Set**</span></span>](/windows/desktop/api/tapi3if/nf-tapi3if-itasrterminalevent-get_error)         | <span data-ttu-id="9aac8-122">Définit la valeur d’une [propriété de paramètre audio](audiosettingsproperty.md)donnée.</span><span class="sxs-lookup"><span data-stu-id="9aac8-122">Sets the value of a given [audio setting property](audiosettingsproperty.md).</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="9aac8-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9aac8-123">Requirements</span></span>



| <span data-ttu-id="9aac8-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9aac8-124">Requirement</span></span> | <span data-ttu-id="9aac8-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="9aac8-125">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9aac8-126">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="9aac8-126">TAPI version</span></span><br/> | <span data-ttu-id="9aac8-127">Nécessite TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="9aac8-127">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="9aac8-128">En-tête</span><span class="sxs-lookup"><span data-stu-id="9aac8-128">Header</span></span><br/>       | <dl> <span data-ttu-id="9aac8-129"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="9aac8-129"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="9aac8-130">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9aac8-130">Library</span></span><br/>      | <dl> <span data-ttu-id="9aac8-131"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9aac8-131"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="9aac8-132">DLL</span><span class="sxs-lookup"><span data-stu-id="9aac8-132">DLL</span></span><br/>          | <dl> <span data-ttu-id="9aac8-133"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9aac8-133"><dt>Tapi3.dll</dt></span></span> </dl> |



 

