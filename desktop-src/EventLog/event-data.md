---
description: Chaque événement peut être associé à des données spécifiques à l’événement.
ms.assetid: fa2f9e71-44c3-4569-bde4-24112a756664
title: Données d'événements
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdf6809b837d36f4cf2ddc0d74b90fe3a925f5eae7efc96973a9bf845c610bcb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901479"
---
# <a name="event-data"></a>Données d'événements

Chaque événement peut être associé à des données spécifiques à l’événement. Le observateur d’événements n’interprète pas ces données ; il affiche des données supplémentaires uniquement dans un format de texte et hexadécimal combiné. La limite maximale de la taille d’un événement dans le journal pair est de 0x3FFFF octets. Par conséquent, utilisez des données spécifiques aux événements avec modération, y compris uniquement si vous êtes certain qu’elles seront utiles pour le débogage d’un problème. Par exemple, de nombreux événements liés au réseau incluent des blocs de contrôle réseau (NCB) en tant que données spécifiques à l’événement.

Lorsque vous utilisez des données spécifiques à un événement, la dernière partie de sa chaîne de description doit fournir une note sur les informations fournies sous forme de données spécifiques à l’événement. Par exemple, le logiciel réseau peut fournir une note telle que : « (le NCB est les données d’événement.) » En guise de Convention, utilisez des parenthèses autour de ces remarques, comme indiqué dans cet exemple.

Vous pouvez également utiliser des données spécifiques aux événements pour stocker des informations que l’application peut traiter indépendamment de la observateur d’événements. Par exemple, vous pouvez écrire une visionneuse spécifique pour vos événements ou écrire un programme qui analyse le journal et crée un rapport qui contient des informations à partir des données spécifiques à l’événement.

 

 



