---
description: la configuration et la destruction des connexions point à point et point à multipoint ATM sont prises en charge en mode natif par la spécification Windows sockets 2.
ms.assetid: 07e4fcb8-f7b5-450d-a2f4-ba81267ef8ca
title: Contrôles ATM Winsock
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eed891f24c16f01025d0bd06da1ea3ec9c0cca01abdcaf3c9950229bf512f0b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051447"
---
# <a name="winsock-atm-controls"></a>Contrôles ATM Winsock

la configuration et la destruction des connexions point à point et point à multipoint ATM sont prises en charge en mode natif par la spécification Windows sockets 2. en fait, la spécification QoS de Windows sockets 2 et les mécanismes multipoint/multidiffusion indépendants des protocoles ont été conçus avec ATM à l’esprit, ainsi que d’autres protocoles. consultez la Section 2,7 et l’annexe D de la spécification de l’API Windows sockets 2 pour Windows sockets 2, la qualité de Service et la prise en charge Multipoint, respectivement. Par conséquent, aucune IOCTL propre à ATM n’a besoin d’être introduite dans ce document.

 

 



