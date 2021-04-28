---
description: Prise en main de DirectX Graphics
ms.assetid: 49E0D0C2-E6EC-4849-A44F-36FDEFBB9838
title: Prise en main de DirectX Graphics
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7c5e8cca9f0cea4c1c5e484ba330c7c108cad40
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117587"
---
# <a name="getting-started-with-directx-graphics"></a>Prise en main de DirectX Graphics

Microsoft DirectX Graphics fournit un ensemble d’API que vous pouvez utiliser pour créer des jeux et d’autres applications multimédias à hautes performances. DirectX Graphics prend en charge les graphiques 3D et 2D haute performance.

Pour les graphiques 3D, utilisez l’API Microsoft Direct3D 11. Même si vous disposez d’un matériel Microsoft Direct3D 9 ou Microsoft Direct3D 10, vous pouvez utiliser l’API Direct3D 11 et cibler un appareil de niveau de [fonctionnalité](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x ou de fonctionnalité de niveau de fonctionnalité 10 \_ x. Pour plus d’informations sur le développement de graphiques 3D avec DirectX, consultez [créer des graphiques 3D avec DirectX](/previous-versions/windows/apps/hh465137(v=win.10)
).

Pour les graphiques 2D et le texte, utilisez Direct2D et [DirectWrite](./directwrite/direct-write-portal.md) plutôt que Windows Graphics Device Interface (GDI).

Pour composer des bitmaps alimentées par Direct3D 11 ou Direct2D, utilisez [DirectComposition](./directcomp/directcomposition-portal.md).

Pour en savoir plus sur la création d’une application du Windows Store qui utilise DirectX, consultez [créer votre première application du Windows Store à l’aide de DirectX](/previous-versions/windows/apps/br229580(v=win.10)
). Vous pouvez utiliser la classe [**Windows. UI :: XAML :: Controls :: SwapChainPanel**](/uwp/api/Windows.UI.Xaml.Controls.SwapChainPanel?view=winrt-19041) pour créer des applications DirectX haute performance avec une superposition de l’interface utilisateur XAML. Pour plus d’informations sur la combinaison de code XAML et DirectX dans une application Windows, consultez [DirectX and XAML Interop](/previous-versions/windows/apps/hh825871(v=win.10)).

Pour en savoir plus sur la création d’un pilote d’affichage pour Windows 8, consultez feuille [de route pour le modèle WDDM (Windows Display Driver Model)](/windows-hardware/drivers/display/roadmap-for-developing-drivers-for-the-windows-vista-display-driver-mo).

Si vous avez besoin de la documentation pour les versions précédentes de DirectX, consultez [Graphics DirectX Classic](/windows/desktop/classic-directx-graphics).


 

 
