---
description: Direct3D 9 prend en charge les textures de palette via un ensemble de palettes d’entrée 256 associées à l’objet IDirect3DDevice9.
ms.assetid: dea4b4bc-7eba-40fa-9c2c-0851fe7e231b
title: Palettes de texture (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a0fbb1c5d6766b879b898145ec2385a41d94b8e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106540794"
---
# <a name="texture-palettes-direct3d-9"></a><span data-ttu-id="d5162-103">Palettes de texture (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="d5162-103">Texture Palettes (Direct3D 9)</span></span>

<span data-ttu-id="d5162-104">Direct3D 9 prend en charge les textures de palette via un ensemble de palettes d’entrée 256 associées à l’objet [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) .</span><span class="sxs-lookup"><span data-stu-id="d5162-104">Direct3D 9 supports paletted textures through a set of 256 entry palettes associated with the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) object.</span></span> <span data-ttu-id="d5162-105">Une palette est rendue active en appelant la méthode [**IDirect3DDevice9 :: SetCurrentTexturePalette**](/windows/desktop/api) .</span><span class="sxs-lookup"><span data-stu-id="d5162-105">A palette is made current by calling the [**IDirect3DDevice9::SetCurrentTexturePalette**](/windows/desktop/api) method.</span></span> <span data-ttu-id="d5162-106">La palette actuelle est utilisée pour la conversion de toutes les textures de palette pour toutes les étapes de texture actives.</span><span class="sxs-lookup"><span data-stu-id="d5162-106">The current palette is used for translating all paletted textures for all active texture stages.</span></span> <span data-ttu-id="d5162-107">[**IDirect3DDevice9 :: SetPaletteEntries**](/windows/desktop/api) met à jour toutes les entrées 256 de la palette.</span><span class="sxs-lookup"><span data-stu-id="d5162-107">[**IDirect3DDevice9::SetPaletteEntries**](/windows/desktop/api) updates all of a palette's 256 entries.</span></span> <span data-ttu-id="d5162-108">Chaque entrée est une structure [**PaletteEntry**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) au format D3DFMT \_ A8R8G8B8.</span><span class="sxs-lookup"><span data-stu-id="d5162-108">Each entry is a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure of the format D3DFMT\_A8R8G8B8.</span></span> <span data-ttu-id="d5162-109">Toutes les entrées ont la valeur par défaut 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="d5162-109">All entries default to 0xFFFFFFFF.</span></span>

<span data-ttu-id="d5162-110">Les palettes [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) contiennent un canal alpha.</span><span class="sxs-lookup"><span data-stu-id="d5162-110">The [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) palettes contain an alpha channel.</span></span> <span data-ttu-id="d5162-111">Ce canal alpha peut être utilisé lorsque l’indicateur de fonctionnalité de l' \_ appareil D3DPTEXTURECAPS ALPHAPALETTE est défini, ce qui indique que l’appareil prend en charge alpha à partir de la palette.</span><span class="sxs-lookup"><span data-stu-id="d5162-111">This alpha channel can be used when the D3DPTEXTURECAPS\_ALPHAPALETTE device capability flag is set, indicating that the device supports alpha from the palette.</span></span> <span data-ttu-id="d5162-112">Le canal alpha de la palette est utilisé lorsque le format de texture n’a pas de canal alpha.</span><span class="sxs-lookup"><span data-stu-id="d5162-112">The palette alpha channel is used when the texture format does not have an alpha channel.</span></span> <span data-ttu-id="d5162-113">Si l’appareil ne prend pas en charge alpha de la palette et que le format de texture n’a pas de canal alpha, la valeur 0xFF est utilisée pour alpha.</span><span class="sxs-lookup"><span data-stu-id="d5162-113">If the device does not support alpha from the palette and the texture format does not have an alpha channel, then a value of 0xFF is used for alpha.</span></span>

<span data-ttu-id="d5162-114">Il y a un maximum de 65 536 (0x0000FFFF) palettes.</span><span class="sxs-lookup"><span data-stu-id="d5162-114">There is a maximum of 65,536 (0x0000FFFF) palettes.</span></span> <span data-ttu-id="d5162-115">Étant donné que les ressources mémoire associées à l’ensemble de palettes sont proportionnelles au nombre maximal de palettes référencées par une application, utilisez des numéros de palette contigus à partir de zéro.</span><span class="sxs-lookup"><span data-stu-id="d5162-115">Because memory resources associated with the set of palettes are proportional to the maximum palette number that an application references, use contiguous palette numbers starting at zero.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d5162-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="d5162-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d5162-117">Concepts de base de la texturation</span><span class="sxs-lookup"><span data-stu-id="d5162-117">Basic Texturing Concepts</span></span>](basic-texturing-concepts.md)
</dt> </dl>

 

 
