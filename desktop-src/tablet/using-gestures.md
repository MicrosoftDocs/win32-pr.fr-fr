---
description: Vue d’ensemble de l’utilisation des gestes.
ms.assetid: 5bc80086-7acf-4f86-a9fb-a663de489f8b
title: Utilisation des mouvements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53c267cff446d1bb6d092ba50bde21c1b3e25184
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951147"
---
# <a name="using-gestures"></a><span data-ttu-id="8562e-103">Utilisation des mouvements</span><span class="sxs-lookup"><span data-stu-id="8562e-103">Using Gestures</span></span>

<span data-ttu-id="8562e-104">La plateforme Tablet PC fournit le module de reconnaissance de mouvement Microsoft pour la prise en charge des mouvements d’application.</span><span class="sxs-lookup"><span data-stu-id="8562e-104">The Tablet PC platform provides the Microsoft gesture recognizer for supporting application gestures.</span></span> <span data-ttu-id="8562e-105">Pour obtenir la liste des mouvements pris en charge par le module de reconnaissance de mouvement de Microsoft, consultez le tableau des mouvements d’application dans l’énumération [**ApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) .</span><span class="sxs-lookup"><span data-stu-id="8562e-105">For a list of gestures supported by the Microsoft gesture recognizer, see the table of application gestures in the [**ApplicationGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inkapplicationgesture) enumeration.</span></span> <span data-ttu-id="8562e-106">Le Tablet PC prend également en charge les gestes système.</span><span class="sxs-lookup"><span data-stu-id="8562e-106">The Tablet PC also supports system gestures.</span></span> <span data-ttu-id="8562e-107">Pour obtenir la liste des gestes système pris en charge par Tablet PC, consultez la table des gestes système dans l’énumération [**SystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) .</span><span class="sxs-lookup"><span data-stu-id="8562e-107">For a list of system gestures supported by the Tablet PC, see the table of system gestures in the [**SystemGesture**](/windows/desktop/api/msinkaut/ne-msinkaut-inksystemgesture) enumeration.</span></span>

## <a name="microsoft-gesture-recognizer"></a><span data-ttu-id="8562e-108">Module de reconnaissance de mouvement Microsoft</span><span class="sxs-lookup"><span data-stu-id="8562e-108">Microsoft Gesture Recognizer</span></span>

<span data-ttu-id="8562e-109">Vous pouvez utiliser le module de reconnaissance de mouvement Microsoft à l’aide de la propriété [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) de l’objet [**InkCollector**](inkcollector-class.md) , de l’objet [**InkOverlay**](inkoverlay-class.md) ou du contrôle [InkPicture](inkpicture-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="8562e-109">You can employ the Microsoft gesture recognizer by using the [**CollectionMode**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_collectionmode) property of the [**InkCollector**](inkcollector-class.md) object, the [**InkOverlay**](inkoverlay-class.md) object, or the [InkPicture](inkpicture-control-reference.md) control.</span></span> <span data-ttu-id="8562e-110">La définition de la propriété **CollectionMode** en mode mixte (**InkAndGesture**) ou en mode geste uniquement (**GestureOnly**) transmet l’encre à la reconnaissance de mouvement Microsoft par défaut.</span><span class="sxs-lookup"><span data-stu-id="8562e-110">Setting the **CollectionMode** property to mixed mode (**InkAndGesture**) or gesture-only mode (**GestureOnly**) passes ink to the Microsoft gesture recognizer by default.</span></span> <span data-ttu-id="8562e-111">Vous pouvez utiliser le module de reconnaissance de mouvement Microsoft avec le contrôle [InkEdit](inkedit-control-reference.md) en affectant à la propriété [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) la valeur **InkAndGesture**.</span><span class="sxs-lookup"><span data-stu-id="8562e-111">You can employ the Microsoft gesture recognizer with the [InkEdit](inkedit-control-reference.md) control by setting the [**InkMode**](/windows/desktop/api/inked/nf-inked-iinkedit-get_inkmode) property to **InkAndGesture**.</span></span> <span data-ttu-id="8562e-112">Vous pouvez également utiliser la reconnaissance de mouvement avec l’objet [**RealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) en ajoutant un objet [**GestureRecognizer**](gesturerecognizer-class.md) à l’une de ses collections de plug-ins.</span><span class="sxs-lookup"><span data-stu-id="8562e-112">You can also use gesture recognition with the [**RealTimeStylus**](/windows/desktop/api/RTSCom/nn-rtscom-irealtimestylus) object by adding a [**GestureRecognizer**](gesturerecognizer-class.md) object to one of its plug-in collections.</span></span>

<span data-ttu-id="8562e-113">Toutefois, si les mouvements que vous souhaitez utiliser ne sont pas pris en charge par la version actuelle du module de reconnaissance de mouvement Microsoft, vous pouvez créer votre propre module de reconnaissance et l’utiliser conjointement avec le module de reconnaissance de mouvement Microsoft.</span><span class="sxs-lookup"><span data-stu-id="8562e-113">However, if the gestures that you want to use are not supported by the current version of the Microsoft gesture recognizer, you can build your own recognizer and use it in conjunction with the Microsoft gesture recognizer.</span></span> <span data-ttu-id="8562e-114">Cela permet la prise en charge complète des mouvements dans votre application.</span><span class="sxs-lookup"><span data-stu-id="8562e-114">This allows full support for the gestures in your application.</span></span>

<span data-ttu-id="8562e-115">Le Tablet PC utilise un stylet pour une partie ou la totalité de l’entrée.</span><span class="sxs-lookup"><span data-stu-id="8562e-115">The Tablet PC uses a pen for some or all input.</span></span> <span data-ttu-id="8562e-116">Il est ainsi très facile d’écrire de l’encre.</span><span class="sxs-lookup"><span data-stu-id="8562e-116">This makes it extremely easy to write ink.</span></span> <span data-ttu-id="8562e-117">La plateforme Tablet PC offre une architecture d’entrée de stylet qui prend en charge une structure à plusieurs niveaux de mouvements.</span><span class="sxs-lookup"><span data-stu-id="8562e-117">The Tablet PC platform delivers architecture for pen input that supports a tiered structure of gestures.</span></span> <span data-ttu-id="8562e-118">Les mouvements et le mappage sont définis pour permettre à l’utilisateur d’écrire et d’appeler des mouvements avancés sur de nouvelles surfaces, tout en réservant les gestes qui appellent des messages de souris traditionnels d’autres applications Windows.</span><span class="sxs-lookup"><span data-stu-id="8562e-118">Gestures and mapping are defined to allow the user to write and invoke advanced gestures on new surfaces, while reserving gestures that invoke traditional mouse messages of other Windows-based applications.</span></span>

<span data-ttu-id="8562e-119">La plateforme Tablet PC introduit deux niveaux de gestes : les gestes système, également appelés événements système et les gestes d’application.</span><span class="sxs-lookup"><span data-stu-id="8562e-119">The Tablet PC platform introduces two levels of gestures: system gestures, also known as system events, and application gestures.</span></span> <span data-ttu-id="8562e-120">L’architecture du stylet prend en charge les gestes du système et de l’application.</span><span class="sxs-lookup"><span data-stu-id="8562e-120">The pen architecture supports both system and application gestures.</span></span> <span data-ttu-id="8562e-121">Les gestes d’application à un seul trait et à plusieurs traits sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="8562e-121">Both single-stroke and multiple-stroke application gestures are supported.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8562e-122">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8562e-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8562e-123">Mouvements d’application</span><span class="sxs-lookup"><span data-stu-id="8562e-123">Application Gestures</span></span>](application-gestures.md)
</dt> <dt>

[<span data-ttu-id="8562e-124">Mouvements de raccourcis</span><span class="sxs-lookup"><span data-stu-id="8562e-124">Flicks Gestures</span></span>](flicks-gestures.md)
</dt> <dt>

[<span data-ttu-id="8562e-125">Gestes système</span><span class="sxs-lookup"><span data-stu-id="8562e-125">System Gestures</span></span>](system-gestures.md)
</dt> </dl>

 

 



