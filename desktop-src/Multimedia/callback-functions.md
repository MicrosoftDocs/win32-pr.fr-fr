---
title: Fonctions de rappel
description: Fonctions de rappel
ms.assetid: d96e93e5-ebc9-4ad4-aaec-dcc4197a3fc5
keywords:
- pilotes installables, fonctions de rappel
- pilotes installables, fonction DriverCallback
- pilotes installables, événements
- DriverCallback fonction)
- Message DRV_OPEN
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fabb833b0aa3adef444f8242d540eb48dcbe381ebc5c7f62c6dedc0d5e9160e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119786199"
---
# <a name="callback-functions"></a>Fonctions de rappel

Les pilotes installables peuvent notifier l’application, la fenêtre ou la tâche qui a ouvert l’instance donnée à propos des événements à l’aide de la fonction [DriverCallback](/windows/win32/api/mmiscapi/nf-mmiscapi-drivercallback) . Cette fonction donne au pilote le moyen de retourner des informations à une application ou à une DLL tout en continuant à traiter une demande.

Si un pilote prend en charge les fonctions de rappel, l’application ou la DLL qui ouvre l’instance doit fournir une valeur. il s’agit de l’adresse d’une fonction de rappel, d’un handle de fenêtre ou d’un handle de tâche. Cette valeur et un indicateur identifiant le type de la valeur sont généralement transmis dans une structure vers laquelle pointe le second paramètre du [**DRV \_ Open**](drv-open.md) message.

 

 