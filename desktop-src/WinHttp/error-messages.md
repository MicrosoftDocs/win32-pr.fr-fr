---
description: Les valeurs d’erreur identifiées dans cette rubrique sont retournées par GetLastError en cas d’échec de l’une des fonctions des services HTTP Microsoft Windows (WinHTTP).
ms.assetid: c8a863cd-d36c-4ec8-ac49-0b714a5e4cc2
title: Messages d’erreur (WinHTTP. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eccdc8be4b1e7c3cc7f9a03403c2f8778ddd19b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866233"
---
# <a name="error-messages-winhttph"></a><span data-ttu-id="b601e-103">Messages d’erreur (WinHTTP. h)</span><span class="sxs-lookup"><span data-stu-id="b601e-103">Error Messages (Winhttp.h)</span></span>

<span data-ttu-id="b601e-104">Les valeurs d’erreur répertoriées ci-dessous sont retournées par [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) lorsque l’une des fonctions des services http Microsoft Windows (WinHTTP) échoue, et elles sont également retournées dans les 16 bits d’erreur de [**HRESULT**](../com/structure-of-com-error-codes.md) inférieurs renvoyés par l’objet [**WinHttpRequest**](winhttprequest.md) .</span><span class="sxs-lookup"><span data-stu-id="b601e-104">The error values listed below are returned by [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) when one of the Microsoft Windows HTTP Services (WinHTTP) functions fails, and are also returned in the lower 16 bits of [**HRESULT**](../com/structure-of-com-error-codes.md) error returns from the [**WinHttpRequest**](winhttprequest.md) object.</span></span>

<span data-ttu-id="b601e-105">Les valeurs d’erreur dont les noms commencent par « erreur \_ WinHTTP \_ » sont spécifiques aux fonctions WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="b601e-105">Error values whose names begin with "ERROR\_WINHTTP\_" are specific to the WinHTTP functions.</span></span> <span data-ttu-id="b601e-106">Les fonctions WinHTTP retournent également des messages d’erreur Windows, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="b601e-106">The WinHTTP functions also return Windows error messages where appropriate.</span></span>

<dl> <dt>

<span data-ttu-id="b601e-107"><span id="ERROR_WINHTTP_AUTO_PROXY_SERVICE_ERROR"></span><span id="error_winhttp_auto_proxy_service_error"></span>**ERREUR \_ de \_ \_ service de proxy automatique \_ WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="b601e-107"><span id="ERROR_WINHTTP_AUTO_PROXY_SERVICE_ERROR"></span><span id="error_winhttp_auto_proxy_service_error"></span>**ERROR\_WINHTTP\_AUTO\_PROXY\_SERVICE\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b601e-108">12178</span><span class="sxs-lookup"><span data-stu-id="b601e-108">12178</span></span>
</dt> <dt>



<span data-ttu-id="b601e-109">Retourné par [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) lorsqu’un proxy pour l’URL spécifiée est introuvable.</span><span class="sxs-lookup"><span data-stu-id="b601e-109">Returned by [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) when a proxy for the specified URL cannot be located.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b601e-110"><span id="ERROR_WINHTTP_AUTODETECTION_FAILED"></span><span id="error_winhttp_autodetection_failed"></span>**ERREUR lors de la \_ détection automatique WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b601e-110"><span id="ERROR_WINHTTP_AUTODETECTION_FAILED"></span><span id="error_winhttp_autodetection_failed"></span>**ERROR\_WINHTTP\_AUTODETECTION\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b601e-111">12180</span><span class="sxs-lookup"><span data-stu-id="b601e-111">12180</span></span>
</dt> <dt>



<span data-ttu-id="b601e-112">Retourné par [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) si WinHTTP n’a pas pu découvrir l’URL du fichier de configuration automatique de proxy (PAC).</span><span class="sxs-lookup"><span data-stu-id="b601e-112">Returned by [**WinHttpDetectAutoProxyConfigUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpdetectautoproxyconfigurl) if WinHTTP was unable to discover the URL of the Proxy Auto-Configuration (PAC) file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b601e-113"><span id="ERROR_WINHTTP_BAD_AUTO_PROXY_SCRIPT"></span><span id="error_winhttp_bad_auto_proxy_script"></span>**ERREUR \_ WinHTTP \_ \_ script de \_ proxy \_ automatique incorrect**</span><span class="sxs-lookup"><span data-stu-id="b601e-113"><span id="ERROR_WINHTTP_BAD_AUTO_PROXY_SCRIPT"></span><span id="error_winhttp_bad_auto_proxy_script"></span>**ERROR\_WINHTTP\_BAD\_AUTO\_PROXY\_SCRIPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b601e-114">12166</span><span class="sxs-lookup"><span data-stu-id="b601e-114">12166</span></span>
</dt> <dt>



<span data-ttu-id="b601e-115">Une erreur s’est produite lors de l’exécution du code de script dans le fichier de configuration automatique de proxy (PAC).</span><span class="sxs-lookup"><span data-stu-id="b601e-115">An error occurred executing the script code in the Proxy Auto-Configuration (PAC) file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b601e-116"><span id="ERROR_WINHTTP_CANNOT_CALL_AFTER_OPEN"></span><span id="error_winhttp_cannot_call_after_open"></span>**ERREUR \_ WinHTTP \_ ne peut pas \_ appeler \_ après l' \_ ouverture**</span><span class="sxs-lookup"><span data-stu-id="b601e-116"><span id="ERROR_WINHTTP_CANNOT_CALL_AFTER_OPEN"></span><span id="error_winhttp_cannot_call_after_open"></span>**ERROR\_WINHTTP\_CANNOT\_CALL\_AFTER\_OPEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b601e-117">12103</span><span class="sxs-lookup"><span data-stu-id="b601e-117">12103</span></span>
</dt> <dt>



<span data-ttu-id="b601e-118">Retourné par l’objet [**HttpRequest**](winhttprequest.md) si une option spécifiée ne peut pas être demandée après l’appel de la méthode [**Open**](iwinhttprequest-open.md) .</span><span class="sxs-lookup"><span data-stu-id="b601e-118">Returned by the [**HttpRequest**](winhttprequest.md) object if a specified option cannot be requested after the [**Open**](iwinhttprequest-open.md) method has been called.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b601e-119"><span id="ERROR_WINHTTP_CANNOT_CALL_AFTER_SEND"></span><span id="error_winhttp_cannot_call_after_send"></span>**ERREUR \_ WinHTTP \_ ne peut pas \_ appeler \_ après l' \_ envoi**</span><span class="sxs-lookup"><span data-stu-id="b601e-119"><span id="ERROR_WINHTTP_CANNOT_CALL_AFTER_SEND"></span><span id="error_winhttp_cannot_call_after_send"></span>**ERROR\_WINHTTP\_CANNOT\_CALL\_AFTER\_SEND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b601e-120">12102</span><span class="sxs-lookup"><span data-stu-id="b601e-120">12102</span></span>
</dt> <dt>



<span data-ttu-id="b601e-121">Retourné par l’objet [**HttpRequest**](winhttprequest.md) si une opération demandée ne peut pas être effectuée après l’appel de la méthode [**Send**](iwinhttprequest-send.md) .</span><span class="sxs-lookup"><span data-stu-id="b601e-121">Returned by the [**HttpRequest**](winhttprequest.md) object if a requested operation cannot be performed after calling the [**Send**](iwinhttprequest-send.md) method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b601e-122"><span id="ERROR_WINHTTP_CANNOT_CALL_BEFORE_OPEN"></span><span id="error_winhttp_cannot_call_before_open"></span>**ERREUR \_ WinHTTP \_ ne peut pas \_ appeler \_ avant l' \_ ouverture**</span><span class="sxs-lookup"><span data-stu-id="b601e-122"><span id="ERROR_WINHTTP_CANNOT_CALL_BEFORE_OPEN"></span><span id="error_winhttp_cannot_call_before_open"></span>**ERROR\_WINHTTP\_CANNOT\_CALL\_BEFORE\_OPEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b601e-123">12100</span><span class="sxs-lookup"><span data-stu-id="b601e-123">12100</span></span>
</dt> <dt>



<span data-ttu-id="b601e-124">Retourné par l’objet [**HttpRequest**](winhttprequest.md) si une opération demandée ne peut pas être exécutée avant d’appeler la méthode [**Open**](iwinhttprequest-open.md) .</span><span class="sxs-lookup"><span data-stu-id="b601e-124">Returned by the [**HttpRequest**](winhttprequest.md) object if a requested operation cannot be performed before calling the [**Open**](iwinhttprequest-open.md) method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b601e-125"><span id="ERROR_WINHTTP_CANNOT_CALL_BEFORE_SEND"></span><span id="error_winhttp_cannot_call_before_send"></span>**ERREUR \_ WinHTTP \_ ne peut pas \_ appeler \_ avant \_ Send**</span><span class="sxs-lookup"><span data-stu-id="b601e-125"><span id="ERROR_WINHTTP_CANNOT_CALL_BEFORE_SEND"></span><span id="error_winhttp_cannot_call_before_send"></span>**ERROR\_WINHTTP\_CANNOT\_CALL\_BEFORE\_SEND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b601e-126">12101</span><span class="sxs-lookup"><span data-stu-id="b601e-126">12101</span></span>
</dt> <dt>



<span data-ttu-id="b601e-127">Retourné par l’objet [**HttpRequest**](winhttprequest.md) si une opération demandée ne peut pas être exécutée avant d’appeler la méthode [**Send**](iwinhttprequest-send.md) .</span><span class="sxs-lookup"><span data-stu-id="b601e-127">Returned by the [**HttpRequest**](winhttprequest.md) object if a requested operation cannot be performed before calling the [**Send**](iwinhttprequest-send.md) method.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b601e-128"><span id="ERROR_WINHTTP_CANNOT_CONNECT"></span><span id="error_winhttp_cannot_connect"></span>**ERREUR \_ WinHTTP \_ ne peut pas \_ se connecter**</span><span class="sxs-lookup"><span data-stu-id="b601e-128"><span id="ERROR_WINHTTP_CANNOT_CONNECT"></span><span id="error_winhttp_cannot_connect"></span>**ERROR\_WINHTTP\_CANNOT\_CONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b601e-129">12029</span><span class="sxs-lookup"><span data-stu-id="b601e-129">12029</span></span>
</dt> <dt>



<span data-ttu-id="b601e-130">Retourné si la connexion au serveur a échoué.</span><span class="sxs-lookup"><span data-stu-id="b601e-130">Returned if connection to the server failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b601e-131"><span id="ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_winhttp_client_auth_cert_needed"></span>**ERREUR \_ du \_ certificat d’authentification du client WinHTTP \_ \_ \_ nécessaire**</span><span class="sxs-lookup"><span data-stu-id="b601e-131"><span id="ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_winhttp_client_auth_cert_needed"></span>**ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b601e-132">Le serveur requiert l’authentification du client SSL.</span><span class="sxs-lookup"><span data-stu-id="b601e-132">The server requires SSL client Authentication.</span></span> <span data-ttu-id="b601e-133">L’application récupère la liste des émetteurs de certificats en appelant [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) à l’aide de l’option **WinHTTP \_ \_ \_ \_ \_ liste d’émetteurs** de certificats client.</span><span class="sxs-lookup"><span data-stu-id="b601e-133">The application retrieves the list of certificate issuers by calling [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) with the **WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST** option.</span></span> <span data-ttu-id="b601e-134">Pour plus d’informations, consultez l’option **WinHTTP \_ \_ liste d' \_ \_ émetteurs \_ de certificats client** .</span><span class="sxs-lookup"><span data-stu-id="b601e-134">For more information, see the **WINHTTP\_OPTION\_CLIENT\_CERT\_ISSUER\_LIST** option.</span></span>

<span data-ttu-id="b601e-135">Si le serveur demande le certificat client, mais ne l’exige pas, l’application peut également appeler [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) avec l’option **WinHTTP \_ \_ \_ \_ contexte CERT client** .</span><span class="sxs-lookup"><span data-stu-id="b601e-135">If the server requests the client certificate, but does not require it, the application can alternately call [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) with the **WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT** option.</span></span> <span data-ttu-id="b601e-136">Dans ce cas, l’application spécifie la \_ \_ macro de contexte de certificat non client WinHTTP \_ \_ dans le paramètre *lpBuffer* de **WinHttpSetOption**.</span><span class="sxs-lookup"><span data-stu-id="b601e-136">In this case, the application specifies the WINHTTP\_NO\_CLIENT\_CERT\_CONTEXT macro in the *lpBuffer* parameter of **WinHttpSetOption**.</span></span> <span data-ttu-id="b601e-137">Pour plus d’informations, consultez l’option de **\_ \_ \_ \_ contexte certificat du client de l’option WinHTTP** .</span><span class="sxs-lookup"><span data-stu-id="b601e-137">For more information, see the **WINHTTP\_OPTION\_CLIENT\_CERT\_CONTEXT** option.</span></span>

<span data-ttu-id="b601e-138">**Windows Server 2003 avec SP1 et Windows XP avec SP2 :** Cette erreur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="b601e-138">**Windows Server 2003 with SP1 and Windows XP with SP2:** This error is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b601e-139"><span id="ERROR_WINHTTP_CLIENT_CERT_NO_ACCESS_PRIVATE_KEY"></span><span id="error_winhttp_client_cert_no_access_private_key"></span>**ERREUR \_ de \_ certificat client WinHTTP \_ \_ aucune \_ \_ clé privée d’accès \_**</span><span class="sxs-lookup"><span data-stu-id="b601e-139"><span id="ERROR_WINHTTP_CLIENT_CERT_NO_ACCESS_PRIVATE_KEY"></span><span id="error_winhttp_client_cert_no_access_private_key"></span>**ERROR\_WINHTTP\_CLIENT\_CERT\_NO\_ACCESS\_PRIVATE\_KEY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b601e-140">L’application ne dispose pas des privilèges nécessaires pour accéder à la clé privée associée au certificat client.</span><span class="sxs-lookup"><span data-stu-id="b601e-140">The application does not have the required privileges to access the private key associated with the client certificate.</span></span>

<span data-ttu-id="b601e-141">**Windows Server 2003 avec SP1 et Windows XP avec SP2 :** Cette erreur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="b601e-141">**Windows Server 2003 with SP1 and Windows XP with SP2:** This error is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b601e-142"><span id="ERROR_WINHTTP_CLIENT_CERT_NO_PRIVATE_KEY"></span><span id="error_winhttp_client_cert_no_private_key"></span>**ERREUR \_ de \_ certificat client WinHTTP \_ \_ sans \_ \_ clé privée**</span><span class="sxs-lookup"><span data-stu-id="b601e-142"><span id="ERROR_WINHTTP_CLIENT_CERT_NO_PRIVATE_KEY"></span><span id="error_winhttp_client_cert_no_private_key"></span>**ERROR\_WINHTTP\_CLIENT\_CERT\_NO\_PRIVATE\_KEY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b601e-143">Aucune clé privée n’est associée au contexte du certificat client SSL.</span><span class="sxs-lookup"><span data-stu-id="b601e-143">The context for the SSL client certificate does not have a private key associated with it.</span></span> <span data-ttu-id="b601e-144">Le certificat client a peut-être été importé sur l’ordinateur sans la clé privée.</span><span class="sxs-lookup"><span data-stu-id="b601e-144">The client certificate may have been imported to the computer without the private key.</span></span>

<span data-ttu-id="b601e-145">**Windows Server 2003 avec SP1 et Windows XP avec SP2 :** Cette erreur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="b601e-145">**Windows Server 2003 with SP1 and Windows XP with SP2:** This error is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b601e-146"><span id="ERROR_WINHTTP_CHUNKED_ENCODING_HEADER_SIZE_OVERFLOW"></span><span id="error_winhttp_chunked_encoding_header_size_overflow"></span>**ERREUR \_ WinHTTP \_ dépassement de \_ \_ taille d’en-tête de codage mémorisé en bloc \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b601e-146"><span id="ERROR_WINHTTP_CHUNKED_ENCODING_HEADER_SIZE_OVERFLOW"></span><span id="error_winhttp_chunked_encoding_header_size_overflow"></span>**ERROR\_WINHTTP\_CHUNKED\_ENCODING\_HEADER\_SIZE\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b601e-147">12183</span><span class="sxs-lookup"><span data-stu-id="b601e-147">12183</span></span>
</dt> <dt>



<span data-ttu-id="b601e-148">Retourné par [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) lorsqu’une condition de dépassement de capacité se produit au cours de l’analyse du codage mémorisé en bloc.</span><span class="sxs-lookup"><span data-stu-id="b601e-148">Returned by [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) when an overflow condition is encountered in the course of parsing chunked encoding.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b601e-149"><span id="ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_winhttp_client_auth_cert_needed"></span>**ERREUR \_ du \_ certificat d’authentification du client WinHTTP \_ \_ \_ nécessaire**</span><span class="sxs-lookup"><span data-stu-id="b601e-149"><span id="ERROR_WINHTTP_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_winhttp_client_auth_cert_needed"></span>**ERROR\_WINHTTP\_CLIENT\_AUTH\_CERT\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b601e-150">12044</span><span class="sxs-lookup"><span data-stu-id="b601e-150">12044</span></span>
</dt> <dt>



<span data-ttu-id="b601e-151">Retourné par [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) lorsque le serveur demande l’authentification du client.</span><span class="sxs-lookup"><span data-stu-id="b601e-151">Returned by [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) when the server requests client authentication.</span></span>

<span data-ttu-id="b601e-152">**Windows Server 2003 avec SP1 et Windows XP avec SP2 :** Cette erreur n’est pas prise en charge.</span><span class="sxs-lookup"><span data-stu-id="b601e-152">**Windows Server 2003 with SP1 and Windows XP with SP2:** This error is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b601e-153"><span id="ERROR_WINHTTP_CONNECTION_ERROR"></span><span id="error_winhttp_connection_error"></span>**ERREUR \_ de \_ connexion \_ WinHTTP erreur**</span><span class="sxs-lookup"><span data-stu-id="b601e-153"><span id="ERROR_WINHTTP_CONNECTION_ERROR"></span><span id="error_winhttp_connection_error"></span>**ERROR\_WINHTTP\_CONNECTION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b601e-154">12030</span><span class="sxs-lookup"><span data-stu-id="b601e-154">12030</span></span>
</dt> <dt>



<span data-ttu-id="b601e-155">La connexion avec le serveur a été réinitialisée ou terminée, ou un protocole SSL incompatible a été rencontré.</span><span class="sxs-lookup"><span data-stu-id="b601e-155">The connection with the server has been reset or terminated, or an incompatible SSL protocol was encountered.</span></span> <span data-ttu-id="b601e-156">Par exemple, WinHTTP version 5,1 ne prend pas en charge SSL2, sauf si le client l’active spécifiquement.</span><span class="sxs-lookup"><span data-stu-id="b601e-156">For example, WinHTTP version 5.1 does not support SSL2 unless the client specifically enables it.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b601e-157"><span id="ERROR_WINHTTP_HEADER_ALREADY_EXISTS"></span><span id="error_winhttp_header_already_exists"></span>**l' \_ \_ en-tête WinHTTP d’erreur \_ \_ existe déjà**</span><span class="sxs-lookup"><span data-stu-id="b601e-157"><span id="ERROR_WINHTTP_HEADER_ALREADY_EXISTS"></span><span id="error_winhttp_header_already_exists"></span>**ERROR\_WINHTTP\_HEADER\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b601e-158">12155</span><span class="sxs-lookup"><span data-stu-id="b601e-158">12155</span></span>
</dt> <dt>



<span data-ttu-id="b601e-159">Périmé n’est plus utilisé.</span><span class="sxs-lookup"><span data-stu-id="b601e-159">Obsolete; no longer used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b601e-160"><span id="ERROR_WINHTTP_HEADER_COUNT_EXCEEDED"></span><span id="error_winhttp_header_count_exceeded"></span>**ERREUR \_ du \_ nombre d’en-têtes WinHTTP \_ \_ dépassé**</span><span class="sxs-lookup"><span data-stu-id="b601e-160"><span id="ERROR_WINHTTP_HEADER_COUNT_EXCEEDED"></span><span id="error_winhttp_header_count_exceeded"></span>**ERROR\_WINHTTP\_HEADER\_COUNT\_EXCEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b601e-161">12181</span><span class="sxs-lookup"><span data-stu-id="b601e-161">12181</span></span>
</dt> <dt>



<span data-ttu-id="b601e-162">Retourné par [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) lorsqu’un plus grand nombre d’en-têtes étaient présents dans une réponse que WinHTTP pouvait recevoir.</span><span class="sxs-lookup"><span data-stu-id="b601e-162">Returned by [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) when a larger number of headers were present in a response than WinHTTP could receive.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b601e-163"><span id="ERROR_WINHTTP_HEADER_NOT_FOUND"></span><span id="error_winhttp_header_not_found"></span>**ERREUR de l' \_ \_ en-tête WinHTTP \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="b601e-163"><span id="ERROR_WINHTTP_HEADER_NOT_FOUND"></span><span id="error_winhttp_header_not_found"></span>**ERROR\_WINHTTP\_HEADER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b601e-164">12150</span><span class="sxs-lookup"><span data-stu-id="b601e-164">12150</span></span>
</dt> <dt>



<span data-ttu-id="b601e-165">L’en-tête demandé est introuvable.</span><span class="sxs-lookup"><span data-stu-id="b601e-165">The requested header cannot be located.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b601e-166"><span id="ERROR_WINHTTP_HEADER_SIZE_OVERFLOW"></span><span id="error_winhttp_header_size_overflow"></span>**ERREUR \_ de \_ \_ dépassement de taille d’en-tête WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="b601e-166"><span id="ERROR_WINHTTP_HEADER_SIZE_OVERFLOW"></span><span id="error_winhttp_header_size_overflow"></span>**ERROR\_WINHTTP\_HEADER\_SIZE\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b601e-167">12182</span><span class="sxs-lookup"><span data-stu-id="b601e-167">12182</span></span>
</dt> <dt>



<span data-ttu-id="b601e-168">Retourné par [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) lorsque la taille des en-têtes reçus dépasse la limite du handle de demande.</span><span class="sxs-lookup"><span data-stu-id="b601e-168">Returned by [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) when the size of headers received exceeds the limit for the request handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b601e-169"><span id="ERROR_WINHTTP_INCORRECT_HANDLE_STATE"></span><span id="error_winhttp_incorrect_handle_state"></span>**ERREUR \_ WinHTTP \_ \_ État de handle incorrect \_**</span><span class="sxs-lookup"><span data-stu-id="b601e-169"><span id="ERROR_WINHTTP_INCORRECT_HANDLE_STATE"></span><span id="error_winhttp_incorrect_handle_state"></span>**ERROR\_WINHTTP\_INCORRECT\_HANDLE\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b601e-170">12019</span><span class="sxs-lookup"><span data-stu-id="b601e-170">12019</span></span>
</dt> <dt>



<span data-ttu-id="b601e-171">Impossible d’effectuer l’opération demandée, car le handle fourni n’est pas dans l’état correct.</span><span class="sxs-lookup"><span data-stu-id="b601e-171">The requested operation cannot be carried out because the handle supplied is not in the correct state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b601e-172"><span id="ERROR_WINHTTP_INCORRECT_HANDLE_TYPE"></span><span id="error_winhttp_incorrect_handle_type"></span>**ERREUR \_ WinHTTP \_ \_ type de handle incorrect \_**</span><span class="sxs-lookup"><span data-stu-id="b601e-172"><span id="ERROR_WINHTTP_INCORRECT_HANDLE_TYPE"></span><span id="error_winhttp_incorrect_handle_type"></span>**ERROR\_WINHTTP\_INCORRECT\_HANDLE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b601e-173">12018</span><span class="sxs-lookup"><span data-stu-id="b601e-173">12018</span></span>
</dt> <dt>



<span data-ttu-id="b601e-174">Le type de handle fourni est incorrect pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="b601e-174">The type of handle supplied is incorrect for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b601e-175"><span id="ERROR_WINHTTP_INTERNAL_ERROR"></span><span id="error_winhttp_internal_error"></span>**ERREUR \_ WinHTTP \_ interne \_ erreur**</span><span class="sxs-lookup"><span data-stu-id="b601e-175"><span id="ERROR_WINHTTP_INTERNAL_ERROR"></span><span id="error_winhttp_internal_error"></span>**ERROR\_WINHTTP\_INTERNAL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b601e-176">12004</span><span class="sxs-lookup"><span data-stu-id="b601e-176">12004</span></span>
</dt> <dt>



<span data-ttu-id="b601e-177">Une erreur interne s'est produite.</span><span class="sxs-lookup"><span data-stu-id="b601e-177">An internal error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b601e-178"><span id="ERROR_WINHTTP_INVALID_OPTION"></span><span id="error_winhttp_invalid_option"></span>**ERREUR \_ WinHTTP \_ non valide, \_ option**</span><span class="sxs-lookup"><span data-stu-id="b601e-178"><span id="ERROR_WINHTTP_INVALID_OPTION"></span><span id="error_winhttp_invalid_option"></span>**ERROR\_WINHTTP\_INVALID\_OPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b601e-179">12009</span><span class="sxs-lookup"><span data-stu-id="b601e-179">12009</span></span>
</dt> <dt>



<span data-ttu-id="b601e-180">Une requête à [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) ou [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) A spécifié une valeur d’option non valide.</span><span class="sxs-lookup"><span data-stu-id="b601e-180">A request to [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) or [**WinHttpSetOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsetoption) specified an invalid option value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b601e-181"><span id="ERROR_WINHTTP_INVALID_QUERY_REQUEST"></span><span id="error_winhttp_invalid_query_request"></span>**ERREUR \_ WinHTTP requête de \_ requête non valide \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b601e-181"><span id="ERROR_WINHTTP_INVALID_QUERY_REQUEST"></span><span id="error_winhttp_invalid_query_request"></span>**ERROR\_WINHTTP\_INVALID\_QUERY\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b601e-182">12154</span><span class="sxs-lookup"><span data-stu-id="b601e-182">12154</span></span>
</dt> <dt>



<span data-ttu-id="b601e-183">Périmé n’est plus utilisé.</span><span class="sxs-lookup"><span data-stu-id="b601e-183">Obsolete; no longer used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b601e-184"><span id="ERROR_WINHTTP_INVALID_SERVER_RESPONSE"></span><span id="error_winhttp_invalid_server_response"></span>**ERREUR \_ WinHTTP \_ \_ réponse du serveur non valide \_**</span><span class="sxs-lookup"><span data-stu-id="b601e-184"><span id="ERROR_WINHTTP_INVALID_SERVER_RESPONSE"></span><span id="error_winhttp_invalid_server_response"></span>**ERROR\_WINHTTP\_INVALID\_SERVER\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b601e-185">12152</span><span class="sxs-lookup"><span data-stu-id="b601e-185">12152</span></span>
</dt> <dt>



<span data-ttu-id="b601e-186">La réponse du serveur ne peut pas être analysée.</span><span class="sxs-lookup"><span data-stu-id="b601e-186">The server response cannot be parsed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b601e-187"><span id="ERROR_WINHTTP_INVALID_URL"></span><span id="error_winhttp_invalid_url"></span>**ERREUR \_ WinHTTP \_ URL non valide \_**</span><span class="sxs-lookup"><span data-stu-id="b601e-187"><span id="ERROR_WINHTTP_INVALID_URL"></span><span id="error_winhttp_invalid_url"></span>**ERROR\_WINHTTP\_INVALID\_URL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b601e-188">12005</span><span class="sxs-lookup"><span data-stu-id="b601e-188">12005</span></span>
</dt> <dt>



<span data-ttu-id="b601e-189">L’URL n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="b601e-189">The URL is not valid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b601e-190"><span id="ERROR_WINHTTP_LOGIN_FAILURE"></span><span id="error_winhttp_login_failure"></span>**ERREUR \_ d' \_ échec de connexion WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="b601e-190"><span id="ERROR_WINHTTP_LOGIN_FAILURE"></span><span id="error_winhttp_login_failure"></span>**ERROR\_WINHTTP\_LOGIN\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b601e-191">12015</span><span class="sxs-lookup"><span data-stu-id="b601e-191">12015</span></span>
</dt> <dt>



<span data-ttu-id="b601e-192">La tentative de connexion a échoué.</span><span class="sxs-lookup"><span data-stu-id="b601e-192">The login attempt failed.</span></span> <span data-ttu-id="b601e-193">Lorsque cette erreur se produit, le descripteur de demande doit être fermé avec [**WinHttpCloseHandle**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle).</span><span class="sxs-lookup"><span data-stu-id="b601e-193">When this error is encountered, the request handle should be closed with [**WinHttpCloseHandle**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpclosehandle).</span></span> <span data-ttu-id="b601e-194">Un nouveau descripteur de demande doit être créé avant de retenter la fonction qui a produit cette erreur à l’origine.</span><span class="sxs-lookup"><span data-stu-id="b601e-194">A new request handle must be created before retrying the function that originally produced this error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b601e-195"><span id="ERROR_WINHTTP_NAME_NOT_RESOLVED"></span><span id="error_winhttp_name_not_resolved"></span>**ERREUR \_ de \_ nom WinHTTP \_ non \_ résolue**</span><span class="sxs-lookup"><span data-stu-id="b601e-195"><span id="ERROR_WINHTTP_NAME_NOT_RESOLVED"></span><span id="error_winhttp_name_not_resolved"></span>**ERROR\_WINHTTP\_NAME\_NOT\_RESOLVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b601e-196">12007</span><span class="sxs-lookup"><span data-stu-id="b601e-196">12007</span></span>
</dt> <dt>



<span data-ttu-id="b601e-197">Impossible de résoudre le nom du serveur.</span><span class="sxs-lookup"><span data-stu-id="b601e-197">The server name cannot be resolved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b601e-198"><span id="ERROR_WINHTTP_NOT_INITIALIZED"></span><span id="error_winhttp_not_initialized"></span>**ERREUR \_ WinHTTP \_ non \_ initialisée**</span><span class="sxs-lookup"><span data-stu-id="b601e-198"><span id="ERROR_WINHTTP_NOT_INITIALIZED"></span><span id="error_winhttp_not_initialized"></span>**ERROR\_WINHTTP\_NOT\_INITIALIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b601e-199">12172</span><span class="sxs-lookup"><span data-stu-id="b601e-199">12172</span></span>
</dt> <dt>



<span data-ttu-id="b601e-200">Périmé n’est plus utilisé.</span><span class="sxs-lookup"><span data-stu-id="b601e-200">Obsolete; no longer used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b601e-201"><span id="ERROR_WINHTTP_OPERATION_CANCELLED"></span><span id="error_winhttp_operation_cancelled"></span>**ERREUR de l' \_ \_ opération WinHTTP \_ annulée**</span><span class="sxs-lookup"><span data-stu-id="b601e-201"><span id="ERROR_WINHTTP_OPERATION_CANCELLED"></span><span id="error_winhttp_operation_cancelled"></span>**ERROR\_WINHTTP\_OPERATION\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b601e-202">12017</span><span class="sxs-lookup"><span data-stu-id="b601e-202">12017</span></span>
</dt> <dt>



<span data-ttu-id="b601e-203">L’opération a été annulée, généralement parce que le descripteur sur lequel la demande a été exécutée a été fermé avant la fin de l’opération.</span><span class="sxs-lookup"><span data-stu-id="b601e-203">The operation was canceled, usually because the handle on which the request was operating was closed before the operation completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b601e-204"><span id="ERROR_WINHTTP_OPTION_NOT_SETTABLE"></span><span id="error_winhttp_option_not_settable"></span>**ERREUR \_ WinHTTP \_ \_ non \_ définissable**</span><span class="sxs-lookup"><span data-stu-id="b601e-204"><span id="ERROR_WINHTTP_OPTION_NOT_SETTABLE"></span><span id="error_winhttp_option_not_settable"></span>**ERROR\_WINHTTP\_OPTION\_NOT\_SETTABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b601e-205">12011</span><span class="sxs-lookup"><span data-stu-id="b601e-205">12011</span></span>
</dt> <dt>



<span data-ttu-id="b601e-206">L’option demandée ne peut pas être définie, uniquement interrogée.</span><span class="sxs-lookup"><span data-stu-id="b601e-206">The requested option cannot be set, only queried.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b601e-207"><span id="ERROR_WINHTTP_OUT_OF_HANDLES"></span><span id="error_winhttp_out_of_handles"></span>**ERREUR \_ WinHTTP \_ hors \_ des \_ Handles**</span><span class="sxs-lookup"><span data-stu-id="b601e-207"><span id="ERROR_WINHTTP_OUT_OF_HANDLES"></span><span id="error_winhttp_out_of_handles"></span>**ERROR\_WINHTTP\_OUT\_OF\_HANDLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b601e-208">12001</span><span class="sxs-lookup"><span data-stu-id="b601e-208">12001</span></span>
</dt> <dt>



<span data-ttu-id="b601e-209">Périmé n’est plus utilisé.</span><span class="sxs-lookup"><span data-stu-id="b601e-209">Obsolete; no longer used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b601e-210"><span id="ERROR_WINHTTP_REDIRECT_FAILED"></span><span id="error_winhttp_redirect_failed"></span>**ERREUR lors de \_ \_ la redirection WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="b601e-210"><span id="ERROR_WINHTTP_REDIRECT_FAILED"></span><span id="error_winhttp_redirect_failed"></span>**ERROR\_WINHTTP\_REDIRECT\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b601e-211">12156</span><span class="sxs-lookup"><span data-stu-id="b601e-211">12156</span></span>
</dt> <dt>



<span data-ttu-id="b601e-212">La redirection a échoué parce que le schéma a été modifié ou que toutes les tentatives de redirection ont échoué (cinq tentatives par défaut).</span><span class="sxs-lookup"><span data-stu-id="b601e-212">The redirection failed because either the scheme changed or all attempts made to redirect failed (default is five attempts).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b601e-213"><span id="ERROR_WINHTTP_RESEND_REQUEST"></span><span id="error_winhttp_resend_request"></span>**ERREUR \_ WinHTTP de \_ renvoi de \_ demande**</span><span class="sxs-lookup"><span data-stu-id="b601e-213"><span id="ERROR_WINHTTP_RESEND_REQUEST"></span><span id="error_winhttp_resend_request"></span>**ERROR\_WINHTTP\_RESEND\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b601e-214">12032</span><span class="sxs-lookup"><span data-stu-id="b601e-214">12032</span></span>
</dt> <dt>



<span data-ttu-id="b601e-215">Échec de la fonction WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="b601e-215">The WinHTTP function failed.</span></span> <span data-ttu-id="b601e-216">La fonction souhaitée peut être retentée sur le même handle de demande.</span><span class="sxs-lookup"><span data-stu-id="b601e-216">The desired function can be retried on the same request handle.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b601e-217"><span id="ERROR_WINHTTP_RESPONSE_DRAIN_OVERFLOW"></span><span id="error_winhttp_response_drain_overflow"></span>**ERREUR de dépassement du drainage de la \_ \_ réponse WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b601e-217"><span id="ERROR_WINHTTP_RESPONSE_DRAIN_OVERFLOW"></span><span id="error_winhttp_response_drain_overflow"></span>**ERROR\_WINHTTP\_RESPONSE\_DRAIN\_OVERFLOW**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b601e-218">12184</span><span class="sxs-lookup"><span data-stu-id="b601e-218">12184</span></span>
</dt> <dt>



<span data-ttu-id="b601e-219">Retourné lorsqu’une réponse entrante dépasse une limite de taille WinHTTP interne.</span><span class="sxs-lookup"><span data-stu-id="b601e-219">Returned when an incoming response exceeds an internal WinHTTP size limit.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b601e-220"><span id="ERROR_WINHTTP_SCRIPT_EXECUTION_ERROR"></span><span id="error_winhttp_script_execution_error"></span>**ERREUR \_ d' \_ exécution du script WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b601e-220"><span id="ERROR_WINHTTP_SCRIPT_EXECUTION_ERROR"></span><span id="error_winhttp_script_execution_error"></span>**ERROR\_WINHTTP\_SCRIPT\_EXECUTION\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b601e-221">12177</span><span class="sxs-lookup"><span data-stu-id="b601e-221">12177</span></span>
</dt> <dt>



<span data-ttu-id="b601e-222">Une erreur s’est produite lors de l’exécution d’un script.</span><span class="sxs-lookup"><span data-stu-id="b601e-222">An error was encountered while executing a script.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b601e-223"><span id="ERROR_WINHTTP_SECURE_CERT_CN_INVALID"></span><span id="error_winhttp_secure_cert_cn_invalid"></span>**ERREUR \_ WinHTTP \_ \_ \_ non valide du certificat sécurisé \_ WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="b601e-223"><span id="ERROR_WINHTTP_SECURE_CERT_CN_INVALID"></span><span id="error_winhttp_secure_cert_cn_invalid"></span>**ERROR\_WINHTTP\_SECURE\_CERT\_CN\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b601e-224">12038</span><span class="sxs-lookup"><span data-stu-id="b601e-224">12038</span></span>
</dt> <dt>



<span data-ttu-id="b601e-225">Retourné lorsqu’un nom de nom commun de certificat ne correspond pas à la valeur transmise (équivalent à une erreur **CERT \_ E \_ CN \_ no \_ match** ).</span><span class="sxs-lookup"><span data-stu-id="b601e-225">Returned when a certificate CN name does not match the passed value (equivalent to a **CERT\_E\_CN\_NO\_MATCH** error).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b601e-226"><span id="ERROR_WINHTTP_SECURE_CERT_DATE_INVALID"></span><span id="error_winhttp_secure_cert_date_invalid"></span>**ERREUR \_ WinHTTP \_ sécurité de \_ certificat sécurisé \_ \_ non valide**</span><span class="sxs-lookup"><span data-stu-id="b601e-226"><span id="ERROR_WINHTTP_SECURE_CERT_DATE_INVALID"></span><span id="error_winhttp_secure_cert_date_invalid"></span>**ERROR\_WINHTTP\_SECURE\_CERT\_DATE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b601e-227">12037</span><span class="sxs-lookup"><span data-stu-id="b601e-227">12037</span></span>
</dt> <dt>



<span data-ttu-id="b601e-228">Indique qu’un certificat requis n’est pas dans sa période de validité lors de la vérification par rapport à l’horloge système actuelle ou à l’horodateur du fichier signé, ou que les périodes de validité de la chaîne de certification ne s’imbriquent pas correctement (équivalent à un **certificat \_ e \_ expiré** ou à une erreur de **certificat \_ e \_ VALIDITYPERIODNESTING** ).</span><span class="sxs-lookup"><span data-stu-id="b601e-228">Indicates that a required certificate is not within its validity period when verifying against the current system clock or the timestamp in the signed file, or that the validity periods of the certification chain do not nest correctly (equivalent to a **CERT\_E\_EXPIRED** or a **CERT\_E\_VALIDITYPERIODNESTING** error).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b601e-229"><span id="ERROR_WINHTTP_SECURE_CERT_REV_FAILED"></span><span id="error_winhttp_secure_cert_rev_failed"></span>**ERREUR \_ WinHTTP \_ échec de la \_ révision du certificat sécurisé \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b601e-229"><span id="ERROR_WINHTTP_SECURE_CERT_REV_FAILED"></span><span id="error_winhttp_secure_cert_rev_failed"></span>**ERROR\_WINHTTP\_SECURE\_CERT\_REV\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b601e-230">12057</span><span class="sxs-lookup"><span data-stu-id="b601e-230">12057</span></span>
</dt> <dt>



<span data-ttu-id="b601e-231">Indique que la révocation ne peut pas être vérifiée, car le serveur de révocation était hors connexion (ce qui équivaut à **Crypter \_ E \_ Revocation \_ hors connexion**).</span><span class="sxs-lookup"><span data-stu-id="b601e-231">Indicates that revocation cannot be checked because the revocation server was offline (equivalent to **CRYPT\_E\_REVOCATION\_OFFLINE**).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b601e-232"><span id="ERROR_WINHTTP_SECURE_CERT_REVOKED"></span><span id="error_winhttp_secure_cert_revoked"></span>**ERREUR \_ de \_ certificat sécurisé WinHTTP \_ \_ révoqué**</span><span class="sxs-lookup"><span data-stu-id="b601e-232"><span id="ERROR_WINHTTP_SECURE_CERT_REVOKED"></span><span id="error_winhttp_secure_cert_revoked"></span>**ERROR\_WINHTTP\_SECURE\_CERT\_REVOKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b601e-233">12170</span><span class="sxs-lookup"><span data-stu-id="b601e-233">12170</span></span>
</dt> <dt>



<span data-ttu-id="b601e-234">Indique qu’un certificat a été révoqué (ce qui équivaut à **Crypter \_ E \_ révoqué**).</span><span class="sxs-lookup"><span data-stu-id="b601e-234">Indicates that a certificate has been revoked (equivalent to **CRYPT\_E\_REVOKED**).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b601e-235"><span id="ERROR_WINHTTP_SECURE_CERT_WRONG_USAGE"></span><span id="error_winhttp_secure_cert_wrong_usage"></span>**ERREUR \_ d' \_ \_ \_ utilisation incorrecte du certificat sécurisé WinHTTP \_**</span><span class="sxs-lookup"><span data-stu-id="b601e-235"><span id="ERROR_WINHTTP_SECURE_CERT_WRONG_USAGE"></span><span id="error_winhttp_secure_cert_wrong_usage"></span>**ERROR\_WINHTTP\_SECURE\_CERT\_WRONG\_USAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b601e-236">12179</span><span class="sxs-lookup"><span data-stu-id="b601e-236">12179</span></span>
</dt> <dt>



<span data-ttu-id="b601e-237">Indique qu’un certificat n’est pas valide pour l’utilisation demandée (équivalent au certificat **\_ E \_ \_ utilisation incorrecte**).</span><span class="sxs-lookup"><span data-stu-id="b601e-237">Indicates that a certificate is not valid for the requested usage (equivalent to **CERT\_E\_WRONG\_USAGE**).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b601e-238"><span id="ERROR_WINHTTP_SECURE_CHANNEL_ERROR"></span><span id="error_winhttp_secure_channel_error"></span>**erreur \_ de \_ canal sécurisé WinHTTP \_ \_ erreur**</span><span class="sxs-lookup"><span data-stu-id="b601e-238"><span id="ERROR_WINHTTP_SECURE_CHANNEL_ERROR"></span><span id="error_winhttp_secure_channel_error"></span>**ERROR\_WINHTTP\_SECURE\_CHANNEL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b601e-239">12157</span><span class="sxs-lookup"><span data-stu-id="b601e-239">12157</span></span>
</dt> <dt>



<span data-ttu-id="b601e-240">Indique qu’une erreur s’est produite avec un canal sécurisé (équivalent aux codes d’erreur commençant par « SEC \_ e \_ » et « sec \_ I \_ » figurant dans le fichier d’en-tête « winerror. h »).</span><span class="sxs-lookup"><span data-stu-id="b601e-240">Indicates that an error occurred having to do with a secure channel (equivalent to error codes that begin with "SEC\_E\_" and "SEC\_I\_" listed in the "winerror.h" header file).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b601e-241"><span id="ERROR_WINHTTP_SECURE_FAILURE"></span><span id="error_winhttp_secure_failure"></span>**ERREUR \_ WinHTTP \_ Secure \_ Failure**</span><span class="sxs-lookup"><span data-stu-id="b601e-241"><span id="ERROR_WINHTTP_SECURE_FAILURE"></span><span id="error_winhttp_secure_failure"></span>**ERROR\_WINHTTP\_SECURE\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b601e-242">12175</span><span class="sxs-lookup"><span data-stu-id="b601e-242">12175</span></span>
</dt> <dt>



<span data-ttu-id="b601e-243">Une ou plusieurs erreurs ont été détectées dans le certificat SSL (Secure Sockets Layer) (SSL) envoyé par le serveur.</span><span class="sxs-lookup"><span data-stu-id="b601e-243">One or more errors were found in the Secure Sockets Layer (SSL) certificate sent by the server.</span></span> <span data-ttu-id="b601e-244">Pour déterminer le type d’erreur rencontré, recherchez une notification de [**\_ \_ \_ \_ défaillance sécurisée d’état de rappel WinHTTP**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) dans une fonction de rappel d’État.</span><span class="sxs-lookup"><span data-stu-id="b601e-244">To determine what type of error was encountered, check for a [**WINHTTP\_CALLBACK\_STATUS\_SECURE\_FAILURE**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) notification in a status callback function.</span></span> <span data-ttu-id="b601e-245">Pour plus d’informations, voir [**WinHTTP \_ Status \_ callback**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback).</span><span class="sxs-lookup"><span data-stu-id="b601e-245">For more information, see [**WINHTTP\_STATUS\_CALLBACK**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b601e-246"><span id="ERROR_WINHTTP_SECURE_INVALID_CA"></span><span id="error_winhttp_secure_invalid_ca"></span>**ERREUR \_ WinHTTP \_ sécurisée \_ non valide pour l' \_ autorité de certification**</span><span class="sxs-lookup"><span data-stu-id="b601e-246"><span id="ERROR_WINHTTP_SECURE_INVALID_CA"></span><span id="error_winhttp_secure_invalid_ca"></span>**ERROR\_WINHTTP\_SECURE\_INVALID\_CA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b601e-247">12045</span><span class="sxs-lookup"><span data-stu-id="b601e-247">12045</span></span>
</dt> <dt>



<span data-ttu-id="b601e-248">Indique qu’une chaîne de certificats a été traitée, mais s’est terminée dans un certificat racine qui n’est pas approuvé par le fournisseur d’approbation (équivalent au **CERT \_ E \_ UNTRUSTEDROOT**).</span><span class="sxs-lookup"><span data-stu-id="b601e-248">Indicates that a certificate chain was processed, but terminated in a root certificate that is not trusted by the trust provider (equivalent to **CERT\_E\_UNTRUSTEDROOT**).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b601e-249"><span id="ERROR_WINHTTP_SECURE_INVALID_CERT"></span><span id="error_winhttp_secure_invalid_cert"></span>**ERREUR \_ WinHTTP \_ sécuriser le \_ certificat non valide \_**</span><span class="sxs-lookup"><span data-stu-id="b601e-249"><span id="ERROR_WINHTTP_SECURE_INVALID_CERT"></span><span id="error_winhttp_secure_invalid_cert"></span>**ERROR\_WINHTTP\_SECURE\_INVALID\_CERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b601e-250">12169</span><span class="sxs-lookup"><span data-stu-id="b601e-250">12169</span></span>
</dt> <dt>



<span data-ttu-id="b601e-251">Indique qu’un certificat n’est pas valide (équivalent à des erreurs telles que le **\_ \_ rôle CERT e**, **CERT \_ e \_ PATHLENCONST**, CERT e **\_ \_ Critical**, **CERT \_ e \_ Purpose**, **CERT \_ e \_ ISSUERCHAINING**, **CERT \_ e \_ incorrecte** et le **\_ \_ chaînage e Cert**).</span><span class="sxs-lookup"><span data-stu-id="b601e-251">Indicates that a certificate is invalid (equivalent to errors such as **CERT\_E\_ROLE**, **CERT\_E\_PATHLENCONST**, **CERT\_E\_CRITICAL**, **CERT\_E\_PURPOSE**, **CERT\_E\_ISSUERCHAINING**, **CERT\_E\_MALFORMED** and **CERT\_E\_CHAINING**).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b601e-252"><span id="ERROR_WINHTTP_SHUTDOWN"></span><span id="error_winhttp_shutdown"></span>**ERREUR \_ d' \_ arrêt WinHTTP**</span><span class="sxs-lookup"><span data-stu-id="b601e-252"><span id="ERROR_WINHTTP_SHUTDOWN"></span><span id="error_winhttp_shutdown"></span>**ERROR\_WINHTTP\_SHUTDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b601e-253">12012</span><span class="sxs-lookup"><span data-stu-id="b601e-253">12012</span></span>
</dt> <dt>



<span data-ttu-id="b601e-254">La prise en charge de la fonction WinHTTP est en cours d’arrêt ou de déchargement.</span><span class="sxs-lookup"><span data-stu-id="b601e-254">The WinHTTP function support is being shut down or unloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b601e-255"><span id="ERROR_WINHTTP_TIMEOUT"></span><span id="error_winhttp_timeout"></span>**ERREUR \_ WinHTTP de \_ dépassement de délai**</span><span class="sxs-lookup"><span data-stu-id="b601e-255"><span id="ERROR_WINHTTP_TIMEOUT"></span><span id="error_winhttp_timeout"></span>**ERROR\_WINHTTP\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b601e-256">12002</span><span class="sxs-lookup"><span data-stu-id="b601e-256">12002</span></span>
</dt> <dt>



<span data-ttu-id="b601e-257">Le délai d'attente de la requête a expiré.</span><span class="sxs-lookup"><span data-stu-id="b601e-257">The request has timed out.</span></span>

<span data-ttu-id="b601e-258">Cette erreur peut être retournée à la suite du comportement du délai d’expiration TCP/IP, quelles que soient les valeurs de délai d’attente définies dans les services HTTP Windows.</span><span class="sxs-lookup"><span data-stu-id="b601e-258">This error can be returned as a result of TCP/IP time-out behavior, regardless of time-out values set in Windows HTTP Services.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b601e-259"><span id="ERROR_WINHTTP_UNABLE_TO_DOWNLOAD_SCRIPT"></span><span id="error_winhttp_unable_to_download_script"></span>**ERREUR \_ WinHTTP \_ Impossible \_ de \_ Télécharger le \_ script**</span><span class="sxs-lookup"><span data-stu-id="b601e-259"><span id="ERROR_WINHTTP_UNABLE_TO_DOWNLOAD_SCRIPT"></span><span id="error_winhttp_unable_to_download_script"></span>**ERROR\_WINHTTP\_UNABLE\_TO\_DOWNLOAD\_SCRIPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b601e-260">12167</span><span class="sxs-lookup"><span data-stu-id="b601e-260">12167</span></span>
</dt> <dt>



<span data-ttu-id="b601e-261">Impossible de télécharger le fichier PAC.</span><span class="sxs-lookup"><span data-stu-id="b601e-261">The PAC file cannot be downloaded.</span></span> <span data-ttu-id="b601e-262">Par exemple, le serveur référencé par l’URL PAC n’a peut-être pas été accessible ou le serveur a retourné une réponse 404 introuvable.</span><span class="sxs-lookup"><span data-stu-id="b601e-262">For example, the server referenced by the PAC URL may not have been reachable, or the server returned a 404 NOT FOUND response.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b601e-263"><span id="ERROR_WINHTTP_UNHANDLED_SCRIPT_TYPE"></span><span id="error_winhttp_unhandled_script_type"></span>**ERREUR \_ de \_ type de script non géré WinHTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="b601e-263"><span id="ERROR_WINHTTP_UNHANDLED_SCRIPT_TYPE"></span><span id="error_winhttp_unhandled_script_type"></span>**ERROR\_WINHTTP\_UNHANDLED\_SCRIPT\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b601e-264">12176</span><span class="sxs-lookup"><span data-stu-id="b601e-264">12176</span></span>
</dt> <dt>



<span data-ttu-id="b601e-265">Le type de script n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="b601e-265">The script type is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b601e-266"><span id="ERROR_WINHTTP_UNRECOGNIZED_SCHEME"></span><span id="error_winhttp_unrecognized_scheme"></span>**ERREUR \_ de \_ schéma WinHTTP non reconnu \_**</span><span class="sxs-lookup"><span data-stu-id="b601e-266"><span id="ERROR_WINHTTP_UNRECOGNIZED_SCHEME"></span><span id="error_winhttp_unrecognized_scheme"></span>**ERROR\_WINHTTP\_UNRECOGNIZED\_SCHEME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b601e-267">12006</span><span class="sxs-lookup"><span data-stu-id="b601e-267">12006</span></span>
</dt> <dt>



<span data-ttu-id="b601e-268">L’URL a spécifié un schéma autre que « http : » ou « https : ».</span><span class="sxs-lookup"><span data-stu-id="b601e-268">The URL specified a scheme other than "http:" or "https:".</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b601e-269"><span id="ERROR_NOT_ENOUGH_MEMORY"></span><span id="error_not_enough_memory"></span>**ERREUR \_ de \_ mémoire insuffisante \_**</span><span class="sxs-lookup"><span data-stu-id="b601e-269"><span id="ERROR_NOT_ENOUGH_MEMORY"></span><span id="error_not_enough_memory"></span>**ERROR\_NOT\_ENOUGH\_MEMORY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b601e-270">Mémoire disponible insuffisante pour terminer l’opération demandée.</span><span class="sxs-lookup"><span data-stu-id="b601e-270">Not enough memory was available to complete the requested operation.</span></span>

<span data-ttu-id="b601e-271">**En-tête :** Déclaré dans Winerror. h</span><span class="sxs-lookup"><span data-stu-id="b601e-271">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b601e-272"><span id="ERROR_INSUFFICIENT_BUFFER"></span><span id="error_insufficient_buffer"></span>**ERREUR \_ de \_ mémoire tampon insuffisante**</span><span class="sxs-lookup"><span data-stu-id="b601e-272"><span id="ERROR_INSUFFICIENT_BUFFER"></span><span id="error_insufficient_buffer"></span>**ERROR\_INSUFFICIENT\_BUFFER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b601e-273">La taille, en octets, de la mémoire tampon fournie à une fonction était insuffisante pour contenir les données retournées.</span><span class="sxs-lookup"><span data-stu-id="b601e-273">The size, in bytes, of the buffer supplied to a function was insufficient to contain the returned data.</span></span> <span data-ttu-id="b601e-274">Pour plus d’informations, consultez la fonction spécifique.</span><span class="sxs-lookup"><span data-stu-id="b601e-274">For more information, see the specific function.</span></span>

<span data-ttu-id="b601e-275">**En-tête :** Déclaré dans Winerror. h</span><span class="sxs-lookup"><span data-stu-id="b601e-275">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b601e-276"><span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**HANDLE d’erreur \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="b601e-276"><span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**ERROR\_INVALID\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b601e-277">Le descripteur passé à l’interface de programmation d’applications (API) a été invalidé ou fermé.</span><span class="sxs-lookup"><span data-stu-id="b601e-277">The handle passed to the application programming interface (API) has been either invalidated or closed.</span></span>

<span data-ttu-id="b601e-278">**En-tête :** Déclaré dans Winerror. h</span><span class="sxs-lookup"><span data-stu-id="b601e-278">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b601e-279"><span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**ERREUR \_ \_ plus aucun \_ fichier**</span><span class="sxs-lookup"><span data-stu-id="b601e-279"><span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**ERROR\_NO\_MORE\_FILES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b601e-280">Aucun autre fichier n’a été trouvé.</span><span class="sxs-lookup"><span data-stu-id="b601e-280">No more files have been found.</span></span>

<span data-ttu-id="b601e-281">**En-tête :** Déclaré dans Winerror. h</span><span class="sxs-lookup"><span data-stu-id="b601e-281">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b601e-282"><span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**ERREUR \_ aucun \_ autre \_ élément**</span><span class="sxs-lookup"><span data-stu-id="b601e-282"><span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**ERROR\_NO\_MORE\_ITEMS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b601e-283">Aucun autre élément n’a été trouvé.</span><span class="sxs-lookup"><span data-stu-id="b601e-283">No more items have been found.</span></span>

<span data-ttu-id="b601e-284">**En-tête :** Déclaré dans Winerror. h</span><span class="sxs-lookup"><span data-stu-id="b601e-284">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="b601e-285"><span id="ERROR_NOT_SUPPORTED"></span><span id="error_not_supported"></span>**ERREUR \_ non \_ prise en charge**</span><span class="sxs-lookup"><span data-stu-id="b601e-285"><span id="ERROR_NOT_SUPPORTED"></span><span id="error_not_supported"></span>**ERROR\_NOT\_SUPPORTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="b601e-286">La pile de protocoles requise n’est pas chargée et l’application ne peut pas démarrer WinSock.</span><span class="sxs-lookup"><span data-stu-id="b601e-286">The required protocol stack is not loaded and the application cannot start WinSock.</span></span>

<span data-ttu-id="b601e-287">**En-tête :** Déclaré dans Winerror. h</span><span class="sxs-lookup"><span data-stu-id="b601e-287">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b601e-288">Notes</span><span class="sxs-lookup"><span data-stu-id="b601e-288">Remarks</span></span>

<span data-ttu-id="b601e-289">Pour Windows XP et Windows 2000, consultez la section [Configuration requise](winhttp-start-page.md) pour l’exécution de la page de démarrage de WinHTTP.</span><span class="sxs-lookup"><span data-stu-id="b601e-289">For Windows XP and Windows 2000, see the [Run-Time Requirements](winhttp-start-page.md) section of the WinHttp start page.</span></span>

## <a name="requirements"></a><span data-ttu-id="b601e-290">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b601e-290">Requirements</span></span>



| <span data-ttu-id="b601e-291">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b601e-291">Requirement</span></span> | <span data-ttu-id="b601e-292">Valeur</span><span class="sxs-lookup"><span data-stu-id="b601e-292">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="b601e-293">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b601e-293">Minimum supported client</span></span><br/> | <span data-ttu-id="b601e-294">Windows XP, Windows 2000 Professionnel avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b601e-294">Windows XP, Windows 2000 Professional with SP3 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="b601e-295">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b601e-295">Minimum supported server</span></span><br/> | <span data-ttu-id="b601e-296">Windows Server 2003, Windows 2000 Server avec les \[ applications de bureau SP3 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b601e-296">Windows Server 2003, Windows 2000 Server with SP3 \[desktop apps only\]</span></span><br/>         |
| <span data-ttu-id="b601e-297">Composant redistribuable</span><span class="sxs-lookup"><span data-stu-id="b601e-297">Redistributable</span></span><br/>          | <span data-ttu-id="b601e-298">WinHTTP 5,0 et Internet Explorer 5,01 ou version ultérieure sur Windows XP et Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="b601e-298">WinHTTP 5.0 and Internet Explorer 5.01 or later on Windows XP and Windows 2000.</span></span><br/> |
| <span data-ttu-id="b601e-299">En-tête</span><span class="sxs-lookup"><span data-stu-id="b601e-299">Header</span></span><br/>                   | <dl> <span data-ttu-id="b601e-300"><dt>WinHTTP. h</dt></span><span class="sxs-lookup"><span data-stu-id="b601e-300"><dt>Winhttp.h</dt></span></span> </dl>       |



## <a name="see-also"></a><span data-ttu-id="b601e-301">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b601e-301">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b601e-302">Versions de WinHTTP</span><span class="sxs-lookup"><span data-stu-id="b601e-302">WinHTTP Versions</span></span>](winhttp-versions.md)
</dt> </dl>

 

