---
description: Vous créez une texture de la carte de l’environnement cubique en appelant la méthode CreateCubeTexture. Les textures de la carte d’environnement cubique doivent être carrées, avec des dimensions qui sont une puissance de deux.
ms.assetid: 3879d215-064b-4d7d-afae-2ed46569c8bf
title: Création de surfaces de mappage d’environnement cubique (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36be3067c6a5f21c39cfed7cab731ca875b70799
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523836"
---
# <a name="creating-cubic-environment-map-surfaces-direct3d-9"></a>Création de surfaces de mappage d’environnement cubique (Direct3D 9)

Vous créez une texture de la carte de l’environnement cubique en appelant la méthode [**CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture) . Les textures de la carte d’environnement cubique doivent être carrées, avec des dimensions qui sont une puissance de deux.

L’exemple de code suivant montre comment votre application C++ peut créer un mappage d’environnement cubique simple.


```
// Init m_d3dDevice to point to an IDirect3DDevice9 interface

LPDIRECT3DCUBETEXTURE9 m_pCubeMap;

m_d3dDevice->CreateCubeTexture(256, 1, D3DUSAGE_RENDERTARGET, D3DFMT_R8G8B8,
                                D3DPOOL_DEFAULT, &m_pCubeMap);
```



## <a name="accessing-cubic-environment-map-faces"></a>Accès aux visages de la carte d’environnement cubique

Vous pouvez naviguer entre les faces d’un mappage d’environnement cubique à l’aide de la méthode [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) .

L’exemple de code suivant utilise [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) pour récupérer la surface de la table des cubes utilisée pour le visage en y positif (face 2).


```
// Init m_pCubeMap to point to an IDirect3DCubeTexture9 interface

LPDIRECT3DSURFACE9 pFace2;
m_pCubeMap->GetCubeMapSurface(D3DCUBEMAP_FACE_POSITIVE_Y, 0, &pFace2);
```



Le premier paramètre que [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) accepte est une valeur énumérée [**D3DCUBEMAP \_**](./d3dcubemap-faces.md) qui décrit la surface attachée que la méthode doit récupérer. Le deuxième paramètre indique à Direct3D le niveau de texture de cube mipmapped à récupérer. Le troisième paramètre accepté est l’adresse de l’interface [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) , qui représente la surface de texture de cube retournée. Étant donné que ce mappage de cube n’est pas mipmapped, 0 est utilisé ici.

> [!Note]
>
> Après l’appel de cette méthode, le nombre de références internes sur l’interface [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) est augmenté. Lorsque vous avez fini d’utiliser cette surface, veillez à appeler la méthode [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) sur cette interface **IDirect3DSurface9** , sinon vous obtiendrez une fuite de mémoire.

 

## <a name="rendering-to-cubic-environment-maps"></a>Rendu des mappages d’environnement cubiques

Vous pouvez copier des images sur les faces individuelles du mappage de cube comme vous le feriez pour tout autre objet de texture ou de surface. La chose la plus importante à faire avant d’effectuer un rendu sur un visage est de définir les matrices de transformation afin que la caméra soit positionnée correctement et qu’elle pointe vers la bonne direction pour cette face : vers l’avant (+ z), vers la gauche (-x), vers la droite (+ x), vers le haut (+ y) ou vers le bas.

L’exemple de code C++ suivant prépare et définit une matrice de vue en fonction de la face rendue.


```
// Init pCubeMap to point to an IDirect3DCubeTexture9 interface
// Init d3dDevice to point to an IDirect3DDevice9 interface

void RenderFaces()
{
    // Save transformation matrices of the device
    D3DXMATRIX matProjSave, matViewSave;
    d3dDevice->GetTransform(D3DTS_VIEW,       &matViewSave ;
    d3dDevice->GetTransform(D3DTS_PROJECTION, &matProjSave);

    // Store the current back buffer and z-buffer
    LPDIRECT3DSURFACE9 pBackBuffer, pZBuffer;
    d3dDevice->GetRenderTarget(&pBackBuffer);
    d3dDevice->GetDepthStencilSurface(&pZBuffer);
```



N’oubliez pas que chaque face d’une carte d’environnement cubique représente un champ de vue de 90 degré. À moins que votre application ne nécessite un champ différent de l’angle de vue, pour des effets spéciaux, par exemple, veillez à définir la matrice de projection en conséquence.

Cet exemple de code crée et définit une matrice de projection pour le cas le plus courant.


```
    // Use 90-degree field of view in the projection
    D3DMATRIX matProj;
    D3DXMatrixPerspectiveFovLH(matProj, D3DX_PI/2, 1.0f, 0.5f, 1000.0f);
    d3dDevice->SetTransform(D3DTS_PROJECTION, &matProj);

    // Loop through the six faces of the cube map
    for(DWORD i=0; i<6; i++)
    {
        // Standard view that will be overridden below
        D3DVECTOR vEnvEyePt = D3DVECTOR(0.0f, 0.0f, 0.0f);
        D3DVECTOR vLookatPt, vUpVec;

        switch(i)
        {
            case D3DCUBEMAP_FACE_POSITIVE_X:
                vLookatPt = D3DVECTOR(1.0f, 0.0f, 0.0f);
                vUpVec    = D3DVECTOR(0.0f, 1.0f, 0.0f);
                break;
            case D3DCUBEMAP_FACE_NEGATIVE_X:
                vLookatPt = D3DVECTOR(-1.0f, 0.0f, 0.0f);
                vUpVec    = D3DVECTOR( 0.0f, 1.0f, 0.0f);
                break;
            case D3DCUBEMAP_FACE_POSITIVE_Y:
                vLookatPt = D3DVECTOR(0.0f, 1.0f, 0.0f);
                vUpVec    = D3DVECTOR(0.0f, 0.0f,-1.0f);
                break;
            case D3DCUBEMAP_FACE_NEGATIVE_Y:
                vLookatPt = D3DVECTOR(0.0f,-1.0f, 0.0f);
                vUpVec    = D3DVECTOR(0.0f, 0.0f, 1.0f);
                break;
            case D3DCUBEMAP_FACE_POSITIVE_Z:
                vLookatPt = D3DVECTOR( 0.0f, 0.0f, 1.0f);
                vUpVec    = D3DVECTOR( 0.0f, 1.0f, 0.0f);
                break;
            case D3DCUBEMAP_FACE_NEGATIVE_Z:
                vLookatPt = D3DVECTOR(0.0f, 0.0f,-1.0f);
                vUpVec    = D3DVECTOR(0.0f, 1.0f, 0.0f);
                break;
        }

         D3DMATRIX matView;
         D3DXMatrixLookAtLH(matView, vEnvEyePt, vLookatPt, vUpVec);
         d3dDevice->SetTransform(D3DTS_VIEW, &matView);
```



Lorsque l’appareil photo est en position et la matrice de projection définie, vous pouvez effectuer le rendu de la scène. Chaque objet de la scène doit être positionné comme vous le feriez normalement. L’exemple de code suivant, fourni à des fins d’exhaustivité, décrit cette tâche.


```
        // Get pointer to surface in order to render to it
        LPDIRECT3DSURFACE9 pFace;
        pCubeMap->GetCubeMapSurface((D3DCUBEMAP_FACES)i, 0, &pFace);
        d3dDevice->SetRenderTarget (pFace , pZBuffer);
        SAFE_RELEASE(pFace);

        d3dDevice->BeginScene();
        // Render scene here
        ...
        d3dDevice->EndScene();
    }

    // Change the render target back to the main back buffer.
    d3dDevice->SetRenderTarget(pBackBuffer, pZBuffer);
    SAFE_RELEASE(pBackBuffer);
    SAFE_RELEASE(pZBuffer);

    // Restore the original transformation matrices
    d3dDevice->SetTransform(D3DTS_VIEW,       &matViewSave);
    d3dDevice->SetTransform(D3DTS_PROJECTION, &matProjSave);
}
```



Notez l’appel à la méthode [**SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget) . Lors du rendu des visages de la carte du cube, vous devez affecter la face comme surface de la cible de rendu actuelle. Les applications qui utilisent des mémoires tampons de profondeur peuvent créer explicitement un tampon de profondeur pour la cible de rendu, ou réassigner une mémoire tampon de profondeur existante à la surface de cible de rendu. L’exemple de code ci-dessus utilise la dernière approche.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mappage d’environnement cubique](cubic-environment-mapping.md)
</dt> </dl>

 

 
