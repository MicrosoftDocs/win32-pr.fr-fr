---
title: Que pouvez-vous savoir, et quand le savoir
description: Les applications sensibles aux États induits par la latence doivent reconnaître les États des problèmes et prendre les mesures appropriées.
ms.assetid: d1d0135e-2d67-47dd-82ac-4869203ce85e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05845de7fe6f578627ced8c7acbc8e14065a779f67e6e8c6a5ce281514640be0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118182243"
---
# <a name="what-can-you-know-and-when-can-you-know-it"></a>Que pouvez-vous savoir, et quand pouvez-vous le savoir ?

Les applications sensibles aux États induits par la latence doivent reconnaître les États des problèmes et prendre les mesures appropriées. Deux États posent problème : le décalage de version et la mise à jour partielle. Le décalage de version n’est pas détectable en examinant le service d’annuaire (n’oubliez pas le axiome de l’informatique distribuée indiqué dans [pourquoi Active Directory Domain Services utiliser ce modèle de réplication](why-active-directory-domain-services-uses-this-replication-model.md)). Une mise à jour partielle peut être détectée en ajoutant des métadonnées aux objets qui composent le jeu associé. Des suggestions pour ces métadonnées s’affichent dans les sections suivantes de ce document. Certaines stratégies d’évitement peuvent être nécessaires pour réduire le risque de décalage de version et de mise à jour partielle. Ces stratégies sont également abordées dans les sections suivantes de ce document.

 

 




