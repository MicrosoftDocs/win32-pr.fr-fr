---
description: Lors de l’utilisation d’un nuanceur de sommets programmé, les éléments mis à jour dans la mémoire tampon de vertex de destination sont contrôlés par le programme de fonction de nuanceur.
ms.assetid: c75564ef-528b-4af5-9ed7-a32b9120bf6a
title: Traitement de vertex programmable (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56ee1e781aa811d8d85a8865bdf07a8811e26d027f6d385b40126a8321172a3b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120118589"
---
# <a name="programmable-vertex-processing-direct3d-9"></a>Traitement de vertex programmable (Direct3D 9)

Lors de l’utilisation d’un nuanceur de sommets programmé, les éléments mis à jour dans la mémoire tampon de vertex de destination sont contrôlés par le programme de fonction de nuanceur. Lorsque l’application écrit dans l’un des registres de vertex de destination, l’élément correspondant dans chaque vertex de la mémoire tampon de vertex de destination est mis à jour. Les éléments de la mémoire tampon de vertex de destination qui ne sont pas écrits par l’application ne sont pas modifiés. [**IDirect3DDevice9 ::P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) échoue si l’application écrit dans des éléments qui ne sont pas présents dans la mémoire tampon de vertex de destination.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mémoires tampons de vertex](vertex-buffers.md)
</dt> </dl>

 

 
