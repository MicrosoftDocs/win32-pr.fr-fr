---
description: Inscription et activation de composants dans des partitions
ms.assetid: 2cca71da-c7f7-4997-b63a-74ba266e9e95
title: Inscription et activation de composants dans des partitions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31790bc9a3df12d961a4b16271937ae22f963c38
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523532"
---
# <a name="registering-and-activating-components-in-partitions"></a><span data-ttu-id="ca78c-103">Inscription et activation de composants dans des partitions</span><span class="sxs-lookup"><span data-stu-id="ca78c-103">Registering and Activating Components in Partitions</span></span>

<span data-ttu-id="ca78c-104">Une fois qu’une partition a été créée, l’étape suivante consiste à inscrire vos composants COM+ au sein de cette partition.</span><span class="sxs-lookup"><span data-stu-id="ca78c-104">After a partition has been created, the next step is register your COM+ components within that partition.</span></span> <span data-ttu-id="ca78c-105">Un composant est inscrit dans une partition lors de la création d’une nouvelle application COM+ ou lors de l’installation d’une application COM+ existante dans la partition.</span><span class="sxs-lookup"><span data-stu-id="ca78c-105">A component is registered within a partition when a new COM+ application is created or when an existing COM+ application is installed into the partition.</span></span> <span data-ttu-id="ca78c-106">Pour faciliter l’administration de l’inscription lorsque plusieurs partitions contiennent les mêmes composants COM+, le service partitions permet à un administrateur de copier des applications ou des composants d’une partition vers une autre.</span><span class="sxs-lookup"><span data-stu-id="ca78c-106">To ease the administration of registration when multiple partitions contain the same COM+ components, the partitions service allows an administrator to copy applications or components from one partition into another.</span></span> <span data-ttu-id="ca78c-107">Lorsqu’une application COM+ ou un composant est copié, toutes les propriétés de partition associées sont copiées avec celle-ci, à l’exception de l’identité de l’application ou de l’un des membres d’un rôle.</span><span class="sxs-lookup"><span data-stu-id="ca78c-107">When a COM+ application or a component is copied, all associated partition properties are copied with it, except the application's identity or any of the members of a role.</span></span>

<span data-ttu-id="ca78c-108">Lorsque le programme client appelle la fonction [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) ou [**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) pour instancier un objet, com+ effectue deux étapes distinctes, comme suit :</span><span class="sxs-lookup"><span data-stu-id="ca78c-108">When the client program calls the [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) or [**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) function to instantiate an object, COM+ performs two distinct steps, as follows:</span></span>

1.  <span data-ttu-id="ca78c-109">Localise la partition dans laquelle le composant réside</span><span class="sxs-lookup"><span data-stu-id="ca78c-109">Locates the partition in which the component resides</span></span>
2.  <span data-ttu-id="ca78c-110">Localise le composant approprié dans cette partition</span><span class="sxs-lookup"><span data-stu-id="ca78c-110">Locates the correct component within that partition</span></span>

<span data-ttu-id="ca78c-111">Les rubriques suivantes de cette section décrivent ces étapes en détail :</span><span class="sxs-lookup"><span data-stu-id="ca78c-111">The following topics in this section describe these steps in detail:</span></span>

-   [<span data-ttu-id="ca78c-112">Recherche de partitions pendant l’activation</span><span class="sxs-lookup"><span data-stu-id="ca78c-112">Locating Partitions During Activation</span></span>](locating-partitions-during-activation.md)
-   [<span data-ttu-id="ca78c-113">Recherche d’un composant pour l’activation</span><span class="sxs-lookup"><span data-stu-id="ca78c-113">Locating a Component for Activation</span></span>](locating-a-component-for-activation.md)

## <a name="related-topics"></a><span data-ttu-id="ca78c-114">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="ca78c-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ca78c-115">Restrictions relatives à la conception d’applications</span><span class="sxs-lookup"><span data-stu-id="ca78c-115">Application Design Restrictions</span></span>](application-design-restrictions.md)
</dt> <dt>

[<span data-ttu-id="ca78c-116">Composants et partitions COM+ en file d’attente</span><span class="sxs-lookup"><span data-stu-id="ca78c-116">COM+ Queued Components and Partitions</span></span>](com--queued-components-and-partitions.md)
</dt> <dt>

[<span data-ttu-id="ca78c-117">Implémentation de la partition</span><span class="sxs-lookup"><span data-stu-id="ca78c-117">Partition Implementation</span></span>](partition-implementation.md)
</dt> <dt>

[<span data-ttu-id="ca78c-118">Que sont les partitions COM+ ?</span><span class="sxs-lookup"><span data-stu-id="ca78c-118">What Are COM+ Partitions?</span></span>](what-are-com--partitions-.md)
</dt> </dl>

 

 
