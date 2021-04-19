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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513800"
---
# <a name="api-flags"></a><span data-ttu-id="42ccb-104">Indicateurs d’API</span><span class="sxs-lookup"><span data-stu-id="42ccb-104">API Flags</span></span>

<span data-ttu-id="42ccb-105">La plupart des fonctions WinINet acceptent un tableau d’indicateurs en tant que paramètre.</span><span class="sxs-lookup"><span data-stu-id="42ccb-105">Many of the WinINet functions accept an array of flags as a parameter.</span></span> <span data-ttu-id="42ccb-106">Vous trouverez ci-dessous une brève description des indicateurs définis.</span><span class="sxs-lookup"><span data-stu-id="42ccb-106">The following is a brief description of the defined flags.</span></span>

<dl> <dt>

<span data-ttu-id="42ccb-107"><span id="INTERNET_COOKIE_EVALUATE_P3P"></span><span id="internet_cookie_evaluate_p3p"></span>**Le \_ cookie Internet \_ évalue \_ P3P**</span><span class="sxs-lookup"><span data-stu-id="42ccb-107"><span id="INTERNET_COOKIE_EVALUATE_P3P"></span><span id="internet_cookie_evaluate_p3p"></span>**INTERNET\_COOKIE\_EVALUATE\_P3P**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42ccb-108">0x80</span><span class="sxs-lookup"><span data-stu-id="42ccb-108">0x80</span></span>
</dt> <dt>



<span data-ttu-id="42ccb-109">Indique qu’un en-tête P3P (Platform for Privacy Protection) doit être associé à un cookie.</span><span class="sxs-lookup"><span data-stu-id="42ccb-109">Indicates that a Platform for Privacy Protection (P3P) header is to be associated with a cookie.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42ccb-110"><span id="INTERNET_COOKIE_THIRD_PARTY"></span><span id="internet_cookie_third_party"></span>**\_cookie Internet \_ tiers \_**</span><span class="sxs-lookup"><span data-stu-id="42ccb-110"><span id="INTERNET_COOKIE_THIRD_PARTY"></span><span id="internet_cookie_third_party"></span>**INTERNET\_COOKIE\_THIRD\_PARTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42ccb-111">0x10</span><span class="sxs-lookup"><span data-stu-id="42ccb-111">0x10</span></span>
</dt> <dt>



<span data-ttu-id="42ccb-112">Indique qu’un cookie tiers est défini ou récupéré.</span><span class="sxs-lookup"><span data-stu-id="42ccb-112">Indicates that a third-party cookie is being set or retrieved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42ccb-113"><span id="INTERNET_FLAG_ASYNC"></span><span id="internet_flag_async"></span>**\_indicateur Internet \_ Async**</span><span class="sxs-lookup"><span data-stu-id="42ccb-113"><span id="INTERNET_FLAG_ASYNC"></span><span id="internet_flag_async"></span>**INTERNET\_FLAG\_ASYNC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42ccb-114">0x10000000</span><span class="sxs-lookup"><span data-stu-id="42ccb-114">0x10000000</span></span>
</dt> <dt>



<span data-ttu-id="42ccb-115">Effectue uniquement des requêtes asynchrones sur des handles descendants du handle retourné à partir de cette fonction.</span><span class="sxs-lookup"><span data-stu-id="42ccb-115">Makes only asynchronous requests on handles descended from the handle returned from this function.</span></span> <span data-ttu-id="42ccb-116">Seule la fonction [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) utilise cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="42ccb-116">Only the [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) function uses this flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42ccb-117"><span id="INTERNET_FLAG_CACHE_ASYNC"></span><span id="internet_flag_cache_async"></span>**\_cache d’indicateur Internet \_ \_ asynchrone**</span><span class="sxs-lookup"><span data-stu-id="42ccb-117"><span id="INTERNET_FLAG_CACHE_ASYNC"></span><span id="internet_flag_cache_async"></span>**INTERNET\_FLAG\_CACHE\_ASYNC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42ccb-118">0x00000080</span><span class="sxs-lookup"><span data-stu-id="42ccb-118">0x00000080</span></span>
</dt> <dt>



<span data-ttu-id="42ccb-119">Autorise l’écriture différée du cache.</span><span class="sxs-lookup"><span data-stu-id="42ccb-119">Allows a lazy cache write.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42ccb-120"><span id="INTERNET_FLAG_CACHE_IF_NET_FAIL"></span><span id="internet_flag_cache_if_net_fail"></span>**INTERNET \_ Flag \_ cache en \_ cas d' \_ \_ échec net**</span><span class="sxs-lookup"><span data-stu-id="42ccb-120"><span id="INTERNET_FLAG_CACHE_IF_NET_FAIL"></span><span id="internet_flag_cache_if_net_fail"></span>**INTERNET\_FLAG\_CACHE\_IF\_NET\_FAIL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42ccb-121">0x00010000</span><span class="sxs-lookup"><span data-stu-id="42ccb-121">0x00010000</span></span>
</dt> <dt>



<span data-ttu-id="42ccb-122">Retourne la ressource à partir du cache en cas d’échec de la demande réseau de la ressource en raison d’une [erreur de \_ \_ \_ réinitialisation de la connexion Internet](wininet-errors.md) ou d’une erreur [ \_ Internet \_ ne peut pas \_ se connecter](wininet-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="42ccb-122">Returns the resource from the cache if the network request for the resource fails due to an [ERROR\_INTERNET\_CONNECTION\_RESET](wininet-errors.md) or [ERROR\_INTERNET\_CANNOT\_CONNECT](wininet-errors.md) error.</span></span> <span data-ttu-id="42ccb-123">Cet indicateur est utilisé par [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span><span class="sxs-lookup"><span data-stu-id="42ccb-123">This flag is used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42ccb-124"><span id="INTERNET_FLAG_DONT_CACHE"></span><span id="internet_flag_dont_cache"></span>**\_cache sans indicateur Internet \_ \_**</span><span class="sxs-lookup"><span data-stu-id="42ccb-124"><span id="INTERNET_FLAG_DONT_CACHE"></span><span id="internet_flag_dont_cache"></span>**INTERNET\_FLAG\_DONT\_CACHE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42ccb-125">0x04000000</span><span class="sxs-lookup"><span data-stu-id="42ccb-125">0x04000000</span></span>
</dt> <dt>



<span data-ttu-id="42ccb-126">N’ajoute pas l’entité retournée au cache.</span><span class="sxs-lookup"><span data-stu-id="42ccb-126">Does not add the returned entity to the cache.</span></span> <span data-ttu-id="42ccb-127">Cela est identique à la valeur par défaut [, \_ indicateur \_ Internet \_ sans \_ écriture](/windows)dans le cache.</span><span class="sxs-lookup"><span data-stu-id="42ccb-127">This is identical to the preferred value, [INTERNET\_FLAG\_NO\_CACHE\_WRITE](/windows).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42ccb-128"><span id="INTERNET_FLAG_EXISTING_CONNECT"></span><span id="internet_flag_existing_connect"></span>**\_indicateur Internet \_ existant \_ connecter**</span><span class="sxs-lookup"><span data-stu-id="42ccb-128"><span id="INTERNET_FLAG_EXISTING_CONNECT"></span><span id="internet_flag_existing_connect"></span>**INTERNET\_FLAG\_EXISTING\_CONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42ccb-129">0x20000000</span><span class="sxs-lookup"><span data-stu-id="42ccb-129">0x20000000</span></span>
</dt> <dt>



<span data-ttu-id="42ccb-130">Tente d’utiliser un objet [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) existant s’il en existe un avec les mêmes attributs que ceux requis pour effectuer la demande.</span><span class="sxs-lookup"><span data-stu-id="42ccb-130">Attempts to use an existing [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) object if one exists with the same attributes required to make the request.</span></span> <span data-ttu-id="42ccb-131">Cela est utile uniquement avec les opérations FTP, car FTP est le seul protocole qui effectue généralement plusieurs opérations au cours de la même session.</span><span class="sxs-lookup"><span data-stu-id="42ccb-131">This is useful only with FTP operations, since FTP is the only protocol that typically performs multiple operations during the same session.</span></span> <span data-ttu-id="42ccb-132">WinINet met en cache un handle de connexion unique pour chaque handle [**HINTERNET**](appendix-a-hinternet-handles.md) généré par [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span><span class="sxs-lookup"><span data-stu-id="42ccb-132">WinINet caches a single connection handle for each [**HINTERNET**](appendix-a-hinternet-handles.md) handle generated by [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span> <span data-ttu-id="42ccb-133">Les fonctions [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) et **internetconnect** utilisent cet indicateur pour les connexions HTTP et FTP.</span><span class="sxs-lookup"><span data-stu-id="42ccb-133">The [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) and **InternetConnect** functions use this flag for Http and Ftp connections.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42ccb-134"><span id="INTERNET_FLAG_FORMS_SUBMIT"></span><span id="internet_flag_forms_submit"></span>**\_envoi de \_ formulaires d’indicateur Internet \_**</span><span class="sxs-lookup"><span data-stu-id="42ccb-134"><span id="INTERNET_FLAG_FORMS_SUBMIT"></span><span id="internet_flag_forms_submit"></span>**INTERNET\_FLAG\_FORMS\_SUBMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42ccb-135">0x00000040</span><span class="sxs-lookup"><span data-stu-id="42ccb-135">0x00000040</span></span>
</dt> <dt>



<span data-ttu-id="42ccb-136">Indique qu’il s’agit d’une soumission de formulaires.</span><span class="sxs-lookup"><span data-stu-id="42ccb-136">Indicates that this is a Forms submission.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42ccb-137"><span id="INTERNET_FLAG_FROM_CACHE"></span><span id="internet_flag_from_cache"></span>**\_indicateur Internet \_ à partir du \_ cache**</span><span class="sxs-lookup"><span data-stu-id="42ccb-137"><span id="INTERNET_FLAG_FROM_CACHE"></span><span id="internet_flag_from_cache"></span>**INTERNET\_FLAG\_FROM\_CACHE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42ccb-138">0x01000000</span><span class="sxs-lookup"><span data-stu-id="42ccb-138">0x01000000</span></span>
</dt> <dt>



<span data-ttu-id="42ccb-139">N’effectue pas de demandes réseau.</span><span class="sxs-lookup"><span data-stu-id="42ccb-139">Does not make network requests.</span></span> <span data-ttu-id="42ccb-140">Toutes les entités sont retournées à partir du cache.</span><span class="sxs-lookup"><span data-stu-id="42ccb-140">All entities are returned from the cache.</span></span> <span data-ttu-id="42ccb-141">Si l’élément demandé n’est pas dans le cache, une erreur appropriée, telle qu’un fichier d’erreur \_ \_ \_ introuvable, est retournée.</span><span class="sxs-lookup"><span data-stu-id="42ccb-141">If the requested item is not in the cache, a suitable error, such as ERROR\_FILE\_NOT\_FOUND, is returned.</span></span> <span data-ttu-id="42ccb-142">Seule la fonction [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) utilise cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="42ccb-142">Only the [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) function uses this flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42ccb-143"><span id="INTERNET_FLAG_FWD_BACK"></span><span id="internet_flag_fwd_back"></span>**\_indicateur de \_ \_ retour sur Internet**</span><span class="sxs-lookup"><span data-stu-id="42ccb-143"><span id="INTERNET_FLAG_FWD_BACK"></span><span id="internet_flag_fwd_back"></span>**INTERNET\_FLAG\_FWD\_BACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42ccb-144">0x00000020</span><span class="sxs-lookup"><span data-stu-id="42ccb-144">0x00000020</span></span>
</dt> <dt>



<span data-ttu-id="42ccb-145">Indique que la fonction doit utiliser la copie de la ressource qui se trouve actuellement dans le cache Internet.</span><span class="sxs-lookup"><span data-stu-id="42ccb-145">Indicates that the function should use the copy of the resource that is currently in the Internet cache.</span></span> <span data-ttu-id="42ccb-146">La date d’expiration et les autres informations relatives à la ressource ne sont pas vérifiées.</span><span class="sxs-lookup"><span data-stu-id="42ccb-146">The expiration date and other information about the resource is not checked.</span></span> <span data-ttu-id="42ccb-147">Si l’élément demandé est introuvable dans le cache Internet, le système tente de localiser la ressource sur le réseau.</span><span class="sxs-lookup"><span data-stu-id="42ccb-147">If the requested item is not found in the Internet cache, the system attempts to locate the resource on the network.</span></span> <span data-ttu-id="42ccb-148">Cette valeur a été introduite dans Microsoft Internet Explorer 5 et est associée aux opérations de bouton **suivant** et **précédent** d’Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="42ccb-148">This value was introduced in Microsoft Internet Explorer 5 and is associated with the **Forward** and **Back** button operations of Internet Explorer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42ccb-149"><span id="INTERNET_FLAG_HYPERLINK"></span><span id="internet_flag_hyperlink"></span>**\_ \_ lien hypertexte indicateur Internet**</span><span class="sxs-lookup"><span data-stu-id="42ccb-149"><span id="INTERNET_FLAG_HYPERLINK"></span><span id="internet_flag_hyperlink"></span>**INTERNET\_FLAG\_HYPERLINK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42ccb-150">0x00000400</span><span class="sxs-lookup"><span data-stu-id="42ccb-150">0x00000400</span></span>
</dt> <dt>



<span data-ttu-id="42ccb-151">Force un rechargement s’il n’y a pas de délai d’expiration et qu’aucune heure LastModified n’est retournée par le serveur pour déterminer s’il faut recharger l’élément à partir du réseau.</span><span class="sxs-lookup"><span data-stu-id="42ccb-151">Forces a reload if there is no Expires time and no LastModified time returned from the server when determining whether to reload the item from the network.</span></span> <span data-ttu-id="42ccb-152">Cet indicateur peut être utilisé par [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)et [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span><span class="sxs-lookup"><span data-stu-id="42ccb-152">This flag can be used by [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span></span>

<span data-ttu-id="42ccb-153">**Windows XP et Windows Server 2003 R2 et versions antérieures :** Également utilisé par [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) et [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).</span><span class="sxs-lookup"><span data-stu-id="42ccb-153">**Windows XP and Windows Server 2003 R2 and earlier:** Also used by [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) and [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42ccb-154"><span id="INTERNET_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="internet_flag_ignore_cert_cn_invalid"></span>**indicateur INTERNET ignore le nom de \_ \_ \_ certificat \_ CN \_ non valide**</span><span class="sxs-lookup"><span data-stu-id="42ccb-154"><span id="INTERNET_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="internet_flag_ignore_cert_cn_invalid"></span>**INTERNET\_FLAG\_IGNORE\_CERT\_CN\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42ccb-155">0x00001000</span><span class="sxs-lookup"><span data-stu-id="42ccb-155">0x00001000</span></span>
</dt> <dt>



<span data-ttu-id="42ccb-156">Désactive la vérification des certificats SSL/PCT retournés par le serveur par rapport au nom d’hôte spécifié dans la demande.</span><span class="sxs-lookup"><span data-stu-id="42ccb-156">Disables checking of SSL/PCT-based certificates that are returned from the server against the host name given in the request.</span></span> <span data-ttu-id="42ccb-157">WinINet utilise une simple vérification par rapport aux certificats en comparant les noms d’hôte correspondants et les règles de caractères génériques simples.</span><span class="sxs-lookup"><span data-stu-id="42ccb-157">WinINet uses a simple check against certificates by comparing for matching host names and simple wildcarding rules.</span></span> <span data-ttu-id="42ccb-158">Cet indicateur peut être utilisé par [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) et [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (pour les requêtes http).</span><span class="sxs-lookup"><span data-stu-id="42ccb-158">This flag can be used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (for HTTP requests).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42ccb-159"><span id="INTERNET_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="internet_flag_ignore_cert_date_invalid"></span>**\_indicateur Internet \_ ignorer la date du \_ certificat \_ \_ non valide**</span><span class="sxs-lookup"><span data-stu-id="42ccb-159"><span id="INTERNET_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="internet_flag_ignore_cert_date_invalid"></span>**INTERNET\_FLAG\_IGNORE\_CERT\_DATE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42ccb-160">0x00002000</span><span class="sxs-lookup"><span data-stu-id="42ccb-160">0x00002000</span></span>
</dt> <dt>



<span data-ttu-id="42ccb-161">Désactive la vérification des certificats basés sur SSL/PCT pour les dates de validité appropriées.</span><span class="sxs-lookup"><span data-stu-id="42ccb-161">Disables checking of SSL/PCT-based certificates for proper validity dates.</span></span> <span data-ttu-id="42ccb-162">Cet indicateur peut être utilisé par [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) et [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (pour les requêtes http).</span><span class="sxs-lookup"><span data-stu-id="42ccb-162">This flag can be used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (for HTTP requests).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42ccb-163"><span id="INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTP"></span><span id="internet_flag_ignore_redirect_to_http"></span>**\_indicateur Internet \_ Ignorer \_ la redirection \_ vers \_ http**</span><span class="sxs-lookup"><span data-stu-id="42ccb-163"><span id="INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTP"></span><span id="internet_flag_ignore_redirect_to_http"></span>**INTERNET\_FLAG\_IGNORE\_REDIRECT\_TO\_HTTP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42ccb-164">0x00008000</span><span class="sxs-lookup"><span data-stu-id="42ccb-164">0x00008000</span></span>
</dt> <dt>



<span data-ttu-id="42ccb-165">Désactive la détection de ce type spécial de redirection.</span><span class="sxs-lookup"><span data-stu-id="42ccb-165">Disables detection of this special type of redirect.</span></span> <span data-ttu-id="42ccb-166">Lorsque cet indicateur est utilisé, WinINet autorise en toute transparence les redirections à partir de HTTPs vers les URL HTTP.</span><span class="sxs-lookup"><span data-stu-id="42ccb-166">When this flag is used, WinINet transparently allows redirects from HTTPS to HTTP URLs.</span></span> <span data-ttu-id="42ccb-167">Cet indicateur peut être utilisé par [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) et [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (pour les requêtes http).</span><span class="sxs-lookup"><span data-stu-id="42ccb-167">This flag can be used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (for HTTP requests).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42ccb-168"><span id="INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTPS"></span><span id="internet_flag_ignore_redirect_to_https"></span>**\_indicateur Internet \_ Ignorer \_ la redirection \_ vers \_ https**</span><span class="sxs-lookup"><span data-stu-id="42ccb-168"><span id="INTERNET_FLAG_IGNORE_REDIRECT_TO_HTTPS"></span><span id="internet_flag_ignore_redirect_to_https"></span>**INTERNET\_FLAG\_IGNORE\_REDIRECT\_TO\_HTTPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42ccb-169">0x00004000</span><span class="sxs-lookup"><span data-stu-id="42ccb-169">0x00004000</span></span>
</dt> <dt>



<span data-ttu-id="42ccb-170">Désactive la détection de ce type spécial de redirection.</span><span class="sxs-lookup"><span data-stu-id="42ccb-170">Disables detection of this special type of redirect.</span></span> <span data-ttu-id="42ccb-171">Lorsque cet indicateur est utilisé, WinINet autorise en toute transparence les redirections des URL HTTP vers HTTPs.</span><span class="sxs-lookup"><span data-stu-id="42ccb-171">When this flag is used, WinINet transparently allow redirects from HTTP to HTTPS URLs.</span></span> <span data-ttu-id="42ccb-172">Cet indicateur peut être utilisé par [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) et [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (pour les requêtes http).</span><span class="sxs-lookup"><span data-stu-id="42ccb-172">This flag can be used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (for HTTP requests).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42ccb-173"><span id="INTERNET_FLAG_KEEP_CONNECTION"></span><span id="internet_flag_keep_connection"></span>**\_indicateur Internet \_ maintenir la \_ connexion**</span><span class="sxs-lookup"><span data-stu-id="42ccb-173"><span id="INTERNET_FLAG_KEEP_CONNECTION"></span><span id="internet_flag_keep_connection"></span>**INTERNET\_FLAG\_KEEP\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42ccb-174">0x00400000</span><span class="sxs-lookup"><span data-stu-id="42ccb-174">0x00400000</span></span>
</dt> <dt>



<span data-ttu-id="42ccb-175">Utilise la sémantique Keep-Alive, si elle est disponible, pour la connexion.</span><span class="sxs-lookup"><span data-stu-id="42ccb-175">Uses keep-alive semantics, if available, for the connection.</span></span> <span data-ttu-id="42ccb-176">Cet indicateur est utilisé par [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) et [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (pour les requêtes http).</span><span class="sxs-lookup"><span data-stu-id="42ccb-176">This flag is used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (for HTTP requests).</span></span> <span data-ttu-id="42ccb-177">Cet indicateur est requis pour Microsoft Network (MSN), NTLM et d’autres types d’authentification.</span><span class="sxs-lookup"><span data-stu-id="42ccb-177">This flag is required for Microsoft Network (MSN), NTLM, and other types of authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42ccb-178"><span id="INTERNET_FLAG_MAKE_PERSISTENT"></span><span id="internet_flag_make_persistent"></span>**\_indicateur Internet \_ rendre \_ persistant**</span><span class="sxs-lookup"><span data-stu-id="42ccb-178"><span id="INTERNET_FLAG_MAKE_PERSISTENT"></span><span id="internet_flag_make_persistent"></span>**INTERNET\_FLAG\_MAKE\_PERSISTENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42ccb-179">0x02000000</span><span class="sxs-lookup"><span data-stu-id="42ccb-179">0x02000000</span></span>
</dt> <dt>



<span data-ttu-id="42ccb-180">N'est plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="42ccb-180">No longer supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42ccb-181"><span id="INTERNET_FLAG_MUST_CACHE_REQUEST"></span><span id="internet_flag_must_cache_request"></span>**l' \_ indicateur Internet \_ doit mettre \_ en cache la \_ demande**</span><span class="sxs-lookup"><span data-stu-id="42ccb-181"><span id="INTERNET_FLAG_MUST_CACHE_REQUEST"></span><span id="internet_flag_must_cache_request"></span>**INTERNET\_FLAG\_MUST\_CACHE\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42ccb-182">0x00000010</span><span class="sxs-lookup"><span data-stu-id="42ccb-182">0x00000010</span></span>
</dt> <dt>



<span data-ttu-id="42ccb-183">Identique à la valeur par défaut, l' **indicateur Internet a besoin d’un \_ \_ \_ fichier**.</span><span class="sxs-lookup"><span data-stu-id="42ccb-183">Identical to the preferred value, **INTERNET\_FLAG\_NEED\_FILE**.</span></span> <span data-ttu-id="42ccb-184">Entraîne la création d’un fichier temporaire si le fichier ne peut pas être mis en cache.</span><span class="sxs-lookup"><span data-stu-id="42ccb-184">Causes a temporary file to be created if the file cannot be cached.</span></span> <span data-ttu-id="42ccb-185">Cet indicateur peut être utilisé par [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)et [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span><span class="sxs-lookup"><span data-stu-id="42ccb-185">This flag can be used by [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span></span>

<span data-ttu-id="42ccb-186">**Windows XP et Windows Server 2003 R2 et versions antérieures :** Également utilisé par [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) et [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).</span><span class="sxs-lookup"><span data-stu-id="42ccb-186">**Windows XP and Windows Server 2003 R2 and earlier:** Also used by [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) and [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42ccb-187"><span id="INTERNET_FLAG_NEED_FILE"></span><span id="internet_flag_need_file"></span>**fichier de l' \_ indicateur Internet \_ requis \_**</span><span class="sxs-lookup"><span data-stu-id="42ccb-187"><span id="INTERNET_FLAG_NEED_FILE"></span><span id="internet_flag_need_file"></span>**INTERNET\_FLAG\_NEED\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42ccb-188">0x00000010</span><span class="sxs-lookup"><span data-stu-id="42ccb-188">0x00000010</span></span>
</dt> <dt>



<span data-ttu-id="42ccb-189">Entraîne la création d’un fichier temporaire si le fichier ne peut pas être mis en cache.</span><span class="sxs-lookup"><span data-stu-id="42ccb-189">Causes a temporary file to be created if the file cannot be cached.</span></span> <span data-ttu-id="42ccb-190">Cet indicateur peut être utilisé par [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)et [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span><span class="sxs-lookup"><span data-stu-id="42ccb-190">This flag can be used by [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span></span>

<span data-ttu-id="42ccb-191">**Windows XP et Windows Server 2003 R2 et versions antérieures :** Également utilisé par [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) et [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).</span><span class="sxs-lookup"><span data-stu-id="42ccb-191">**Windows XP and Windows Server 2003 R2 and earlier:** Also used by [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) and [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42ccb-192"><span id="INTERNET_FLAG_NO_AUTH"></span><span id="internet_flag_no_auth"></span>**\_indicateur Internet \_ sans \_ authentification**</span><span class="sxs-lookup"><span data-stu-id="42ccb-192"><span id="INTERNET_FLAG_NO_AUTH"></span><span id="internet_flag_no_auth"></span>**INTERNET\_FLAG\_NO\_AUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42ccb-193">0x00040000</span><span class="sxs-lookup"><span data-stu-id="42ccb-193">0x00040000</span></span>
</dt> <dt>



<span data-ttu-id="42ccb-194">Ne tente pas d’effectuer l’authentification automatiquement.</span><span class="sxs-lookup"><span data-stu-id="42ccb-194">Does not attempt authentication automatically.</span></span> <span data-ttu-id="42ccb-195">Cet indicateur peut être utilisé par [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) et [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (pour les requêtes http).</span><span class="sxs-lookup"><span data-stu-id="42ccb-195">This flag can be used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (for HTTP requests).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42ccb-196"><span id="INTERNET_FLAG_NO_AUTO_REDIRECT"></span><span id="internet_flag_no_auto_redirect"></span>**\_indicateur Internet \_ sans \_ \_ redirection automatique**</span><span class="sxs-lookup"><span data-stu-id="42ccb-196"><span id="INTERNET_FLAG_NO_AUTO_REDIRECT"></span><span id="internet_flag_no_auto_redirect"></span>**INTERNET\_FLAG\_NO\_AUTO\_REDIRECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42ccb-197">0x00200000</span><span class="sxs-lookup"><span data-stu-id="42ccb-197">0x00200000</span></span>
</dt> <dt>



<span data-ttu-id="42ccb-198">Ne gère pas automatiquement la redirection dans [**HTTPSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span><span class="sxs-lookup"><span data-stu-id="42ccb-198">Does not automatically handle redirection in [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span></span> <span data-ttu-id="42ccb-199">Cet indicateur peut également être utilisé par [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) pour les requêtes http.</span><span class="sxs-lookup"><span data-stu-id="42ccb-199">This flag can also be used by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) for HTTP requests.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42ccb-200"><span id="INTERNET_FLAG_NO_CACHE_WRITE"></span><span id="internet_flag_no_cache_write"></span>**\_indicateur Internet \_ sans \_ \_ écriture dans le cache**</span><span class="sxs-lookup"><span data-stu-id="42ccb-200"><span id="INTERNET_FLAG_NO_CACHE_WRITE"></span><span id="internet_flag_no_cache_write"></span>**INTERNET\_FLAG\_NO\_CACHE\_WRITE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42ccb-201">0x04000000</span><span class="sxs-lookup"><span data-stu-id="42ccb-201">0x04000000</span></span>
</dt> <dt>



<span data-ttu-id="42ccb-202">N’ajoute pas l’entité retournée au cache.</span><span class="sxs-lookup"><span data-stu-id="42ccb-202">Does not add the returned entity to the cache.</span></span> <span data-ttu-id="42ccb-203">Cet indicateur est utilisé par, [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)et [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span><span class="sxs-lookup"><span data-stu-id="42ccb-203">This flag is used by , [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span></span>

<span data-ttu-id="42ccb-204">**Windows XP et Windows Server 2003 R2 et versions antérieures :** Également utilisé par [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) et [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).</span><span class="sxs-lookup"><span data-stu-id="42ccb-204">**Windows XP and Windows Server 2003 R2 and earlier:** Also used by [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) and [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42ccb-205"><span id="INTERNET_FLAG_NO_COOKIES"></span><span id="internet_flag_no_cookies"></span>**\_indicateur Internet \_ sans \_ cookies**</span><span class="sxs-lookup"><span data-stu-id="42ccb-205"><span id="INTERNET_FLAG_NO_COOKIES"></span><span id="internet_flag_no_cookies"></span>**INTERNET\_FLAG\_NO\_COOKIES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42ccb-206">0x00080000</span><span class="sxs-lookup"><span data-stu-id="42ccb-206">0x00080000</span></span>
</dt> <dt>



<span data-ttu-id="42ccb-207">N’ajoute pas automatiquement les en-têtes de cookie aux demandes et n’ajoute pas automatiquement les cookies renvoyés à la base de données de cookies.</span><span class="sxs-lookup"><span data-stu-id="42ccb-207">Does not automatically add cookie headers to requests, and does not automatically add returned cookies to the cookie database.</span></span> <span data-ttu-id="42ccb-208">Cet indicateur peut être utilisé par [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) et [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (pour les requêtes http).</span><span class="sxs-lookup"><span data-stu-id="42ccb-208">This flag can be used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (for HTTP requests).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42ccb-209"><span id="INTERNET_FLAG_NO_UI"></span><span id="internet_flag_no_ui"></span>**\_indicateur Internet \_ sans \_ interface utilisateur**</span><span class="sxs-lookup"><span data-stu-id="42ccb-209"><span id="INTERNET_FLAG_NO_UI"></span><span id="internet_flag_no_ui"></span>**INTERNET\_FLAG\_NO\_UI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42ccb-210">0x00000200</span><span class="sxs-lookup"><span data-stu-id="42ccb-210">0x00000200</span></span>
</dt> <dt>



<span data-ttu-id="42ccb-211">Désactive la boîte de dialogue cookie.</span><span class="sxs-lookup"><span data-stu-id="42ccb-211">Disables the cookie dialog box.</span></span> <span data-ttu-id="42ccb-212">Cet indicateur peut être utilisé par [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) et [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (requêtes http uniquement).</span><span class="sxs-lookup"><span data-stu-id="42ccb-212">This flag can be used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (HTTP requests only).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42ccb-213"><span id="INTERNET_FLAG_OFFLINE"></span><span id="internet_flag_offline"></span>**\_indicateur Internet \_ hors connexion**</span><span class="sxs-lookup"><span data-stu-id="42ccb-213"><span id="INTERNET_FLAG_OFFLINE"></span><span id="internet_flag_offline"></span>**INTERNET\_FLAG\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42ccb-214">0x01000000</span><span class="sxs-lookup"><span data-stu-id="42ccb-214">0x01000000</span></span>
</dt> <dt>



<span data-ttu-id="42ccb-215">Identique à **l' \_ indicateur Internet \_ du \_ cache**.</span><span class="sxs-lookup"><span data-stu-id="42ccb-215">Identical to **INTERNET\_FLAG\_FROM\_CACHE**.</span></span> <span data-ttu-id="42ccb-216">N’effectue pas de demandes réseau.</span><span class="sxs-lookup"><span data-stu-id="42ccb-216">Does not make network requests.</span></span> <span data-ttu-id="42ccb-217">Toutes les entités sont retournées à partir du cache.</span><span class="sxs-lookup"><span data-stu-id="42ccb-217">All entities are returned from the cache.</span></span> <span data-ttu-id="42ccb-218">Si l’élément demandé n’est pas dans le cache, une erreur appropriée, telle qu’un fichier d’erreur \_ \_ \_ introuvable, est retournée.</span><span class="sxs-lookup"><span data-stu-id="42ccb-218">If the requested item is not in the cache, a suitable error, such as ERROR\_FILE\_NOT\_FOUND, is returned.</span></span> <span data-ttu-id="42ccb-219">Seule la fonction [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) utilise cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="42ccb-219">Only the [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) function uses this flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42ccb-220"><span id="INTERNET_FLAG_PASSIVE"></span><span id="internet_flag_passive"></span>**\_indicateur Internet \_ passif**</span><span class="sxs-lookup"><span data-stu-id="42ccb-220"><span id="INTERNET_FLAG_PASSIVE"></span><span id="internet_flag_passive"></span>**INTERNET\_FLAG\_PASSIVE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42ccb-221">0x08000000</span><span class="sxs-lookup"><span data-stu-id="42ccb-221">0x08000000</span></span>
</dt> <dt>



<span data-ttu-id="42ccb-222">Utilise la sémantique FTP passive.</span><span class="sxs-lookup"><span data-stu-id="42ccb-222">Uses passive FTP semantics.</span></span> <span data-ttu-id="42ccb-223">Seuls [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) et [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) utilisent cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="42ccb-223">Only [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) use this flag.</span></span> <span data-ttu-id="42ccb-224">[**Internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) utilise cet indicateur pour les requêtes FTP et [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) utilise cet indicateur pour les fichiers et les répertoires FTP.</span><span class="sxs-lookup"><span data-stu-id="42ccb-224">[**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) uses this flag for FTP requests, and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) uses this flag for FTP files and directories.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42ccb-225"><span id="INTERNET_FLAG_PRAGMA_NOCACHE"></span><span id="internet_flag_pragma_nocache"></span>**\_indicateur Internet \_ pragma \_ NoCache**</span><span class="sxs-lookup"><span data-stu-id="42ccb-225"><span id="INTERNET_FLAG_PRAGMA_NOCACHE"></span><span id="internet_flag_pragma_nocache"></span>**INTERNET\_FLAG\_PRAGMA\_NOCACHE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42ccb-226">0x00000100</span><span class="sxs-lookup"><span data-stu-id="42ccb-226">0x00000100</span></span>
</dt> <dt>



<span data-ttu-id="42ccb-227">Force la résolution de la demande par le serveur d’origine, même si une copie mise en cache existe sur le proxy.</span><span class="sxs-lookup"><span data-stu-id="42ccb-227">Forces the request to be resolved by the origin server, even if a cached copy exists on the proxy.</span></span> <span data-ttu-id="42ccb-228">La fonction [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) (sur les requêtes HTTP et HTTPS uniquement) et la fonction [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) utilisent cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="42ccb-228">The [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) function (on HTTP and HTTPS requests only) and [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) function use this flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42ccb-229"><span id="INTERNET_FLAG_RAW_DATA"></span><span id="internet_flag_raw_data"></span>**\_ \_ données brutes de drapeau Internet \_**</span><span class="sxs-lookup"><span data-stu-id="42ccb-229"><span id="INTERNET_FLAG_RAW_DATA"></span><span id="internet_flag_raw_data"></span>**INTERNET\_FLAG\_RAW\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42ccb-230">0x40000000</span><span class="sxs-lookup"><span data-stu-id="42ccb-230">0x40000000</span></span>
</dt> <dt>



<span data-ttu-id="42ccb-231">Retourne les données sous la forme d’une structure de [**\_ \_ données de recherche Win32**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) lors de la récupération des informations de répertoire FTP.</span><span class="sxs-lookup"><span data-stu-id="42ccb-231">Returns the data as a [**WIN32\_FIND\_DATA**](/windows/desktop/api/minwinbase/ns-minwinbase-win32_find_dataa) structure when retrieving FTP directory information.</span></span> <span data-ttu-id="42ccb-232">Si cet indicateur n’est pas spécifié ou si l’appel est effectué via un proxy CERN, [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) retourne la version HTML du répertoire.</span><span class="sxs-lookup"><span data-stu-id="42ccb-232">If this flag is not specified or if the call is made through a CERN proxy, [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) returns the HTML version of the directory.</span></span> <span data-ttu-id="42ccb-233">Seule la fonction [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) utilise cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="42ccb-233">Only the [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) function uses this flag.</span></span>

<span data-ttu-id="42ccb-234">**Windows XP et Windows Server 2003 R2 et versions antérieures :** Retourne également une structure de [**\_ \_ données Gopher Find**](/windows/desktop/api/Wininet/ns-wininet-gopher_find_dataa) lors de la récupération des informations de répertoire Gopher.</span><span class="sxs-lookup"><span data-stu-id="42ccb-234">**Windows XP and Windows Server 2003 R2 and earlier:** Also returns a [**GOPHER\_FIND\_DATA**](/windows/desktop/api/Wininet/ns-wininet-gopher_find_dataa) structure when retrieving Gopher directory information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42ccb-235"><span id="INTERNET_FLAG_READ_PREFETCH"></span><span id="internet_flag_read_prefetch"></span>**\_indicateur Internet \_ lecture \_ prérécupération**</span><span class="sxs-lookup"><span data-stu-id="42ccb-235"><span id="INTERNET_FLAG_READ_PREFETCH"></span><span id="internet_flag_read_prefetch"></span>**INTERNET\_FLAG\_READ\_PREFETCH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42ccb-236">0x00100000</span><span class="sxs-lookup"><span data-stu-id="42ccb-236">0x00100000</span></span>
</dt> <dt>



<span data-ttu-id="42ccb-237">Cet indicateur est actuellement désactivé.</span><span class="sxs-lookup"><span data-stu-id="42ccb-237">This flag is currently disabled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42ccb-238"><span id="INTERNET_FLAG_RELOAD"></span><span id="internet_flag_reload"></span>**\_REchargement des indicateurs Internet \_**</span><span class="sxs-lookup"><span data-stu-id="42ccb-238"><span id="INTERNET_FLAG_RELOAD"></span><span id="internet_flag_reload"></span>**INTERNET\_FLAG\_RELOAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42ccb-239">0x80000000</span><span class="sxs-lookup"><span data-stu-id="42ccb-239">0x80000000</span></span>
</dt> <dt>



<span data-ttu-id="42ccb-240">Force le téléchargement du fichier, de l’objet ou de la liste de répertoires demandés à partir du serveur d’origine, et non à partir du cache.</span><span class="sxs-lookup"><span data-stu-id="42ccb-240">Forces a download of the requested file, object, or directory listing from the origin server, not from the cache.</span></span> <span data-ttu-id="42ccb-241">Les fonctions [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)et [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) utilisent cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="42ccb-241">The [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) functions use this flag.</span></span>

<span data-ttu-id="42ccb-242">**Windows XP et Windows Server 2003 R2 et versions antérieures :** Également utilisé par [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) et [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).</span><span class="sxs-lookup"><span data-stu-id="42ccb-242">**Windows XP and Windows Server 2003 R2 and earlier:** Also used by [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) and [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42ccb-243"><span id="INTERNET_FLAG_RESTRICTED_ZONE"></span><span id="internet_flag_restricted_zone"></span>**\_ \_ zone RESTREINTe \_ Internet**</span><span class="sxs-lookup"><span data-stu-id="42ccb-243"><span id="INTERNET_FLAG_RESTRICTED_ZONE"></span><span id="internet_flag_restricted_zone"></span>**INTERNET\_FLAG\_RESTRICTED\_ZONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42ccb-244">0x00020000</span><span class="sxs-lookup"><span data-stu-id="42ccb-244">0x00020000</span></span>
</dt> <dt>



<span data-ttu-id="42ccb-245">Indique que le cookie en cours de définition est associé à un site non approuvé.</span><span class="sxs-lookup"><span data-stu-id="42ccb-245">Indicates that the cookie being set is associated with an untrusted site.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42ccb-246"><span id="INTERNET_FLAG_RESYNCHRONIZE"></span><span id="internet_flag_resynchronize"></span>**resynchronisation des \_ indicateurs Internet \_**</span><span class="sxs-lookup"><span data-stu-id="42ccb-246"><span id="INTERNET_FLAG_RESYNCHRONIZE"></span><span id="internet_flag_resynchronize"></span>**INTERNET\_FLAG\_RESYNCHRONIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42ccb-247">0x00000800</span><span class="sxs-lookup"><span data-stu-id="42ccb-247">0x00000800</span></span>
</dt> <dt>



<span data-ttu-id="42ccb-248">Recharge les ressources HTTP si la ressource a été modifiée depuis son dernier téléchargement.</span><span class="sxs-lookup"><span data-stu-id="42ccb-248">Reloads HTTP resources if the resource has been modified since the last time it was downloaded.</span></span> <span data-ttu-id="42ccb-249">Toutes les ressources FTP sont rechargées.</span><span class="sxs-lookup"><span data-stu-id="42ccb-249">All FTP resources are reloaded.</span></span> <span data-ttu-id="42ccb-250">Cet indicateur peut être utilisé par [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta)et [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span><span class="sxs-lookup"><span data-stu-id="42ccb-250">This flag can be used by [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea), [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta), and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla).</span></span>

<span data-ttu-id="42ccb-251">**Windows XP et Windows Server 2003 R2 et versions antérieures :** Également utilisé par [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) et [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea), et les ressources Gopher sont rechargées.</span><span class="sxs-lookup"><span data-stu-id="42ccb-251">**Windows XP and Windows Server 2003 R2 and earlier:** Also used by [**GopherFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-gopherfindfirstfilea) and [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea), and Gopher resources are reloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42ccb-252"><span id="INTERNET_FLAG_SECURE"></span><span id="internet_flag_secure"></span>**\_indicateur Internet \_ sécurisé**</span><span class="sxs-lookup"><span data-stu-id="42ccb-252"><span id="INTERNET_FLAG_SECURE"></span><span id="internet_flag_secure"></span>**INTERNET\_FLAG\_SECURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42ccb-253">0x00800000</span><span class="sxs-lookup"><span data-stu-id="42ccb-253">0x00800000</span></span>
</dt> <dt>



<span data-ttu-id="42ccb-254">Utilise la sémantique des transactions sécurisées.</span><span class="sxs-lookup"><span data-stu-id="42ccb-254">Uses secure transaction semantics.</span></span> <span data-ttu-id="42ccb-255">Cela se traduit par l’utilisation de la technologie de communication SSL (Secure Sockets Layer)/privée (SSL/PCT) et n’est significative que pour les requêtes HTTP.</span><span class="sxs-lookup"><span data-stu-id="42ccb-255">This translates to using Secure Sockets Layer/Private Communications Technology (SSL/PCT) and is only meaningful in HTTP requests.</span></span> <span data-ttu-id="42ccb-256">Cet indicateur est utilisé par [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) et [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), mais il est redondant si https://apparaît dans l’URL. La fonction [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) utilise cet indicateur pour les connexions http ; tous les descripteurs de demande créés sous cette connexion héritent de cet indicateur.</span><span class="sxs-lookup"><span data-stu-id="42ccb-256">This flag is used by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) and [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), but this is redundant if https:// appears in the URL.The [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) function uses this flag for HTTP connections; all the request handles created under this connection will inherit this flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42ccb-257"><span id="INTERNET_FLAG_TRANSFER_ASCII"></span><span id="internet_flag_transfer_ascii"></span>**\_transfert de drapeau Internet \_ \_ ASCII**</span><span class="sxs-lookup"><span data-stu-id="42ccb-257"><span id="INTERNET_FLAG_TRANSFER_ASCII"></span><span id="internet_flag_transfer_ascii"></span>**INTERNET\_FLAG\_TRANSFER\_ASCII**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42ccb-258">0x00000001</span><span class="sxs-lookup"><span data-stu-id="42ccb-258">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="42ccb-259">Transfère le fichier au format ASCII (FTP uniquement).</span><span class="sxs-lookup"><span data-stu-id="42ccb-259">Transfers file as ASCII (FTP only).</span></span> <span data-ttu-id="42ccb-260">Cet indicateur peut être utilisé par [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)et [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea).</span><span class="sxs-lookup"><span data-stu-id="42ccb-260">This flag can be used by [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), and [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42ccb-261"><span id="INTERNET_FLAG_TRANSFER_BINARY"></span><span id="internet_flag_transfer_binary"></span>**\_binaire de \_ transfert de drapeau Internet \_**</span><span class="sxs-lookup"><span data-stu-id="42ccb-261"><span id="INTERNET_FLAG_TRANSFER_BINARY"></span><span id="internet_flag_transfer_binary"></span>**INTERNET\_FLAG\_TRANSFER\_BINARY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42ccb-262">0x00000002</span><span class="sxs-lookup"><span data-stu-id="42ccb-262">0x00000002</span></span>
</dt> <dt>



<span data-ttu-id="42ccb-263">Transfère le fichier au format binaire (FTP uniquement).</span><span class="sxs-lookup"><span data-stu-id="42ccb-263">Transfers file as binary (FTP only).</span></span> <span data-ttu-id="42ccb-264">Cet indicateur peut être utilisé par [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea)et [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea).</span><span class="sxs-lookup"><span data-stu-id="42ccb-264">This flag can be used by [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpGetFile**](/windows/desktop/api/Wininet/nf-wininet-ftpgetfilea), and [**FtpPutFile**](/windows/desktop/api/Wininet/nf-wininet-ftpputfilea).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42ccb-265"><span id="INTERNET_NO_CALLBACK"></span><span id="internet_no_callback"></span>**INTERNET \_ sans \_ rappel**</span><span class="sxs-lookup"><span data-stu-id="42ccb-265"><span id="INTERNET_NO_CALLBACK"></span><span id="internet_no_callback"></span>**INTERNET\_NO\_CALLBACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42ccb-266">0x00000000</span><span class="sxs-lookup"><span data-stu-id="42ccb-266">0x00000000</span></span>
</dt> <dt>



<span data-ttu-id="42ccb-267">Indique qu’aucun rappel ne doit être effectué pour cette API.</span><span class="sxs-lookup"><span data-stu-id="42ccb-267">Indicates that no callbacks should be made for that API.</span></span> <span data-ttu-id="42ccb-268">Il est utilisé pour le paramètre *dxContext* des fonctions qui autorisent les opérations asynchrones.</span><span class="sxs-lookup"><span data-stu-id="42ccb-268">This is used for the *dxContext* parameter of the functions that allow asynchronous operations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42ccb-269"><span id="INTERNET_OPTION_SUPPRESS_SERVER_AUTH"></span><span id="internet_option_suppress_server_auth"></span>**\_option Internet \_ supprimer \_ l' \_ authentification du serveur**</span><span class="sxs-lookup"><span data-stu-id="42ccb-269"><span id="INTERNET_OPTION_SUPPRESS_SERVER_AUTH"></span><span id="internet_option_suppress_server_auth"></span>**INTERNET\_OPTION\_SUPPRESS\_SERVER\_AUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42ccb-270">104</span><span class="sxs-lookup"><span data-stu-id="42ccb-270">104</span></span>
</dt> <dt>



<span data-ttu-id="42ccb-271">Définit un objet de requête HTTP de sorte qu’il ne se connecte pas aux serveurs d’origine, mais effectue une ouverture de session automatique sur les serveurs proxy HTTP.</span><span class="sxs-lookup"><span data-stu-id="42ccb-271">Sets an HTTP request object such that it will not logon to origin servers, but will perform automatic logon to HTTP proxy servers.</span></span> <span data-ttu-id="42ccb-272">Cette option diffère de l’indicateur de requête INTERNET \_ Flag \_ no \_ auth, qui empêche l’authentification aux serveurs proxy et aux serveurs d’origine.</span><span class="sxs-lookup"><span data-stu-id="42ccb-272">This option differs from the Request flag INTERNET\_FLAG\_NO\_AUTH, which prevents authentication to both proxy servers and origin servers.</span></span> <span data-ttu-id="42ccb-273">En définissant ce mode, vous supprimez l’utilisation de tout document d’informations d’identification (nom d’utilisateur/mot de passe ou certificat SSL client précédemment fourni) lors de la communication avec un serveur d’origine.</span><span class="sxs-lookup"><span data-stu-id="42ccb-273">Setting this mode will suppress the use of any credential material (either previously provided username/password or client SSL certificate) when communicating with an origin server.</span></span> <span data-ttu-id="42ccb-274">Toutefois, si la demande doit transiter via un proxy d’authentification, WinINet effectue toujours l’authentification automatique sur le proxy HTTP en fonction des paramètres de la zone Intranet de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="42ccb-274">However, if the request must transit via an authenticating proxy, WinINet will still perform automatic authentication to the HTTP proxy per the Intranet Zone settings for the user.</span></span> <span data-ttu-id="42ccb-275">Le paramètre de zone Intranet par défaut permet d’autoriser l’ouverture de session automatique à l’aide des informations d’identification par défaut de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="42ccb-275">The default Intranet Zone setting is to permit automatic logon using the user s default credentials.</span></span> <span data-ttu-id="42ccb-276">Pour garantir la suppression de toutes les informations d’identification, l’appelant doit combiner l' \_ option Internet option \_ supprimer \_ \_ l’authentification du serveur avec l' \_ indicateur de requête Internet indicateur \_ aucun \_ cookie.</span><span class="sxs-lookup"><span data-stu-id="42ccb-276">To ensure suppression of all identifying information, the caller should combine INTERNET\_OPTION\_SUPPRESS\_SERVER\_AUTH with the INTERNET\_FLAG\_NO\_COOKIES request flag.</span></span> <span data-ttu-id="42ccb-277">Cette option ne peut être définie que sur des objets de requête avant d’être envoyés.</span><span class="sxs-lookup"><span data-stu-id="42ccb-277">This option may only be set on request objects before they have been sent.</span></span> <span data-ttu-id="42ccb-278">Toute tentative de définition de cette option après l’envoi de la demande retourne l’état d’erreur du \_ \_ handle Internet incorrect \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="42ccb-278">Attempts to set this option after the request has been sent will return ERROR\_INTERNET\_INCORRECT\_HANDLE\_STATE.</span></span> <span data-ttu-id="42ccb-279">Aucune mémoire tampon n’est requise pour cette option.</span><span class="sxs-lookup"><span data-stu-id="42ccb-279">No buffer is required for this option.</span></span> <span data-ttu-id="42ccb-280">Cela est utilisé par InternetSetOption sur les handles retournés par HttpOpenRequest uniquement.</span><span class="sxs-lookup"><span data-stu-id="42ccb-280">This is used by InternetSetOption on handles returned by HttpOpenRequest only.</span></span> <span data-ttu-id="42ccb-281">Version : nécessite Internet Explorer 8,0 ou version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="42ccb-281">Version: Requires Internet Explorer 8.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42ccb-282"><span id="WININET_API_FLAG_ASYNC"></span><span id="wininet_api_flag_async"></span>**\_indicateur d’API WinInet \_ \_ Async**</span><span class="sxs-lookup"><span data-stu-id="42ccb-282"><span id="WININET_API_FLAG_ASYNC"></span><span id="wininet_api_flag_async"></span>**WININET\_API\_FLAG\_ASYNC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42ccb-283">0x00000001</span><span class="sxs-lookup"><span data-stu-id="42ccb-283">0x00000001</span></span>
</dt> <dt>



<span data-ttu-id="42ccb-284">Force les opérations asynchrones.</span><span class="sxs-lookup"><span data-stu-id="42ccb-284">Forces asynchronous operations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42ccb-285"><span id="WININET_API_FLAG_SYNC"></span><span id="wininet_api_flag_sync"></span>**synchronisation des indicateurs de l' \_ API WinInet \_ \_**</span><span class="sxs-lookup"><span data-stu-id="42ccb-285"><span id="WININET_API_FLAG_SYNC"></span><span id="wininet_api_flag_sync"></span>**WININET\_API\_FLAG\_SYNC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42ccb-286">0x00000004</span><span class="sxs-lookup"><span data-stu-id="42ccb-286">0x00000004</span></span>
</dt> <dt>



<span data-ttu-id="42ccb-287">Force les opérations synchrones.</span><span class="sxs-lookup"><span data-stu-id="42ccb-287">Forces synchronous operations.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="42ccb-288"><span id="WININET_API_FLAG_USE_CONTEXT"></span><span id="wininet_api_flag_use_context"></span>**contexte d’utilisation de l' \_ indicateur d’API WinInet \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="42ccb-288"><span id="WININET_API_FLAG_USE_CONTEXT"></span><span id="wininet_api_flag_use_context"></span>**WININET\_API\_FLAG\_USE\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="42ccb-289">0x00000008</span><span class="sxs-lookup"><span data-stu-id="42ccb-289">0x00000008</span></span>
</dt> <dt>



<span data-ttu-id="42ccb-290">Force l’API à utiliser la valeur de contexte, même si elle est définie sur zéro.</span><span class="sxs-lookup"><span data-stu-id="42ccb-290">Forces the API to use the context value, even if it is set to zero.</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="42ccb-291">Notes</span><span class="sxs-lookup"><span data-stu-id="42ccb-291">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="42ccb-292">WinINet ne prend pas en charge les implémentations de serveur.</span><span class="sxs-lookup"><span data-stu-id="42ccb-292">WinINet does not support server implementations.</span></span> <span data-ttu-id="42ccb-293">En outre, il ne doit pas être utilisé à partir d’un service.</span><span class="sxs-lookup"><span data-stu-id="42ccb-293">In addition, it should not be used from a service.</span></span> <span data-ttu-id="42ccb-294">Pour les implémentations de serveur ou les services, utilisez les [services http Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="42ccb-294">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="42ccb-295">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="42ccb-295">Requirements</span></span>



| <span data-ttu-id="42ccb-296">Condition requise</span><span class="sxs-lookup"><span data-stu-id="42ccb-296">Requirement</span></span> | <span data-ttu-id="42ccb-297">Valeur</span><span class="sxs-lookup"><span data-stu-id="42ccb-297">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="42ccb-298">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="42ccb-298">Minimum supported client</span></span><br/> | <span data-ttu-id="42ccb-299">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="42ccb-299">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="42ccb-300">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="42ccb-300">Minimum supported server</span></span><br/> | <span data-ttu-id="42ccb-301">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="42ccb-301">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="42ccb-302">En-tête</span><span class="sxs-lookup"><span data-stu-id="42ccb-302">Header</span></span><br/>                   | <dl> <span data-ttu-id="42ccb-303"><dt>Wininet. h</dt></span><span class="sxs-lookup"><span data-stu-id="42ccb-303"><dt>Wininet.h</dt></span></span> </dl> |



 

