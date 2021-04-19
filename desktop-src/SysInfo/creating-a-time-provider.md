---
description: Un fournisseur de temps est implémenté en tant que DLL. Chaque DLL peut prendre en charge plusieurs fournisseurs de temps. Chaque fournisseur est responsable de sa propre configuration et de sa propre synchronisation.
ms.assetid: 04f523d7-7e99-4bf5-941f-ae67f4b9df0a
title: Création d’un fournisseur de temps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93ac5a12e19651d88c3328ac72280c486a54c4d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531226"
---
# <a name="creating-a-time-provider"></a>Création d’un fournisseur de temps

Un fournisseur de temps est implémenté en tant que DLL. Chaque DLL peut prendre en charge plusieurs fournisseurs de temps. Chaque fournisseur est responsable de sa propre configuration et de sa propre synchronisation.

Les fournisseurs de temps doivent implémenter les fonctions de rappel suivantes :

-   [**TimeProvClose**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovclose)
-   [**TimeProvCommand**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovcommand)
-   [**TimeProvOpen**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen)

Une fois la DLL du fournisseur chargée, le gestionnaire de fournisseurs de temps appelle [**TimeProvOpen**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen), en passant le nom du fournisseur et les pointeurs aux fonctions suivantes :

-   [**AlertSamplesAvailFunc**](/windows/desktop/api/Timeprov/nc-timeprov-alertsamplesavailfunc)
-   [**GetTimeSysInfoFunc**](/windows/desktop/api/Timeprov/nc-timeprov-gettimesysinfofunc)
-   [**LogTimeProvEventFunc**](/windows/desktop/api/Timeprov/nc-timeprov-logtimeproveventfunc)

Ces fonctions sont utilisées par le fournisseur de temps. Le fournisseur de temps utilise [**TimeProvOpen**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen) pour retourner un handle de fournisseur que le gestionnaire de fournisseurs de temps utilise lors de l’envoi de commandes au fournisseur de temps. La valeur de handle est définie par le fournisseur de temps et est utilisée principalement pour faire la distinction entre les différents fournisseurs implémentés dans la même DLL. Le fournisseur de temps peut consigner des événements importants à l’aide de [**LogTimeProvEventFunc**](/windows/desktop/api/Timeprov/nc-timeprov-logtimeproveventfunc).

Le gestionnaire de fournisseurs de temps utilise [**TimeProvCommand**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovcommand) pour envoyer des commandes au fournisseur de temps. Lorsque le fournisseur de temps doit informer le gestionnaire de fournisseurs de temps qu’il dispose d’exemples de temps disponibles, il appelle [**AlertSamplesAvailFunc**](/windows/desktop/api/Timeprov/nc-timeprov-alertsamplesavailfunc). Le gestionnaire de fournisseurs de temps appelle ensuite **TimeProvCommand** avec la \_ commande TPC getSamples pour récupérer les échantillons d’heure. Il peut falloir jusqu’à 16 secondes pour que le gestionnaire de fournisseurs de temps demande l’exemple. Par conséquent, l’application ne doit pas attendre la demande.

Pour garantir la précision, le fournisseur de temps doit récupérer toutes les informations relatives au temps à l’aide de [**GetTimeSysInfoFunc**](/windows/desktop/api/Timeprov/nc-timeprov-gettimesysinfofunc).

Lorsqu’il est temps d’arrêter le fournisseur de temps, le gestionnaire de fournisseurs de temps appelle [**TimeProvClose**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovclose).

 

 



