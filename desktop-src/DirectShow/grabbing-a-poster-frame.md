---
description: Saisie d’un cadre d’affiche
ms.assetid: 0727a1ed-1bc7-49fc-a288-00283e637a71
title: Saisie d’un cadre d’affiche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2cf06a10d74bb6c81622ac9bad7a1b770f5dc12
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482696"
---
# <a name="grabbing-a-poster-frame"></a><span data-ttu-id="3a428-103">Saisie d’un cadre d’affiche</span><span class="sxs-lookup"><span data-stu-id="3a428-103">Grabbing a Poster Frame</span></span>

<span data-ttu-id="3a428-104">\[Cette API n’est pas prise en charge et peut être modifiée ou non disponible à l’avenir.\]</span><span class="sxs-lookup"><span data-stu-id="3a428-104">\[This API is not supported and may be altered or unavailable in the future.\]</span></span>

<span data-ttu-id="3a428-105">Cet article explique comment afficher un cadre d’affiche à partir d’un fichier multimédia numérique, à l’aide de l’objet [détecteur de média (MediaDet)](media-detector--mediadet.md) fourni avec les [services de modification DirectShow](directshow-editing-services.md).</span><span class="sxs-lookup"><span data-stu-id="3a428-105">This article describes how to display a poster frame from a digital media file, using the [Media Detector (MediaDet)](media-detector--mediadet.md) object provided with [DirectShow Editing Services](directshow-editing-services.md).</span></span>

<span data-ttu-id="3a428-106">Le détecteur de média est un objet d’assistance qui peut obtenir des informations de format à partir d’un fichier source de média.</span><span class="sxs-lookup"><span data-stu-id="3a428-106">The Media Detector is a helper object that can get format information from a media source file.</span></span> <span data-ttu-id="3a428-107">Il peut également récupérer une image bitmap à partir d’un flux vidéo dans le fichier source.</span><span class="sxs-lookup"><span data-stu-id="3a428-107">It can also grab a bitmap image from a video stream in the source file.</span></span> <span data-ttu-id="3a428-108">En supposant que le fichier peut être recherché, vous pouvez obtenir l’image à partir de n’importe quel point du fichier.</span><span class="sxs-lookup"><span data-stu-id="3a428-108">Assuming the file is seekable, you can obtain the image from any point in the file.</span></span> <span data-ttu-id="3a428-109">L’image retournée est toujours au format RGB 24 bits.</span><span class="sxs-lookup"><span data-stu-id="3a428-109">The returned image is always in 24-bit RGB format.</span></span>

<span data-ttu-id="3a428-110">Le détecteur de média n’est pas un filtre et l’application n’a pas besoin d’utiliser le gestionnaire de graphique de filtre ou de créer un graphique de filtre.</span><span class="sxs-lookup"><span data-stu-id="3a428-110">The Media Detector is not a filter, and the application does not need to use the Filter Graph Manager or create a filter graph.</span></span> <span data-ttu-id="3a428-111">En interne, le détecteur de média crée un graphique de filtre qui contient l' [**exemple de filtre d’accrochage**](sample-grabber-filter.md).</span><span class="sxs-lookup"><span data-stu-id="3a428-111">Internally, the Media Detector creates a filter graph that contains the [**Sample Grabber Filter**](sample-grabber-filter.md).</span></span> <span data-ttu-id="3a428-112">Pour obtenir une image bitmap, le détecteur de média recherche et interrompt le graphique de filtre, puis récupère le bitmap à partir de l’exemple de filtre d’accrochage.</span><span class="sxs-lookup"><span data-stu-id="3a428-112">To get a bitmap, the Media Detector seeks and pauses the filter graph, and then retrieves the bitmap from the Sample Grabber filter.</span></span> <span data-ttu-id="3a428-113">L’application communique avec le détecteur de média par le biais de l’interface [**IMediaDet**](imediadet.md) .</span><span class="sxs-lookup"><span data-stu-id="3a428-113">The application communicates with the Media Detector through the [**IMediaDet**](imediadet.md) interface.</span></span> <span data-ttu-id="3a428-114">Le détecteur de média est un bon exemple d’encapsulation d’un graphique de filtre à l’intérieur d’un objet d’assistance, afin de protéger les applications des détails liés au graphique.</span><span class="sxs-lookup"><span data-stu-id="3a428-114">The Media Detector is a good example of encapsulating a filter graph inside a helper object, in order to shield applications from graph-related details.</span></span>

<span data-ttu-id="3a428-115">Le détecteur de média fonctionne en deux modes.</span><span class="sxs-lookup"><span data-stu-id="3a428-115">The Media Detector operates in two modes.</span></span> <span data-ttu-id="3a428-116">La première fois que vous la créez, le détecteur de média est en mode « collecte d’informations ».</span><span class="sxs-lookup"><span data-stu-id="3a428-116">When you first create it, the Media Detector is in "information gathering" mode.</span></span> <span data-ttu-id="3a428-117">Vous pouvez spécifier le nom d’un fichier multimédia et obtenir des informations sur chacun des flux du fichier, tels que le type de format, la fréquence d’images ou la durée.</span><span class="sxs-lookup"><span data-stu-id="3a428-117">You can specify the name of a media file and get information about each of the streams in the file, such as the format type, the frame rate, or the duration.</span></span> <span data-ttu-id="3a428-118">Si le fichier contient un flux vidéo, vous pouvez basculer le détecteur de média en mode « manipulation bitmap » et récupérer les bitmaps à partir de la source.</span><span class="sxs-lookup"><span data-stu-id="3a428-118">If the file contains a video stream, you can switch the Media Detector into "bitmap grab" mode and retrieve bitmaps from the source.</span></span> <span data-ttu-id="3a428-119">Toutefois, une fois que vous avez fait cela, vous ne pouvez pas rétablir le mode d’origine du détecteur de média. elle est attachée de manière permanente à ce flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="3a428-119">However, once you do so, you cannot switch the Media Detector back to its original mode; it is permanently attached to that video stream.</span></span> <span data-ttu-id="3a428-120">Pour utiliser un autre flux ou un autre fichier, vous devez créer une nouvelle instance du détecteur de média.</span><span class="sxs-lookup"><span data-stu-id="3a428-120">To work with another stream or another file, you must create a new instance of the Media Detector.</span></span>

> [!Note]  
> <span data-ttu-id="3a428-121">Les exemples de code de ce didacticiel utilisent la classe ATL **CComPtr** qui gère automatiquement les décomptes de références.</span><span class="sxs-lookup"><span data-stu-id="3a428-121">The code examples in this tutorial use the ATL **CComPtr** class, which automatically manages reference counts.</span></span> <span data-ttu-id="3a428-122">Si vous préférez utiliser des pointeurs d’interface bruts, n’oubliez pas de libérer chaque interface lorsque vous n’en avez plus besoin.</span><span class="sxs-lookup"><span data-stu-id="3a428-122">If you prefer to use raw interface pointers, remember to release every interface when you are done with it.</span></span> <span data-ttu-id="3a428-123">Par ailleurs, par souci de concision, les exemples de code omettent une grande partie de la vérification des erreurs qu’une application doit effectuer.</span><span class="sxs-lookup"><span data-stu-id="3a428-123">Also, for brevity the code examples omit much of the error checking that an application should perform.</span></span> <span data-ttu-id="3a428-124">Dans le code de travail, vérifiez toujours les valeurs **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="3a428-124">In working code, always check **HRESULT** values.</span></span>

 

<span data-ttu-id="3a428-125">Ce didacticiel comprend les étapes suivantes :</span><span class="sxs-lookup"><span data-stu-id="3a428-125">This tutorial contains the following steps:</span></span>

-   [<span data-ttu-id="3a428-126">Étape 1 : créer le Framework Windows</span><span class="sxs-lookup"><span data-stu-id="3a428-126">Step 1: Create the Windows Framework</span></span>](step-1--create-the-windows-framework.md)
-   [<span data-ttu-id="3a428-127">Étape 2 : ajouter une commande de menu pour récupérer un cadre d’affiche</span><span class="sxs-lookup"><span data-stu-id="3a428-127">Step 2: Add a Menu Command to Grab a Poster Frame</span></span>](step-2--add-a-menu-command-to-grab-a-poster-frame.md)
-   [<span data-ttu-id="3a428-128">Étape 3 : implémenter la fonction Frame-Grabbing</span><span class="sxs-lookup"><span data-stu-id="3a428-128">Step 3: Implement the Frame-Grabbing Function</span></span>](step-3--implement-the-frame-grabbing-function.md)
-   [<span data-ttu-id="3a428-129">Étape 4 : dessiner l’image bitmap sur la zone cliente</span><span class="sxs-lookup"><span data-stu-id="3a428-129">Step 4: Draw the Bitmap on the Client Area</span></span>](step-4--draw-the-bitmap-on-the-client-area.md)

## <a name="related-topics"></a><span data-ttu-id="3a428-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="3a428-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3a428-131">Utilisation des services de modification DirectShow</span><span class="sxs-lookup"><span data-stu-id="3a428-131">Using DirectShow Editing Services</span></span>](using-directshow-editing-services.md)
</dt> </dl>

 

 



