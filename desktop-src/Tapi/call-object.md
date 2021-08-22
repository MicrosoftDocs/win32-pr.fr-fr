---
description: L’objet d’appel représente une connexion d’adresses entre l’adresse locale et une ou plusieurs autres adresses.
ms.assetid: 67c063ba-8b12-40d6-9011-923bdee8b214
title: Objet d’appel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb2b37ff30e1e47cc3daf5e3152d5051161535f0f4e6cdcb9d27d5537619e967
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118870015"
---
# <a name="call-object"></a>Objet d’appel

L’objet d’appel représente la connexion d’une adresse entre l’adresse locale et une ou plusieurs autres adresses. Tout le contrôle d’appel est effectué par le biais de l’objet d’appel. [**ITBasicCallControl**](/windows/desktop/api/tapi3if/nn-tapi3if-itbasiccallcontrol) et [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) sont les interfaces les plus fréquemment utilisées sur l’objet d’appel. Ces interfaces implémentent une variété d’opérations et de requêtes, telles que l’acquisition de pointeurs d’interface pour les flux multimédias ou l’obtention de l’ID de l’appelant. Consultez les principales sections de la vue d’ensemble sur les [opérations de session](session-operations-ovr.md) et les [informations de session](session-information-ovr.md) pour les révisions de celles prises en charge par TAPI.

Un fournisseur de services multimédias peut implémenter des [interfaces spécifiques au fournisseur](provider-specific-interfaces.md), qui sont agrégées sur un objet d’appel par l’interface TAPI. Pour plus d’informations sur l’implémentation d’un fournisseur, consultez la documentation du fournisseur de services.

Les exemples [créer un appel](make-a-call.md) et [recevoir un](receive-a-call.md) code d’appel montrent quelques illustrations de l’utilisation d’un objet d’appel.

Consultez [appeler des interfaces d’objet](call-object-interfaces.md) pour obtenir la liste de toutes les interfaces associées à l’objet d’appel.

 

 



