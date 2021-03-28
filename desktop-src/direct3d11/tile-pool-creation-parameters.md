---
title: Paramètres de création d’un pool de vignettes
description: Utilisez les paramètres de cette section pour définir des pools de mosaïques via l’API ID3D11Device CreateBuffer.
ms.assetid: 04290AAF-8517-4557-954E-1CAA3A0CA7F6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c22ef3acf1c7b926890d1c5867df55bea4821b90
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028731"
---
# <a name="tile-pool-creation-parameters"></a><span data-ttu-id="41f07-103">Paramètres de création d’un pool de vignettes</span><span class="sxs-lookup"><span data-stu-id="41f07-103">Tile pool creation parameters</span></span>

<span data-ttu-id="41f07-104">Utilisez les paramètres de cette section pour définir des pools de mosaïques via l’API [**ID3D11Device :: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) .</span><span class="sxs-lookup"><span data-stu-id="41f07-104">Use the parameters in this section to define tile pools via the [**ID3D11Device::CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) API.</span></span>

<dl> <dt>

<span data-ttu-id="41f07-105"><span id="Size"></span><span id="size"></span><span id="SIZE"></span>**Corps**</span><span class="sxs-lookup"><span data-stu-id="41f07-105"><span id="Size"></span><span id="size"></span><span id="SIZE"></span>**Size**</span></span>
</dt> <dd>

<span data-ttu-id="41f07-106">Taille d’allocation, en tant que multiple de 64 Ko.</span><span class="sxs-lookup"><span data-stu-id="41f07-106">Allocation size, as a multiple of 64KB.</span></span> <span data-ttu-id="41f07-107">0 est valide, car vous pouvez utiliser ultérieurement une opération [**ID3D11DeviceContext2 :: ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool) .</span><span class="sxs-lookup"><span data-stu-id="41f07-107">0 is valid because you can later use a [**ID3D11DeviceContext2::ResizeTilePool**](/windows/desktop/api/D3D11_2/nf-d3d11_2-id3d11devicecontext2-resizetilepool) operation.</span></span>

</dd> <dt>

<span data-ttu-id="41f07-108"><span id="Supported_Resource_Misc_Flags"></span><span id="supported_resource_misc_flags"></span><span id="SUPPORTED_RESOURCE_MISC_FLAGS"></span>**Indicateurs divers des ressources pris en charge**</span><span class="sxs-lookup"><span data-stu-id="41f07-108"><span id="Supported_Resource_Misc_Flags"></span><span id="supported_resource_misc_flags"></span><span id="SUPPORTED_RESOURCE_MISC_FLAGS"></span>**Supported Resource Misc Flags**</span></span>
</dt> <dd>

<span data-ttu-id="41f07-109">D3D11 \_ \_ pool de \_ mosaïques divers \_ de ressources (identifie la ressource en tant que pool de MOSAÏQUEs), d3d11 partagé \_ divers de la ressource \_ \_ , \_ \_ KEYEDMUTEX partagé ou \_ \_ NTHANDLE partagé.</span><span class="sxs-lookup"><span data-stu-id="41f07-109">D3D11\_RESOURCE\_MISC\_TILE\_POOL (identifies the resource as a tile pool), D3D11\_RESOURCE\_MISC\_SHARED, \_SHARED\_KEYEDMUTEX, or \_SHARED\_NTHANDLE.</span></span>

</dd> <dt>

<span data-ttu-id="41f07-110"><span id="Supported_Resource_Usage"></span><span id="supported_resource_usage"></span><span id="SUPPORTED_RESOURCE_USAGE"></span>**Utilisation des ressources prise en charge**</span><span class="sxs-lookup"><span data-stu-id="41f07-110"><span id="Supported_Resource_Usage"></span><span id="supported_resource_usage"></span><span id="SUPPORTED_RESOURCE_USAGE"></span>**Supported Resource Usage**</span></span>
</dt> <dd>

<span data-ttu-id="41f07-111">Utilisation de D3D11 \_ \_ par défaut uniquement.</span><span class="sxs-lookup"><span data-stu-id="41f07-111">D3D11\_USAGE\_DEFAULT only.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="41f07-112">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="41f07-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41f07-113">Création de ressources en mosaïque</span><span class="sxs-lookup"><span data-stu-id="41f07-113">Creating tiled resources</span></span>](creating-tiled-resources.md)
</dt> </dl>

 

 




