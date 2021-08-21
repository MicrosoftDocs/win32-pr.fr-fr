---
description: 'Après avoir créé une mémoire tampon de profondeur, comme décrit dans création d’un tampon de profondeur (Direct3D 9), vous activez la mise en mémoire tampon de profondeur en appelant la méthode IDirect3DDevice9 :: SetRenderState.'
ms.assetid: a3c972dd-3630-4d21-a22b-64a68e9acd19
title: Activation de la mise en mémoire tampon de profondeur (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e495b06e6c7d10890393f563c67053294010515e32a2eeb984abb371b8158231
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118095094"
---
# <a name="enabling-depth-buffering-direct3d-9"></a>Activation de la mise en mémoire tampon de profondeur (Direct3D 9)

Après avoir créé une mémoire tampon de profondeur, comme décrit dans [création d’un tampon de profondeur (Direct3D 9)](creating-a-depth-buffer.md), vous activez la mise en mémoire tampon de profondeur en appelant la méthode [**IDirect3DDevice9 :: SetRenderState**](/windows/desktop/api) . Définissez l' \_ État de rendu D3DRS ZENABLE pour activer la mise en mémoire tampon de profondeur. Utilisez le \_ membre D3DZB true du type énuméré [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) (ou **true**) pour activer la mise en mémoire tampon z, D3DZB \_ USEW pour activer la mise en mémoire tampon w ou D3DZB \_ false (ou **false**) pour désactiver la mise en mémoire tampon de profondeur.

> [!Note]  
> Pour utiliser la mise en mémoire tampon w, votre application doit définir une matrice de projection conforme même si elle n’utilise pas le pipeline de transformation Direct3D. Pour plus d’informations sur la façon de fournir une matrice de projection appropriée, consultez [une matrice de projection avec l’W-friendly](projection-transform.md)

 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mémoires tampons de profondeur](depth-buffers.md)
</dt> </dl>

 

 
