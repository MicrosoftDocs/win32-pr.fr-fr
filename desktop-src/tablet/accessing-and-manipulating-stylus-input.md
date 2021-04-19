---
description: Le Tablet PC comprend une technologie qui permet d’interagir avec les données du stylet de tablette au fur et à mesure de leur collecte.
ms.assetid: e026f860-be4d-40a5-b951-15b8be3cd626
title: Accès et manipulation de l’entrée du stylet
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 333126f195154241333127ec585864bd9d592a08
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106515185"
---
# <a name="accessing-and-manipulating-stylus-input"></a><span data-ttu-id="8598b-103">Accès et manipulation de l’entrée du stylet</span><span class="sxs-lookup"><span data-stu-id="8598b-103">Accessing and Manipulating Stylus Input</span></span>

<span data-ttu-id="8598b-104">Le Tablet PC comprend une technologie qui permet d’interagir avec les données du stylet de tablette au fur et à mesure de leur collecte.</span><span class="sxs-lookup"><span data-stu-id="8598b-104">The Tablet PC includes technology for interacting with tablet pen data as it is being gathered.</span></span> <span data-ttu-id="8598b-105">La classe [**RealTimeStylus**](realtimestylus-class.md) fait partie des interfaces de programmation d’applications (API) StylusInput qui fournissent l’accès au flux de données de stylet de tablette.</span><span class="sxs-lookup"><span data-stu-id="8598b-105">The [**RealTimeStylus**](realtimestylus-class.md) class is part of the StylusInput application programming interfaces (API), which provide access to the tablet pen data stream.</span></span> <span data-ttu-id="8598b-106">Ces API vous permettent de capturer, d’interrompre et de modifier le flux de façon indépendante du rendu et de la collecte de l’encre.</span><span class="sxs-lookup"><span data-stu-id="8598b-106">These APIs allow you to capture, interrupt, and modify the stream independently from rendering and collecting ink.</span></span>

<span data-ttu-id="8598b-107">Les API StylusInput sont conçues pour :</span><span class="sxs-lookup"><span data-stu-id="8598b-107">The StylusInput APIs are designed to:</span></span>

-   <span data-ttu-id="8598b-108">Fournir un accès en temps réel au flux de données de stylet de tablette.</span><span class="sxs-lookup"><span data-stu-id="8598b-108">Provide real-time access to the tablet pen data stream.</span></span>
-   <span data-ttu-id="8598b-109">Empêchez le thread d’interface utilisateur de bloquer le rendu d’encre dynamique en mettant en file d’attente les données de paquets sur le thread d’interface utilisateur et en faisant de la collection d’entrée manuscrite un thread unique.</span><span class="sxs-lookup"><span data-stu-id="8598b-109">Keep the user interface (UI) thread from blocking dynamic ink rendering by queuing the packet data on the UI thread and making ink collection single threaded.</span></span>
-   <span data-ttu-id="8598b-110">Augmentez les performances et réduisez l’utilisation globale des threads par le biais de l’objet [**InkCollector**](inkcollector-class.md) , de l’objet [**InkOverlay**](inkoverlay-class.md) , du contrôle [InkPicture](inkpicture-control-reference.md) ou du contrôle [InkEdit](inkedit-control-reference.md) pour collecter l’encre.</span><span class="sxs-lookup"><span data-stu-id="8598b-110">Increase the performance and lower the overall thread usage over using the [**InkCollector**](inkcollector-class.md) object, [**InkOverlay**](inkoverlay-class.md) object, [InkPicture](inkpicture-control-reference.md) control, or [InkEdit](inkedit-control-reference.md) control to collect ink.</span></span>

<span data-ttu-id="8598b-111">Les API StylusInput ne sont pas conçues pour fonctionner avec l’objet [**InkCollector**](inkcollector-class.md) , l’objet [**InkOverlay**](inkoverlay-class.md) , le contrôle [InkPicture](inkpicture-control-reference.md) ou le contrôle [InkEdit](inkedit-control-reference.md) .</span><span class="sxs-lookup"><span data-stu-id="8598b-111">The StylusInput APIs are not designed to work with the [**InkCollector**](inkcollector-class.md) object, [**InkOverlay**](inkoverlay-class.md) object, [InkPicture](inkpicture-control-reference.md) control, or [InkEdit](inkedit-control-reference.md) control.</span></span>

<span data-ttu-id="8598b-112">Lorsque vous devez interagir directement avec le flux de données du stylet de tablette ou lorsque votre application peut bloquer l’encrage en temps réel, utilisez l’objet [**RealTimeStylus**](realtimestylus-class.md) .</span><span class="sxs-lookup"><span data-stu-id="8598b-112">When you need to interact directly with the tablet pen data stream or when your application may block real-time inking, use the [**RealTimeStylus**](realtimestylus-class.md) object.</span></span> <span data-ttu-id="8598b-113">Utilisez l’objet [**InkCollector**](inkcollector-class.md) , l’objet [**InkOverlay**](inkoverlay-class.md) , le contrôle [InkPicture](inkpicture-control-reference.md) ou le contrôle [InkEdit](inkedit-control-reference.md) lorsque le comportement par défaut de ces objets fournit le comportement dont vous avez besoin.</span><span class="sxs-lookup"><span data-stu-id="8598b-113">Use the [**InkCollector**](inkcollector-class.md) object, [**InkOverlay**](inkoverlay-class.md) object, [InkPicture](inkpicture-control-reference.md) control, or [InkEdit](inkedit-control-reference.md) control when the default behavior of these objects provides the behavior you need.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8598b-114">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="8598b-114">In This Section</span></span>

<span data-ttu-id="8598b-115">Les sections suivantes décrivent les éléments des API StylusInput :</span><span class="sxs-lookup"><span data-stu-id="8598b-115">The following sections describe elements of the StylusInput APIs:</span></span>

-   [<span data-ttu-id="8598b-116">Architecture des API StylusInput</span><span class="sxs-lookup"><span data-stu-id="8598b-116">Architecture of the StylusInput APIs</span></span>](architecture-of-the-stylusinput-apis.md)
-   [<span data-ttu-id="8598b-117">Utilisation des API StylusInput</span><span class="sxs-lookup"><span data-stu-id="8598b-117">Working with the StylusInput APIs</span></span>](working-with-the-stylusinput-apis.md)
    -   [<span data-ttu-id="8598b-118">Utilisation de la classe RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="8598b-118">Working with the RealTimeStylus Class</span></span>](working-with-the-realtimestylus-class.md)
    -   [<span data-ttu-id="8598b-119">Plug-ins et classe RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="8598b-119">Plug-ins and the RealTimeStylus Class</span></span>](plug-ins-and-the-realtimestylus-class.md)
    -   [<span data-ttu-id="8598b-120">Données de plug-in et classe RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="8598b-120">Plug-in Data and the RealTimeStylus Class</span></span>](plug-in-data-and-the-realtimestylus-class.md)
    -   [<span data-ttu-id="8598b-121">Remarques sur l’implémentation des API StylusInput</span><span class="sxs-lookup"><span data-stu-id="8598b-121">Implementation Notes for the StylusInput APIs</span></span>](implementation-notes-for-the-stylusinput-apis.md)
    -   [<span data-ttu-id="8598b-122">Plug-ins de collection d’encres</span><span class="sxs-lookup"><span data-stu-id="8598b-122">Ink-Collection Plug-ins</span></span>](ink-collection-plug-ins.md)
    -   [<span data-ttu-id="8598b-123">Plug-ins de rendu dynamique</span><span class="sxs-lookup"><span data-stu-id="8598b-123">Dynamic-Renderer Plug-ins</span></span>](dynamic-renderer-plug-ins.md)
    -   [<span data-ttu-id="8598b-124">Plug-ins de reconnaissance</span><span class="sxs-lookup"><span data-stu-id="8598b-124">Recognizer Plug-ins</span></span>](recognizer-plug-ins.md)
-   [<span data-ttu-id="8598b-125">Considérations relatives à l’utilisation des API StylusInput</span><span class="sxs-lookup"><span data-stu-id="8598b-125">Considerations when Using the StylusInput APIs</span></span>](considerations-when-using-the-stylusinput-apis.md)
    -   [<span data-ttu-id="8598b-126">Considérations relatives à la conception des API StylusInput</span><span class="sxs-lookup"><span data-stu-id="8598b-126">Design Considerations for the StylusInput APIs</span></span>](design-considerations-for-the-stylusinput-apis.md)
    -   [<span data-ttu-id="8598b-127">Considérations relatives aux threads pour les API StylusInput</span><span class="sxs-lookup"><span data-stu-id="8598b-127">Threading Considerations for the StylusInput APIs</span></span>](threading-considerations-for-the-stylusinput-apis.md)

[<span data-ttu-id="8598b-128">Modèle RealTimeStylus monté en cascade</span><span class="sxs-lookup"><span data-stu-id="8598b-128">The Cascaded RealTimeStylus Model</span></span>](the-cascaded-realtimestylus-model.md)

-   [<span data-ttu-id="8598b-129">Considérations relatives à la gestion des erreurs pour les API StylusInput</span><span class="sxs-lookup"><span data-stu-id="8598b-129">Error Handling Considerations for the StylusInput APIs</span></span>](error-handling-considerations-for-the-stylusinput-apis.md)
-   [<span data-ttu-id="8598b-130">Considérations sur les performances pour les API StylusInput</span><span class="sxs-lookup"><span data-stu-id="8598b-130">Performance Considerations for the StylusInput APIs</span></span>](performance-considerations-for-the-stylusinput-apis.md)
-   [<span data-ttu-id="8598b-131">Considérations relatives à la confiance partielle pour les API StylusInput</span><span class="sxs-lookup"><span data-stu-id="8598b-131">Partial Trust Considerations for the StylusInput APIs</span></span>](partial-trust-considerations-for-the-stylusinput-apis.md)

## <a name="related-topics"></a><span data-ttu-id="8598b-132">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8598b-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8598b-133">Exemple de plug-in RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="8598b-133">RealTimeStylus Plug-in Sample</span></span>](realtimestylus-plug-in-sample.md)
</dt> <dt>

[<span data-ttu-id="8598b-134">Exemple de collection d’encres RealTimeStylus</span><span class="sxs-lookup"><span data-stu-id="8598b-134">RealTimeStylus Ink Collection Sample</span></span>](realtimestylus-ink-collection-sample.md)
</dt> </dl>

 

 



