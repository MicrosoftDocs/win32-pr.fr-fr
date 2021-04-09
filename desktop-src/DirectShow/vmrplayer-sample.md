---
description: Exemple VMRPlayer
ms.assetid: 7fc893a6-afa5-4ada-9295-29122b43b21e
title: Exemple VMRPlayer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2214d94628a90daf0dd543f4e3a7f0166f4968a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863398"
---
# <a name="vmrplayer-sample"></a><span data-ttu-id="a7a15-103">Exemple VMRPlayer</span><span class="sxs-lookup"><span data-stu-id="a7a15-103">VMRPlayer Sample</span></span>

## <a name="description"></a><span data-ttu-id="a7a15-104">Description</span><span class="sxs-lookup"><span data-stu-id="a7a15-104">Description</span></span>

<span data-ttu-id="a7a15-105">Cet exemple utilise le filtre de mixage vidéo 9 (VMR-9) pour mélanger alpha une ou deux vidéos en cours d’exécution et une image statique.</span><span class="sxs-lookup"><span data-stu-id="a7a15-105">This sample uses the Video Mixing Renderer 9 (VMR-9) filter to alpha blend one or two running videos and a static image.</span></span>

## <a name="usage"></a><span data-ttu-id="a7a15-106">Utilisation</span><span class="sxs-lookup"><span data-stu-id="a7a15-106">Usage</span></span>

<span data-ttu-id="a7a15-107">Pour ouvrir la première vidéo, choisissez **ouvrir le flux principal** dans le menu **fichier** .</span><span class="sxs-lookup"><span data-stu-id="a7a15-107">To open the first video, choose **Open Primary Stream** from the **File** menu.</span></span> <span data-ttu-id="a7a15-108">Pour ouvrir une deuxième vidéo, choisissez **ouvrir un flux secondaire** dans le menu **fichier** (vous devez d’abord ouvrir le flux de données principal).</span><span class="sxs-lookup"><span data-stu-id="a7a15-108">To open a second video, choose **Open Secondary Stream** from the **File** menu (you must open the primary stream first).</span></span> <span data-ttu-id="a7a15-109">Pour lire la vidéo, cliquez sur le bouton **lecture** .</span><span class="sxs-lookup"><span data-stu-id="a7a15-109">To play the video, click the **Play** button.</span></span>

<span data-ttu-id="a7a15-110">Vous pouvez définir la position, la taille et les valeurs alpha des vidéos en sélectionnant **flux principal** ou **flux Secondard** dans le menu **Propriétés de VMR** .</span><span class="sxs-lookup"><span data-stu-id="a7a15-110">You can set the position, size, and alpha values of the videos by selecting **Primary Stream** or **Secondard Stream** from the **VMR Properties** menu.</span></span>

<span data-ttu-id="a7a15-111">Pour ajouter une image bitmap statique sur la vidéo, choisissez **image d’application statique** dans le menu **Propriétés de VMR** , puis cliquez sur la zone afficher l’image de l' **application** .</span><span class="sxs-lookup"><span data-stu-id="a7a15-111">To add a static bitmap over the video, choose **Static App Image** from the **VMR Properties** menu and click the **Display App Image** box.</span></span> <span data-ttu-id="a7a15-112">Vous pouvez utiliser la même boîte de dialogue pour contrôler la position, la taille et la valeur alpha de la bitmap.</span><span class="sxs-lookup"><span data-stu-id="a7a15-112">You can use the same dialog to control the position, size, and alpha value of the bitmap.</span></span>

<span data-ttu-id="a7a15-113">Pour capturer l’image vidéo fusionnée, choisissez **capturer l’image bitmap** dans le menu **Propriétés de VMR** .</span><span class="sxs-lookup"><span data-stu-id="a7a15-113">To capture the blended video image, choose **Capture Bitmap Image** from the **VMR Properties** menu.</span></span>

<span data-ttu-id="a7a15-114">Vous pouvez également spécifier le flux de l’image principale à partir de la ligne de commande :</span><span class="sxs-lookup"><span data-stu-id="a7a15-114">You can also specify the primary image stream from the command line:</span></span>

<span data-ttu-id="a7a15-115">**VMRPlayer** **/p** *nom_fichier*</span><span class="sxs-lookup"><span data-stu-id="a7a15-115">**VMRPlayer** **/P** *filename*</span></span>

## <a name="downloading-the-sample"></a><span data-ttu-id="a7a15-116">Téléchargement de l’exemple</span><span class="sxs-lookup"><span data-stu-id="a7a15-116">Downloading the Sample</span></span>

<span data-ttu-id="a7a15-117">Pour télécharger les exemples du kit de développement logiciel (SDK) DirectShow, installez la dernière version du [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span><span class="sxs-lookup"><span data-stu-id="a7a15-117">To download the DirectShow SDK samples, install the latest version of the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a7a15-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a7a15-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7a15-119">Exemples DirectShow</span><span class="sxs-lookup"><span data-stu-id="a7a15-119">DirectShow Samples</span></span>](directshow-samples.md)
</dt> </dl>

 

 



