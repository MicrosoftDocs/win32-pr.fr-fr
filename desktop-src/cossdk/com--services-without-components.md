---
description: Services COM+ sans composants
ms.assetid: 5ef67411-334b-476e-b9b7-3677b24ab7df
title: Services COM+ sans composants
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1eeed5a9af96e241d137714d151cc632dd0f20e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110926"
---
# <a name="com-services-without-components"></a><span data-ttu-id="90d4f-103">Services COM+ sans composants</span><span class="sxs-lookup"><span data-stu-id="90d4f-103">COM+ Services Without Components</span></span>

<span data-ttu-id="90d4f-104">Avec COM+ 1,5, vous pouvez utiliser les services fournis par COM+ sans avoir à créer un composant pour contenir les méthodes qui appellent ces services.</span><span class="sxs-lookup"><span data-stu-id="90d4f-104">With COM+ 1.5, you can use the services provided by COM+ without needing to build a component to contain the methods that call those services.</span></span> <span data-ttu-id="90d4f-105">Cela permet aux développeurs qui n’utilisent pas généralement des composants d’utiliser des services COM+ tels que des transactions ou le dispositif de suivi COM+.</span><span class="sxs-lookup"><span data-stu-id="90d4f-105">This greatly benefits developers who do not normally use components but want to use COM+ services such as transactions or the COM+ Tracker.</span></span> <span data-ttu-id="90d4f-106">En utilisant des services COM+ sans composants, les développeurs peuvent éviter la surcharge liée à la création d’un composant qui est utilisé pour accéder uniquement aux services COM+ dont ils ont besoin.</span><span class="sxs-lookup"><span data-stu-id="90d4f-106">By using COM+ services without components, developers can avoid the overhead of creating a component that is used to access only the COM+ services they need.</span></span>

<span data-ttu-id="90d4f-107">Par exemple, les environnements de script ont traditionnellement été les plus grands consommateurs de services COM+, mais ils n’ont jamais pu utiliser ces services efficacement parce que les services devaient être regroupés dans un composant COM+.</span><span class="sxs-lookup"><span data-stu-id="90d4f-107">For example, script environments traditionally have been the largest consumers of COM+ services but they were never able to use those services efficiently because the services needed to be bundled within a COM+ component.</span></span> <span data-ttu-id="90d4f-108">Cette exigence de regroupement a augmenté les coûts de performances en raison de l’augmentation de la communication et de la duplication des données nécessaires à l’environnement de script pour interagir avec le composant.</span><span class="sxs-lookup"><span data-stu-id="90d4f-108">This bundling requirement increased performance costs because of the increased communication and duplication of data necessary for the scripting environment to interact with the component.</span></span> <span data-ttu-id="90d4f-109">En utilisant des services sans composants, ces coûts sont réduits.</span><span class="sxs-lookup"><span data-stu-id="90d4f-109">By using services without components, such costs are minimized.</span></span>

<span data-ttu-id="90d4f-110">Les rubriques décrites dans le tableau suivant fournissent des informations générales et sur les tâches relatives à l’utilisation des services COM+ sans composants.</span><span class="sxs-lookup"><span data-stu-id="90d4f-110">The topics described in the following table provide background and task information about using COM+ services without components.</span></span> <span data-ttu-id="90d4f-111">Cette fonctionnalité est destinée aux développeurs avancés Visual C++ qui se soucient des performances.</span><span class="sxs-lookup"><span data-stu-id="90d4f-111">This feature is intended for advanced Visual C++ developers who are concerned about performance.</span></span>



| <span data-ttu-id="90d4f-112">Rubrique</span><span class="sxs-lookup"><span data-stu-id="90d4f-112">Topic</span></span>                                                                                                 | <span data-ttu-id="90d4f-113">Description</span><span class="sxs-lookup"><span data-stu-id="90d4f-113">Description</span></span>                                                                                    |
|-------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="90d4f-114">Concepts des services COM+ sans composants</span><span class="sxs-lookup"><span data-stu-id="90d4f-114">COM+ Services Without Components Concepts</span></span>](com--services-without-components-concepts.md)<br/> | <span data-ttu-id="90d4f-115">Fournit une vue d’ensemble de l’utilisation des services COM+ sans composants.</span><span class="sxs-lookup"><span data-stu-id="90d4f-115">Provides an overview of using COM+ services without components.</span></span><br/>                     |
| [<span data-ttu-id="90d4f-116">Tâches des services COM+ sans composants</span><span class="sxs-lookup"><span data-stu-id="90d4f-116">COM+ Services Without Components Tasks</span></span>](com--services-without-components-tasks.md)<br/>       | <span data-ttu-id="90d4f-117">Fournit des instructions sur l’utilisation de COM+ pour créer et utiliser des services sans composants.</span><span class="sxs-lookup"><span data-stu-id="90d4f-117">Provides instructions for using COM+ to create and use services without components.</span></span><br/> |



 

 

 




