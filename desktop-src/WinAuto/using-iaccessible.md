---
title: Utilisation de l’interface IAccessible
description: L’interface IAccessible est une collection de méthodes qui exposent les attributs et les comportements les plus courants d’un large éventail d’éléments d’interface utilisateur.
ms.assetid: 82f6e934-58ea-47f2-98a3-2ab1c20f24c3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 218d009793dc1bebac2a7e5caeba8fa140ac0d96
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310254"
---
# <a name="using-the-iaccessible-interface"></a><span data-ttu-id="bdba0-103">Utilisation de l’interface IAccessible</span><span class="sxs-lookup"><span data-stu-id="bdba0-103">Using the IAccessible Interface</span></span>

<span data-ttu-id="bdba0-104">L’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) est une collection de méthodes qui exposent les attributs et les comportements les plus courants d’un large éventail d’éléments d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bdba0-104">The [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface is a collection of methods that expose the most common attributes and behaviors of a wide range of UI elements.</span></span> <span data-ttu-id="bdba0-105">Un élément d’interface utilisateur est un contrôle, tel qu’un menu ou un bouton de commande, qui fait partie de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bdba0-105">A UI element is a control, such as a menu or push button, that is part of the user interface.</span></span> <span data-ttu-id="bdba0-106">Un objet accessible est un élément d’interface utilisateur qui a une interface **IAccessible** significative.</span><span class="sxs-lookup"><span data-stu-id="bdba0-106">An accessible object is a UI element that has a meaningful **IAccessible** interface.</span></span>

<span data-ttu-id="bdba0-107">Certaines propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) ne sont pas applicables à chaque type d’élément d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="bdba0-107">Some of the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties are not applicable to every kind of user interface element.</span></span> <span data-ttu-id="bdba0-108">En outre, l’implémentation de **IAccessible** varie d’une application à l’autres.</span><span class="sxs-lookup"><span data-stu-id="bdba0-108">Also, the implementation of **IAccessible** varies from application to application.</span></span>

<span data-ttu-id="bdba0-109">Bien que les paramètres et les valeurs de retour pour les propriétés et les méthodes [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) soient entièrement spécifiés, la manière dont un client doit utiliser une propriété ou la manière dont un serveur doit implémenter une propriété est parfois sujette à l’interprétation.</span><span class="sxs-lookup"><span data-stu-id="bdba0-109">Although the parameters and return values for the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties and methods are fully specified, how a client should use a property or how a server should implement a property is sometimes subject to interpretation.</span></span>

<span data-ttu-id="bdba0-110">Cette section fournit des suggestions, des instructions et des exemples pour aider les applications clientes à obtenir des informations sur les éléments d’interface utilisateur et à aider les applications serveur à fournir les informations appropriées.</span><span class="sxs-lookup"><span data-stu-id="bdba0-110">This section provides suggestions, guidelines, and examples for helping client applications obtain information about UI elements and for helping server applications provide appropriate information.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="bdba0-111">Dans cette section</span><span class="sxs-lookup"><span data-stu-id="bdba0-111">In this section</span></span>

-   [<span data-ttu-id="bdba0-112">Contenu des propriétés descriptives</span><span class="sxs-lookup"><span data-stu-id="bdba0-112">Content of Descriptive Properties</span></span>](content-of-descriptive-properties.md)
-   [<span data-ttu-id="bdba0-113">Propriétés et méthodes de sélection et de focus</span><span class="sxs-lookup"><span data-stu-id="bdba0-113">Selection and Focus Properties and Methods</span></span>](selection-and-focus-properties-and-methods.md)
-   [<span data-ttu-id="bdba0-114">Propriétés et méthodes de navigation entre les objets</span><span class="sxs-lookup"><span data-stu-id="bdba0-114">Object Navigation Properties and Methods</span></span>](object-navigation-properties-and-methods.md)

 

 




