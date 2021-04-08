---
title: Concepts de base
description: Cette rubrique décrit les concepts clés relatifs à l’échange dynamique de données.
ms.assetid: 37826d83-4dcd-484f-b1aa-87bf309c5c09
keywords:
- Interface utilisateur Windows, échange dynamique de données (DDE)
- Interface utilisateur Windows, bibliothèque de gestion des échange dynamique de données (DDEML)
- Échange dynamique de données (DDE), interaction du serveur client
- DDE (échange dynamique de données), interaction du serveur client
- échange de données, échange dynamique de données (DDE)
- échange de données, bibliothèque de gestion des échange dynamique de données (DDEML)
- Échange dynamique de données (DDE), applications clientes
- DDE (échange dynamique de données), applications clientes
- Échange dynamique de données (DDE), applications serveur
- DDE (échange dynamique de données), applications serveur
- Échange dynamique de données (DDE), fonctions de rappel
- DDE (échange dynamique de données), fonctions de rappel
- Échange dynamique de données (DDE), transactions
- DDE (échange dynamique de données), transactions
- Échange dynamique de données (DDE), noms de service
- DDE (échange dynamique de données), noms de service
- Échange dynamique de données (DDE), noms d’éléments
- DDE (échange dynamique de données), noms d’éléments
- Échange dynamique de données (DDE), noms de rubriques
- DDE (échange dynamique de données), noms de rubriques
- Échange dynamique de données (DDE), rubrique système
- DDE (échange dynamique de données), rubrique système
- Bibliothèque de gestion des échange dynamique de données (DDEML), initialisation
- DDEML (bibliothèque de gestion échange dynamique de données), initialisation
- Bibliothèque de gestion des échange dynamique de données (DDEML), fonctions de rappel
- DDEML (bibliothèque de gestion échange dynamique de données), fonctions de rappel
- Bibliothèque de gestion des échange dynamique de données (DDEML), gestion des chaînes
- DDEML (bibliothèque de gestion échange dynamique de données), gestion des chaînes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c564bffbcbb06ddc3a0e0fa4e0a9ed398d3ca55
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103727917"
---
# <a name="basic-concepts-dde"></a>Concepts de base (DDE)

Ces concepts sont essentiels pour comprendre échange dynamique de données (DDE) et la bibliothèque de gestion des échange dynamique de données (DDEML).

-   [Interaction entre le client et le serveur](#client-and-server-interaction)
-   [Transactions et fonction de rappel DDE](#transactions-and-the-dde-callback-function)
-   [Noms de service, noms de rubriques et noms d’éléments](#service-names-topic-names-and-item-names)
-   [Rubrique système](#system-topic)
-   [D’initialisation](#initialization)
-   [Fonction de rappel](#callback-function)
-   [Gestion des chaînes](#string-management)
-   [DDEML et threads](#ddeml-and-threads)

## <a name="client-and-server-interaction"></a>Interaction entre le client et le serveur

DDE se produit toujours entre une application cliente et une application serveur. L' *application cliente DDE* initie l’échange en établissant une conversation avec le serveur pour envoyer des transactions au serveur. Une transaction est une demande de données ou de services. L' *application de serveur DDE* répond aux transactions en fournissant des données ou des services au client. Par exemple, une application graphique peut contenir un graphique à barres représentant les bénéfices trimestriels d’une entreprise, mais les données du graphique à barres peuvent être contenues dans une application de feuille de calcul. Pour obtenir les derniers résultats, l’application Graphics (le client) peut établir une conversation avec l’application Spreadsheet (le serveur). L’application Graphics peut ensuite envoyer une transaction à l’application de feuille de calcul, en demandant les derniers résultats.

Un serveur peut avoir plusieurs clients en même temps et un client peut demander des données à partir de plusieurs serveurs. Une application peut également être à la fois un client et un serveur. Le client ou le serveur peut mettre fin à la conversation à tout moment.

## <a name="transactions-and-the-dde-callback-function"></a>Transactions et fonction de rappel DDE

Le DDEML informe une application de l’activité DDE qui affecte l’application en envoyant des transactions à la fonction de rappel DDE de l’application. Une *transaction DDE* est semblable à un message. il s’agit d’une constante nommée accompagnée d’autres paramètres qui contiennent des informations supplémentaires sur la transaction.

Le DDEML transmet une transaction à une fonction de rappel DDE définie par l’application qui exécute une action appropriée pour le type de transaction. Par exemple, lorsqu’une application cliente tente d’établir une conversation avec une application serveur, le client appelle la fonction [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) . Cette fonction force DDEML à envoyer une transaction [**XTYP \_ Connect**](xtyp-connect.md) à la fonction de rappel DDE du serveur. La fonction de rappel peut autoriser la conversation en retournant la **valeur true** à Ddeml, ou elle peut refuser la conversation en retournant **false**. Pour une présentation détaillée des transactions, consultez [gestion des transactions](transaction-management.md).

## <a name="service-names-topic-names-and-item-names"></a>Noms de service, noms de rubriques et noms d’éléments

Un serveur DDE utilise un nom de service de hiérarchie à trois niveaux (appelé « nom de l’application » dans la documentation DDE précédente), un nom de rubrique et un nom d’élément pour identifier de manière unique une unité de données que le serveur peut échanger au cours d’une conversation.

Un *nom de service* est une chaîne à laquelle une application serveur répond lorsqu’un client tente d’établir une conversation avec le serveur. Un client doit spécifier ce nom de service pour établir une conversation avec le serveur. Bien qu’un serveur puisse répondre à de nombreux noms de service, la plupart des serveurs répondent à un seul nom.

Un *nom de rubrique* est une chaîne qui identifie un contexte de données logique. Pour les serveurs qui opèrent sur des documents basés sur des fichiers, les noms de rubriques sont généralement des noms de fichiers ; pour les autres serveurs, il s’agit d’autres chaînes propres à l’application. Un client doit spécifier un nom de rubrique avec le nom de service d’un serveur lorsqu’il tente d’établir une conversation avec un serveur.

Un *nom d’élément* est une chaîne qui identifie une unité de données qu’un serveur peut passer à un client au cours d’une transaction. Par exemple, un nom d’élément peut identifier un entier, une chaîne, plusieurs paragraphes de texte ou une image bitmap.

Les noms de service, de rubrique et d’élément permettent au client d’établir une conversation avec un serveur et de recevoir des données du serveur.

## <a name="system-topic"></a>Rubrique système

La rubrique système fournit un contexte pour les informations d’intérêt général pour un client DDE. Il est recommandé que les applications serveur prennent en charge la rubrique système à tout moment. La rubrique système est définie dans DDEML. Fichier d’en-tête H comme \_ rubrique SZDDESYS.

Pour déterminer les serveurs présents et les types d’informations qu’ils peuvent fournir, une application cliente peut demander une conversation sur la rubrique du système au démarrage, en affectant la **valeur null** au nom de l’appareil. Ces conversations par caractères génériques sont coûteuses en termes de performances du système. elles doivent donc être limitées au minimum. Pour plus d’informations sur l’initiation des conversations DDE, consultez [gestion](conversation-management.md)des conversations.

Un serveur doit prendre en charge les noms d’éléments suivants dans la rubrique système et tout autre nom d’élément utile pour un client.



| Élément                     | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_élément SZDDE \_ ITEMLIST    | Liste des éléments pris en charge dans une rubrique non-système. (Cette liste peut varier d’un moment à l’autres et d’un sujet à un sujet.)                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| \_formats d’élément SZDDESYS \_  | Liste de chaînes délimitées par des tabulations représentant tous les formats de presse-papiers potentiellement pris en charge par l’application de service. Les chaînes qui représentent des formats de presse-papiers prédéfinis sont équivalentes aux \_ valeurs CF avec le \_ préfixe « CF » supprimé. Par exemple, le \_ format de texte CF est représenté par la chaîne « Text ». Ces chaînes doivent être en majuscules pour les identifier plus en tant que formats prédéfinis. La liste des formats doit apparaître dans l’ordre de contenu le plus riche pour le contenu le moins riche. Pour plus d’informations sur les formats de presse-papiers et les données de rendu, consultez [presse-papiers](clipboard.md).<br/> |
| \_ \_ aide sur l’élément SZDDESYS     | Informations explicites d’intérêt général. Cet élément doit contenir au minimum des informations sur l’utilisation des fonctionnalités DDE de l’application serveur. Ces informations peuvent inclure, sans s’y limiter, comment spécifier des éléments dans les rubriques, les chaînes d’exécution que le serveur peut exécuter, les transactions d’enchaînement autorisées et comment rechercher de l’aide sur d’autres éléments de rubrique système.                                                                                                                                                                                                                           |
| \_élément SZDDESYS \_ RTNMSG   | Détails de la prise en charge du message d’accusé de réception [**\_ DDE DDE \_**](wm-dde-ack.md) récemment utilisé. Cet élément est utile lorsque plus de 8 bits de données de retour spécifiques à l’application sont nécessaires.                                                                                                                                                                                                                                                                                                                                                                                                                        |
| État de l' \_ élément SZDDESYS \_   | Indication de l’état actuel du serveur. En règle générale, cet élément prend en charge uniquement le \_ format de texte CF et contient la chaîne prête ou occupée.                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| \_élément SZDDESYS \_ SYSITEMS | Liste des éléments pris en charge dans la rubrique système par ce serveur.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| \_rubriques relatives aux éléments SZDDESYS \_   | Liste des rubriques prises en charge par le serveur à l’heure actuelle. (Cette liste peut varier d’un moment à l’autres).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



 

Ces noms d’élément sont des valeurs définies dans DDEML. Fichier d’en-tête H. Pour obtenir des handles de chaîne pour ces chaînes, une application doit utiliser les fonctions de gestion de chaînes DDEML, tout comme pour toute autre chaîne dans une application DDEML. Pour plus d’informations sur la gestion des chaînes, consultez [gestion](#string-management)des chaînes.

## <a name="initialization"></a>Initialisation

Avant d’appeler toute autre fonction DDEML, une application doit appeler la fonction [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) . **DdeInitialize** obtient un identificateur d’instance pour l’application, inscrit la fonction de rappel DDE de l’application auprès du DDE et spécifie les indicateurs de filtre de transaction pour la fonction de rappel.

Chaque instance d’une application ou d’une DLL doit passer son identificateur d’instance en tant que paramètre *idInst* à toute autre fonction Ddeml qui l’exige. L’objectif de plusieurs instances DDEML consiste à prendre en charge les dll qui doivent utiliser le DDEML en même temps qu’une application l’utilise. Une application ne doit pas utiliser plus d’une instance de DDEML.

Les *filtres de transaction* optimisent les performances du système en empêchant le Ddeml de transmettre des transactions indésirables à la fonction de rappel DDE de l’application. Une application définit les filtres de transaction dans le paramètre [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) *ufCmd* . Une application doit spécifier un indicateur de filtre de transaction pour chaque type de transaction qu’elle ne traite pas dans sa fonction de rappel. Une application peut modifier ses filtres de transactions avec un appel ultérieur à **DdeInitialize**. Pour plus d’informations sur les transactions, consultez [gestion des transactions](transaction-management.md).

L’exemple suivant montre comment initialiser une application pour utiliser le DDEML.


```
DWORD idInst = 0; 
HINSTANCE hinst; 
 
DdeInitialize(&idInst,         // receives instance identifier 
    (PFNCALLBACK) DdeCallback, // pointer to callback function 
    CBF_FAIL_EXECUTES |        // filter XTYPE_EXECUTE 
    CBF_SKIP_ALLNOTIFICATIONS, // filter notifications 
    0); 
```



Une application doit appeler la fonction [**DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) lorsqu’elle n’utilise plus le Ddeml. Cette fonction met fin à toutes les conversations actuellement ouvertes pour l’application et libère les ressources DDEML allouées par le système pour l’application.

## <a name="callback-function"></a>Fonction de rappel

Une application qui utilise DDEML doit fournir une fonction de rappel qui traite les événements DDE affectant l’application. Le DDEML notifie une application de tels événements en envoyant des transactions à la fonction de rappel DDE de l’application. Les transactions qu’une fonction de rappel reçoit dépendent du filtre de rappel qui signale l’application spécifiée dans [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) et si l’application est un client, un serveur ou les deux. Pour plus d’informations, consultez [**DdeCallback**](/windows/win32/api/ddeml/nc-ddeml-pfncallback).

L’exemple suivant illustre la structure générale d’une fonction de rappel pour une application cliente classique.


```
HDDEDATA CALLBACK DdeCallback(uType, uFmt, hconv, hsz1, 
    hsz2, hdata, dwData1, dwData2) 
UINT uType;       // transaction type 
UINT uFmt;        // clipboard data format 
HCONV hconv;      // handle to conversation 
HSZ hsz1;         // handle to string 
HSZ hsz2;         // handle to string 
HDDEDATA hdata;   // handle to global memory object 
DWORD dwData1;    // transaction-specific data 
DWORD dwData2;    // transaction-specific data 
{ 
    switch (uType) 
    { 
        case XTYP_REGISTER: 
        case XTYP_UNREGISTER: 
            . 
            . 
            . 
            return (HDDEDATA) NULL; 
 
        case XTYP_ADVDATA: 
            . 
            . 
            . 
            return (HDDEDATA) DDE_FACK; 
 
        case XTYP_XACT_COMPLETE: 
            
            // 
            
            return (HDDEDATA) NULL; 
 
        case XTYP_DISCONNECT: 
            
            // 
            
            return (HDDEDATA) NULL; 
 
        default: 
            return (HDDEDATA) NULL; 
    } 
} 
```



Le paramètre *uType* spécifie le type de transaction envoyé à la fonction de rappel par le Ddeml. Les valeurs des autres paramètres dépendent du type de transaction. Les types de transactions et les événements qui les génèrent sont décrits dans les rubriques suivantes. Pour plus d’informations sur chaque type de transaction, consultez [gestion des transactions](transaction-management.md).

## <a name="string-management"></a>Gestion des chaînes

Pour effectuer une tâche DDE, de nombreuses fonctions DDEML requièrent l’accès aux chaînes. Par exemple, un client doit spécifier un nom de service et un nom de rubrique lorsqu’il appelle la fonction [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) pour demander une conversation avec un serveur. Une application spécifie une chaîne en passant un handle de chaîne (HSZ) au lieu d’un pointeur dans une fonction DDEML. Un *descripteur de chaîne* est une valeur **DWORD** , assignée par le système, qui identifie une chaîne.

Une application peut obtenir un descripteur de chaîne d’une chaîne particulière en appelant la fonction [**DdeCreateStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea) . Cette fonction inscrit la chaîne auprès du système et retourne un handle de chaîne à l’application. L’application peut passer le descripteur aux fonctions DDEML qui doivent accéder à la chaîne. L’exemple suivant obtient des handles de chaîne à la chaîne de rubrique système et à la chaîne de nom de service.


```
HSZ hszServName; 
HSZ hszSysTopic; 
hszServName = DdeCreateStringHandle( 
    idInst,         // instance identifier 
    "MyServer",     // string to register 
    CP_WINANSI);    // Windows ANSI code page 
 
hszSysTopic = DdeCreateStringHandle( 
    idInst,         // instance identifier 
    SZDDESYS_TOPIC, // System topic 
    CP_WINANSI);    // Windows ANSI code page 
    
```



Le paramètre *idInst* dans l’exemple précédent spécifie l’identificateur d’instance obtenu par la fonction [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .

La fonction de rappel DDE d’une application reçoit un ou plusieurs descripteurs de chaîne au cours de la plupart des transactions DDE. Par exemple, un serveur reçoit deux descripteurs de chaîne lors de la transaction de [**\_ demande XTYP**](xtyp-request.md) : l’un identifie une chaîne spécifiant un nom de rubrique et l’autre identifie une chaîne spécifiant un nom d’élément. Une application peut obtenir la longueur de la chaîne qui correspond à un handle de chaîne et copier la chaîne dans une mémoire tampon définie par l’application en appelant la fonction [**DdeQueryString**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerystringa) , comme illustré dans l’exemple suivant.


```
DWORD idInst; 
DWORD cb; 
HSZ hszServ; 
PSTR pszServName; 
cb = DdeQueryString(idInst, hszServ, (LPSTR) NULL, 0, 
    CP_WINANSI) + 1; 
pszServName = (PSTR) LocalAlloc(LPTR, (UINT) cb); 
DdeQueryString(idInst, hszServ, pszServName, cb, CP_WINANSI); 
```



Un handle de chaîne spécifique à l’instance ne peut pas être mappé du descripteur de chaîne à la chaîne et revenir au handle de chaîne. Par exemple, bien que [**DdeQueryString**](/windows/desktop/api/Ddeml/nf-ddeml-ddequerystringa) crée une chaîne à partir d’un handle de chaîne, puis [**DdeCreateStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea) crée un handle de chaîne à partir de cette chaîne, les deux Handles ne sont pas les mêmes, comme illustré dans l’exemple suivant.


```
DWORD idInst; 
DWORD cb; 
HSZ hszInst, hszNew; 
PSZ pszInst; 
DdeQueryString(idInst, hszInst, pszInst, cb, CP_WINANSI); 
hszNew = DdeCreateStringHandle(idInst, pszInst, CP_WINANSI); 
// hszNew != hszInst ! 
```



Pour comparer les valeurs de deux descripteurs de chaîne, utilisez la fonction [**DdeCmpStringHandles**](/windows/desktop/api/Ddeml/nf-ddeml-ddecmpstringhandles) .

Un descripteur de chaîne passé à la fonction de rappel DDE d’une application devient non valide lorsque la fonction de rappel retourne. Une application peut enregistrer un handle de chaîne pour une utilisation après le retour de la fonction de rappel à l’aide de la fonction [**DdeKeepStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddekeepstringhandle) .

Quand une application appelle [**DdeCreateStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea), le système entre la chaîne spécifiée dans une table de chaînes et génère un handle qu’elle utilise pour accéder à la chaîne. Le système gère également un nombre d’utilisations pour chaque chaîne dans la table de chaînes.

Quand une application appelle [**DdeCreateStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatestringhandlea) et spécifie une chaîne qui existe déjà dans la table, le système incrémente le nombre d’utilisations plutôt que d’ajouter une autre occurrence de la chaîne. (Une application peut également incrémenter le nombre d’utilisations à l’aide de [**DdeKeepStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddekeepstringhandle).) Quand une application appelle la fonction [**DdeFreeStringHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddefreestringhandle) , le système décrémente le nombre d’utilisations.

Une chaîne est supprimée de la table lorsque son nombre d’utilisations est égal à zéro. Étant donné que plusieurs applications peuvent obtenir le descripteur d’une chaîne particulière, une application ne doit pas libérer un handle de chaîne plus de fois qu’il n’a créé ou conservé le descripteur. Dans le cas contraire, l’application peut provoquer la suppression de la chaîne de la table, ce qui a pour effet de refuser à d’autres applications l’accès à la chaîne.

Les fonctions de gestion de chaînes DDEML sont basées sur le gestionnaire Atom et sont soumises aux mêmes restrictions de taille que les atomes.

## <a name="ddeml-and-threads"></a>DDEML et threads

La fonction [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) inscrit une application avec Ddeml, créant une instance Ddeml. Une instance DDEML est basée sur un thread, associée au thread qui a appelé **DdeInitialize**.

Tous les appels de fonction DDEML pour les objets appartenant à une instance DDEML doivent être effectués à partir du même thread que celui qui a appelé [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) pour créer l’instance. Si vous appelez une fonction DDEML à partir d’un autre thread, la fonction échoue. Vous ne pouvez pas accéder à une conversation DDEML à partir d’un thread autre que celui qui a alloué la conversation.

 

