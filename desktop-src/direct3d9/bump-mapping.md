---
description: Le placage de relief est une forme spéciale de mappage d’environnement spéculaire ou diffus qui simule les réflexions des objets fractionnés de manière fine sans nécessiter des nombres de polygones extrêmement élevés.
ms.assetid: 3e195e4f-3fa9-43c4-b2e5-42a6b3aaccf2
title: Placage de relief (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9dba4621568f595eae965941168ad6930e183f7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111274"
---
# <a name="bump-mapping-direct3d-9"></a><span data-ttu-id="cb686-103">Placage de relief (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="cb686-103">Bump Mapping (Direct3D 9)</span></span>

<span data-ttu-id="cb686-104">Le placage de relief est une forme spéciale de mappage d’environnement spéculaire ou diffus qui simule les réflexions des objets fractionnés de manière fine sans nécessiter des nombres de polygones extrêmement élevés.</span><span class="sxs-lookup"><span data-stu-id="cb686-104">Bump mapping is a special form of specular or diffuse environment mapping that simulates the reflections of finely tessellated objects without requiring extremely high polygon counts.</span></span> <span data-ttu-id="cb686-105">Le mappage de relief implémenté par Direct3D peut être décrit avec précision en cas de perturbation de la coordonnée de texture par pixel des cartes d’environnement spéculaires ou diffuses, car vous fournissez des informations sur le contour de la carte de relief en termes de valeurs Delta, que le système applique aux coordonnées de texture vous et v d’une carte d’environnement lors de la prochaine étape de texture.</span><span class="sxs-lookup"><span data-stu-id="cb686-105">Bump mapping implemented by Direct3D can be accurately described as per-pixel texture coordinate perturbation of specular or diffuse environment maps, because you provide information about the contour of the bump map in terms of delta values, which the system applies to the u and v texture coordinates of an environment map in the next texture stage.</span></span> <span data-ttu-id="cb686-106">Les valeurs Delta sont encodées au format de pixel de la surface de la carte de relief (voir formats de pixel de la [carte de relief](bump-map-pixel-formats.md)).</span><span class="sxs-lookup"><span data-stu-id="cb686-106">The delta values are encoded in the pixel format of the bump map surface (see [Bump Map Pixel Formats](bump-map-pixel-formats.md)).</span></span>

<span data-ttu-id="cb686-107">Le placage de relief repose sur la fusion de plusieurs textures.</span><span class="sxs-lookup"><span data-stu-id="cb686-107">Bump mapping relies on blending multiple textures.</span></span> <span data-ttu-id="cb686-108">Cela signifie que l’appareil doit prendre en charge au moins deux phases de fusion ; une pour la carte de relief et une autre pour une carte d’environnement.</span><span class="sxs-lookup"><span data-stu-id="cb686-108">This means the device must support at least two blending stages; one for the bump map and another for an environment map.</span></span> <span data-ttu-id="cb686-109">Au moins trois étapes de fusion de texture sont requises pour appliquer une carte de texture de base supplémentaire, ce qui est le cas le plus courant.</span><span class="sxs-lookup"><span data-stu-id="cb686-109">A minimum of three texture blending stages are required to apply an additional base texture map, which is the most common case.</span></span> <span data-ttu-id="cb686-110">Le diagramme suivant montre les relations entre la texture de base, la carte de relief et la carte d’environnement dans la texture de fusion en cascade.</span><span class="sxs-lookup"><span data-stu-id="cb686-110">The following diagram shows the relationships between the base texture, the bump map, and the environment map in the texture blending cascade.</span></span>

![diagramme de la fusion en cascade de la texture](images/bumpmap-tcascade.png)

<span data-ttu-id="cb686-112">Vous devez préparer les étapes de texture de manière appropriée pour activer le mappage de relief.</span><span class="sxs-lookup"><span data-stu-id="cb686-112">You must prepare the texture stages appropriately to enable bump mapping.</span></span> <span data-ttu-id="cb686-113">Les rubriques suivantes présentent un placage de relief et fournissent des détails sur la façon dont vous pouvez l’utiliser dans vos applications :</span><span class="sxs-lookup"><span data-stu-id="cb686-113">The following topics introduce bump mapping, and provide details about how you can use it in your applications:</span></span>

-   [<span data-ttu-id="cb686-114">Formats de pixel de la carte de relief</span><span class="sxs-lookup"><span data-stu-id="cb686-114">Bump Map Pixel Formats</span></span>](bump-map-pixel-formats.md)
-   [<span data-ttu-id="cb686-115">Formules de mappage de relief</span><span class="sxs-lookup"><span data-stu-id="cb686-115">Bump Mapping Formulas</span></span>](bump-mapping-formulas.md)
-   [<span data-ttu-id="cb686-116">Utilisation du mappage de relief</span><span class="sxs-lookup"><span data-stu-id="cb686-116">Using Bump Mapping</span></span>](using-bump-mapping.md)

<span data-ttu-id="cb686-117">Direct3D ne prend pas en charge en mode natif les mappages de hauteur ; Il s’agit simplement d’un format pratique dans lequel stocker et visualiser les données de contour.</span><span class="sxs-lookup"><span data-stu-id="cb686-117">Direct3D does not natively support height maps; they are merely a convenient format in which to store and visualize contour data.</span></span> <span data-ttu-id="cb686-118">Votre application peut stocker des informations de contour dans n’importe quel format, voire générer une carte de relief des procédures.</span><span class="sxs-lookup"><span data-stu-id="cb686-118">Your application can store contour information in any format, or even generate a procedural bump map.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cb686-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="cb686-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cb686-120">Pipeline de pixels</span><span class="sxs-lookup"><span data-stu-id="cb686-120">Pixel Pipeline</span></span>](pixel-pipeline.md)
</dt> </dl>

 

 



