---
title: Instance du gestionnaire de table de routage
description: Une instance est une table distincte que le gestionnaire de tables de routage utilise pour gérer les informations de routage relatives à un sous-ensemble d’interfaces.
ms.assetid: a17233fc-2c40-4d00-8a6b-86f08fef5690
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3215baf7a3cf093ecf47e8cf9965a71e75dea17a0527949e68b2c5f929d336ab
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073919"
---
# <a name="routing-table-manager-instance"></a>Instance du gestionnaire de table de routage

Une instance est une table distincte que le gestionnaire de tables de routage utilise pour gérer les informations de routage relatives à un sous-ensemble d’interfaces. Les instances sont généralement utilisées pour permettre à un routeur physique d’agir comme un ensemble de routeurs virtuels, un routeur virtuel par réseau logique.

Actuellement, le gestionnaire de table de routage ne prend en charge qu’une seule instance (identifiée comme zéro, valeur par défaut). Le client peut s’inscrire auprès d’autres instances, mais aucun routeur virtuel, à l’exception de celui par défaut, n’est reconnu ou utilisé par le gestionnaire de routeur.

 

 




