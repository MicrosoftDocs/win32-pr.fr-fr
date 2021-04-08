---
title: Notions fondamentales de la sécurité RPC
description: Pour effectuer un appel de procédure distante, toutes les applications distribuées doivent créer une liaison entre le client et le serveur.
ms.assetid: 7b8adba2-19aa-4179-b6b3-ef27f4383bd4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56fdd64352df4bbefc1ec41960b78109b22510c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840650"
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

 

 




