---
description: Un service, un pilote ou une application qui souhaite fournir des données de compteur peut écrire une DLL de performance pour fournir les données.
ms.assetid: 030316e5-f9f3-4333-9bb4-7ad301bbe7bf
title: Fourniture de données de compteur à l’aide d’une DLL de performance
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: e14b8a0e59b1fc9af3d8cad6e895d4a0067b9ae6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106536154"
---
# <a name="providing-counter-data-using-a-performance-dll"></a><span data-ttu-id="c5ece-103">Fourniture de données de compteur à l’aide d’une DLL de performance</span><span class="sxs-lookup"><span data-stu-id="c5ece-103">Providing Counter Data Using a Performance DLL</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c5ece-104">En raison des limitations de performances et de fiabilité significatives, la méthode permettant de fournir des données de compteurs de performances que cette rubrique décrit peut être modifiée ou non disponible à l’avenir.</span><span class="sxs-lookup"><span data-stu-id="c5ece-104">Due to significant performance and reliability limitations, the method for providing performance counter data that this topic describes may be altered or unavailable in the future.</span></span> <span data-ttu-id="c5ece-105">Au lieu de cela, Microsoft vous recommande d’utiliser la méthode décrite dans la rubrique [fourniture de données de compteur à l’aide de la Version 2,0](providing-counter-data-using-version-2-0.md) pour la création de nouveaux compteurs de performances et la migration des compteurs de performances existants pour utiliser également cette méthode.</span><span class="sxs-lookup"><span data-stu-id="c5ece-105">Instead, Microsoft recommends that you use the method described in [Providing Counter Data Using Version 2.0](providing-counter-data-using-version-2-0.md) for creating new performance counters, and that you migrate existing performance counters to use that method as well.</span></span>

<span data-ttu-id="c5ece-106">Un service, un pilote ou une application qui souhaite fournir des données de compteur peut écrire une DLL de performance pour fournir les données.</span><span class="sxs-lookup"><span data-stu-id="c5ece-106">A service, driver, or application that wants to provide counter data can write a performance DLL to provide the data.</span></span> <span data-ttu-id="c5ece-107">Lorsqu’un consommateur interroge des données de performances, le système charge la DLL du fournisseur dans le processus du consommateur et appelle le fournisseur pour collecter les données.</span><span class="sxs-lookup"><span data-stu-id="c5ece-107">When a consumer queries performance data, the system loads the provider DLL into the consumer's process and calls the provider to collect the data.</span></span> <span data-ttu-id="c5ece-108">Pour plus d’informations sur l’écriture de la DLL de performance, consultez [création d’une DLL d’extension de performance](creating-a-performance-extension-dll.md).</span><span class="sxs-lookup"><span data-stu-id="c5ece-108">For details on writing the performance DLL, see [Creating a Performance Extension DLL](creating-a-performance-extension-dll.md).</span></span>

<span data-ttu-id="c5ece-109">Le système utilise le registre pour déterminer le fournisseur à appeler.</span><span class="sxs-lookup"><span data-stu-id="c5ece-109">The system uses the registry to determine which provider to call.</span></span> <span data-ttu-id="c5ece-110">Pour plus d’informations sur l’inscription de votre fournisseur et les compteurs qu’il prend en charge, consultez [Ajout de compteurs de performances](adding-performance-counters.md).</span><span class="sxs-lookup"><span data-stu-id="c5ece-110">For information on registering your provider and the counters that it supports, see [Adding Performance Counters](adding-performance-counters.md).</span></span>

> [!Note]
> <span data-ttu-id="c5ece-111">Les dll de performance ne sont pas prises en charge sur Windows OneCore.</span><span class="sxs-lookup"><span data-stu-id="c5ece-111">Performance DLLs are not supported on Windows OneCore.</span></span> <span data-ttu-id="c5ece-112">Si vous écrivez un composant qui doit s’exécuter sur Windows OneCore, utilisez la méthode décrite dans la rubrique [fourniture de données de compteur à l’aide de la Version 2,0](providing-counter-data-using-version-2-0.md).</span><span class="sxs-lookup"><span data-stu-id="c5ece-112">If writing a component that must run on Windows OneCore, use the method described in [Providing Counter Data Using Version 2.0](providing-counter-data-using-version-2-0.md).</span></span>
