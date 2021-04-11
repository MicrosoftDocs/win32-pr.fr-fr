---
title: Annotation de serveur
description: Cette section fournit des informations sur l’utilisation des annotations de serveur.
ms.assetid: d8de90af-f5ed-42ef-bd74-e383360e8128
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fe1b8fba9849b25a29c50ea1f55507e61eb69f9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104028820"
---
# <a name="server-annotation"></a><span data-ttu-id="39036-103">Annotation de serveur</span><span class="sxs-lookup"><span data-stu-id="39036-103">Server Annotation</span></span>

<span data-ttu-id="39036-104">Cette section fournit des informations sur l’utilisation des annotations de serveur.</span><span class="sxs-lookup"><span data-stu-id="39036-104">This section provides information about using server annotation.</span></span>

## <a name="summary"></a><span data-ttu-id="39036-105">Résumé</span><span class="sxs-lookup"><span data-stu-id="39036-105">Summary</span></span>

<span data-ttu-id="39036-106">Vous définissez une classe qui implémente [**IAccPropServer**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropserver), créez une instance de celle-ci et indiquez au système que vous souhaitez qu’elle remplace des propriétés spécifiques sur des éléments d’interface utilisateur spécifiques.</span><span class="sxs-lookup"><span data-stu-id="39036-106">You define a class that implements [**IAccPropServer**](/windows/desktop/api/oleacc/nn-oleacc-iaccpropserver), create an instance of it, and tell the system that you want it to override specific properties on specific UI elements.</span></span> <span data-ttu-id="39036-107">Quand un client demande l’une des propriétés à partir de l’un des éléments d’interface utilisateur, votre objet est appelé et donne la possibilité de fournir une valeur.</span><span class="sxs-lookup"><span data-stu-id="39036-107">When a client requests one of the properties from one of the UI elements, your object is called and given an opportunity to provide a value.</span></span> <span data-ttu-id="39036-108">Si votre objet retourne une valeur, cette valeur est repassée au client.</span><span class="sxs-lookup"><span data-stu-id="39036-108">If your object returns a value, that value is passed back to the client.</span></span> <span data-ttu-id="39036-109">Si votre objet ne retourne pas de valeur, la valeur par défaut de cet élément d’interface utilisateur est retournée au client.</span><span class="sxs-lookup"><span data-stu-id="39036-109">If your object does not return a value, the default value for that UI element is returned to the client.</span></span>

## <a name="when-to-use-this-technique"></a><span data-ttu-id="39036-110">Quand utiliser cette technique</span><span class="sxs-lookup"><span data-stu-id="39036-110">When to Use This Technique</span></span>

<span data-ttu-id="39036-111">Utilisez cette technique lorsque vous souhaitez substituer les propriétés [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) pour un objet.</span><span class="sxs-lookup"><span data-stu-id="39036-111">Use this technique when you want to override the [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) properties for an object.</span></span> <span data-ttu-id="39036-112">Cette technique est bien plus simple que les techniques **IAccessible** précédentes.</span><span class="sxs-lookup"><span data-stu-id="39036-112">This technique is much simpler than previous **IAccessible** techniques.</span></span> <span data-ttu-id="39036-113">Pour plus d’informations, consultez [alternatives à l’annotation dynamique](alternatives-to-dynamic-annotation.md).</span><span class="sxs-lookup"><span data-stu-id="39036-113">For more information, see [Alternatives to Dynamic Annotation](alternatives-to-dynamic-annotation.md).</span></span>

<span data-ttu-id="39036-114">Vous ne pouvez pas utiliser l’annotation de serveur pour modifier la structure d’objets exposée.</span><span class="sxs-lookup"><span data-stu-id="39036-114">You cannot use server annotation to alter the exposed object structure.</span></span> <span data-ttu-id="39036-115">Pour modifier la structure d’un objet, vous devez implémenter un pointeur d’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) complet.</span><span class="sxs-lookup"><span data-stu-id="39036-115">To change the structure of an object, you must implement a full [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) interface pointer.</span></span>

<span data-ttu-id="39036-116">Pour plus d’informations sur les annotations de serveur, consultez les rubriques suivantes :</span><span class="sxs-lookup"><span data-stu-id="39036-116">For more information on server annotation, see the following topics:</span></span>

-   [<span data-ttu-id="39036-117">Utilisation de l’annotation de serveur</span><span class="sxs-lookup"><span data-stu-id="39036-117">Using Server Annotation</span></span>](using-server-annotation.md)
-   [<span data-ttu-id="39036-118">Exemple d’annotation de serveur</span><span class="sxs-lookup"><span data-stu-id="39036-118">Server Annotation Sample</span></span>](server-annotation-sample.md)

 

 




