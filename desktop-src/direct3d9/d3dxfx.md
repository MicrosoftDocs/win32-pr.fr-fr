---
description: Options d’enregistrement et de création d’effets.
ms.assetid: df24a132-665e-4eb7-992b-d7a6144257f5
title: D3DXFX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad9077c8c7e3da479dd8963484bc289b84093ac0
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107995076"
---
# <a name="d3dxfx"></a><span data-ttu-id="a4aa2-103">D3DXFX</span><span class="sxs-lookup"><span data-stu-id="a4aa2-103">D3DXFX</span></span>

<span data-ttu-id="a4aa2-104">Options d’enregistrement et de création d’effets.</span><span class="sxs-lookup"><span data-stu-id="a4aa2-104">Options for saving and creating effects.</span></span>

<span data-ttu-id="a4aa2-105">Les constantes dans le tableau suivant sont définies dans d3dx9effect. h.</span><span class="sxs-lookup"><span data-stu-id="a4aa2-105">The constants in the following table are defined in d3dx9effect.h.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a4aa2-106">Indicateurs d’enregistrement et de restauration de l’état d’effet</span><span class="sxs-lookup"><span data-stu-id="a4aa2-106">Effect State Save and Restore Flags</span></span></td>
<td><span data-ttu-id="a4aa2-107">Description</span><span class="sxs-lookup"><span data-stu-id="a4aa2-107">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4aa2-108">D3DXFX_DONOTSAVESTATE</span><span class="sxs-lookup"><span data-stu-id="a4aa2-108">D3DXFX_DONOTSAVESTATE</span></span></td>
<td><span data-ttu-id="a4aa2-109">Aucun État n’est enregistré lors de l’appel de <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> ou de Restore lors de l’appel de <a href="id3dxeffect--end.md"><strong>end</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="a4aa2-109">No state is saved when calling <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> or restored when calling <a href="id3dxeffect--end.md"><strong>End</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4aa2-110">D3DXFX_DONOTSAVESAMPLERSTATE</span><span class="sxs-lookup"><span data-stu-id="a4aa2-110">D3DXFX_DONOTSAVESAMPLERSTATE</span></span></td>
<td><span data-ttu-id="a4aa2-111">Un stateblock enregistre l’état lors de l’appel de <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> et restaure l’état lors de l’appel de <a href="id3dxeffect--end.md"><strong>end</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="a4aa2-111">A stateblock saves state when calling <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> and restores state when calling <a href="id3dxeffect--end.md"><strong>End</strong></a>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4aa2-112">D3DXFX_DONOTSAVESHADERSTATE</span><span class="sxs-lookup"><span data-stu-id="a4aa2-112">D3DXFX_DONOTSAVESHADERSTATE</span></span></td>
<td><span data-ttu-id="a4aa2-113">Un stateblock enregistre l’État (à l’exception des nuanceurs et des constantes de nuanceur) lors de l’appel de <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> et restaure l’état lors de l’appel de <a href="id3dxeffect--end.md"><strong>end</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="a4aa2-113">A stateblock saves state (except shaders and shader constants) when calling <a href="id3dxeffect--begin.md"><strong>Begin</strong></a> and restores state when calling <a href="id3dxeffect--end.md"><strong>End</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4aa2-114">Indicateurs de création d’effet</span><span class="sxs-lookup"><span data-stu-id="a4aa2-114">Effect Creation Flags</span></span></td>
<td><span data-ttu-id="a4aa2-115">Description</span><span class="sxs-lookup"><span data-stu-id="a4aa2-115">Description</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a4aa2-116">D3DXFX_NOT_CLONEABLE</span><span class="sxs-lookup"><span data-stu-id="a4aa2-116">D3DXFX_NOT_CLONEABLE</span></span></td>
<td><span data-ttu-id="a4aa2-117">L’effet ne peut pas être cloné et ne contient pas de données binaires de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="a4aa2-117">The effect will be non-cloneable and will not contain any shader binary data.</span></span> <span data-ttu-id="a4aa2-118"><a href="id3dxbaseeffect--getpassdesc.md"><strong>GetPassDesc</strong></a> ne retourne pas les pointeurs de fonction de nuanceur.</span><span class="sxs-lookup"><span data-stu-id="a4aa2-118"><a href="id3dxbaseeffect--getpassdesc.md"><strong>GetPassDesc</strong></a> will not return shader function pointers.</span></span> <span data-ttu-id="a4aa2-119">La définition de cet indicateur réduit l’effet de l’utilisation de la mémoire d’environ 50%, car elle élimine la nécessité pour le système d’effet de conserver une copie des nuanceurs en mémoire.</span><span class="sxs-lookup"><span data-stu-id="a4aa2-119">Setting this flag reduces effect memory usage by about 50% because it eliminates the need for the effect system to keep a copy of the shaders in memory.</span></span> <span data-ttu-id="a4aa2-120">Cet indicateur est utilisé par <a href="d3dxcreateeffect.md"><strong>D3DXCreateEffect</strong></a>, <a href="d3dxcreateeffectfromfile.md"><strong>D3DXCreateEffectFromFile</strong></a>et <a href="d3dxcreateeffectfromresource.md"><strong>D3DXCreateEffectFromResource</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="a4aa2-120">This flag is used by <a href="d3dxcreateeffect.md"><strong>D3DXCreateEffect</strong></a>, <a href="d3dxcreateeffectfromfile.md"><strong>D3DXCreateEffectFromFile</strong></a>, and <a href="d3dxcreateeffectfromresource.md"><strong>D3DXCreateEffectFromResource</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a4aa2-121">D3DXFX_LARGEADDRESSAWARE</span><span class="sxs-lookup"><span data-stu-id="a4aa2-121">D3DXFX_LARGEADDRESSAWARE</span></span></td>
<td><span data-ttu-id="a4aa2-122">Active l’allocation d’une ressource Effect dans l’espace d’adressage uppder d’un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="a4aa2-122">Enables the allocation of an effect resource into the uppder address space of a machine.</span></span> <span data-ttu-id="a4aa2-123">Une limitation importante est que vous ne pouvez pas utiliser des chaînes et les gère de façon interchangeable.</span><span class="sxs-lookup"><span data-stu-id="a4aa2-123">One important limitation is that you cannot use strings and handles interchangeably.</span></span> <span data-ttu-id="a4aa2-124">Par exemple, le code suivant ne fonctionnera plus.</span><span class="sxs-lookup"><span data-stu-id="a4aa2-124">For example, the following would no longer work.</span></span> <span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>g_pEffect->SetMatrix( &quot;g_mWorldViewProjection&quot;, &mWorldViewProjection );</code></pre></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a4aa2-125">Au lieu de cela, une méthode telle que [<strong>GetParameterByName</strong>](id3dxbaseeffect--getparameterbyname.md) doit être utilisée pour stocker le handle du paramètre, qui est ensuite utilisé pour passer des variables à l’effet.</span><span class="sxs-lookup"><span data-stu-id="a4aa2-125">Instead, a method such as [<strong>GetParameterByName</strong>](id3dxbaseeffect--getparameterbyname.md) must be used to store the handle of the parameter, which is then used to pass variables to the effect.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="a4aa2-126">Les constantes dans le tableau suivant ne sont pas définies par défaut et doivent être définies par le développeur.</span><span class="sxs-lookup"><span data-stu-id="a4aa2-126">The constants in the following table are not defined by default and must be defined by the developer.</span></span>



| <span data-ttu-id="a4aa2-127">Définition du préprocesseur \# d’effet</span><span class="sxs-lookup"><span data-stu-id="a4aa2-127">Effect Preprocessor \#define's</span></span> | <span data-ttu-id="a4aa2-128">Description</span><span class="sxs-lookup"><span data-stu-id="a4aa2-128">Description</span></span>                                                                                                                                                                                                                          |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4aa2-129">\_Handle D3DXFX LARGEADDRESS \_</span><span class="sxs-lookup"><span data-stu-id="a4aa2-129">D3DXFX\_LARGEADDRESS\_HANDLE</span></span>   | <span data-ttu-id="a4aa2-130">Définissez cette valeur avant d’inclure d3dx9. h afin que votre application ne soit pas compilée quand vous tentez de passer des chaînes dans des paramètres D3DXHANDLE.</span><span class="sxs-lookup"><span data-stu-id="a4aa2-130">Define this value before including d3dx9.h so that your application fails to compile when attempting to pass strings into D3DXHANDLE parameters.</span></span> <span data-ttu-id="a4aa2-131">Cela permet de s’assurer que des informations valides sont passées au Runtime.</span><span class="sxs-lookup"><span data-stu-id="a4aa2-131">This will aid in making sure that valid information is being passed to the runtime.</span></span> |
| <span data-ttu-id="a4aa2-132">Indicateurs de l’éditeur de liens Effects</span><span class="sxs-lookup"><span data-stu-id="a4aa2-132">Effect Linker Flags</span></span>            | <span data-ttu-id="a4aa2-133">Description</span><span class="sxs-lookup"><span data-stu-id="a4aa2-133">Description</span></span>                                                                                                                                                                                                                          |
| <span data-ttu-id="a4aa2-134">prise en \_ charge d’adresses volumineuses \_</span><span class="sxs-lookup"><span data-stu-id="a4aa2-134">LARGE\_ADDRESS\_AWARE</span></span>          | <span data-ttu-id="a4aa2-135">La définition de l’indicateur de l’éditeur de liens pour la grande prise \_ \_ en charge de l’adresse = 1 permettra à l’application d’allouer des ressources au-delà de la limite de 2 Go si nécessaire.</span><span class="sxs-lookup"><span data-stu-id="a4aa2-135">Setting the linker flag LARGE\_ADDRESS\_AWARE = 1 will will allow the application to allocate resources past the 2GB address limit when needed.</span></span>                                                                                      |



 

<span data-ttu-id="a4aa2-136">Le système d’effet utilise des blocs d’État pour enregistrer et restaurer automatiquement l’État.</span><span class="sxs-lookup"><span data-stu-id="a4aa2-136">The effect system uses state blocks to save and restore state automatically.</span></span> <span data-ttu-id="a4aa2-137">Pour plus d’informations sur les blocs d’État, consultez State [Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md).</span><span class="sxs-lookup"><span data-stu-id="a4aa2-137">For more information about state blocks, see [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a4aa2-138">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a4aa2-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4aa2-139">Constantes d’effet</span><span class="sxs-lookup"><span data-stu-id="a4aa2-139">Effect Constants</span></span>](dx9-graphics-reference-effects-constants.md)
</dt> </dl>

 

 



