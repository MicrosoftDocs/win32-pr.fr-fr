---
title: Types de prise en charge de IAccessible
description: Types de prise en charge de IAccessible
ms.assetid: 4a61d9a4-3c05-4f12-bdf1-426223b679b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fb2cb3d25e4cf95cc1ad790c77ffe66e02efda2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673325"
---
# <a name="types-of-iaccessible-support"></a><span data-ttu-id="647f0-103">Types de prise en charge de IAccessible</span><span class="sxs-lookup"><span data-stu-id="647f0-103">Types of IAccessible Support</span></span>

<span data-ttu-id="647f0-104">Les serveurs Microsoft Active Accessibility ont deux types de prise en charge de [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) : natif et proxy.</span><span class="sxs-lookup"><span data-stu-id="647f0-104">Microsoft Active Accessibility servers have two types of [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) support: native and proxied.</span></span> <span data-ttu-id="647f0-105">Les éléments d’interface utilisateur utilisés dans une application déterminent le type de prise en charge approprié.</span><span class="sxs-lookup"><span data-stu-id="647f0-105">The UI elements used in an application determine which type of support is appropriate.</span></span> <span data-ttu-id="647f0-106">De nombreux serveurs écrits aujourd’hui tirent pleinement parti des proxies et implémentent uniquement **IAccessible** pour les contrôles qui ne sont pas proxyés **par des Oleacc.dll** , tels que les contrôles ou les contrôles sans fenêtre avec un nom de classe de fenêtre personnalisé.</span><span class="sxs-lookup"><span data-stu-id="647f0-106">Many servers being written today take full advantage of **IAccessible** proxies and only implement **IAccessible** for those controls that are not proxied by Oleacc.dll, such as windowless controls or controls with a custom window class name.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="647f0-107">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="647f0-107">In this section</span></span>

-   [<span data-ttu-id="647f0-108">Implémentation de Active Accessibility Native</span><span class="sxs-lookup"><span data-stu-id="647f0-108">Native Active Accessibility Implementation</span></span>](native-active-accessibility-implementation.md)
-   [<span data-ttu-id="647f0-109">Proxys IAccessible</span><span class="sxs-lookup"><span data-stu-id="647f0-109">IAccessible Proxies</span></span>](iaccessible-proxies.md)

 

 




