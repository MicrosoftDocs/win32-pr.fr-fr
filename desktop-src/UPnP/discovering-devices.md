---
title: Détection des appareils
description: Vous pouvez rechercher des appareils de trois façons par type, par UDN et par la recherche asynchrone (qui est une recherche par type d’appareil).
ms.assetid: 511fb119-ad4e-406a-8a1e-fb508eceff2a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f4975c14008dcf98b7a9145320f509a3c2bceb245cd54481654ed6548a92348
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058070"
---
# <a name="discovering-devices"></a>Détection des appareils

Vous pouvez rechercher des appareils de trois manières : par type, par UDN et par recherche asynchrone (qui est une recherche par type d’appareil).

![fenêtre découvrir les appareils](images/ucp-disc.png)

**Pour découvrir des appareils**

1.  Sélectionnez le type de recherche que vous souhaitez utiliser : **Rechercher par type**, **Rechercher par UDN** ou **recherche asynchrone**.
2.  Sélectionnez le type d’appareil ou le UDN que vous souhaitez rechercher dans la liste (pour les recherches par type ou UDN). Le contenu de la liste est basé sur le contenu de la udn.txt et devtype.txt fichiers que vous avez modifiés précédemment.
3.  Cliquez sur **Démarrer la découverte**. La recherche est démarrée. Les résultats s’affichent dans la liste **appareils trouvés** . Si aucun appareil n’est trouvé, un message s’affiche pour indiquer cette condition. L’état de la progression de la recherche s’affiche dans le champ **État** .

Lorsque vous utilisez la recherche asynchrone, les nouveaux périphériques détectés s’affichent dans la liste **appareils trouvés** et dans la barre d' **État** . Une fois la recherche asynchrone terminée, la barre d' **État** affiche un message indiquant cela. Toutefois, étant donné qu’une recherche asynchrone s’exécute jusqu’à ce qu’elle soit arrêtée manuellement, les nouveaux périphériques s’affichent dans la liste **appareils trouvés** et la barre d' **État** à mesure que les appareils s’affichent sur le réseau.

Une fois que vous avez découvert des appareils, vous pouvez [les contrôler](controlling-a-device.md).

 

 




