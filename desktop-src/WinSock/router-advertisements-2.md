---
description: Le contenu des publications de routeur IPv6 est dérivé automatiquement des itinéraires publiés dans la table de routage. Les itinéraires non publiés sont utilisés pour le routage, mais sont ignorés lors de la construction des publications de routeur.
ms.assetid: 27b735db-4e87-497b-b39c-e464cf44f09e
title: Annonces de routeur IPv6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef8a7be2139c03d94e8a84eae410e9f4f2e92da6059def1ef89997138009d351
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612939"
---
# <a name="ipv6-router-advertisements"></a>Annonces de routeur IPv6

Le contenu des publications de routeur IPv6 est dérivé automatiquement des itinéraires publiés dans la table de routage. Les itinéraires non publiés sont utilisés pour le routage, mais sont ignorés lors de la construction des publications de routeur.

Les annonces de routeur pour IPv6 contiennent toujours une option d’adresse de couche de liaison source et une option MTU. La valeur de l’option MTU est extraite de l’unité de transmission de liens actuelle de l’interface d’envoi. Cette valeur peut être modifiée à l’aide de la commande IPv6 IFC MTU.

L’annonce de routeur n’a qu’une durée de vie de routeur différente de zéro si un itinéraire par défaut est publié. Un itinéraire par défaut est un itinéraire pour le préfixe de longueur nulle.

Les itinéraires sur liaison publiés entraînent des options d’informations de préfixe dans les annonces de routeur. Si le préfixe on-Link a 64 bits, l’option informations sur le préfixe a les deux bits, et les hôtes les recevant configurent automatiquement les adresses.

Une interface qui envoie des annonces de routeur configure également automatiquement les adresses pour elle-même en fonction des options d’informations de préfixe qu’elle envoie.

Une durée de vie non âgée finie sur tous les itinéraires publiés (par exemple, 30 minutes) est recommandée. Si vous décidez de retirer un itinéraire, vous pouvez modifier l’itinéraire pour avoir une durée de vie chronologique. L’itinéraire vieillit au cours de plusieurs publications de routeur, puis disparaissent du routeur et des hôtes recevant les annonces de routeur.

Les itinéraires qui hébergent les annonces par l’intermédiaire des publications de routeur et ne sont pas publiés. Les adresses sont également configurées automatiquement à partir de l’ancienneté des publications de routeur.

 

 



