---
title: Considérations sur la sécurité des points de contrôle
description: Lorsque vous créez un point de contrôle, vous devez prendre en compte les problèmes de sécurité suivants.
ms.assetid: 3281b4c3-d730-4273-9031-840a6ac655ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85378d7f530177bb42a6751a13f643bad984e994ae65178c0ab06cd5ce4792a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118126006"
---
# <a name="control-point-security-considerations"></a>Considérations sur la sécurité des points de contrôle

Lorsque vous créez un point de contrôle, vous devez prendre en compte les problèmes de sécurité suivants.

-   Toutes les recherches de points de contrôle sont envoyées par défaut avec une durée de vie de 1. Cela signifie que seuls les appareils au sein du même sous-réseau sont découverts. Vous pouvez configurer une durée de vie plus élevée dans le registre.
-   L’appareil et la description de service d’un appareil sont téléchargés uniquement s’ils sont présents sur le même appareil que celui qui a envoyé l’annonce de l’appareil.
-   Un appareil reçoit uniquement des demandes de contrôle et d’abonnement si ses URL de contrôle et d’abonnement se trouvent sur le même appareil que celui qui a envoyé les annonces de l’appareil.

 

 




