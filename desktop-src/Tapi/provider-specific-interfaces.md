---
description: TAPI 3 prend en charge l’intégration d’interfaces spécifiques au fournisseur de services dans les objets standard, ce qui permet aux applications de tirer parti des fonctionnalités spécifiques au fournisseur.
ms.assetid: 8077c9a7-3235-41a7-97dc-ca5f3c291ee6
title: Interfaces Provider-Specific
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f95499f005c8c3b3e854f33835b9c9b183416d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035040"
---
# <a name="provider-specific-interfaces"></a>Interfaces Provider-Specific

TAPI 3 prend en charge l’intégration d’interfaces spécifiques au fournisseur de services dans les objets standard, ce qui permet aux applications de tirer parti des fonctionnalités spécifiques au fournisseur. En outre, TAPI 3 permet aux fournisseurs de services de fournir des événements spécifiques au fournisseur aux applications en tant qu’objets COM sur la même interface que celle sur laquelle l’application reçoit des événements standard.

L’interface TAPI réalise cette intégration en regroupant des objets spécifiques au fournisseur avec les objets standard (TAPI, Address, terminal, Call et CallHub) et en distribuant ou déléguant des méthodes inconnues à ces objets spécifiques au fournisseur.

Par exemple, un fournisseur de services peut autoriser les applications à obtenir des informations sur un appel au-delà de ce qui est exposé par l’interface [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) . Le fournisseur doit définir une interface qui permet aux applications d’effectuer ces requêtes supplémentaires et d’implémenter cette interface sur un objet. Cet objet implémente également une interface d’interrogation des informations sur le fournisseur afin qu’une application puisse découvrir les types de fonctions spécifiques au fournisseur qui peuvent être disponibles.

Lorsque l’application obtient une référence à un objet d’appel, l’application peut utiliser la nouvelle interface propre au fournisseur et ses méthodes comme si elles étaient implémentées par l’objet d’appel lui-même.

Consultez la [référence MspI (Media Service Provider Interface)](media-service-provider-interface-mspi-reference.md) pour obtenir la liste de toutes les interfaces MSP standard.

Pour obtenir la liste de toutes les interfaces spécifiques au MSP IPConf, consultez la page [interfaces IPCONF MSP](ipconf-msp-interfaces.md) .

 

 



