---
description: Les requêtes d’événement sont utilisées par les consommateurs d’événements temporaires, les consommateurs d’événements permanents et les fournisseurs d’événements. Les consommateurs d’événements utilisent des requêtes d’événements pour spécifier des événements intéressants, et les fournisseurs d’événements utilisent les requêtes pour spécifier les événements qu’ils fournissent.
ms.assetid: 851ad9bd-2604-4988-8de0-8d29b5300b21
ms.tgt_platform: multiple
title: Réception des notifications d’événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43873c03155f2186f9d3a9a3daff9b8e322e511f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106540843"
---
# <a name="receiving-event-notifications"></a>Réception des notifications d’événements

Les requêtes d’événement sont utilisées par les consommateurs d’événements temporaires, les consommateurs d’événements permanents et les fournisseurs d’événements. Les consommateurs d’événements utilisent des requêtes d’événements pour spécifier des événements intéressants, et les fournisseurs d’événements utilisent les requêtes pour spécifier les événements qu’ils fournissent.

Les [consommateurs temporaires](receiving-events-for-the-duration-of-your-application.md) placent les requêtes dans les appels à la méthode [**IWbemServices :: ExecNotificationQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationquery) ou [**IWbemServices :: ExecNotificationQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execnotificationqueryasync) . Les [consommateurs d’événements permanents](receiving-events-at-all-times.md) placent les requêtes dans la propriété **query** d’une instance de la classe système [**\_ \_ EventFilter**](--eventfilter.md) .

Les [fournisseurs d’événements](writing-an-event-provider.md) utilisent des requêtes d’événement pour s’inscrire afin de prendre en charge un ou plusieurs types d’événements. Elles placent les requêtes dans la propriété **EventQueryList** d’une instance de la classe système [**\_ \_ EventProviderRegistration**](--eventproviderregistration.md) . Tous les fournisseurs d’événements créent une instance **\_ \_ EventProviderRegistration** à inscrire auprès d’Windows Management Instrumentation (WMI). Pour plus d’informations, consultez [inscription d’un fournisseur d’événements](registering-an-event-provider.md).

Les consommateurs et les fournisseurs d’événements utilisent l' [instruction SELECT](select-statement-for-event-queries.md) et une clause WHERE associée pour les requêtes d’événements, ainsi qu’une variété d’extensions spécifiques au langage de requêtes WMI (WQL) (WQL). Les extensions sont utilisées pour empêcher les consommateurs d’être submergés par des notifications qui se produisent trop fréquemment pour être utiles.

Les consommateurs qui ne nécessitent pas de notification chaque fois qu’un événement se produit peuvent spécifier les clauses suivantes dans leurs requêtes :

-   Clause [within](within-clause.md)
-   [Group](group-clause.md) , clause
-   [Having](having-clause.md) (clause)

Les clauses in et HAVING affectent le minutage des événements, et la clause GROUP provoque l’envoi d’un événement représentatif à la place d’un événement qui se produit fréquemment.

 

 



