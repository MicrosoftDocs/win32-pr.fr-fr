---
description: Notification de suppression de l’appareil
ms.assetid: 0b96231a-f990-4c1c-8d00-cafeb3985ab3
title: Notification de suppression de l’appareil
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3cc73aba6ad02eb1dfba095b6f45b9fa6c067c51dbe165f4ded86141dae1c66
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120052019"
---
# <a name="device-removal-notification"></a>Notification de suppression de l’appareil

Si l’utilisateur supprime un appareil Plug-and-Play que le graphique utilisait, le gestionnaire de graphique de filtre publie un événement de [**\_ \_ perte d’appareil ce**](ec-device-lost.md) . Si le périphérique redevient disponible, le gestionnaire de graphique de filtre publie un autre événement de **\_ \_ perte d’appareil EC** . Toutefois, l’état précédent du filtre de capture n’est plus valide. L’application doit reconstruire le graphique pour utiliser l’appareil.

DirectShow n’envoie aucun événement lorsqu’un nouvel appareil est branché. Pour savoir quand un nouvel appareil est disponible, l’application peut surveiller les \_ messages de fenêtre WM DEVICECHANGE. Pour plus d’informations, consultez « Gestion des périphériques » dans la documentation du kit de développement Platform SDK.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Notification d’événements dans DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 



