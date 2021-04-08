---
title: Recherche de systèmes hôtes serveur
description: Recherche de systèmes hôtes de serveur à l’aide de liaisons de chaîne et en interrogeant une base de données de service de noms pour l’emplacement d’un programme serveur.
ms.assetid: 4aadda88-2109-481f-aa4b-b1983d81dec5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2357fcafa35d4f64cfb4f6841c0b56e1e94b7aa
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840182"
---
# <a name="finding-server-host-systems"></a>Recherche de systèmes hôtes serveur

Un système hôte serveur est l’ordinateur qui exécute le programme serveur de l’application distribuée. Il peut y avoir un ou plusieurs systèmes hôtes serveur sur un réseau. La façon dont votre programme client trouve un serveur auquel se connecter dépend des besoins de votre programme.

Il existe deux méthodes pour rechercher des systèmes hôtes serveur :

-   Utilisation des informations stockées dans les chaînes du code source du client, des variables d’environnement ou des fichiers de configuration spécifiques à l’application. Votre application cliente peut utiliser les données de la chaîne pour composer une liaison entre le client et le serveur.
-   Interrogation d’une base de données de service de noms pour l’emplacement d’un programme serveur.

Cette section fournit des informations sur ces deux techniques dans les rubriques suivantes :

-   [Utilisation des liaisons de chaînes](#using-string-bindings)
-   [Importation à partir des bases de données de service de noms](#importing-from-name-service-databases)

## <a name="using-string-bindings"></a>Utilisation des liaisons de chaînes

Les applications peuvent créer des liaisons à partir d’informations stockées dans des chaînes. Votre application cliente compose ces informations sous forme de chaîne, puis appelle la fonction [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) . Le client doit fournir les informations suivantes pour identifier le serveur :

-   Nom de l’interface, identificateur global unique (GUID) de l’objet ou UUID de l’objet. Pour plus d’informations, consultez [génération d’UUID d’interface](generating-interface-uuids.md) et de [chaîne UUID](string-uuid.md).
-   Type de transport sur lequel communiquer, par exemple les canaux nommés ou TCP/IP. Pour plus d’informations, consultez [terminologie de liaison RPC essentielle](essential-rpc-binding-terminology.md) et [sélection d’une séquence de protocole](selecting-a-protocol-sequence.md).
-   Adresse réseau ou nom de l’ordinateur hôte du serveur.
-   Le point de terminaison du programme serveur sur l’ordinateur hôte du serveur. Pour plus d’informations, consultez [recherche de points de terminaison](finding-endpoints.md)et spécification des points de [terminaison](specifying-endpoints.md).

(L’UUID de l’objet et les informations sur le point de terminaison sont facultatifs.)

Dans les exemples suivants, le paramètre *pszNetworkAddress* et d’autres paramètres incluent des barres obliques inverses incorporées. La barre oblique inverse est un caractère d’échappement dans le langage de programmation C. Deux barres obliques inverses sont nécessaires pour représenter chaque caractère barre oblique inverse d’un littéral. La structure de liaison de chaîne doit contenir quatre barres obliques inverses pour représenter les deux barres obliques inverses littérales qui précèdent le nom du serveur.

L’exemple suivant montre que le nom du serveur doit être précédé de huit barres obliques inverses afin que quatre barres obliques inverses littérales apparaissent dans la structure de données de liaison de chaîne après que la fonction **sprintf \_ s** a traité la chaîne.


```C++
/* client application */

char * pszUuid = "6B29FC40-CA47-1067-B31D-00DD010662DA";
char * pszProtocol = "ncacn_np";
char * pszNetworkAddress = "\\\\\\\\servername";
char * pszEndpoint = "\\\\pipe\\\\pipename";
char * pszString;
 
int len = 0;
 
len  = sprintf_s(pszString, strlen(pszUuid), "%s", pszUuid);
len += sprintf_s(pszString + len, strlen(pszProtocolSequence) + 2, "@%s:",
    pszProtocolSequence);
if (pszNetworkAddress != NULL)
    len += sprintf_s(pszString + len, strlen(pszNetworkAddress), "%s",
    pszNetworkAddress);
len += sprintf_s(pszString + len, strlen(pszEndpoint) + 2, "[%s]", pszEndpoint);
```



Dans l’exemple suivant, la liaison de chaîne se présente comme suit :

6B29FC40-CA47-1067-B31D-00DD010662DA@ncacn\_NP : \\ \\ \\ \\ *nom_serveur* \[ \\ \\ canal \\ \\ *pipeName*\]

Le client appelle ensuite [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding) pour obtenir le handle de liaison :


```C++
RPC_BINDING_HANDLE hBinding;
 
status = RpcBindingFromStringBinding(pszString, &hBinding);
//...
```



Une fonction pratique, [**RpcStringBindingCompose**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcstringbindingcompose) assemble l’UUID d’objet, la séquence de protocole, l’adresse réseau et le point de terminaison dans la syntaxe correcte pour l’appel à [**RpcBindingFromStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingfromstringbinding). Vous n’avez pas à vous soucier de l’insertion de l’esperluette, du signe deux-points et des différents composants de chaque séquence de protocole au bon endroit. il vous suffit de fournir les chaînes en tant que paramètres à la fonction. La bibliothèque Runtime alloue même la mémoire nécessaire pour la liaison de chaîne.


```C++
char * pszNetworkAddress = "\\\\server";
char * pszEndpoint = "\\pipe\\pipename";
status = RpcStringBindingCompose(
            pszUuid,
            pszProtocolSequence,
            pszNetworkAddress,
            pszEndpoint,
            pszOptions,
            &pszString);
//...
status = RpcBindingFromStringBinding(
            pszString,
            &hBinding);
//...
```



Une autre fonction pratique, [**RpcBindingToStringBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingtostringbinding), prend un handle de liaison comme entrée et génère la liaison de chaîne correspondante.

## <a name="importing-from-name-service-databases"></a>Importation à partir des bases de données de service de noms

Les bases de données de service de noms stockent, entre autres choses, des handles de liaison et des UUID. Votre application cliente peut Rechercher l’un ou l’autre ou les deux lorsqu’il doit effectuer une liaison avec le serveur. Pour en savoir plus sur les informations stockées par un service de noms et le format de stockage, consultez [la base de données du service de noms RPC](the-rpc-name-service-database.md).

La bibliothèque RPC fournit deux ensembles de fonctions que votre programme client peut utiliser pour rechercher la base de données de service de noms. Les noms d’un jeu commencent par RpcNsBindingImport. Les noms de l’autre jeu commencent par RpcNsBindingLookup. La différence entre les deux groupes de fonctions est que les fonctions RpcNsBindingImport retournent un seul handle de liaison par appel et que les fonctions RpcNsBindingLookup retournent des groupes de handles par appel.

Pour commencer une recherche avec les fonctions RpcNsBindingImport, appelez d’abord [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina), comme indiqué dans le fragment de code suivant.


```C++
RPC_STATUS status;
RPC_NS_HANDLE hNameServiceHandle;
 
status = RpcNsBindingImportBegin(
    RPC_C_NS_SYNTAX_DEFAULT,
    NULL,
    MyInterface_v1_0_c_ifspec,
    NULL,
    &hNameServiceHandle);
```



Lorsque les fonctions RPC recherchent la base de données de service de noms, elles ont besoin d’un emplacement pour commencer la recherche. Dans la terminologie RPC, il s’agit du nom de l’entrée. Votre programme client transmet le nom de l’entrée en tant que deuxième paramètre à [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina). Ce paramètre peut avoir la **valeur null** si vous souhaitez effectuer une recherche dans l’intégralité de la base de données du service de noms. Vous pouvez également effectuer une recherche sur l’entrée de serveur en passant un nom d’entrée de serveur ou effectuer une recherche dans l’entrée de groupe en passant un nom d’entrée de groupe. Le passage d’un nom d’entrée restreint la recherche au contenu de cette entrée.

Dans l’exemple précédent, la valeur \_ par défaut de la syntaxe RPC C \_ NS \_ \_ est passée comme premier paramètre à [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina). Cela sélectionne la syntaxe du nom d’entrée par défaut. Actuellement, il s’agit de la seule syntaxe de nom d’entrée prise en charge.

Votre application cliente peut rechercher un nom d’interface, un UUID ou les deux dans la base de données de service de noms. Si vous souhaitez qu’il recherche une interface par nom, transmettez la variable d’interface globale que le compilateur MIDL génère à partir de votre fichier IDL en tant que troisième paramètre de [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina). Vous trouverez sa déclaration dans le fichier d’en-tête généré par le compilateur MIDL lorsqu’il a généré le stub client. Si vous souhaitez que votre programme client recherche par UUID uniquement, définissez le troisième paramètre sur la **valeur null**.

Lors de la recherche d’un UUID dans la base de données de service de noms, définissez le quatrième paramètre de [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) sur l’UUID que vous souhaitez rechercher. Si vous ne recherchez pas d’UUID, affectez la valeur **null** à ce paramètre.

La fonction [**RpcNsBindingImportBegin**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina) transmet l’adresse d’un handle de contexte de recherche de service de nom via son cinquième paramètre. Vous transmettez ce paramètre à d’autres fonctions RpcNsBindingImport.

En particulier, la fonction suivante que votre application cliente appelle est [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext). Les programmes clients utilisent cette fonction pour récupérer les descripteurs de liaison compatibles de la base de données du service de noms. Le fragment de code suivant montre comment cette fonction peut être appelée :


```C++
RPC_STATUS status;
RPC_BINDING_HANDLE hBindingHandle;
// The variable hNameServiceHandle is a valid name service search 
// context handle obtained from the RpcNsBindingBegin function.
 
status = RpcNsBindingImportNext(hNameServiceHandle, &hBindingHandle);
```



Une fois que la fonction [**RpcNsBindingImportNext**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportnext) a été appelée pour obtenir un handle de liaison, votre application cliente peut déterminer si le handle qu’elle a reçu est acceptable. Si ce n’est pas le cas, votre programme client peut exécuter une boucle et appeler à nouveau **RpcNsBindingImportNext** pour voir si le service de noms contient un handle plus approprié. Pour chaque appel à **RpcNsBindingImportNext**, il doit y avoir un appel correspondant à RpcNsBindingFree. Lorsque votre recherche est terminée, appelez la fonction [**RpcNsBindingImportDone**](/windows/desktop/api/Rpcnsi/nf-rpcnsi-rpcnsbindingimportdone) pour libérer le contexte de recherche.

Une fois que votre application cliente a un handle de liaison acceptable, elle doit vérifier que l’application serveur est en cours d’exécution. Votre client peut utiliser deux méthodes pour effectuer cette vérification. La première consiste à appeler une fonction dans l’interface du client. Si le programme serveur est en cours d’exécution, l’appel se termine. Si ce n’est pas le cas, l’appel échoue. Une meilleure façon de vérifier que le serveur est en cours d’exécution consiste à appeler [**RpcEpResolveBinding**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcepresolvebinding), suivi d’un appel à [**RpcMgmtIsServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtisserverlistening). Pour plus d’informations sur la base de données du service de noms, consultez [la base de données du service de noms RPC](the-rpc-name-service-database.md).

 

 




