---
title: Méthodes de plug-in d’autorisation
description: Tous les points d’entrée de plug-in d’autorisation ont un mécanisme de rappel pour signaler la réussite ou l’échec de l’appel. Certains mécanismes de rappel sont appelés plusieurs fois jusqu’à ce que tous les résultats soient signalés.
ms.assetid: 6d7c1c54-fab5-431b-b123-eee6fd4dfb92
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0db09430d83e91a8df25dbbc09607c3a9ac3cad266f3a15c1738565c651271b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119955329"
---
# <a name="authorization-plug-in-methods"></a>Méthodes de plug-in d’autorisation

Tous les points d’entrée de plug-in d’autorisation ont un mécanisme de rappel pour signaler la réussite ou l’échec de l’appel. Certains mécanismes de rappel sont appelés plusieurs fois jusqu’à ce que tous les résultats soient signalés.

Le tableau suivant fournit une vue d’ensemble des méthodes de rappel d’autorisation.



| Méthode                                                                           | Description                                                          |
|----------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [**WSManPluginAuthzOperationComplete**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzoperationcomplete)   | Signale la réussite ou l’échec d’une opération utilisateur.                |
| [**WSManPluginAuthzQueryQuotaComplete**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzqueryquotacomplete) | Signale les détails de quota pertinents pour l’utilisateur spécifié.      |
| [**WSManPluginAuthzUserComplete**](/windows/desktop/api/Wsman/nf-wsman-wsmanpluginauthzusercomplete)             | Signale une autorisation de connexion utilisateur ayant réussi ou échoué. |



 

 

 




