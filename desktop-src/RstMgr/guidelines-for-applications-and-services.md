---
title: Instructions pour les applications et les services
description: Pour réduire le nombre de redémarrages du système lors de l’installation et de la maintenance des applications sur Windows Vista ou Windows Server 2008, vous devez respecter les consignes suivantes pour permettre à votre application ou service d’être arrêté correctement et redémarré.
ms.assetid: d0b9344f-05c6-4054-90b9-86942df50b3d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaf2963c03432a8b016f01316b79b387754f1459
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510603"
---
# <a name="guidelines-for-applications-and-services"></a>Instructions pour les applications et les services

Pour réduire le nombre de redémarrages du système lors de l’installation et de la maintenance des applications sur Windows Vista ou Windows Server 2008, vous devez respecter les consignes suivantes pour permettre à votre application ou service d’être arrêté correctement et redémarré.

-   Vos applications et services doivent être prêts à être arrêtés et redémarrés par le système lorsque cela est nécessaire pour installer une mise à jour. En général, lorsqu’une mise à jour est installée, une application ou un service doit être arrêté, car il contient actuellement un fichier affecté en cours d’utilisation. Toutes les applications ou tous les services qui peuvent contenir un fichier en cours d’utilisation pendant une mise à jour doivent être prêts à s’arrêter correctement.
-   Vos applications doivent enregistrer les données utilisateur et les informations d’État nécessaires après un redémarrage. elles doivent respecter les instructions décrites dans la section [instructions pour les applications](guidelines-for-applications.md).
-   Vos services doivent respecter les instructions décrites dans la section [instructions pour les services](guidelines-for-services.md).
-   Le gestionnaire de redémarrage n’arrête pas les [services système critiques](critical-system-services.md); par conséquent, ces services doivent limiter le nombre de dll dont ils dépendent.

 

 




