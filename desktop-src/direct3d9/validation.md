---
description: La validation est effectuée lors de la compilation de l’effet. Pour valider la technique actuelle, spécifiez NULL comme handle de technique à valider.
ms.assetid: d1268f68-2893-4d7f-acd2-484346a20193
title: Validation (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ecc64a17aba21af4b43bd41cc060a8711e5bb4e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515897"
---
# <a name="validation-direct3d-9"></a><span data-ttu-id="6f786-104">Validation (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="6f786-104">Validation (Direct3D 9)</span></span>

<span data-ttu-id="6f786-105">La validation est effectuée lors de la compilation de l’effet.</span><span class="sxs-lookup"><span data-stu-id="6f786-105">Validation is performed during the effect compile.</span></span> <span data-ttu-id="6f786-106">Pour valider la technique actuelle, spécifiez **null** comme handle de technique à valider.</span><span class="sxs-lookup"><span data-stu-id="6f786-106">To validate the current technique, specify **NULL** as the technique handle to be validated.</span></span>

<span data-ttu-id="6f786-107">La validation échoue pour l’un des éléments suivants :</span><span class="sxs-lookup"><span data-stu-id="6f786-107">Validation will fail for any of the following:</span></span>

-   <span data-ttu-id="6f786-108">Si le handle de technique spécifié n’existe pas.</span><span class="sxs-lookup"><span data-stu-id="6f786-108">If the specified technique handle does not exist.</span></span>
-   <span data-ttu-id="6f786-109">Si l’application d’un État quelconque dans le cas d’un passage de la technique échoue.</span><span class="sxs-lookup"><span data-stu-id="6f786-109">If the application of any state in any pass of the technique fails.</span></span>
-   <span data-ttu-id="6f786-110">Si la validation de l’appareil échoue après l’application de tous les États dans le cas d’un passage de la technique.</span><span class="sxs-lookup"><span data-stu-id="6f786-110">If device validation fails after the application of all the states in any pass of the technique.</span></span>
-   <span data-ttu-id="6f786-111">Si des nuanceurs non valides sont affectés aux États d’effet PIXELSHADER ou VERTEXSHADER dans n’importe quel passage de la technique.</span><span class="sxs-lookup"><span data-stu-id="6f786-111">If the PIXELSHADER or VERTEXSHADER effect states are assigned invalid shaders in any pass of the technique.</span></span>
-   <span data-ttu-id="6f786-112">Si les extrémités de l’appareil ne prennent pas en charge le mappage de cube et qu’une valeur de type textureCUBE est assignée à un état d’effet de TEXTURE, dans n’importe quelle étape de la technique.</span><span class="sxs-lookup"><span data-stu-id="6f786-112">If the device caps do not support cube mapping, and a TEXTURE effect state is assigned a value of type textureCUBE in any pass of the technique.</span></span>
-   <span data-ttu-id="6f786-113">Si les extrémités de l’appareil ne prennent pas en charge le mappage de volume et qu’une valeur de type texture3D est assignée à un état d’effet de TEXTURE, dans n’importe quelle étape de la technique.</span><span class="sxs-lookup"><span data-stu-id="6f786-113">If the device caps do not support volume mapping and a TEXTURE effect state is assigned a value of type texture3D in any pass of the technique.</span></span>

<span data-ttu-id="6f786-114">Pour plus d’informations, consultez [États d’effet (Direct3D 9)](effect-states.md).</span><span class="sxs-lookup"><span data-stu-id="6f786-114">For more information, see [Effect States (Direct3D 9)](effect-states.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6f786-115">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="6f786-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f786-116">Format d’effet</span><span class="sxs-lookup"><span data-stu-id="6f786-116">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 



