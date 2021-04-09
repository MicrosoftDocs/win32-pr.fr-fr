---
description: .
ms.assetid: 49E0D0C2-E6EC-4849-A44F-36FDEFBB9838
title: Prise en main de DirectX Graphics
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5278e759ea0faf04ac8b247ad3ea1c687dd205c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034598"
---
# <a name="getting-started-with-directx-graphics"></a><span data-ttu-id="af45f-103">Prise en main de DirectX Graphics</span><span class="sxs-lookup"><span data-stu-id="af45f-103">Getting started with DirectX Graphics</span></span>

<span data-ttu-id="af45f-104">Microsoft DirectX Graphics fournit un ensemble d’API que vous pouvez utiliser pour créer des jeux et d’autres applications multimédias à hautes performances.</span><span class="sxs-lookup"><span data-stu-id="af45f-104">Microsoft DirectX graphics provides a set of APIs that you can use to create games and other high-performance multimedia applications.</span></span> <span data-ttu-id="af45f-105">DirectX Graphics prend en charge les graphiques 3D et 2D haute performance.</span><span class="sxs-lookup"><span data-stu-id="af45f-105">DirectX graphics includes support for high-performance 2-D and 3-D graphics.</span></span>

<span data-ttu-id="af45f-106">Pour les graphiques 3D, utilisez l’API Microsoft Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="af45f-106">For 3-D graphics, use the Microsoft Direct3D 11 API.</span></span> <span data-ttu-id="af45f-107">Même si vous disposez d’un matériel Microsoft Direct3D 9 ou Microsoft Direct3D 10, vous pouvez utiliser l’API Direct3D 11 et cibler un appareil de niveau de [fonctionnalité](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9 \_ x ou de fonctionnalité de niveau de fonctionnalité 10 \_ x.</span><span class="sxs-lookup"><span data-stu-id="af45f-107">Even if you have Microsoft Direct3D 9-level or Microsoft Direct3D 10-level hardware, you can use the Direct3D 11 API and target a [feature level](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9\_x or feature level 10\_x device.</span></span> <span data-ttu-id="af45f-108">Pour plus d’informations sur le développement de graphiques 3D avec DirectX, consultez [créer des graphiques 3D avec DirectX](/previous-versions/windows/apps/hh465137(v=win.10)
).</span><span class="sxs-lookup"><span data-stu-id="af45f-108">For info about how to develop 3-D graphics with DirectX, see [Create 3D graphics with DirectX](/previous-versions/windows/apps/hh465137(v=win.10)
).</span></span>

<span data-ttu-id="af45f-109">Pour les graphiques 2D et le texte, utilisez Direct2D et [DirectWrite](./directwrite/direct-write-portal.md) plutôt que Windows Graphics Device Interface (GDI).</span><span class="sxs-lookup"><span data-stu-id="af45f-109">For 2-D graphics and text, use Direct2D and [DirectWrite](./directwrite/direct-write-portal.md) rather than Windows Graphics Device Interface (GDI).</span></span>

<span data-ttu-id="af45f-110">Pour composer des bitmaps alimentées par Direct3D 11 ou Direct2D, utilisez [DirectComposition](./directcomp/directcomposition-portal.md).</span><span class="sxs-lookup"><span data-stu-id="af45f-110">To compose bitmaps that Direct3D 11 or Direct2D populated, use [DirectComposition](./directcomp/directcomposition-portal.md).</span></span>

<span data-ttu-id="af45f-111">Pour en savoir plus sur la création d’une application du Windows Store qui utilise DirectX, consultez [créer votre première application du Windows Store à l’aide de DirectX](/previous-versions/windows/apps/br229580(v=win.10)
).</span><span class="sxs-lookup"><span data-stu-id="af45f-111">To learn about how to create a Windows Store app that uses DirectX, see [Create your first Windows Store app using DirectX](/previous-versions/windows/apps/br229580(v=win.10)
).</span></span> <span data-ttu-id="af45f-112">Vous pouvez utiliser la classe [**Windows. UI :: XAML :: Controls :: SwapChainPanel**](/uwp/api/Windows.UI.Xaml.Controls.SwapChainPanel?view=winrt-19041) pour créer des applications DirectX haute performance avec une superposition de l’interface utilisateur XAML.</span><span class="sxs-lookup"><span data-stu-id="af45f-112">You can use the [**Windows.UI::Xaml::Controls::SwapChainPanel**](/uwp/api/Windows.UI.Xaml.Controls.SwapChainPanel?view=winrt-19041) class to create high-performance DirectX apps with a XAML UI overlay.</span></span> <span data-ttu-id="af45f-113">Pour plus d’informations sur la combinaison de code XAML et DirectX dans une application Windows, consultez [DirectX and XAML Interop](/previous-versions/windows/apps/hh825871(v=win.10)).</span><span class="sxs-lookup"><span data-stu-id="af45f-113">For more info about combining XAML and DirectX in a Windows app, see [DirectX and XAML interop](/previous-versions/windows/apps/hh825871(v=win.10)).</span></span>

<span data-ttu-id="af45f-114">Pour en savoir plus sur la création d’un pilote d’affichage pour Windows 8, consultez feuille [de route pour le modèle WDDM (Windows Display Driver Model)](/windows-hardware/drivers/display/roadmap-for-developing-drivers-for-the-windows-vista-display-driver-mo).</span><span class="sxs-lookup"><span data-stu-id="af45f-114">To learn about how to build a display driver for Windows 8, see [Roadmap for the Windows Display Driver Model (WDDM)](/windows-hardware/drivers/display/roadmap-for-developing-drivers-for-the-windows-vista-display-driver-mo).</span></span>

<span data-ttu-id="af45f-115">Si vous avez besoin de la documentation pour les versions précédentes de DirectX, consultez [Graphics DirectX Classic](/windows/desktop/classic-directx-graphics).</span><span class="sxs-lookup"><span data-stu-id="af45f-115">If you need the documentation for previous DirectX versions, see [Classic DirectX Graphics](/windows/desktop/classic-directx-graphics).</span></span>


 

 
