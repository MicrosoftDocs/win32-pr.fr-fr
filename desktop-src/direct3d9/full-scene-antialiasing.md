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
# <a name="full-scene-antialiasing-direct3d-9"></a>Anticrénelage de Full-Scene (Direct3D 9)

L’anticrénelage de scène entière fait référence à l’atténuation des bords de chaque polygone dans la scène au fur et à mesure qu’il est pixellisé en une seule passe. aucune deuxième passe n’est nécessaire. L’anticrénelage de scène entière, lorsqu’il est pris en charge, affecte uniquement les triangles et les groupes de triangles. Les lignes ne peuvent pas être antialiasées à l’aide des services Direct3D. L’anticrénelage de scène entière est effectué dans Direct3D en utilisant l’échantillonnage multiple sur chaque pixel. Lorsque l’échantillonnage multiple est activé, tous les sous-échantillons d’un pixel sont mis à jour en une seule passe, mais lorsqu’ils sont utilisés pour d’autres effets impliquant plusieurs passes de rendu, l’application peut spécifier que seuls certains sous-échantillons doivent être affectés par une passe de rendu donnée. Cette dernière approche active la simulation de flou de mouvement, les effets de focus de niveau de champ de profondeur, le flou de la réflexion, et ainsi de suite.

Dans les deux cas, les divers échantillons enregistrés pour chaque pixel sont fusionnés et générés à l’écran. Cela permet d’améliorer la qualité d’image de l’anticrénelage ou d’autres effets.

Avant de créer un appareil avec la méthode [**IDirect3D9 :: CreateDevice**](/windows/desktop/api) , vous devez déterminer si l’anticrénelage de scène intégrale est pris en charge. Pour ce faire, appelez la méthode [**IDirect3D9 :: CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) comme indiqué dans l’exemple de code ci-dessous.


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



Le premier paramètre que [**IDirect3D9 :: CheckDeviceMultiSampleType**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-checkdevicemultisampletype) accepte est un nombre ordinal qui indique la carte d’affichage à interroger. Cet exemple utilise \_ la valeur par défaut D3DADAPTER pour spécifier la carte d’affichage principale. Le deuxième paramètre est une valeur du type énuméré [**D3DDEVTYPE**](./d3ddevtype.md) , en spécifiant le type d’appareil. Le troisième paramètre spécifie le format de la surface. Le quatrième paramètre indique à Direct3D s’il faut se renseigner sur l’échantillonnage multiple avec fenêtres entières (**true**) ou l’anticrénelage de scène complète (**false**). Cet exemple utilise la **valeur false** pour indiquer à Direct3D qu’il s’interroge sur l’anticrénelage de scène complète. Le dernier paramètre spécifie la technique d’échantillonnage multiple que vous souhaitez tester. Utilisez une valeur du type [**énuméré \_ D3DMULTISAMPLE**](./d3dmultisample-type.md) . Cet exemple vérifie si deux niveaux d’échantillonnage multiple sont pris en charge.

Si l’appareil prend en charge le niveau d’échantillonnage multiple que vous souhaitez utiliser, l’étape suivante consiste à définir les paramètres de présentation en remplissant les membres appropriés de la structure de [**\_ paramètres D3DPRESENT**](d3dpresent-parameters.md) pour créer une surface de rendu à échantillonnage multiple. Après cela, vous pouvez créer l’appareil. L’exemple de code ci-dessous montre comment configurer un appareil avec une surface de rendu d’échantillonnage multiple.


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



Pour utiliser l’échantillonnage multiple, le membre SwapEffect du \_ paramètre D3DPRESENT doit avoir la valeur D3DSWAPEFFECT \_ Discard.

La dernière étape consiste à activer l’anticrénelage d’échantillonnage multiple en appelant la méthode [**IDirect3DDevice9 :: SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) et en affectant \_ à D3DRS MULTISAMPLEANTIALIAS la **valeur true**. Une fois cette valeur définie sur **true**, l’échantillonnage est appliqué à tous les rendus. Vous pouvez activer et désactiver l’échantillonnage multiple, en fonction de ce que vous rendez.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Anticrénelage](antialiasing.md)
</dt> </dl>

 

 
