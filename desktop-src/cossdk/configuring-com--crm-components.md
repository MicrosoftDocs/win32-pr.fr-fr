---
description: Les composants CRM peuvent être installés dans une application serveur COM+ ou une application de bibliothèque COM+.
ms.assetid: d1ce3a0c-1278-498c-b5dc-4e14b26b4fc2
title: Configuration des composants CRM de COM+
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f3614c2c34d36cb140f08529c05b31bcc5a4c7f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514549"
---
# <a name="configuring-com-crm-components"></a><span data-ttu-id="a2ec9-103">Configuration des composants CRM de COM+</span><span class="sxs-lookup"><span data-stu-id="a2ec9-103">Configuring COM+ CRM Components</span></span>

<span data-ttu-id="a2ec9-104">Les composants CRM peuvent être installés dans une application serveur COM+ ou une application de bibliothèque COM+.</span><span class="sxs-lookup"><span data-stu-id="a2ec9-104">CRM components can be installed into either a COM+ server application or a COM+ library application.</span></span> <span data-ttu-id="a2ec9-105">Toutefois, ils doivent toujours s’exécuter dans une application serveur COM+.</span><span class="sxs-lookup"><span data-stu-id="a2ec9-105">However, they must always run in a COM+ server application.</span></span> <span data-ttu-id="a2ec9-106">S’ils sont installés dans une application de bibliothèque COM+, ils ne peuvent pas être utilisés dans les processus client.</span><span class="sxs-lookup"><span data-stu-id="a2ec9-106">If they are installed in a COM+ library application, they are not available for use in client processes.</span></span>

<span data-ttu-id="a2ec9-107">Si les composants CRM sont installés dans une application de bibliothèque, ils sont disponibles pour plusieurs applications serveur.</span><span class="sxs-lookup"><span data-stu-id="a2ec9-107">If the CRM components they are installed in a library application, they are available to more than one server application.</span></span> <span data-ttu-id="a2ec9-108">S’il est installé dans une application serveur spécifique, il est uniquement disponible pour cette application serveur spécifique.</span><span class="sxs-lookup"><span data-stu-id="a2ec9-108">If installed in a specific server application, they are available only to that specific server application.</span></span>

<span data-ttu-id="a2ec9-109">Pour activer l’utilisation d’un CRM dans une application serveur, procédez comme suit :</span><span class="sxs-lookup"><span data-stu-id="a2ec9-109">To enable use of a CRM in a server application, use the following steps:</span></span>

1.  <span data-ttu-id="a2ec9-110">Dans services de composants, sous la page Propriétés de l’application serveur, cliquez sur l’onglet **avancé** .</span><span class="sxs-lookup"><span data-stu-id="a2ec9-110">From Component Services, under the server application properties page, click the **Advanced** tab.</span></span>

2.  <span data-ttu-id="a2ec9-111">Sélectionnez l’option **activer les gestionnaires de ressources de compensation** pour cette application serveur.</span><span class="sxs-lookup"><span data-stu-id="a2ec9-111">Select the **Enable compensating Resource Managers** option for that server application.</span></span> <span data-ttu-id="a2ec9-112">Si cette option n’est pas sélectionnée, les tentatives d’utilisation d’un CRM au sein de cette application serveur échoueront.</span><span class="sxs-lookup"><span data-stu-id="a2ec9-112">If this option is not selected, attempts to use a CRM within this server application will fail.</span></span>

    > [!Note]  
    > <span data-ttu-id="a2ec9-113">S’il est installé dans une application de bibliothèque, il n’est pas nécessaire de sélectionner l’option **activer les gestionnaires de ressources de compensation** pour cette application de bibliothèque, mais cette option doit être sélectionnée pour l’application serveur dans laquelle le CRM est destiné à être exécuté.</span><span class="sxs-lookup"><span data-stu-id="a2ec9-113">If installed in a library application, it is not necessary to select the **Enable compensating Resource Managers** option for that library application, but this option must be selected for the server application in which the CRM is intended to run.</span></span>

     

<span data-ttu-id="a2ec9-114">Il est recommandé d’installer les composants de travail CRM et du compensateur CRM pour un CRM spécifique dans la même application.</span><span class="sxs-lookup"><span data-stu-id="a2ec9-114">It is recommended that the CRM Worker and CRM Compensator components for a specific CRM be installed in the same application.</span></span>

<span data-ttu-id="a2ec9-115">Les paramètres recommandés pour les composants CRM sont les suivants :</span><span class="sxs-lookup"><span data-stu-id="a2ec9-115">The recommended settings for CRM components are as follows.</span></span>



| <span data-ttu-id="a2ec9-116">Composant</span><span class="sxs-lookup"><span data-stu-id="a2ec9-116">Component</span></span>           | <span data-ttu-id="a2ec9-117">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a2ec9-117">Settings</span></span>                                                                                             |
|---------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2ec9-118">**CRM Worker**</span><span class="sxs-lookup"><span data-stu-id="a2ec9-118">**CRM Worker**</span></span>      | <span data-ttu-id="a2ec9-119">transaction = requiredsync = yesJIT = yesthreading Model = both (ou modèle de thread = Apartment)</span><span class="sxs-lookup"><span data-stu-id="a2ec9-119">transaction = requiredsync = yesJIT = yesthreading model = Both (or threading model = Apartment)</span></span>     |
| <span data-ttu-id="a2ec9-120">**Compensateur CRM**</span><span class="sxs-lookup"><span data-stu-id="a2ec9-120">**CRM Compensator**</span></span> | <span data-ttu-id="a2ec9-121">transaction = disabledsync = disabledJIT = nothreading Model = both (ou modèle de thread = Apartment)</span><span class="sxs-lookup"><span data-stu-id="a2ec9-121">transaction = disabledsync = disabledJIT = nothreading model = Both (or threading model = Apartment)</span></span> |



 

> [!Note]  
> <span data-ttu-id="a2ec9-122">Les composants qui utilisent le CRM doivent spécifier explicitement un modèle de thread lorsqu’ils sont inscrits.</span><span class="sxs-lookup"><span data-stu-id="a2ec9-122">Components that use the CRM must explicitly specify a threading model when they are registered.</span></span> <span data-ttu-id="a2ec9-123">La valeur par défaut « principal thread Apartment » n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="a2ec9-123">The default, 'Main Thread Apartment,' is not supported.</span></span> <span data-ttu-id="a2ec9-124">Les deux seuls modèles de thread pris en charge sont Apartment et Both.</span><span class="sxs-lookup"><span data-stu-id="a2ec9-124">The only two threading models supported are Apartment and Both.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="a2ec9-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="a2ec9-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a2ec9-126">Concepts de Gestionnaire des ressources de compensation COM+</span><span class="sxs-lookup"><span data-stu-id="a2ec9-126">COM+ Compensating Resource Manager Concepts</span></span>](com--compensating-resource-manager-concepts.md)
</dt> </dl>

 

 



