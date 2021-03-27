---
title: Liaison dynamique
description: Les développeurs de graphiques créent parfois des nuanceurs de grande taille et à usage général qui peuvent être utilisés par un large éventail d’éléments de scène.
ms.assetid: 2f5f7852-0f0a-4fad-a412-9a0d634c73b6
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: d5cd10bab8e2b4a28458cad1050847e0184ce43b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673441"
---
# <a name="dynamic-linking"></a><span data-ttu-id="077d4-103">Liaison dynamique</span><span class="sxs-lookup"><span data-stu-id="077d4-103">Dynamic Linking</span></span>

<span data-ttu-id="077d4-104">Les développeurs de graphiques créent parfois des nuanceurs de grande taille et à usage général qui peuvent être utilisés par un large éventail d’éléments de scène.</span><span class="sxs-lookup"><span data-stu-id="077d4-104">Graphics developers sometimes create large, general-purpose shaders that can be used by a wide variety of scene items.</span></span> <span data-ttu-id="077d4-105">Lors de l’exécution, le nuanceur exécute de manière conditionnelle le code approprié pour la situation donnée.</span><span class="sxs-lookup"><span data-stu-id="077d4-105">At runtime, the shader conditionally runs code appropriate for the given situation.</span></span> <span data-ttu-id="077d4-106">Malheureusement, ces gros nuanceurs à usage général utilisent des registres à usage général (GPRs) de manière inefficace et peuvent être beaucoup plus lents que les plus petits et les plus petits.</span><span class="sxs-lookup"><span data-stu-id="077d4-106">Unfortunately, these large, general-purpose shaders use general-purpose registers (GPRs) inefficiently, and can be much slower than smaller, more targeted shaders.</span></span>

<span data-ttu-id="077d4-107">Le Shader Model 5 résout ce problème de performances en introduisant une liaison de nuanceur dynamique.</span><span class="sxs-lookup"><span data-stu-id="077d4-107">Shader model 5 addresses this performance problem by introducing dynamic shader linking.</span></span> <span data-ttu-id="077d4-108">La liaison dynamique sépare les fragments de code du nuanceur en utilisant des interfaces et des fonctions virtuelles et permet à l’application de sélectionner le fragment à utiliser au moment du tracé.</span><span class="sxs-lookup"><span data-stu-id="077d4-108">Dynamic linking separates shader code fragments by using interfaces and virtual functions and allows the application to select the fragment to use at draw time.</span></span> <span data-ttu-id="077d4-109">Cela améliore les performances en liant uniquement le code du nuanceur nécessaire et non l’intégralité du nuanceur à usage général.</span><span class="sxs-lookup"><span data-stu-id="077d4-109">This improves performance by binding only the shader code needed and not the entire large, general-purpose shader.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="077d4-110">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="077d4-110">In This Section</span></span>



| <span data-ttu-id="077d4-111">Élément</span><span class="sxs-lookup"><span data-stu-id="077d4-111">Item</span></span>                                                                                                                                                                                                                                                                                                                         | <span data-ttu-id="077d4-112">Description</span><span class="sxs-lookup"><span data-stu-id="077d4-112">Description</span></span>                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="077d4-113"><span id="Storing_Variables_and_Types_for_Shaders_to_Share"></span><span id="storing_variables_and_types_for_shaders_to_share"></span><span id="STORING_VARIABLES_AND_TYPES_FOR_SHADERS_TO_SHARE"></span>[Stockage des variables et des types pour les nuanceurs à partager](storing-variables-and-types-for-shaders-to-share.md)</span><span class="sxs-lookup"><span data-stu-id="077d4-113"><span id="Storing_Variables_and_Types_for_Shaders_to_Share"></span><span id="storing_variables_and_types_for_shaders_to_share"></span><span id="STORING_VARIABLES_AND_TYPES_FOR_SHADERS_TO_SHARE"></span>[Storing Variables and Types for Shaders to Share](storing-variables-and-types-for-shaders-to-share.md)</span></span><br/> | <span data-ttu-id="077d4-114">Décrit l’objet de liaison de classe pour stocker des variables et des types que plusieurs nuanceurs peuvent partager.</span><span class="sxs-lookup"><span data-stu-id="077d4-114">Describes the class linkage object for storing variables and types that multiple shaders can share.</span></span><br/> |
| <span data-ttu-id="077d4-115"><span id="Interfaces_and_Classes"></span><span id="interfaces_and_classes"></span><span id="INTERFACES_AND_CLASSES"></span>[Interfaces et classes](overviews-direct3d-11-hlsl-dynamic-linking-class.md)</span><span class="sxs-lookup"><span data-stu-id="077d4-115"><span id="Interfaces_and_Classes"></span><span id="interfaces_and_classes"></span><span id="INTERFACES_AND_CLASSES"></span>[Interfaces and Classes](overviews-direct3d-11-hlsl-dynamic-linking-class.md)</span></span><br/>                                                                                                         | <span data-ttu-id="077d4-116">Décrit l’utilisation d’interfaces et de classes HLSL pour implémenter la liaison dynamique.</span><span class="sxs-lookup"><span data-stu-id="077d4-116">Describes using HLSL interfaces and classes to implement dynamic linking.</span></span><br/>                           |
| <span data-ttu-id="077d4-117"><span id="Interface_Usage_Restrictions"></span><span id="interface_usage_restrictions"></span><span id="INTERFACE_USAGE_RESTRICTIONS"></span>[Restrictions d’utilisation de l’interface](overviews-direct3d-11-hlsl-dynamic-linking-expression.md)</span><span class="sxs-lookup"><span data-stu-id="077d4-117"><span id="Interface_Usage_Restrictions"></span><span id="interface_usage_restrictions"></span><span id="INTERFACE_USAGE_RESTRICTIONS"></span>[Interface Usage Restrictions](overviews-direct3d-11-hlsl-dynamic-linking-expression.md)</span></span><br/>                                                                            | <span data-ttu-id="077d4-118">Décrit les restrictions sur l’utilisation des interfaces dans le code du nuanceur.</span><span class="sxs-lookup"><span data-stu-id="077d4-118">Describes restrictions on the use of interfaces in shader code.</span></span><br/>                                     |



 

## <a name="related-topics"></a><span data-ttu-id="077d4-119">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="077d4-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="077d4-120">HLSL</span><span class="sxs-lookup"><span data-stu-id="077d4-120">HLSL</span></span>](overviews-direct3d-11-hlsl.md)
</dt> </dl>

 

 





