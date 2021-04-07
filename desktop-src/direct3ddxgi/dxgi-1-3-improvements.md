---
description: Les fonctionnalités suivantes ont été ajoutées dans Microsoft DirectX Graphics infrastructure (DXGI) 1,3, qui est inclus à partir de Windows 8.1.
ms.assetid: 56816212-2B6A-41EC-B57D-29DEBBF440E7
title: Améliorations de DXGI 1,3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c863bc30ffdf27705492b56a5348040c8e12f4fa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846045"
---
# <a name="dxgi-13-improvements"></a>Améliorations de DXGI 1,3

Les fonctionnalités suivantes ont été ajoutées dans Microsoft DirectX Graphics infrastructure (DXGI) 1,3, qui est inclus à partir de Windows 8.1.

## <a name="trim-dxgi-adapter-memory-usage"></a>Ajuster l’utilisation de la mémoire de l’adaptateur DXGI

À partir de Windows 8.1, DXGI 1,3 ajoute la possibilité de vider et de libérer les ressources mémoire inutilisées allouées par l’adaptateur DXGI. Cela permet aux applications de libérer de la mémoire temporaire pendant la suspension, ce qui réduit le risque d’arrêt de l’application afin de libérer des ressources pour d’autres applications. Lorsque l’application reprend, les pilotes de périphérique qui prennent en charge la fonction Trim recréent les ressources dès qu’elles sont nécessaires. À partir de Windows 8.1, tous les périphériques Direct3D créés par une application doivent appeler [**IDXGIDevice3 :: Trim**](/windows/desktop/api/DXGI1_3/nf-dxgi1_3-idxgidevice3-trim) lors de la suspension pour réduire l’encombrement mémoire et réduire le risque que l’application se termine pour récupérer des ressources système.

## <a name="multi-plane-overlays"></a>Superpositions à plusieurs plans

À partir de Windows 8.1, DXGI 1,3 prend en charge les superpositions à plusieurs plans. Vous pouvez déterminer si l’appareil prend en charge les superpositions à plusieurs plans dans le matériel à l’aide de [**IDXGIOutput2 :: SupportsOverlays**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgioutput2-supportsoverlays).

## <a name="overlapping-swap-chains-and-swap-chain-scaling"></a>Chaînes d’échange se chevauchant et mise à l’échelle de la chaîne de permutation

À partir de Windows 8.1, DXGI 1,3 prend en charge les chaînes de permutation qui se chevauchent. Les chaînes de permutation qui se chevauchent sont utilisées pour dessiner des graphiques 3D à des résolutions non natives (avec mise à l’échelle du matériel) tout en présentant l’interface utilisateur à la résolution native. Cela permet aux jeux de tirer parti des taux de remplissage plus élevés pour le jeu réactif sans dégrader la qualité visuelle des éléments d’interface utilisateur, tels que le score du joueur et le texte de la boîte de dialogue. Sur les appareils qui prennent en charge les superpositions à plusieurs plans, Direct3D utilise des superpositions à plusieurs plans pour le chevauchement des chaînes de permutation. Créez une chaîne de permutation de premier plan en spécifiant l’indicateur de [**chaîne de permutation dxgi indicateur de \_ \_ \_ \_ \_ couche de premier plan**](/windows/win32/api/dxgi/ne-dxgi-dxgi_swap_chain_flag) lors de la création de la chaîne de permutation, puis utilisez [**IDXGISwapChain2 :: SetMatrixTransform**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-setmatrixtransform) et [**IDXGISwapChain2 :: GetMatrixTransform**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-getmatrixtransform) pour mettre à l’échelle la chaîne de permutation utilisée pour le jeu.

## <a name="select-backbuffer-subregion-for-swap-chain"></a>Sélectionner la sous-région de mémoire tampon pour la chaîne de permutation

À partir de Windows 8.1, DXGI 1,3 peut être utilisé pour sélectionner une sous-région de la mémoire tampon d’arrière-plan à utiliser avec la chaîne de permutation, ce qui permet un rendu à une mémoire tampon d’arrière-plan plus petite sans recréer la chaîne de permutation. Consultez [**IDXGISwapChain2 :: SetSourceSize**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-setsourcesize) et [**IDXGISwapChain2 :: GetSourceSize**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-getsourcesize).

## <a name="lower-latency-swap-chain-presentation"></a>Présentation de la chaîne de permutation à latence faible

À partir de Windows 8.1, DXGI 1,3 permet de réduire la latence en laissant à la chaîne de permutation la possibilité de présenter le frame précédent avant de commencer à utiliser l’appareil pour dessiner le frame suivant. Consultez [**IDXGISwapChain2 :: GetFrameLatencyWaitableObject**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-getframelatencywaitableobject), [**IDXGISwapChain2 :: GetMaximumFrameLatency**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-getmaximumframelatency)et [**IDXGISwapChain2 :: SetMaximumFrameLatency**](/windows/desktop/api/dxgi1_3/nf-dxgi1_3-idxgiswapchain2-setmaximumframelatency).

## <a name="related-topics"></a>Rubriques connexes

[Guide de programmation pour DXGI](dx-graphics-dxgi-overviews.md)
