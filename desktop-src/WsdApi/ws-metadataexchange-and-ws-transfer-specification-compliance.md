---
description: Avant le 2006 août, WS-MetadataExchange défini sa propre méthode d’échange de métadonnées, utilisée par le profil de périphériques pour les services Web (DPWS).
ms.assetid: 2441beac-ee40-405a-8e98-8b8d65477911
title: Conformité à la spécification WS-MetadataExchange et WS-Transfer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db78bec29d96b4ba3671f176349a56b891cd4d642762670fd16cf582da53208c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793969"
---
# <a name="ws-metadataexchange-and-ws-transfer-specification-compliance"></a>Conformité à la spécification WS-MetadataExchange et WS-Transfer

Avant le 2006 août, [WS-MetadataExchange](https://schemas.xmlsoap.org/ws/2004/09/mex/) définissait [sa propre méthode](get--metadata-exchange--http-request-and-message.md) d’échange de métadonnées, qui était utilisée par le [profil de périphériques pour les services Web](https://specs.xmlsoap.org/ws/2006/02/devprof/) (DPWS). La version 1,1 de la spécification de WS-MetadataExchange a remplacé cette méthode par la méthode d’extraction définie dans la spécification WS-Transfer.

Dans le modèle actuel, WS-Transfer fournit la méthode d' [extraction](get--metadata-exchange--http-request-and-message.md) et ne fait pas référence au type du corps. WS-MetadataExchange décrit le format du corps et un mécanisme pour l’empaquetage de plusieurs éléments de métadonnées dans une réponse unique, et DPWS décrit des éléments de métadonnées spécifiques qu’un service doit inclure dans une réponse de métadonnées.

WSDAPI ne prend pas entièrement en charge la spécification WS-Transfer. Étant donné que seule la méthode d' [extraction](get--metadata-exchange--http-request-and-message.md) est requise pour les appareils, aucune autre partie de WS-Transfer n’a été implémentée. En outre, WSDAPI n’implémente pas la méthode GetMetadata facultative décrite dans WS-MetadataExchange.

 

 



