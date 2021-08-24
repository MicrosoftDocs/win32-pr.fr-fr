---
title: Configuration RAS et informations de connexion
description: les Applications qui s’exécutent sur Windows NT 4,0 et versions ultérieures et Windows 95 peuvent utiliser la fonction RasEnumConnections pour obtenir des informations sur les connexions existantes sur l’ordinateur local.
ms.assetid: b738ed87-1ff5-4366-9e83-08ac08ec261c
keywords:
- Configuration et connexion, RAS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af528af93318247b7f88a50dc1db240670d17bcc48e11a7d683bfccd9054d671
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119673429"
---
# <a name="ras-configuration-and-connection-information"></a>Configuration RAS et informations de connexion

les Applications qui s’exécutent sur Windows NT 4,0 et versions ultérieures et Windows 95 peuvent utiliser la fonction [**RasEnumConnections**](/windows/desktop/api/Ras/nf-ras-rasenumconnectionsa) pour obtenir des informations sur les connexions existantes sur l’ordinateur local. Les informations relatives à chaque connexion incluent un descripteur de connexion et le nom de l’entrée de l’annuaire téléphonique utilisée pour établir la connexion. Vous pouvez utiliser le descripteur de connexion dans un appel à la fonction [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) pour obtenir l’état actuel de la connexion.

Windows NT Server 4,0 et versions ultérieures fournissent deux nouvelles fonctions pour récupérer les informations RAS. Windows 95does ne prend pas en charge ces fonctions.

La fonction [**RasEnumDevices**](/windows/desktop/api/Ras/nf-ras-rasenumdevicesa) retourne le nom et le type des appareils prenant en charge RAS qui sont configurés sur l’ordinateur local.

La fonction [**RasConnectionNotification**](/windows/desktop/api/Ras/nf-ras-rasconnectionnotificationa) spécifie un objet d’événement que le système signale lorsqu’une connexion RAS est créée ou arrêtée.

 

 




