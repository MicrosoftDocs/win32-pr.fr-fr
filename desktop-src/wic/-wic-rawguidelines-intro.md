---
description: Introduction (recommandations de WIC pour les formats d’image RAW Camera)
ms.assetid: 3c588386-1d4d-4ee0-b633-bfc94ca751ea
title: Introduction (recommandations de WIC pour les formats d’image RAW Camera)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec6ee2607326afe289e0a3e54b254dcf581cbf86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204210"
---
# <a name="introduction-wic-guidelines-for-camera-raw-image-formats"></a><span data-ttu-id="fc7bb-103">Introduction (recommandations de WIC pour les formats d’image RAW Camera)</span><span class="sxs-lookup"><span data-stu-id="fc7bb-103">Introduction (WIC Guidelines for Camera RAW Image Formats)</span></span>

<span data-ttu-id="fc7bb-104">Le composant WIC (Windows Imaging Component) fournit une infrastructure extensible pour l’utilisation des images et des métadonnées d’image.</span><span class="sxs-lookup"><span data-stu-id="fc7bb-104">The Windows Imaging Component (WIC) provides an extensible framework for working with images and image metadata.</span></span> <span data-ttu-id="fc7bb-105">Le WIC permet aux fournisseurs de logiciels et de matériel de développer des codecs afin que leurs propres formats d’image puissent obtenir la même prise en charge de plate-forme que les formats d’images natifs tels que TIFF (Tagged Image File Format), JPEG (Joint Photographic Experts Group) ou photo HD.</span><span class="sxs-lookup"><span data-stu-id="fc7bb-105">WIC makes it possible for software and hardware vendors to develop codecs so that their own image formats can obtain the same platform support as native image formats such as tagged image file format (TIFF), Joint Photographic Experts Group (JPEG), or HD Photo.</span></span>

<span data-ttu-id="fc7bb-106">WIC fournit un ensemble unique et cohérent d’interfaces pour le traitement de tous les images, quel que soit le format d’image.</span><span class="sxs-lookup"><span data-stu-id="fc7bb-106">WIC provides a single, consistent set of interfaces for all image processing, regardless of image format.</span></span> <span data-ttu-id="fc7bb-107">Par conséquent, toute application qui utilise WIC reçoit la prise en charge automatique des nouveaux formats d’image dès l’installation du codec.</span><span class="sxs-lookup"><span data-stu-id="fc7bb-107">Therefore, any application that uses WIC receives automatic support for new image formats as soon as the codec is installed.</span></span> <span data-ttu-id="fc7bb-108">WIC fournit également une infrastructure de métadonnées extensible qui permet aux applications de lire et d’écrire leurs propres métadonnées propriétaires directement dans des fichiers image, de sorte que les métadonnées ne sont jamais perdues ou séparées de l’image.</span><span class="sxs-lookup"><span data-stu-id="fc7bb-108">WIC also provides an extensible metadata framework that makes it possible for applications to read and write their own proprietary metadata directly to image files, so the metadata is never lost or separated from the image.</span></span>

<span data-ttu-id="fc7bb-109">WIC est inclus avec Windows Presentation Foundation (WPF) et est intégré à Windows Vista et versions ultérieures de Windows.</span><span class="sxs-lookup"><span data-stu-id="fc7bb-109">WIC is included with Windows Presentation Foundation (WPF) and is built into Windows Vista and later Windows versions.</span></span> <span data-ttu-id="fc7bb-110">Il est également disponible en tant que composant redistribuable autonome pour Windows XP.</span><span class="sxs-lookup"><span data-stu-id="fc7bb-110">It is also available as a stand-alone redistributable component for Windows XP.</span></span>

<span data-ttu-id="fc7bb-111">Ces instructions sont conçues pour aider les fabricants de format RAW dans le développement de codecs WIC.</span><span class="sxs-lookup"><span data-stu-id="fc7bb-111">These guidelines are designed to help RAW format manufacturers in their development of WIC codecs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fc7bb-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="fc7bb-112">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="fc7bb-113">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="fc7bb-113">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="fc7bb-114">Vue d’ensemble du composant Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="fc7bb-114">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="fc7bb-115">Recommandations de WIC pour les formats d’image RAW Camera</span><span class="sxs-lookup"><span data-stu-id="fc7bb-115">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="fc7bb-116">Comment écrire un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="fc7bb-116">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



