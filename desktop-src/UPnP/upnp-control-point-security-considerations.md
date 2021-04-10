---
title: Considérations sur la sécurité des points de contrôle
description: Lorsque vous créez un point de contrôle, vous devez prendre en compte les problèmes de sécurité suivants.
ms.assetid: 3281b4c3-d730-4273-9031-840a6ac655ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0165ad0c8a721b10d5cc34c49947a98f2c15d1de
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940178"
---
# <a name="control-point-security-considerations"></a>Considérations sur la sécurité des points de contrôle

Lorsque vous créez un point de contrôle, vous devez prendre en compte les problèmes de sécurité suivants.

-   Toutes les recherches de points de contrôle sont envoyées par défaut avec une durée de vie de 1. Cela signifie que seuls les appareils au sein du même sous-réseau sont découverts. Vous pouvez configurer une durée de vie plus élevée dans le registre.
-   L’appareil et la description de service d’un appareil sont téléchargés uniquement s’ils sont présents sur le même appareil que celui qui a envoyé l’annonce de l’appareil.
-   Un appareil reçoit uniquement des demandes de contrôle et d’abonnement si ses URL de contrôle et d’abonnement se trouvent sur le même appareil que celui qui a envoyé les annonces de l’appareil.

 

 




