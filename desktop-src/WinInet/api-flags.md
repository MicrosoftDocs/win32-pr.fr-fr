---
title: Indicateurs d’API (Wininet. h)
description: La plupart des fonctions WinINet acceptent un tableau d’indicateurs en tant que paramètre. Vous trouverez ci-dessous une brève description des indicateurs définis.
ms.assetid: 63027a3b-dc59-41c4-a22a-5d6e841159aa
topic_type:
- apiref
api_name:
- INTERNET_COOKIE_EVALUATE_P3P
- INTERNET_COOKIE_THIRD_PARTY
- INTERNET_FLAG_ASYNC
- INTERNET_FLAG_CACHE_ASYNC
- INTERNET_FLAG_CACHE_IF_NET_FAIL
- INTERNET_FLAG_DONT_CACHE
- INTERNET_FLAG_EXISTING_CONNECT
- INTERNET_FLAG_FORMS_SUBMIT
- INTERNET_FLAG_FROM_CACHE
- INTERNET_FLAG_FWD_BACK
- INTERNET_FLAG_HYPERLINK
- INTERNET_FLAG_IGNORE_CERT_CN_INVALID
- INTERNET_FLAG_IGNORE_CERT_DATE_INVALID
- INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTP
- INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTPS
- INTERNET_FLAG_KEEP_CONNECTION
- INTERNET_FLAG_MAKE_PERSISTENT
- INTERNET_FLAG_MUST_CACHE_REQUEST
- INTERNET_FLAG_NEED_FILE
- INTERNET_FLAG_NO_AUTH
- INTERNET_FLAG_NO_AUTO_REDIRECT
- INTERNET_FLAG_NO_CACHE_WRITE
- INTERNET_FLAG_NO_COOKIES
- INTERNET_FLAG_NO_UI
- INTERNET_FLAG_OFFLINE
- INTERNET_FLAG_PASSIVE
- INTERNET_FLAG_PRAGMA_NOCACHE
- INTERNET_FLAG_RAW_DATA
- INTERNET_FLAG_READ_PREFETCH
- INTERNET_FLAG_RELOAD
- INTERNET_FLAG_RESTRICTED_ZONE
- INTERNET_FLAG_RESYNCHRONIZE
- INTERNET_FLAG_SECURE
- INTERNET_FLAG_TRANSFER_ASCII
- INTERNET_FLAG_TRANSFER_BINARY
- INTERNET_NO_CALLBACK
- INTERNET_OPTION_SUPPRESS_SERVER_AUTH
- WININET_API_FLAG_ASYNC
- WININET_API_FLAG_SYNC
- WININET_API_FLAG_USE_CONTEXT
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a111bf418e6cf599f99c9dfa34ca0f5025a1d779
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127518997"
---
# <a name="api-flags"></a>Indicateurs d’API

La plupart des fonctions WinINet acceptent un tableau d’indicateurs en tant que paramètre. Vous trouverez ci-dessous une brève description des indicateurs définis.

<dl> <dt>

<span id="INTERNET_COOKIE_EVALUATE_P3P"></span><span id="internet_cookie_evaluate_p3p"></span>**Le \_ cookie Internet \_ évalue \_ P3P**
</dt> <dd> <dl> <dt>

0x80
</dt> <dt>



Indique qu’un en-tête P3P (Platform for Privacy Protection) doit être associé à un cookie.


</dt> </dl> </dd> <dt>

<span id="INTERNET_COOKIE_THIRD_PARTY"></span><span id="internet_cookie_third_party"></span>**\_cookie Internet \_ tiers \_**
</dt> <dd> <dl> <dt>

0x10
</dt> <dt>



Indique qu’un cookie tiers est défini ou récupéré.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_ASYNC"></span><span id="internet_flag_async"></span>**\_indicateur Internet \_ Async**
</dt> <dd> <dl> <dt>

0x10000000
</dt> <dt>



Effectue uniquement des requêtes asynchrones sur des handles descendants du handle retourné à partir de cette fonction. Seule la fonction [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) utilise cet indicateur.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_CACHE_ASYNC"></span><span id="internet_flag_cache_async"></span>**\_cache d’indicateur Internet \_ \_ asynchrone**
</dt> <dd> <dl> <dt>

0x00000080
</dt> <dt>



Autorise l’écriture différée du cache.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_CACHE_IF_NET_FAIL"></span><span id="internet_flag_cache_if_net_fail"></span>**INTERNET \_ Flag \_ cache en \_ cas d' \_ \_ échec net**
</dt> <dd> <dl> <dt>

0x00010000
</dt> <dt>



Retourne la ressource à partir du cache en cas d’échec de la demande réseau de la ressource en raison d’une [erreur de \_ \_ \_ réinitialisation de la connexion Internet](wininet-errors.md) ou d’une erreur [ \_ Internet \_ ne peut pas \_ se connecter](wininet-errors.md) . Cet indicateur est utilisé par [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_DONT_CACHE"></span><span id="internet_flag_dont_cache"></span>**\_cache sans indicateur Internet \_ \_**
</dt> <dd> <dl> <dt>

0x04000000
</dt> <dt>



N’ajoute pas l’entité retournée au cache. Cela est identique à la valeur par défaut [, \_ indicateur \_ Internet \_ sans \_ écriture](/windows)dans le cache.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_EXISTING_CONNECT"></span><span id="internet_flag_existing_connect"></span>**\_indicateur Internet \_ existant \_ connecter**
</dt> <dd> <dl> <dt>

0x20000000
</dt> <dt>



Tente d’utiliser un objet [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) existant s’il en existe un avec les mêmes attributs que ceux requis pour effectuer la demande. Cela est utile uniquement avec les opérations FTP, car FTP est le seul protocole qui effectue généralement plusieurs opérations au cours de la même session. WinINet met en cache un handle de connexion unique pour chaque handle [**HINTERNET**](appendix-a-hinternet-handles.md) généré par [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena). Les fonctions [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) et **internetconnect** utilisent cet indicateur pour les connexions HTTP et FTP.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_FORMS_SUBMIT"></span><span id="internet_flag_forms_submit"></span>**\_envoi de \_ formulaires d’indicateur Internet \_**
</dt> <dd> <dl> <dt>

0x00000040
</dt> <dt>



Indique qu’il s’agit d’une soumission de formulaires.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_FROM_CACHE"></span><span id="internet_flag_from_cache"></span>**\_indicateur Internet \_ à partir du \_ cache**
</dt> <dd> <dl> <dt>

0x01000000
</dt> <dt>



N’effectue pas de demandes réseau. Toutes les entités sont retournées à partir du cache. Si l’élément demandé n’est pas dans le cache, une erreur appropriée, telle qu’un fichier d’erreur \_ \_ \_ introuvable, est retournée. Seule la fonction [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) utilise cet indicateur.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_FWD_BACK"></span><span id="internet_flag_fwd_back"></span>**\_indicateur de \_ \_ retour sur Internet**
</dt> <dd> <dl> <dt>

0x00000020
</dt> <dt>



Indique que la fonction doit utiliser la copie de la ressource qui se trouve actuellement dans le cache Internet. La date d’expiration et les autres informations relatives à la ressource ne sont pas vérifiées. Si l’élément demandé est introuvable dans le cache Internet, le système tente de localiser la ressource sur le réseau. Cette valeur a été introduite dans Microsoft Internet Explorer 5 et est associée aux opérations de bouton **suivant** et **précédent** d’Internet Explorer.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_HYPERLINK"></span><span id="internet_flag_hyperlink"></span>**\_ \_ lien hypertexte indicateur Internet**
</dt> <dd> <dl> <dt>

0x00000400
</dt> <dt>



Force un rechargement s’il n’y a pas de délai d’expiration et qu’aucune heure LastModified n’est retournée par le serveur pour déterminer s’il faut recharger l’élément à partir du réseau. Cet indicateur peut être utilisé par [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)et [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).

**Windows XP et Windows Server 2003 R2 et versions antérieures :** Également utilisé par [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) et [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="internet_flag_ignore_cert_cn_invalid"></span>**indicateur INTERNET ignore le nom de \_ \_ \_ certificat \_ CN \_ non valide**
</dt> <dd> <dl> <dt>

0x00001000
</dt> <dt>



Désactive la vérification des certificats SSL/PCT retournés par le serveur par rapport au nom d’hôte spécifié dans la demande. WinINet utilise une simple vérification par rapport aux certificats en comparant les noms d’hôte correspondants et les règles de caractères génériques simples. Cet indicateur peut être utilisé par [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) et [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (pour les requêtes http).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="internet_flag_ignore_cert_date_invalid"></span>**\_indicateur Internet \_ ignorer la date du \_ certificat \_ \_ non valide**
</dt> <dd> <dl> <dt>

0x00002000
</dt> <dt>



Désactive la vérification des certificats basés sur SSL/PCT pour les dates de validité appropriées. Cet indicateur peut être utilisé par [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) et [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (pour les requêtes http).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTP"></span><span id="internet_flag_ignore_redirect_to_http"></span>**\_indicateur Internet \_ Ignorer \_ la redirection \_ vers \_ http**
</dt> <dd> <dl> <dt>

0x00008000
</dt> <dt>



Désactive la détection de ce type spécial de redirection. Lorsque cet indicateur est utilisé, WinINet autorise en toute transparence les redirections à partir de HTTPs vers les URL HTTP. Cet indicateur peut être utilisé par [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) et [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (pour les requêtes http).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTPS"></span><span id="internet_flag_ignore_redirect_to_https"></span>**\_indicateur Internet \_ Ignorer \_ la redirection \_ vers \_ https**
</dt> <dd> <dl> <dt>

0x00004000
</dt> <dt>



Désactive la détection de ce type spécial de redirection. Lorsque cet indicateur est utilisé, WinINet autorise en toute transparence les redirections des URL HTTP vers HTTPs. Cet indicateur peut être utilisé par [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) et [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (pour les requêtes http).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_KEEP_CONNECTION"></span><span id="internet_flag_keep_connection"></span>**\_indicateur Internet \_ maintenir la \_ connexion**
</dt> <dd> <dl> <dt>

0x00400000
</dt> <dt>



Utilise la sémantique Keep-Alive, si elle est disponible, pour la connexion. Cet indicateur est utilisé par [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) et [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (pour les requêtes http). Cet indicateur est requis pour Microsoft Network (MSN), NTLM et d’autres types d’authentification.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_MAKE_PERSISTENT"></span><span id="internet_flag_make_persistent"></span>**\_indicateur Internet \_ rendre \_ persistant**
</dt> <dd> <dl> <dt>

0x02000000
</dt> <dt>



N'est plus pris en charge.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_MUST_CACHE_REQUEST"></span><span id="internet_flag_must_cache_request"></span>**l' \_ indicateur Internet \_ doit mettre \_ en cache la \_ demande**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Identique à la valeur par défaut, l' **indicateur Internet a besoin d’un \_ \_ \_ fichier**. Entraîne la création d’un fichier temporaire si le fichier ne peut pas être mis en cache. Cet indicateur peut être utilisé par [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)et [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).

**Windows XP et Windows Server 2003 R2 et versions antérieures :** Également utilisé par [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) et [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_NEED_FILE"></span><span id="internet_flag_need_file"></span>**fichier de l' \_ indicateur Internet \_ requis \_**
</dt> <dd> <dl> <dt>

0x00000010
</dt> <dt>



Entraîne la création d’un fichier temporaire si le fichier ne peut pas être mis en cache. Cet indicateur peut être utilisé par [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)et [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).

**Windows XP et Windows Server 2003 R2 et versions antérieures :** Également utilisé par [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) et [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_NO_AUTH"></span><span id="internet_flag_no_auth"></span>**\_indicateur Internet \_ sans \_ authentification**
</dt> <dd> <dl> <dt>

0x00040000
</dt> <dt>



Ne tente pas d’effectuer l’authentification automatiquement. Cet indicateur peut être utilisé par [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) et [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (pour les requêtes http).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_NO_AUTO_REDIRECT"></span><span id="internet_flag_no_auto_redirect"></span>**\_indicateur Internet \_ sans \_ \_ redirection automatique**
</dt> <dd> <dl> <dt>

0x00200000
</dt> <dt>



Ne gère pas automatiquement la redirection dans [**HTTPSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta). Cet indicateur peut également être utilisé par [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) pour les requêtes http.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_NO_CACHE_WRITE"></span><span id="internet_flag_no_cache_write"></span>**\_indicateur Internet \_ sans \_ \_ écriture dans le cache**
</dt> <dd> <dl> <dt>

0x04000000
</dt> <dt>



N’ajoute pas l’entité retournée au cache. Cet indicateur est utilisé par, [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)et [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).

**Windows XP et Windows Server 2003 R2 et versions antérieures :** Également utilisé par [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) et [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_NO_COOKIES"></span><span id="internet_flag_no_cookies"></span>**\_indicateur Internet \_ sans \_ cookies**
</dt> <dd> <dl> <dt>

0x00080000
</dt> <dt>



N’ajoute pas automatiquement les en-têtes de cookie aux demandes et n’ajoute pas automatiquement les cookies renvoyés à la base de données de cookies. Cet indicateur peut être utilisé par [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) et [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (pour les requêtes http).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_NO_UI"></span><span id="internet_flag_no_ui"></span>**\_indicateur Internet \_ sans \_ interface utilisateur**
</dt> <dd> <dl> <dt>

0x00000200
</dt> <dt>



Désactive la boîte de dialogue cookie. Cet indicateur peut être utilisé par [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) et [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (requêtes http uniquement).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_OFFLINE"></span><span id="internet_flag_offline"></span>**\_indicateur Internet \_ hors connexion**
</dt> <dd> <dl> <dt>

0x01000000
</dt> <dt>



Identique à **l' \_ indicateur Internet \_ du \_ cache**. N’effectue pas de demandes réseau. Toutes les entités sont retournées à partir du cache. Si l’élément demandé n’est pas dans le cache, une erreur appropriée, telle qu’un fichier d’erreur \_ \_ \_ introuvable, est retournée. Seule la fonction [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) utilise cet indicateur.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_PASSIVE"></span><span id="internet_flag_passive"></span>**\_indicateur Internet \_ passif**
</dt> <dd> <dl> <dt>

0x08000000
</dt> <dt>



Utilise la sémantique FTP passive. Seuls [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) et [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) utilisent cet indicateur. [**Internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) utilise cet indicateur pour les requêtes FTP et [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) utilise cet indicateur pour les fichiers et les répertoires FTP.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_PRAGMA_NOCACHE"></span><span id="internet_flag_pragma_nocache"></span>**\_indicateur Internet \_ pragma \_ NoCache**
</dt> <dd> <dl> <dt>

0x00000100
</dt> <dt>



Force la résolution de la demande par le serveur d’origine, même si une copie mise en cache existe sur le proxy. La fonction [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (sur les requêtes HTTP et HTTPS uniquement) et la fonction [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) utilisent cet indicateur.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_RAW_DATA"></span><span id="internet_flag_raw_data"></span>**\_ \_ données brutes de drapeau Internet \_**
</dt> <dd> <dl> <dt>

0x40000000
</dt> <dt>



Retourne les données sous la forme d’une structure de [**\_ \_ données de recherche Win32**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) lors de la récupération des informations de répertoire FTP. Si cet indicateur n’est pas spécifié ou si l’appel est effectué via un proxy CERN, [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) retourne la version HTML du répertoire. Seule la fonction [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) utilise cet indicateur.

**Windows XP et Windows Server 2003 R2 et versions antérieures :** Retourne également une structure de [**\_ \_ données Gopher Find**](/windows/desktop/api/Wininet/ns-wininet-gopher_find_dataa) lors de la récupération des informations de répertoire Gopher.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_READ_PREFETCH"></span><span id="internet_flag_read_prefetch"></span>**\_indicateur Internet \_ lecture \_ prérécupération**
</dt> <dd> <dl> <dt>

0x00100000
</dt> <dt>



Cet indicateur est actuellement désactivé.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_RELOAD"></span><span id="internet_flag_reload"></span>**\_REchargement des indicateurs Internet \_**
</dt> <dd> <dl> <dt>

0x80000000
</dt> <dt>



Force le téléchargement du fichier, de l’objet ou de la liste de répertoires demandés à partir du serveur d’origine, et non à partir du cache. Les fonctions [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)et [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) utilisent cet indicateur.

**Windows XP et Windows Server 2003 R2 et versions antérieures :** Également utilisé par [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) et [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_RESTRICTED_ZONE"></span><span id="internet_flag_restricted_zone"></span>**\_ \_ zone RESTREINTe \_ Internet**
</dt> <dd> <dl> <dt>

0x00020000
</dt> <dt>



Indique que le cookie en cours de définition est associé à un site non approuvé.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_RESYNCHRONIZE"></span><span id="internet_flag_resynchronize"></span>**resynchronisation des \_ indicateurs Internet \_**
</dt> <dd> <dl> <dt>

0x00000800
</dt> <dt>



Recharge les ressources HTTP si la ressource a été modifiée depuis son dernier téléchargement. Toutes les ressources FTP sont rechargées. Cet indicateur peut être utilisé par [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)et [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).

**Windows XP et Windows Server 2003 R2 et versions antérieures :** Également utilisé par [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) et [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea), et les ressources Gopher sont rechargées.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_SECURE"></span><span id="internet_flag_secure"></span>**\_indicateur Internet \_ sécurisé**
</dt> <dd> <dl> <dt>

0x00800000
</dt> <dt>



Utilise la sémantique des transactions sécurisées. Cela se traduit par l’utilisation de la technologie de communication SSL (Secure Sockets Layer)/privée (SSL/PCT) et n’est significative que pour les requêtes HTTP. Cet indicateur est utilisé par [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) et [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), mais il est redondant si https://apparaît dans l’URL. La fonction [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) utilise cet indicateur pour les connexions http ; tous les descripteurs de demande créés sous cette connexion héritent de cet indicateur.


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_TRANSFER_ASCII"></span><span id="internet_flag_transfer_ascii"></span>**\_transfert de drapeau Internet \_ \_ ASCII**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Transfère le fichier au format ASCII (FTP uniquement). Cet indicateur peut être utilisé par [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)et [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea).


</dt> </dl> </dd> <dt>

<span id="INTERNET_FLAG_TRANSFER_BINARY"></span><span id="internet_flag_transfer_binary"></span>**\_binaire de \_ transfert de drapeau Internet \_**
</dt> <dd> <dl> <dt>

0x00000002
</dt> <dt>



Transfère le fichier au format binaire (FTP uniquement). Cet indicateur peut être utilisé par [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)et [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea).


</dt> </dl> </dd> <dt>

<span id="INTERNET_NO_CALLBACK"></span><span id="internet_no_callback"></span>**INTERNET \_ sans \_ rappel**
</dt> <dd> <dl> <dt>

0x00000000
</dt> <dt>



Indique qu’aucun rappel ne doit être effectué pour cette API. Il est utilisé pour le paramètre *dxContext* des fonctions qui autorisent les opérations asynchrones.


</dt> </dl> </dd> <dt>

<span id="INTERNET_OPTION_SUPPRESS_SERVER_AUTH"></span><span id="internet_option_suppress_server_auth"></span>**\_option Internet \_ supprimer \_ l' \_ authentification du serveur**
</dt> <dd> <dl> <dt>

104
</dt> <dt>



Définit un objet de requête HTTP de sorte qu’il ne se connecte pas aux serveurs d’origine, mais effectue une ouverture de session automatique sur les serveurs proxy HTTP. Cette option diffère de l’indicateur de requête INTERNET \_ Flag \_ no \_ auth, qui empêche l’authentification aux serveurs proxy et aux serveurs d’origine. En définissant ce mode, vous supprimez l’utilisation de tout document d’informations d’identification (nom d’utilisateur/mot de passe ou certificat SSL client précédemment fourni) lors de la communication avec un serveur d’origine. Toutefois, si la demande doit transiter via un proxy d’authentification, WinINet effectue toujours l’authentification automatique sur le proxy HTTP en fonction des paramètres de la zone Intranet de l’utilisateur. Le paramètre de zone Intranet par défaut permet d’autoriser l’ouverture de session automatique à l’aide des informations d’identification par défaut de l’utilisateur. Pour garantir la suppression de toutes les informations d’identification, l’appelant doit combiner l' \_ option Internet option \_ supprimer \_ \_ l’authentification du serveur avec l' \_ indicateur de requête Internet indicateur \_ aucun \_ cookie. Cette option ne peut être définie que sur des objets de requête avant d’être envoyés. Toute tentative de définition de cette option après l’envoi de la demande retourne l’état d’erreur du \_ \_ handle Internet incorrect \_ \_ . Aucune mémoire tampon n’est requise pour cette option. Cela est utilisé par InternetSetOption sur les handles retournés par HttpOpenRequest uniquement. Version : nécessite Internet Explorer 8,0 ou version ultérieure.


</dt> </dl> </dd> <dt>

<span id="WININET_API_FLAG_ASYNC"></span><span id="wininet_api_flag_async"></span>**\_indicateur d’API WinInet \_ \_ Async**
</dt> <dd> <dl> <dt>

0x00000001
</dt> <dt>



Force les opérations asynchrones.


</dt> </dl> </dd> <dt>

<span id="WININET_API_FLAG_SYNC"></span><span id="wininet_api_flag_sync"></span>**synchronisation des indicateurs de l' \_ API WinInet \_ \_**
</dt> <dd> <dl> <dt>

0x00000004
</dt> <dt>



Force les opérations synchrones.


</dt> </dl> </dd> <dt>

<span id="WININET_API_FLAG_USE_CONTEXT"></span><span id="wininet_api_flag_use_context"></span>**contexte d’utilisation de l' \_ indicateur d’API WinInet \_ \_ \_**
</dt> <dd> <dl> <dt>

0x00000008
</dt> <dt>



Force l’API à utiliser la valeur de contexte, même si elle est définie sur zéro.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Remarques

> [!Note]  
> WinINet ne prend pas en charge les implémentations de serveur. En outre, il ne doit pas être utilisé à partir d’un service. pour les implémentations de serveur ou les services [, utilisez Microsoft Windows HTTP services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                           |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Wininet. h</dt> </dl> |



 

