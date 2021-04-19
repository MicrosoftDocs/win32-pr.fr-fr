---
description: Pour améliorer les performances, l’accès aux objets GDI (Graphics Device Interface) (tels que les palettes, les contextes de périphérique, les régions, etc.) n’est pas sérialisé.
ms.assetid: aefb6a0b-ca00-4951-a173-8d7806b5d4e7
title: Threads multiples et objets GDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5822539248be5189f7a8e7fb15f4ef8a42ff1b70
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524217"
---
# <a name="multiple-threads-and-gdi-objects"></a><span data-ttu-id="9a12f-103">Threads multiples et objets GDI</span><span class="sxs-lookup"><span data-stu-id="9a12f-103">Multiple Threads and GDI Objects</span></span>

<span data-ttu-id="9a12f-104">Pour améliorer les performances, l’accès aux objets GDI (Graphics Device Interface) (tels que les palettes, les contextes de périphérique, les régions, etc.) n’est pas sérialisé.</span><span class="sxs-lookup"><span data-stu-id="9a12f-104">To enhance performance, access to graphics device interface (GDI) objects (such as palettes, device contexts, regions, and the like) is not serialized.</span></span> <span data-ttu-id="9a12f-105">Cela crée un danger potentiel pour les processus qui ont plusieurs threads partageant ces objets.</span><span class="sxs-lookup"><span data-stu-id="9a12f-105">This creates a potential danger for processes that have multiple threads sharing these objects.</span></span> <span data-ttu-id="9a12f-106">Par exemple, si un thread supprime un objet GDI alors qu’un autre thread l’utilise, les résultats sont imprévisibles.</span><span class="sxs-lookup"><span data-stu-id="9a12f-106">For example, if one thread deletes a GDI object while another thread is using it, the results are unpredictable.</span></span> <span data-ttu-id="9a12f-107">Ce danger peut être évité simplement en ne partageant pas d’objets GDI.</span><span class="sxs-lookup"><span data-stu-id="9a12f-107">This danger can be avoided simply by not sharing GDI objects.</span></span> <span data-ttu-id="9a12f-108">Si le partage est inévitable (ou souhaitable), l’application doit fournir ses propres mécanismes pour synchroniser l’accès.</span><span class="sxs-lookup"><span data-stu-id="9a12f-108">If sharing is unavoidable (or desirable), the application must provide its own mechanisms for synchronizing access.</span></span> <span data-ttu-id="9a12f-109">Pour plus d’informations sur la synchronisation de l’accès, consultez [synchronisation de plusieurs threads](synchronizing-execution-of-multiple-threads.md).</span><span class="sxs-lookup"><span data-stu-id="9a12f-109">For more information about synchronizing access, see [Synchronizing Execution of Multiple Threads](synchronizing-execution-of-multiple-threads.md).</span></span>

 

 



