---
title: Gestion de l’alimentation (services de base GPC)
description: Le TBS reçoit des événements de gestion de l’alimentation.
ms.assetid: 21f76bea-a313-46b7-99b3-422f17376a5a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71e21f2c6a2292b7d49fae3b15691703fa34667a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193631"
---
# <a name="power-management-tpm-base-services"></a>Gestion de l’alimentation (services de base GPC)

Le TBS reçoit des événements de gestion de l’alimentation. Lors de la réception d’une indication indiquant que le module de plateforme sécurisée (TPM) ou d’autres parties de la plateforme vont entrer dans un état d’alimentation dans lequel l’exécution est interrompue ou que l’état du module de plateforme sécurisée est perdu, le TBS vérifie si la commande en cours d’exécution est susceptible de se terminer avant que le système ne soit hors tension. En général, le TBS permet de terminer les commandes de durées courtes et moyennes, mais annule les commandes de longue durée. Une fois que la commande a été retournée, le TBS cesse d’envoyer de nouvelles commandes au module de plateforme sécurisée et se prépare à la mise en veille prolongée. Lorsque l’alimentation est restaurée, le TBS retourne le résultat de la commande à l’appelant, puis poursuit le traitement des commandes TBS en attente. Le code de gestion de l’alimentation TBS s’exécute de manière asynchrone, de sorte qu’il peut gérer les demandes de gestion de l’alimentation, même si le module de plateforme sécurisée traite une longue commande.

Lorsqu’un ordinateur entre en état de veille, y compris S3 (veille) et S4 (mise en veille prolongée), le module de plateforme sécurisée est éteint. Par conséquent, tous les États TPM non persistants sont perdus. Avant d’entrer dans ces États, les logiciels d’application sont censés se préparer à la perte des États de module de plateforme sécurisée volatils. Lorsque le système revient d’un état de veille, le TBS se synchronise avec le module de plateforme sécurisée afin que l’état de TBS soit cohérent avec l’état du module de plateforme sécurisée. Les logiciels d’application devront peut-être réémettre des commandes qui ont été interrompues.

 

 




