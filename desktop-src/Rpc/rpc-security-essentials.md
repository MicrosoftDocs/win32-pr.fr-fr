---
title: Notions fondamentales de la sécurité RPC
description: Pour effectuer un appel de procédure distante, toutes les applications distribuées doivent créer une liaison entre le client et le serveur.
ms.assetid: 7b8adba2-19aa-4179-b6b3-ef27f4383bd4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8ed8bce6f97ecfc7bd257d20eebbb35d068624fe017c01a662b47fceb463b98
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118926030"
---
# <a name="rpc-security-essentials"></a>Notions fondamentales de la sécurité RPC

Pour effectuer un appel de procédure distante, toutes les applications distribuées doivent créer une liaison entre le client et le serveur. Pour plus d’informations sur les liaisons, consultez [liaison et Handles](binding-and-handles.md). Pour effectuer un appel de procédure distante sécurisé, des étapes supplémentaires sont nécessaires. Tout d’abord, le serveur doit choisir un fournisseur de sécurité (service d’authentification dans la terminologie DCE). Il doit ensuite décider de son mécanisme d’authentification. Après cela, le client obtient une liaison au serveur et demande un appel de procédure distante sécurisé à partir de l’exécution RPC, et spécifie différentes options de sécurité, telles que le fournisseur de sécurité, les options QOS de sécurité, etc.

Cette section explique les concepts et les informations essentiels nécessaires à l’utilisation des fonctions RPC pour créer un client et un serveur pour une application distribuée authentifiée. Elle est organisée dans les rubriques suivantes :

-   [Noms principaux](principal-names.md)
-   [Niveaux d’authentification](authentication-levels.md)
-   [Services d’authentification](authentication-services.md)
-   [Informations d’identification d’authentification du client](client-authentication-credentials.md)
-   [Services d’autorisation](authorization-services.md)
-   [Qualité de service](quality-of-service.md)
-   [Fonctions d’autorisation](authorization-functions.md)
-   [Fonctions d’acquisition de clé](key-acquisition-functions.md)
-   [Emprunt d'identité de client](client-impersonation.md)

 

 




