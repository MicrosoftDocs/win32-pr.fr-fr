---
description: La mise en mémoire tampon de profondeur est une méthode de suppression des lignes et des surfaces masquées. Par défaut, Direct3D n’utilise pas la mise en mémoire tampon de profondeur.
ms.assetid: 03795e4e-1daa-48e3-8724-8dd4b5187edc
title: État de la mise en mémoire tampon de profondeur (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e632d3dfe6eebd54970c59ef6a666cfcb0950fcb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104481553"
---
# <a name="depth-buffering-state-direct3d-9"></a><span data-ttu-id="99ce7-104">État de la mise en mémoire tampon de profondeur (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="99ce7-104">Depth Buffering State (Direct3D 9)</span></span>

<span data-ttu-id="99ce7-105">La mise en mémoire tampon de profondeur est une méthode de suppression des lignes et des surfaces masquées.</span><span class="sxs-lookup"><span data-stu-id="99ce7-105">Depth buffering is a method of removing hidden lines and surfaces.</span></span> <span data-ttu-id="99ce7-106">Par défaut, Direct3D n’utilise pas la mise en mémoire tampon de profondeur.</span><span class="sxs-lookup"><span data-stu-id="99ce7-106">By default, Direct3D does not use depth buffering.</span></span>

<span data-ttu-id="99ce7-107">Pour obtenir une vue d’ensemble conceptuelle des mémoires tampons de profondeur, consultez [mémoires tampons de profondeur (Direct3D 9)](depth-buffers.md).</span><span class="sxs-lookup"><span data-stu-id="99ce7-107">For a conceptual overview of depth buffers, see [Depth Buffers (Direct3D 9)](depth-buffers.md).</span></span>

<span data-ttu-id="99ce7-108">Les applications C++ mettent à jour l’état de mise en mémoire tampon de profondeur avec l' \_ État de rendu D3DRS ZENABLE, à l’aide d’un membre de l’énumération [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) pour spécifier la nouvelle valeur d’État.</span><span class="sxs-lookup"><span data-stu-id="99ce7-108">C++ applications update the depth-buffering state with the D3DRS\_ZENABLE render state, using a member of the [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) enumeration to specify the new state value.</span></span>

<span data-ttu-id="99ce7-109">Si votre application doit empêcher Direct3D d’écrire dans le tampon de profondeur, elle peut utiliser la \_ valeur énumérée D3DRS ZWRITEENABLE, en spécifiant D3DZB \_ false comme deuxième paramètre pour l’appel à [**IDirect3DDevice9 :: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate).</span><span class="sxs-lookup"><span data-stu-id="99ce7-109">If your application needs to prevent Direct3D from writing to the depth buffer, it can use the D3DRS\_ZWRITEENABLE enumerated value, specifying D3DZB\_FALSE as the second parameter for the call to [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate).</span></span>

<span data-ttu-id="99ce7-110">L’exemple de code suivant montre comment l’état de la mémoire tampon de profondeur est défini pour activer la mise en mémoire tampon z.</span><span class="sxs-lookup"><span data-stu-id="99ce7-110">The following code example shows how the depth-buffer state is set to enable z-buffering.</span></span>


```
// This code example assumes that d3dDevice is a 
// valid pointer to an IDirect3DDevice9 interface.
// Enable z-buffering.
d3dDevice->SetRenderState(D3DRS_ZENABLE, D3DZB_TRUE);
```



<span data-ttu-id="99ce7-111">Votre application peut également utiliser l' \_ État de rendu D3DRS ZFUNC pour contrôler la fonction de comparaison utilisée par Direct3D lors de l’exécution de la mise en mémoire tampon de profondeur.</span><span class="sxs-lookup"><span data-stu-id="99ce7-111">Your application can also use the D3DRS\_ZFUNC render state to control the comparison function that Direct3D uses when performing depth buffering.</span></span>

<span data-ttu-id="99ce7-112">L’inclinaison Z est une méthode qui consiste à afficher une surface devant l’autre, même si leurs valeurs de profondeur sont identiques.</span><span class="sxs-lookup"><span data-stu-id="99ce7-112">Z-biasing is a method of displaying one surface in front of another, even if their depth values are the same.</span></span> <span data-ttu-id="99ce7-113">Vous pouvez utiliser cette technique pour un grand nombre d’effets.</span><span class="sxs-lookup"><span data-stu-id="99ce7-113">You can use this technique for a variety of effects.</span></span> <span data-ttu-id="99ce7-114">Un exemple courant est le rendu des ombres sur les murs.</span><span class="sxs-lookup"><span data-stu-id="99ce7-114">A common example is rendering shadows on walls.</span></span> <span data-ttu-id="99ce7-115">L’ombre et le mur ont la même valeur de profondeur.</span><span class="sxs-lookup"><span data-stu-id="99ce7-115">Both the shadow and the wall have the same depth value.</span></span> <span data-ttu-id="99ce7-116">Toutefois, vous souhaitez que votre application affiche l’ombre sur le mur.</span><span class="sxs-lookup"><span data-stu-id="99ce7-116">However, you want your application to show the shadow on the wall.</span></span> <span data-ttu-id="99ce7-117">En donnant une polarisation z à l’ombre, Direct3D les affiche correctement (consultez D3DRS \_ DEPTHBIAS).</span><span class="sxs-lookup"><span data-stu-id="99ce7-117">Giving a z-bias to the shadow makes Direct3D display them properly (see D3DRS\_DEPTHBIAS).</span></span>

## <a name="related-topics"></a><span data-ttu-id="99ce7-118">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="99ce7-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="99ce7-119">États de rendu</span><span class="sxs-lookup"><span data-stu-id="99ce7-119">Render States</span></span>](render-states.md)
</dt> </dl>

 

 
