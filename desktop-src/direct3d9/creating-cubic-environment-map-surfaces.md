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
# <a name="creating-cubic-environment-map-surfaces-direct3d-9"></a><span data-ttu-id="c425c-104">Création de surfaces de mappage d’environnement cubique (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="c425c-104">Creating Cubic Environment Map Surfaces (Direct3D 9)</span></span>

<span data-ttu-id="c425c-105">Vous créez une texture de la carte de l’environnement cubique en appelant la méthode [**CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture) .</span><span class="sxs-lookup"><span data-stu-id="c425c-105">You create a cubic environment map texture by calling the [**CreateCubeTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createcubetexture) method.</span></span> <span data-ttu-id="c425c-106">Les textures de la carte d’environnement cubique doivent être carrées, avec des dimensions qui sont une puissance de deux.</span><span class="sxs-lookup"><span data-stu-id="c425c-106">Cubic environment map textures must be square, with dimensions that are a power of two.</span></span>

<span data-ttu-id="c425c-107">L’exemple de code suivant montre comment votre application C++ peut créer un mappage d’environnement cubique simple.</span><span class="sxs-lookup"><span data-stu-id="c425c-107">The following code example shows how your C++ application might create a simple cubic environment map.</span></span>


```
// Init m_d3dDevice to point to an IDirect3DDevice9 interface

LPDIRECT3DCUBETEXTURE9 m_pCubeMap;

m_d3dDevice->CreateCubeTexture(256, 1, D3DUSAGE_RENDERTARGET, D3DFMT_R8G8B8,
                                D3DPOOL_DEFAULT, &m_pCubeMap);
```



## <a name="accessing-cubic-environment-map-faces"></a><span data-ttu-id="c425c-108">Accès aux visages de la carte d’environnement cubique</span><span class="sxs-lookup"><span data-stu-id="c425c-108">Accessing Cubic Environment Map Faces</span></span>

<span data-ttu-id="c425c-109">Vous pouvez naviguer entre les faces d’un mappage d’environnement cubique à l’aide de la méthode [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) .</span><span class="sxs-lookup"><span data-stu-id="c425c-109">You can navigate between faces of a cubic environment map by using the [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) method.</span></span>

<span data-ttu-id="c425c-110">L’exemple de code suivant utilise [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) pour récupérer la surface de la table des cubes utilisée pour le visage en y positif (face 2).</span><span class="sxs-lookup"><span data-stu-id="c425c-110">The following code example uses [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) to retrieve the cube-map surface used for the positive y-face (face 2).</span></span>


```
// Init m_pCubeMap to point to an IDirect3DCubeTexture9 interface

LPDIRECT3DSURFACE9 pFace2;
m_pCubeMap->GetCubeMapSurface(D3DCUBEMAP_FACE_POSITIVE_Y, 0, &pFace2);
```



<span data-ttu-id="c425c-111">Le premier paramètre que [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) accepte est une valeur énumérée [**D3DCUBEMAP \_**](./d3dcubemap-faces.md) qui décrit la surface attachée que la méthode doit récupérer.</span><span class="sxs-lookup"><span data-stu-id="c425c-111">The first parameter that [**GetCubeMapSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dcubetexture9-getcubemapsurface) accepts is a [**D3DCUBEMAP\_FACES**](./d3dcubemap-faces.md) enumerated value that describes the attached surface that the method should retrieve.</span></span> <span data-ttu-id="c425c-112">Le deuxième paramètre indique à Direct3D le niveau de texture de cube mipmapped à récupérer.</span><span class="sxs-lookup"><span data-stu-id="c425c-112">The second parameter tells Direct3D which level of a mipmapped cube texture to retrieve.</span></span> <span data-ttu-id="c425c-113">Le troisième paramètre accepté est l’adresse de l’interface [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) , qui représente la surface de texture de cube retournée.</span><span class="sxs-lookup"><span data-stu-id="c425c-113">The third parameter accepted is the address of the [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface, representing the returned cube texture surface.</span></span> <span data-ttu-id="c425c-114">Étant donné que ce mappage de cube n’est pas mipmapped, 0 est utilisé ici.</span><span class="sxs-lookup"><span data-stu-id="c425c-114">Because this cube-map is not mipmapped, 0 is used here.</span></span>

> [!Note]
>
> <span data-ttu-id="c425c-115">Après l’appel de cette méthode, le nombre de références internes sur l’interface [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) est augmenté.</span><span class="sxs-lookup"><span data-stu-id="c425c-115">After calling this method, the internal reference count on the [**IDirect3DSurface9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dsurface9) interface is increased.</span></span> <span data-ttu-id="c425c-116">Lorsque vous avez fini d’utiliser cette surface, veillez à appeler la méthode [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) sur cette interface **IDirect3DSurface9** , sinon vous obtiendrez une fuite de mémoire.</span><span class="sxs-lookup"><span data-stu-id="c425c-116">When you are done using this surface, be sure to call the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) method on this **IDirect3DSurface9** interface or you will have a memory leak.</span></span>

 

## <a name="rendering-to-cubic-environment-maps"></a><span data-ttu-id="c425c-117">Rendu des mappages d’environnement cubiques</span><span class="sxs-lookup"><span data-stu-id="c425c-117">Rendering to Cubic Environment Maps</span></span>

<span data-ttu-id="c425c-118">Vous pouvez copier des images sur les faces individuelles du mappage de cube comme vous le feriez pour tout autre objet de texture ou de surface.</span><span class="sxs-lookup"><span data-stu-id="c425c-118">You can copy images to the individual faces of the cube map just like you would any other texture or surface object.</span></span> <span data-ttu-id="c425c-119">La chose la plus importante à faire avant d’effectuer un rendu sur un visage est de définir les matrices de transformation afin que la caméra soit positionnée correctement et qu’elle pointe vers la bonne direction pour cette face : vers l’avant (+ z), vers la gauche (-x), vers la droite (+ x), vers le haut (+ y) ou vers le bas.</span><span class="sxs-lookup"><span data-stu-id="c425c-119">The most important thing to do before rendering to a face is set the transformation matrices so that the camera is positioned properly and points in the proper direction for that face: forward (+z), backward (-z), left (-x), right (+x), up (+y), or down (-y).</span></span>

<span data-ttu-id="c425c-120">L’exemple de code C++ suivant prépare et définit une matrice de vue en fonction de la face rendue.</span><span class="sxs-lookup"><span data-stu-id="c425c-120">The following C++ code example prepares and sets a view matrix according to the face being rendered.</span></span>


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



<span data-ttu-id="c425c-121">N’oubliez pas que chaque face d’une carte d’environnement cubique représente un champ de vue de 90 degré.</span><span class="sxs-lookup"><span data-stu-id="c425c-121">Remember, each face of a cubic environment map represents a 90-degree field of view.</span></span> <span data-ttu-id="c425c-122">À moins que votre application ne nécessite un champ différent de l’angle de vue, pour des effets spéciaux, par exemple, veillez à définir la matrice de projection en conséquence.</span><span class="sxs-lookup"><span data-stu-id="c425c-122">Unless your application requires a different field of view angle - for special effects, for example - take care to set the projection matrix accordingly.</span></span>

<span data-ttu-id="c425c-123">Cet exemple de code crée et définit une matrice de projection pour le cas le plus courant.</span><span class="sxs-lookup"><span data-stu-id="c425c-123">This code example creates and sets a projection matrix for the most common case.</span></span>


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



<span data-ttu-id="c425c-124">Lorsque l’appareil photo est en position et la matrice de projection définie, vous pouvez effectuer le rendu de la scène.</span><span class="sxs-lookup"><span data-stu-id="c425c-124">When the camera is in position and the projection matrix set, you can render the scene.</span></span> <span data-ttu-id="c425c-125">Chaque objet de la scène doit être positionné comme vous le feriez normalement.</span><span class="sxs-lookup"><span data-stu-id="c425c-125">Each object in the scene should be positioned as you would normally position them.</span></span> <span data-ttu-id="c425c-126">L’exemple de code suivant, fourni à des fins d’exhaustivité, décrit cette tâche.</span><span class="sxs-lookup"><span data-stu-id="c425c-126">The following code example, provided for completeness, outlines this task.</span></span>


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



<span data-ttu-id="c425c-127">Notez l’appel à la méthode [**SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget) .</span><span class="sxs-lookup"><span data-stu-id="c425c-127">Note the call to the [**SetRenderTarget**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrendertarget) method.</span></span> <span data-ttu-id="c425c-128">Lors du rendu des visages de la carte du cube, vous devez affecter la face comme surface de la cible de rendu actuelle.</span><span class="sxs-lookup"><span data-stu-id="c425c-128">When rendering to the cube map faces, you must assign the face as the current render-target surface.</span></span> <span data-ttu-id="c425c-129">Les applications qui utilisent des mémoires tampons de profondeur peuvent créer explicitement un tampon de profondeur pour la cible de rendu, ou réassigner une mémoire tampon de profondeur existante à la surface de cible de rendu.</span><span class="sxs-lookup"><span data-stu-id="c425c-129">Applications that use depth buffers can explicitly create a depth-buffer for the render-target, or reassign an existing depth-buffer to the render-target surface.</span></span> <span data-ttu-id="c425c-130">L’exemple de code ci-dessus utilise la dernière approche.</span><span class="sxs-lookup"><span data-stu-id="c425c-130">The code sample above uses the latter approach.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c425c-131">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="c425c-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c425c-132">Mappage d’environnement cubique</span><span class="sxs-lookup"><span data-stu-id="c425c-132">Cubic Environment Mapping</span></span>](cubic-environment-mapping.md)
</dt> </dl>

 

 
