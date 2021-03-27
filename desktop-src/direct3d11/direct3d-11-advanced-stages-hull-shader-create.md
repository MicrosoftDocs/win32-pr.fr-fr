---
title: Comment créer un nuanceur de coque
description: Cette rubrique montre comment créer un nuanceur de coque.
ms.assetid: 221cb578-fcfc-411a-8515-7880a96e32ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1a1eea7d2e6e70377028976f9576790ce3b64ab
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671654"
---
# <a name="how-to-create-a-hull-shader"></a>Comment : créer un nuanceur de coque

Un nuanceur de coque est le premier des trois étapes qui fonctionnent ensemble pour implémenter le [pavage](direct3d-11-advanced-stages-tessellation.md). Les sorties de nuanceur de coque désignent l’étape du paveur, ainsi que l’étape de nuanceur de domaine. Cette rubrique montre comment créer un nuanceur de coque.

Un nuanceur de coque transforme un ensemble de points de contrôle d’entrée (à partir d’un nuanceur de sommets) en un ensemble de points de contrôle de sortie. Le nombre de points d’entrée et de sortie peut varier en fonction du contenu et du nombre selon la transformation (une transformation classique est une transformation de base).

Un nuanceur de coque génère également des informations sur les constantes correctifs, telles que les facteurs de pavage, pour un nuanceur de domaine et le du paveur. L’étape du paveur de la fonction fixe utilise les facteurs de pavage ainsi que les autres États déclarés dans un nuanceur de coque pour déterminer la quantité à paver.

**Pour créer un nuanceur de coque**

1.  Concevoir un nuanceur de coque. Consultez [Comment : concevoir un nuanceur de coque](direct3d-11-advanced-stages-hull-shader-design.md).
2.  Compiler le code du nuanceur
3.  Créez un objet de nuanceur de coque à l’aide de [**ID3D11Device :: CreateHullShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createhullshader).
    ```
    HRESULT CreateHullShader(
      const void *pShaderBytecode,  
      SIZE_T BytecodeLength,  
      ID3D11ClassLinkage *pClassLinkage,  
      ID3D11HullShader **ppHullShader
    );
    ```

    

4.  Initialisez l’étape de pipeline à l’aide de [**ID3D11DeviceContext :: HSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader).
    ```
    void HSSetShader(
      ID3D11HullShader *pHullShader,  
      ID3D11ClassInstance *const *ppClassInstances,
      UINT NumClassInstances
    );
    ```

    

Un nuanceur de domaine doit être lié au pipeline si un nuanceur de coque est lié. En particulier, il n’est pas valide de diffuser directement en continu des points de contrôle de nuanceur de coque avec le nuanceur Geometry.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Comment utiliser Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[Vue d’ensemble de la polygonalisation](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 




