---
title: Fermeture d’un appareil
description: Fermeture d’un appareil
ms.assetid: eef40f23-2c58-4deb-a6f0-3563d9c30d10
keywords:
- Commande MCI_CLOSE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 824d156baa72ee404f29ae490d4d9816078f4d15
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124368191"
---
# <a name="closing-a-device"></a>Fermeture d’un appareil

La commande [**Fermer**](close.md) ([**MCI \_ Close**](mci-close.md)) libère l’accès à un appareil ou à un fichier. MCI libère un appareil lorsque toutes les tâches utilisant un appareil l’ont fermé. Pour faciliter la gestion des appareils par MCI, votre application doit fermer chaque appareil ou fichier une fois qu’il a fini de l’utiliser.

Lorsque vous fermez un périphérique MCI externe qui utilise son propre support au lieu de fichiers (tels qu’un CD audio), le pilote laisse l’appareil dans son mode de fonctionnement actuel. Ainsi, si vous fermez un périphérique CD audio en train de jouer, même si le pilote de périphérique est libéré de la mémoire, le périphérique CD audio continue de fonctionner jusqu’à ce qu’il atteigne la fin de son contenu.

> [!Note]  
> la fermeture d’une application avec des appareils MCI ouverts peut empêcher d’autres applications d’utiliser ces appareils jusqu’à ce que Windows redémarre.

 

 

 




