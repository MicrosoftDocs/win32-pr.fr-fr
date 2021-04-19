---
description: Les contrôles de centre d’appels étendent le modèle d’objet TAPI 3 pour prendre en charge les exigences de systèmes ACD (Automatic Call distribution).
ms.assetid: cb7a4231-6249-4ab9-9de7-243768a18775
title: Utilisation des contrôles de centre d’appels
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdc01cac4b068c5ec17ff5794e2e7ffff46dbf95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106531826"
---
# <a name="using-call-center-controls"></a>Utilisation des contrôles de centre d’appels

Les contrôles de centre d’appels étendent le modèle d’objet TAPI 3 pour prendre en charge les exigences de systèmes ACD (Automatic Call distribution). Un centre d’appels est un lieu avec les agents ou les opérateurs des banques de téléphones qui effectuent des appels téléphoniques sortants ou des champs entrants. Par exemple, une société bancaire ou une société de carte de crédit utilisera un centre d’appels pour traiter les demandes de compte.

Les applications de centre d’appels sont divisées en trois types de base :

-   [Proxy ACD](acd-proxy.md): gère les sessions entrantes ou sortantes sur le serveur, qui peuvent être issues d’un commutateur téléphonique propriétaire vers une passerelle Internet.
-   [Client de l’agent ACD](acd-agent-client.md): services d’un agent individuel recevant ou effectuant des appels.
-   ACD superviseur client : fournit une vue d’ensemble des opérations de l’agent et du ACD.

> [!Note]  
> Pour Windows 2000, la fonctionnalité de proxy est disponible à l’aide de TAPI 2,2, et les fonctions de superviseur ne sont pas implémentées.

 

La section Exemples de l’SDK Windows contient des exemples de code ACD sous netds \\ TAPI \\ Tapi2 \\ ACD et netds \\ TAPI \\ Tapi3 \\ ACD.

 

 



