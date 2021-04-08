---
title: Classification des composants
description: Classification des composants
ms.assetid: 4d805532-96c9-400d-b78a-f8d0d9bdbf83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53ea1547c219a44262fdeaf7edb02f65c7a3aac6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840501"
---
# <a name="classifying-components"></a><span data-ttu-id="8c5be-103">Classification des composants</span><span class="sxs-lookup"><span data-stu-id="8c5be-103">Classifying Components</span></span>

<span data-ttu-id="8c5be-104">Lorsqu’un client peut parcourir la liste des CLSID du Registre et sélectionner un composant à utiliser, le chargement de chaque composant dans le registre et l’interrogation de ses interfaces prises en charge sont très longs.</span><span class="sxs-lookup"><span data-stu-id="8c5be-104">While a client is able to browse through the list of CLSIDs in the registry and select a component to use, loading each component in the registry and querying it for its supported interfaces is very time-consuming.</span></span> <span data-ttu-id="8c5be-105">Pour déterminer si un composant prend en charge les interfaces requises avant de créer une instance du composant, une méthode de classification des composants en catégories a été développée.</span><span class="sxs-lookup"><span data-stu-id="8c5be-105">To determine whether a component supports the interfaces required before creating an instance of the component, a method to classify components into categories was developed.</span></span>

<span data-ttu-id="8c5be-106">Une catégorie de composant est un ensemble d’interfaces auxquelles un GUID nommé CATID a été affecté.</span><span class="sxs-lookup"><span data-stu-id="8c5be-106">A component category is a set of interfaces that have been assigned a GUID named CATID.</span></span> <span data-ttu-id="8c5be-107">Les composants qui implémentent toutes les interfaces dans une catégorie de composant s’inscrivent en tant que membres de cette catégorie de composant.</span><span class="sxs-lookup"><span data-stu-id="8c5be-107">Components that implement all of the interfaces in a component category register themselves as members of that component category.</span></span> <span data-ttu-id="8c5be-108">Vous pouvez ensuite sélectionner des composants appartenant à une certaine catégorie de composants dans le registre.</span><span class="sxs-lookup"><span data-stu-id="8c5be-108">Components that belong to a certain component category can then be selected from the registry.</span></span> <span data-ttu-id="8c5be-109">En s’inscrivant lui-même en tant que membre d’une catégorie de composant, le composant garantit qu’il prend en charge toutes les interfaces membres dans la catégorie de composant.</span><span class="sxs-lookup"><span data-stu-id="8c5be-109">By registering itself as a member of a component category, the component is guaranteeing that it supports all of the member interfaces in the component category.</span></span>

<span data-ttu-id="8c5be-110">Un composant peut être membre de nombreuses catégories.</span><span class="sxs-lookup"><span data-stu-id="8c5be-110">A component can be a member of many categories.</span></span> <span data-ttu-id="8c5be-111">Elle n’est pas limitée à la prise en charge des interfaces dans une catégorie de composant.</span><span class="sxs-lookup"><span data-stu-id="8c5be-111">It is not limited to supporting interfaces in a component category.</span></span> <span data-ttu-id="8c5be-112">Elle peut prendre en charge n’importe quelle interface, en plus de celles qui se trouvent dans une catégorie de composant.</span><span class="sxs-lookup"><span data-stu-id="8c5be-112">It can support any interface, in addition to those in a component category.</span></span>

<span data-ttu-id="8c5be-113">Contrairement à l’inscription standard des composants, dans laquelle les développeurs doivent écrire du code qui enregistre manuellement les objets, les catégories de composants automatisent la majeure partie de ce travail.</span><span class="sxs-lookup"><span data-stu-id="8c5be-113">In contrast to the standard registration of components, in which developers must write code that manually registers objects, component categories automates much of this work.</span></span> <span data-ttu-id="8c5be-114">Les six méthodes de l’interface [**ICatRegister**](/windows/desktop/api/ComCat/nn-comcat-icatregister) définissent les catégories de composants et inscrivent les objets qui les implémentent ou les nécessitent.</span><span class="sxs-lookup"><span data-stu-id="8c5be-114">The six methods of the [**ICatRegister**](/windows/desktop/api/ComCat/nn-comcat-icatregister) interface define component categories and register objects that implement or require them.</span></span> <span data-ttu-id="8c5be-115">L’objet [Gestionnaire de catégories de composants](the-component-categories-manager.md) implémente cette interface.</span><span class="sxs-lookup"><span data-stu-id="8c5be-115">The [Component Categories Manager](the-component-categories-manager.md) object implements this interface.</span></span> <span data-ttu-id="8c5be-116">Pour plus d’informations sur l’utilisation des catégories de composants, consultez **ICatRegister** et [**ICatInformation**](/windows/desktop/api/ComCat/nn-comcat-icatinformation) .</span><span class="sxs-lookup"><span data-stu-id="8c5be-116">See **ICatRegister** and [**ICatInformation**](/windows/desktop/api/ComCat/nn-comcat-icatinformation) for additional information on using component categories.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8c5be-117">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="8c5be-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8c5be-118">Inscription des applications COM</span><span class="sxs-lookup"><span data-stu-id="8c5be-118">Registering COM Applications</span></span>](registering-com-applications.md)
</dt> </dl>

 

 




