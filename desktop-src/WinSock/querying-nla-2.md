---
description: Pour obtenir la notification des réseaux logiques invalidés, utilisez la fonction WSANSPIoctl pour vous inscrire aux événements de changement d’emplacement réseau.
ms.assetid: 531b6269-5f35-44c1-ad0f-c5f103029893
title: Interrogation de NLA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ac7a4f57e14bb967b04d3a9fd6fe66717da3878
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106518186"
---
# <a name="querying-nla"></a>Interrogation de NLA

Pour obtenir la notification des réseaux logiques invalidés, utilisez la fonction [**WSANSPIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl) pour vous inscrire aux événements de changement d’emplacement réseau. Deux méthodes peuvent être utilisées pour déterminer si un emplacement réseau précédemment valide est devenu non valide : des méthodes d’interrogation ou une notification utilisant des e/s avec chevauchement ou une messagerie Windows.

Les requêtes sont formées à l’aide des fonctions [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina), [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) et [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) pour énumérer tous les réseaux logiques disponibles. L’utilisation de chacune de ces fonctions est expliquée individuellement dans le reste de cette section, en commençant par la fonction **WSALookupServiceBegin** .

> [!Note]  
> NLA requiert le fichier d’en-tête mswsock. h, qui, par défaut, n’est pas inclus dans le fichier Winsock2. h.

 

## <a name="step-1-initiate-the-query"></a>Étape 1 : lancer la requête

Pour référence rapide, la fonction [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) a la syntaxe suivante :

``` syntax
INT WSALookupServiceBegin(
  LPWSAQUERYSET lpqsRestrictions,
  DWORD dwControlFlags,
  LPHANDLE lphLookup
);
```

NLA prend en charge les indicateurs de recherche *dwControlFlags* suivants :

<dl> LUP \_ nom de retour \_  
LUP \_ retourner le \_ Commentaire  
LUP \_ retourne un \_ objet BLOB  
LUP \_ renvoyer \_ tout  
LUP \_ profonde  
</dl>

Ces indicateurs limitent les jeux de résultats retournés dans les appels suivants à la fonction [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta), aux réseaux qui contiennent des champs du type spécifié. Par exemple, si vous spécifiez LUP, \_ \_ l’objet blob de retour dans le paramètre *dwControlFlags* de l’appel de fonction [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) restreint les jeux de résultats des appels suivants à **WSALookupServiceNext**, aux réseaux qui contiennent des informations d’objet BLOB. L’utilisation de l' \_ indicateur lup Return \_ All est équivalente à la spécification du \_ nom de retour lup, du commentaire de \_ \_ retour lup et lup à l' \_ \_ \_ objet BLOB Return, mais pas à la \_ profondeur lup.

Pour obtenir une explication de ces indicateurs de recherche, consultez la page de référence sur les fonctions [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) .

Le handle de recherche retourné par NLA dans le paramètre *lphLookup* est privé pour NLA et ne doit pas être modifié. Étant donné que le handle retourné est privé pour NLA, les fonctions telles que [**WSAGetOverlappedResult**](/windows/desktop/api/Winsock2/nf-winsock2-wsagetoverlappedresult) ne sont pas disponibles.

NLA retourne la valeur zéro en cas de réussite, comme défini dans la page de référence de la fonction [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) . Dans le cas contraire, NLA prend en charge les codes d’erreur suivants.

| Error                    | Signification                                                                                                                                                     |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WSANOTINITIALISED        | Un appel réussi à la fonction [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) pour initialiser NLA n’a pas été effectué.                                                   |
| WSAEINVAL                | Un ou plusieurs paramètres ne sont pas valides, ou les paramètres spécifiés dans l’appel de fonction s’appliquent à des protocoles autres que l’adresse IP.                                         |
| WSASERVICE \_ \_ introuvable   | Le paramètre *lpServiceClassId* de la structure [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) passée dans le paramètre *lpqsRestrictions* contient un GUID non valide. |
| \_données WSANO              | L' \_ indicateur lup Containers a été spécifié dans le paramètre *dwControlFlags* .                                                                                       |
| WSAEFAULT                | Une violation d’accès s’est produite lors de la tentative d’accès aux paramètres fournis par l’utilisateur.                                                                            |
| WSASYSNOTREADY           | Le service NLA n’est pas disponible pour traiter la demande.                                                                                                      |
| \_mémoire WSA \_ insuffisante \_ | NLA ou le service NLA n’a pas pu allouer suffisamment de mémoire pour traiter cette demande.                                                                        |



 

## <a name="step-2-perform-the-query"></a>Étape 2 : exécuter la requête

L’étape suivante de l’interrogation de NLA requiert l’utilisation de la fonction [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) . Pour référence rapide, la fonction **WSALookupServiceNext** a la syntaxe suivante :

``` syntax
INT WSALookupServiceNext(
  HANDLE hLookup,
  DWORD dwControlFlags,
  LPDWORD lpdwBufferLength,
  LPWSAQUERYSET lpqsResults
);
```

Le paramètre *lLookup* est le handle de recherche retourné par l’appel précédent à la fonction [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) .

Le paramètre *dwControlFlags* prend en charge les indicateurs suivants :

<dl> LUP \_ nom de retour \_  
LUP \_ retourner le \_ Commentaire  
LUP \_ retourne un \_ objet BLOB  
LUP \_ renvoyer \_ tout  
LUP \_ FLUSHPREVIOUS  
</dl>

Ces indicateurs sont indépendants des indicateurs pris en charge dans l’appel de la fonction [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) . Notez que toutes les contraintes spécifiées dans l’appel précédent à la fonction **WSALookupServiceBegin** contraignent la recherche ; l’ajout d’indicateurs avec la fonction [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) dans une tentative d’élargissement de la requête au-delà des contraintes spécifiées dans l’appel **WSALookupServiceBegin** est ignoré en mode silencieux. Toutefois, la spécification d’un jeu d’indicateurs plus restrictif que celui spécifié dans l’appel **WSALookupServiceBegin** est autorisée.

Si le réseau détaillé dans *lpqsResults* est un réseau actif, une série de **structures \_ BLOB NLA** est ajoutée comme spécifié dans le membre **lpBlob** de la structure [**WSAQUERYSET**](/windows/desktop/api/Winsock2/ns-winsock2-wsaquerysetw) retournée dans *lpqsResults*. Ces **structures \_ BLOB NLA** peuvent être chaînées et peuvent être énumérées en parcourant la liste pendant que l' \_ objet BLOB NLA. Header. nextOffset est différent de zéro. Pour obtenir les résultats de toutes les informations relatives à l’emplacement du réseau, continuez à appeler la fonction [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)jusqu’à ce que le WSA \_ E \_ n' \_ ait plus d’erreur est renvoyée, comme expliqué dans la page de référence **WSALookupServiceNext**.

La fonction [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) est également utilisée conjointement avec la fonction [**WSANSPIoctl**](/windows/desktop/api/Winsock2/nf-winsock2-wsanspioctl) pour recevoir la notification des modifications du réseau. Pour plus d’informations, consultez [notification d’NLA](notification-from-nla-2.md) .

NLA retourne la valeur zéro en cas de réussite. Les clients d’NLA doivent continuer à appeler la fonction [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)jusqu’à ce que le WSA \_ E \_ ne \_ soit pas retourné, ce qui indique que toutes les informations sur les réseaux disponibles ont été retournées.

Sinon, l’appel de la fonction [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta)pour NLA prend en charge les codes d’erreur suivants.

| Error                    | Signification                                                                                                                                                                                                                                                                                                                                                                                                     |
|--------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WSANOTINITIALISED        | Un appel réussi à la fonction [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) qui a initialisé NLA n’a pas été effectué.                                                                                                                                                                                                                                                                                                |
| \_descripteur WSA non valide \_     | Le descripteur de recherche fourni dans le paramètre *RECHERCHEH* n’était pas un handle NLA valide. Les clients doivent d’abord appeler la fonction [**WSALookupServiceBegin**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicebegina) et recevoir un handle NLA valide pour obtenir les résultats de la requête.                                                                                                                                                               |
| WSAESYSNOTREADY          | Le service NLA n’est pas disponible pour traiter cette demande.                                                                                                                                                                                                                                                                                                                                                     |
| WSAEFAULT                | La taille de la mémoire tampon spécifiée dans le paramètre *lpdwBufferLength* est insuffisante pour contenir les résultats pointés par *lpqsResults*. La mémoire tampon requise est spécifiée dans *lpdwBufferLength*; Si le client ne peut pas fournir une mémoire tampon suffisamment grande, le client peut appeler la fonction [**WSALookupServiceNext**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupservicenexta) avec *DWCONTROLFLAGS* défini sur lup \_ FLUSHPREVIOUS pour ignorer l’entrée. |
| \_mémoire WSA \_ insuffisante \_ | NLA ne parvient pas à obtenir les informations réseau à partir du service système NLA en raison d’une insuffisance de mémoire dans le processus appelant.                                                                                                                                                                                                                                                                                  |
| WSA \_ E \_ plus \_         | Il n’existe aucun réseau supplémentaire à énumérer pour la requête.                                                                                                                                                                                                                                                                                                                                                |



 

## <a name="step-3-terminate-the-query"></a>Étape 3 : terminer la requête

Lorsque toutes les requêtes à NLA sont terminées et qu’une application n’exige plus l’utilisation de NLA, un appel à la fonction [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) doit être effectué. N’appelez pas **WSALookupServiceEnd** si l’application reçoit une notification de modification en fonction de la requête envoyée. Pour plus d’informations sur la réception de notifications, consultez [notification d’NLA](notification-from-nla-2.md) . Comme la plupart des fournisseurs de services Windows Sockets, NLA conserve un décompte de références pour ses clients. L’appel de la fonction **WSALookupServiceEnd** lorsque les requêtes à NLA sont effectuées permet de libérer les ressources système qui ne sont plus requises par NLA.

NLA prend en charge les codes d’erreur suivants pour les appels de fonction [**WSALookupServiceEnd**](/windows/desktop/api/Winsock2/nf-winsock2-wsalookupserviceend) .

| Error                | Signification                                                                                                   |
|----------------------|-----------------------------------------------------------------------------------------------------------|
| WSANOTINITIALISED    | Un appel réussi à la fonction [**WSAStartup**](/windows/desktop/api/winsock/nf-winsock-wsastartup) pour initialiser NLA n’a pas été effectué. |
| \_descripteur WSA non valide \_ | Le handle fourni dans le paramètre *RECHERCHEH* n’était pas un handle NLA valide.                             |



 

 

 



