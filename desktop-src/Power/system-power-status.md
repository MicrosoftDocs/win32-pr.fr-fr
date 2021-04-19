---
description: L’état de l’alimentation du système indique si la source d’alimentation d’un ordinateur est une batterie du système ou une alimentation secteur. Pour les ordinateurs qui utilisent des batteries, l’état de l’alimentation du système indique également la durée de vie de la batterie et la charge de la batterie.
ms.assetid: b9a5e7de-a603-4bd9-b854-1e58572c3b2b
title: État de l’alimentation du système
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e221142b5d39a4cb5bc49dbe85271c99837d0a20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524648"
---
# <a name="system-power-status"></a><span data-ttu-id="224e2-104">État de l’alimentation du système</span><span class="sxs-lookup"><span data-stu-id="224e2-104">System Power Status</span></span>

<span data-ttu-id="224e2-105">L’état de l’alimentation du système indique si la source d’alimentation d’un ordinateur est une batterie du système ou une alimentation secteur.</span><span class="sxs-lookup"><span data-stu-id="224e2-105">The system power status indicates whether the source of power for a computer is a system battery or AC power.</span></span> <span data-ttu-id="224e2-106">Pour les ordinateurs qui utilisent des batteries, l’état de l’alimentation du système indique également la durée de vie de la batterie et la charge de la batterie.</span><span class="sxs-lookup"><span data-stu-id="224e2-106">For computers that use batteries, the system power status also indicates how much battery life remains and whether the battery is charging.</span></span>

<span data-ttu-id="224e2-107">Les informations d’alimentation sont récupérées en s’inscrivant pour les notifications de paramètre d’alimentation via la fonction [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification) .</span><span class="sxs-lookup"><span data-stu-id="224e2-107">Power information is retrieved by registering for power setting notifications through the [**RegisterPowerSettingNotification**](/windows/desktop/api/WinUser/nf-winuser-registerpowersettingnotification) function.</span></span> <span data-ttu-id="224e2-108">Cette fonction permet aux applications de s’inscrire pour des paramètres d’alimentation spécifiques et de recevoir une notification en cas de changement.</span><span class="sxs-lookup"><span data-stu-id="224e2-108">This function allows applications to register for specific power settings and be notified when they change.</span></span>

> [!Note]  
> <span data-ttu-id="224e2-109">Pour rechercher des informations sur l’état de l’alimentation sans notifications, utilisez [**CallNtPowerInformation**](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation).</span><span class="sxs-lookup"><span data-stu-id="224e2-109">To query for power status information without notifications, use [**CallNtPowerInformation**](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation).</span></span>

 

<span data-ttu-id="224e2-110">Les applications et les pilotes installables utilisent généralement l’état de l’alimentation du système pour déterminer si la poursuite de l’opération est possible.</span><span class="sxs-lookup"><span data-stu-id="224e2-110">Applications and installable drivers typically use the system power status to determine whether continued operation is feasible.</span></span> <span data-ttu-id="224e2-111">Par exemple, avant qu’une application effectue des opérations en arrière-plan, telles que la compression ou la pagination d’un fichier, elle doit vérifier si le système se trouve sur batteries.</span><span class="sxs-lookup"><span data-stu-id="224e2-111">For example, before an application performs background operations such as compressing or paginating a file, it should check whether the system is on batteries.</span></span> <span data-ttu-id="224e2-112">Autre exemple : une application qui commence une longue opération doit vérifier l’État pour déterminer s’il existe suffisamment de batterie pour terminer l’opération.</span><span class="sxs-lookup"><span data-stu-id="224e2-112">As another example, an application that is beginning a lengthy operation should check the status to determine whether enough battery power exists to complete the operation.</span></span>

<span data-ttu-id="224e2-113">Par défaut, le système n’interroge pas les applications ou les pilotes pendant les transitions de veille.</span><span class="sxs-lookup"><span data-stu-id="224e2-113">By default, the system does not query applications or drivers during sleep transitions.</span></span>

> [!Note]  
> <span data-ttu-id="224e2-114">Si la puissance est faible, une application peut demander l’intervention de l’utilisateur ou demander que le système s’interrompt.</span><span class="sxs-lookup"><span data-stu-id="224e2-114">If power is low, an application can request user intervention or request that the system suspend itself.</span></span> <span data-ttu-id="224e2-115">Vous pouvez suspendre le fonctionnement du système à l’aide de la fonction [**SetSuspendState**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate) .</span><span class="sxs-lookup"><span data-stu-id="224e2-115">You can suspend system operation by using the [**SetSuspendState**](/windows/desktop/api/PowrProf/nf-powrprof-setsuspendstate) function.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="224e2-116">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="224e2-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="224e2-117">À propos de la gestion de l’alimentation</span><span class="sxs-lookup"><span data-stu-id="224e2-117">About Power Management</span></span>](about-power-management.md)
</dt> </dl>

 

 



