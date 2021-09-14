---
description: Gestion des cookies dans WinHTTP
ms.assetid: ef0f0847-05f6-4477-8e48-e0bea66314ab
title: Gestion des cookies dans WinHTTP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e3b596225dc3c741ab9ed0139a63e343e7afb3d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127414539"
---
# <a name="cookie-handling-in-winhttp"></a>Gestion des cookies dans WinHTTP

Les données de session HTTP sont transmises entre le client et le serveur dans l’en-tête de cookie de la demande ou de la réponse. Le serveur envoie des cookies au client dans l’en-tête Set-Cookie de la réponse et l’API WinHTTP renvoie le cookie de serveur au serveur dans l’en-tête du cookie de la demande. Les spécifications de gestion des cookies, décrites dans le document RFC 2109 (mécanisme de gestion d’état HTTP), sont implémentées par défaut dans WinHTTP. Les spécifications de gestion des cookies récentes, décrites dans le document RFC 2964, ne sont pas prises en charge par WinHTTP.

WinHTTP obtient le cookie de l’en-tête serveurs Set-Cookie et le stocke dans un cache pour chaque session. Ce cookie est renvoyé sur les demandes suivantes dans la même session WinHTTP où la cible correspond à la source du cookie. L’API WinHTTP régénère l’en-tête du cookie de la demande pour chaque tronçon de la demande.

La liste suivante décrit plusieurs options que les applications clientes WinHTTP peuvent utiliser pour gérer les cookies :

-   Gestion automatique des cookies : WinHTTP gère automatiquement les cookies et l’application cliente n’effectue aucune gestion personnalisée des cookies.
-   Désactiver la gestion automatique des cookies : la gestion automatique des cookies dans l’API WinHTTP est désactivée et aucun cookie n’est envoyé.
-   Spécifier manuellement tous les cookies : la gestion automatique des cookies est désactivée et l’application cliente ajoute ou supprime tous les en-têtes de cookies pour chaque demande de la session.
-   Gestion manuelle et automatique des cookies : combine la gestion automatique et manuelle des cookies.

## <a name="disabling-automatic-cookie-handling"></a>Désactivation de la gestion automatique des cookies

Pour désactiver la gestion des cookies, l’application cliente WinHTTP appelle la fonction [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) avec le paramètre *valeur dwOption* défini sur la \_ fonctionnalité de désactivation de l’option WinHTTP \_ \_ et le paramètre *lpBuffer* défini sur WinHTTP \_ désactiver \_ les cookies. Le paramètre *hInternet* peut être un handle de session ou un handle de demande. Lorsque la gestion des cookies est désactivée sur un handle de demande qui a envoyé une demande précédente, le client doit supprimer manuellement les en-têtes de cookie de requête existants avec la fonction [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) avant d’envoyer la requête suivante. Pour plus d’informations, consultez [Suppression d’en-têtes de cookies](#removing-cookie-headers).

**Remarque**  L’application cliente doit définir tous les cookies de la session après la désactivation du mode automatique.

## <a name="manually-specifying-all-cookies"></a>Spécification manuelle de tous les cookies

Lorsque la gestion automatique des cookies est désactivée, l’application cliente WinHTTP a la possibilité de spécifier manuellement tous les cookies. Pour définir manuellement le cookie, l’application appelle [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) en spécifiant l’en-tête de cookie dans le paramètre *pwszHeaders* . L’application cliente doit effacer tous les en-têtes de cookies avant de renvoyer la requête.

L’application cliente doit également modifier l’en-tête du cookie lorsque la requête a été redirigée. Pour modifier le cookie sur les demandes redirigées, le client spécifie une fonction de rappel avec [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback) qui répond au cas de rappel de redirection. Le gestionnaire de rappel doit effacer le cookie précédemment envoyé sur la demande en appelant [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders). Pour plus d’informations sur la suppression des en-têtes de cookie, consultez [suppression des en-têtes de cookies](#removing-cookie-headers).

## <a name="manual-and-automatic-cookie-handling"></a>Gestion manuelle et automatique des cookies

Les applications clientes WinHTTP peuvent combiner le mécanisme de gestion automatique des cookies WinHTTP avec la gestion manuelle des cookies. L’application ajoute des cookies personnalisés à l’en-tête de cookie généré automatiquement avant d’envoyer la demande avec la fonction [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) . Le cookie personnalisé doit être le premier en-tête de cookie de la demande pour que l’API WinHTTP met correctement en cache le cookie. L’application cliente doit également supprimer les cookies envoyés sur les demandes précédentes avant de renvoyer une demande sur le même handle de demande. Pour plus d’informations, consultez Suppression d’en-têtes de cookies.

Les cookies ajoutés à une demande avant l’appel à [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) sont inclus dans toutes les demandes WinHTTP envoyées pour le compte des appels **WinHttpSendRequest** et [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) suivants. L’application cliente peut avoir besoin de supprimer l’en-tête de cookie lorsque la requête a été redirigée. Pour effacer le cookie sur les demandes redirigées, le client spécifie une fonction de rappel avec [**WinHttpSetStatusCallback**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetstatuscallback) qui répond au cas de rappel de redirection. Le gestionnaire de rappel doit effacer le cookie qui a été précédemment envoyé sur la demande en appelant [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders). La fonction de rappel ne peut pas définir de nouveaux cookies personnalisés sur le rappel de redirection. Le client doit attendre la fin de **WinHttpReceiveResponse** avant d’ajouter de nouveaux cookies pour l’appel **WinHttpSendRequest** suivant.

## <a name="removing-cookie-headers"></a>Suppression des en-têtes de cookie

L’application cliente WinHTTP devra peut-être effacer le cookie de requête existant avant de renvoyer une demande pour empêcher les cookies qui ont été envoyés sur les demandes précédentes d’être renvoyés à nouveau sur la requête actuelle. Pour plus d’informations, consultez la remarque suivante. Sachez également que les cookies n’ont pas besoin d’être effacés avant l’envoi de la première requête sur le descripteur de demande. Le client peut effacer les cookies existants en appelant [**WinHttpAddRequestHeaders**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpaddrequestheaders) avec un en-tête de cookie vide dans le paramètre *pwszHeaders* et l' \_ \_ \_ indicateur de remplacement d’indicateur de ADDREQ WinHTTP défini dans le paramètre *dwModifier* . L’exemple de code suivant montre comment effacer l’en-tête de cookie de la demande.

``` syntax
WinHttpAddRequestHeaders( hRequest, 
                          L"Cookie:", 
                          -1, 
                          WINHTTP_ADDREQ_FLAG_REPLACE);
```

l’API WinHTTP présente différents comportements de gestion des cookies pour les versions du système d’exploitation antérieures à Windows XP avec service pack 2 (SP2) et Windows Server 2003 avec service pack 1 (SP1).

* * Windows XP avec SP2 et versions ultérieures et Windows Server 2003 avec SP1 et versions ultérieures : * *

L’API WinHTTP efface tous les cookies envoyés sur les requêtes précédentes pour le handle de demande. Le client peut ajouter manuellement de nouveaux en-têtes de cookie avant chaque appel à WinHttpSendRequest. Si la fonctionnalité de gestion automatique des cookies de l’API WinHTTP n’a pas été désactivée, l’API WinHTTP ajoute le nouvel en-tête de cookie (ou ajoute un nouvel en-tête de cookie si l’application cliente n’en a pas ajouté manuellement) avec le cookie du serveur.

* * Windows XP avec SP2 et Windows Server 2003 avec SP1 : * *

L’API WinHTTP n’efface pas l’en-tête de cookie de requête une fois [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) terminé. Les cookies envoyés dans les demandes précédentes seront renvoyés dans les appels suivants à [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest). L’application cliente WinHTTP doit effacer les en-têtes de cookies existants avant de renvoyer une demande sur le handle de demande.

 

 



