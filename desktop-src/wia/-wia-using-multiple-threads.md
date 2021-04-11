---
description: Lors de l’utilisation d’une interface WIA (Windows Image Acquisition) dans plusieurs threads au sein d’un même processus, une application doit fournir un marshaling pour cette interface.
ms.assetid: b125b36e-1428-4aa6-b367-eac78291c88e
title: Utilisation de plusieurs threads dans une application WIA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebb1dbfa552e72dc068aff63a0a316d9af680ed1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113274"
---
# <a name="using-multiple-threads-in-a-wia-application"></a><span data-ttu-id="94e31-103">Utilisation de plusieurs threads dans une application WIA</span><span class="sxs-lookup"><span data-stu-id="94e31-103">Using Multiple Threads in a WIA Application</span></span>

<span data-ttu-id="94e31-104">Lors de l’utilisation d’une interface WIA (Windows Image Acquisition) dans plusieurs threads au sein d’un même processus, une application doit fournir un marshaling pour cette interface.</span><span class="sxs-lookup"><span data-stu-id="94e31-104">When using a Windows Image Acquisition (WIA) interface in more than one thread within a single process, an application must provide marshalling for that interface.</span></span> <span data-ttu-id="94e31-105">Si un thread crée un pointeur d’interface, vous ne pouvez pas utiliser ce pointeur dans un thread différent sans marshaling.</span><span class="sxs-lookup"><span data-stu-id="94e31-105">If one thread creates an interface pointer, you cannot use that pointer in a different thread without marshalling.</span></span>

<span data-ttu-id="94e31-106">Par exemple, si un thread dans une application obtient un pointeur vers l’interface [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) ou [**IWiaItem2**](-wia-iwiaitem2.md) , un thread distinct ne peut pas utiliser ce pointeur d’interface sans marshaling.</span><span class="sxs-lookup"><span data-stu-id="94e31-106">For example, if one thread in an application obtains a pointer to the [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) or [**IWiaItem2**](-wia-iwiaitem2.md) interface, a separate thread cannot use that interface pointer without marshalling.</span></span>

<span data-ttu-id="94e31-107">Une technique courante utilisée pour effectuer ce marshaling consiste à utiliser la table d’interface globale.</span><span class="sxs-lookup"><span data-stu-id="94e31-107">A common technique used to accomplish this marshalling is to use the global interface table.</span></span> <span data-ttu-id="94e31-108">La table d’interface globale est une table gérée sur tous les threads au sein d’un même processus.</span><span class="sxs-lookup"><span data-stu-id="94e31-108">The global interface table is a table maintained across all threads within a single process.</span></span> <span data-ttu-id="94e31-109">Tous les threads qui s’exécutent dans le processus peuvent récupérer des interfaces qui sont inscrites dans la table d’interface globale.</span><span class="sxs-lookup"><span data-stu-id="94e31-109">All threads running within the process can retrieve interfaces that are registered to the global interface table.</span></span> <span data-ttu-id="94e31-110">Cette technique évite d’avoir à créer des flux pour passer des interfaces entre les threads.</span><span class="sxs-lookup"><span data-stu-id="94e31-110">This technique avoids the need to create streams for passing interfaces between threads.</span></span>

<span data-ttu-id="94e31-111">Pour plus d’informations sur l’utilisation de la table d’interface globale, consultez [IGlobalInterfaceTable](/windows/win32/api/objidl/nn-objidl-iglobalinterfacetable).</span><span class="sxs-lookup"><span data-stu-id="94e31-111">For information on how to use the global interface table, see [IGlobalInterfaceTable](/windows/win32/api/objidl/nn-objidl-iglobalinterfacetable).</span></span>

<span data-ttu-id="94e31-112">Même si vous n’envisagez pas d’utiliser plusieurs threads dans une application WIA, vous devez supposer que toutes les fonctions de transfert de données ou de rappel d’événement d’appareil s’exécutent dans des threads distincts.</span><span class="sxs-lookup"><span data-stu-id="94e31-112">Even if you do not intend to use multiple threads in a WIA application, you must assume that all data transfer or device event callback functions run in separate threads.</span></span>

 

 
