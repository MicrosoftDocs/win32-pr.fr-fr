---
title: Canaux virtuels persistants de contrôle à distance
description: Un canal virtuel persistant de contrôle à distance n’est pas fermé lorsqu’un contrôle à distance se connecte ou se déconnecte pour la session connectée au client. Les données continueront à être transmises et reçues via ce canal.
ms.assetid: 0c3d5429-250e-4272-8cdd-69097acfaff4
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71206b8272fb516da9a3c39bed7f7d54edbc5227958d975bf11b114db9c13869
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988779"
---
# <a name="remote-control-persistent-virtual-channels"></a>Canaux virtuels persistants de contrôle à distance

sur Windows XP, une DLL peut spécifier un ou plusieurs canaux virtuels comme *contrôle à distance persistant*. Un canal virtuel persistant de contrôle à distance n’est pas fermé lorsqu’un contrôle à distance se connecte ou se déconnecte pour la session connectée au client. Les données continueront à être transmises et reçues via ce canal. Les canaux virtuels que la DLL ne spécifie pas en tant que contrôle à distance persistant se ferment dans ce scénario.

Les canaux virtuels persistants de contrôle à distance sont spécifiés lors de l’appel à **VirtualChannelInit**. Pour plus d’informations à ce sujet, reportez-vous à la page de référence de [**VirtualChannelInit**](/windows/desktop/api/Cchannel/nc-cchannel-virtualchannelinit) .

 

 




