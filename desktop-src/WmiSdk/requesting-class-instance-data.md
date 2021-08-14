---
description: 'Les requêtes de données sont des instructions WQL qui demandent des instances de classes. Pour émettre une requête de données, les applications appellent la méthode IWbemServices :: ExecQuery ou IWbemServices :: ExecQueryAsync.'
ms.assetid: a8b9bf2f-300d-4570-8b30-7532f3421d39
ms.tgt_platform: multiple
title: Demande de données d’instance de classe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3332ff8b5ba0aae7d1ac33fb8faba6340bbd795401fa81a52ea9c21abc4fde2e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118316286"
---
# <a name="requesting-class-instance-data"></a>Demande de données d’instance de classe

Les requêtes de données sont des instructions WQL qui demandent des instances de classes. Pour émettre une requête de données, les applications appellent la méthode [**IWbemServices :: ExecQuery**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execquery) ou [**IWbemServices :: ExecQueryAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-execqueryasync) .

Les instructions suivantes sont utilisées pour effectuer des requêtes de données :

-   [SELECT](select-statement-for-data-queries.md)
-   [ASSOCIATEURS DE](associators-of-statement.md)
-   [RÉFÉRENCES DE](references-of-statement.md)
-   [ISA](isa-operator-for-data-queries.md)

l’instruction WQL SELECT est l’instruction langage SQL standard (SQL) pour la récupération d’informations, avec quelques restrictions et extensions spécifiques à WQL. bien que l’instruction select SQL soit généralement utilisée dans l’environnement de base de données pour récupérer des colonnes particulières de tables, l’instruction WQL SELECT est utilisée dans WMI pour récupérer les instances d’une classe unique. WQL ne prend pas en charge les requêtes sur plusieurs classes.

Les ASSOCIateurs et les références des instructions sont spécifiques à WQL et ne font pas partie du SQL standard. Les ASSOCIateurs de l’instruction récupèrent toutes les instances de classe qui sont associées à une instance de classe source particulière, et les références de récupèrent toutes les instances qui font référence à une instance source particulière. Les associations sont représentées par des instances d’une [classe d’association](declaring-an-association-class.md).

 

 



