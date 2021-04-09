---
description: Définit un cadre de coordonnées, ou &\# 0034 ; cadre de référence. &\# 0034 ; Le modèle de frame est ouvert et peut contenir n’importe quel objet. Les fonctions de maillage de D3DX reconnaissent les instances de modèle Mesh, FrameTransformMatrix et Frame comme des objets enfants lors du chargement d’une instance de frame.
ms.assetid: vs|directx_sdk|~\frame.htm
title: Frame (Direct3D 9 Graphics)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81cc9d02b1bcbc21cc299739d93272afcf110c92
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845969"
---
# <a name="frame-direct3d-9-graphics"></a>Frame (Direct3D 9 Graphics)

Définit un cadre de coordonnées, ou « cadre de référence ». Le modèle de frame est ouvert et peut contenir n’importe quel objet. Les fonctions de maillage de D3DX reconnaissent les instances de modèle [**Mesh**](mesh.md), [**FrameTransformMatrix**](frametransformmatrix.md)et **Frame** comme des objets enfants lors du chargement d’une instance de **Frame** .

``` syntax
template Frame
{
    < 3D82AB46-62DA-11CF-AB39-0020AF71E433 >
    [...]           
} 
```

Le modèle de frame reconnaît les nœuds **Frame** et de [**maillage**](mesh.md) enfants à l’intérieur d’un frame et peut reconnaître les modèles définis par l’utilisateur par le biais d’une fonction de rappel.

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Modèles](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



