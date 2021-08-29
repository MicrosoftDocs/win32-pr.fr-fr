---
description: Par défaut, lorsque le test de profondeur est effectué sur une surface de rendu, le système Direct3D met à jour la surface de la cible de rendu si la valeur de profondeur correspondante (z ou w) pour chaque point est inférieure à la valeur de la mémoire tampon de profondeur.
ms.assetid: e9243c05-e943-4a42-ab73-e684900fc81d
title: Modification des fonctions de comparaison du tampon de profondeur (D3D9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11bdbb808b84fd95eb36e3ea66c4e6faf882826faf8a8c2ab3ed3b9b06f9da79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989319"
---
# <a name="changing-depth-buffer-comparison-functions-d3d9"></a>Modification des fonctions de comparaison du tampon de profondeur (D3D9)

Par défaut, lorsque le test de profondeur est effectué sur une surface de rendu, le système Direct3D met à jour la surface de la cible de rendu si la valeur de profondeur correspondante (z ou w) pour chaque point est inférieure à la valeur de la mémoire tampon de profondeur. Dans une application C++, vous modifiez la manière dont le système effectue des comparaisons sur les valeurs de profondeur en appelant la méthode [**IDirect3DDevice9 :: SetRenderState**](/windows/desktop/api) avec le paramètre d' *État* défini sur D3DRS \_ ZFUNC. Le paramètre de *valeur* doit être défini sur une valeur dans le type énuméré [**D3DCMPFUNC**](./d3dcmpfunc.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mémoires tampons de profondeur](depth-buffers.md)
</dt> </dl>

 

 
