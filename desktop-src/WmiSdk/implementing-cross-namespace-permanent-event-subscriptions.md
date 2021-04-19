---
description: Il est recommandé de compiler tous les abonnements permanents dans l’espace de noms de l' \\ \\ abonnement racine.
ms.assetid: 6d4ccc86-f29f-4ca5-bea5-c77ee07d7789
ms.tgt_platform: multiple
title: Implémentation des abonnements d’événements permanents entre espaces de noms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52771e40d4dfb036354c3b37b562b32edd3034ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106541883"
---
# <a name="implementing-cross-namespace-permanent-event-subscriptions"></a><span data-ttu-id="8a925-103">Implémentation des abonnements d’événements permanents entre espaces de noms</span><span class="sxs-lookup"><span data-stu-id="8a925-103">Implementing Cross-Namespace Permanent Event Subscriptions</span></span>

<span data-ttu-id="8a925-104">Il est recommandé de compiler tous les abonnements permanents dans l’espace de noms de l' \\ \\ abonnement racine.</span><span class="sxs-lookup"><span data-stu-id="8a925-104">It is recommended that all permanent subscriptions be compiled into the \\root\\subscription namespace.</span></span> <span data-ttu-id="8a925-105">Cela évite d’avoir à compiler le consommateur permanent dans chaque espace de noms utilisé, ce qui signifie qu’il n’existe qu’un seul espace de noms pour rechercher les abonnements permanents.</span><span class="sxs-lookup"><span data-stu-id="8a925-105">This prevents the need to compile the permanent consumer into each namespace being used, which means that there is only one namespace to look for permanent subscriptions.</span></span> <span data-ttu-id="8a925-106">Utilisez la propriété **EventNamespace** de [**\_ \_ EventFilter**](--eventfilter.md) pour implémenter un abonnement entre espaces de noms.</span><span class="sxs-lookup"><span data-stu-id="8a925-106">Use the **EventNamespace** property of [**\_\_EventFilter**](--eventfilter.md) to implement a cross-namespace subscription.</span></span>

<span data-ttu-id="8a925-107">Lorsque vous utilisez [**CommandLineEventConsumer**](commandlineeventconsumer.md), il est important de sécuriser l’exécutable que vous lancez.</span><span class="sxs-lookup"><span data-stu-id="8a925-107">When using the [**CommandLineEventConsumer**](commandlineeventconsumer.md), it is important to secure the executable you are launching.</span></span> <span data-ttu-id="8a925-108">Si l’exécutable ne se trouve pas dans un emplacement sécurisé ou sécurisé avec une liste de contrôle d’accès (ACL) forte, n’importe qui peut remplacer votre exécutable par l’un de leurs propres fichiers.</span><span class="sxs-lookup"><span data-stu-id="8a925-108">If the executable is not in a secure location, or secured with a strong access control list (ACL), anyone can replace your executable with one of their own.</span></span> <span data-ttu-id="8a925-109">Pour plus d’informations sur les listes de contrôle d’accès, consultez [création d’un descripteur de sécurité pour un nouvel objet en C++](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span><span class="sxs-lookup"><span data-stu-id="8a925-109">For more information about ACLs, see [Creating a Security Descriptor for a New Object in C++](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).</span></span>

<span data-ttu-id="8a925-110">L’exemple de code format MOF (MOF) suivant illustre un abonnement entre espaces de noms.</span><span class="sxs-lookup"><span data-stu-id="8a925-110">The following Managed Object Format (MOF) code example shows a cross-namespace subscription.</span></span>

``` syntax
#pragma namespace("\\root\\subscription")

instance of __EventFilter as $FLT
{
  Name = "Filter";
  Query = "SELECT * FROM __InstanceModificationEvent "
          "WHERE TargetInstance ISA \"Win32_LocalTime\" "
          "AND TargetInstance.Hour = 8 "
          "AND TargetInstance.Minute = 0 "
          "AND TargetInstance.Second = 0 "
          "AND TargetInstance.DayOfWeek = 6";
  QueryLanguage = "WQL";
  EventNamespace = "root\\cimv2";
};

instance of CommandLineEventConsumer as $CONS
{
  ExecutablePath = "cmd.exe";
  ShowWindowCommand = 7;
  RunInteractively = true;
};

instance of __FilterToConsumerBinding
{
  Consumer = $CONS;
  Filter = $FLT;
};
```

 

 
