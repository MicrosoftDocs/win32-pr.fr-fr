---
title: Instance du gestionnaire de table de routage
description: Une instance est une table distincte que le gestionnaire de tables de routage utilise pour gérer les informations de routage relatives à un sous-ensemble d’interfaces.
ms.assetid: a17233fc-2c40-4d00-8a6b-86f08fef5690
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d209f254bb9111c786bde6635b43895604785d5b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013849"
---
# <a name="routing-table-manager-instance"></a>Instance du gestionnaire de table de routage

Une instance est une table distincte que le gestionnaire de tables de routage utilise pour gérer les informations de routage relatives à un sous-ensemble d’interfaces. Les instances sont généralement utilisées pour permettre à un routeur physique d’agir comme un ensemble de routeurs virtuels, un routeur virtuel par réseau logique.

Actuellement, le gestionnaire de table de routage ne prend en charge qu’une seule instance (identifiée comme zéro, valeur par défaut). Le client peut s’inscrire auprès d’autres instances, mais aucun routeur virtuel, à l’exception de celui par défaut, n’est reconnu ou utilisé par le gestionnaire de routeur.

 

 




