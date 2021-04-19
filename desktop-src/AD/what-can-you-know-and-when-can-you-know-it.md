---
title: Que pouvez-vous savoir, et quand le savoir
description: Les applications sensibles aux États induits par la latence doivent reconnaître les États des problèmes et prendre les mesures appropriées.
ms.assetid: d1d0135e-2d67-47dd-82ac-4869203ce85e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e9a8a6c6def8475946ad5faa63615d17742fbcb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106541811"
---
# <a name="what-can-you-know-and-when-can-you-know-it"></a>Que pouvez-vous savoir, et quand pouvez-vous le savoir ?

Les applications sensibles aux États induits par la latence doivent reconnaître les États des problèmes et prendre les mesures appropriées. Deux États posent problème : le décalage de version et la mise à jour partielle. Le décalage de version n’est pas détectable en examinant le service d’annuaire (n’oubliez pas le axiome de l’informatique distribuée indiqué dans [pourquoi Active Directory Domain Services utiliser ce modèle de réplication](why-active-directory-domain-services-uses-this-replication-model.md)). Une mise à jour partielle peut être détectée en ajoutant des métadonnées aux objets qui composent le jeu associé. Des suggestions pour ces métadonnées s’affichent dans les sections suivantes de ce document. Certaines stratégies d’évitement peuvent être nécessaires pour réduire le risque de décalage de version et de mise à jour partielle. Ces stratégies sont également abordées dans les sections suivantes de ce document.

 

 




