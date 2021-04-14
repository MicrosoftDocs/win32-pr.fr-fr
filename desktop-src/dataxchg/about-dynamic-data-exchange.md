---
title: À propos de échange dynamique de données
description: Cette rubrique explique comment transférer des données entre des applications.
ms.assetid: 0bcd8de4-a6f0-4f2a-8b9d-0b1b638925fb
keywords:
- Échange dynamique de données (DDE), à propos de
- DDE (échange dynamique de données), à propos de
- échange de données, échange dynamique de données (DDE)
- Échange dynamique de données (DDE), liaison à des données en temps réel
- DDE (échange dynamique de données), liaison à des données en temps réel
- Échange dynamique de données (DDE), création de documents composés
- DDE (échange dynamique de données), création de documents composés
- Échange dynamique de données (DDE), requêtes de données
- DDE (échange dynamique de données), requêtes de données
- Échange dynamique de données (DDE), exemples
- DDE (échange dynamique de données), exemples
- Échange dynamique de données (DDE), emprunt d’identité
- DDE (échange dynamique de données), emprunt d’identité
- Échange dynamique de données (DDE), messages
- DDE (échange dynamique de données), messages
- Échange dynamique de données (DDE), atomes
- DDE (échange dynamique de données), atomes
- Échange dynamique de données (DDE), objets de mémoire partagée
- DDE (échange dynamique de données), objets de mémoire partagée
- Échange dynamique de données (DDE), fonctions de compression de paramètre
- DDE (échange dynamique de données), fonctions de compression des paramètres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d38574e9182255e8f6761520aea60575d8affbc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382463"
---
# <a name="about-dynamic-data-exchange"></a>À propos de échange dynamique de données

Windows fournit plusieurs méthodes pour transférer des données entre les applications. Une méthode consiste à utiliser le protocole échange dynamique de données (DDE). Le protocole DDE est un ensemble de messages et d’instructions. Elle envoie des messages entre les applications qui partagent des données et utilise la mémoire partagée pour échanger des données entre les applications. Les applications peuvent utiliser le protocole DDE pour les transferts de données à usage unique et pour les échanges continus dans lesquels les applications envoient des mises à jour les unes aux autres au fur et à mesure que de nouvelles données deviennent disponibles.

Windows prend également en charge la bibliothèque de gestion des échange dynamique de données (DDEML). DDEML est une bibliothèque de liens dynamiques (DLL) que les applications peuvent utiliser pour partager des données. DDEML fournit des fonctions et des messages qui simplifient la tâche d’ajout de la fonctionnalité DDE à une application. Au lieu d’envoyer, de publier et de traiter des messages DDE directement, une application utilise les fonctions DDEML pour gérer les conversations DDE. (Une conversation DDE est l’interaction entre les applications client et serveur.)

DDEML fournit également une fonctionnalité de gestion des chaînes et des données partagées par les applications DDE. Au lieu d’utiliser des atomes et des pointeurs vers des objets mémoire partagés, les applications DDE créent et échangent des handles de chaîne, qui identifient les chaînes et les handles de données qui identifient les objets mémoire. Le DDEML permet également à une application serveur d’inscrire les noms de service qu’elle prend en charge. Les noms sont diffusés à d’autres applications dans le système, qui peuvent utiliser les noms pour se connecter au serveur. En outre, le DDEML garantit la compatibilité entre les applications DDE en les forçant à implémenter le protocole DDE de manière cohérente.

Les applications existantes qui utilisent le protocole DDE basé sur des messages sont entièrement compatibles avec celles qui utilisent DDEML. Autrement dit, une application qui utilise une liaison DDE basée sur des messages peut établir des conversations et exécuter des transactions avec des applications qui utilisent DDEML. En raison des nombreux avantages du DDEML, les nouvelles applications doivent l’utiliser plutôt que les messages DDE. Pour utiliser les éléments de l’API de DDEML, vous devez inclure le fichier d’en-tête DDEML dans vos fichiers sources, établir une liaison avec la bibliothèque DDEML et vérifier que la bibliothèque de liens dynamiques DDEML se trouve dans le chemin de recherche du système.

Les rubriques suivantes sont présentées dans cette section.

-   [Protocole échange dynamique de données](#dynamic-data-exchange-protocol)
-   [Utilisations de Windows échange dynamique de données](#uses-for-windows-dynamic-data-exchange)
-   [Échange dynamique de données du point de vue de l’utilisateur](#dynamic-data-exchange-from-the-users-point-of-view)
-   [Concepts de échange dynamique de données](#dynamic-data-exchange-concepts)
    -   [Client, serveur et conversation](#client-server-and-conversation)
    -   [Noms d’application, de rubrique et d’élément](#application-topic-and-item-names)
    -   [Rubrique système](#the-system-topic)
    -   [Liaisons de données permanentes](#permanent-data-links)
    -   [Atomes et objets de mémoire partagée](#atoms-and-shared-memory-objects)
-   [Présentation des messages échange dynamique de données](#dynamic-data-exchange-messages-overview)
-   [échange dynamique de données le workflow du message](#dynamic-data-exchange-message-flow)
-   [Fonctions de compression des paramètres](#parameter-packing-functions)
-   [échange dynamique de données et emprunt d’identité](#dynamic-data-exchange-and-impersonation)

## <a name="dynamic-data-exchange-protocol"></a>Protocole échange dynamique de données

Étant donné que Windows dispose d’une architecture basée sur les messages, le passage de messages est la méthode la plus appropriée pour transférer automatiquement les informations entre les applications. Toutefois, les messages contiennent uniquement deux paramètres (*wParam* et *lParam*) pour le passage de données. Par conséquent, ces paramètres doivent faire référence indirectement à d’autres éléments de données lorsque plusieurs mots d’informations transitent entre les applications. Le protocole DDE définit exactement comment les applications doivent utiliser les paramètres *wParam* et *lParam* pour transmettre des éléments de données plus volumineux au moyen d’atomes globaux et de handles de mémoire partagée. Le protocole DDE contient des règles spécifiques pour l’allocation et la suppression des atomes globaux et des objets de mémoire partagée.

Un atome global est une référence à une chaîne de caractères. Dans le protocole DDE, les atomes identifient les applications qui échangent des données, la nature des données échangées et les éléments de données eux-mêmes. Pour plus d’informations sur les atomes, consultez [à propos des atomes](about-atom-tables.md).

## <a name="uses-for-windows-dynamic-data-exchange"></a>Utilisations de Windows échange dynamique de données

DDE est plus approprié pour les échanges de données qui ne nécessitent pas d’intervention de l’utilisateur en cours. En règle générale, une application fournit une méthode permettant à l’utilisateur d’établir le lien entre les applications qui échangent des données. Toutefois, une fois que ce lien est établi, les applications échangent des données sans intervention supplémentaire de l’utilisateur.

DDE peut être utilisé pour implémenter un large éventail de fonctionnalités d’application, par exemple :

-   Liaison à des données en temps réel, telles que la cotation des mises à jour du marché, les instruments scientifiques ou le contrôle de processus.
-   Création de documents composés, tels qu’un document de traitement de texte qui comprend un graphique produit par une application graphique. À l’aide de DDE, le graphique change lorsque les données sources sont modifiées, tandis que le reste du document reste le même.
-   Exécution de requêtes de données entre des applications, par exemple une feuille de calcul interrogeant une base de données pour les comptes en retard.

## <a name="dynamic-data-exchange-from-the-users-point-of-view"></a>Échange dynamique de données du point de vue de l’utilisateur

L’exemple suivant illustre la façon dont deux applications DDE peuvent coopérer, comme le montre le point de vue de l’utilisateur.

Un utilisateur de feuille de calcul souhaite utiliser Microsoft Excel pour suivre le prix d’une action spécifique sur la bourse de New York. L’utilisateur dispose d’une application appelée quote qui, à son tour, a accès aux données du NYSE. La conversation DDE entre Excel et le devis s’effectue comme suit :

-   L’utilisateur lance la conversation en fournissant le nom de l’application (devis) qui fournira les données et la rubrique d’intérêt (NYSE) particulière. La conversation DDE qui en résulte est utilisée pour demander des devis sur des actions spécifiques.
-   Excel diffuse les noms d’application et de rubrique dans toutes les applications DDE en cours d’exécution dans le système. Quote répond, établissant une conversation avec Excel sur la rubrique NYSE.
-   L’utilisateur peut ensuite créer une formule de feuille de calcul dans une cellule qui demande que la feuille de calcul soit automatiquement mise à jour à chaque fois qu’une cotation boursière particulière change. Par exemple, l’utilisateur peut demander une mise à jour automatique chaque fois qu’une modification intervient dans le prix de vente de ZAXX stock en spécifiant la formule Excel suivante : = 'quote' \| 'NYSE' ! ZAXX
-   L’utilisateur peut mettre fin à la mise à jour automatique de la cotation boursière ZAXX à tout moment. Les autres liaisons de données qui ont été établies séparément (par exemple, pour les devis d’autres stocks) resteront actives au cours de la même conversation NYSE.
-   L’utilisateur peut également mettre fin à la conversation entière entre Excel et quote sur la rubrique NYSE, afin qu’aucun lien de données spécifique sur cette rubrique ne puisse être établi sans lancer de nouvelle conversation.

## <a name="dynamic-data-exchange-concepts"></a>Concepts de échange dynamique de données

Les sections suivantes expliquent les concepts et la terminologie importants qui sont essentiels pour comprendre l’échange dynamique de données.

-   [Client, serveur et conversation](#client-server-and-conversation)
-   [Noms d’application, de rubrique et d’élément](#application-topic-and-item-names)
-   [Rubrique système](#the-system-topic)
-   [Liaisons de données permanentes](#permanent-data-links)
-   [Atomes et objets de mémoire partagée](#atoms-and-shared-memory-objects)

### <a name="client-server-and-conversation"></a>Client, serveur et conversation

Deux applications qui participent à DDE sont dites engagées dans une conversation DDE. L’application qui initie la conversation est l’application cliente DDE. l’application qui répond au client est l’application de serveur DDE. Une application peut intervenir dans plusieurs conversations en même temps, en agissant en tant que client dans certains et en tant que serveur dans d’autres.

Une conversation DDE est effectuée entre deux fenêtres, une pour chacune des applications participantes. Une fenêtre peut être la fenêtre principale de l’application. fenêtre associée à un document spécifique, comme dans une application d’interface multidocument (MDI, multiple-document interface); ou une fenêtre masquée (invisible) dont l’objectif est de traiter les messages DDE.

Étant donné qu’une conversation DDE est identifiée par la paire de handles de la Windows engagée dans la conversation, aucune fenêtre ne doit être engagée dans plusieurs conversations avec une autre fenêtre. L’application cliente ou l’application serveur doit fournir une fenêtre différente pour chacune de ses conversations avec un serveur ou une application cliente spécifique.

Une application peut s’assurer qu’une paire de fenêtres client et serveur n’est jamais impliquée dans plusieurs conversations en créant une fenêtre cachée pour chaque conversation. Le seul objectif de cette fenêtre est de traiter les messages DDE.

### <a name="application-topic-and-item-names"></a>Noms d’application, de rubrique et d’élément

Le protocole DDE identifie les unités de données passées entre le client et le serveur avec une hiérarchie à trois niveaux de noms d’application, de rubrique et d’élément.

Chaque conversation DDE est définie de façon unique par le nom et la rubrique de l’application. Au début d’une conversation DDE, le client et le serveur déterminent le nom et la rubrique de l’application. Le nom de l’application est généralement le nom de l’application serveur. Par exemple, lorsqu’Excel agit en tant que serveur dans une conversation, le nom de l’application est Excel.

La rubrique DDE est une classification générale des données dans laquelle plusieurs éléments de données peuvent être « discutés » (échangés) au cours de la conversation. Pour les applications qui opèrent sur des documents basés sur des fichiers, la rubrique est généralement un nom de fichier. Pour les autres applications, la rubrique est un nom propre à l’application.

Étant donné que les handles de fenêtre du client et du serveur identifient ensemble une conversation DDE, le nom et la rubrique de l’application qui définissent une conversation ne peuvent pas être modifiés au cours de la conversation.

Un élément de données DDE est des informations relatives à la rubrique de conversation échangée entre les applications. Les valeurs de l’élément de données peuvent être transmises du serveur au client ou du client au serveur. Les données peuvent être passées avec l’un des formats de presse-papiers standard ou avec un format de presse-papiers inscrit. Un format spécial enregistré nommé Link identifie un élément dans une conversation DDE. Pour plus d’informations sur les formats de presse-papiers, consultez [presse-papiers](clipboard.md).

### <a name="the-system-topic"></a>Rubrique système

Les applications doivent prendre en charge la rubrique système à tout moment. Cette rubrique fournit un contexte pour les informations qui peuvent présenter un intérêt général pour une autre application.

Les valeurs des éléments de données doivent être rendues dans le format de presse-papiers de [**\_ texte CF**](standard-clipboard-formats.md) . Les éléments individuels des valeurs d’éléments d’une rubrique système doivent être délimités par des caractères de tabulation. Le tableau suivant suggère quelques éléments pour la rubrique système.



| Élément          | Description                                                                                                                                                                                                                                                                                             |
|---------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Formats       | Liste de formats de presse-papiers, délimités par des tabulations, que l’application peut restituer. En règle générale, les formats **CF \_** sont répertoriés avec la partie «**CF \_**» des noms supprimés (par exemple, le **\_ texte CF** est répertorié comme «**texte**»).                                                                                        |
| Aide          | Texte qui explique brièvement comment utiliser le serveur DDE.                                                                                                                                                                                                                                                   |
| ReturnMessage | Détails de la prise en charge du message d’accusé de réception [**\_ DDE DDE \_**](wm-dde-ack.md) récemment utilisé. Cet élément est utile lorsque plus de huit bits de données de retour spécifiques à l’application sont nécessaires.                                                                                                                |
| Statut        | Indication de l’état actuel de l’application. Lorsqu’un serveur reçoit un message de [**\_ \_ demande DDE WM**](wm-dde-request.md) pour cet élément de rubrique système, il doit répondre en publiant un message de [**données ( \_ DDE \_ ) WM**](wm-dde-data.md) avec une chaîne contenant soit Busy, soit Ready, le cas échéant. |
| SysItems      | Liste des éléments de rubrique système pris en charge par l’application.                                                                                                                                                                                                                                                    |
| TopicItemList | Semblable à l’élément SysItems, à ceci près que TopicItemList doit être pris en charge pour chaque rubrique autre que la rubrique System. Cela permet de parcourir les éléments pris en charge sous n’importe quelle rubrique. Si les éléments ne peuvent pas être énumérés, cet élément doit contenir uniquement « TopicItemList ».                                  |
| Rubriques        | Liste des rubriques prises en charge par l’application à l’heure actuelle ; Cette liste peut varier d’un moment à l’autres.                                                                                                                                                                                                  |



 

### <a name="permanent-data-links"></a>Liaisons de données permanentes

Une fois qu’une conversation DDE a commencé, le client peut établir une ou plusieurs liaisons de données permanentes avec le serveur. Une liaison de données est un mécanisme de communication par lequel le serveur notifie le client chaque fois que la valeur d’un élément de données spécifié change. La liaison de données est permanente dans le sens où ce processus de notification se poursuit jusqu’à ce que la liaison de données ou la conversation DDE proprement dite soit terminée.

Il existe deux types de liaisons de données DDE permanentes : chaud et chaud. Dans le cas d’une liaison de données à chaud, le serveur informe le client que la valeur de l’élément de données a changé, mais que le serveur n’envoie pas la valeur de données au client tant que le client ne l’a pas demandé. Dans un lien de données réactif, le serveur envoie immédiatement la valeur de données modifiée au client.

Les applications qui prennent en charge les liaisons de données chaudes ou chaudes fournissent généralement une commande **copier** ou **coller le lien** dans le menu **Edition** pour permettre à l’utilisateur d’établir des liens entre les applications.

### <a name="atoms-and-shared-memory-objects"></a>Atomes et objets de mémoire partagée

Certains arguments des messages DDE sont des atomes globaux ou des objets de mémoire partagée. Les applications qui utilisent ces arguments doivent suivre des règles explicites sur le moment où les allouer et les supprimer. Dans tous les cas, l’expéditeur du message doit supprimer tout objet Atom ou mémoire partagée que le destinataire prévu ne recevra pas en raison d’une condition d’erreur, telle que l’échec de la fonction [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea) .

DDE utilise les objets de mémoire partagée pour trois raisons :

-   Pour transporter une valeur d’élément de données à échanger. Il s’agit d’un élément référencé par le paramètre *hdata* dans les messages de données de l' [**échange de \_ \_ données (DDE) WM**](wm-dde-data.md) et de messages d’aide au protocole [**WM \_ DDE \_**](wm-dde-poke.md) .
-   Pour transporter des options dans un message. Il s’agit d’un élément référencé par le paramètre *hOptions* dans un message d' [**\_ \_ avis DDE**](wm-dde-advise.md) .
-   Pour transporter une chaîne d’exécution de commande. Il s’agit d’un élément référencé par le paramètre *hCommands* dans le message d' [**\_ \_ exécution DDE de WM**](wm-dde-execute.md) et son message d' [**\_ \_ accusé**](wm-dde-ack.md) de réception DDE correspondant.

Une application qui reçoit un objet de mémoire partagée DDE doit la considérer comme étant en lecture seule. L’application ne doit pas utiliser l’objet comme zone de lecture-écriture mutuelle pour l’échange de données gratuit.

Comme c’est le cas avec un atome DDE, une application doit libérer un objet mémoire partagé pour gérer efficacement la mémoire. L’application doit également verrouiller et déverrouiller des objets mémoire.

## <a name="dynamic-data-exchange-messages-overview"></a>Présentation des messages échange dynamique de données

Comme DDE est un protocole basé sur les messages, il n’utilise aucune fonction ou bibliothèque. Toutes les transactions DDE sont effectuées en passant certains messages DDE définis entre les fenêtres client et serveur.

Il y a neuf messages DDE ; les constantes symboliques pour ces messages sont définies dans le fichier d’en-tête DDE. Certaines structures pour les différents messages DDE sont également définies dans ce fichier d’en-tête.

Le tableau suivant récapitule les messages DDE.



| Message                                        | Description                                                                                                                                      |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_ACK DDE \_ ACK**](wm-dde-ack.md)             | Accuse réception ou non de réception d’un message.                                                                                               |
| [**\_avis DDE \_ WM**](wm-dde-advise.md)       | Demande à l’application serveur de fournir une mise à jour ou une notification pour un élément de données chaque fois qu’il change. Cela établit une liaison de données permanente. |
| [**\_données DDE \_ WM**](wm-dde-data.md)           | Envoie une valeur d’élément de données à l’application cliente.                                                                                               |
| [**\_exécution DDE de WM \_**](wm-dde-execute.md)     | Envoie une chaîne à l’application serveur, qui est censée traiter la chaîne sous la forme d’une série de commandes.                                       |
| [**\_lancement de DDE de WM \_**](wm-dde-initiate.md)   | Initie une conversation entre les applications client et serveur.                                                                             |
| [**en-dessous du protocole WM \_ DDE \_**](wm-dde-poke.md)           | Envoie une valeur d’élément de données à l’application serveur.                                                                                               |
| [**\_requête DDE \_ WM**](wm-dde-request.md)     | Demande à l’application serveur de fournir la valeur d’un élément de données.                                                                             |
| [**arrêt de l’échange de thread WM \_ \_**](wm-dde-terminate.md) | Met fin à une conversation.                                                                                                                       |
| [**informer de l' \_ échange de \_ notification**](wm-dde-unadvise.md)   | Met fin à un lien de données permanent.                                                                                                                |



 

Une application appelle [**SendMessage**](/windows/desktop/api/winuser/nf-winuser-sendmessage) pour émettre le message de [**\_ \_ lancement DDE**](wm-dde-initiate.md) ou un message d’accusé de réception DDE avec un message d' [**\_ \_ accusé**](wm-dde-ack.md) de réception DDE envoyé en réponse à l' **\_ \_ initialisation** de l’échange de messages WM. Tous les autres messages sont envoyés par [**PostMessage**](/windows/desktop/api/winuser/nf-winuser-postmessagea). Le premier paramètre de ces appels est un handle de la fenêtre de réception ; le deuxième paramètre contient le message à envoyer ; le troisième paramètre identifie la fenêtre émettrice ; et le quatrième paramètre contient les arguments spécifiques au message.

## <a name="dynamic-data-exchange-message-flow"></a>échange dynamique de données le workflow du message

Une conversation DDE classique est constituée des événements suivants :

1.  L’application cliente initie la conversation et l’application serveur répond.
2.  Les applications échangent des données par l’une ou l’ensemble des méthodes suivantes :
    -   -   L’application serveur envoie des données au client à la demande du client.
        -   L’application cliente envoie des données non sollicitées à l’application serveur.
        -   L’application cliente demande à l’application serveur de notifier le client chaque fois qu’un élément de données change (lien de données à chaud).
        -   L’application cliente demande à l’application serveur d’envoyer des données chaque fois que les données sont modifiées (liaison de données à chaud).
        -   L’application serveur exécute une commande à la demande du client.

3.  L’application cliente ou serveur met fin à la conversation.

Une fenêtre d’application qui traite les demandes d’un client ou d’un serveur doit les traiter de manière stricte dans l’ordre dans lequel elles sont reçues.

Un client peut établir des conversations avec plusieurs serveurs ; un serveur peut avoir des conversations avec plusieurs clients. Lors de la gestion des messages à partir de plusieurs sources, un client ou un serveur doit traiter les messages d’une conversation de façon synchrone, mais ils n’ont pas besoin de traiter tous les messages de façon synchrone. En d’autres termes, il peut passer d’une conversation à une autre en fonction des besoins.

Si une application ne parvient pas à traiter une demande entrante parce qu’elle attend une réponse DDE, elle doit empêcher tout interblocage en publiant un message d’accusé de réception [**\_ DDE \_ de WM**](wm-dde-ack.md) avec le membre **fBusy** de la structure [**DDEACK**](/windows/desktop/api/Dde/ns-dde-ddeack) défini sur 1. Une application peut également envoyer un message **d' \_ \_ accusé** de réception DDE actif occupé si, pour une raison quelconque, elle ne peut pas traiter une demande entrante dans un laps de temps raisonnable.

Une application doit être en mesure de gérer l’échec d’un client ou d’un serveur à répondre à un message dans un certain délai. Étant donné que l’intervalle de délai d’attente peut varier en fonction de la nature de l’application et de la configuration du système de l’utilisateur (notamment si elle est connectée à un réseau), l’application doit fournir à l’utilisateur un moyen de spécifier l’intervalle.

## <a name="parameter-packing-functions"></a>Fonctions de compression des paramètres

Le paramètre *lParam* d’un grand nombre de messages DDE contient deux éléments de données. Par exemple, le *lParam* du message [**de \_ \_ données DDE WM**](wm-dde-data.md) contient un descripteur de données et un Atom. Les applications doivent utiliser la fonction [**PackDDElParam**](/windows/desktop/api/Dde/nf-dde-packddelparam) pour empaqueter le handle et Atom dans un paramètre *lParam* , et la fonction [**UnpackDDElParam**](/windows/desktop/api/Dde/nf-dde-unpackddelparam) pour supprimer les valeurs. Les applications DDE doivent utiliser **PackDDElParam** et **UnpackDDElParam** pour tous les messages publiés au cours d’une conversation DDE.

Les applications peuvent également utiliser les fonctions [**ReuseDDElParam**](/windows/desktop/api/Dde/nf-dde-reuseddelparam) et [**FreeDDElParam**](/windows/desktop/api/Dde/nf-dde-freeddelparam) . **ReuseDDElParam** permet à une application DDE de réutiliser un paramètre *lParam* condensé, ce qui contribue à réduire le nombre de réallocations de mémoire que l’application doit effectuer pendant une conversation. Une application peut utiliser **FreeDDElParam** pour libérer la mémoire associée à un handle de données reçu au cours d’une conversation DDE.

## <a name="dynamic-data-exchange-and-impersonation"></a>échange dynamique de données et emprunt d’identité

Pour permettre à un serveur d’emprunter l’identité d’un client, le client appelle la fonction [**DdeSetQualityOfService**](/windows/desktop/api/Dde/nf-dde-ddesetqualityofservice) . La structure de [**\_ \_ niveau d’emprunt d’identité de sécurité**](/windows/win32/api/winnt/ne-winnt-security_impersonation_level) est utilisée pour contrôler le niveau d’emprunt d’identité que le serveur peut effectuer.

Un serveur DDE peut emprunter l’identité d’un client DDE en appelant la fonction [**ImpersonateDdeClientWindow**](/windows/desktop/api/Dde/nf-dde-impersonateddeclientwindow) . Un serveur DDEML doit utiliser la fonction [**DdeImpersonateClient**](/windows/desktop/api/Ddeml/nf-ddeml-ddeimpersonateclient) .

 

 