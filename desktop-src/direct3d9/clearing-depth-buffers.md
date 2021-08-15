---
description: De nombreuses applications C++ effacent le tampon de profondeur avant de restituer chaque nouveau Frame.
ms.assetid: b8930211-82a1-4808-b042-1641e567cb6d
title: Effacement des tampons de profondeur (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce150d729768321cb51abbea9f24ba8b490b7705f35945a4fd03e2a8ed58a039
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989309"
---
# <a name="clearing-depth-buffers-direct3d-9"></a>Effacement des tampons de profondeur (Direct3D 9)

De nombreuses applications C++ effacent le tampon de profondeur avant de restituer chaque nouveau Frame. Vous pouvez effacer explicitement la mémoire tampon de profondeur par le biais de Direct3D en appelant [**IDirect3DDevice9 :: Clear**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-clear) et en spécifiant D3DCLEAR \_ ZBUFFER pour le paramètre flags. La méthode **IDirect3DDevice9 :: Clear** vous permet de spécifier une valeur de profondeur arbitraire dans le paramètre Z.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mémoires tampons de profondeur](depth-buffers.md)
</dt> </dl>

 

 
