---
title: échange dynamique de données
description: cette section fournit des instructions pour l’implémentation de l’échange dynamique de données pour les applications qui ne peuvent pas utiliser la bibliothèque de gestion des échange dynamique de données (DDEML).
ms.assetid: vs|winui|~\winui\windowsuserinterface\dataexchange\dynamicdataexchange.htm
keywords:
- échange dynamique de données (DDE), à propos de
- DDE (échange dynamique de données), à propos de
- échange de données, échange dynamique de données (DDE)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 91d5fa52078c2fa1d2e67a74d019535c801c4c96
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126922847"
---
# <a name="dynamic-data-exchange"></a>échange dynamique de données

cette section fournit des instructions pour l’implémentation de l’échange dynamique de données pour les applications qui ne peuvent pas utiliser la bibliothèque de gestion des échange dynamique de données (DDEML). pour plus d’informations sur DDEML, consultez [bibliothèque de gestion des échange dynamique de données](dynamic-data-exchange-management-library.md).

### <a name="overviews"></a>Vues d'ensemble



| Nom                                                           | Description                                                        |
|----------------------------------------------------------------|--------------------------------------------------------------------|
| [À propos de échange dynamique de données](about-dynamic-data-exchange.md) | Décrit le transfert de données entre les applications.<br/>       |
| [Utilisation de échange dynamique de données](using-dynamic-data-exchange.md) | Fournit des exemples de code relatifs à l’échange dynamique de données.<br/> |
| [Référence DDE](dynamic-data-exchange-reference.md)           | Référence de l’API.<br/>                                      |



 

### <a name="dde-functions"></a>Fonctions DDE



| Nom                                                             | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DdeSetQualityOfService**](/windows/desktop/api/Dde/nf-dde-ddesetqualityofservice)         | spécifie la qualité de service (QOS) qu’une application de échange dynamique de données brute désire pour les futures conversations DDE qu’elle initialise. La qualité de service spécifiée s’applique à toutes les conversations démarrées pendant que ces paramètres sont en place. La qualité de service d’une conversation DDE dure pour la durée de la conversation ; les appels à la fonction [**DdeSetQualityOfService**](/windows/desktop/api/Dde/nf-dde-ddesetqualityofservice) pendant une conversation n’affectent pas la qualité de service de cette conversation. <br/> |
| [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam)                           | Libère la mémoire spécifiée par le paramètre *lParam* d’un message DDE publié. Une application recevant un message DDE publié doit appeler cette fonction après avoir utilisé la fonction [**UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam) pour décompresser la valeur *lParam* . <br/>                                                                                                                                                                                                     |
| [**ImpersonateDdeClientWindow**](/windows/desktop/api/Dde/nf-dde-impersonateddeclientwindow) | Permet à une application de serveur DDE d’emprunter l’identité du contexte de sécurité d’une application cliente DDE. Cela protège les données du serveur sécurisé contre les clients DDE non autorisés. <br/>                                                                                                                                                                                                                                                                                                      |
| [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam)                           | Compresse une valeur *lParam* DDE dans une structure interne utilisée pour partager des données DDE entre des processus.<br/>                                                                                                                                                                                                                                                                                                                                                                 |
| [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam)                         | Permet à une application de réutiliser un paramètre DDE *lParam* condensé, plutôt que d’allouer une nouvelle valeur *lParam* compressée. L’utilisation de cette fonction réduit les réallocations pour les applications qui transmettent des messages DDE compressés. <br/>                                                                                                                                                                                                                                                          |
| [**UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam)                       | Décompresse une valeur *lParam* DDE reçue à partir d’un message DDE publié. <br/>                                                                                                                                                                                                                                                                                                                                                                                                  |



 

### <a name="dde-messages"></a>Messages DDE



| Nom                                         | Description                                                                                                                                                                                                                                                                                      |
|----------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_lancement de DDE de WM \_**](wm-dde-initiate.md) | Lance une conversation avec une application serveur qui répond aux noms d’application et de rubrique spécifiés. Lors de la réception de ce message, toutes les applications serveur avec des noms qui correspondent à l’application spécifiée et qui prennent en charge la rubrique spécifiée sont censées la reconnaître.<br/> |



 

### <a name="dde-notifications"></a>Notifications DDE



| Nom                                           | Description                                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ACK DDE \_ ACK**](wm-dde-ack.md)             | Nnotifies une application DDE de la réception et du traitement des messages suivants : [**WM \_ DDE \_**](wm-dde-poke.md)en cours [**d' \_ \_ exécution, Execute DDE Execute**](wm-dde-execute.md), [**WM DDE \_ \_ Data**](wm-dde-data.md), [**WM \_ DDE \_ readvit**](wm-dde-advise.md), [**WM \_ DDE \_ unadvi**](wm-dde-unadvise.md), [**WM \_ DDE \_ initiate**](wm-dde-initiate.md)ou [**WM DDE \_ \_ Request**](wm-dde-request.md) (dans certains cas). <br/> |
| [**\_avis DDE \_ WM**](wm-dde-advise.md)       | Une application cliente DDE publie le message de [**\_ \_ notification**](wm-dde-advise.md) de l’échange de données (DDE) WM dans une application de serveur DDE pour demander au serveur de fournir une mise à jour pour un élément de données à chaque modification de l’élément. <br/>                                                                                                                                                                                                              |
| [**\_données DDE \_ WM**](wm-dde-data.md)           | Une application de serveur DDE publie un message de [**\_ \_ données WM**](wm-dde-data.md) dans une application cliente DDE pour transmettre un élément de données au client ou pour notifier au client la disponibilité d’un élément de données. <br/>                                                                                                                                                                                                           |
| [**\_exécution DDE de WM \_**](wm-dde-execute.md)     | Une application cliente DDE publie un message [**WM d' \_ \_ exécution DDE**](wm-dde-execute.md) dans une application de serveur DDE pour envoyer une chaîne au serveur à traiter en tant que série de commandes. L’application serveur doit poster un message d' [**\_ \_ accusé**](wm-dde-ack.md) de réception DDE en réponse. <br/>                                                                                                                      |
| [**en-dessous du protocole WM \_ DDE \_**](wm-dde-poke.md)           | Une application cliente DDE publie un message WM de l’application DDE dans une application de serveur DDE. [**\_ \_**](wm-dde-poke.md) Un client utilise ce message pour demander au serveur d’accepter un élément de données non sollicité. Le serveur doit répondre avec un message d' [**\_ \_ accusé**](wm-dde-ack.md) de réception DDE qui indique s’il a accepté l’élément de données. <br/>                                                                                   |
| [**\_requête DDE \_ WM**](wm-dde-request.md)     | Une application cliente DDE publie un message de [**\_ \_ demande d’échange**](wm-dde-request.md) de données (DDE) WM dans une application de serveur DDE pour demander la valeur d’un élément de données. <br/>                                                                                                                                                                                                                                                              |
| [**arrêt de l’échange de thread WM \_ \_**](wm-dde-terminate.md) | Une application DDE (client ou serveur) publie un message [**WM \_ DDE \_ Terminate**](wm-dde-terminate.md) pour mettre fin à une conversation. <br/>                                                                                                                                                                                                                                                                                  |
| [**informer de l' \_ échange de \_ notification**](wm-dde-unadvise.md)   | Une application cliente DDE publie un message « [**WM \_ DDE \_ Unadvise**](wm-dde-unadvise.md) » pour informer une application serveur DDE que l’élément spécifié ou un format de presse-papiers particulier pour l’élément ne doit plus être mis à jour. Cela met fin au lien de données chaud ou chaud pour l’élément spécifié. <br/>                                                                                                                     |



 

### <a name="dde-structures"></a>Structures DDE



| Nom                           | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|--------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack)       | Contient des indicateurs d’État qu’une application DDE transmet à son partenaire dans le cadre du message d' [**\_ \_ accusé**](wm-dde-ack.md) de réception DDE de WM. Les indicateurs fournissent des détails sur la réponse de l’application aux messages [**WM \_ DDE \_ Data**](wm-dde-data.md), [**WM \_ DDE \_**](wm-dde-poke.md)en action, [**WM DDE \_ \_ EXECUTe**](wm-dde-execute.md), [**WM \_ DDE \_ readvi**](wm-dde-advise.md), [**WM \_ DDE \_ Unadvise**](wm-dde-unadvise.md)et une [**\_ \_ demande DDE**](wm-dde-request.md)WM. <br/> |
| [**DDEADVISE**](/windows/desktop/api/Dde/ns-dde-ddeadvise) | Contient des indicateurs qui spécifient comment une application de serveur DDE doit envoyer des données à une application cliente pendant une boucle de notification. Un client transmet un handle à une structure [**DDEADVISE**](/windows/desktop/api/Dde/ns-dde-ddeadvise) à un serveur dans le cadre d’un message de [**\_ \_ notification**](wm-dde-advise.md) de l’échange de messages. <br/>                                                                                                                                                                                               |
| [**DDEDATA**](/windows/desktop/api/Dde/ns-dde-ddedata)     | Contient les données et les informations sur les données envoyées dans le cadre d’un message de données de l' [**\_ échange de \_ données (DDE) WM**](wm-dde-data.md) . <br/>                                                                                                                                                                                                                                                                                                                                                       |
| [**DDEPOKE**](/windows/desktop/api/Dde/ns-dde-ddepoke)     | Contient les données et les informations relatives aux données, envoyées dans le cadre d’un message de l’élément de transfert de données de l' [**\_ \_ échange WM**](wm-dde-poke.md) . <br/>                                                                                                                                                                                                                                                                                                                                                       |
| [**HSZPAIR**](/windows/win32/api/ddeml/ns-ddeml-hszpair)     | Contient un nom de service DDE et un nom de rubrique. Une application de serveur DDE peut utiliser cette structure pendant une transaction [**XTYP \_ WILDCONNECT**](xtyp-wildconnect.md) pour énumérer les paires de rubriques de services qu’elle prend en charge. <br/>                                                                                                                                                                                                                                                   |



 

 

 





