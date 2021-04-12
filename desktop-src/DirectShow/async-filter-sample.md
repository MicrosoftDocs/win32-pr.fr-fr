---
description: Exemple de filtre Async
ms.assetid: ad1f2386-6d23-4a6d-8542-bbca53df4825
title: Exemple de filtre Async
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 099931e9a20c977da18a67f9fe232c2ec391dd4e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104033544"
---
# <a name="async-filter-sample"></a><span data-ttu-id="7cbb4-103">Exemple de filtre Async</span><span class="sxs-lookup"><span data-stu-id="7cbb4-103">Async Filter Sample</span></span>

## <a name="description"></a><span data-ttu-id="7cbb4-104">Description</span><span class="sxs-lookup"><span data-stu-id="7cbb4-104">Description</span></span>

<span data-ttu-id="7cbb4-105">L’exemple de filtre Async est un filtre de lecteur de fichier qui prend en charge le téléchargement progressif.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-105">The Async Filter sample is a file reader filter that supports progressive download.</span></span> <span data-ttu-id="7cbb4-106">Cet exemple de filtre implémente les interfaces [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) et [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) .</span><span class="sxs-lookup"><span data-stu-id="7cbb4-106">This sample filter implements the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) and [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter) interfaces.</span></span> <span data-ttu-id="7cbb4-107">Il prend en charge les fichiers MPEG, mais pas les fichiers AVI.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-107">It supports MPEG files, but not AVI files.</span></span>

## <a name="usage"></a><span data-ttu-id="7cbb4-108">Utilisation</span><span class="sxs-lookup"><span data-stu-id="7cbb4-108">Usage</span></span>

<span data-ttu-id="7cbb4-109">Cet exemple comprend une petite application en ligne de commande, Memfile.exe, qui illustre le filtre.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-109">This sample includes a small command-line application, Memfile.exe, that demonstrates the filter.</span></span> <span data-ttu-id="7cbb4-110">Les arguments de ligne de commande spécifient un fichier multimédia et une vitesse de transmission, en kilo-octets par seconde.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-110">The command-line arguments specify a media file and a bit rate, in kilobytes per second.</span></span> <span data-ttu-id="7cbb4-111">L’application lit le fichier en mémoire à la vitesse spécifiée et lit le fichier.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-111">The application reads the file into memory at the specified rate and plays the file.</span></span> <span data-ttu-id="7cbb4-112">Pour ce faire, il crée une instance du filtre, ajoute le filtre au graphique de filtre et restitue la broche de sortie du filtre.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-112">To do so, it creates an instance of the filter, adds the filter to the filter graph, and renders the filter's output pin.</span></span>

<span data-ttu-id="7cbb4-113">Sur la ligne de commande, tapez :</span><span class="sxs-lookup"><span data-stu-id="7cbb4-113">At the command line, type:</span></span>

<span data-ttu-id="7cbb4-114">**Débit binaire de nom de fichier Memfile**</span><span class="sxs-lookup"><span data-stu-id="7cbb4-114">**Memfile Filename BitRate**</span></span>  

<span data-ttu-id="7cbb4-115">Le filtre d’exemple Async ne prend pas en charge les fichiers AVI, car il ne peut pas se connecter au filtre de [fractionnement AVI](avi-splitter-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="7cbb4-115">The Async sample filter does not support AVI files, because it cannot connect to the [AVI Splitter](avi-splitter-filter.md) filter.</span></span> <span data-ttu-id="7cbb4-116">La broche de sortie du filtre Async propose un flux de MEDIATYPE \_ et MEDIASUBTYPE \_ null pour le type de média.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-116">The Async filter's output pin proposes MEDIATYPE\_Stream and MEDIASUBTYPE\_NULL for the media type.</span></span> <span data-ttu-id="7cbb4-117">La broche d’entrée sur le filtre de séparateur AVI n’accepte pas la \_ valeur null MEDIASUBTYPE et ne propose pas de types propres.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-117">The input pin on the AVI Splitter filter does not accept MEDIASUBTYPE\_NULL, and does not propose any types of its own.</span></span> <span data-ttu-id="7cbb4-118">Par conséquent, la connexion du code confidentiel échoue.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-118">Therefore, the pin connection fails.</span></span> <span data-ttu-id="7cbb4-119">Le filtre asynchrone peut être amélioré pour proposer MEDIASUBTYPE \_ AVI le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-119">The Async filter could be enhanced to offer MEDIASUBTYPE\_Avi when appropriate.</span></span> <span data-ttu-id="7cbb4-120">Par exemple, il peut examiner le format de fichier ou utiliser l’extension de fichier.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-120">For example, it could examine the file format, or use the file extension.</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="7cbb4-121">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="7cbb4-121">Downloading the Sample</span></span>

<span data-ttu-id="7cbb4-122">Pour télécharger les exemples du kit de développement logiciel (SDK) DirectShow, installez la dernière version du [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="7cbb4-122">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="7cbb4-123">Cet exemple est installé sous le chemin d’accès suivant : \[ exemples *racine SDK* \] \\ \\ \\ filtres DirectShow multimédias \\ \\ asynchrones.</span><span class="sxs-lookup"><span data-stu-id="7cbb4-123">This sample is installed under the following path: \[*SDK Root*\]\\Samples\\Multimedia\\DirectShow\\Filters\\Async.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7cbb4-124">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7cbb4-124">Related topics</span></span>



[<span data-ttu-id="7cbb4-125">Exemples DirectShow</span><span class="sxs-lookup"><span data-stu-id="7cbb4-125">DirectShow Samples</span></span>](directshow-samples.md)


 

 



