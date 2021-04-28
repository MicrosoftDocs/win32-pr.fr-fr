---
description: La règle générale est qu’une application de bureau peut appeler une API Windows Runtime (WinRT). Toutefois, certaines API, y compris les API d’interface utilisateur XAML, requièrent que l’application appelante ait une identité de package.
ms.assetid: F3808C28-72DE-49B5-A389-EB085EFC02CC
title: API WinRT pouvant être appelées à partir d’une application de bureau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36f99cca14c066f372ad7fd417e04137a62ae628
ms.sourcegitcommit: 133954d5dbcd5b2b3b50c8efd16cd101278fc1db
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108172481"
---
# <a name="winrt-apis-callable-from-a-desktop-app"></a><span data-ttu-id="baa80-104">API WinRT pouvant être appelées à partir d’une application de bureau</span><span class="sxs-lookup"><span data-stu-id="baa80-104">WinRT APIs callable from a desktop app</span></span>

<span data-ttu-id="baa80-105">La plupart des [api Windows Runtime (WinRT)](/uwp/api/) peuvent être utilisées par les applications de bureau (.net et C++).</span><span class="sxs-lookup"><span data-stu-id="baa80-105">Most [Windows Runtime (WinRT) APIs](/uwp/api/) can be used by desktop (.NET and native C++) apps.</span></span> <span data-ttu-id="baa80-106">Toutefois, certaines classes WinRT sont conçues pour et sont uniquement prises en charge pour une utilisation dans les applications UWP.</span><span class="sxs-lookup"><span data-stu-id="baa80-106">However, some WinRT classes are designed for and are only supported for use in UWP apps.</span></span> <span data-ttu-id="baa80-107">Cela comprend [CoreDispatcher](/uwp/api/Windows.UI.Core.CoreDispatcher), [CoreWindow](/uwp/api/Windows.UI.Core.CoreWindow), [ApplicationView](/uwp/api/windows.ui.viewmanagement.applicationview)et certaines classes associées.</span><span class="sxs-lookup"><span data-stu-id="baa80-107">This includes [CoreDispatcher](/uwp/api/Windows.UI.Core.CoreDispatcher), [CoreWindow](/uwp/api/Windows.UI.Core.CoreWindow), [ApplicationView](/uwp/api/windows.ui.viewmanagement.applicationview), and some related classes.</span></span> <span data-ttu-id="baa80-108">D’autres classes WinRT fonctionnent dans les applications de bureau, à l’exception des membres spécifiques.</span><span class="sxs-lookup"><span data-stu-id="baa80-108">Other WinRT classes work in desktop apps except for specific members.</span></span>

<span data-ttu-id="baa80-109">Pour plus d’informations, consultez [Windows Runtime API non prises en charge dans les applications de bureau](/windows/apps/desktop/modernize/desktop-to-uwp-supported-api).</span><span class="sxs-lookup"><span data-stu-id="baa80-109">For more information, see [Windows Runtime APIs not supported in desktop apps](/windows/apps/desktop/modernize/desktop-to-uwp-supported-api).</span></span> <span data-ttu-id="baa80-110">Le cas échéant, cet article suggère d’autres API pour obtenir les mêmes fonctionnalités que les API non prises en charge.</span><span class="sxs-lookup"><span data-stu-id="baa80-110">Where available, this article suggests alternative APIs to achieve the same functionality as the unsupported APIs.</span></span>
