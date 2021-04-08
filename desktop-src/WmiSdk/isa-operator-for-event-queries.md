---
description: L’opérateur ISA est un opérateur spécifique à WQL qui peut être utilisé dans les requêtes d’événement. Quand ISA est inclus dans la clause WHERE d’une requête d’événement, il demande la notification des événements pour toutes les classes dans une hiérarchie de classes, plutôt qu’une classe d’événements spécifique.
ms.assetid: 68b7a903-a206-4491-95c4-4a412537f6f5
ms.tgt_platform: multiple
title: Opérateur ISA pour les requêtes d’événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0acdd262492bfd876867bdfa7e13fd50e5380270
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104034933"
---
# <a name="isa-operator-for-event-queries"></a><span data-ttu-id="2f5e6-104">Opérateur ISA pour les requêtes d’événements</span><span class="sxs-lookup"><span data-stu-id="2f5e6-104">ISA Operator for Event Queries</span></span>

<span data-ttu-id="2f5e6-105">L’opérateur ISA est un opérateur spécifique à WQL qui peut être utilisé dans les requêtes d’événement.</span><span class="sxs-lookup"><span data-stu-id="2f5e6-105">The ISA operator is a WQL-specific operator that can be used in event queries.</span></span> <span data-ttu-id="2f5e6-106">Quand ISA est inclus dans la [clause WHERE](where-clause.md) d’une requête d’événement, il demande la notification des événements pour toutes les classes dans une hiérarchie de classes, plutôt qu’une classe d’événements spécifique.</span><span class="sxs-lookup"><span data-stu-id="2f5e6-106">When ISA is included in the [WHERE clause](where-clause.md) of an event query, it requests notification of events for all classes within a class hierarchy, rather than a specific event class.</span></span>

<span data-ttu-id="2f5e6-107">L’exemple suivant demande une notification toutes les 10 minutes des événements de modification d’instance pour toutes les instances qui sont membres de toute classe dérivée de la classe [**\_ disque logique Win32**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) .</span><span class="sxs-lookup"><span data-stu-id="2f5e6-107">The following example requests notification every 10 minutes of instance modification events for all instances that are members of any class derived from the [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk) class.</span></span>


```sql
SELECT * FROM __InstanceModificationEvent WITHIN 600
WHERE TargetInstance ISA "Win32_LogicalDisk"
```



<span data-ttu-id="2f5e6-108">Pour plus d’informations sur l’utilisation d’ISA avec une requête d’événement, consultez [création d’un événement de minuterie avec Win32 \_ localtime ou Win32 \_ UTCTime](./creating-a-timer-event-with-win32-localtime-or-win32-utctime.md).</span><span class="sxs-lookup"><span data-stu-id="2f5e6-108">For more information on using ISA with an event query, see [Creating a Timer Event with Win32\_LocalTime or Win32\_UTCTime](./creating-a-timer-event-with-win32-localtime-or-win32-utctime.md).</span></span>

 

 
