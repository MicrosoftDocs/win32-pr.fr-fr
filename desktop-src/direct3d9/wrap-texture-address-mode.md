---
description: Le mode d’adresse de la texture encapsulé, identifié par le \_ membre D3DTADDRESS Wrap du type énuméré D3DTEXTUREADDRESS, fait en sorte que Direct3D répète la texture sur chaque jonction d’entier.
ms.assetid: fe33c484-346d-4888-ba88-b8ab00feefbb
title: Mode d’adressage de texture de retour à la ligne (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e721ace45599236022f32e6b0ec3723e346befbd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104200676"
---
# <a name="wrap-texture-address-mode-direct3d-9"></a><span data-ttu-id="877f5-103">Mode d’adressage de texture de retour à la ligne (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="877f5-103">Wrap Texture Address Mode (Direct3D 9)</span></span>

<span data-ttu-id="877f5-104">Le mode d’adresse de la texture encapsulé, identifié par le \_ membre D3DTADDRESS Wrap du type énuméré [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) , fait en sorte que Direct3D répète la texture sur chaque jonction d’entier.</span><span class="sxs-lookup"><span data-stu-id="877f5-104">The wrap texture address mode, identified by the D3DTADDRESS\_WRAP member of the [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) enumerated type, makes Direct3D repeat the texture on every integer junction.</span></span> <span data-ttu-id="877f5-105">Supposons, par exemple, que votre application crée une primitive carrée et spécifie des coordonnées de texture (0.0, 0.0), (0.0, 3.0), (3.0, 3.0) et (3,0, 0.0).</span><span class="sxs-lookup"><span data-stu-id="877f5-105">Suppose, for example, your application creates a square primitive and specifies texture coordinates of (0.0,0.0), (0.0,3.0), (3.0,3.0), and (3.0,0.0).</span></span> <span data-ttu-id="877f5-106">La définition du mode d’adressage de la texture sur D3DTADDRESS \_ encapsule les résultats dans la texture appliquée trois fois dans les directions u et v, comme indiqué dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="877f5-106">Setting the texture addressing mode to D3DTADDRESS\_WRAP results in the texture being applied three times in both the u-and v-directions, as shown in the following illustration.</span></span>

![illustration d’une texture faciale encapsulée dans la direction u et l’axe v](images/wrap.png)

<span data-ttu-id="877f5-108">Les effets de ce mode d’adresse de texture sont similaires à ceux du mode miroir, mais diffèrent de ceux-ci.</span><span class="sxs-lookup"><span data-stu-id="877f5-108">The effects of this texture address mode are similar to, but distinct from, those of the mirror mode.</span></span> <span data-ttu-id="877f5-109">Pour plus d’informations, consultez [mode d’adresse de texture miroir (Direct3D 9)](mirror-texture-address-mode.md).</span><span class="sxs-lookup"><span data-stu-id="877f5-109">For more information, see [Mirror Texture Address Mode (Direct3D 9)](mirror-texture-address-mode.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="877f5-110">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="877f5-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="877f5-111">Modes d’adressage de la texture</span><span class="sxs-lookup"><span data-stu-id="877f5-111">Texture Addressing Modes</span></span>](texture-addressing-modes.md)
</dt> </dl>

 

 
