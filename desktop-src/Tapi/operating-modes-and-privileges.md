---
description: L’application peut demander l’un des deux modes de fonctionnement lors de l’ouverture d’un appareil téléphonique.
ms.assetid: 2bb16fbe-883e-4734-a071-f14f5e5737e3
title: Modes de fonctionnement et privilèges
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44f7d3c1f6b7049c3986b96734a537906dc62166c48d62e549684cdaa6d35ba2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012469"
---
# <a name="operating-modes-and-privileges"></a>Modes de fonctionnement et privilèges

L’application peut demander l’un des deux modes de fonctionnement lors de l’ouverture d’un appareil téléphonique. Ces modes reflètent les privilèges que l’application demande pour l’appareil :

-   L’ouverture d’un téléphone pour les privilèges du moniteur permet à l’application de déterminer l’état de l’appareil téléphonique. Les messages sont envoyés à l’application lorsque des modifications d’État sur l’appareil téléphonique sont détectées.
-   Une application qui ouvre un appareil téléphonique pour des privilèges de propriétaire peut utiliser des opérations qui modifient l’état du périphérique téléphonique. Le privilège propriétaire comprend également des privilèges d’analyse complets. À tout moment, un appareil téléphonique donné ne peut être ouvert qu’une seule fois pour les privilèges du propriétaire, mais plusieurs fois pour les privilèges du moniteur. Toutes les opérations **phoneSet** requièrent des privilèges de propriétaire, tandis que toutes les opérations **phoneGet** requièrent uniquement des privilèges d’analyse.

 

 



