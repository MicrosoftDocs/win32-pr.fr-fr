---
description: Les lampes sur un appareil téléphonique peuvent être allumées dans divers modes d’éclairage différents.
ms.assetid: d8e8ef57-9faa-4122-b99a-3956362cd9d8
title: Lampes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e01005c282b7a86b4b8c8ee27348ba4cf8d43db9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035042"
---
# <a name="lamps"></a>Lampes

Les lampes sur un appareil téléphonique peuvent être allumées dans divers modes d’éclairage différents. Contrairement aux modèles de sonnerie, les modes de lampe sont plus uniformes pour les différents groupes de téléphones de différents fournisseurs. Un ensemble commun de modes de lampe est défini par l’API. Une lampe identifiée par son identificateur de bouton de lampe peut être allumée dans un mode de lampe donné. Une lampe peut également être interrogée pour son mode de lampe actuel.

Les fonctions TAPI utilisées pour les lampes sont [**phoneSetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonesetlamp), qui illumine une lampe sur un appareil téléphonique ouvert spécifié dans un mode d’éclairage de lampe donné et [**phoneGetLamp**](/windows/desktop/api/Tapi/nf-tapi-phonegetlamp), qui retourne le mode de lampe actuel de la lampe spécifiée.

Quand une lampe d’appareil téléphonique est modifiée, un message [**d' \_ État de téléphone**](phone-state.md) est envoyé à l’application pour notifier l’application du changement d’État. Les paramètres de ce message fournissent une indication de la modification.

 

 



