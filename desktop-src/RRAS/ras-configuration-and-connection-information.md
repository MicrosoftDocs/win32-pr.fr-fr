---
title: Configuration RAS et informations de connexion
description: Les applications qui s’exécutent sur Windows NT 4,0 et versions ultérieures, ainsi que sur Windows 95, peuvent utiliser la fonction RasEnumConnections pour obtenir des informations sur les connexions existantes sur l’ordinateur local.
ms.assetid: b738ed87-1ff5-4366-9e83-08ac08ec261c
keywords:
- Configuration et connexion, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44c4e768f4686a24857a75212e40f2e64bc91109
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106511424"
---
# <a name="ras-configuration-and-connection-information"></a>Configuration RAS et informations de connexion

Les applications qui s’exécutent sur Windows NT 4,0 et versions ultérieures, ainsi que sur Windows 95, peuvent utiliser la fonction [**RasEnumConnections**](/windows/desktop/api/Ras/nf-ras-rasenumconnectionsa) pour obtenir des informations sur les connexions existantes sur l’ordinateur local. Les informations relatives à chaque connexion incluent un descripteur de connexion et le nom de l’entrée de l’annuaire téléphonique utilisée pour établir la connexion. Vous pouvez utiliser le descripteur de connexion dans un appel à la fonction [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) pour obtenir l’état actuel de la connexion.

Windows NT Server 4,0 et versions ultérieures fournissent deux nouvelles fonctions pour récupérer les informations RAS. Windows 95does ne prend pas en charge ces fonctions.

La fonction [**RasEnumDevices**](/windows/desktop/api/Ras/nf-ras-rasenumdevicesa) retourne le nom et le type des appareils prenant en charge RAS qui sont configurés sur l’ordinateur local.

La fonction [**RasConnectionNotification**](/windows/desktop/api/Ras/nf-ras-rasconnectionnotificationa) spécifie un objet d’événement que le système signale lorsqu’une connexion RAS est créée ou arrêtée.

 

 




