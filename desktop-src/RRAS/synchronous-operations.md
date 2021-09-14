---
title: Opérations synchrones
description: Lorsque RasDial est appelé en tant qu’opération synchrone, la fonction ne retourne pas tant que la connexion n’a pas été établie ou qu’une erreur ne se produit pas.
ms.assetid: 5333ca88-bcec-48bc-88d2-3c6c0701802e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2463e3112c3faac4d7601023ea73f0182e2d5b73
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127121254"
---
# <a name="synchronous-operations"></a>Opérations synchrones

Lorsque [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) est appelé en tant qu’opération synchrone, la fonction ne retourne pas tant que la connexion n’a pas été établie ou qu’une erreur ne se produit pas. Le mode synchrone offre un moyen simple pour un client RAS d’établir une connexion. Le client peut simplement appeler **rasdial**, attendre la fin du retour de la fonction, puis appeler la fonction [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) pour déterminer si l’opération de connexion a réussi. Une fois la connexion établie, l’application cliente peut se terminer sans rompre la connexion. Si une erreur se produit, l’application cliente doit [arrêter l’opération de connexion avant de](disconnecting.md) se terminer.

L’inconvénient du mode synchrone est que le client ne reçoit pas de notifications de progression lorsque l’opération de connexion continue. En guise de solution de contournement pour ce manque de notifications de progression, un client en mode synchrone peut utiliser un thread distinct qui appelle [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) pour interroger et afficher l’état actuel. Toutefois, pour les clients RAS qui souhaitent recevoir des informations de progression, la méthode recommandée consiste à appeler [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) de manière asynchrone.

 

 




