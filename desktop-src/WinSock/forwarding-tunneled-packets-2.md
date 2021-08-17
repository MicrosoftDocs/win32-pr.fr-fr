---
description: Il existe une limitation dans le code qui reçoit les paquets encapsulés (en tunnel) et les démultiplexe vers une interface spécifique.
ms.assetid: 6148fca7-adf4-460d-afd6-79c43285af6c
title: Transfert IPv6 de paquets Tunnelés
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42138c746ea9d0ec8ea61bc3801b84a97a6bdd4c6fb6de0871e6b74447fdf28b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119132432"
---
# <a name="ipv6-forwarding-tunneled-packets"></a>Transfert IPv6 de paquets Tunnelés

Il existe une limitation dans le code qui reçoit les paquets encapsulés (en tunnel) et les démultiplexe vers une interface spécifique. Si vous souhaitez transférer des paquets tunnelés reçus via un tunnel configuré, il est nécessaire d’activer le transfert sur les interfaces 6-sur-4 et l’interface \# 2. Le simple fait d’activer le transfert sur l’interface \# 2 ne fonctionnera pas. En général, lors de la configuration d’un routeur, vous activez le transfert sur toutes les interfaces, à l’exception du bouclage.

 

 



