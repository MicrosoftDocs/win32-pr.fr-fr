---
title: Création d’un pool de vignettes
description: Un pool de mosaïques est créé par le biais de l’API ID3D11Device CreateBuffer en passant l' \_ \_ \_ indicateur de pool de mosaïques divers de la ressource d3d11 \_ dans le membre MiscFlags de la \_ structure DESC de mémoire tampon d3d11 \_ vers laquelle pointe le paramètre pDesc.
ms.assetid: 751A64A6-C9B6-4797-BA1C-B3BEF655DF32
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1f3b66a9a548d27382f8cbb4e447516beea6eca8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918519"
---
# <a name="tile-pool-creation"></a>Création d’un pool de vignettes

Un pool de mosaïques est créé via l’API [**ID3D11Device :: CreateBuffer**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createbuffer) en passant l’indicateur de [**\_ \_ \_ \_ pool de mosaïques divers de la ressource d3d11**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_resource_misc_flag) dans le membre **MiscFlags** de  la structure [**\_ \_ desc de mémoire tampon d3d11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_buffer_desc) vers laquelle pointe le paramètre pDesc.

Les applications peuvent créer un ou plusieurs pools de mosaïques par appareil Direct3D. La taille totale de chaque pool de mosaïques est limitée à la limite de taille des ressources de Direct3D 11, soit environ 1/4 de RAM de l’unité de traitement graphique (GPU).

Un pool de mosaïques est constitué de 64 Ko, mais le système d’exploitation (pilote d’affichage) gère l’ensemble du pool comme une ou plusieurs allocations en arrière-plan : la répartition n’est pas visible pour les applications. Les ressources en mosaïque définissent le contenu en pointant sur les vignettes d’un pool de mosaïques. Le démappage d’une vignette à partir d’une ressource en mosaïque est effectué en pointant la vignette sur la **valeur null**. Ces vignettes non mappées ont des règles sur le comportement des lectures ou des écritures. Pour plus d’informations, consultez le [suivi des risques et les ressources de pool de mosaïques](hazard-tracking-versus-tile-pool-resources.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mappages dans un pool de vignettes](mappings-are-into-a-tile-pool.md)
</dt> </dl>

 

 




