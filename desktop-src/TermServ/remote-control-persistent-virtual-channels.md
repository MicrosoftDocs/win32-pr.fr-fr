---
title: Canaux virtuels persistants de contrôle à distance
description: Un canal virtuel persistant de contrôle à distance n’est pas fermé lorsqu’un contrôle à distance se connecte ou se déconnecte pour la session connectée au client. Les données continueront à être transmises et reçues via ce canal.
ms.assetid: 0c3d5429-250e-4272-8cdd-69097acfaff4
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d87054a79863df5816b30fced648ab40251a80e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380327"
---
# <a name="remote-control-persistent-virtual-channels"></a>Canaux virtuels persistants de contrôle à distance

Sur Windows XP, une DLL peut spécifier un ou plusieurs canaux virtuels comme *contrôle à distance persistant*. Un canal virtuel persistant de contrôle à distance n’est pas fermé lorsqu’un contrôle à distance se connecte ou se déconnecte pour la session connectée au client. Les données continueront à être transmises et reçues via ce canal. Les canaux virtuels que la DLL ne spécifie pas en tant que contrôle à distance persistant se ferment dans ce scénario.

Les canaux virtuels persistants de contrôle à distance sont spécifiés lors de l’appel à **VirtualChannelInit**. Pour plus d’informations à ce sujet, reportez-vous à la page de référence de [**VirtualChannelInit**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit) .

 

 




