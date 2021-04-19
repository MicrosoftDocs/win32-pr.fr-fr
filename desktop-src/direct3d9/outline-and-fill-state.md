---
description: Les primitives qui n’ont pas de textures sont rendues avec la couleur spécifiée par leur matériau, ou avec les couleurs spécifiées pour les vertex, le cas échéant.
ms.assetid: 8a7ed4b1-25a1-4984-baea-6e176f0545ea
title: État du contour et du remplissage (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65092fb2e4bfe29ac5e9f9291250a0c78b80626d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106517368"
---
# <a name="outline-and-fill-state-direct3d-9"></a>État du contour et du remplissage (Direct3D 9)

Les primitives qui n’ont pas de textures sont rendues avec la couleur spécifiée par leur matériau, ou avec les couleurs spécifiées pour les vertex, le cas échéant. Vous pouvez sélectionner la méthode pour les remplir en spécifiant une valeur définie par le type énuméré [**D3DFILLMODE**](./d3dfillmode.md) pour l' \_ État de rendu D3DRS FillMode.

Pour activer le tramage, votre application doit passer la \_ valeur énumérée D3DRS DITHERENABLE en tant que premier paramètre à [**IDirect3DDevice9 :: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate). Il doit affecter la **valeur true** au deuxième paramètre pour activer le tramage et la **valeur false** pour le désactiver.

À des moments, le fait de dessiner le dernier pixel d’une ligne peut entraîner un chevauchement des primitives environnantes. Vous pouvez contrôler cela à l’aide de la \_ valeur énumérée D3DRS LASTPIXEL. Toutefois, ne modifiez pas ce paramètre sans une réflexion. Dans certaines conditions, la suppression du rendu du dernier Pixel peut entraîner des écarts imesthétiques entre les primitives.

Les contours d’objets peuvent être dessinés en définissant le modèle de dessin de ligne approprié. L’état de dessin par défaut consiste à dessiner des lignes pleines. Pour plus d’informations, consultez [prise en charge du dessin en ligne dans l’état de rendu D3DX (Direct3D 9)](line-drawing-support-in-d3dx.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[États de rendu](render-states.md)
</dt> </dl>

 

 
