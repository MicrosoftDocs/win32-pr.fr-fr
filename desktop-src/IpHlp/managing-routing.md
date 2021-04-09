---
description: L’assistance IP fournit des fonctionnalités permettant de gérer le routage réseau. Utilisez les fonctions suivantes pour gérer la table de routage IP et pour obtenir d’autres informations de routage.
ms.assetid: 879b90e3-aecc-492e-9b22-9ebbf505a610
title: Gestion du routage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93ec199de19b4c8d724fbe6a2e77c3fac7dc19b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862437"
---
# <a name="managing-routing"></a>Gestion du routage

L’assistance IP fournit des fonctionnalités permettant de gérer le routage réseau. Utilisez les fonctions suivantes pour gérer la table de routage IP et pour obtenir d’autres informations de routage.

Récupérez le contenu de la table de routage IP en effectuant un appel à la fonction [**GetIpForwardTable**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getipforwardtable) . Manipuler des entrées spécifiques dans la table de routage IP à l’aide des fonctions [**CreateIpForwardEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-createipforwardentry), [**DeleteIpForwardEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-deleteipforwardentry)et [**SetIpForwardEntry**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-setipforwardentry) . Utilisez la fonction **CreateIpForwardEntry** pour ajouter une nouvelle entrée de table de routage. Utilisez la fonction **DeleteIpForwardEntry** pour supprimer une entrée existante. La fonction **SetIpForwardEntry** modifie une entrée existante.

Les fonctionnalités de gestion de routeur d’assistance IP peuvent être utilisées pour récupérer des informations sur le mode de routage des datagrammes sur le réseau. La fonction [**GetBestRoute**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestroute) récupère le meilleur itinéraire vers une adresse de destination spécifiée. La fonction [**GetBestInterface**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getbestinterface) récupère l’index de l’interface utilisée par le meilleur itinéraire vers une adresse de destination spécifiée. Enfin, la fonction [**GetRTTAndHopCount**](/windows/desktop/api/Iphlpapi/nf-iphlpapi-getrttandhopcount) récupère le temps d’aller-retour (RTT) et le nombre de tronçons vers une adresse de destination spécifiée.

 

 



