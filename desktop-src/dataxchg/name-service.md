---
title: Service de noms
description: cette rubrique explique comment la bibliothèque de gestion échange dynamique de données permet à une application serveur d’inscrire les noms de service qu’elle prend en charge.
ms.assetid: 4b7e7f43-18aa-4c2e-aa2b-5ce7bb18048f
keywords:
- Windows Interface utilisateur, échange dynamique de données (DDE)
- échange dynamique de données (DDE), service de nom
- DDE (échange dynamique de données), service de nom
- échange de données, échange dynamique de données (DDE)
- Windows Interface utilisateur, échange dynamique de données Management Library (DDEML)
- bibliothèque de gestion des échange dynamique de données (DDEML), service de noms
- DDEML (bibliothèque de gestion échange dynamique de données), service de nom
- échange de données, bibliothèque de gestion des échange dynamique de données (DDEML)
- échange dynamique de données (DDE), inscription de nom de service
- DDE (échange dynamique de données), inscription de nom de service
- bibliothèque de gestion des échange dynamique de données (DDEML), inscription du nom de service
- DDEML (bibliothèque de gestion échange dynamique de données), inscription de nom de service
- échange dynamique de données (DDE), filtre de nom de service
- DDE (échange dynamique de données), filtre de nom de service
- bibliothèque de gestion des échange dynamique de données (DDEML), filtre de nom de service
- DDEML (bibliothèque de gestion échange dynamique de données), filtre de nom de service
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7346bd98979e9bd5a4aa0e43493e975d802875cf8fd0fc79d7bd002bcd0c5494
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118811646"
---
# <a name="name-service"></a>Service de noms

la bibliothèque de gestion des échange dynamique de données (DDEML) permet à une application serveur d’inscrire les noms de service qu’elle prend en charge et d’empêcher le DDEML d’envoyer des transactions [**XTYP \_ CONNECT**](xtyp-connect.md) pour les noms de service non pris en charge à la fonction de rappel échange dynamique de données (DDE) du serveur.

Les rubriques suivantes décrivent le service de noms.

-   [Inscription de nom de service](#service-name-registration)
-   [Filtre de nom de service](#service-name-filter)

## <a name="service-name-registration"></a>Inscription de nom de service

En inscrivant ses noms de service auprès du DDEML, un serveur informe d’autres applications DDE du système qu’un nouveau serveur est disponible. Un serveur inscrit un nom de service en appelant la fonction [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) et en spécifiant un descripteur de chaîne qui identifie le nom. En réponse, DDEML envoie une transaction [**\_ Register XTYP**](xtyp-register.md) à la fonction de rappel de chaque application Ddeml dans le système (à l’exception de celles qui spécifient l' \_ indicateur de filtre des inscriptions CBF Skip \_ dans la fonction [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) ). La **transaction \_ Register XTYP** passe deux descripteurs de chaîne à une fonction de rappel : la première identifie la chaîne qui spécifie le nom du service de base et la seconde identifie la chaîne spécifiant le service spécifique à l’instance. Un client utilise généralement le nom du service de base dans une liste de serveurs disponibles, de sorte que l’utilisateur peut sélectionner un serveur dans la liste. Le client utilise le nom du service spécifique à l’instance pour établir une conversation avec une instance spécifique d’une application serveur, si plusieurs instances sont en cours d’exécution.

Un serveur peut utiliser [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) pour annuler l’inscription d’un nom de service. Cette fonction force DDEML à envoyer [**XTYP \_ Annuler l’inscription**](xtyp-unregister.md) des transactions aux autres applications DDE du système, en les informant qu’elles ne peuvent plus utiliser le nom pour établir des conversations.

Un serveur doit appeler [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) pour enregistrer ses noms de service peu après l’appel de [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea). Un serveur doit annuler l’inscription de ses noms de service à l’aide de **DdeNameService** juste avant d’appeler la fonction [**DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) .

## <a name="service-name-filter"></a>Filtre de nom de service

Outre l’inscription des noms de service, [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice) permet à un serveur d’activer ou de désactiver son filtre de nom de service. Lorsqu’un serveur désactive son filtre de nom de service, DDEML envoie la transaction de [**\_ connexion XTYP**](xtyp-connect.md) à la fonction de rappel DDE du serveur chaque fois qu’un client appelle la fonction [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) , quel que soit le nom du service spécifié dans la fonction. Lorsqu’un serveur Active son filtre de nom de service, DDEML envoie la transaction de **\_ connexion XTYP** au serveur uniquement lorsque **DdeConnect** spécifie un nom de service que le serveur a spécifié dans un appel à **DdeNameService**.

Par défaut, le filtre de nom de service est activé lorsqu’une application appelle [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea). Cette valeur par défaut empêche DDEML d’envoyer la transaction [**XTYP \_ Connect**](xtyp-connect.md) à un serveur avant que le serveur ait créé les handles de chaîne dont elle a besoin. Un serveur peut désactiver son filtre de nom de service en spécifiant l' \_ indicateur FILTEROFF DNS dans un appel à [**DdeNameService**](/windows/desktop/api/Ddeml/nf-ddeml-ddenameservice). L' \_ indicateur FilterOn DNS Active le filtre.

 

 




