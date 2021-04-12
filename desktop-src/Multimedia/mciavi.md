---
title: MCIAVI
description: MCIAVI
ms.assetid: 68639f35-bc20-457d-b937-760af8323dce
keywords:
- Périphériques MCI, pilote MCIAVI
- Commandes MCI, pilote MCIAVI
- Pilote MCIAVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be2e69cf2b0fd9ee71650c56b0d7d9efb50a46e4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104462322"
---
# <a name="mciavi"></a><span data-ttu-id="a8b50-106">MCIAVI</span><span class="sxs-lookup"><span data-stu-id="a8b50-106">MCIAVI</span></span>

<span data-ttu-id="a8b50-107">Un fichier AVI peut contenir plus de deux flux, par exemple une séquence vidéo, une piste audio anglaise et une bande son française.</span><span class="sxs-lookup"><span data-stu-id="a8b50-107">An AVI file can contain more than two streams — for example, a video sequence, an English soundtrack, and a French soundtrack.</span></span> <span data-ttu-id="a8b50-108">Votre application peut utiliser un flux indépendamment des autres flux du fichier.</span><span class="sxs-lookup"><span data-stu-id="a8b50-108">Your application can use a stream independently of the other streams in the file.</span></span>

<span data-ttu-id="a8b50-109">Le type d’appareil **Digitalvideo** contrôle les fichiers vidéo.</span><span class="sxs-lookup"><span data-stu-id="a8b50-109">The **digitalvideo** device type controls video files.</span></span> <span data-ttu-id="a8b50-110">Pour obtenir la liste des commandes MCI reconnues par les périphériques vidéo numériques, consultez [jeu de commandes vidéo numérique](digital-video-command-set.md).</span><span class="sxs-lookup"><span data-stu-id="a8b50-110">For a list of the MCI commands recognized by digital-video devices, see [Digital-Video Command Set](digital-video-command-set.md).</span></span>

<span data-ttu-id="a8b50-111">Le pilote MCIAVI lit les séquences vidéo et d’autres flux de données sous le contrôle de commandes MCI.</span><span class="sxs-lookup"><span data-stu-id="a8b50-111">The MCIAVI driver plays video sequences and other data streams under the control of MCI commands.</span></span> <span data-ttu-id="a8b50-112">Les flux de données peuvent contenir des images, des données audio et des palettes.</span><span class="sxs-lookup"><span data-stu-id="a8b50-112">Data streams can contain images, audio, and palettes.</span></span> <span data-ttu-id="a8b50-113">Les données de l’image peuvent se composer d’images avec des palettes de couleurs ou des informations de couleurs vraies.</span><span class="sxs-lookup"><span data-stu-id="a8b50-113">The image data can consist of images with either color palettes or true-color information.</span></span>

<span data-ttu-id="a8b50-114">L’audio est synchronisé avec la vidéo dans un trentième de seconde.</span><span class="sxs-lookup"><span data-stu-id="a8b50-114">Audio is synchronized with the video within one-thirtieth of a second.</span></span> <span data-ttu-id="a8b50-115">Toutefois, si le matériel audio n’est pas disponible, le pilote ne lit que le flux vidéo.</span><span class="sxs-lookup"><span data-stu-id="a8b50-115">If audio hardware is not available, however, the driver plays only the video stream.</span></span> <span data-ttu-id="a8b50-116">Le pilote MCIAVI peut supprimer des images vidéo, si nécessaire, pour lire un flux sans interruption audio.</span><span class="sxs-lookup"><span data-stu-id="a8b50-116">The MCIAVI driver can drop video frames, if necessary, to play a stream without audio interruption.</span></span>

<span data-ttu-id="a8b50-117">Votre application peut utiliser les services de la classe de fenêtre MCIWnd au lieu de l’interface de commande MCI pour contrôler tout pilote MCI.</span><span class="sxs-lookup"><span data-stu-id="a8b50-117">Your application can use the MCIWnd window class services instead of the MCI command interface to control any MCI driver.</span></span> <span data-ttu-id="a8b50-118">Cette classe de fenêtre gère la plupart des détails de la gestion de la fenêtre qui prend en charge le périphérique MCI et simplifie la programmation requise pour envoyer les commandes MCI.</span><span class="sxs-lookup"><span data-stu-id="a8b50-118">This window class handles many of the details of managing the window supporting the MCI device and simplifies the programming required to send the MCI commands.</span></span> <span data-ttu-id="a8b50-119">Votre application peut utiliser directement les services de bibliothèque MCIWnd pour contrôler l’appareil MCI, ou elle peut avoir des MCIWnd afficher une barre d’outils, une barre de défilement et des menus qui permettent à l’utilisateur de contrôler l’appareil.</span><span class="sxs-lookup"><span data-stu-id="a8b50-119">Your application can use the MCIWnd library services directly to control the MCI device, or it can have MCIWnd display a toolbar, scroll bar, and menus that let the user control the device.</span></span> <span data-ttu-id="a8b50-120">Pour plus d’informations sur la classe de fenêtre MCIWnd, consultez [classe de fenêtre MCIWnd](mciwnd-window-class.md).</span><span class="sxs-lookup"><span data-stu-id="a8b50-120">For more information about the MCIWnd window class, see [MCIWnd Window Class](mciwnd-window-class.md).</span></span>

 

 




