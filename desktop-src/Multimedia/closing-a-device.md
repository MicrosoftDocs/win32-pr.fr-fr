---
title: Fermeture d’un appareil
description: Fermeture d’un appareil
ms.assetid: eef40f23-2c58-4deb-a6f0-3563d9c30d10
keywords:
- Commande MCI_CLOSE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29f81ddaf42ef5509b55271159b8e36ac56584b92734a6b04e5b555041596530
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119498079"
---
# <a name="closing-a-device"></a>Fermeture d’un appareil

La commande [**Fermer**](close.md) ([**MCI \_ Close**](mci-close.md)) libère l’accès à un appareil ou à un fichier. MCI libère un appareil lorsque toutes les tâches utilisant un appareil l’ont fermé. Pour faciliter la gestion des appareils par MCI, votre application doit fermer chaque appareil ou fichier une fois qu’il a fini de l’utiliser.

Lorsque vous fermez un périphérique MCI externe qui utilise son propre support au lieu de fichiers (tels qu’un CD audio), le pilote laisse l’appareil dans son mode de fonctionnement actuel. Ainsi, si vous fermez un périphérique CD audio en train de jouer, même si le pilote de périphérique est libéré de la mémoire, le périphérique CD audio continue de fonctionner jusqu’à ce qu’il atteigne la fin de son contenu.

> [!Note]  
> la fermeture d’une application avec des appareils MCI ouverts peut empêcher d’autres applications d’utiliser ces appareils jusqu’à ce que Windows redémarre.

 

 

 




