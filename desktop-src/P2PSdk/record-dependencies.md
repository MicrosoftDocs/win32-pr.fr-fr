---
description: L’infrastructure homologue ne garantit pas l’ordre de réception et de traitement des enregistrements.
ms.assetid: 840aa931-c54c-463d-b37b-7d01c8a44409
title: Dépendances d’enregistrement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75a7cce0803ad25f4a67908256ad78c7abe4b4af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106529838"
---
# <a name="record-dependencies"></a>Dépendances d’enregistrement

L’infrastructure homologue ne garantit pas l’ordre de réception et de traitement des enregistrements. Si votre application a des dépendances d’enregistrement, ce qui signifie que le traitement ou la validation d’un enregistrement repose sur un autre enregistrement, votre application doit être en mesure de gérer les situations où les enregistrements peuvent être reçus dans un ordre arbitraire et imprévisible. Par exemple, une application de conversation peut avoir deux types d’enregistrements : un enregistrement qui contient des informations sur un utilisateur spécifique et un enregistrement qui contient un message de conversation qui fait référence à l’enregistrement de l’utilisateur.

Une application doit être en mesure de gérer la situation lorsqu’un enregistrement de message de conversation est reçu avant l’enregistrement de l’utilisateur pour le message de conversation. Une manière de gérer la situation consiste à attendre l’enregistrement de l’utilisateur à l’aide d’une liste de mise **en veille**, ou d’un cache et d’un minuteur. L’application peut examiner périodiquement chaque enregistrement de la liste ou du cache, puis gérer la situation lors de la réception de l’enregistrement utilisateur requis.

Pour gérer les dépendances d’enregistrement, une application bien conçue se compose des éléments suivants :

-   Recherche toujours les dépendances d’enregistrement avant d’effectuer une action.
-   Anticipe les conditions qui peuvent se produire lorsque des enregistrements sont reçus dans un ordre inattendu, puis gère la situation.

 

 



