---
title: Services d’autorisation
description: Un service d’autorisation est la méthode utilisée par le fournisseur de services partagés pour autoriser l’accès à une procédure distante. Les SSP peuvent fournir plusieurs services d’autorisation. Toutefois, ils sélectionnent généralement un par défaut.
ms.assetid: 5ea3cde9-96e9-4208-bb61-d0f98f23b90c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ef09377ae70d36b6d4eb7aa87794669bf247842d109cec87852db9970ea8c97
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120023417"
---
# <a name="authorization-services"></a>Services d’autorisation

Un service d’autorisation est la méthode utilisée par le fournisseur de services partagés pour autoriser l’accès à une procédure distante. Les SSP peuvent fournir plusieurs services d’autorisation. Toutefois, ils sélectionnent généralement un par défaut.

Votre application peut utiliser la méthode d’autorisation par défaut pour le fournisseur de services partagés actuel ou en spécifier une. À l’heure actuelle, Microsoft RPC prend en charge deux méthodes d’autorisation. L’un est pour le serveur de fournir une autorisation basée sur le nom du programme client. L’autre est que le serveur compare les informations d’identification d’authentification du client à la liste de contrôle d’accès (ACL) du serveur.

Pour obtenir la liste des services d’autorisation, consultez [autorisations-services, constantes](authorization-service-constants.md).

> [!Note]  
> Il est recommandé que les développeurs utilisent l’autorisation RPC \_ C \_ auth \_ aucun.

 

 

 




