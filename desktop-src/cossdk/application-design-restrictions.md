---
description: Certaines applications sont conçues d’une manière qui empêche l’installation de plusieurs instances de l’application sur un ordinateur.
ms.assetid: 951d20c8-7908-40d8-a9d5-d321340c97f3
title: Restrictions relatives à la conception d’applications
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1c4307a979866e3df9f019e69b858e8347c295b
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517399"
---
# <a name="application-design-restrictions"></a><span data-ttu-id="1d4cd-103">Restrictions relatives à la conception d’applications</span><span class="sxs-lookup"><span data-stu-id="1d4cd-103">Application Design Restrictions</span></span>

<span data-ttu-id="1d4cd-104">Certaines applications sont conçues d’une manière qui empêche l’installation de plusieurs instances de l’application sur un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="1d4cd-104">Some applications are designed in a way that prevents multiple instances of the application from being installed on a computer.</span></span> <span data-ttu-id="1d4cd-105">Avec une telle limitation, une application ne peut pas utiliser la fonctionnalité de partitions.</span><span class="sxs-lookup"><span data-stu-id="1d4cd-105">With such a limitation, an application cannot make use of the partitions feature.</span></span> <span data-ttu-id="1d4cd-106">Vous devrez peut-être modifier les fonctionnalités de conception d’application suivantes pour que les partitions puissent être utilisées pour cette application.</span><span class="sxs-lookup"><span data-stu-id="1d4cd-106">The following application design features might need to be modified before partitions can be used for that application.</span></span>

## <a name="tables-and-arrays"></a><span data-ttu-id="1d4cd-107">Tables et tableaux</span><span class="sxs-lookup"><span data-stu-id="1d4cd-107">Tables and Arrays</span></span>

<span data-ttu-id="1d4cd-108">Certaines applications créent des tables de base de données, des tables en mémoire ou des tableaux qui utilisent un CLSID comme clé de Registre unique.</span><span class="sxs-lookup"><span data-stu-id="1d4cd-108">Some applications create database tables, in-memory tables, or arrays that use a CLSID as a unique registry key.</span></span> <span data-ttu-id="1d4cd-109">Sur un ordinateur sans partitions, cette clé de Registre est généralement ordinateur/CLSID (un CLSID par ordinateur).</span><span class="sxs-lookup"><span data-stu-id="1d4cd-109">On a computer without partitions, this registry key is typically computer/CLSID (one CLSID per computer).</span></span>

<span data-ttu-id="1d4cd-110">À l’inverse, sur un ordinateur avec des partitions, cette clé de Registre est ID d’ordinateur/partition/ID d’application/CLSID (plusieurs instances d’un CLSID par ordinateur).</span><span class="sxs-lookup"><span data-stu-id="1d4cd-110">Conversely, on a computer with partitions, this registry key is computer/partition ID/application ID/CLSID (multiple instances of a CLSID per computer).</span></span> <span data-ttu-id="1d4cd-111">Étant donné que la fonctionnalité partitions permet à plusieurs instances d’un CLSID d’exister sur un ordinateur, les applications qui contiennent des éléments de conception qui requièrent un CLSID unique par ordinateur peuvent être affectées.</span><span class="sxs-lookup"><span data-stu-id="1d4cd-111">Because the partitions feature allows multiple instances of a CLSID to exist on a computer, applications that contain design elements that require a unique CLSID per computer might be adversely affected.</span></span>

## <a name="global-resources"></a><span data-ttu-id="1d4cd-112">Ressources globales</span><span class="sxs-lookup"><span data-stu-id="1d4cd-112">Global Resources</span></span>

<span data-ttu-id="1d4cd-113">Certaines applications utilisent des ressources globales, telles que la mémoire partagée, les fichiers de données et les entrées de registre.</span><span class="sxs-lookup"><span data-stu-id="1d4cd-113">Some applications use global resources such as shared memory, data files, and registry entries.</span></span> <span data-ttu-id="1d4cd-114">Cela peut entraîner des problèmes si plusieurs instances d’une telle application s’exécutent simultanément.</span><span class="sxs-lookup"><span data-stu-id="1d4cd-114">This could cause problems if multiple instances of such an application are executing simultaneously.</span></span>

<span data-ttu-id="1d4cd-115">Par exemple, si un composant utilise de la mémoire partagée pour interagir avec d’autres composants, le composant doit être modifié afin que chaque instance du composant alloue sa propre mémoire partagée.</span><span class="sxs-lookup"><span data-stu-id="1d4cd-115">For example, if a component uses shared memory for interacting with other components, the component will need to be modified so that each instance of the component allocates its own shared memory.</span></span>

## <a name="type-libraries"></a><span data-ttu-id="1d4cd-116">Bibliothèques de types</span><span class="sxs-lookup"><span data-stu-id="1d4cd-116">Type Libraries</span></span>

<span data-ttu-id="1d4cd-117">Les bibliothèques de types fournissent des informations sur les interfaces et les méthodes d’un composant.</span><span class="sxs-lookup"><span data-stu-id="1d4cd-117">Type libraries provide information about a component's interfaces and methods.</span></span> <span data-ttu-id="1d4cd-118">Ces informations sont utilisées à plusieurs fins, notamment les suivantes :</span><span class="sxs-lookup"><span data-stu-id="1d4cd-118">This information is used for several purposes, including the following:</span></span>

-   <span data-ttu-id="1d4cd-119">Marshaling de données entre des composants lorsque des appels de fonction sont effectués</span><span class="sxs-lookup"><span data-stu-id="1d4cd-119">Marshaling data between components when function calls are made</span></span>
-   <span data-ttu-id="1d4cd-120">Assistance des composants COM+ mis en file d’attente et des services d’événements COM+</span><span class="sxs-lookup"><span data-stu-id="1d4cd-120">Helping the COM+ Queued Components and COM+ Events services</span></span>
-   <span data-ttu-id="1d4cd-121">Fournir les informations correctes dans un éditeur de Visual Basic Microsoft</span><span class="sxs-lookup"><span data-stu-id="1d4cd-121">Providing the correct information within a Microsoft Visual Basic editor</span></span>

<span data-ttu-id="1d4cd-122">Les références à une bibliothèque de types sont installées dans le registre d’un ordinateur.</span><span class="sxs-lookup"><span data-stu-id="1d4cd-122">References to a type library are installed in the registry of a computer.</span></span> <span data-ttu-id="1d4cd-123">Lorsque vous développez des applications qui seront appelées à partir de partitions, il est important que la dernière version d’une bibliothèque de types soit installée dans le registre.</span><span class="sxs-lookup"><span data-stu-id="1d4cd-123">When developing applications that will be invoked from within partitions, it is important that the latest version of a type library is installed in the registry.</span></span> <span data-ttu-id="1d4cd-124">Cela permet de s’assurer que l’éditeur de Visual Basic est utilisé pour obtenir des informations précises sur les méthodes disponibles pour ce composant.</span><span class="sxs-lookup"><span data-stu-id="1d4cd-124">This ensures that the Visual Basic editor being used will get accurate information about the methods available for that component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1d4cd-125">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="1d4cd-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1d4cd-126">Composants et partitions COM+ en file d’attente</span><span class="sxs-lookup"><span data-stu-id="1d4cd-126">COM+ Queued Components and Partitions</span></span>](com--queued-components-and-partitions.md)
</dt> <dt>

[<span data-ttu-id="1d4cd-127">Implémentation de la partition</span><span class="sxs-lookup"><span data-stu-id="1d4cd-127">Partition Implementation</span></span>](partition-implementation.md)
</dt> <dt>

[<span data-ttu-id="1d4cd-128">Inscription et activation de composants dans des partitions</span><span class="sxs-lookup"><span data-stu-id="1d4cd-128">Registering and Activating Components in Partitions</span></span>](registering-and-activating-components-in-partitions.md)
</dt> <dt>

[<span data-ttu-id="1d4cd-129">Que sont les partitions COM+ ?</span><span class="sxs-lookup"><span data-stu-id="1d4cd-129">What Are COM+ Partitions?</span></span>](what-are-com--partitions-.md)
</dt> </dl>

 

 



