---
description: Il est recommandé de compiler tous les abonnements permanents dans l’espace de noms de l' \\ \\ abonnement racine.
ms.assetid: 6d4ccc86-f29f-4ca5-bea5-c77ee07d7789
ms.tgt_platform: multiple
title: Implémentation des abonnements d’événements permanents entre espaces de noms
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b175f89a4a686aa47818daf3479d521306f6190fb245222c4c21c17ca6470dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119757949"
---
# <a name="implementing-cross-namespace-permanent-event-subscriptions"></a>Implémentation des abonnements d’événements permanents entre espaces de noms

Il est recommandé de compiler tous les abonnements permanents dans l’espace de noms de l' \\ \\ abonnement racine. Cela évite d’avoir à compiler le consommateur permanent dans chaque espace de noms utilisé, ce qui signifie qu’il n’existe qu’un seul espace de noms pour rechercher les abonnements permanents. Utilisez la propriété **EventNamespace** de [**\_ \_ EventFilter**](--eventfilter.md) pour implémenter un abonnement entre espaces de noms.

Lorsque vous utilisez [**CommandLineEventConsumer**](commandlineeventconsumer.md), il est important de sécuriser l’exécutable que vous lancez. Si l’exécutable ne se trouve pas dans un emplacement sécurisé ou sécurisé avec une liste de contrôle d’accès (ACL) forte, n’importe qui peut remplacer votre exécutable par l’un de leurs propres fichiers. Pour plus d’informations sur les listes de contrôle d’accès, consultez [création d’un descripteur de sécurité pour un nouvel objet en C++](/windows/desktop/SecAuthZ/creating-a-security-descriptor-for-a-new-object-in-c--).

L’exemple de code format MOF (MOF) suivant illustre un abonnement entre espaces de noms.

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

 

 
