---
description: Le mode d’adresse de texture miroir, identifié par le \_ membre miroir D3DTADDRESS du type énuméré D3DTEXTUREADDRESS, amène Direct3D à refléter la texture à chaque limite d’entier.
ms.assetid: 816efd4d-94b3-4b6c-9fc9-218cc2207b97
title: Mode d’adresse de texture miroir (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 471ad8b715d9375947162c66474687b9d6376bec
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104392536"
---
# <a name="mirror-texture-address-mode-direct3d-9"></a><span data-ttu-id="24783-103">Mode d’adresse de texture miroir (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="24783-103">Mirror Texture Address Mode (Direct3D 9)</span></span>

<span data-ttu-id="24783-104">Le mode d’adresse de texture miroir, identifié par le \_ membre miroir D3DTADDRESS du type énuméré [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) , amène Direct3D à refléter la texture à chaque limite d’entier.</span><span class="sxs-lookup"><span data-stu-id="24783-104">The mirror texture address mode, identified by the D3DTADDRESS\_MIRROR member of the [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) enumerated type, causes Direct3D to mirror the texture at every integer boundary.</span></span> <span data-ttu-id="24783-105">Supposons, par exemple, que votre application crée une primitive carrée et spécifie des coordonnées de texture (0.0, 0.0), (0.0, 3.0), (3.0, 3.0) et (3,0, 0.0).</span><span class="sxs-lookup"><span data-stu-id="24783-105">Suppose, for example, your application creates a square primitive and specifies texture coordinates of (0.0,0.0), (0.0,3.0), (3.0,3.0), and (3.0,0.0).</span></span> <span data-ttu-id="24783-106">Si vous définissez le mode d’adressage de la texture sur D3DTADDRESS, \_ les résultats de la texture sont appliqués trois fois dans les directions u et v.</span><span class="sxs-lookup"><span data-stu-id="24783-106">Setting the texture addressing mode to D3DTADDRESS\_MIRROR results in the texture being applied three times in both the u- and v-directions.</span></span> <span data-ttu-id="24783-107">Chaque ligne et colonne à laquelle il est appliqué est une image miroir de la ligne ou de la colonne précédente, comme indiqué dans l’illustration suivante.</span><span class="sxs-lookup"><span data-stu-id="24783-107">Every other row and column that it is applied to is a mirror image of the preceding row or column, as shown in the following illustration.</span></span>

![illustration d’images miroir dans une grille 3x3](images/mirror.png)

<span data-ttu-id="24783-109">Les effets de ce mode d’adresse de texture sont similaires à ceux du mode habillage, mais diffèrent de ceux-ci.</span><span class="sxs-lookup"><span data-stu-id="24783-109">The effects of this texture address mode are similar to, but distinct from, those of the wrap mode.</span></span> <span data-ttu-id="24783-110">Pour plus d’informations, consultez [Wrap texture mode Address (Direct3D 9)](wrap-texture-address-mode.md).</span><span class="sxs-lookup"><span data-stu-id="24783-110">For more information, see [Wrap Texture Address Mode (Direct3D 9)](wrap-texture-address-mode.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="24783-111">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="24783-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="24783-112">Modes d’adressage de la texture</span><span class="sxs-lookup"><span data-stu-id="24783-112">Texture Addressing Modes</span></span>](texture-addressing-modes.md)
</dt> </dl>

 

 
