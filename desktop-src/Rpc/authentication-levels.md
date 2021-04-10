---
title: Niveaux d’authentification
description: Microsoft RPC fournit plusieurs niveaux d’authentification.
ms.assetid: d9ed938e-4cd4-4355-8d08-830f955dd00c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c5fd25efb84b4ee2834e6f79c7fdd21dd903d55
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104196725"
---
# <a name="authentication-levels"></a>Niveaux d’authentification

Microsoft RPC fournit plusieurs niveaux d’authentification. En fonction du niveau d’authentification, l’origine du trafic (le principal de sécurité qui a envoyé le trafic) peut être vérifiée lorsque la connexion est établie, lorsque le client démarre un nouvel appel de procédure distante ou au cours de chaque échange de paquets entre le client et le serveur.

Même lorsque l’expéditeur du trafic est vérifié, la sécurité est toujours faible, car cette vérification ne garantit pas que le paquet n’a pas été modifié ou endommagé en cours d’acheminement. Il vérifie uniquement que le paquet provient du principal donné. Pour une sécurité accrue, les applications distribuées peuvent définir la bibliothèque Runtime RPC pour vérifier qu’aucune des données échangées entre le client et le serveur n’est modifiée. La bibliothèque RPC peut également chiffrer le contenu de chaque paquet avant de l’envoyer. En général, les applications qui souhaitent sécuriser leur trafic doivent utiliser uniquement les deux derniers niveaux : l’intégrité et la confidentialité.

Sachez que les niveaux d’authentification plus élevés nécessitent une surcharge de calcul plus élevée. En tant que développeur, vous devez décider de ce qui est plus important pour votre application : la vitesse ou la sécurité. La plupart des développeurs trouvent qu’avec des tests de performances, ils peuvent atteindre des niveaux de performances acceptables tout en conservant une sécurité appropriée.

Les parties client et serveur de l’application distribuée doivent utiliser le même niveau d’authentification. Pour obtenir la liste des niveaux d’authentification RPC, consultez [constantes au niveau de l’authentification](authentication-level-constants.md).

 

 




