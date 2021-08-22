---
description: Prise en main de DirectX Graphics
ms.assetid: 49E0D0C2-E6EC-4849-A44F-36FDEFBB9838
title: Prise en main de DirectX Graphics
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32e0bc8a3485091ec8b8fa53c8245a3a4916e11af96493d4895585061f2b080f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830569"
---
# <a name="getting-started-with-directx-graphics"></a>Prise en main de DirectX Graphics

Microsoft DirectX Graphics fournit un ensemble d’API que vous pouvez utiliser pour créer des jeux et d’autres applications multimédias à hautes performances. DirectX Graphics prend en charge les graphiques 3D et 2D haute performance.

Pour les graphiques 3D, utilisez l’API Microsoft Direct3D 11. Même si vous disposez d’un matériel Microsoft Direct3D 9 ou Microsoft Direct3D 10, vous pouvez utiliser l’API Direct3D 11 et cibler un appareil de niveau de [fonctionnalité](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x ou de fonctionnalité de niveau de fonctionnalité 10 \_ x. Pour plus d’informations sur le développement de graphiques 3D avec DirectX, consultez [créer des graphiques 3D avec DirectX](/previous-versions/windows/apps/hh465137(v=win.10)
).

pour les graphiques 2d et le texte, utilisez Direct2D et [DirectWrite](./directwrite/direct-write-portal.md) plutôt que Windows Graphics Device Interface (GDI).

Pour composer des bitmaps alimentées par Direct3D 11 ou Direct2D, utilisez [DirectComposition](./directcomp/directcomposition-portal.md).

pour en savoir plus sur la création d’une application Windows store qui utilise directx, consultez [créer votre première application Windows store à l’aide de directx](/previous-versions/windows/apps/br229580(v=win.10)
). Vous pouvez utiliser la [**Windows. UI :: XAML :: Controls :: SwapChainPanel**](/uwp/api/Windows.UI.Xaml.Controls.SwapChainPanel?view=winrt-19041) pour créer des applications DirectX haute performance avec une superposition d’interface utilisateur XAML. pour plus d’informations sur la combinaison de code XAML et directx dans une application Windows, consultez [DirectX and XAML interop](/previous-versions/windows/apps/hh825871(v=win.10)).

pour en savoir plus sur la création d’un pilote d’affichage pour Windows 8, consultez feuille [de route pour le modèle WDDM (Windows display driver Model)](/windows-hardware/drivers/display/roadmap-for-developing-drivers-for-the-windows-vista-display-driver-mo).

Si vous avez besoin de la documentation pour les versions précédentes de DirectX, consultez [Graphics DirectX Classic](/windows/desktop/classic-directx-graphics).


 

 
