---
title: Comment créer un nuanceur de domaine
description: Cette rubrique montre comment créer un nuanceur de domaine.
ms.assetid: 7d02fee4-2d7c-434b-86ab-e5ee615ae93b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f89b7f3d7ec6cf801432a5745520fcbd924d139
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028735"
---
# <a name="how-to-create-a-domain-shader"></a>Comment : créer un nuanceur de domaine

Un nuanceur de domaine est le troisième des trois étapes qui fonctionnent ensemble pour implémenter le [pavage](direct3d-11-advanced-stages-tessellation.md). Les entrées de l’étape de nuanceur de domaine proviennent d’un nuanceur de coque. Cette rubrique montre comment créer un nuanceur de domaine.

Un nuanceur de domaine transforme la géométrie de surface (créée par l’étape du paveur de la fonction fixe) à l’aide des points de contrôle de sortie de nuanceur de coque, des données de correction de sortie de nuanceur de coque et un ensemble unique de coordonnées UV du paveur.

**Pour créer un nuanceur de domaine**

1.  Concevoir un nuanceur de domaine. Consultez [Comment : concevoir un nuanceur de domaine](direct3d-11-advanced-stages-domain-shader-design.md).
2.  Compilez le code du nuanceur.
3.  Créez un objet de nuanceur de domaine à l’aide de [**ID3D11Device :: CreateDomainShader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createdomainshader).
    ```
    HRESULT CreateDomainShader(
      const void *pShaderBytecode, // 
      SIZE_T BytecodeLength, // 
      ID3D11ClassLinkage *pClassLinkage, // 
      ID3D11DomainShader **ppDomainShader
    );
    ```

    

4.  Initialisez l’étape de pipeline à l’aide de [**ID3D11DeviceContext ::D ssetshader**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-dssetshader).
    ```
    void DSSetShader(
      ID3D11DomainShader *pDomainShader, // 
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

 

 




