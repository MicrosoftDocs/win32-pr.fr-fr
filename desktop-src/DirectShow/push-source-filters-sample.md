---
description: Exemple de filtres de source Push
ms.assetid: fc52f7bc-e9c7-4cd4-91e8-5c8f3450ca95
title: Exemple de filtres de source Push
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ce22c7c6d73f54152ce469b4b3bb40c20db6c29
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104521332"
---
# <a name="push-source-filters-sample"></a><span data-ttu-id="f04f7-103">Exemple de filtres de source Push</span><span class="sxs-lookup"><span data-stu-id="f04f7-103">Push Source Filters Sample</span></span>

## <a name="description"></a><span data-ttu-id="f04f7-104">Description</span><span class="sxs-lookup"><span data-stu-id="f04f7-104">Description</span></span>

<span data-ttu-id="f04f7-105">Cet exemple se compose d’un ensemble de trois filtres sources qui fournissent les données sources suivantes sous la forme d’un flux vidéo :</span><span class="sxs-lookup"><span data-stu-id="f04f7-105">This sample consists of a set of three source filters that provide the following source data as a video stream:</span></span>

-   <span data-ttu-id="f04f7-106">CPushSourceBitmap : bitmap unique (chargée à partir du répertoire actif)</span><span class="sxs-lookup"><span data-stu-id="f04f7-106">CPushSourceBitmap: Single bitmap (loaded from current directory)</span></span>
-   <span data-ttu-id="f04f7-107">CPushSourceBitmapSet : ensemble de bitmaps (chargé à partir du répertoire actif)</span><span class="sxs-lookup"><span data-stu-id="f04f7-107">CPushSourceBitmapSet: Set of bitmaps (loaded from current directory)</span></span>
-   <span data-ttu-id="f04f7-108">CPushSourceDesktop : copie de l’image de bureau actuelle (GDI uniquement)</span><span class="sxs-lookup"><span data-stu-id="f04f7-108">CPushSourceDesktop: Copy of current desktop image (GDI only)</span></span>

## <a name="usage"></a><span data-ttu-id="f04f7-109">Utilisation</span><span class="sxs-lookup"><span data-stu-id="f04f7-109">Usage</span></span>

<span data-ttu-id="f04f7-110">Pour utiliser un filtre, chargez-le dans GraphEdit et affichez sa broche de sortie.</span><span class="sxs-lookup"><span data-stu-id="f04f7-110">To use a filter, load it into GraphEdit and render its output pin.</span></span> <span data-ttu-id="f04f7-111">Cela permet de connecter un convertisseur vidéo (et éventuellement un filtre de convertisseur d’espace colorimétrique) et d’afficher la sortie.</span><span class="sxs-lookup"><span data-stu-id="f04f7-111">This will connect a video renderer (and possibly a Color Space Converter filter) and allow you to display the output.</span></span> <span data-ttu-id="f04f7-112">Si vous souhaitez afficher la sortie dans un fichier AVI, chargez le fichier AVI MUX, chargez un filtre de writer de fichier, fournissez un nom de sortie au writer de fichier et affichez la broche de sortie du filtre PushSource.</span><span class="sxs-lookup"><span data-stu-id="f04f7-112">If you want to render the output to an AVI file, load the AVI Mux, load a File Writer Filter, provide an output name to the File Writer, and render the PushSource filter's output pin.</span></span> <span data-ttu-id="f04f7-113">Vous pouvez également charger et connecter des compresseurs vidéo, des effets vidéo, etc.</span><span class="sxs-lookup"><span data-stu-id="f04f7-113">You can also load and connect video compressors, video effects, and so on.</span></span>

> [!Note]  
> <span data-ttu-id="f04f7-114">Le filtre de capture du Bureau ne prend pas en charge les superpositions matérielles. il ne capture donc pas la vidéo rendue sur une surface de recouvrement ou des curseurs affichés via la superposition matérielle.</span><span class="sxs-lookup"><span data-stu-id="f04f7-114">The desktop capture filter does not support hardware overlays, so it will not capture video rendered to an overlay surface or cursors displayed via hardware overlay.</span></span> <span data-ttu-id="f04f7-115">Il utilise GDI pour convertir l’image de bureau actuelle en une image bitmap, qui est transmise à la broche de sortie en tant qu’exemple de média.</span><span class="sxs-lookup"><span data-stu-id="f04f7-115">It uses GDI to convert the current desktop image into a bitmap, which is passed to the output pin as a media sample.</span></span>

 

## <a name="downloading-the-sample"></a><span data-ttu-id="f04f7-116">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="f04f7-116">Downloading the Sample</span></span>

<span data-ttu-id="f04f7-117">Pour télécharger les exemples du kit de développement logiciel (SDK) DirectShow, installez la dernière version du [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="f04f7-117">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

<span data-ttu-id="f04f7-118">Cet exemple est installé sous le chemin d’accès suivant : exemples *\[ racine \] du kit de développement logiciel (SDK)* \\ fichiers de \\ \\ \\ filtres DirectShow \\ PushSource.</span><span class="sxs-lookup"><span data-stu-id="f04f7-118">This sample is installed under the following path: *\[SDK Root\]*\\Samples\\Multimedia\\DirectShow\\Filters\\PushSource.</span></span>

## <a name="related-topics"></a><span data-ttu-id="f04f7-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="f04f7-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f04f7-120">Exemples DirectShow</span><span class="sxs-lookup"><span data-stu-id="f04f7-120">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



