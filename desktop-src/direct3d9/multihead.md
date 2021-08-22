---
description: Les cartes multitête sont celles qui ont une mémoire tampon de frame et un accélérateur communs, des convertisseurs numériques-analogiques (DAC) indépendants et des sorties de surveillance.
ms.assetid: f741cdb4-2eb6-42e9-81ea-a8c677e07582
title: Multitête (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04a74f51cea282618c9471eb9a63eedf8eef73c38b4d961209064261a93c4d46
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119563513"
---
# <a name="multihead-direct3d-9"></a>Multitête (Direct3D 9)

Les cartes multitête sont celles qui ont une mémoire tampon de frame et un accélérateur communs, des convertisseurs numériques-analogiques (DAC) indépendants et des sorties de surveillance. Ces appareils peuvent offrir une prise en charge de plusieurs moniteurs plus utilisable qu’un nombre similaire de cartes d’affichage hétérogènes.

Les cartes multitêtes sont exposées dans l’API en tant qu’appareil unique au niveau de l’API qui peut générer plusieurs chaînes de permutation plein écran. Par conséquent, toutes les ressources sont partagées avec tous les en-têtes, et chaque tête a exactement les mêmes fonctionnalités. Chaque tête peut être définie en mode d’affichage indépendant. Vous pouvez utiliser des appels distincts à [**IDirect3DSwapChain9 ::P renvoyés**](/windows/desktop/api) pour actualiser chaque tête. Vous pouvez également utiliser un appel à [**IDirect3DDevice9 ::P renvoyé**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) pour actualiser chaque tête de manière séquentielle.

> [!Note]  
> L’actualisation de chaque tête ne se produit pas simultanément avec un seul appel à [**IDirect3DDevice9 ::P renvoyé**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present). Les statistiques présentes dans Direct3D 9Ex peuvent utiliser la structure [**D3DPRESENTSTATS**](d3dpresentstats.md) pour conserver les actualisations de chaque tête près les unes des autres afin de limiter les effets de déchirage sur plusieurs têtes de cartes. Pour plus d’informations sur la synchronisation des frames des applications Direct3D 9Ex Flip Model, consultez [améliorations de Direct3D 9Ex](../direct3darticles/direct3d-9ex-improvements.md).

 

Chaque chaîne de permutation pour un appareil multitête doit être en mode plein écran. Quand un appareil est entré en mode multitête, il doit rester en mode plein écran. La transition vers le mode avec fenêtres nécessite la destruction de l’appareil (à l’exception de l’opération ALT normale + TAB-to-Minimize).

L’ancienne méthode de division de la mémoire vidéo entre les têtes et le traitement de chaque tête en tant qu’accélérateur entièrement indépendant sera toujours un scénario d’utilisation courant. Cette proposition ne remplace pas ce mécanisme, sauf si l’application a été spécifiquement codée pour fonctionner en mode multitête Direct3D 9.

Les pilotes disposent d’une connaissance adéquate pour basculer entre les deux modes de fonctionnement.

L’une des têtes est appelée tête principale et toutes les autres têtes sur la même carte sont appelées têtes subordonnées. Si plus d’un adaptateur multitête est présent dans un système, le maître et ses subordonnés d’un adaptateur multitête sont appelés groupes. Les groupes sont dénotés par l’ordinal d’adaptateur de leur en-tête maître.

La structure [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) a été mise à jour pour exposer les nouvelles extrémités matérielles suivantes.


```
UINT NumberOfAdaptersInGroup; 
UINT MasterAdapterOrdinal; 
UINT AdapterOrdinalInGroup;
```



-   NumberOfAdaptersInGroup est égal à 1 pour les adaptateurs conventionnels et supérieur à 1 pour la carte maîtresse d’une carte multitête. La valeur sera 0 pour un adaptateur subordonné d’une carte multitête. Chaque carte peut avoir au plus une base de référence, mais elle peut avoir de nombreux subordonnés.
-   MasterAdapterOrdinal indique quel appareil est le maître de ce subordonné.
-   AdapterOrdinalInGroup indique l’ordre dans lequel les têtes sont référencées par l’API. L’adaptateur maître a toujours le AdapterOrdinalInGroup 0. Ces valeurs ne correspondent pas aux ordinaux des adaptateurs passés aux méthodes IDirect3D9, mais s’appliquent uniquement aux têtes d’un groupe.

Cette définition permet aux cartes multitête de continuer à présenter plusieurs adaptateurs comme s’il s’agissait de cartes indépendantes, comme c’était le cas dans DirectX 8.

Pour créer un périphérique multitête, spécifiez l’indicateur de comportement D3DCREATE \_ ADAPTERGROUP \_ Device dans [**IDirect3D9 :: CreateDevice**](/windows/desktop/api). Les paramètres de présentation (un tableau [**de \_ paramètres D3DPRESENT**](d3dpresent-parameters.md)) doivent contenir des éléments NumberOfAdaptersInGroup. Le runtime assignera chaque élément à chaque tête dans l’ordre numérique AdapterOrdinalInGroup. Lorsque l' \_ appareil D3DCREATE ADAPTERGROUP \_ est défini, chaque paramètre de présentation doit avoir :

-   Le membre avec fenêtres a la valeur **false** (en d’autres termes, en mode plein écran).
-   La même valeur pour le membre EnableAutoDepthStencil des [**\_ paramètres D3DPRESENT**](d3dpresent-parameters.md).

En outre, si EnableAutoDepthStencil a la valeur **true**, chacun des champs suivants doit avoir la même valeur pour chaque [**\_ paramètre D3DPRESENT**](d3dpresent-parameters.md):

-   AutoDepthStencilFormat
-   BackBufferWidth
-   BackBufferHeight
-   BackBufferFormat

Si la DAC est définie, les appels supplémentaires à [**IDirect3DDevice9 :: CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) ne sont pas conformes.

Si l’appareil a été créé avec la DAC, [**IDirect3DDevice9 :: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) attend un tableau de [**\_ paramètres D3DPRESENT**](d3dpresent-parameters.md).

Chaque structure de [**\_ paramètres D3DPRESENT**](d3dpresent-parameters.md) transmise à [**IDirect3DDevice9 :: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) doit être en mode plein écran. Pour revenir au mode fenêtre, l’application doit détruire l’appareil et recréer un appareil non-en-tête en mode fenêtre.

Voici un scénario d’utilisation de base :


```
1. Create multihead device 
2. For each swap chain of device:
   3. Call GetBackBuffer for the i-th swapchain
   4. Call SetRenderTarget 
   5. Call DrawPrimitive 
   6. Optionally call swapchain::Present (or wait until 
all swap chains are drawn and present outside of loop)
7. End the for loop
8. Optionally present all swap chains with device::Present
```



Pour plus d’informations, consultez [**IDirect3D9 :: CreateDevice**](/windows/desktop/api) et [**IDirect3DDevice9 :: GetNumberOfSwapChains**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getnumberofswapchains).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Astuces de programmation](programming-tips.md)
</dt> </dl>

 

 
