---
description: TAPI 3 implique un certain nombre d’objets qui sont indépendants de ses cinq objets TAPI principaux (TAPI, Address, Call, CallHub et terminal).
ms.assetid: 090fa8e5-58a5-46ee-89a3-bd97fcfbf0f0
title: Objets Stand-Alone
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e71fdea9c7ed4b66f57c3c0fe35625f35656555e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103865002"
---
# <a name="stand-alone-objects"></a><span data-ttu-id="ff5eb-103">Objets Stand-Alone</span><span class="sxs-lookup"><span data-stu-id="ff5eb-103">Stand-Alone Objects</span></span>

<span data-ttu-id="ff5eb-104">TAPI 3 implique un certain nombre d’objets qui sont indépendants de ses cinq objets TAPI principaux (TAPI, Address, Call, CallHub et terminal).</span><span class="sxs-lookup"><span data-stu-id="ff5eb-104">TAPI 3 involves a number of objects that are independent of its five main TAPI objects (TAPI, Address, Call, CallHub, and Terminal).</span></span> <span data-ttu-id="ff5eb-105">Les interfaces d' [événements](./event-interfaces.md) et les [interfaces d’énumérateur](enumerator-interfaces.md) sont des objets autonomes et sont résumées séparément.</span><span class="sxs-lookup"><span data-stu-id="ff5eb-105">[Event Interfaces](./event-interfaces.md) and [Enumerator Interfaces](enumerator-interfaces.md) are stand-alone objects, and are summarized separately.</span></span> <span data-ttu-id="ff5eb-106">Les éléments suivants résument les interfaces autonomes non-événementielles et non-Enumerator.</span><span class="sxs-lookup"><span data-stu-id="ff5eb-106">The following summarizes non-event and non-enumerator stand-alone interfaces.</span></span>



| <span data-ttu-id="ff5eb-107">Interface</span><span class="sxs-lookup"><span data-stu-id="ff5eb-107">Interface</span></span>                                             | <span data-ttu-id="ff5eb-108">Description</span><span class="sxs-lookup"><span data-stu-id="ff5eb-108">Description</span></span>                                                                                                                                                                                                   |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ff5eb-109">**ITCollection**</span><span class="sxs-lookup"><span data-stu-id="ff5eb-109">**ITCollection**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection)                  | <span data-ttu-id="ff5eb-110">Fournit des méthodes pour permettre aux applications clientes Automation telles que Visual Basic de récupérer des informations de collecte.</span><span class="sxs-lookup"><span data-stu-id="ff5eb-110">Provides methods to allow Automation client applications such as Visual Basic to retrieve collection information.</span></span>                                                                                             |
| [<span data-ttu-id="ff5eb-111">**ITCollection2**</span><span class="sxs-lookup"><span data-stu-id="ff5eb-111">**ITCollection2**</span></span>](/windows/desktop/api/Tapi3if/nn-tapi3if-itcollection2)                | <span data-ttu-id="ff5eb-112">Étend [**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) en fournissant des méthodes supplémentaires pour la modification des collections.</span><span class="sxs-lookup"><span data-stu-id="ff5eb-112">Extends [**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) by providing additional methods for modifying collections.</span></span>                                                                                                       |
| [<span data-ttu-id="ff5eb-113">**IDispatch**</span><span class="sxs-lookup"><span data-stu-id="ff5eb-113">**IDispatch**</span></span>](/previous-versions/windows/desktop/automat/implementing-the-idispatch-interface) | <span data-ttu-id="ff5eb-114">Interface COM standard pour l’implémentation de l’automatisation.</span><span class="sxs-lookup"><span data-stu-id="ff5eb-114">Standard COM interface for implementing Automation.</span></span>                                                                                                                                                           |
| [<span data-ttu-id="ff5eb-115">**IUnknown**</span><span class="sxs-lookup"><span data-stu-id="ff5eb-115">**IUnknown**</span></span>](/windows/win32/api/unknwn/nn-unknwn-iunknown)                         | <span data-ttu-id="ff5eb-116">Interface COM standard pour l’obtention de pointeurs vers des interfaces d’objet.</span><span class="sxs-lookup"><span data-stu-id="ff5eb-116">Standard COM interface for getting pointers to object interfaces.</span></span>                                                                                                                                             |
| [<span data-ttu-id="ff5eb-117">**ITDispatchMapper**</span><span class="sxs-lookup"><span data-stu-id="ff5eb-117">**ITDispatchMapper**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itdispatchmapper)          | <span data-ttu-id="ff5eb-118">Permet à une application de récupérer le pointeur de dispatch d’une autre interface sur un objet, en fonction d’un pointeur [**IDispatch**](/previous-versions/windows/desktop/automat/implementing-the-idispatch-interface) en cours.</span><span class="sxs-lookup"><span data-stu-id="ff5eb-118">Allows an application to retrieve the dispatch pointer of another interface on an object, given a current [**IDispatch**](/previous-versions/windows/desktop/automat/implementing-the-idispatch-interface) pointer.</span></span> <span data-ttu-id="ff5eb-119">Utile pour certains langages de script.</span><span class="sxs-lookup"><span data-stu-id="ff5eb-119">Useful for some scripting languages.</span></span> |
| [<span data-ttu-id="ff5eb-120">**ITRequest**</span><span class="sxs-lookup"><span data-stu-id="ff5eb-120">**ITRequest**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itrequest)                        | <span data-ttu-id="ff5eb-121">Fournit des méthodes qui permettent à une application TAPI 3 d’utiliser la [téléphonie assistée](assisted-telephony-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ff5eb-121">Provides methods that allow a TAPI 3 application to use [Assisted Telephony](assisted-telephony-overview.md).</span></span>                                                                                                |



 



| <span data-ttu-id="ff5eb-122">Interface</span><span class="sxs-lookup"><span data-stu-id="ff5eb-122">Interface</span></span>                                  | <span data-ttu-id="ff5eb-123">Description</span><span class="sxs-lookup"><span data-stu-id="ff5eb-123">Description</span></span>                                                                                                                                                                |
|--------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ff5eb-124">**ITMediaControl**</span><span class="sxs-lookup"><span data-stu-id="ff5eb-124">**ITMediaControl**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itmediacontrol)   | <span data-ttu-id="ff5eb-125">Démarre, arrête et interrompt les actions en cours, telles qu’une lecture.</span><span class="sxs-lookup"><span data-stu-id="ff5eb-125">Starts, stops, and pauses current actions, such as a playback.</span></span>                                                                                                             |
| [<span data-ttu-id="ff5eb-126">**ITMediaPlayback**</span><span class="sxs-lookup"><span data-stu-id="ff5eb-126">**ITMediaPlayback**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itmediaplayback) | <span data-ttu-id="ff5eb-127">Fournit des méthodes spécifiques à la lecture qui permettent à une application d’effectuer des opérations telles que définir la liste des fichiers à lire et modifier la vitesse de lecture.</span><span class="sxs-lookup"><span data-stu-id="ff5eb-127">Provides playback-specific methods that allow an application to perform such operations as setting the list of files to play and changing the playback speed.</span></span>              |
| [<span data-ttu-id="ff5eb-128">**ITMediaRecord**</span><span class="sxs-lookup"><span data-stu-id="ff5eb-128">**ITMediaRecord**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itmediarecord)     | <span data-ttu-id="ff5eb-129">Fournit des méthodes spécifiques à l’enregistrement qui permettent à une application d’effectuer des opérations telles que la définition des noms des fichiers à enregistrer et la modification de la durée d’un enregistrement.</span><span class="sxs-lookup"><span data-stu-id="ff5eb-129">Provides recording-specific methods that allow an application to perform such operations as setting the names of files to record and changing the duration of a recording.</span></span> |



 



| <span data-ttu-id="ff5eb-130">Interface</span><span class="sxs-lookup"><span data-stu-id="ff5eb-130">Interface</span></span>                                                  | <span data-ttu-id="ff5eb-131">Description</span><span class="sxs-lookup"><span data-stu-id="ff5eb-131">Description</span></span>                                                                                                                                                         |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ff5eb-132">**ITScriptableAudioFormat**</span><span class="sxs-lookup"><span data-stu-id="ff5eb-132">**ITScriptableAudioFormat**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itscriptableaudioformat) | <span data-ttu-id="ff5eb-133">Récupère le format audio de ou définit le format audio pour une piste.</span><span class="sxs-lookup"><span data-stu-id="ff5eb-133">Retrieves the audio format from, or sets the audio format for, a track.</span></span>                                                                                             |
| [<span data-ttu-id="ff5eb-134">**ITStaticAudioTerminal**</span><span class="sxs-lookup"><span data-stu-id="ff5eb-134">**ITStaticAudioTerminal**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itstaticaudioterminal)     | <span data-ttu-id="ff5eb-135">Fournit des méthodes sur les objets de terminal audio statiques qui sont nécessaires pour prendre en charge les appareils téléphoniques.</span><span class="sxs-lookup"><span data-stu-id="ff5eb-135">Provides methods on static audio terminal objects that are needed to support phone devices.</span></span> <span data-ttu-id="ff5eb-136">Les MSP TAPI 3,1 doivent exposer cette interface sur tous les terminaux audio statiques.</span><span class="sxs-lookup"><span data-stu-id="ff5eb-136">TAPI 3.1 MSPs must expose this interface on all static audio terminals.</span></span> |



 

 

 
