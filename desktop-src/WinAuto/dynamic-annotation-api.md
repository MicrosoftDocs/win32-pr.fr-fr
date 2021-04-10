---
title: API d’annotation dynamique
description: L’API d’annotation dynamique est une extension de Microsoft Active Accessibility qui permet aux développeurs de personnaliser la prise en charge des IAccessible existants sans avoir à utiliser des techniques de sous-classe ou d’encapsulage sujettes aux erreurs.
ms.assetid: 2daf0e76-b300-47e7-994b-d1d00d0dca4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7f73c1da79784fdd86652128b572fd81904023c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940338"
---
# <a name="dynamic-annotation-api"></a><span data-ttu-id="70278-103">API d’annotation dynamique</span><span class="sxs-lookup"><span data-stu-id="70278-103">Dynamic Annotation API</span></span>

<span data-ttu-id="70278-104">L’API d’annotation dynamique est une extension de Microsoft Active Accessibility qui permet aux développeurs de personnaliser la prise en charge des [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) existants sans avoir à utiliser des techniques de sous-classe ou d’encapsulage sujettes aux erreurs.</span><span class="sxs-lookup"><span data-stu-id="70278-104">The Dynamic Annotation API is an extension to Microsoft Active Accessibility that allows developers to customize existing [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) support without having to use error-prone subclassing or wrapping techniques.</span></span> <span data-ttu-id="70278-105">Ce mécanisme permet également aux développeurs de transmettre des indications ou d’autres informations utiles aux proxies Oleacc.dll.</span><span class="sxs-lookup"><span data-stu-id="70278-105">This mechanism also allows developers to pass hints or other useful information to the Oleacc.dll proxies.</span></span>

<span data-ttu-id="70278-106">L’annotation dynamique est généralement utilisée pour corriger ou modifier une instance inexacte d’un objet [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) exposé par un proxy Oleacc.dll existant.</span><span class="sxs-lookup"><span data-stu-id="70278-106">Dynamic Annotation is typically used to correct or amend an inaccurate instance of an [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) object exposed by an existing Oleacc.dll proxy.</span></span> <span data-ttu-id="70278-107">Par exemple, vous pouvez l’utiliser pour remplacer le [**nom**](name-property.md) et les propriétés de [**rôle**](role-property.md) fournis par le proxy par défaut, et pour fournir la [**Description**](description-property.md) et les propriétés [**d’aide**](help-property.md) (qui peuvent ne pas être fournies par le proxy par défaut).</span><span class="sxs-lookup"><span data-stu-id="70278-107">For example, you can use it to override the [**Name**](name-property.md) and [**Role**](role-property.md) properties provided by the default proxy, and to supply [**Description**](description-property.md) and [**Help**](help-property.md) properties (which may not be provided by the default proxy).</span></span>

<span data-ttu-id="70278-108">Avec Windows 7, les développeurs peuvent utiliser l’API d’annotation dynamique pour annoter les propriétés de Microsoft UI Automation, ainsi que les propriétés de Active Accessibility de Microsoft des objets proxy que Oleacc.dll crée pour les contrôles Windows standard.</span><span class="sxs-lookup"><span data-stu-id="70278-108">With Windows 7, developers can use the Dynamic Annotation API to annotate Microsoft UI Automation properties as well as Microsoft Active Accessibility properties of the proxy objects that Oleacc.dll creates for standard Windows controls.</span></span> <span data-ttu-id="70278-109">Les objets proxy Oleacc.dll servent à la fois à des clients Microsoft Active Accessibility et UI Automation.</span><span class="sxs-lookup"><span data-stu-id="70278-109">The Oleacc.dll proxy objects serve both Microsoft Active Accessibility and UI Automation clients.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="70278-110">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="70278-110">In this section</span></span>

-   [<span data-ttu-id="70278-111">Informations générales</span><span class="sxs-lookup"><span data-stu-id="70278-111">Background Information</span></span>](background-information.md)
-   [<span data-ttu-id="70278-112">Alternatives à l’annotation dynamique</span><span class="sxs-lookup"><span data-stu-id="70278-112">Alternatives to Dynamic Annotation</span></span>](alternatives-to-dynamic-annotation.md)
-   [<span data-ttu-id="70278-113">Types d’annotation dynamique</span><span class="sxs-lookup"><span data-stu-id="70278-113">Types of Dynamic Annotation</span></span>](types-of-dynamic-annotation.md)
-   [<span data-ttu-id="70278-114">Annotation directe</span><span class="sxs-lookup"><span data-stu-id="70278-114">Direct Annotation</span></span>](direct-annotation.md)
-   [<span data-ttu-id="70278-115">Annotation de la carte des valeurs</span><span class="sxs-lookup"><span data-stu-id="70278-115">Value Map Annotation</span></span>](value-map-annotation.md)
-   [<span data-ttu-id="70278-116">Annotation de serveur</span><span class="sxs-lookup"><span data-stu-id="70278-116">Server Annotation</span></span>](server-annotation.md)
-   [<span data-ttu-id="70278-117">Problèmes et limitations</span><span class="sxs-lookup"><span data-stu-id="70278-117">Issues and Limitations</span></span>](issues-and-limitations.md)

 

 




