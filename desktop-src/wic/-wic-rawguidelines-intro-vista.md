---
description: Formats d’images BRUTes dans Windows Vista
ms.assetid: e28b642c-03c8-4ecc-b5f5-e3911b8003a7
title: Formats d’images BRUTes dans Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c48b4e3ab5b0d373dbc0313267e58177b189538
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104204211"
---
# <a name="raw-image-formats-in-windows-vista"></a><span data-ttu-id="8e3d1-103">Formats d’images BRUTes dans Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8e3d1-103">RAW Image Formats in Windows Vista</span></span>

<span data-ttu-id="8e3d1-104">L’Explorateur Windows Vista, la Galerie de photos Windows Vista, la Galerie de photos Windows Live et la visionneuse de photos Windows 7 utilisent tous Windows Imaging Component (WIC) et, par conséquent, prennent en charge les formats d’images BRUTes quand les codecs appropriés sont installés sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="8e3d1-104">Windows Vista Explorer , Windows Vista Photo Gallery, Window Live Photo Gallery, and the Windows 7 Photo Viewer all use Windows Imaging Component (WIC) and therefore support RAW image formats when appropriate codecs are installed on the computer.</span></span>

<span data-ttu-id="8e3d1-105">Étant donné que WIC est une architecture d’imagerie extensible, toute application WIC peut consommer de nouveaux formats d’image dès que de nouveaux codecs sont installés sur le système.</span><span class="sxs-lookup"><span data-stu-id="8e3d1-105">Because WIC is an extensible imaging architecture, any WIC application can consume new image formats as soon as new codecs are installed on the system.</span></span> <span data-ttu-id="8e3d1-106">Le WIC est donc idéal comme solution de Plug-and-Play pour les formats d’images BRUTs produits par les appareils photo numériques.</span><span class="sxs-lookup"><span data-stu-id="8e3d1-106">This makes WIC ideal as a Plug and Play solution for the RAW image formats that digital cameras produce.</span></span> <span data-ttu-id="8e3d1-107">Grâce au WIC, les applications Windows peuvent prendre en charge de nouveaux modèles d’appareil photo chaque fois que des codecs mis à jour sont disponibles (dans l’idéal, avec de nouvelles caméras).</span><span class="sxs-lookup"><span data-stu-id="8e3d1-107">Through WIC, Windows applications can gain support for new camera models whenever updated codecs are made available (ideally in-box with new cameras).</span></span> <span data-ttu-id="8e3d1-108">Les auteurs de codec peuvent prendre en charge ces scénarios en implémentant des interfaces WIC communes à tous les types d’images, comme décrit plus en détail dans ce document.</span><span class="sxs-lookup"><span data-stu-id="8e3d1-108">Codec authors can support these scenarios by implementing WIC interfaces that are common to all image types, as described in more detail in this document.</span></span>

<span data-ttu-id="8e3d1-109">Aujourd’hui, la plupart des applications grand public n’ont aucune connaissance particulière des formats d’images BRUTes et n’exposent pas d’interface utilisateur pour ajuster les paramètres de traitement brut.</span><span class="sxs-lookup"><span data-stu-id="8e3d1-109">Today, most mainstream consumer applications have no special knowledge of RAW image formats and do not expose a user interface for adjusting RAW processing settings.</span></span>

<span data-ttu-id="8e3d1-110">Toutefois, pour prendre en charge des applications d’imagerie spécialisées, les auteurs de codec brut doivent également implémenter l’interface [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) .</span><span class="sxs-lookup"><span data-stu-id="8e3d1-110">However, to support specialized imaging applications, RAW codec authors must also implement the [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) interface.</span></span> <span data-ttu-id="8e3d1-111">Cette interface expose des fonctionnalités spéciales pour les images BRUTes, telles que la possibilité d’effectuer des réglages d’image courants et de traiter (développer) des images BRUTes dans des espaces de couleur rouge-vert-bleu (RVB) spécifiés.</span><span class="sxs-lookup"><span data-stu-id="8e3d1-111">This interface exposes special features for RAW images, such as the ability to make common image adjustments and to process (develop) RAW images into specified red-green-blue (RGB) color spaces.</span></span>

<span data-ttu-id="8e3d1-112">Plusieurs autres interfaces WIC sont importantes pour les auteurs de codec brut à implémenter.</span><span class="sxs-lookup"><span data-stu-id="8e3d1-112">Several other WIC interfaces are important for RAW codec authors to implement.</span></span> <span data-ttu-id="8e3d1-113">Celles-ci sont décrites plus en détail dans cette série de rubriques.</span><span class="sxs-lookup"><span data-stu-id="8e3d1-113">These are discussed in more detail in this series of topics.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8e3d1-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8e3d1-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="8e3d1-115">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="8e3d1-115">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8e3d1-116">Vue d’ensemble du composant Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="8e3d1-116">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="8e3d1-117">Recommandations de WIC pour les formats d’image RAW Camera</span><span class="sxs-lookup"><span data-stu-id="8e3d1-117">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="8e3d1-118">Comment écrire un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="8e3d1-118">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



