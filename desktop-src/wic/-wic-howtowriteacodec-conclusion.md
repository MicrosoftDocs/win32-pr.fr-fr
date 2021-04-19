---
description: La création de votre codec sur la plateforme WIC (Windows Imaging Component) permet à toutes les applications basées sur WIC d’obtenir la même prise en charge de plate-forme pour votre format d’image qu’elles obtiennent pour les formats d’image courants fournis avec la plateforme.
ms.assetid: 4f25f0f4-246c-4cbd-bd11-d061dbc7de45
title: Conclusion (écriture d’un codec WIC-Enabled)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de165f20ff81094c3b64d7e9667795f0bf80cef8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106527924"
---
# <a name="conclusion-how-to-write-a-wic-enabled-codec"></a><span data-ttu-id="05390-103">Conclusion (écriture d’un codec WIC-Enabled)</span><span class="sxs-lookup"><span data-stu-id="05390-103">Conclusion (How to Write a WIC-Enabled Codec)</span></span>

<span data-ttu-id="05390-104">La création de votre codec sur la plateforme WIC (Windows Imaging Component) permet à toutes les applications basées sur WIC d’obtenir la même prise en charge de plate-forme pour votre format d’image qu’elles obtiennent pour les formats d’image courants fournis avec la plateforme.</span><span class="sxs-lookup"><span data-stu-id="05390-104">Building your codec on the Windows Imaging Component (WIC) platform makes it possible for all applications built on WIC to get the same platform support for your image format that they get for the common image formats shipped with the platform.</span></span> <span data-ttu-id="05390-105">Il permet également à la Galerie de photos Windows Vista, à l’Explorateur Windows et à la visionneuse de photos d’afficher des miniatures et des aperçus d’images dans votre format à l’aide du décodeur que vous fournissez.</span><span class="sxs-lookup"><span data-stu-id="05390-105">It also enables the Windows Vista Photo Gallery, Windows Explorer, and Photo Viewer to display thumbnails and previews of images in your format using the decoder that you provide.</span></span> <span data-ttu-id="05390-106">Pour les formats bruts, il permet aux applications de création d’images plus sophistiquées de tirer parti des fonctionnalités de traitement brut de votre décodeur.</span><span class="sxs-lookup"><span data-stu-id="05390-106">For raw formats, it enables more sophisticated imaging applications to take advantage of your decoder’s raw processing capabilities.</span></span> <span data-ttu-id="05390-107">En fonction des options d’encodeur que vous prenez en charge, vous pouvez également exposer des fonctionnalités uniques de votre encodeur pour permettre aux applications de tirer pleinement parti des fonctionnalités avancées de votre format d’image.</span><span class="sxs-lookup"><span data-stu-id="05390-107">Depending on the encoder options you support, you can also expose unique capabilities of your encoder to enable applications to take full advantage of the advanced features of your image format.</span></span>

<span data-ttu-id="05390-108">Le développement d’un codec avec WIC activé nécessite que vous implémentiez de nouvelles interfaces.</span><span class="sxs-lookup"><span data-stu-id="05390-108">Developing a WIC-enabled codec requires you to implement some new interfaces.</span></span> <span data-ttu-id="05390-109">Dans de nombreux cas, vous pouvez écrire un wrapper pour votre codec existant qui implémente ces interfaces.</span><span class="sxs-lookup"><span data-stu-id="05390-109">In many cases, you can write a wrapper for your existing codec that implements these interfaces.</span></span> <span data-ttu-id="05390-110">Lorsque vous installez votre codec, vous devez créer des entrées de Registre pour que votre codec soit détectable par la plateforme WIC et l’associer aux gestionnaires de métadonnées appropriés.</span><span class="sxs-lookup"><span data-stu-id="05390-110">When you install your codec, you must make some registry entries to make your codec discoverable by the WIC platform and associate it with the appropriate metadata handlers.</span></span> <span data-ttu-id="05390-111">Vous devez également appeler une API pour effacer le cache de miniatures des miniatures par défaut (vides) qui peuvent avoir été précédemment associées à des images dans votre format.</span><span class="sxs-lookup"><span data-stu-id="05390-111">You also need to invoke an API to clear the thumbnail cache of any default (empty) thumbnails that may have previously associated with images in your format.</span></span> <span data-ttu-id="05390-112">Si vous le souhaitez, vous pouvez activer la Galerie de photos Windows Vista pour fournir aux utilisateurs un lien leur permettant de télécharger votre codec lorsque la Galerie de photos rencontre une image avec votre extension de nom de fichier.</span><span class="sxs-lookup"><span data-stu-id="05390-112">If you want, you can enable the Windows Vista Photo Gallery to provide users with a link to download your codec when the Photo Gallery encounters an image with your file name extension.</span></span> <span data-ttu-id="05390-113">Pour ce faire, vous devez fournir à Microsoft des informations sur l’extension de nom de fichier de votre codec et l’URL de votre site de téléchargement.</span><span class="sxs-lookup"><span data-stu-id="05390-113">To do this, you must provide Microsoft with information about your codec’s file name extension and the URL for your download site.</span></span>

## <a name="related-topics"></a><span data-ttu-id="05390-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="05390-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="05390-115">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="05390-115">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="05390-116">Installation et inscription du CODEC</span><span class="sxs-lookup"><span data-stu-id="05390-116">CODEC Installation and Registration</span></span>](-wic-codecinstallandreg.md)
</dt> <dt>

[<span data-ttu-id="05390-117">Comment écrire un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="05390-117">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="05390-118">Vue d’ensemble du composant Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="05390-118">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



