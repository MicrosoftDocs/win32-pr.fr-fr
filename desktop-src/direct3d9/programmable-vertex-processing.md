---
description: Lors de l’utilisation d’un nuanceur de sommets programmé, les éléments mis à jour dans la mémoire tampon de vertex de destination sont contrôlés par le programme de fonction de nuanceur.
ms.assetid: c75564ef-528b-4af5-9ed7-a32b9120bf6a
title: Traitement de vertex programmable (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5108792350aebbca4f58924fde81d191b062591b
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106512868"
---
# <a name="programmable-vertex-processing-direct3d-9"></a>Traitement de vertex programmable (Direct3D 9)

Lors de l’utilisation d’un nuanceur de sommets programmé, les éléments mis à jour dans la mémoire tampon de vertex de destination sont contrôlés par le programme de fonction de nuanceur. Lorsque l’application écrit dans l’un des registres de vertex de destination, l’élément correspondant dans chaque vertex de la mémoire tampon de vertex de destination est mis à jour. Les éléments de la mémoire tampon de vertex de destination qui ne sont pas écrits par l’application ne sont pas modifiés. [**IDirect3DDevice9 ::P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) échoue si l’application écrit dans des éléments qui ne sont pas présents dans la mémoire tampon de vertex de destination.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mémoires tampons de vertex](vertex-buffers.md)
</dt> </dl>

 

 
