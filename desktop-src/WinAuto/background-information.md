---
title: Informations générales
description: Le composant Microsoft Active Accessibility, oleacc.dll, crée des objets proxy qui implémentent IAccessible pour le compte de contrôles Windows standard.
ms.assetid: c010af48-384c-40c0-ab52-c80b225502fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0a9b044f8035a474f02b8457dc99ec39aca73c2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100649"
---
# <a name="background-information"></a><span data-ttu-id="5ab73-103">Informations générales</span><span class="sxs-lookup"><span data-stu-id="5ab73-103">Background Information</span></span>

<span data-ttu-id="5ab73-104">Le composant Microsoft Active Accessibility, oleacc.dll, crée des objets proxy qui implémentent [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) pour le compte de contrôles Windows standard.</span><span class="sxs-lookup"><span data-stu-id="5ab73-104">The Microsoft Active Accessibility component, oleacc.dll, creates proxy objects that implement [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) on behalf of standard Windows controls.</span></span> <span data-ttu-id="5ab73-105">Étant donné que ces proxies utilisent des messages Windows standard et des API spécifiques au contrôle pour collecter des informations sur chaque contrôle, il n’existe aucun mécanisme direct pour la personnalisation des informations exposées par ces proxies par le biais de **IAccessible**.</span><span class="sxs-lookup"><span data-stu-id="5ab73-105">Because these proxies use standard Windows messages and control-specific APIs to collect information about each control, there has been no direct mechanism for customizing the information these proxies expose through **IAccessible**.</span></span>

<span data-ttu-id="5ab73-106">Actuellement, vous pouvez personnaliser une implémentation [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) existante à l’aide de techniques de sous-classe et d’encapsulation.</span><span class="sxs-lookup"><span data-stu-id="5ab73-106">Currently, you can customize an existing [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) implementation using subclassing and wrapping techniques.</span></span> <span data-ttu-id="5ab73-107">Toutefois, ces techniques sont fastidieuses et sujettes aux erreurs.</span><span class="sxs-lookup"><span data-stu-id="5ab73-107">However, these techniques are tedious and error-prone.</span></span> <span data-ttu-id="5ab73-108">En fait, la majorité du code écrit pour remplacer une ou deux propriétés s’intéresse à l’implémentation de la sous-classe et de l’encapsulation. seule une petite fraction effectue la tâche réelle de remplacement des informations.</span><span class="sxs-lookup"><span data-stu-id="5ab73-108">In fact, the majority of the code written to override one or two properties is concerned with implementing subclassing and wrapping; only a small fraction carries out the real task of overriding information.</span></span> <span data-ttu-id="5ab73-109">L’annotation dynamique améliore la situation en fournissant des fonctionnalités similaires sans avoir à écrire du code de sous-classe ou d’habillage.</span><span class="sxs-lookup"><span data-stu-id="5ab73-109">Dynamic Annotation improves the situation by providing similar capabilities without requiring you to write subclassing or wrapping code.</span></span> <span data-ttu-id="5ab73-110">Au lieu de cela, vous pouvez vous concentrer sur la fourniture de code qui fournit les informations correctes.</span><span class="sxs-lookup"><span data-stu-id="5ab73-110">Instead, you can focus on providing code that supplies the correct information.</span></span> <span data-ttu-id="5ab73-111">L’annotation dynamique permet aux développeurs de passer des indications et d’autres informations utiles à OLEACC pour personnaliser les informations qu’elle expose.</span><span class="sxs-lookup"><span data-stu-id="5ab73-111">Dynamic Annotation allows developers to pass hints and other useful information to OLEACC to customize the information it exposes.</span></span> <span data-ttu-id="5ab73-112">Cette fonctionnalité permet de réduire le coût de prise en charge de Microsoft Active Accessibility et de permettre aux développeurs d’améliorer de façon considérable l’accessibilité de leurs interfaces utilisateur.</span><span class="sxs-lookup"><span data-stu-id="5ab73-112">This capability alone will reduce the cost of supporting Microsoft Active Accessibility and allow developers to greatly improve the accessibility of their user interfaces.</span></span>

 

 




