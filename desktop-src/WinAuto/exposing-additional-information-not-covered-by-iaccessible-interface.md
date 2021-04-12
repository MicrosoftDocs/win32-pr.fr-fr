---
title: Exposition d’informations supplémentaires non couvertes par l’interface IAccessible
description: En fonction de leurs produits, les développeurs de serveurs peuvent avoir besoin d’exposer des informations ou des fonctionnalités en plus de la prise en charge de Microsoft Active Accessibility.
ms.assetid: c45009ca-6be3-4645-9097-36671a41dfce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3834c60de8f18fd5ec0719919a1cd79e22f451e3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316026"
---
# <a name="exposing-additional-information-not-covered-by-iaccessible-interface"></a><span data-ttu-id="636b6-103">Exposition d’informations supplémentaires non couvertes par l’interface IAccessible</span><span class="sxs-lookup"><span data-stu-id="636b6-103">Exposing Additional Information Not Covered by IAccessible Interface</span></span>

<span data-ttu-id="636b6-104">En fonction de leurs produits, les développeurs de serveurs peuvent avoir besoin d’exposer des informations ou des fonctionnalités en plus de la prise en charge de Microsoft Active Accessibility.</span><span class="sxs-lookup"><span data-stu-id="636b6-104">Depending on their products, server developers might need to expose information or functionality in addition to Microsoft Active Accessibility support.</span></span> <span data-ttu-id="636b6-105">Dans ce cas, collaborez avec les fournisseurs de technologie d’assistance (clients) pour vous assurer qu’ils ajoutent la prise en charge des fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="636b6-105">If this is the case, work with assistive technology vendors (clients) to ensure that they add support for the features.</span></span>

<span data-ttu-id="636b6-106">N’essayez pas d’étendre l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) .</span><span class="sxs-lookup"><span data-stu-id="636b6-106">Do not attempt to extend the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface.</span></span> <span data-ttu-id="636b6-107">Les interfaces ne peuvent pas être modifiées une fois qu’elles sont publiées.</span><span class="sxs-lookup"><span data-stu-id="636b6-107">Interfaces cannot be changed once they are published.</span></span> <span data-ttu-id="636b6-108">Pour exposer des informations supplémentaires, utilisez une interface personnalisée et exposez-la à l’aide de l’une des techniques suivantes :</span><span class="sxs-lookup"><span data-stu-id="636b6-108">To expose additional information, use a custom interface and expose it by using one of the following techniques:</span></span>

-   [<span data-ttu-id="636b6-109">Utilisation \_ d’objid NATIVEOM pour exposer une interface de modèle objet natif pour une fenêtre</span><span class="sxs-lookup"><span data-stu-id="636b6-109">Using OBJID\_NATIVEOM to expose a native object model interface for a window</span></span>](using-objid-nativeom-to-expose-a-native-object-model-interface-for-a-window.md)
-   [<span data-ttu-id="636b6-110">Utilisation de QueryService pour exposer une interface de modèle objet natif pour un objet IAccessible</span><span class="sxs-lookup"><span data-stu-id="636b6-110">Using QueryService to expose a native object model interface for an IAccessible object</span></span>](using-queryservice-to-expose-a-native-object-model-interface-for-an-iaccessible-object.md)

<span data-ttu-id="636b6-111">Notez que l’objectif de l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) est d’avoir une interface bien définie qui est utilisée par les serveurs et les clients.</span><span class="sxs-lookup"><span data-stu-id="636b6-111">Note that the goal of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface is to have a well-defined interface that is used by servers and clients.</span></span> <span data-ttu-id="636b6-112">Avant d’exposer des interfaces personnalisées, veillez à exposer le plus d’informations possible via **IAccessible**.</span><span class="sxs-lookup"><span data-stu-id="636b6-112">Before exposing custom interfaces, be sure to expose as much information as possible through **IAccessible**.</span></span>

<span data-ttu-id="636b6-113">Vous ne pouvez pas utiliser [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) pour exposer des interfaces personnalisées.</span><span class="sxs-lookup"><span data-stu-id="636b6-113">You cannot use [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) to expose custom interfaces.</span></span> <span data-ttu-id="636b6-114">Utilisez **IServiceProvider :: QueryService** comme indiqué dans les procédures suivantes.</span><span class="sxs-lookup"><span data-stu-id="636b6-114">Use **IServiceProvider::QueryService** as outlined in the following procedures.</span></span>

 

 