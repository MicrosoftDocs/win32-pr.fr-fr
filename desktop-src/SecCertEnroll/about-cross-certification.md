---
description: La certification croisée permet aux entités d’une infrastructure à clé publique (PKI) d’approuver les entités d’une autre infrastructure à clé publique.
ms.assetid: 93cdb10d-4b77-4511-8c5b-c27b290f9154
title: Certification croisée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b18fcb8317145b7239464893391c5d2231ab1cb4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127095946"
---
# <a name="cross-certification"></a>Certification croisée

La certification croisée permet aux entités d’une infrastructure à clé publique (PKI) d’approuver les entités d’une autre infrastructure à clé publique. Cette relation d’approbation mutuelle est généralement prise en charge par un accord de certification croisée entre les autorités de certification (ca) de chaque infrastructure à clé publique. L’accord établit les responsabilités et la responsabilité de chaque partie.

Une relation d’approbation mutuelle entre deux autorités de certification requiert que chaque autorité de certification émette un certificat à l’autre pour établir la relation dans les deux directions. Le chemin d’accès de l’approbation n’est pas hiérarchique (aucune des autorités de certification gouvernementales n’est subordonnée à l’autre), bien que les infrastructures à clé publique distinctes soient des hiérarchies de certificats. Une fois que deux autorités de certification ont établi et spécifié les conditions de confiance et les certificats émis entre eux, les entités dans les infrastructures à clé publique distinctes peuvent interagir selon les stratégies spécifiées dans les certificats.

![diagramme de certification croisée](images/cross-certification.png)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Modèles d’approbation](about-trust-models.md)
</dt> </dl>

 

 



