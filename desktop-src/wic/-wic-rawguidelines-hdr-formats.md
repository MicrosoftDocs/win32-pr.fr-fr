---
description: Formats de pixel à plage dynamique élevée
ms.assetid: 037b6bde-a3e0-401d-9be7-b58c5f74c30a
title: Formats de pixel à plage dynamique élevée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8405a01fa5397dd5681077ac1ac9acc28e7d1003
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867322"
---
# <a name="high-dynamic-range-pixel-formats"></a><span data-ttu-id="db420-103">Formats de pixel à plage dynamique élevée</span><span class="sxs-lookup"><span data-stu-id="db420-103">High Dynamic Range Pixel Formats</span></span>

<span data-ttu-id="db420-104">Les codecs doivent utiliser des formats de pixel WIC (Windows Imaging Component) qui conservent l’ensemble de la plage dynamique des données de capteur sous-jacentes.</span><span class="sxs-lookup"><span data-stu-id="db420-104">Codecs should use Windows Imaging Component (WIC) pixel formats that preserve all of the dynamic range of the underlying sensor data.</span></span> <span data-ttu-id="db420-105">GUID \_ WICPixelFormat48bppRGB est un format de 16 bits à virgule fixe standard qui peut être utilisé.</span><span class="sxs-lookup"><span data-stu-id="db420-105">GUID\_WICPixelFormat48bppRGB is a typical fixed-point 16-bit-per-channel format that can be used.</span></span> <span data-ttu-id="db420-106">D’autres formats de précision plus élevée peuvent également être utilisés.</span><span class="sxs-lookup"><span data-stu-id="db420-106">Other higher precision formats can be used also.</span></span> <span data-ttu-id="db420-107">Pour activer la prise en charge complète du pipeline de rendu accéléré par l’unité de traitement graphique (GPU) Windows Presentation Foundation, Microsoft encourage fortement la prise en charge d’un format de pixel à virgule flottante 32 bits.</span><span class="sxs-lookup"><span data-stu-id="db420-107">To enable full support for the Windows Presentation Foundation graphics processing unit (GPU)-accelerated rendering pipeline, Microsoft strongly encourages support for a 32-bit floating point pixel format.</span></span>

<span data-ttu-id="db420-108">Formats de pixel de couleur élevée : avec Windows 7, deux nouveaux formats de pixel WIC ont été ajoutés pour prendre en charge les nouveaux formats d’affichage 65536 couleurs.</span><span class="sxs-lookup"><span data-stu-id="db420-108">High Color Pixel Formats: With Windows 7, two new WIC pixel formats have been added to support the new High Color display formats.</span></span> <span data-ttu-id="db420-109">Il s’agit des éléments suivants : GUID \_ WICPixelFormat32bppRGBA1010102 et GUID \_ WICPixelFormat32bppRGBA1010102XR.</span><span class="sxs-lookup"><span data-stu-id="db420-109">These are: GUID\_WICPixelFormat32bppRGBA1010102 and GUID\_WICPixelFormat32bppRGBA1010102XR.</span></span>

<span data-ttu-id="db420-110">Le format haute couleur flottant (BPC) de 16 bits par canal est pris en charge par le \_ format de pixel WICPIXELFORMAT64BPPRGBAHALF GUID existant.</span><span class="sxs-lookup"><span data-stu-id="db420-110">The 16 bit per channel (bpc) float High Color format is supported by the existing GUID\_WICPixelFormat64bppRGBAHalf pixel format.</span></span>

## <a name="related-topics"></a><span data-ttu-id="db420-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="db420-111">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="db420-112">**Méthodologique**</span><span class="sxs-lookup"><span data-stu-id="db420-112">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="db420-113">Vue d’ensemble du composant Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="db420-113">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="db420-114">Recommandations de WIC pour les formats d’image RAW Camera</span><span class="sxs-lookup"><span data-stu-id="db420-114">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="db420-115">Comment écrire un CODEC WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="db420-115">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



