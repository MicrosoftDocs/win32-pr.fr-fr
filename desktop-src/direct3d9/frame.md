---
description: Définit un cadre de coordonnées, ou &\# 0034 ; cadre de référence. &\# 0034 ; Le modèle de frame est ouvert et peut contenir n’importe quel objet. Les fonctions de maillage de D3DX reconnaissent les instances de modèle Mesh, FrameTransformMatrix et Frame comme des objets enfants lors du chargement d’une instance de frame.
ms.assetid: vs|directx_sdk|~\frame.htm
title: Frame (Direct3D 9 Graphics)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff77cc6f4618b3ded3afc9453c12a96b115ec4bfe0f90cb83a92826378212c83
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118523032"
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

 

 



