---
description: L’attribut stretchmode spécifie comment étirer une image qui ne correspond pas aux dimensions de sortie.
ms.assetid: 9a26bb8b-2b1c-424a-ae30-e175c60c76a1
title: Attribut stretchmode
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48a629a34dc1875a7f1d3669e32c53d0e8d3d29c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867085"
---
# <a name="stretchmode-attribute"></a><span data-ttu-id="e5de6-103">Attribut stretchmode</span><span class="sxs-lookup"><span data-stu-id="e5de6-103">stretchmode Attribute</span></span>

> [!Note]  
> <span data-ttu-id="e5de6-104">\[Action déconseillée.</span><span class="sxs-lookup"><span data-stu-id="e5de6-104">\[Deprecated.</span></span> <span data-ttu-id="e5de6-105">Cette API peut être supprimée dans les versions futures de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e5de6-105">This API may be removed from future releases of Windows.\]</span></span>

 

<span data-ttu-id="e5de6-106">L' `stretchmode` attribut spécifie comment étirer une image qui ne correspond pas aux dimensions de sortie.</span><span class="sxs-lookup"><span data-stu-id="e5de6-106">The `stretchmode` attribute specifies how to stretch an image that does not match the output dimensions.</span></span>

## <a name="possible-values"></a><span data-ttu-id="e5de6-107">Valeurs possibles</span><span class="sxs-lookup"><span data-stu-id="e5de6-107">Possible Values</span></span>

<span data-ttu-id="e5de6-108">Doit avoir l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="e5de6-108">Must have one of the following values.</span></span>

-   <span data-ttu-id="e5de6-109">« Stretch » : l’image est étirée pour s’ajuster à la taille de l’image de sortie sans conserver les proportions.</span><span class="sxs-lookup"><span data-stu-id="e5de6-109">"stretch": The image is stretched to fit the output frame size without preserving aspect ratio.</span></span> <span data-ttu-id="e5de6-110">(Par défaut)</span><span class="sxs-lookup"><span data-stu-id="e5de6-110">(Default)</span></span>
-   <span data-ttu-id="e5de6-111">« Crop » : l’image est rognée pour s’ajuster à la taille de trame de sortie.</span><span class="sxs-lookup"><span data-stu-id="e5de6-111">"crop": The image is cropped to fit the output frame size.</span></span>
-   <span data-ttu-id="e5de6-112">« preserveaspectratio » : les proportions d’origine sont conservées, avec une bandes noire le long de la dimension plus petite.</span><span class="sxs-lookup"><span data-stu-id="e5de6-112">"preserveaspectratio": The original aspect ratio is preserved, with a black letterbox along the shorter dimension.</span></span>
-   <span data-ttu-id="e5de6-113">« preserveaspectrationoletterbox » : l’image est redimensionnée pour remplir l’intégralité du frame cible tout en préservant les proportions.</span><span class="sxs-lookup"><span data-stu-id="e5de6-113">"preserveaspectrationoletterbox": The image is resized to fill the entire target frame while preserving the aspect ratio.</span></span>

## <a name="applies-to"></a><span data-ttu-id="e5de6-114">S'applique à</span><span class="sxs-lookup"><span data-stu-id="e5de6-114">Applies To</span></span>

[<span data-ttu-id="e5de6-115">**clip**</span><span class="sxs-lookup"><span data-stu-id="e5de6-115">**clip**</span></span>](clip-element.md)

## <a name="see-also"></a><span data-ttu-id="e5de6-116">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e5de6-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5de6-117">Attributs XTL</span><span class="sxs-lookup"><span data-stu-id="e5de6-117">XTL Attributes</span></span>](xtl-attributes.md)
</dt> <dt>

[<span data-ttu-id="e5de6-118">**IAMTimelineSrc::SetStretchMode**</span><span class="sxs-lookup"><span data-stu-id="e5de6-118">**IAMTimelineSrc::SetStretchMode**</span></span>](iamtimelinesrc-setstretchmode.md)
</dt> </dl>

 

 



