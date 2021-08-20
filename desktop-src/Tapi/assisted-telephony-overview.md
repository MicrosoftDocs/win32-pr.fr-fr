---
description: Une fonctionnalité intéressante de la téléphonie est le petit ensemble de fonctions appelées téléphonie assistée.
ms.assetid: 1c41f52b-f8bf-410e-a966-9323a690a4d5
title: Vue d’ensemble de la téléphonie assistée
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86adba883e558419731405c5b1274e812816944295c5743e8a91d343b42082c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117948842"
---
# <a name="assisted-telephony-overview"></a>Vue d’ensemble de la téléphonie assistée

Une fonctionnalité intéressante de la téléphonie est le petit ensemble de fonctions appelées téléphonie assistée. La téléphonie assistée est conçue pour créer des appels vocaux et des appels multimédias disponibles pour n’importe quelle application, et pas seulement pour ceux dédiés à la fonctionnalité de téléphonie. En d’autres termes, la téléphonie assistée permet aux applications d’effectuer des appels téléphoniques sans avoir à connaître les détails des services de l’API de téléphonie complète. Il étend la téléphonie aux applications de traitement de texte, aux feuilles de calcul, aux bases de données, aux gestionnaires d’informations personnelles et à d’autres applications non basées sur la téléphonie.

Pour obtenir la liste des fonctions de téléphonie assistée par TAPI 2. x de la téléphonie de base, consultez [référence des fonctions rapides TAPI](./tapi-quick-function-reference.md). TAPI 3. x prend en charge la téléphonie assistée via l’interface [**ITRequest**](/windows/desktop/api/tapi3if/nn-tapi3if-itrequest) .

L’exemple suivant illustre l’utilité de la téléphonie assistée. Une application de feuille de calcul peut incorporer des fonctions qui composent un numéro de téléphone pour un appel vocal. Tant que l’application n’a besoin d’aucun des contrôles d’appel détaillés fournis par l’API de téléphonie complète, la téléphonie assistée est le moyen le plus simple et le plus efficace de fournir des fonctionnalités de téléphonie.

![téléphonie assistée avec une application de feuille de calcul](images/assist4.png)

La téléphonie assistée et l’API de téléphonie complète sont utilisées et implémentées de différentes façons. il n’est donc pas recommandé de mélanger les appels de fonction de téléphonie assistée et les appels de fonction d’API de téléphonie dans une seule application.

## <a name="using-assisted-telephony"></a>Utilisation de la téléphonie assistée

Les applications qui utilisent des services de téléphonie assistés initialisent uniquement les demandes d’appel qui sont temporairement mises en file d’attente par TAPI. L’application destinataire de la demande récupère ces requêtes et les exécute pour le compte de l’application de téléphonie assistée. La fonction [**tapiRequestMakeCall**](/windows/win32/api/tapi/nf-tapi-tapirequestmakecall) demande l’établissement d’un appel vocal. L’application qui effectue la demande ne contrôle pas l’appel.

L’interface TAPI permet à l’utilisateur d’établir différentes ou les mêmes applications destinataires de demande pour chacun de ces services. Une application devient un destinataire de la demande en s’inscrivant auprès de [**lineRegisterRequestRecipient**](/windows/win32/api/tapi/nf-tapi-lineregisterrequestrecipient), dans laquelle **true** est spécifié comme valeur pour le paramètre *bEnable*. (La spécification de la **valeur false** annule l’inscription de l’application en tant que destinataire de la demande, ce qu’elle doit faire lorsqu’elle a déterminé que ses tâches de destinataires sont liées à la session active.) L’application sélectionne les services qu’elle souhaite gérer dans le paramètre *dwRequestMode* de **lineRegisterRequestRecipient**. Une valeur possible pour une demande est LINEREQUESTMODE \_ MAKECALL, pour indiquer que l’application doit gérer les demandes [**tapiRequestMakeCall**](/windows/win32/api/tapi/nf-tapi-tapirequestmakecall) . Si plusieurs applications s’inscrivent pour les mêmes services, un schéma de priorité est utilisé pour permettre à l’utilisateur de sélectionner l’application à privilégier pour gérer les demandes. Ce schéma de priorité est identique à celui utilisé pour le transfert d’appels et le routage des appels entrants sur la base d’une liste de noms de fichiers dans **HandoffPriorities** dans le registre.

## <a name="call-requests"></a>Demandes d’appel

La téléphonie assistée fournit des applications prenant en charge la téléphonie avec un mécanisme facile à utiliser pour passer des appels téléphoniques sans que le développeur n’ait à être entièrement responsable de la téléphonie.

La fonction [**tapiRequestMakeCall**](/windows/win32/api/tapi/nf-tapi-tapirequestmakecall) demande un appel vocal entre l’utilisateur et un tiers distant spécifié par son numéro de téléphone. La demande est transmise à l’interface TAPI, qui la transmet à une application inscrite en tant que destinataire de ces demandes. Ce destinataire est une application de gestionnaire d’appels.

Une fois que l’application a effectué la requête, l’appel est entièrement contrôlé à partir de l’application du gestionnaire d’appels, car les applications de téléphonie assistée ne peuvent pas gérer les appels. Étant donné que les aspects plus complexes de la téléphonie et de toutes les opérations de l’interface utilisateur sont gérés par l’application du gestionnaire d’appels, les applications prenant en charge la téléphonie n’ont pas besoin d’être modifiées de quelque manière que ce soit. En fait, les applications qui permettent à cette opération d’être appelées à partir de leur langage de script intégré n’ont peut-être pas besoin d’être modifiées du tout.

La fonction [**tapiGetLocationInfo**](/windows/win32/api/tapi/nf-tapi-tapigetlocationinfo) retourne à l’application le code du pays ou de la région et la ville (zone) définis par l’utilisateur dans les paramètres de l’emplacement actuel dans le panneau de configuration de la téléphonie. L’application peut utiliser ces informations pour aider l’utilisateur à créer des numéros de téléphone canoniques corrects, par exemple en les proposant par défaut lorsque de nouveaux nombres sont entrés dans une entrée d’annuaire téléphonique ou un enregistrement de base de données.

## <a name="request-recipients"></a>Destinataires de la demande

Deux types d’applications sont nécessaires pour exécuter la téléphonie assistée. Les *clients* de téléphonie assistée sont des applications qui utilisent la téléphonie assistée en appelant les fonctions qui ont le préfixe « TAPI ». Un exemple d’une telle application cliente est une feuille de calcul à laquelle une commande de menu ou un bouton de barre d’outils de **numérotation** est ajouté.

Les *serveurs* de téléphonie assistés sont des applications qui peuvent exécuter des fonctions d’API de téléphonie qui résultent d’un appel d’une autre application à une fonction de préfixe « TAPI ». Pour se faire connaître comme un serveur de téléphonie assisté, une telle application s’inscrit comme un serveur à l’aide de la fonction [**lineRegisterRequestRecipient**](/windows/win32/api/tapi/nf-tapi-lineregisterrequestrecipient) .

Les fonctions de téléphonie assistée (qui commencent par le préfixe « TAPI ») sont appelées *fonctions de requête*. Les applications de téléphonie assistée qui traitent ces demandes (les serveurs de téléphonie assistés) sont appelées *destinataires de demande*.

## <a name="processing-assisted-telephony-requests"></a>Traitement des demandes de téléphonie assistée

Le processus avec lequel les demandes sont remises et traitées est le suivant :

1.  Lorsque TAPI reçoit une demande de téléphonie assistée, il recherche un destinataire de demande, c’est-à-dire une application actuellement inscrite pour traiter ce type de demande. S’il existe un destinataire de demande, la demande est mise en file d’attente et l’application de priorité la plus élevée qui a été inscrite pour le service de cette requête reçoit un message de [**\_ demande de ligne**](./line-request.md) . Le message avertit le destinataire de la demande qu’une nouvelle demande est arrivée et contient une indication du mode de la demande.
2.  Si l’interface TAPI ne parvient pas à trouver une application en cours d’exécution pour traiter une telle requête, elle tente de lancer une application qui a été inscrite comme capable de le faire. Ces informations d’inscription sont enregistrées dans **HandoffPriorities** dans le registre. L’interface TAPI tente de lancer des applications dans l’ordre dans lequel elles sont répertoriées dans la section **HandoffPriorities** . (Voir l’étape suivante.)

    Si aucune application n’est actuellement inscrite, TAPI examine la liste des applications de traitement des requêtes sur l’entrée associée dans **HandoffPriorities**. Si la ligne associée ne figure pas dans le fichier, si aucune application n’est répertoriée sur celle-ci, ou si aucune des applications de la liste ne peut être lancée, la demande est rejetée avec l’erreur TAPIERR \_ NOREQUESTRECIPIENT.

    Lorsqu’un destinataire de la demande est lancé (qu’il ait été lancé ou non par TAPI), il doit appeler [**lineRegisterRequestRecipient**](/windows/win32/api/tapi/nf-tapi-lineregisterrequestrecipient) pendant le processus de démarrage et s’inscrire lui-même en tant que destinataire de la demande.

3.  Si une ou plusieurs applications sont répertoriées dans l’entrée, TAPI commence par la première application répertoriée (priorité la plus élevée) et tente de la lancer à l’aide de la fonction [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa) . Si la tentative de lancement de l’application échoue, TAPI tente de lancer l’application suivante dans la liste. Quand une application est lancée avec succès, TAPI met simplement en file d’attente la demande et renvoie une indication de succès à l’application, même si la demande n’a pas encore été signalée au destinataire de la demande.

    Une fois l’application destinataire de la demande lancée, elle appelle [**lineRegisterRequestRecipient**](/windows/win32/api/tapi/nf-tapi-lineregisterrequestrecipient), ce qui entraîne l’envoi d’un message de [**\_ demande de ligne**](./line-request.md) , signalant que la demande est mise en file d’attente. Si, pour une raison quelconque, l’application lancée ne s’inscrit jamais, la demande reste en file d’attente et reste dans la file d’attente indéfiniment jusqu’à ce qu’une application s’inscrive pour ce type de demande.

4.  Si l’interface TAPI détecte qu’une telle application inscrite est déjà en cours d’exécution ou qu’elle en lance une, elle met la demande en file d’attente, envoie un \_ message de demande de ligne à l’application serveur et retourne une indication de réussite pour l’appel de fonction à l’application de téléphonie assistée. Ce message de réussite indique uniquement que la demande a été acceptée et en file d’attente, et non qu’elle a été exécutée avec succès.

Lorsque l’application serveur est prête à traiter une demande, elle appelle la fonction [**lineGetRequest**](/windows/win32/api/tapi/nf-tapi-linegetrequest) . Cela lui permet de recevoir toutes les informations dont il a besoin, par exemple une adresse à composer. Il traite ensuite la demande, à l’aide des fonctions TAPI (telles que [**lineMakeCall**](/windows/win32/api/tapi/nf-tapi-linemakecall) et [**lineDrop**](/windows/win32/api/tapi/nf-tapi-linedrop)) qui seraient autrement utilisées pour passer l’appel. L’appel de **lineGetRequest** supprime la requête de l’interface TAPI et les paramètres de la demande sont copiés dans une mémoire tampon de demande allouée par l’application. La taille et l’interprétation du contenu de la mémoire tampon varient en fonction du mode de demande.

Le serveur doit s’assurer qu’il utilise les paramètres corrects lors de l’exécution des requêtes. Lorsque vous procédez ainsi, ces étapes sont suivies :

1.  Le destinataire de la demande reçoit d’abord un message de [**\_ demande de ligne**](./line-request.md) l’informant que des demandes peuvent exister dans la file d’attente des demandes. Cela indique à l’application d’appeler [**lineGetRequest**](/windows/win32/api/tapi/nf-tapi-linegetrequest) et de continuer à l’appeler jusqu’à ce que la file d’attente soit vidée (si la demande est pour effectuer un nouvel appel) ou de supprimer un appel existant. Ce message ne contient pas les paramètres de la demande, sauf dans le cas d’une demande de suppression d’un appel existant.
2.  Si la demande consiste à effectuer un nouvel appel, le serveur de téléphonie assisté utilise la fonction [**lineGetRequest**](/windows/win32/api/tapi/nf-tapi-linegetrequest) pour récupérer la demande complète, qui comprend les paramètres de la demande. Le serveur dispose maintenant de toutes les informations dont il a besoin, telles que le numéro de connexion ou l’identification du créateur de la demande. Toutefois, le serveur doit d’abord allouer la mémoire nécessaire pour stocker ces informations.
3.  Enfin, le serveur exécute la requête en appelant la fonction TAPI appropriée ou le jeu de fonctions approprié.

Si l’interface TAPI ne peut pas lancer une application pouvant servir de destinataire de demande, l’appel de téléphonie assisté échoue et retourne l’erreur TAPIERR \_ NOREQUESTRECIPIENT.

## <a name="notes-on-request-recipient-operations"></a>Remarques sur les opérations du destinataire de la demande

Les informations suivantes concernent les systèmes sur lesquels les demandes de téléphonie assistée sont traitées :

-   Le registre par défaut doit répertorier une application de gestionnaire d’appels dans la liste des priorités pour [**tapiRequestMakeCall**](/windows/win32/api/tapi/nf-tapi-tapirequestmakecall). Il serait utile, mais pas essentiel, que l’application du gestionnaire d’appels ait une option de menu qui permette aux utilisateurs de définir la priorité la plus élevée.
-   Quand une application de destinataire de téléphonie assistée est lancée automatiquement par TAPI et s’il s’agit de la seule application TAPI dans le système, cette action Initialise l’interface TAPI. Si l’application de destinataire de téléphonie assistée initialise et arrête l’appareil de ligne avant d’inscrire des demandes de téléphonie assistée, TAPI est également arrêté et la demande de téléphonie assistée est perdue. Les demandes de téléphonie assistée peuvent également être perdues lorsqu’une autre application TAPI lancée exécute un initialisation et un arrêt.

 

 
