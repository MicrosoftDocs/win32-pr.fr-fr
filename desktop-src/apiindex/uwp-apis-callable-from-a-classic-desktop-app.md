---
description: la règle générale est qu’une application de bureau peut appeler une API Windows Runtime (WinRT). Toutefois, certaines API, y compris les API d’interface utilisateur XAML, requièrent que l’application appelante ait une identité de package.
ms.assetid: F3808C28-72DE-49B5-A389-EB085EFC02CC
title: API WinRT pouvant être appelées à partir d’une application de bureau
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3bbfb2316a6fd4dd8d35d0744acc4ad301dba7f42aee36ee865d67bb2fff805
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119130301"
---
# <a name="winrt-apis-callable-from-a-desktop-app"></a>API WinRT pouvant être appelées à partir d’une application de bureau

la plupart des [api Windows Runtime (WinRT)](/uwp/api/) peuvent être utilisées par les applications de bureau (.net et C++). Toutefois, certaines classes WinRT sont conçues pour et sont uniquement prises en charge pour une utilisation dans les applications UWP. Cela comprend [CoreDispatcher](/uwp/api/Windows.UI.Core.CoreDispatcher), [CoreWindow](/uwp/api/Windows.UI.Core.CoreWindow), [ApplicationView](/uwp/api/windows.ui.viewmanagement.applicationview)et certaines classes associées. D’autres classes WinRT fonctionnent dans les applications de bureau, à l’exception de certains membres.

Pour plus d’informations, consultez [API Windows Runtime non prises en charge dans les applications de bureau](/windows/apps/desktop/modernize/desktop-to-uwp-supported-api). Lorsque cela s’applique, cet article suggère d’autres API qui permettent d’obtenir les mêmes fonctionnalités que les API non prises en charge.
