---
description: Les fonctions suivantes sont utilisées par les fournisseurs de temps.
ms.assetid: 05687a67-4e0b-4a44-9c2d-7e097be9008c
title: Fonctions du fournisseur de temps
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3c0647574aaa807788e9cf510ce9293460c0394bcdaa794e243009ad6710bc6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118884814"
---
# <a name="time-provider-functions"></a>Fonctions du fournisseur de temps

Les fonctions suivantes sont utilisées par les fournisseurs de temps.



| Fonction                                                               | Description                                                                                            |
|------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| [**AlertSamplesAvailFunc**](/windows/desktop/api/Timeprov/nc-timeprov-alertsamplesavailfunc)                     | Informe le système que de nouveaux exemples sont disponibles.                                              |
| [**GetTimeSysInfoFunc**](/windows/desktop/api/Timeprov/nc-timeprov-gettimesysinfofunc)                           | Récupère les informations sur l’état de l’heure système.                                                           |
| [**LogTimeProvEventFunc**](/windows/desktop/api/Timeprov/nc-timeprov-logtimeproveventfunc)                       | Journalise un événement de fournisseur de temps dans le journal des événements.                                                           |
| [**SetProviderStatusFunc**](/windows/desktop/api/Timeprov/nc-timeprov-setproviderstatusfunc)                 | Définit les informations d’État du fournisseur de temps.                                                           |
| [**SetProviderStatusInfoFreeFunc**](/windows/desktop/api/Timeprov/nc-timeprov-setproviderstatusinfofreefunc) | Libère une structure [**SetProviderStatusInfo**](/windows/desktop/api/Timeprov/ns-timeprov-setproviderstatusinfo) .                          |
| [**TimeProvClose**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovclose)                                 | Fonction de rappel qui est appelée par le gestionnaire de fournisseurs de temps pour arrêter le fournisseur de temps.        |
| [**TimeProvCommand**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovcommand)                             | Fonction de rappel qui est appelée par le gestionnaire du fournisseur de temps pour envoyer des commandes au fournisseur de temps. |
| [**TimeProvOpen**](/windows/desktop/api/Timeprov/nf-timeprov-timeprovopen)                                   | Fonction de rappel qui est appelée par le gestionnaire de fournisseur de temps lors du chargement de la DLL du fournisseur de temps.  |



 

 

 



