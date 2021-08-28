---
title: Comment initialiser l’étape du paveur
description: Cette rubrique montre comment initialiser l’étape du paveur.
ms.assetid: 81f5461a-0938-4c46-b3e8-bef2bea125a5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f842b1095a4053ad35838864bac6d6677194d85f48e0a78e2fc6975af1e3b8d8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096279"
---
# <a name="how-to-initialize-the-tessellator-stage"></a>Comment : initialiser l’étape du paveur

En général, la facettisation étend le modèle compact, défini par l’utilisateur, d’un correctif dans une géométrie qui contient une quantité programmable de détails. La géométrie est généralement un ensemble de triangles qui représente une géométrie de surface détaillée. Cette rubrique montre comment initialiser l’étape du paveur.

L’étape du paveur est la seconde des trois étapes qui fonctionnent ensemble pour paver ou juxtaposer une surface. La première étape est l’étape de nuanceur de coque ; Il fonctionne une fois par correctif et configure la façon dont l’étape suivante (la fonction fixe du paveur) se comporte. Un nuanceur de coque génère également des sorties définies par l’utilisateur, telles que des points de contrôle de sortie et des constantes de correction qui sont envoyées au-delà du du paveur directement à la troisième étape, l’étape de nuanceur de domaine. Un nuanceur de domaine est appelé une fois par point de du paveur et évalue les positions de surface.

L’étape du paveur est une étape de fonction fixe, aucun nuanceur à générer et aucun État à définir. Elle reçoit tout son état d’installation à partir de l’étape de nuanceur de coque ; une fois que l’étape de nuanceur de coque a été initialisée, l’étape du paveur est initialisée automatiquement.

**Pour initialiser l’étape du paveur**

-   Initialisez l’étape de nuanceur de coque à l’aide de [**ID3D11DeviceContext :: HSSetShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-hssetshader).

    ```
    void HSSetShader(
      ID3D11HullShader *pHullShader,  
      ID3D11ClassInstance *const *ppClassInstances,
      UINT NumClassInstances
    );
    ```

    

    *ppClassInstances* est un pointeur vers un tableau d’interfaces de nuanceur, représenté par les pointeurs [**ID3D11ClassInstance**](/windows/desktop/api/D3D11/nn-d3d11-id3d11classinstance) et le nombre d’interfaces, représenté par *NumClassInstances*. Si ce paramètre n’est pas utilisé, ces paramètres peuvent avoir la valeur **null** et la valeur 0 respectivement.

Après l’initialisation de l’étape de nuanceur de coque, vous devez également initialiser l’étape de nuanceur de domaine.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Comment utiliser Direct3D 11](how-to-use-direct3d-11.md)
</dt> <dt>

[Vue d’ensemble de la polygonalisation](direct3d-11-advanced-stages-tessellation.md)
</dt> </dl>

 

 




