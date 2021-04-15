---
description: L’anticrénelage de scène entière fait référence à l’atténuation des bords de chaque polygone dans la scène au fur et à mesure qu’il est pixellisé en une seule passe. aucune deuxième passe n’est nécessaire.
ms.assetid: b57974ab-5654-412d-ae59-58f67a88c121
title: Anticrénelage de Full-Scene (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d73d559c4b4fec060efbff7468ee29e6c83b64c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104520911"
---
# <a name="full-scene-antialiasing-direct3d-9"></a><span data-ttu-id="b1bb7-103">Anticrénelage de Full-Scene (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="b1bb7-103">Full-Scene Antialiasing (Direct3D 9)</span></span>

<span data-ttu-id="b1bb7-104">L’anticrénelage de scène entière fait référence à l’atténuation des bords de chaque polygone dans la scène au fur et à mesure qu’il est pixellisé en une seule passe. aucune deuxième passe n’est nécessaire.</span><span class="sxs-lookup"><span data-stu-id="b1bb7-104">Full-scene antialiasing refers to blurring the edges of each polygon in the scene as it is rasterized in a single pass; no second pass is required.</span></span> <span data-ttu-id="b1bb7-105">L’anticrénelage de scène entière, lorsqu’il est pris en charge, affecte uniquement les triangles et les groupes de triangles.</span><span class="sxs-lookup"><span data-stu-id="b1bb7-105">Full-scene antialiasing, when supported, affects only triangles and groups of triangles.</span></span> <span data-ttu-id="b1bb7-106">Les lignes ne peuvent pas être antialiasées à l’aide des services Direct3D.</span><span class="sxs-lookup"><span data-stu-id="b1bb7-106">Lines cannot be antialiased by using Direct3D services.</span></span> <span data-ttu-id="b1bb7-107">L’anticrénelage de scène entière est effectué dans Direct3D en utilisant l’échantillonnage multiple sur chaque pixel.</span><span class="sxs-lookup"><span data-stu-id="b1bb7-107">Full-scene antialiasing is done in Direct3D by using multisampling on each pixel.</span></span> <span data-ttu-id="b1bb7-108">Lorsque l’échantillonnage multiple est activé, tous les sous-échantillons d’un pixel sont mis à jour en une seule passe, mais lorsqu’ils sont utilisés pour d’autres effets impliquant plusieurs passes de rendu, l’application peut spécifier que seuls certains sous-échantillons doivent être affectés par une passe de rendu donnée.</span><span class="sxs-lookup"><span data-stu-id="b1bb7-108">When multisampling is enabled, all subsamples of a pixel are updated in one pass but when used for other effects that involve multiple rendering passes, the application can specify that only some subsamples are to be affected by a given rendering pass.</span></span> <span data-ttu-id="b1bb7-109">Cette dernière approche active la simulation de flou de mouvement, les effets de focus de niveau de champ de profondeur, le flou de la réflexion, et ainsi de suite.</span><span class="sxs-lookup"><span data-stu-id="b1bb7-109">This latter approach enables simulation of motion blur, depth-of-field focus effects, reflection blur, and so on.</span></span>

<span data-ttu-id="b1bb7-110">Dans les deux cas, les divers échantillons enregistrés pour chaque pixel sont fusionnés et générés à l’écran.</span><span class="sxs-lookup"><span data-stu-id="b1bb7-110">In both cases, the various samples recorded for each pixel are blended together and output to the screen.</span></span> <span data-ttu-id="b1bb7-111">Cela permet d’améliorer la qualité d’image de l’anticrénelage ou d’autres effets.</span><span class="sxs-lookup"><span data-stu-id="b1bb7-111">This enables the improved image quality of antialiasing or other effects.</span></span>

<span data-ttu-id="b1bb7-112">Avant de créer un appareil avec la méthode [**IDirect3D9 :: CreateDevice**](/windows/desktop/api) , vous devez déterminer si l’anticrénelage de scène intégrale est pris en charge.</span><span class="sxs-lookup"><span data-stu-id="b1bb7-112">Before creating a device with the [**IDirect3D9::CreateDevice**](/windows/desktop/api) method, you need to determine if full-scene antialiasing is supported.</span></span> <span data-ttu-id="b1bb7-113">Pour ce faire, appelez la méthode [**IDirect3D9 :: CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) comme indiqué dans l’exemple de code ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="b1bb7-113">Do this by calling the [**IDirect3D9::CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) method as shown in the code example below.</span></span>


```
/*
* The code below assumes that pD3D is a valid pointer 
*   to a IDirect3D9 interface.
*/

if( SUCCEEDED(pD3D->CheckDeviceMultiSampleType( D3DADAPTER_DEFAULT, 
                    D3DDEVTYPE_HAL , D3DFMT_R8G8B8, FALSE, 
                    D3DMULTISAMPLE_2_SAMPLES, NULL ) ) )
// Full-scene antialiasing is supported. Enable it here.
```



<span data-ttu-id="b1bb7-114">Le premier paramètre que [**IDirect3D9 :: CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) accepte est un nombre ordinal qui indique la carte d’affichage à interroger.</span><span class="sxs-lookup"><span data-stu-id="b1bb7-114">The first parameter that [**IDirect3D9::CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) accepts is an ordinal number that denotes the display adapter to query.</span></span> <span data-ttu-id="b1bb7-115">Cet exemple utilise \_ la valeur par défaut D3DADAPTER pour spécifier la carte d’affichage principale.</span><span class="sxs-lookup"><span data-stu-id="b1bb7-115">This sample uses D3DADAPTER\_DEFAULT to specify the primary display adapter.</span></span> <span data-ttu-id="b1bb7-116">Le deuxième paramètre est une valeur du type énuméré [**D3DDEVTYPE**](./d3ddevtype.md) , en spécifiant le type d’appareil.</span><span class="sxs-lookup"><span data-stu-id="b1bb7-116">The second parameter is a value from the [**D3DDEVTYPE**](./d3ddevtype.md) enumerated type, specifying the device type.</span></span> <span data-ttu-id="b1bb7-117">Le troisième paramètre spécifie le format de la surface.</span><span class="sxs-lookup"><span data-stu-id="b1bb7-117">The third parameter specifies the format of the surface.</span></span> <span data-ttu-id="b1bb7-118">Le quatrième paramètre indique à Direct3D s’il faut se renseigner sur l’échantillonnage multiple avec fenêtres entières (**true**) ou l’anticrénelage de scène complète (**false**).</span><span class="sxs-lookup"><span data-stu-id="b1bb7-118">The fourth parameter tells Direct3D whether to inquire about full-windowed multisampling (**TRUE**) or full-scene antialiasing (**FALSE**).</span></span> <span data-ttu-id="b1bb7-119">Cet exemple utilise la **valeur false** pour indiquer à Direct3D qu’il s’interroge sur l’anticrénelage de scène complète.</span><span class="sxs-lookup"><span data-stu-id="b1bb7-119">This sample uses **FALSE** to tell Direct3D that it is inquiring about full-scene antialiasing.</span></span> <span data-ttu-id="b1bb7-120">Le dernier paramètre spécifie la technique d’échantillonnage multiple que vous souhaitez tester.</span><span class="sxs-lookup"><span data-stu-id="b1bb7-120">The last parameter specifies the multisampling technique that you want to test.</span></span> <span data-ttu-id="b1bb7-121">Utilisez une valeur du type [**énuméré \_ D3DMULTISAMPLE**](./d3dmultisample-type.md) .</span><span class="sxs-lookup"><span data-stu-id="b1bb7-121">Use a value from the [**D3DMULTISAMPLE\_TYPE**](./d3dmultisample-type.md) enumerated type.</span></span> <span data-ttu-id="b1bb7-122">Cet exemple vérifie si deux niveaux d’échantillonnage multiple sont pris en charge.</span><span class="sxs-lookup"><span data-stu-id="b1bb7-122">This sample tests to see if two levels of multisampling are supported.</span></span>

<span data-ttu-id="b1bb7-123">Si l’appareil prend en charge le niveau d’échantillonnage multiple que vous souhaitez utiliser, l’étape suivante consiste à définir les paramètres de présentation en remplissant les membres appropriés de la structure de [**\_ paramètres D3DPRESENT**](d3dpresent-parameters.md) pour créer une surface de rendu à échantillonnage multiple.</span><span class="sxs-lookup"><span data-stu-id="b1bb7-123">If the device supports the level of multisampling that you want to use, the next step is to set the presentation parameters by filling in the appropriate members of the [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md) structure to create a multisample rendering surface.</span></span> <span data-ttu-id="b1bb7-124">Après cela, vous pouvez créer l’appareil.</span><span class="sxs-lookup"><span data-stu-id="b1bb7-124">After that, you can create the device.</span></span> <span data-ttu-id="b1bb7-125">L’exemple de code ci-dessous montre comment configurer un appareil avec une surface de rendu d’échantillonnage multiple.</span><span class="sxs-lookup"><span data-stu-id="b1bb7-125">The sample code below shows how to set up a device with a multisampling render surface.</span></span>


```
/*
* The example below assumes that pD3D is a valid pointer 
* to a IDirect3D9 interface, d3dDevice is a pointer to a 
* IDirect3DDevice9 interface, and hWnd is a valid handle
* to a window.
*/

D3DPRESENT_PARAMETER d3dPP
ZeroMemory( &d3dPP, sizeof( d3dPP ) );
d3dPP.Windowed        = FALSE
d3dPP.SwapEffect      = D3DSWAPEFFECT_DISCARD;
d3dPP.MultiSampleType = D3DMULTISAMPLE_2_SAMPLES;
pD3D->CreateDevice(D3DADAPTER_DEFAULT, D3DDEVTYPE_HAL, hWnd,
                    D3DCREATE_SOFTWARE_VERTEXPROCESSING,
                    &d3dpp, &d3dDevice)
```



<span data-ttu-id="b1bb7-126">Pour utiliser l’échantillonnage multiple, le membre SwapEffect du \_ paramètre D3DPRESENT doit avoir la valeur D3DSWAPEFFECT \_ Discard.</span><span class="sxs-lookup"><span data-stu-id="b1bb7-126">To use multisampling, the SwapEffect member of D3DPRESENT\_PARAMETER must be set to D3DSWAPEFFECT\_DISCARD.</span></span>

<span data-ttu-id="b1bb7-127">La dernière étape consiste à activer l’anticrénelage d’échantillonnage multiple en appelant la méthode [**IDirect3DDevice9 :: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) et en affectant \_ à D3DRS MULTISAMPLEANTIALIAS la **valeur true**.</span><span class="sxs-lookup"><span data-stu-id="b1bb7-127">The last step is to enable multisampling antialiasing by calling the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method and setting the D3DRS\_MULTISAMPLEANTIALIAS to **TRUE**.</span></span> <span data-ttu-id="b1bb7-128">Une fois cette valeur définie sur **true**, l’échantillonnage est appliqué à tous les rendus.</span><span class="sxs-lookup"><span data-stu-id="b1bb7-128">After setting this value to **TRUE**, any rendering that you do will have multisampling applied to it.</span></span> <span data-ttu-id="b1bb7-129">Vous pouvez activer et désactiver l’échantillonnage multiple, en fonction de ce que vous rendez.</span><span class="sxs-lookup"><span data-stu-id="b1bb7-129">You might want to enable and disable multisampling, depending on what you are rendering.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b1bb7-130">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="b1bb7-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1bb7-131">Anticrénelage</span><span class="sxs-lookup"><span data-stu-id="b1bb7-131">Antialiasing</span></span>](antialiasing.md)
</dt> </dl>

 

 
