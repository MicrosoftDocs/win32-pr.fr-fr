---
description: Les objets de flux sont une abstraction du flux multimédia ou des flux associés à une session d’appel.
ms.assetid: 4bd7a305-69ff-4892-bf03-df9c6479adab
title: Objets de flux
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eeb89dbacf73baaffbca9aa3791aa73937a69e80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528197"
---
# <a name="stream-objects"></a>Objets de flux

Les objets de flux sont une abstraction du flux multimédia ou des flux associés à une session d’appel. Les interfaces et les méthodes exposées sur les objets de flux et sous-flux permettent à une application d’exercer des contrôles très détaillés, tels que la suspension d’un flux, l’ajout de nouveaux types de média à une session de communication ou l’ajustement du volume audio d’un participant à une conférence spécifique.

Les deux principaux types de flux sont le flux et le sous-flux. Les interfaces et les méthodes d’une implémentation standard sont similaires pour les deux, mais le sous-flux autorise un niveau de contrôle inférieur. Tous les fournisseurs de services multimédias (MSP) doivent implémenter les interfaces de contrôle de flux de base, mais la prise en charge des sous-flux est facultative.

En outre, certains fournisseurs de services implémentent des [interfaces spécifiques au fournisseur](provider-specific-interfaces.md) pour les flux. Par exemple, le MSP IPConf fournit des contrôles de niveau participant. Pour obtenir un résumé, consultez la page [interfaces MSP ipconf](ipconf-msp-interfaces.md) . Pour les autres interfaces qui peuvent être implémentées, consultez la documentation du fournisseur de services.

Le MSP et l’interface TAPI créent des objets de flux pour un appel lors de la configuration initiale d’une session sortante ou entrante. L’application est chargée d’identifier les terminaux appropriés pour ces flux et de sélectionner les terminaux sur les flux.

Notez que dans certains cas, un MSP peut exiger que l’application arrête ou interrompt les flux avant certaines opérations d’appel de session.

Les interfaces de flux sont documentées dans la [référence MspI (Media Service Provider Interface)](media-service-provider-interface-mspi-reference.md).

L’exemple de code de [sélection de terminal](select-a-terminal.md) montre un exemple d’énumération de flux et de sélection de terminaux.

 

 



