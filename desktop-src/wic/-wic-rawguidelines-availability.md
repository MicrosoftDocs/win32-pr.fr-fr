---
description: Disponibilité du codec et prise en charge des plateformes
ms.assetid: 6b3d09c9-e91f-4c62-92f7-c2643e51987f
title: Disponibilité du codec et prise en charge des plateformes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcc485c5f8db9ff7883263cd614578705eccd3fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204213"
---
# <a name="codec-availability-and-platform-support"></a><span data-ttu-id="75881-103">Disponibilité du codec et prise en charge des plateformes</span><span class="sxs-lookup"><span data-stu-id="75881-103">Codec Availability and Platform Support</span></span>

<span data-ttu-id="75881-104">Microsoft recommande aux fournisseurs d’appareils photo de mettre à jour les codecs WIC dans la distribution de logiciels avec les nouvelles caméras et d’installer le codec mis à jour avec l’installation du logiciel du fournisseur par défaut Windows 7, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="75881-104">Microsoft recommends that camera vendors include updated RAW Windows Imaging Component (WIC) codecs in the software distribution with new cameras and that the updated codec be installed with the default vendor software installation Windows 7, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="75881-105">Les fournisseurs d’appareils photo doivent également fournir le dernier codec WIC en téléchargement à partir de leurs sites de support.</span><span class="sxs-lookup"><span data-stu-id="75881-105">Camera vendors should also provide the latest WIC codec as a download from their support sites.</span></span>

## <a name="codec-discovery"></a><span data-ttu-id="75881-106">Détection de codec</span><span class="sxs-lookup"><span data-stu-id="75881-106">Codec Discovery</span></span>

<span data-ttu-id="75881-107">Microsoft fait ce qui suit pour aider à pointer les utilisateurs vers les sites Web des fournisseurs pour les téléchargements de codec :</span><span class="sxs-lookup"><span data-stu-id="75881-107">Microsoft is doing the following to help point users to vendors' Web sites for codec downloads:</span></span>

-   <span data-ttu-id="75881-108">Dans l’Explorateur Windows, si un utilisateur double-clique sur un fichier qui n’est pas reconnu (cas par défaut lorsqu’un fichier brut se trouve sur l’ordinateur, mais que le codec n’est pas encore installé), une boîte de dialogue indique que le fichier n’est pas reconnu et vous demande si l’utilisateur souhaite trouver un programme qui comprend le fichier.</span><span class="sxs-lookup"><span data-stu-id="75881-108">In Windows Explorer, if a user double-clicks a file that is not recognized (the default case when a RAW file is on the computer, but the codec is not installed yet), a dialog box reports that the file is not recognized and asks whether the user wants to find a program that understands the file.</span></span> <span data-ttu-id="75881-109">Microsoft gère un service de redirection existant pour transférer les utilisateurs vers les sites Web des fournisseurs qui peuvent fournir le programme pour comprendre le fichier.</span><span class="sxs-lookup"><span data-stu-id="75881-109">Microsoft maintains an existing redirection service to forward users to vendors' Web sites that can supply the program to understand the file.</span></span> <span data-ttu-id="75881-110">Cette fonctionnalité existe dans Windows XP et Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="75881-110">This facility exists in Windows XP and in Windows Vista.</span></span>
-   <span data-ttu-id="75881-111">La Galerie de photos Windows, la Galerie de photos Windows Live et la visionneuse de photos Windows 7 reconnaissent un ensemble d’extensions de fichier en tant que fichiers BRUTs.</span><span class="sxs-lookup"><span data-stu-id="75881-111">The Windows Photo Gallery, Windows Live Photo Gallery, and the Windows 7 Photo Viewer recognize a set of file extensions as RAW files.</span></span> <span data-ttu-id="75881-112">Si des fichiers de ce jeu sont trouvés dans des dossiers que ces applications examinent et qu’un codec pour le fichier n’est pas déjà installé, une boîte de dialogue s’affiche, comme décrit dans le paragraphe précédent.</span><span class="sxs-lookup"><span data-stu-id="75881-112">If files from that set are found in folders that any of these applications are looking at, and a codec for the file is not already installed, then a dialog box appears, as described in the preceding paragraph.</span></span>

<span data-ttu-id="75881-113">Pour plus d’informations sur la détection des codecs, consultez disponibilité du codec et prise en charge de la plateforme.</span><span class="sxs-lookup"><span data-stu-id="75881-113">For more information about codec discovery, see Codec Availability and Platform Support.</span></span>

## <a name="windows-xp-platform-support"></a><span data-ttu-id="75881-114">Prise en charge des plateformes Windows XP</span><span class="sxs-lookup"><span data-stu-id="75881-114">Windows XP Platform Support</span></span>

<span data-ttu-id="75881-115">Microsoft a publié Windows XP SP3 avec WIC et un programme d’installation autonome de WIC pour Windows XP SP2.</span><span class="sxs-lookup"><span data-stu-id="75881-115">Microsoft has released Windows XP SP3 with WIC, and a standalone WIC installer for Windows XP SP2.</span></span> <span data-ttu-id="75881-116">Celles-ci utilisent des codecs WIC pour permettre la prise en charge des miniatures et des aperçus sur ces plateformes.</span><span class="sxs-lookup"><span data-stu-id="75881-116">These use WIC codecs to enable support for thumbnails and previews on those platforms.</span></span> <span data-ttu-id="75881-117">Par conséquent, il est important que le téléchargement et l’installation du codec soient pris en charge et testés sur Windows 7, Windows Vista et Windows XP.</span><span class="sxs-lookup"><span data-stu-id="75881-117">Therefore, it is important that codec download and installation be supported and tested on the Windows 7, Windows Vista, and Windows XP.</span></span>

## <a name="related-topics"></a><span data-ttu-id="75881-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="75881-118">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="75881-119">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="75881-119">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="75881-120">Vue d’ensemble du composant Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="75881-120">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="75881-121">Recommandations de WIC pour les formats d’image RAW Camera</span><span class="sxs-lookup"><span data-stu-id="75881-121">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="75881-122">Comment écrire un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="75881-122">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



