---
title: Énumération de format de sortie
description: Énumération de format de sortie
ms.assetid: 53d5724b-f875-4b2e-92fa-279f46111f29
keywords:
- Windows Media Format SDK, énumérations de format de sortie
- ASF (Advanced Systems Format), énumérations de format de sortie
- ASF (format de systèmes avancés), énumérations de format de sortie
- Windows Media Format SDK, interface IWMReaderTypeNegotiation
- ASF (Advanced Systems Format), interface IWMReaderTypeNegotiation
- ASF (format des systèmes avancés), interface IWMReaderTypeNegotiation
- énumérations de format de sortie
- IWMReaderTypeNegotiation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d49999c3da2afd05b0d2231d259d24a50356eb4f
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/19/2020
ms.locfileid: "104030758"
---
# <a name="output-format-enumeration"></a><span data-ttu-id="80139-111">Énumération de format de sortie</span><span class="sxs-lookup"><span data-stu-id="80139-111">Output Format Enumeration</span></span>

<span data-ttu-id="80139-112">L’objet lecteur et l’objet lecteur synchrone communiquent avec les codecs pour énumérer les formats de sortie possibles pour les flux compressés.</span><span class="sxs-lookup"><span data-stu-id="80139-112">Both the reader object and the synchronous reader object communicate with the codecs to enumerate the possible output formats for compressed streams.</span></span> <span data-ttu-id="80139-113">Quand vous lisez un fichier contenant du contenu compressé avec un ou plusieurs codecs Windows Media, vous pouvez examiner les formats de sortie possibles pour choisir celui qui convient le mieux à vos besoins.</span><span class="sxs-lookup"><span data-stu-id="80139-113">When you read a file containing content compressed with one or more of the Windows Media codecs, you can examine the possible output formats to choose the one that best suits your needs.</span></span> <span data-ttu-id="80139-114">Pour plus de commodité, chaque codec a un format de sortie par défaut qui est défini sur le format le plus couramment utilisé.</span><span class="sxs-lookup"><span data-stu-id="80139-114">For convenience, each codec has a default output format which is set to the most commonly used format.</span></span> <span data-ttu-id="80139-115">Pour plus d’informations sur l’énumération de sortie, consultez [utilisation des sorties](working-with-outputs.md).</span><span class="sxs-lookup"><span data-stu-id="80139-115">For more information about output enumeration, see [Working with Outputs](working-with-outputs.md).</span></span>

<span data-ttu-id="80139-116">Vous pouvez apporter certaines modifications à un format de sortie en fonction du type de média.</span><span class="sxs-lookup"><span data-stu-id="80139-116">You can make certain changes to an output format depending upon the media type.</span></span> <span data-ttu-id="80139-117">Pour les flux vidéo, par exemple, vous pouvez modifier la taille de l’image et la profondeur de couleur.</span><span class="sxs-lookup"><span data-stu-id="80139-117">For video streams, for example, you can change the frame size and color depth.</span></span> <span data-ttu-id="80139-118">Les objets de lecture prennent tous deux en charge une interface pour tester les modifications que vous apportez au format de sortie, appelé [**IWMReaderTypeNegotiation**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertypenegotiation).</span><span class="sxs-lookup"><span data-stu-id="80139-118">The reading objects both support an interface to test changes you make to the output format, called [**IWMReaderTypeNegotiation**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreadertypenegotiation).</span></span>

## <a name="related-topics"></a><span data-ttu-id="80139-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="80139-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="80139-120">**Fonctionnalités de lecture de fichier**</span><span class="sxs-lookup"><span data-stu-id="80139-120">**File Reading Features**</span></span>](file-reading-features.md)
</dt> </dl>

 

 




