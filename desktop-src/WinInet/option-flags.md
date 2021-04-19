---
title: Indicateurs d’option (Wininet. h)
description: Les indicateurs d’option suivants sont utilisés avec les fonctions InternetQueryOption et InternetSetOption. Tous les indicateurs d’option valides ont une valeur supérieure ou égale à INTERNET \_ First \_ option et sont inférieures ou égales à Internet \_ Last \_ option.
ms.assetid: 708510b8-468a-4287-849b-cba3d7001ea8
topic_type:
- apiref
api_name:
- INTERNET_OPTION_ALTER_IDENTITY
- INTERNET_OPTION_ASYNC
- INTERNET_OPTION_ASYNC_ID
- INTERNET_OPTION_ASYNC_PRIORITY
- INTERNET_OPTION_BYPASS_EDITED_ENTRY
- INTERNET_OPTION_CACHE_STREAM_HANDLE
- INTERNET_OPTION_CACHE_TIMESTAMPS
- INTERNET_OPTION_CALLBACK
- INTERNET_OPTION_CALLBACK_FILTER
- INTERNET_OPTION_CLIENT_CERT_CONTEXT
- INTERNET_OPTION_CODEPAGE
- INTERNET_OPTION_CODEPAGE_PATH
- INTERNET_OPTION_CODEPAGE_EXTRA
- INTERNET_OPTION_COMPRESSED_CONTENT_LENGTH
- INTERNET_OPTION_CONNECT_BACKOFF
- INTERNET_OPTION_CONNECT_RETRIES
- INTERNET_OPTION_CONNECT_TIME
- INTERNET_OPTION_CONNECT_TIMEOUT
- INTERNET_OPTION_CONNECTED_STATE
- INTERNET_OPTION_CONTEXT_VALUE
- INTERNET_OPTION_CONTROL_RECEIVE_TIMEOUT
- INTERNET_OPTION_CONTROL_SEND_TIMEOUT
- INTERNET_OPTION_DATA_RECEIVE_TIMEOUT
- INTERNET_OPTION_DATA_SEND_TIMEOUT
- INTERNET_OPTION_DATAFILE_NAME
- INTERNET_OPTION_DATAFILE_EXT
- INTERNET_OPTION_DIAGNOSTIC_SOCKET_INFO
- INTERNET_OPTION_DIGEST_AUTH_UNLOAD
- INTERNET_OPTION_DISABLE_AUTODIAL
- INTERNET_OPTION_DISCONNECTED_TIMEOUT
- INTERNET_OPTION_ENABLE_HTTP_PROTOCOL
- INTERNET_OPTION_ENABLE_REDIRECT_CACHE_READ
- INTERNET_OPTION_ENCODE_EXTRA
- INTERNET_OPTION_END_BROWSER_SESSION
- INTERNET_OPTION_ERROR_MASK
- INTERNET_OPTION_ENTERPRISE_CONTEXT
- INTERNET_OPTION_EXTENDED_ERROR
- INTERNET_OPTION_FROM_CACHE_TIMEOUT
- INTERNET_OPTION_HANDLE_TYPE
- INTERNET_OPTION_HSTS
- INTERNET_OPTION_HTTP_DECODING
- INTERNET_OPTION_HTTP_PROTOCOL_USED
- INTERNET_OPTION_HTTP_VERSION
- INTERNET_OPTION_IDENTITY
- INTERNET_OPTION_IDLE_STATE
- INTERNET_OPTION_IDN
- INTERNET_OPTION_IGNORE_OFFLINE
- INTERNET_OPTION_KEEP_CONNECTION
- INTERNET_OPTION_LISTEN_TIMEOUT
- INTERNET_OPTION_MAX_CONNS_PER_1_0_SERVER
- INTERNET_OPTION_MAX_CONNS_PER_PROXY
- INTERNET_OPTION_MAX_CONNS_PER_SERVER
- INTERNET_OPTION_OFFLINE_MODE
- INTERNET_OPTION_OFFLINE_SEMANTICS
- INTERNET_OPTION_OPT_IN_WEAK_SIGNATURE
- INTERNET_OPTION_PARENT_HANDLE
- INTERNET_OPTION_PASSWORD
- INTERNET_OPTION_PER_CONNECTION_OPTION
- INTERNET_OPTION_POLICY
- INTERNET_OPTION_PROXY
- INTERNET_OPTION_PROXY_PASSWORD
- INTERNET_OPTION_PROXY_SETTINGS_CHANGED
- INTERNET_OPTION_PROXY_USERNAME
- INTERNET_OPTION_READ_BUFFER_SIZE
- INTERNET_OPTION_RECEIVE_THROUGHPUT
- INTERNET_OPTION_RECEIVE_TIMEOUT
- INTERNET_OPTION_REFRESH
- INTERNET_OPTION_REMOVE_IDENTITY
- INTERNET_OPTION_REQUEST_FLAGS
- INTERNET_OPTION_REQUEST_PRIORITY
- INTERNET_OPTION_RESET_URLCACHE_SESSION
- INTERNET_OPTION_SECONDARY_CACHE_KEY
- INTERNET_OPTION_SECURITY_CERTIFICATE
- INTERNET_OPTION_SECURITY_CERTIFICATE_STRUCT
- INTERNET_OPTION_SECURITY_FLAGS
- INTERNET_OPTION_SECURITY_KEY_BITNESS
- INTERNET_OPTION_SEND_THROUGHPUT
- INTERNET_OPTION_SEND_TIMEOUT
- INTERNET_OPTION_SERVER_CERT_CHAIN_CONTEXT
- INTERNET_OPTION_SETTINGS_CHANGED
- INTERNET_OPTION_SUPPRESS_SERVER_AUTH
- INTERNET_OPTION_SUPPRESS_BEHAVIOR
- INTERNET_OPTION_URL
- INTERNET_OPTION_USER_AGENT
- INTERNET_OPTION_USERNAME
- INTERNET_OPTION_VERSION
- INTERNET_OPTION_WRITE_BUFFER_SIZE
api_location:
- Wininet.h
- Winineti.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0c99ca6f12836c620ed7c952e0ceb1844aee3b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106516104"
---
# <a name="option-flags-winineth"></a><span data-ttu-id="ecc71-104">Indicateurs d’option (Wininet. h)</span><span class="sxs-lookup"><span data-stu-id="ecc71-104">Option Flags (Wininet.h)</span></span>

<span data-ttu-id="ecc71-105">Les indicateurs d’option suivants sont utilisés avec les fonctions [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) et [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) .</span><span class="sxs-lookup"><span data-stu-id="ecc71-105">The following option flags are used with the [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) functions.</span></span> <span data-ttu-id="ecc71-106">Tous les indicateurs d’option valides ont une valeur supérieure ou égale à **Internet \_ First \_ option** et sont inférieures ou égales à **Internet \_ Last \_ option**.</span><span class="sxs-lookup"><span data-stu-id="ecc71-106">All valid option flags have a value greater than or equal to **INTERNET\_FIRST\_OPTION** and less than or equal to **INTERNET\_LAST\_OPTION**.</span></span>

<dl> <dt>

<span data-ttu-id="ecc71-107"><span id="INTERNET_OPTION_ALTER_IDENTITY"></span><span id="internet_option_alter_identity"></span>**\_option Internet \_ ALTER \_ Identity**</span><span class="sxs-lookup"><span data-stu-id="ecc71-107"><span id="INTERNET_OPTION_ALTER_IDENTITY"></span><span id="internet_option_alter_identity"></span>**INTERNET\_OPTION\_ALTER\_IDENTITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-108">80</span><span class="sxs-lookup"><span data-stu-id="ecc71-108">80</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-109">Non implémenté</span><span class="sxs-lookup"><span data-stu-id="ecc71-109">Not implemented</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-110"><span id="INTERNET_OPTION_ASYNC"></span><span id="internet_option_async"></span>**\_option Internet \_ Async**</span><span class="sxs-lookup"><span data-stu-id="ecc71-110"><span id="INTERNET_OPTION_ASYNC"></span><span id="internet_option_async"></span>**INTERNET\_OPTION\_ASYNC**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-111">30</span><span class="sxs-lookup"><span data-stu-id="ecc71-111">30</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-112">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="ecc71-112">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-113"><span id="INTERNET_OPTION_ASYNC_ID"></span><span id="internet_option_async_id"></span>**\_ \_ ID Async de l’option Internet \_**</span><span class="sxs-lookup"><span data-stu-id="ecc71-113"><span id="INTERNET_OPTION_ASYNC_ID"></span><span id="internet_option_async_id"></span>**INTERNET\_OPTION\_ASYNC\_ID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-114">15</span><span class="sxs-lookup"><span data-stu-id="ecc71-114">15</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-115">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="ecc71-115">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-116"><span id="INTERNET_OPTION_ASYNC_PRIORITY"></span><span id="internet_option_async_priority"></span>**\_option Internet \_ \_ priorité asynchrone**</span><span class="sxs-lookup"><span data-stu-id="ecc71-116"><span id="INTERNET_OPTION_ASYNC_PRIORITY"></span><span id="internet_option_async_priority"></span>**INTERNET\_OPTION\_ASYNC\_PRIORITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-117">16</span><span class="sxs-lookup"><span data-stu-id="ecc71-117">16</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-118">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="ecc71-118">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-119"><span id="INTERNET_OPTION_BYPASS_EDITED_ENTRY"></span><span id="internet_option_bypass_edited_entry"></span>**\_option Internet \_ Ignorer \_ l' \_ entrée modifiée**</span><span class="sxs-lookup"><span data-stu-id="ecc71-119"><span id="INTERNET_OPTION_BYPASS_EDITED_ENTRY"></span><span id="internet_option_bypass_edited_entry"></span>**INTERNET\_OPTION\_BYPASS\_EDITED\_ENTRY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-120">64</span><span class="sxs-lookup"><span data-stu-id="ecc71-120">64</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-121">Définit ou récupère la valeur booléenne qui détermine si le système doit vérifier si le réseau dispose d’un contenu plus récent et remplacer les entrées du cache modifiées si une version plus récente est trouvée.</span><span class="sxs-lookup"><span data-stu-id="ecc71-121">Sets or retrieves the Boolean value that determines if the system should check the network for newer content and overwrite edited cache entries if a newer version is found.</span></span> <span data-ttu-id="ecc71-122">Si la valeur est **true**, le système vérifie que le contenu du réseau est plus récent et remplace l’entrée de cache modifiée par la version plus récente.</span><span class="sxs-lookup"><span data-stu-id="ecc71-122">If set to **True**, the system checks the network for newer content and overwrites the edited cache entry with the newer version.</span></span> <span data-ttu-id="ecc71-123">La valeur par défaut est **false**, ce qui indique que l’entrée de cache modifiée doit être utilisée sans vérification du réseau.</span><span class="sxs-lookup"><span data-stu-id="ecc71-123">The default is **False**, which indicates that the edited cache entry should be used without checking the network.</span></span> <span data-ttu-id="ecc71-124">Utilisé par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) et [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="ecc71-124">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="ecc71-125">Elle est valide uniquement dans Microsoft Internet Explorer 5 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ecc71-125">It is valid only in Microsoft Internet Explorer 5 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-126"><span id="INTERNET_OPTION_CACHE_STREAM_HANDLE"></span><span id="internet_option_cache_stream_handle"></span>**\_ \_ \_ descripteur du flux de cache des options Internet \_**</span><span class="sxs-lookup"><span data-stu-id="ecc71-126"><span id="INTERNET_OPTION_CACHE_STREAM_HANDLE"></span><span id="internet_option_cache_stream_handle"></span>**INTERNET\_OPTION\_CACHE\_STREAM\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-127">27</span><span class="sxs-lookup"><span data-stu-id="ecc71-127">27</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-128">N'est plus pris en charge.</span><span class="sxs-lookup"><span data-stu-id="ecc71-128">No longer supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-129"><span id="INTERNET_OPTION_CACHE_TIMESTAMPS"></span><span id="internet_option_cache_timestamps"></span>**\_ \_ horodateurs du cache des options Internet \_**</span><span class="sxs-lookup"><span data-stu-id="ecc71-129"><span id="INTERNET_OPTION_CACHE_TIMESTAMPS"></span><span id="internet_option_cache_timestamps"></span>**INTERNET\_OPTION\_CACHE\_TIMESTAMPS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-130">69</span><span class="sxs-lookup"><span data-stu-id="ecc71-130">69</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-131">Récupère une structure [**d' \_ \_ horodateurs de cache Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_timestamps) qui contient l’heure de la LastModified et l’heure d’expiration de la ressource stockée dans le cache Internet.</span><span class="sxs-lookup"><span data-stu-id="ecc71-131">Retrieves an [**INTERNET\_CACHE\_TIMESTAMPS**](/windows/desktop/api/Wininet/ns-wininet-internet_cache_timestamps) structure that contains the LastModified time and Expires time from the resource stored in the Internet cache.</span></span> <span data-ttu-id="ecc71-132">Cette valeur est utilisée par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="ecc71-132">This value is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-133"><span id="INTERNET_OPTION_CALLBACK"></span><span id="internet_option_callback"></span>**\_rappel d’option Internet \_**</span><span class="sxs-lookup"><span data-stu-id="ecc71-133"><span id="INTERNET_OPTION_CALLBACK"></span><span id="internet_option_callback"></span>**INTERNET\_OPTION\_CALLBACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-134">1</span><span class="sxs-lookup"><span data-stu-id="ecc71-134">1</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-135">Définit ou récupère l’adresse de la fonction de rappel définie pour ce handle.</span><span class="sxs-lookup"><span data-stu-id="ecc71-135">Sets or retrieves the address of the callback function defined for this handle.</span></span> <span data-ttu-id="ecc71-136">Cette option peut être utilisée sur tous les descripteurs [**HINTERNET**](appendix-a-hinternet-handles.md) .</span><span class="sxs-lookup"><span data-stu-id="ecc71-136">This option can be used on all [**HINTERNET**](appendix-a-hinternet-handles.md) handles.</span></span> <span data-ttu-id="ecc71-137">Utilisé par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) et [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="ecc71-137">Used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-138"><span id="INTERNET_OPTION_CALLBACK_FILTER"></span><span id="internet_option_callback_filter"></span>**\_filtre de \_ rappel d’option Internet \_**</span><span class="sxs-lookup"><span data-stu-id="ecc71-138"><span id="INTERNET_OPTION_CALLBACK_FILTER"></span><span id="internet_option_callback_filter"></span>**INTERNET\_OPTION\_CALLBACK\_FILTER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-139">54</span><span class="sxs-lookup"><span data-stu-id="ecc71-139">54</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-140">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="ecc71-140">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-141"><span id="INTERNET_OPTION_CLIENT_CERT_CONTEXT"></span><span id="internet_option_client_cert_context"></span>**\_contexte de \_ \_ certificat client \_ de l’option Internet**</span><span class="sxs-lookup"><span data-stu-id="ecc71-141"><span id="INTERNET_OPTION_CLIENT_CERT_CONTEXT"></span><span id="internet_option_client_cert_context"></span>**INTERNET\_OPTION\_CLIENT\_CERT\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-142">84</span><span class="sxs-lookup"><span data-stu-id="ecc71-142">84</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-143">Cet indicateur n’est pas pris en charge par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="ecc71-143">This flag is not supported by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span> <span data-ttu-id="ecc71-144">Le paramètre *lpBuffer* doit être un pointeur vers une structure de [**\_ contexte de certificat**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) et non un pointeur vers un pointeur de **\_ contexte de certificat** .</span><span class="sxs-lookup"><span data-stu-id="ecc71-144">The *lpBuffer* parameter must be a pointer to a [**CERT\_CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) structure and not a pointer to a **CERT\_CONTEXT** pointer.</span></span> <span data-ttu-id="ecc71-145">Si une application reçoit un certificat d' **\_ authentification de \_ client Internet \_ \_ \_ requis**, elle doit appeler [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) ou utiliser [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) pour fournir un certificat avant de retenter la demande.</span><span class="sxs-lookup"><span data-stu-id="ecc71-145">If an application receives **ERROR\_INTERNET\_CLIENT\_AUTH\_CERT\_NEEDED**, it must call [**InternetErrorDlg**](/windows/desktop/api/Wininet/nf-wininet-interneterrordlg) or use [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) to supply a certificate before retrying the request.</span></span> <span data-ttu-id="ecc71-146">[**CertDuplicateCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) est ensuite appelé afin que le contexte de certificat passé puisse être libéré indépendamment par l’application.</span><span class="sxs-lookup"><span data-stu-id="ecc71-146">[**CertDuplicateCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext) is then called so that the certificate context passed can be independently released by the application.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-147"><span id="INTERNET_OPTION_CODEPAGE"></span><span id="internet_option_codepage"></span>**page de codes de l' \_ option Internet \_**</span><span class="sxs-lookup"><span data-stu-id="ecc71-147"><span id="INTERNET_OPTION_CODEPAGE"></span><span id="internet_option_codepage"></span>**INTERNET\_OPTION\_CODEPAGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-148">68</span><span class="sxs-lookup"><span data-stu-id="ecc71-148">68</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-149">Par défaut, la partie hôte ou autorité de l’URL Unicode est encodée en fonction de la spécification IDN.</span><span class="sxs-lookup"><span data-stu-id="ecc71-149">By default, the host or authority portion of the Unicode URL is encoded according to the IDN specification.</span></span> <span data-ttu-id="ecc71-150">Si vous définissez cette option sur la demande, ou sur le descripteur de connexion, lorsque l’IDN est désactivé, spécifie un schéma d’encodage de page de codes pour la partie hôte de l’URL.</span><span class="sxs-lookup"><span data-stu-id="ecc71-150">Setting this option on the request, or connection handle, when IDN is disabled, specifies a code page encoding scheme for the host portion of the URL.</span></span> <span data-ttu-id="ecc71-151">Le paramètre *lpBuffer* dans l’appel à [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) contient la page de codes DBCS souhaitée.</span><span class="sxs-lookup"><span data-stu-id="ecc71-151">The *lpBuffer* parameter in the call to [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) contains the desired DBCS code page.</span></span> <span data-ttu-id="ecc71-152">Si aucune page de codes n’est spécifiée dans *lpBuffer*, Wininet utilise la page de codes système par défaut (CP \_ ACP).</span><span class="sxs-lookup"><span data-stu-id="ecc71-152">If no code page is specified in *lpBuffer*, WinINet uses the default system code page (CP\_ACP).</span></span> <span data-ttu-id="ecc71-153">Remarque : cette option est ignorée si l’IDN n’est pas désactivé.</span><span class="sxs-lookup"><span data-stu-id="ecc71-153">Note: This option is ignored if IDN is not disabled.</span></span> <span data-ttu-id="ecc71-154">Pour plus d’informations sur la désactivation de l’IDN, consultez l’option **Internet \_ \_ IDN** .</span><span class="sxs-lookup"><span data-stu-id="ecc71-154">For more information about how to disable IDN, see the **INTERNET\_OPTION\_IDN** option.</span></span>

<span data-ttu-id="ecc71-155">**Windows XP avec SP2 et Windows Server 2003 avec SP1 :** Cet indicateur n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="ecc71-155">**Windows XP with SP2 and Windows Server 2003 with SP1:** This flag is not supported.</span></span>

<span data-ttu-id="ecc71-156">**Version :** Nécessite Internet Explorer 7,0.</span><span class="sxs-lookup"><span data-stu-id="ecc71-156">**Version:** Requires Internet Explorer 7.0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-157"><span id="INTERNET_OPTION_CODEPAGE_PATH"></span><span id="internet_option_codepage_path"></span>**chemin de la page de codes de l' \_ option Internet \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ecc71-157"><span id="INTERNET_OPTION_CODEPAGE_PATH"></span><span id="internet_option_codepage_path"></span>**INTERNET\_OPTION\_CODEPAGE\_PATH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-158">100</span><span class="sxs-lookup"><span data-stu-id="ecc71-158">100</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-159">Par défaut, la partie chemin d’accès de l’URL est encodée en UTF8.</span><span class="sxs-lookup"><span data-stu-id="ecc71-159">By default, the path portion of the URL is UTF8 encoded.</span></span> <span data-ttu-id="ecc71-160">L’API WinINet exécute un caractère d’échappement (%) encodage sur les caractères étendus.</span><span class="sxs-lookup"><span data-stu-id="ecc71-160">The WinINet API performs escape character (%) encoding on the high-bit characters.</span></span> <span data-ttu-id="ecc71-161">La définition de cette option sur la demande, ou le descripteur de connexion, désactive l’encodage UTF8 et définit une page de codes spécifique.</span><span class="sxs-lookup"><span data-stu-id="ecc71-161">Setting this option on the request, or connection handle, disables the UTF8 encoding and sets a specific code page.</span></span> <span data-ttu-id="ecc71-162">Le paramètre *lpBuffer* dans l’appel à [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) contient la page de codes DBCS souhaitée pour le chemin d’accès.</span><span class="sxs-lookup"><span data-stu-id="ecc71-162">The *lpBuffer* parameter in the call to [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) contains the desired DBCS codepage for the path.</span></span> <span data-ttu-id="ecc71-163">Si aucune page de codes n’est spécifiée dans *lpBuffer*, Wininet utilise la valeur par défaut de CP \_ UTF8.</span><span class="sxs-lookup"><span data-stu-id="ecc71-163">If no code page is specified in *lpBuffer*, WinINet uses the default CP\_UTF8.</span></span>

<span data-ttu-id="ecc71-164">**Windows XP avec SP2 et Windows Server 2003 avec SP1 :** Cet indicateur n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="ecc71-164">**Windows XP with SP2 and Windows Server 2003 with SP1:** This flag is not supported.</span></span>

<span data-ttu-id="ecc71-165">**Version :** Nécessite Internet Explorer 7,0.</span><span class="sxs-lookup"><span data-stu-id="ecc71-165">**Version:** Requires Internet Explorer 7.0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-166"><span id="INTERNET_OPTION_CODEPAGE_EXTRA"></span><span id="internet_option_codepage_extra"></span>**page de codes de l' \_ option Internet \_ \_ extra**</span><span class="sxs-lookup"><span data-stu-id="ecc71-166"><span id="INTERNET_OPTION_CODEPAGE_EXTRA"></span><span id="internet_option_codepage_extra"></span>**INTERNET\_OPTION\_CODEPAGE\_EXTRA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-167">101</span><span class="sxs-lookup"><span data-stu-id="ecc71-167">101</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-168">Par défaut, la partie chemin d’accès de l’URL est la page de codes système par défaut (CP \_ ACP).</span><span class="sxs-lookup"><span data-stu-id="ecc71-168">By default, the path portion of the URL is the default system code page (CP\_ACP).</span></span> <span data-ttu-id="ecc71-169">Caractère d’échappement (%) les conversions ne sont pas effectuées sur la partie supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="ecc71-169">The escape character (%) conversions are not performed on the extra portion.</span></span> <span data-ttu-id="ecc71-170">La définition de cette option sur la demande ou sur le descripteur de connexion désactive le \_ codage ACP ACP.</span><span class="sxs-lookup"><span data-stu-id="ecc71-170">Setting this option on the request, or connection handle disables the CP\_ACP encoding.</span></span> <span data-ttu-id="ecc71-171">Le paramètre *lpBuffer* dans l’appel à [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) contient la page de codes DBCS souhaitée pour la partie supplémentaire de l’URL.</span><span class="sxs-lookup"><span data-stu-id="ecc71-171">The *lpBuffer* parameter in the call to [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) contains the desired DBCS codepage for the extra portion of the URL.</span></span> <span data-ttu-id="ecc71-172">Si aucune page de codes n’est spécifiée dans *lpBuffer*, Wininet utilise la page de codes système par défaut (CP \_ ACP).</span><span class="sxs-lookup"><span data-stu-id="ecc71-172">If no code page is specified in *lpBuffer*, WinINet uses the default system code page (CP\_ACP).</span></span>

<span data-ttu-id="ecc71-173">**Windows XP avec SP2 et Windows Server 2003 avec SP1 :** Cet indicateur n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="ecc71-173">**Windows XP with SP2 and Windows Server 2003 with SP1:** This flag is not supported.</span></span>

<span data-ttu-id="ecc71-174">**Version :** Nécessite Internet Explorer 7,0.</span><span class="sxs-lookup"><span data-stu-id="ecc71-174">**Version:** Requires Internet Explorer 7.0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-175"><span id="INTERNET_OPTION_COMPRESSED_CONTENT_LENGTH_"></span><span id="internet_option_compressed_content_length_"></span>**\_longueur du \_ \_ contenu compressé des options \_ Internet**</span><span class="sxs-lookup"><span data-stu-id="ecc71-175"><span id="INTERNET_OPTION_COMPRESSED_CONTENT_LENGTH_"></span><span id="internet_option_compressed_content_length_"></span>**INTERNET\_OPTION\_COMPRESSED\_CONTENT\_LENGTH**</span></span> 
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-176">147</span><span class="sxs-lookup"><span data-stu-id="ecc71-176">147</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-177">Pour une demande dans laquelle WinInet décompresse l’encodage de contenu fourni par le serveur, récupère la longueur de contenu signalée par le serveur du corps de la réponse en tant que ULONGLONG.</span><span class="sxs-lookup"><span data-stu-id="ecc71-177">For a request where WinInet decompressed the server s supplied Content-Encoding, retrieves the server-reported Content-Length of the response body as a ULONGLONG.</span></span> <span data-ttu-id="ecc71-178">Pris en charge dans Windows 10, version 1507 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ecc71-178">Supported in Windows 10, version 1507 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-179"><span id="INTERNET_OPTION_CONNECT_BACKOFF"></span><span id="internet_option_connect_backoff"></span>**\_option Internet \_ connexion-interruption \_**</span><span class="sxs-lookup"><span data-stu-id="ecc71-179"><span id="INTERNET_OPTION_CONNECT_BACKOFF"></span><span id="internet_option_connect_backoff"></span>**INTERNET\_OPTION\_CONNECT\_BACKOFF**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-180">4</span><span class="sxs-lookup"><span data-stu-id="ecc71-180">4</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-181">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="ecc71-181">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-182"><span id="INTERNET_OPTION_CONNECT_RETRIES"></span><span id="internet_option_connect_retries"></span>**\_ \_ nouvelles tentatives de connexion des options Internet \_**</span><span class="sxs-lookup"><span data-stu-id="ecc71-182"><span id="INTERNET_OPTION_CONNECT_RETRIES"></span><span id="internet_option_connect_retries"></span>**INTERNET\_OPTION\_CONNECT\_RETRIES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-183">3</span><span class="sxs-lookup"><span data-stu-id="ecc71-183">3</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-184">Définit ou récupère une valeur d’entier long non signé qui contient le nombre de fois que WinINet tente de résoudre et de se connecter à un hôte.</span><span class="sxs-lookup"><span data-stu-id="ecc71-184">Sets or retrieves an unsigned long integer value that contains the number of times WinINet attempts to resolve and connect to a host.</span></span> <span data-ttu-id="ecc71-185">Elle tente une seule fois par adresse IP.</span><span class="sxs-lookup"><span data-stu-id="ecc71-185">It only attempts once per IP address.</span></span> <span data-ttu-id="ecc71-186">Par exemple, si vous tentez de vous connecter à un hôte à hébergement multiple qui possède dix adresses IP et que \_ les nouvelles tentatives de connexion d’option Internet ont \_ \_ la valeur 7, Wininet tente uniquement de résoudre les sept premières adresses IP et de s’y connecter.</span><span class="sxs-lookup"><span data-stu-id="ecc71-186">For example, if you attempt to connect to a multihome host that has ten IP addresses and INTERNET\_OPTION\_CONNECT\_RETRIES is set to seven, WinINet only attempts to resolve and connect to the first seven IP addresses.</span></span> <span data-ttu-id="ecc71-187">À l’inverse, étant donné le même ensemble de dix adresses IP, si l' \_ option Internet \_ Connect \_ tentativess est définie sur 20, Wininet tente chacune des dix une seule fois.</span><span class="sxs-lookup"><span data-stu-id="ecc71-187">Conversely, given the same set of ten IP addresses, if INTERNET\_OPTION\_CONNECT\_RETRIES is set to 20, WinINet attempts each of the ten only once.</span></span> <span data-ttu-id="ecc71-188">Si un ordinateur hôte n’a qu’une seule adresse IP et que la première tentative de connexion échoue, il n’y a pas d’autres tentatives.</span><span class="sxs-lookup"><span data-stu-id="ecc71-188">If a host has only one IP address and the first connection attempt fails, there are no further attempts.</span></span> <span data-ttu-id="ecc71-189">Si une tentative de connexion échoue encore après le nombre de tentatives spécifié, la demande est annulée.</span><span class="sxs-lookup"><span data-stu-id="ecc71-189">If a connection attempt still fails after the specified number of attempts, the request is canceled.</span></span> <span data-ttu-id="ecc71-190">La valeur par défaut pour \_ les \_ nouvelles tentatives de connexion des options Internet est de \_ cinq tentatives.</span><span class="sxs-lookup"><span data-stu-id="ecc71-190">The default value for INTERNET\_OPTION\_CONNECT\_RETRIES is five attempts.</span></span> <span data-ttu-id="ecc71-191">Cette option peut être utilisée sur n’importe quel handle [**HINTERNET**](appendix-a-hinternet-handles.md) , y compris un handle **null** .</span><span class="sxs-lookup"><span data-stu-id="ecc71-191">This option can be used on any [**HINTERNET**](appendix-a-hinternet-handles.md) handle, including a **NULL** handle.</span></span> <span data-ttu-id="ecc71-192">Elle est utilisée par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) et [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="ecc71-192">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-193"><span id="INTERNET_OPTION_CONNECT_TIME"></span><span id="internet_option_connect_time"></span>**heure de connexion de l' \_ option Internet \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ecc71-193"><span id="INTERNET_OPTION_CONNECT_TIME"></span><span id="internet_option_connect_time"></span>**INTERNET\_OPTION\_CONNECT\_TIME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-194">55</span><span class="sxs-lookup"><span data-stu-id="ecc71-194">55</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-195">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="ecc71-195">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-196"><span id="INTERNET_OPTION_CONNECT_TIMEOUT"></span><span id="internet_option_connect_timeout"></span>**\_ \_ délai d’attente de connexion des options Internet \_**</span><span class="sxs-lookup"><span data-stu-id="ecc71-196"><span id="INTERNET_OPTION_CONNECT_TIMEOUT"></span><span id="internet_option_connect_timeout"></span>**INTERNET\_OPTION\_CONNECT\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-197">2</span><span class="sxs-lookup"><span data-stu-id="ecc71-197">2</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-198">Définit ou récupère une valeur d’entier long non signé qui contient la valeur du délai d’attente, en millisecondes, à utiliser pour les demandes de connexion Internet.</span><span class="sxs-lookup"><span data-stu-id="ecc71-198">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to use for Internet connection requests.</span></span> <span data-ttu-id="ecc71-199">La définition de cette option sur Infinite (0xFFFFFFFF) désactive ce minuteur.</span><span class="sxs-lookup"><span data-stu-id="ecc71-199">Setting this option to infinite (0xFFFFFFFF) will disable this timer.</span></span>

<span data-ttu-id="ecc71-200">Si une demande de connexion prend plus de temps que cette valeur de délai d’attente, la demande est annulée.</span><span class="sxs-lookup"><span data-stu-id="ecc71-200">If a connection request takes longer than this time-out value, the request is canceled.</span></span> <span data-ttu-id="ecc71-201">Lorsque vous tentez de vous connecter à plusieurs adresses IP pour un seul hôte (un hôte multirésident), le délai d’expiration est cumulatif pour toutes les adresses IP.</span><span class="sxs-lookup"><span data-stu-id="ecc71-201">When attempting to connect to multiple IP addresses for a single host (a multihome host), the timeout limit is cumulative for all of the IP addresses.</span></span> <span data-ttu-id="ecc71-202">Cette option peut être utilisée sur n’importe quel handle [**HINTERNET**](appendix-a-hinternet-handles.md) , y compris un handle **null** .</span><span class="sxs-lookup"><span data-stu-id="ecc71-202">This option can be used on any [**HINTERNET**](appendix-a-hinternet-handles.md) handle, including a **NULL** handle.</span></span> <span data-ttu-id="ecc71-203">Elle est utilisée par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) et [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="ecc71-203">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-204"><span id="INTERNET_OPTION_CONNECTED_STATE"></span><span id="internet_option_connected_state"></span>**\_ \_ état connecté de l’option Internet \_**</span><span class="sxs-lookup"><span data-stu-id="ecc71-204"><span id="INTERNET_OPTION_CONNECTED_STATE"></span><span id="internet_option_connected_state"></span>**INTERNET\_OPTION\_CONNECTED\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-205">50</span><span class="sxs-lookup"><span data-stu-id="ecc71-205">50</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-206">Définit ou récupère une valeur d’entier long non signé qui contient l’état connecté.</span><span class="sxs-lookup"><span data-stu-id="ecc71-206">Sets or retrieves an unsigned long integer value that contains the connected state.</span></span> <span data-ttu-id="ecc71-207">Utilisé par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) et [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="ecc71-207">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-208"><span id="INTERNET_OPTION_CONTEXT_VALUE"></span><span id="internet_option_context_value"></span>**valeur de contexte de l' \_ option Internet \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ecc71-208"><span id="INTERNET_OPTION_CONTEXT_VALUE"></span><span id="internet_option_context_value"></span>**INTERNET\_OPTION\_CONTEXT\_VALUE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-209">45</span><span class="sxs-lookup"><span data-stu-id="ecc71-209">45</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-210">Définit ou récupère un PTR DWORD \_ qui contient l’adresse de la valeur de contexte associée à ce handle [**HINTERNET**](appendix-a-hinternet-handles.md) .</span><span class="sxs-lookup"><span data-stu-id="ecc71-210">Sets or retrieves a DWORD\_PTR that contains the address of the context value associated with this [**HINTERNET**](appendix-a-hinternet-handles.md) handle.</span></span> <span data-ttu-id="ecc71-211">Cette option peut être utilisée sur n’importe quel handle [**HINTERNET**](appendix-a-hinternet-handles.md) .</span><span class="sxs-lookup"><span data-stu-id="ecc71-211">This option can be used on any [**HINTERNET**](appendix-a-hinternet-handles.md) handle.</span></span> <span data-ttu-id="ecc71-212">Utilisé par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) et [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="ecc71-212">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="ecc71-213">Précédemment, cette valeur définit la valeur de contexte sur l’adresse stockée dans le pointeur **lpBuffer** .</span><span class="sxs-lookup"><span data-stu-id="ecc71-213">Previously, this set the context value to the address stored in the **lpBuffer** pointer.</span></span> <span data-ttu-id="ecc71-214">Cela a été corrigé afin que la valeur stockée dans la mémoire tampon soit utilisée et que l’indicateur de [ \_ valeur de \_ contexte \_ d’option Internet](/windows) se voit attribuer une nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="ecc71-214">This has been corrected so that the value stored in the buffer is used and the [INTERNET\_OPTION\_CONTEXT\_VALUE](/windows) flag is assigned a new value.</span></span> <span data-ttu-id="ecc71-215">L’ancienne valeur, 10, a été conservée afin que les applications écrites pour l’ancien comportement soient toujours prises en charge.</span><span class="sxs-lookup"><span data-stu-id="ecc71-215">The old value, 10, has been preserved so that applications written for the old behavior are still supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-216"><span id="INTERNET_OPTION_CONTROL_RECEIVE_TIMEOUT"></span><span id="internet_option_control_receive_timeout"></span>**\_délai de \_ \_ réception du contrôle \_ d’option Internet**</span><span class="sxs-lookup"><span data-stu-id="ecc71-216"><span id="INTERNET_OPTION_CONTROL_RECEIVE_TIMEOUT"></span><span id="internet_option_control_receive_timeout"></span>**INTERNET\_OPTION\_CONTROL\_RECEIVE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-217">6</span><span class="sxs-lookup"><span data-stu-id="ecc71-217">6</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-218">Identique au [ \_ \_ \_ délai d’attente de réception des options Internet](/windows).</span><span class="sxs-lookup"><span data-stu-id="ecc71-218">Identical to [INTERNET\_OPTION\_RECEIVE\_TIMEOUT](/windows).</span></span> <span data-ttu-id="ecc71-219">Utilisé par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) et [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="ecc71-219">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-220"><span id="INTERNET_OPTION_CONTROL_SEND_TIMEOUT"></span><span id="internet_option_control_send_timeout"></span>**\_ \_ \_ \_ délai d’attente d’envoi du contrôle d’option Internet**</span><span class="sxs-lookup"><span data-stu-id="ecc71-220"><span id="INTERNET_OPTION_CONTROL_SEND_TIMEOUT"></span><span id="internet_option_control_send_timeout"></span>**INTERNET\_OPTION\_CONTROL\_SEND\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-221">5</span><span class="sxs-lookup"><span data-stu-id="ecc71-221">5</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-222">Identique au [ \_ \_ \_ délai d’attente d’envoi des options Internet](/windows).</span><span class="sxs-lookup"><span data-stu-id="ecc71-222">Identical to [INTERNET\_OPTION\_SEND\_TIMEOUT](/windows).</span></span> <span data-ttu-id="ecc71-223">Utilisé par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) et [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="ecc71-223">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-224"><span id="INTERNET_OPTION_DATA_RECEIVE_TIMEOUT"></span><span id="internet_option_data_receive_timeout"></span>**\_délai de \_ réception des données des options Internet \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ecc71-224"><span id="INTERNET_OPTION_DATA_RECEIVE_TIMEOUT"></span><span id="internet_option_data_receive_timeout"></span>**INTERNET\_OPTION\_DATA\_RECEIVE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-225">8</span><span class="sxs-lookup"><span data-stu-id="ecc71-225">8</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-226">Définit ou récupère une valeur d’entier long non signé qui contient la valeur du délai d’attente, en millisecondes, pour recevoir une réponse à une demande pour le canal de données d’une transaction FTP.</span><span class="sxs-lookup"><span data-stu-id="ecc71-226">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to receive a response to a request for the data channel of an FTP transaction.</span></span> <span data-ttu-id="ecc71-227">Si la réponse prend plus de temps que cette valeur de délai d’attente, la demande est annulée.</span><span class="sxs-lookup"><span data-stu-id="ecc71-227">If the response takes longer than this time-out value, the request is canceled.</span></span> <span data-ttu-id="ecc71-228">Cette option peut être utilisée sur n’importe quel handle [**HINTERNET**](appendix-a-hinternet-handles.md) , y compris un handle **null** .</span><span class="sxs-lookup"><span data-stu-id="ecc71-228">This option can be used on any [**HINTERNET**](appendix-a-hinternet-handles.md) handle, including a **NULL** handle.</span></span> <span data-ttu-id="ecc71-229">Elle est utilisée par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) et [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="ecc71-229">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>

<span data-ttu-id="ecc71-230">Cet indicateur n’a aucun impact sur la fonctionnalité HTTP.</span><span class="sxs-lookup"><span data-stu-id="ecc71-230">This flag has no impact on HTTP functionality.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-231"><span id="INTERNET_OPTION_DATA_SEND_TIMEOUT"></span><span id="internet_option_data_send_timeout"></span>**\_ \_ \_ délai d’envoi des données des options Internet \_**</span><span class="sxs-lookup"><span data-stu-id="ecc71-231"><span id="INTERNET_OPTION_DATA_SEND_TIMEOUT"></span><span id="internet_option_data_send_timeout"></span>**INTERNET\_OPTION\_DATA\_SEND\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-232">7</span><span class="sxs-lookup"><span data-stu-id="ecc71-232">7</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-233">Définit ou récupère une valeur d’entier long non signé, en millisecondes, qui contient la valeur du délai d’attente pour envoyer une demande pour le canal de données d’une transaction FTP.</span><span class="sxs-lookup"><span data-stu-id="ecc71-233">Sets or retrieves an unsigned long integer value, in milliseconds, that contains the time-out value to send a request for the data channel of an FTP transaction.</span></span> <span data-ttu-id="ecc71-234">Si l’envoi prend plus de temps que cette valeur de délai d’attente, l’envoi est annulé.</span><span class="sxs-lookup"><span data-stu-id="ecc71-234">If the send takes longer than this time-out value, the send is canceled.</span></span> <span data-ttu-id="ecc71-235">Cette option peut être utilisée sur n’importe quel handle [**HINTERNET**](appendix-a-hinternet-handles.md) , y compris un handle **null** .</span><span class="sxs-lookup"><span data-stu-id="ecc71-235">This option can be used on any [**HINTERNET**](appendix-a-hinternet-handles.md) handle, including a **NULL** handle.</span></span> <span data-ttu-id="ecc71-236">Elle est utilisée par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) et [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="ecc71-236">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>

<span data-ttu-id="ecc71-237">Cet indicateur n’a aucun impact sur la fonctionnalité HTTP.</span><span class="sxs-lookup"><span data-stu-id="ecc71-237">This flag has no impact on HTTP functionality.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-238"><span id="INTERNET_OPTION_DATAFILE_NAME"></span><span id="internet_option_datafile_name"></span>**\_nom du \_ fichier de fichier de l’option Internet \_**</span><span class="sxs-lookup"><span data-stu-id="ecc71-238"><span id="INTERNET_OPTION_DATAFILE_NAME"></span><span id="internet_option_datafile_name"></span>**INTERNET\_OPTION\_DATAFILE\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-239">33</span><span class="sxs-lookup"><span data-stu-id="ecc71-239">33</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-240">Récupère une valeur de chaîne qui contient le nom du fichier qui stocke une entité téléchargée.</span><span class="sxs-lookup"><span data-stu-id="ecc71-240">Retrieves a string value that contains the name of the file backing a downloaded entity.</span></span> <span data-ttu-id="ecc71-241">Cet indicateur est valide après la fin de [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)ou [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) .</span><span class="sxs-lookup"><span data-stu-id="ecc71-241">This flag is valid after [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea), or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) has completed.</span></span> <span data-ttu-id="ecc71-242">Cette option ne peut être interrogée que par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="ecc71-242">This option can only be queried by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-243"><span id="INTERNET_OPTION_DATAFILE_EXT"></span><span id="internet_option_datafile_ext"></span>**\_extension du \_ fichier de fichier de l’option Internet \_**</span><span class="sxs-lookup"><span data-stu-id="ecc71-243"><span id="INTERNET_OPTION_DATAFILE_EXT"></span><span id="internet_option_datafile_ext"></span>**INTERNET\_OPTION\_DATAFILE\_EXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-244">96</span><span class="sxs-lookup"><span data-stu-id="ecc71-244">96</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-245">Définit une valeur de chaîne qui contient l’extension du fichier qui stocke une entité téléchargée.</span><span class="sxs-lookup"><span data-stu-id="ecc71-245">Sets a string value that contains the extension of the file backing a downloaded entity.</span></span> <span data-ttu-id="ecc71-246">Cet indicateur doit être défini avant d’appeler [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)ou [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span><span class="sxs-lookup"><span data-stu-id="ecc71-246">This flag should be set before calling [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea), or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span> <span data-ttu-id="ecc71-247">Cette option peut uniquement être définie par [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="ecc71-247">This option can only be set by [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-248"><span id="INTERNET_OPTION_DIAGNOSTIC_SOCKET_INFO"></span><span id="internet_option_diagnostic_socket_info"></span>**\_ \_ \_ informations sur le socket de diagnostic des options Internet \_**</span><span class="sxs-lookup"><span data-stu-id="ecc71-248"><span id="INTERNET_OPTION_DIAGNOSTIC_SOCKET_INFO"></span><span id="internet_option_diagnostic_socket_info"></span>**INTERNET\_OPTION\_DIAGNOSTIC\_SOCKET\_INFO**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-249">67</span><span class="sxs-lookup"><span data-stu-id="ecc71-249">67</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-250">Récupère une structure [**d' \_ \_ \_ informations de socket de diagnostic Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_diagnostic_socket_info) qui contient les données relatives à une requête http spécifiée.</span><span class="sxs-lookup"><span data-stu-id="ecc71-250">Retrieves an [**INTERNET\_DIAGNOSTIC\_SOCKET\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_diagnostic_socket_info) structure that contains data about a specified HTTP Request.</span></span> <span data-ttu-id="ecc71-251">Cet indicateur est utilisé par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="ecc71-251">This flag is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

<span data-ttu-id="ecc71-252">**Windows 7 :** Cette option n’est plus prise en charge.</span><span class="sxs-lookup"><span data-stu-id="ecc71-252">**Windows 7:** This option is no longer supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-253"><span id="INTERNET_OPTION_DIGEST_AUTH_UNLOAD"></span><span id="internet_option_digest_auth_unload"></span>**\_option Internet \_ Digest \_ auth \_ Unload**</span><span class="sxs-lookup"><span data-stu-id="ecc71-253"><span id="INTERNET_OPTION_DIGEST_AUTH_UNLOAD"></span><span id="internet_option_digest_auth_unload"></span>**INTERNET\_OPTION\_DIGEST\_AUTH\_UNLOAD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-254">76</span><span class="sxs-lookup"><span data-stu-id="ecc71-254">76</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-255">Fait en sorte que le système se déconnecte du package SSPI d’authentification Digest, en vidant toutes les informations d’identification créées pour le processus.</span><span class="sxs-lookup"><span data-stu-id="ecc71-255">Causes the system to log off the Digest authentication SSPI package, purging all of the credentials created for the process.</span></span> <span data-ttu-id="ecc71-256">Aucune mémoire tampon n’est requise pour cette option.</span><span class="sxs-lookup"><span data-stu-id="ecc71-256">No buffer is required for this option.</span></span> <span data-ttu-id="ecc71-257">Elle est utilisée par [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="ecc71-257">It is used by [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-258"><span id="INTERNET_OPTION_DISABLE_AUTODIAL"></span><span id="internet_option_disable_autodial"></span>**\_option Internet \_ désactiver la \_ numérotation automatique**</span><span class="sxs-lookup"><span data-stu-id="ecc71-258"><span id="INTERNET_OPTION_DISABLE_AUTODIAL"></span><span id="internet_option_disable_autodial"></span>**INTERNET\_OPTION\_DISABLE\_AUTODIAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-259">70</span><span class="sxs-lookup"><span data-stu-id="ecc71-259">70</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-260">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="ecc71-260">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-261"><span id="INTERNET_OPTION_DISCONNECTED_TIMEOUT"></span><span id="internet_option_disconnected_timeout"></span>**\_délai d’attente de l’option Internet \_ déconnectée \_**</span><span class="sxs-lookup"><span data-stu-id="ecc71-261"><span id="INTERNET_OPTION_DISCONNECTED_TIMEOUT"></span><span id="internet_option_disconnected_timeout"></span>**INTERNET\_OPTION\_DISCONNECTED\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-262">49</span><span class="sxs-lookup"><span data-stu-id="ecc71-262">49</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-263">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="ecc71-263">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-264"><span id="INTERNET_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="internet_option_enable_http_protocol"></span>**\_option Internet \_ activer \_ le \_ protocole http**</span><span class="sxs-lookup"><span data-stu-id="ecc71-264"><span id="INTERNET_OPTION_ENABLE_HTTP_PROTOCOL"></span><span id="internet_option_enable_http_protocol"></span>**INTERNET\_OPTION\_ENABLE\_HTTP\_PROTOCOL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-265">148</span><span class="sxs-lookup"><span data-stu-id="ecc71-265">148</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-266">Définit un masque de réinitialisation DWORD des versions HTTP avancées acceptables.</span><span class="sxs-lookup"><span data-stu-id="ecc71-266">Sets a DWORD bitmask of acceptable advanced HTTP versions.</span></span> <span data-ttu-id="ecc71-267">Peut être défini sur n’importe quel type de handle.</span><span class="sxs-lookup"><span data-stu-id="ecc71-267">May be set on any handle type.</span></span> <span data-ttu-id="ecc71-268">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="ecc71-268">Possible values are:</span></span>

-   <span data-ttu-id="ecc71-269">\_ \_ Indicateur de protocole http \_ http2 (0X2).</span><span class="sxs-lookup"><span data-stu-id="ecc71-269">HTTP\_PROTOCOL\_FLAG\_HTTP2 (0x2).</span></span> <span data-ttu-id="ecc71-270">Pris en charge sur Windows 10, version 1507 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ecc71-270">Supported on Windows 10, version 1507 and later.</span></span>

<span data-ttu-id="ecc71-271">Les versions héritées de HTTP (1,1 et versions antérieures) ne peuvent pas être désactivées à l’aide de cette option.</span><span class="sxs-lookup"><span data-stu-id="ecc71-271">Legacy versions of HTTP (1.1 and prior) cannot be disabled using this option.</span></span> <span data-ttu-id="ecc71-272">La valeur par défaut est 0x0.</span><span class="sxs-lookup"><span data-stu-id="ecc71-272">The default is 0x0.</span></span> <span data-ttu-id="ecc71-273">Pris en charge dans Windows 10, version 1507 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ecc71-273">Supported in Windows 10, version 1507 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-274"><span id="INTERNET_OPTION_ENABLE_REDIRECT_CACHE_READ"></span><span id="internet_option_enable_redirect_cache_read"></span>**\_option Internet \_ activer \_ la \_ lecture du cache de redirection \_**</span><span class="sxs-lookup"><span data-stu-id="ecc71-274"><span id="INTERNET_OPTION_ENABLE_REDIRECT_CACHE_READ"></span><span id="internet_option_enable_redirect_cache_read"></span>**INTERNET\_OPTION\_ENABLE\_REDIRECT\_CACHE\_READ**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-275">122</span><span class="sxs-lookup"><span data-stu-id="ecc71-275">122</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-276">Sur un handle de demande, définit un booléen qui contrôle si les redirections sont retournées à partir du cache WinInet pour une demande donnée.</span><span class="sxs-lookup"><span data-stu-id="ecc71-276">On a request handle, sets a Boolean controlling whether redirects will be returned from the WinInet cache for a given request.</span></span> <span data-ttu-id="ecc71-277">La valeur par défaut est FALSE.</span><span class="sxs-lookup"><span data-stu-id="ecc71-277">The default is FALSE.</span></span> <span data-ttu-id="ecc71-278">Pris en charge dans Windows 8 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ecc71-278">Supported in Windows 8 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-279"><span id="INTERNET_OPTION_ENCODE_EXTRA"></span><span id="internet_option_encode_extra"></span>**\_option Internet \_ coder \_ extra**</span><span class="sxs-lookup"><span data-stu-id="ecc71-279"><span id="INTERNET_OPTION_ENCODE_EXTRA"></span><span id="internet_option_encode_extra"></span>**INTERNET\_OPTION\_ENCODE\_EXTRA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-280">155</span><span class="sxs-lookup"><span data-stu-id="ecc71-280">155</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-281">Obtient/définit une valeur BOOLÉENNE indiquant si les caractères non-ASCII de la chaîne de requête doivent être encodés en pourcentage.</span><span class="sxs-lookup"><span data-stu-id="ecc71-281">Gets/sets a BOOL indicating whether non-ASCII characters in the query string should be percent-encoded.</span></span> <span data-ttu-id="ecc71-282">La valeur par défaut est FALSE.</span><span class="sxs-lookup"><span data-stu-id="ecc71-282">The default is FALSE.</span></span> <span data-ttu-id="ecc71-283">Pris en charge dans Windows 8.1 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ecc71-283">Supported in Windows 8.1 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-284"><span id="INTERNET_OPTION_END_BROWSER_SESSION"></span><span id="internet_option_end_browser_session"></span>**\_option Internet \_ fin \_ de \_ session du navigateur**</span><span class="sxs-lookup"><span data-stu-id="ecc71-284"><span id="INTERNET_OPTION_END_BROWSER_SESSION"></span><span id="internet_option_end_browser_session"></span>**INTERNET\_OPTION\_END\_BROWSER\_SESSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-285">42</span><span class="sxs-lookup"><span data-stu-id="ecc71-285">42</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-286">Vide les entrées qui ne sont pas utilisées à partir du cache de mot de passe sur le disque dur.</span><span class="sxs-lookup"><span data-stu-id="ecc71-286">Flushes entries not in use from the password cache on the hard disk drive.</span></span> <span data-ttu-id="ecc71-287">Réinitialise également le temps de cache utilisé lorsque le mode de synchronisation est une fois par session.</span><span class="sxs-lookup"><span data-stu-id="ecc71-287">Also resets the cache time used when the synchronization mode is once-per-session.</span></span> <span data-ttu-id="ecc71-288">Aucune mémoire tampon n’est requise pour cette option.</span><span class="sxs-lookup"><span data-stu-id="ecc71-288">No buffer is required for this option.</span></span> <span data-ttu-id="ecc71-289">Utilisé par [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="ecc71-289">This is used by [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-290"><span id="INTERNET_OPTION_ERROR_MASK"></span><span id="internet_option_error_mask"></span>**\_masque d' \_ erreur des options Internet \_**</span><span class="sxs-lookup"><span data-stu-id="ecc71-290"><span id="INTERNET_OPTION_ERROR_MASK"></span><span id="internet_option_error_mask"></span>**INTERNET\_OPTION\_ERROR\_MASK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-291">62</span><span class="sxs-lookup"><span data-stu-id="ecc71-291">62</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-292">Définit une valeur d’entier long non signé qui contient les masques d’erreur qui peuvent être gérés par l’application cliente.</span><span class="sxs-lookup"><span data-stu-id="ecc71-292">Sets an unsigned long integer value that contains the error masks that can be handled by the client application.</span></span> <span data-ttu-id="ecc71-293">Il peut s’agir d’une combinaison des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="ecc71-293">This can be a combination of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="ecc71-294"><span id="INTERNET_ERROR_MASK_COMBINED_SEC_CERT"></span><span id="internet_error_mask_combined_sec_cert"></span>\_ \_ \_ \_ certificat sec combiné au masque d’erreurs Internet \_</span><span class="sxs-lookup"><span data-stu-id="ecc71-294"><span id="INTERNET_ERROR_MASK_COMBINED_SEC_CERT"></span><span id="internet_error_mask_combined_sec_cert"></span>INTERNET\_ERROR\_MASK\_COMBINED\_SEC\_CERT</span></span>
</dt> <dd>

<span data-ttu-id="ecc71-295">0x2</span><span class="sxs-lookup"><span data-stu-id="ecc71-295">0x2</span></span>

<span data-ttu-id="ecc71-296">Indique que toutes les erreurs de certificat doivent être signalées à l’aide du même retour d’erreur, à savoir les **\_ Erreurs de certificat Error Internet \_ s \_ \_**.</span><span class="sxs-lookup"><span data-stu-id="ecc71-296">Indicates that all certificate errors are to be reported using the same error return, namely **ERROR\_INTERNET\_SEC\_CERT\_ERRORS**.</span></span> <span data-ttu-id="ecc71-297">Si cet indicateur est défini, appelez **InternetErrorDlg** lors de la réception de l’erreur erreur **\_ Internet \_ s \_ CERT \_** Errors, afin que l’utilisateur puisse répondre à une boîte de dialogue familière décrivant le problème.</span><span class="sxs-lookup"><span data-stu-id="ecc71-297">If this flag is set, call **InternetErrorDlg** upon receiving the **ERROR\_INTERNET\_SEC\_CERT\_ERRORS** error, so that the user can respond to a familiar dialog describing the problem.</span></span>

> [!Caution]  
> <span data-ttu-id="ecc71-298">Le fait de ne pas informer l’utilisateur de cette erreur expose l’utilisateur à des attaques d’usurpation d’identité potentielles.</span><span class="sxs-lookup"><span data-stu-id="ecc71-298">Failing to inform the user of this error exposes the user to potential spoofing attacks.</span></span>

 

</dd> <dt>

<span data-ttu-id="ecc71-299"><span id="INTERNET_ERROR_MASK_INSERT_CDROM"></span><span id="internet_error_mask_insert_cdrom"></span>masque d’erreur INTERNET- \_ \_ Insérer un CD- \_ \_ ROM</span><span class="sxs-lookup"><span data-stu-id="ecc71-299"><span id="INTERNET_ERROR_MASK_INSERT_CDROM"></span><span id="internet_error_mask_insert_cdrom"></span>INTERNET\_ERROR\_MASK\_INSERT\_CDROM</span></span>
</dt> <dd>

<span data-ttu-id="ecc71-300">0x1</span><span class="sxs-lookup"><span data-stu-id="ecc71-300">0x1</span></span>

<span data-ttu-id="ecc71-301">Indique que l’application cliente peut gérer le code d’erreur d’insertion dans le **\_ \_ \_ cdrom Internet** .</span><span class="sxs-lookup"><span data-stu-id="ecc71-301">Indicates that the client application can handle the **ERROR\_INTERNET\_INSERT\_CDROM** error code.</span></span>

</dd> <dt>

<span data-ttu-id="ecc71-302"><span id="INTERNET_ERROR_MASK_LOGIN_FAILURE_DISPLAY_ENTITY_BODY"></span><span id="internet_error_mask_login_failure_display_entity_body"></span>échec de connexion au masque d’erreur INTERNET afficher le corps de l' \_ \_ \_ \_ \_ \_ entité \_</span><span class="sxs-lookup"><span data-stu-id="ecc71-302"><span id="INTERNET_ERROR_MASK_LOGIN_FAILURE_DISPLAY_ENTITY_BODY"></span><span id="internet_error_mask_login_failure_display_entity_body"></span>INTERNET\_ERROR\_MASK\_LOGIN\_FAILURE\_DISPLAY\_ENTITY\_BODY</span></span>
</dt> <dd>

<span data-ttu-id="ecc71-303">0x8</span><span class="sxs-lookup"><span data-stu-id="ecc71-303">0x8</span></span>

<span data-ttu-id="ecc71-304">Indique que l’application cliente peut gérer l' **erreur Échec de la connexion Internet afficher le code d’erreur \_ \_ \_ \_ \_ \_ du corps** de l’entité.</span><span class="sxs-lookup"><span data-stu-id="ecc71-304">Indicates that the client application can handle the **ERROR\_INTERNET\_LOGIN\_FAILURE\_DISPLAY\_ENTITY\_BODY** error code.</span></span>

</dd> <dt>

<span data-ttu-id="ecc71-305"><span id="INTERNET_ERROR_MASK_NEED_MSN_SSPI_PKG"></span><span id="internet_error_mask_need_msn_sspi_pkg"></span>le \_ masque d’erreurs Internet a \_ besoin de \_ \_ MSN \_ SSPI \_ pkg</span><span class="sxs-lookup"><span data-stu-id="ecc71-305"><span id="INTERNET_ERROR_MASK_NEED_MSN_SSPI_PKG"></span><span id="internet_error_mask_need_msn_sspi_pkg"></span>INTERNET\_ERROR\_MASK\_NEED\_MSN\_SSPI\_PKG</span></span>
</dt> <dd>

<span data-ttu-id="ecc71-306">0x4</span><span class="sxs-lookup"><span data-stu-id="ecc71-306">0x4</span></span>

<span data-ttu-id="ecc71-307">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="ecc71-307">Not implemented.</span></span>

</dd> </dl>

</dl> </dd> <dt>

<span data-ttu-id="ecc71-308"><span id="INTERNET_OPTION_ENTERPRISE_CONTEXT"></span><span id="internet_option_enterprise_context"></span>**\_contexte d' \_ entreprise \_ option Internet**</span><span class="sxs-lookup"><span data-stu-id="ecc71-308"><span id="INTERNET_OPTION_ENTERPRISE_CONTEXT"></span><span id="internet_option_enterprise_context"></span>**INTERNET\_OPTION\_ENTERPRISE\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-309">159</span><span class="sxs-lookup"><span data-stu-id="ecc71-309">159</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-310">Définit un PWSTR contenant l’ID d’entreprise (voir https://msdn.microsoft.com/library/windows/desktop/mt759320(v=vs.85).aspx) qui s’applique à la demande.</span><span class="sxs-lookup"><span data-stu-id="ecc71-310">Sets a PWSTR containing the Enterprise ID (see https://msdn.microsoft.com/library/windows/desktop/mt759320(v=vs.85).aspx) which applies to the request.</span></span> <span data-ttu-id="ecc71-311">Pris en charge dans Windows 10, version 1507 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ecc71-311">Supported in Windows 10, version 1507 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-312"><span id="INTERNET_OPTION_EXTENDED_ERROR"></span><span id="internet_option_extended_error"></span>**\_ \_ erreur étendue de l’option Internet \_**</span><span class="sxs-lookup"><span data-stu-id="ecc71-312"><span id="INTERNET_OPTION_EXTENDED_ERROR"></span><span id="internet_option_extended_error"></span>**INTERNET\_OPTION\_EXTENDED\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-313">24</span><span class="sxs-lookup"><span data-stu-id="ecc71-313">24</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-314">Récupère une valeur d’entier long non signé qui contient un code d’erreur Winsock mappé à l’erreur messages d’erreur **\_ Internet \_** retournés dans ce contexte de thread.</span><span class="sxs-lookup"><span data-stu-id="ecc71-314">Retrieves an unsigned long integer value that contains a Winsock error code mapped to the **ERROR\_INTERNET\_** error messages last returned in this thread context.</span></span> <span data-ttu-id="ecc71-315">Cette option est utilisée sur un handle [**HINTERNET**](appendix-a-hinternet-handles.md) **null** par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="ecc71-315">This option is used on a **NULL**[**HINTERNET**](appendix-a-hinternet-handles.md) handle by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-316"><span id="INTERNET_OPTION_FROM_CACHE_TIMEOUT"></span><span id="internet_option_from_cache_timeout"></span>**\_option Internet \_ du \_ délai d’expiration du cache \_**</span><span class="sxs-lookup"><span data-stu-id="ecc71-316"><span id="INTERNET_OPTION_FROM_CACHE_TIMEOUT"></span><span id="internet_option_from_cache_timeout"></span>**INTERNET\_OPTION\_FROM\_CACHE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-317">63</span><span class="sxs-lookup"><span data-stu-id="ecc71-317">63</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-318">Définit ou récupère la valeur d’entier long non signé A1N qui contient la durée pendant laquelle le système doit attendre une réponse à une demande réseau avant de vérifier le cache pour une copie de la ressource.</span><span class="sxs-lookup"><span data-stu-id="ecc71-318">Sets or retrieves a1n unsigned long integer value that contains the amount of time the system should wait for a response to a network request before checking the cache for a copy of the resource.</span></span> <span data-ttu-id="ecc71-319">Si une requête réseau prend plus de temps que l’heure spécifiée et que la ressource demandée est disponible dans le cache, la ressource est récupérée à partir du cache.</span><span class="sxs-lookup"><span data-stu-id="ecc71-319">If a network request takes longer than the time specified and the requested resource is available in the cache, the resource is retrieved from the cache.</span></span> <span data-ttu-id="ecc71-320">Utilisé par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) et [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="ecc71-320">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-321"><span id="INTERNET_OPTION_HANDLE_TYPE"></span><span id="internet_option_handle_type"></span>**TYPE de handle de l' \_ option Internet \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ecc71-321"><span id="INTERNET_OPTION_HANDLE_TYPE"></span><span id="internet_option_handle_type"></span>**INTERNET\_OPTION\_HANDLE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-322">9</span><span class="sxs-lookup"><span data-stu-id="ecc71-322">9</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-323">Récupère une valeur d’entier long non signé qui contient le type des handles [**HINTERNET**](appendix-a-hinternet-handles.md) passés.</span><span class="sxs-lookup"><span data-stu-id="ecc71-323">Retrieves an unsigned long integer value that contains the type of the [**HINTERNET**](appendix-a-hinternet-handles.md) handles passed in.</span></span> <span data-ttu-id="ecc71-324">Utilisé par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) sur n’importe quel handle [HINTERNET](appendix-a-hinternet-handles.md) .</span><span class="sxs-lookup"><span data-stu-id="ecc71-324">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) on any [HINTERNET](appendix-a-hinternet-handles.md) handle.</span></span> <span data-ttu-id="ecc71-325">Les valeurs de retour possibles sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="ecc71-325">Possible return values include the following.</span></span>

<dl> <dt>

<span data-ttu-id="ecc71-326"><span id="INTERNET_HANDLE_TYPE_CONNECT_FTP"></span><span id="internet_handle_type_connect_ftp"></span>\_type de descripteur Internet \_ \_ connecter \_ FTP</span><span class="sxs-lookup"><span data-stu-id="ecc71-326"><span id="INTERNET_HANDLE_TYPE_CONNECT_FTP"></span><span id="internet_handle_type_connect_ftp"></span>INTERNET\_HANDLE\_TYPE\_CONNECT\_FTP</span></span>
</dt> <dd>

<span data-ttu-id="ecc71-327">2</span><span class="sxs-lookup"><span data-stu-id="ecc71-327">2</span></span>

</dd> <dt>

<span data-ttu-id="ecc71-328"><span id="INTERNET_HANDLE_TYPE_CONNECT_GOPHER"></span><span id="internet_handle_type_connect_gopher"></span>\_type de descripteur Internet \_ \_ connecter \_ Gopher</span><span class="sxs-lookup"><span data-stu-id="ecc71-328"><span id="INTERNET_HANDLE_TYPE_CONNECT_GOPHER"></span><span id="internet_handle_type_connect_gopher"></span>INTERNET\_HANDLE\_TYPE\_CONNECT\_GOPHER</span></span>
</dt> <dd>

<span data-ttu-id="ecc71-329">3</span><span class="sxs-lookup"><span data-stu-id="ecc71-329">3</span></span>

</dd> <dt>

<span data-ttu-id="ecc71-330"><span id="INTERNET_HANDLE_TYPE_CONNECT_HTTP"></span><span id="internet_handle_type_connect_http"></span>\_type de descripteur Internet \_ \_ Connect \_ http</span><span class="sxs-lookup"><span data-stu-id="ecc71-330"><span id="INTERNET_HANDLE_TYPE_CONNECT_HTTP"></span><span id="internet_handle_type_connect_http"></span>INTERNET\_HANDLE\_TYPE\_CONNECT\_HTTP</span></span>
</dt> <dd>

<span data-ttu-id="ecc71-331">4</span><span class="sxs-lookup"><span data-stu-id="ecc71-331">4</span></span>

</dd> <dt>

<span data-ttu-id="ecc71-332"><span id="INTERNET_HANDLE_TYPE_FILE_REQUEST"></span><span id="internet_handle_type_file_request"></span>\_demande de \_ fichier de type de handle Internet \_ \_</span><span class="sxs-lookup"><span data-stu-id="ecc71-332"><span id="INTERNET_HANDLE_TYPE_FILE_REQUEST"></span><span id="internet_handle_type_file_request"></span>INTERNET\_HANDLE\_TYPE\_FILE\_REQUEST</span></span>
</dt> <dd>

<span data-ttu-id="ecc71-333">14</span><span class="sxs-lookup"><span data-stu-id="ecc71-333">14</span></span>

</dd> <dt>

<span data-ttu-id="ecc71-334"><span id="INTERNET_HANDLE_TYPE_FTP_FILE"></span><span id="internet_handle_type_ftp_file"></span>\_ \_ fichier FTP de type descripteur Internet \_ \_</span><span class="sxs-lookup"><span data-stu-id="ecc71-334"><span id="INTERNET_HANDLE_TYPE_FTP_FILE"></span><span id="internet_handle_type_ftp_file"></span>INTERNET\_HANDLE\_TYPE\_FTP\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="ecc71-335">7</span><span class="sxs-lookup"><span data-stu-id="ecc71-335">7</span></span>

</dd> <dt>

<span data-ttu-id="ecc71-336"><span id="INTERNET_HANDLE_TYPE_FTP_FILE_HTML"></span><span id="internet_handle_type_ftp_file_html"></span>\_type de descripteur Internet \_ \_ \_ fichier FTP \_ HTML</span><span class="sxs-lookup"><span data-stu-id="ecc71-336"><span id="INTERNET_HANDLE_TYPE_FTP_FILE_HTML"></span><span id="internet_handle_type_ftp_file_html"></span>INTERNET\_HANDLE\_TYPE\_FTP\_FILE\_HTML</span></span>
</dt> <dd>

<span data-ttu-id="ecc71-337">8</span><span class="sxs-lookup"><span data-stu-id="ecc71-337">8</span></span>

</dd> <dt>

<span data-ttu-id="ecc71-338"><span id="INTERNET_HANDLE_TYPE_FTP_FIND"></span><span id="internet_handle_type_ftp_find"></span>\_ \_ recherche FTP du type de descripteur Internet \_ \_</span><span class="sxs-lookup"><span data-stu-id="ecc71-338"><span id="INTERNET_HANDLE_TYPE_FTP_FIND"></span><span id="internet_handle_type_ftp_find"></span>INTERNET\_HANDLE\_TYPE\_FTP\_FIND</span></span>
</dt> <dd>

<span data-ttu-id="ecc71-339">5</span><span class="sxs-lookup"><span data-stu-id="ecc71-339">5</span></span>

</dd> <dt>

<span data-ttu-id="ecc71-340"><span id="INTERNET_HANDLE_TYPE_FTP_FIND_HTML"></span><span id="internet_handle_type_ftp_find_html"></span>\_type de descripteur Internet \_ \_ FTP \_ Rechercher \_ HTML</span><span class="sxs-lookup"><span data-stu-id="ecc71-340"><span id="INTERNET_HANDLE_TYPE_FTP_FIND_HTML"></span><span id="internet_handle_type_ftp_find_html"></span>INTERNET\_HANDLE\_TYPE\_FTP\_FIND\_HTML</span></span>
</dt> <dd>

<span data-ttu-id="ecc71-341">6</span><span class="sxs-lookup"><span data-stu-id="ecc71-341">6</span></span>

</dd> <dt>

<span data-ttu-id="ecc71-342"><span id="INTERNET_HANDLE_TYPE_GOPHER_FILE"></span><span id="internet_handle_type_gopher_file"></span>\_type de descripteur Internet- \_ \_ \_ fichier Gopher</span><span class="sxs-lookup"><span data-stu-id="ecc71-342"><span id="INTERNET_HANDLE_TYPE_GOPHER_FILE"></span><span id="internet_handle_type_gopher_file"></span>INTERNET\_HANDLE\_TYPE\_GOPHER\_FILE</span></span>
</dt> <dd>

<span data-ttu-id="ecc71-343">11</span><span class="sxs-lookup"><span data-stu-id="ecc71-343">11</span></span>

</dd> <dt>

<span data-ttu-id="ecc71-344"><span id="INTERNET_HANDLE_TYPE_GOPHER_FILE_HTML"></span><span id="internet_handle_type_gopher_file_html"></span>\_type de descripteur Internet du \_ \_ \_ fichier Gopher \_ HTML</span><span class="sxs-lookup"><span data-stu-id="ecc71-344"><span id="INTERNET_HANDLE_TYPE_GOPHER_FILE_HTML"></span><span id="internet_handle_type_gopher_file_html"></span>INTERNET\_HANDLE\_TYPE\_GOPHER\_FILE\_HTML</span></span>
</dt> <dd>

<span data-ttu-id="ecc71-345">12</span><span class="sxs-lookup"><span data-stu-id="ecc71-345">12</span></span>

</dd> <dt>

<span data-ttu-id="ecc71-346"><span id="INTERNET_HANDLE_TYPE_GOPHER_FIND"></span><span id="internet_handle_type_gopher_find"></span>\_ \_ recherche Gopher du type de descripteur Internet \_ \_</span><span class="sxs-lookup"><span data-stu-id="ecc71-346"><span id="INTERNET_HANDLE_TYPE_GOPHER_FIND"></span><span id="internet_handle_type_gopher_find"></span>INTERNET\_HANDLE\_TYPE\_GOPHER\_FIND</span></span>
</dt> <dd>

<span data-ttu-id="ecc71-347">9</span><span class="sxs-lookup"><span data-stu-id="ecc71-347">9</span></span>

</dd> <dt>

<span data-ttu-id="ecc71-348"><span id="INTERNET_HANDLE_TYPE_GOPHER_FIND_HTML"></span><span id="internet_handle_type_gopher_find_html"></span>\_type de descripteur Internet \_ \_ Gopher \_ Rechercher \_ HTML</span><span class="sxs-lookup"><span data-stu-id="ecc71-348"><span id="INTERNET_HANDLE_TYPE_GOPHER_FIND_HTML"></span><span id="internet_handle_type_gopher_find_html"></span>INTERNET\_HANDLE\_TYPE\_GOPHER\_FIND\_HTML</span></span>
</dt> <dd>

<span data-ttu-id="ecc71-349">10</span><span class="sxs-lookup"><span data-stu-id="ecc71-349">10</span></span>

</dd> <dt>

<span data-ttu-id="ecc71-350"><span id="INTERNET_HANDLE_TYPE_HTTP_REQUEST"></span><span id="internet_handle_type_http_request"></span>\_ \_ requête HTTP de type descripteur Internet \_ \_</span><span class="sxs-lookup"><span data-stu-id="ecc71-350"><span id="INTERNET_HANDLE_TYPE_HTTP_REQUEST"></span><span id="internet_handle_type_http_request"></span>INTERNET\_HANDLE\_TYPE\_HTTP\_REQUEST</span></span>
</dt> <dd>

<span data-ttu-id="ecc71-351">13</span><span class="sxs-lookup"><span data-stu-id="ecc71-351">13</span></span>

</dd> <dt>

<span data-ttu-id="ecc71-352"><span id="INTERNET_HANDLE_TYPE_INTERNET"></span><span id="internet_handle_type_internet"></span>\_type de descripteur Internet \_ \_ Internet</span><span class="sxs-lookup"><span data-stu-id="ecc71-352"><span id="INTERNET_HANDLE_TYPE_INTERNET"></span><span id="internet_handle_type_internet"></span>INTERNET\_HANDLE\_TYPE\_INTERNET</span></span>
</dt> <dd>

<span data-ttu-id="ecc71-353">1</span><span class="sxs-lookup"><span data-stu-id="ecc71-353">1</span></span>

</dd> </dl>

</dl> </dd> <dt>

<span data-ttu-id="ecc71-354"><span id="INTERNET_OPTION_HSTS"></span><span id="internet_option_hsts"></span>**\_option Internet \_ HSTS**</span><span class="sxs-lookup"><span data-stu-id="ecc71-354"><span id="INTERNET_OPTION_HSTS"></span><span id="internet_option_hsts"></span>**INTERNET\_OPTION\_HSTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-355">157</span><span class="sxs-lookup"><span data-stu-id="ecc71-355">157</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-356">Obtient/définit une valeur BOOLÉENNE qui indique si WinInet doit suivre les directives HSTS (HTTP strict transport Security) des serveurs.</span><span class="sxs-lookup"><span data-stu-id="ecc71-356">Gets/sets a BOOL indicating whether WinInet should follow HTTP Strict Transport Security (HSTS) directives from servers.</span></span> <span data-ttu-id="ecc71-357">Si cette option est activée, les demandes de https://mises en cache pour les domaines qui ont une stratégie HSTS mise en cache par WinInet sont redirigées vers les URL https://correspondantes.</span><span class="sxs-lookup"><span data-stu-id="ecc71-357">If enabled, https:// schemed requests to domains which have an HSTS policy cached by WinInet will be redirected to matching https:// URLs.</span></span> <span data-ttu-id="ecc71-358">La valeur par défaut est FALSE.</span><span class="sxs-lookup"><span data-stu-id="ecc71-358">The default is FALSE.</span></span> <span data-ttu-id="ecc71-359">Pris en charge dans Windows 8.1 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ecc71-359">Supported in Windows 8.1 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-360"><span id="INTERNET_OPTION_HTTP_DECODING"></span><span id="internet_option_http_decoding"></span>**\_décodage http des options Internet \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ecc71-360"><span id="INTERNET_OPTION_HTTP_DECODING"></span><span id="internet_option_http_decoding"></span>**INTERNET\_OPTION\_HTTP\_DECODING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-361">65</span><span class="sxs-lookup"><span data-stu-id="ecc71-361">65</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-362">Permet à WinINet d’effectuer le décodage pour les schémas d’encodage gzip et deflate.</span><span class="sxs-lookup"><span data-stu-id="ecc71-362">Enables WinINet to perform decoding for the gzip and deflate encoding schemes.</span></span> <span data-ttu-id="ecc71-363">Pour plus d’informations, consultez [**encodage du contenu**](content-encoding.md).</span><span class="sxs-lookup"><span data-stu-id="ecc71-363">For more information, see [**Content Encoding**](content-encoding.md).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-364"><span id="INTERNET_OPTION_HTTP_PROTOCOL_USED"></span><span id="internet_option_http_protocol_used"></span>**\_option Internet \_ \_ protocole http \_ utilisée**</span><span class="sxs-lookup"><span data-stu-id="ecc71-364"><span id="INTERNET_OPTION_HTTP_PROTOCOL_USED"></span><span id="internet_option_http_protocol_used"></span>**INTERNET\_OPTION\_HTTP\_PROTOCOL\_USED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-365">149</span><span class="sxs-lookup"><span data-stu-id="ecc71-365">149</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-366">Obtient une valeur DWORD qui indique quelle version HTTP avancée a été utilisée sur une demande donnée.</span><span class="sxs-lookup"><span data-stu-id="ecc71-366">Gets a DWORD indicating which advanced HTTP version was used on a given request.</span></span> <span data-ttu-id="ecc71-367">Les valeurs possibles sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="ecc71-367">Possible values are:</span></span>

-   <span data-ttu-id="ecc71-368">\_ \_ Indicateur de protocole http \_ http2 (0X2).</span><span class="sxs-lookup"><span data-stu-id="ecc71-368">HTTP\_PROTOCOL\_FLAG\_HTTP2 (0x2).</span></span> <span data-ttu-id="ecc71-369">Pris en charge sur Windows 10, version 1507 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ecc71-369">Supported on Windows 10, version 1507 and later.</span></span>

<span data-ttu-id="ecc71-370">0x0 indique HTTP/1.1 ou une version antérieure ; consultez \_ la version http de l’option Internet \_ si une \_ plus grande précision est nécessaire pour déterminer quelle version héritée a été utilisée.</span><span class="sxs-lookup"><span data-stu-id="ecc71-370">0x0 indicates HTTP/1.1 or earlier; see INTERNET\_OPTION\_HTTP\_VERSION if more precision is needed about which legacy version was used.</span></span> <span data-ttu-id="ecc71-371">Pris en charge sur Windows 10, version 1507 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ecc71-371">Supported on Windows 10, version 1507 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-372"><span id="INTERNET_OPTION_HTTP_VERSION"></span><span id="internet_option_http_version"></span>**\_ \_ version http de l’option Internet \_**</span><span class="sxs-lookup"><span data-stu-id="ecc71-372"><span id="INTERNET_OPTION_HTTP_VERSION"></span><span id="internet_option_http_version"></span>**INTERNET\_OPTION\_HTTP\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-373">59</span><span class="sxs-lookup"><span data-stu-id="ecc71-373">59</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-374">Définit ou récupère une structure [**d' \_ \_ informations de version http**](/windows/desktop/api/Wininet/ns-wininet-http_version_info) qui contient la version http prise en charge.</span><span class="sxs-lookup"><span data-stu-id="ecc71-374">Sets or retrieves an [**HTTP\_VERSION\_INFO**](/windows/desktop/api/Wininet/ns-wininet-http_version_info) structure that contains the supported HTTP version.</span></span> <span data-ttu-id="ecc71-375">Elle doit être utilisée sur un handle **null** .</span><span class="sxs-lookup"><span data-stu-id="ecc71-375">This must be used on a **NULL** handle.</span></span> <span data-ttu-id="ecc71-376">Utilisé par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) et [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="ecc71-376">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>

<span data-ttu-id="ecc71-377">Sur Windows 7, Windows Server 2008 R2 et versions ultérieures, la valeur du membre **dwMinorVersion** dans la structure info de la [**\_ version \_ http**](/windows/desktop/api/Wininet/ns-wininet-http_version_info) est remplacée par les paramètres d’Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="ecc71-377">On Windows 7, Windows Server 2008 R2, and later, the value of the **dwMinorVersion** member in the [**HTTP\_VERSION\_INFO**](/windows/desktop/api/Wininet/ns-wininet-http_version_info) structure is overridden by Internet Explorer settings.</span></span> <span data-ttu-id="ecc71-378">**EnableHttp1 \_ 1** est une valeur de Registre sous **HKLM \\ Software \\ Microsoft \\ InternetExplorer \\ AdvacnedOptions \\ http \\ GENABLE** contrôlé par les options Internet définies dans Internet Explorer pour le système.</span><span class="sxs-lookup"><span data-stu-id="ecc71-378">**EnableHttp1\_1** is a registry value under **HKLM\\Software\\Microsoft\\InternetExplorer\\AdvacnedOptions\\HTTP\\GENABLE** controlled by Internet Options set in Internet Explorer for the system.</span></span> <span data-ttu-id="ecc71-379">La valeur **EnableHttp1 \_ 1** est définie par défaut sur 1.</span><span class="sxs-lookup"><span data-stu-id="ecc71-379">The **EnableHttp1\_1** value defaults to 1.</span></span> <span data-ttu-id="ecc71-380">La structure des **\_ \_ informations de version http** est ignorée pour toute VERSION http inférieure à 1,1 si **EnableHttp1 \_ 1** est défini sur 1.</span><span class="sxs-lookup"><span data-stu-id="ecc71-380">The **HTTP\_VERSION\_INFO** structure is ignored for any HTTP version less than 1.1 if **EnableHttp1\_1** is set to 1.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-381"><span id="INTERNET_OPTION_IDENTITY"></span><span id="internet_option_identity"></span>**identité de l' \_ option Internet \_**</span><span class="sxs-lookup"><span data-stu-id="ecc71-381"><span id="INTERNET_OPTION_IDENTITY"></span><span id="internet_option_identity"></span>**INTERNET\_OPTION\_IDENTITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-382">78</span><span class="sxs-lookup"><span data-stu-id="ecc71-382">78</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-383">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="ecc71-383">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-384"><span id="INTERNET_OPTION_IDLE_STATE"></span><span id="internet_option_idle_state"></span>**\_ \_ état inactif des options Internet \_**</span><span class="sxs-lookup"><span data-stu-id="ecc71-384"><span id="INTERNET_OPTION_IDLE_STATE"></span><span id="internet_option_idle_state"></span>**INTERNET\_OPTION\_IDLE\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-385">51</span><span class="sxs-lookup"><span data-stu-id="ecc71-385">51</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-386">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="ecc71-386">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-387"><span id="INTERNET_OPTION_IDN"></span><span id="internet_option_idn"></span>**\_IDN des options Internet \_**</span><span class="sxs-lookup"><span data-stu-id="ecc71-387"><span id="INTERNET_OPTION_IDN"></span><span id="internet_option_idn"></span>**INTERNET\_OPTION\_IDN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-388">102</span><span class="sxs-lookup"><span data-stu-id="ecc71-388">102</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-389">Par défaut, la partie hôte ou autorité de l’URL est encodée en fonction de la spécification IDN pour les connexions directes et par proxy.</span><span class="sxs-lookup"><span data-stu-id="ecc71-389">By default, the host or authority portion of the URL is encoded according to the IDN specification for both direct and proxy connections.</span></span> <span data-ttu-id="ecc71-390">Cette option peut être utilisée sur la demande ou sur le descripteur de connexion pour activer ou désactiver les IDN.</span><span class="sxs-lookup"><span data-stu-id="ecc71-390">This option can be used on the request, or connection handle to enable or disable IDN.</span></span> <span data-ttu-id="ecc71-391">Lorsque l’IDN est désactivé, WinINet utilise la page de codes du système pour encoder la partie hôte ou autorité de l’URL.</span><span class="sxs-lookup"><span data-stu-id="ecc71-391">When IDN is disabled, WinINet uses the system codepage to encode the host or authority portion of the URL.</span></span> <span data-ttu-id="ecc71-392">Pour désactiver la conversion de l’hôte IDN, définissez le paramètre *lpBuffer* dans l’appel à [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) sur zéro.</span><span class="sxs-lookup"><span data-stu-id="ecc71-392">To disable IDN host conversion, set the *lpBuffer* parameter in the call to [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) to zero.</span></span> <span data-ttu-id="ecc71-393">Pour activer la conversion d’IDN uniquement sur la connexion directe, spécifiez les **\_ indicateurs Internet \_ IDN \_ directs** dans le paramètre *lpBuffer* de l’appel à **InternetSetOption**.</span><span class="sxs-lookup"><span data-stu-id="ecc71-393">To enable IDN conversion on only the direct connection, specify **INTERNET\_FLAG\_IDN\_DIRECT** in the *lpBuffer* parameter in the call to **InternetSetOption**.</span></span> <span data-ttu-id="ecc71-394">Pour activer la conversion IDN uniquement sur la connexion proxy, spécifiez le **\_ proxy d’indicateur Internet \_ \_ IDN** dans le paramètre *lpBuffer* de l’appel à **InternetSetOption**.</span><span class="sxs-lookup"><span data-stu-id="ecc71-394">To enable IDN conversion on only the proxy connection, specify **INTERNET\_FLAG\_IDN\_PROXY** in the *lpBuffer* parameter in the call to **InternetSetOption**.</span></span>

<span data-ttu-id="ecc71-395">**Windows XP avec SP2 et Windows Server 2003 avec SP1 :** Cet indicateur n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="ecc71-395">**Windows XP with SP2 and Windows Server 2003 with SP1:** This flag is not supported.</span></span>

<span data-ttu-id="ecc71-396">**Version :** Nécessite Internet Explorer 7,0.</span><span class="sxs-lookup"><span data-stu-id="ecc71-396">**Version:** Requires Internet Explorer 7.0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-397"><span id="INTERNET_OPTION_IGNORE_OFFLINE"></span><span id="internet_option_ignore_offline"></span>**\_option Internet \_ Ignorer \_ hors connexion**</span><span class="sxs-lookup"><span data-stu-id="ecc71-397"><span id="INTERNET_OPTION_IGNORE_OFFLINE"></span><span id="internet_option_ignore_offline"></span>**INTERNET\_OPTION\_IGNORE\_OFFLINE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-398">77</span><span class="sxs-lookup"><span data-stu-id="ecc71-398">77</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-399">Définit ou récupère une valeur indiquant si l’indicateur global Offline doit être ignoré pour le handle de requête spécifié.</span><span class="sxs-lookup"><span data-stu-id="ecc71-399">Sets or retrieves whether the global offline flag should be ignored for the specified request handle.</span></span> <span data-ttu-id="ecc71-400">Aucune mémoire tampon n’est requise pour cette option.</span><span class="sxs-lookup"><span data-stu-id="ecc71-400">No buffer is required for this option.</span></span> <span data-ttu-id="ecc71-401">Cela est utilisé par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) et [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) avec un handle de demande.</span><span class="sxs-lookup"><span data-stu-id="ecc71-401">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) with a request handle.</span></span> <span data-ttu-id="ecc71-402">Cette option n’est valide que dans Internet Explorer 5 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ecc71-402">This option is only valid in Internet Explorer 5 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-403"><span id="INTERNET_OPTION_KEEP_CONNECTION"></span><span id="internet_option_keep_connection"></span>**\_option Internet \_ conserver la \_ connexion**</span><span class="sxs-lookup"><span data-stu-id="ecc71-403"><span id="INTERNET_OPTION_KEEP_CONNECTION"></span><span id="internet_option_keep_connection"></span>**INTERNET\_OPTION\_KEEP\_CONNECTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-404">22</span><span class="sxs-lookup"><span data-stu-id="ecc71-404">22</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-405">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="ecc71-405">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-406"><span id="INTERNET_OPTION_LISTEN_TIMEOUT"></span><span id="internet_option_listen_timeout"></span>**\_ \_ \_ délai d’attente d’écoute des options Internet**</span><span class="sxs-lookup"><span data-stu-id="ecc71-406"><span id="INTERNET_OPTION_LISTEN_TIMEOUT"></span><span id="internet_option_listen_timeout"></span>**INTERNET\_OPTION\_LISTEN\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-407">11</span><span class="sxs-lookup"><span data-stu-id="ecc71-407">11</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-408">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="ecc71-408">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-409"><span id="INTERNET_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="internet_option_max_conns_per_1_0_server"></span>**\_Option Internet \_ Max \_ Conns \_ par \_ \_ serveur 1 0 \_**</span><span class="sxs-lookup"><span data-stu-id="ecc71-409"><span id="INTERNET_OPTION_MAX_CONNS_PER_1_0_SERVER"></span><span id="internet_option_max_conns_per_1_0_server"></span>**INTERNET\_OPTION\_MAX\_CONNS\_PER\_1\_0\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-410">74</span><span class="sxs-lookup"><span data-stu-id="ecc71-410">74</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-411">Définit ou récupère une valeur d’entier long non signé qui contient le nombre maximal de connexions autorisées par serveur HTTP/1.0.</span><span class="sxs-lookup"><span data-stu-id="ecc71-411">Sets or retrieves an unsigned long integer value that contains the maximum number of connections allowed per HTTP/1.0 server.</span></span> <span data-ttu-id="ecc71-412">Utilisé par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) et [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="ecc71-412">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="ecc71-413">Cette option n’est valide que dans Internet Explorer 5 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ecc71-413">This option is only valid in Internet Explorer 5 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-414"><span id="INTERNET_OPTION_MAX_CONNS_PER_PROXY"></span><span id="internet_option_max_conns_per_proxy"></span>**\_option Internet \_ Max \_ Conns \_ par \_ proxy**</span><span class="sxs-lookup"><span data-stu-id="ecc71-414"><span id="INTERNET_OPTION_MAX_CONNS_PER_PROXY"></span><span id="internet_option_max_conns_per_proxy"></span>**INTERNET\_OPTION\_MAX\_CONNS\_PER\_PROXY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-415">103</span><span class="sxs-lookup"><span data-stu-id="ecc71-415">103</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-416">Définit ou récupère une valeur d’entier long non signé qui contient le nombre maximal de connexions autorisées par proxy CERN.</span><span class="sxs-lookup"><span data-stu-id="ecc71-416">Sets or retrieves an unsigned long integer value that contains the maximum number of connections allowed per CERN proxy.</span></span> <span data-ttu-id="ecc71-417">Lorsque cette option est définie ou récupérée, le paramètre *hInternet* doit être défini sur une valeur de handle **null** .</span><span class="sxs-lookup"><span data-stu-id="ecc71-417">When this option is set or retrieved, the *hInternet* parameter must set to a **null** handle value.</span></span> <span data-ttu-id="ecc71-418">Une valeur de handle **null** indique que l’option doit être définie ou interrogée pour le processus actuel.</span><span class="sxs-lookup"><span data-stu-id="ecc71-418">A **null** handle value indicates that the option should be set or queried for the current process.</span></span> <span data-ttu-id="ecc71-419">Lors de l’appel de [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) avec cette option, tous les objets proxy existants recevront la nouvelle valeur.</span><span class="sxs-lookup"><span data-stu-id="ecc71-419">When calling [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) with this option, all existing proxy objects will receive the new value.</span></span> <span data-ttu-id="ecc71-420">Cette valeur est limitée à une plage comprise entre 2 et 128 inclus.</span><span class="sxs-lookup"><span data-stu-id="ecc71-420">This value is limited to a range of 2 to 128, inclusive.</span></span>

<span data-ttu-id="ecc71-421">**Version :** Nécessite Internet Explorer 8,0.</span><span class="sxs-lookup"><span data-stu-id="ecc71-421">**Version:** Requires Internet Explorer 8.0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-422"><span id="INTERNET_OPTION_MAX_CONNS_PER_SERVER"></span><span id="internet_option_max_conns_per_server"></span>**\_option Internet \_ Max \_ Conns \_ par \_ serveur**</span><span class="sxs-lookup"><span data-stu-id="ecc71-422"><span id="INTERNET_OPTION_MAX_CONNS_PER_SERVER"></span><span id="internet_option_max_conns_per_server"></span>**INTERNET\_OPTION\_MAX\_CONNS\_PER\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-423">73</span><span class="sxs-lookup"><span data-stu-id="ecc71-423">73</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-424">Définit ou récupère une valeur d’entier long non signé qui contient le nombre maximal de connexions autorisées par serveur.</span><span class="sxs-lookup"><span data-stu-id="ecc71-424">Sets or retrieves an unsigned long integer value that contains the maximum number of connections allowed per server.</span></span> <span data-ttu-id="ecc71-425">Utilisé par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) et [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="ecc71-425">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="ecc71-426">Cette option n’est valide que dans Internet Explorer 5 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ecc71-426">This option is only valid in Internet Explorer 5 and later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-427"><span id="INTERNET_OPTION_OFFLINE_MODE"></span><span id="internet_option_offline_mode"></span>**\_option Internet \_ \_ en mode hors connexion**</span><span class="sxs-lookup"><span data-stu-id="ecc71-427"><span id="INTERNET_OPTION_OFFLINE_MODE"></span><span id="internet_option_offline_mode"></span>**INTERNET\_OPTION\_OFFLINE\_MODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-428">26</span><span class="sxs-lookup"><span data-stu-id="ecc71-428">26</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-429">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="ecc71-429">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-430"><span id="INTERNET_OPTION_OFFLINE_SEMANTICS"></span><span id="internet_option_offline_semantics"></span>**\_ \_ sémantiques hors connexion des options Internet \_**</span><span class="sxs-lookup"><span data-stu-id="ecc71-430"><span id="INTERNET_OPTION_OFFLINE_SEMANTICS"></span><span id="internet_option_offline_semantics"></span>**INTERNET\_OPTION\_OFFLINE\_SEMANTICS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-431">52</span><span class="sxs-lookup"><span data-stu-id="ecc71-431">52</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-432">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="ecc71-432">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-433"><span id="INTERNET_OPTION_OPT_IN_WEAK_SIGNATURE"></span><span id="internet_option_opt_in_weak_signature"></span>**\_option Internet \_ OPT \_ dans \_ une \_ signature faible**</span><span class="sxs-lookup"><span data-stu-id="ecc71-433"><span id="INTERNET_OPTION_OPT_IN_WEAK_SIGNATURE"></span><span id="internet_option_opt_in_weak_signature"></span>**INTERNET\_OPTION\_OPT\_IN\_WEAK\_SIGNATURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-434">176</span><span class="sxs-lookup"><span data-stu-id="ecc71-434">176</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-435">Abonnez-vous à des signatures faibles (par exemple, SHA-1) pour qu’elles soient considérées comme non sécurisées.</span><span class="sxs-lookup"><span data-stu-id="ecc71-435">Opt-in for weak signatures (e.g. SHA-1) to be treated as insecure.</span></span> <span data-ttu-id="ecc71-436">Cela indique à WinInet d’appeler [**CertGetCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain) à l’aide de la **\_ chaîne \_ de certificats opt dans le paramètre \_ de \_ \_ signature faible** .</span><span class="sxs-lookup"><span data-stu-id="ecc71-436">This will instruct WinInet to call [**CertGetCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain) using the **CERT\_CHAIN\_OPT\_IN\_WEAK\_SIGNATURE** parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-437"><span id="INTERNET_OPTION_PARENT_HANDLE"></span><span id="internet_option_parent_handle"></span>**\_ \_ handle parent de l’option Internet \_**</span><span class="sxs-lookup"><span data-stu-id="ecc71-437"><span id="INTERNET_OPTION_PARENT_HANDLE"></span><span id="internet_option_parent_handle"></span>**INTERNET\_OPTION\_PARENT\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-438">21</span><span class="sxs-lookup"><span data-stu-id="ecc71-438">21</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-439">Récupère le handle parent de ce handle.</span><span class="sxs-lookup"><span data-stu-id="ecc71-439">Retrieves the parent handle to this handle.</span></span> <span data-ttu-id="ecc71-440">Cette option peut être utilisée sur n’importe quel handle [**HINTERNET**](appendix-a-hinternet-handles.md) par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="ecc71-440">This option can be used on any [**HINTERNET**](appendix-a-hinternet-handles.md) handle by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-441"><span id="INTERNET_OPTION_PASSWORD"></span><span id="internet_option_password"></span>**\_ \_ mot de passe de l’option Internet**</span><span class="sxs-lookup"><span data-stu-id="ecc71-441"><span id="INTERNET_OPTION_PASSWORD"></span><span id="internet_option_password"></span>**INTERNET\_OPTION\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-442">29</span><span class="sxs-lookup"><span data-stu-id="ecc71-442">29</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-443">Définit ou récupère une valeur de chaîne qui contient le mot de passe associé à un handle retourné par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="ecc71-443">Sets or retrieves a string value that contains the password associated with a handle returned by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span> <span data-ttu-id="ecc71-444">Utilisé par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) et [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="ecc71-444">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-445"><span id="INTERNET_OPTION_PER_CONNECTION_OPTION"></span><span id="internet_option_per_connection_option"></span>**option \_ Internet \_ par \_ option de connexion \_**</span><span class="sxs-lookup"><span data-stu-id="ecc71-445"><span id="INTERNET_OPTION_PER_CONNECTION_OPTION"></span><span id="internet_option_per_connection_option"></span>**INTERNET\_OPTION\_PER\_CONNECTION\_OPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-446">75</span><span class="sxs-lookup"><span data-stu-id="ecc71-446">75</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-447">Définit ou récupère une structure de liste d’options [**Internet \_ par \_ conn \_ \_**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) qui spécifie une liste d’options pour une connexion particulière.</span><span class="sxs-lookup"><span data-stu-id="ecc71-447">Sets or retrieves an [**INTERNET\_PER\_CONN\_OPTION\_LIST**](/windows/desktop/api/Wininet/ns-wininet-internet_per_conn_option_lista) structure that specifies a list of options for a particular connection.</span></span> <span data-ttu-id="ecc71-448">Utilisé par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) et [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="ecc71-448">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="ecc71-449">Cette option n’est valide que dans Internet Explorer 5 et versions ultérieures.</span><span class="sxs-lookup"><span data-stu-id="ecc71-449">This option is only valid in Internet Explorer 5 and later.</span></span>

> [!Note]  
> <span data-ttu-id="ecc71-450">**Internet \_ Option \_ per \_ Connection \_** entraîne la modification des paramètres à l’échelle du système lorsqu’un descripteur **null** est utilisé dans l’appel à [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="ecc71-450">**INTERNET\_OPTION\_PER\_CONNECTION\_OPTION** causes the settings to be changed on a system-wide basis when a **NULL** handle is used in the call to [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="ecc71-451">Pour actualiser les paramètres de proxy globaux, vous devez appeler **InternetSetOption** avec l’indicateur option d’actualisation de l' **\_ option \_ Internet** .</span><span class="sxs-lookup"><span data-stu-id="ecc71-451">To refresh the global proxy settings, you must call **InternetSetOption** with the **INTERNET\_OPTION\_REFRESH** option flag.</span></span>

 

> [!Note]  
> <span data-ttu-id="ecc71-452">Pour modifier les informations de proxy pour l’ensemble du processus sans affecter les paramètres globaux dans Internet Explorer 5 et versions ultérieures, utilisez cette option sur le descripteur renvoyé par [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span><span class="sxs-lookup"><span data-stu-id="ecc71-452">To change proxy information for the entire process without affecting the global settings in Internet Explorer 5 and later, use this option on the handle that is returned from [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span> <span data-ttu-id="ecc71-453">L’exemple de code suivant modifie le proxy pour l’ensemble du processus, même si le handle [**HINTERNET**](appendix-a-hinternet-handles.md) est fermé et n’est utilisé par aucune demande.</span><span class="sxs-lookup"><span data-stu-id="ecc71-453">The following code example changes the proxy for the whole process even though the [**HINTERNET**](appendix-a-hinternet-handles.md) handle is closed and is not used by any requests.</span></span>

 

<span data-ttu-id="ecc71-454">Pour plus d’informations et d’exemples de code, consultez [l’article 226473](https://support.microsoft.com/kb/226473)de la base de connaissances.</span><span class="sxs-lookup"><span data-stu-id="ecc71-454">For more information and code examples, see [KB article 226473](https://support.microsoft.com/kb/226473).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-455"><span id="INTERNET_OPTION_POLICY"></span><span id="internet_option_policy"></span>**\_stratégie d’option Internet \_**</span><span class="sxs-lookup"><span data-stu-id="ecc71-455"><span id="INTERNET_OPTION_POLICY"></span><span id="internet_option_policy"></span>**INTERNET\_OPTION\_POLICY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-456">48</span><span class="sxs-lookup"><span data-stu-id="ecc71-456">48</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-457">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="ecc71-457">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-458"><span id="INTERNET_OPTION_PROXY"></span><span id="internet_option_proxy"></span>**\_proxy d’option Internet \_**</span><span class="sxs-lookup"><span data-stu-id="ecc71-458"><span id="INTERNET_OPTION_PROXY"></span><span id="internet_option_proxy"></span>**INTERNET\_OPTION\_PROXY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-459">38</span><span class="sxs-lookup"><span data-stu-id="ecc71-459">38</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-460">Définit ou récupère une structure [**d' \_ \_ informations de proxy Internet**](/windows/desktop/api/Wininet/ns-wininet-internet_proxy_info) qui contient les données de proxy pour un handle [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) existant lorsque le descripteur [**HINTERNET**](appendix-a-hinternet-handles.md) n’a pas la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="ecc71-460">Sets or retrieves an [**INTERNET\_PROXY\_INFO**](/windows/desktop/api/Wininet/ns-wininet-internet_proxy_info) structure that contains the proxy data for an existing [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) handle when the [**HINTERNET**](appendix-a-hinternet-handles.md) handle is not **NULL**.</span></span> <span data-ttu-id="ecc71-461">Si le handle [**HINTERNET**](appendix-a-hinternet-handles.md) a la **valeur null**, la fonction définit ou interroge les données de proxy globales.</span><span class="sxs-lookup"><span data-stu-id="ecc71-461">If the [**HINTERNET**](appendix-a-hinternet-handles.md) handle is **NULL**, the function sets or queries the global proxy data.</span></span> <span data-ttu-id="ecc71-462">Cette option peut être utilisée sur le handle retourné par **InternetOpen**.</span><span class="sxs-lookup"><span data-stu-id="ecc71-462">This option can be used on the handle returned by **InternetOpen**.</span></span> <span data-ttu-id="ecc71-463">Elle est utilisée par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) et [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="ecc71-463">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>

> [!Note]  
> <span data-ttu-id="ecc71-464">Il est recommandé \_ d’utiliser l’option option Internet \_ par \_ connexion à la place de l’option \_ Internet \_ \_ proxy.</span><span class="sxs-lookup"><span data-stu-id="ecc71-464">It is recommended that INTERNET\_OPTION\_PER\_CONNECTION\_OPTION be used instead of INTERNET\_OPTION\_PROXY.</span></span> <span data-ttu-id="ecc71-465">Pour plus d’informations, consultez [l’article 226473](https://support.microsoft.com/kb/226473)de la base de connaissances.</span><span class="sxs-lookup"><span data-stu-id="ecc71-465">For more information, see [KB article 226473](https://support.microsoft.com/kb/226473).</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-466"><span id="INTERNET_OPTION_PROXY_PASSWORD"></span><span id="internet_option_proxy_password"></span>**\_ \_ mot de passe du proxy de l’option Internet \_**</span><span class="sxs-lookup"><span data-stu-id="ecc71-466"><span id="INTERNET_OPTION_PROXY_PASSWORD"></span><span id="internet_option_proxy_password"></span>**INTERNET\_OPTION\_PROXY\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-467">44</span><span class="sxs-lookup"><span data-stu-id="ecc71-467">44</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-468">Définit ou récupère une valeur de chaîne qui contient le mot de passe utilisé pour accéder au proxy.</span><span class="sxs-lookup"><span data-stu-id="ecc71-468">Sets or retrieves a string value that contains the password used to access the proxy.</span></span> <span data-ttu-id="ecc71-469">Utilisé par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) et [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="ecc71-469">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="ecc71-470">Cette option peut être définie sur le descripteur renvoyé par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) ou [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span><span class="sxs-lookup"><span data-stu-id="ecc71-470">This option can be set on the handle returned by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-471"><span id="INTERNET_OPTION_PROXY_SETTINGS_CHANGED"></span><span id="internet_option_proxy_settings_changed"></span>**paramètres de proxy de l' \_ option Internet \_ \_ \_ modifiés**</span><span class="sxs-lookup"><span data-stu-id="ecc71-471"><span id="INTERNET_OPTION_PROXY_SETTINGS_CHANGED"></span><span id="internet_option_proxy_settings_changed"></span>**INTERNET\_OPTION\_PROXY\_SETTINGS\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-472">95</span><span class="sxs-lookup"><span data-stu-id="ecc71-472">95</span></span> 
</dt> <dt>



<span data-ttu-id="ecc71-473">Alerte l’instance WinInet actuelle que les paramètres de proxy ont changé et qu’ils doivent mettre à jour avec les nouveaux paramètres.</span><span class="sxs-lookup"><span data-stu-id="ecc71-473">Alerts the current WinInet instance that proxy settings have changed and that they must update with the new settings.</span></span> <span data-ttu-id="ecc71-474">Pour alerter toutes les instances WinInet disponibles, définissez le paramètre *buffer* de [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) sur **null** et *BufferLength* sur 0 lors du passage de cette option.</span><span class="sxs-lookup"><span data-stu-id="ecc71-474">To alert all available WinInet instances, set the *Buffer* parameter of [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) to **NULL** and *BufferLength* to 0 when passing this option.</span></span> <span data-ttu-id="ecc71-475">Cette option peut être définie sur le descripteur renvoyé par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) ou [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span><span class="sxs-lookup"><span data-stu-id="ecc71-475">This option can be set on the handle returned by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-476"><span id="INTERNET_OPTION_PROXY_USERNAME"></span><span id="internet_option_proxy_username"></span>**\_ \_ \_ nom d’utilisateur du proxy de l’option Internet**</span><span class="sxs-lookup"><span data-stu-id="ecc71-476"><span id="INTERNET_OPTION_PROXY_USERNAME"></span><span id="internet_option_proxy_username"></span>**INTERNET\_OPTION\_PROXY\_USERNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-477">43</span><span class="sxs-lookup"><span data-stu-id="ecc71-477">43</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-478">Définit ou récupère une valeur de chaîne qui contient le nom d’utilisateur utilisé pour accéder au proxy.</span><span class="sxs-lookup"><span data-stu-id="ecc71-478">Sets or retrieves a string value that contains the user name used to access the proxy.</span></span> <span data-ttu-id="ecc71-479">Utilisé par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) et [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="ecc71-479">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="ecc71-480">Cette option peut être définie sur le descripteur renvoyé par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) ou [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span><span class="sxs-lookup"><span data-stu-id="ecc71-480">This option can be set on the handle returned by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-481"><span id="INTERNET_OPTION_READ_BUFFER_SIZE"></span><span id="internet_option_read_buffer_size"></span>**\_taille de \_ la \_ mémoire tampon de lecture des options Internet \_**</span><span class="sxs-lookup"><span data-stu-id="ecc71-481"><span id="INTERNET_OPTION_READ_BUFFER_SIZE"></span><span id="internet_option_read_buffer_size"></span>**INTERNET\_OPTION\_READ\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-482">12</span><span class="sxs-lookup"><span data-stu-id="ecc71-482">12</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-483">Définit ou récupère une valeur d’entier long non signé qui contient la taille de la mémoire tampon de lecture.</span><span class="sxs-lookup"><span data-stu-id="ecc71-483">Sets or retrieves an unsigned long integer value that contains the size of the read buffer.</span></span> <span data-ttu-id="ecc71-484">Cette option peut être utilisée sur les handles [**HINTERNET**](appendix-a-hinternet-handles.md) retournés par [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea)et [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) (session FTP uniquement).</span><span class="sxs-lookup"><span data-stu-id="ecc71-484">This option can be used on [**HINTERNET**](appendix-a-hinternet-handles.md) handles returned by [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**FtpFindFirstFile**](/windows/desktop/api/Wininet/nf-wininet-ftpfindfirstfilea), and [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) (FTP session only).</span></span> <span data-ttu-id="ecc71-485">Cette option est utilisée par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) et [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="ecc71-485">This option is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-486"><span id="INTERNET_OPTION_RECEIVE_THROUGHPUT"></span><span id="internet_option_receive_throughput"></span>**\_débit de \_ réception des options Internet \_**</span><span class="sxs-lookup"><span data-stu-id="ecc71-486"><span id="INTERNET_OPTION_RECEIVE_THROUGHPUT"></span><span id="internet_option_receive_throughput"></span>**INTERNET\_OPTION\_RECEIVE\_THROUGHPUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-487">57</span><span class="sxs-lookup"><span data-stu-id="ecc71-487">57</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-488">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="ecc71-488">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-489"><span id="INTERNET_OPTION_RECEIVE_TIMEOUT"></span><span id="internet_option_receive_timeout"></span>**\_délai de \_ réception des options Internet \_**</span><span class="sxs-lookup"><span data-stu-id="ecc71-489"><span id="INTERNET_OPTION_RECEIVE_TIMEOUT"></span><span id="internet_option_receive_timeout"></span>**INTERNET\_OPTION\_RECEIVE\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-490">6</span><span class="sxs-lookup"><span data-stu-id="ecc71-490">6</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-491">Définit ou récupère une valeur d’entier long non signé qui contient la valeur du délai d’attente, en millisecondes, pour recevoir une réponse à une demande.</span><span class="sxs-lookup"><span data-stu-id="ecc71-491">Sets or retrieves an unsigned long integer value that contains the time-out value, in milliseconds, to receive a response to a request.</span></span> <span data-ttu-id="ecc71-492">Si la réponse prend plus de temps que cette valeur de délai d’attente, la demande est annulée.</span><span class="sxs-lookup"><span data-stu-id="ecc71-492">If the response takes longer than this time-out value, the request is canceled.</span></span> <span data-ttu-id="ecc71-493">Cette option peut être utilisée sur n’importe quel handle [**HINTERNET**](appendix-a-hinternet-handles.md) , y compris un handle **null** .</span><span class="sxs-lookup"><span data-stu-id="ecc71-493">This option can be used on any [**HINTERNET**](appendix-a-hinternet-handles.md) handle, including a **NULL** handle.</span></span> <span data-ttu-id="ecc71-494">Elle est utilisée par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) et [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="ecc71-494">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>

<span data-ttu-id="ecc71-495">Cette option n’est pas destinée à représenter un délai d’expiration immédiat et précis.</span><span class="sxs-lookup"><span data-stu-id="ecc71-495">This option is not intended to represent a fine-grained, immediate timeout.</span></span> <span data-ttu-id="ecc71-496">Vous pouvez vous attendre à ce que le délai d’attente se produise jusqu’à six secondes après la valeur définie pour Timeout.</span><span class="sxs-lookup"><span data-stu-id="ecc71-496">You can expect the timeout to occur up to six seconds after the set timeout value.</span></span>

<span data-ttu-id="ecc71-497">Lorsqu’elle est utilisée en référence à une transaction FTP, cette option fait référence au canal de contrôle.</span><span class="sxs-lookup"><span data-stu-id="ecc71-497">When used in reference to an FTP transaction, this option refers to the control channel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-498"><span id="INTERNET_OPTION_REFRESH"></span><span id="internet_option_refresh"></span>**\_actualisation des options Internet \_**</span><span class="sxs-lookup"><span data-stu-id="ecc71-498"><span id="INTERNET_OPTION_REFRESH"></span><span id="internet_option_refresh"></span>**INTERNET\_OPTION\_REFRESH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-499">37</span><span class="sxs-lookup"><span data-stu-id="ecc71-499">37</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-500">Entraîne la relecture des données du proxy à partir du Registre pour un descripteur.</span><span class="sxs-lookup"><span data-stu-id="ecc71-500">Causes the proxy data to be reread from the registry for a handle.</span></span> <span data-ttu-id="ecc71-501">Aucune mémoire tampon n’est requise.</span><span class="sxs-lookup"><span data-stu-id="ecc71-501">No buffer is required.</span></span> <span data-ttu-id="ecc71-502">Cette option peut être utilisée sur le handle [**HINTERNET**](appendix-a-hinternet-handles.md) retourné par [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span><span class="sxs-lookup"><span data-stu-id="ecc71-502">This option can be used on the [**HINTERNET**](appendix-a-hinternet-handles.md) handle returned by [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena).</span></span> <span data-ttu-id="ecc71-503">Elle est utilisée par [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="ecc71-503">It is used by [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-504"><span id="INTERNET_OPTION_REMOVE_IDENTITY"></span><span id="internet_option_remove_identity"></span>**\_option Internet \_ Supprimer l' \_ identité**</span><span class="sxs-lookup"><span data-stu-id="ecc71-504"><span id="INTERNET_OPTION_REMOVE_IDENTITY"></span><span id="internet_option_remove_identity"></span>**INTERNET\_OPTION\_REMOVE\_IDENTITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-505">79</span><span class="sxs-lookup"><span data-stu-id="ecc71-505">79</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-506">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="ecc71-506">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-507"><span id="INTERNET_OPTION_REQUEST_FLAGS"></span><span id="internet_option_request_flags"></span>**\_indicateurs de \_ demande d’option Internet \_**</span><span class="sxs-lookup"><span data-stu-id="ecc71-507"><span id="INTERNET_OPTION_REQUEST_FLAGS"></span><span id="internet_option_request_flags"></span>**INTERNET\_OPTION\_REQUEST\_FLAGS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-508">23</span><span class="sxs-lookup"><span data-stu-id="ecc71-508">23</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-509">Récupère une valeur d’entier long non signé qui contient les indicateurs d’État spéciaux qui indiquent l’état du téléchargement en cours.</span><span class="sxs-lookup"><span data-stu-id="ecc71-509">Retrieves an unsigned long integer value that contains the special status flags that indicate the status of the download in progress.</span></span> <span data-ttu-id="ecc71-510">Utilisé par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="ecc71-510">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span> <span data-ttu-id="ecc71-511">L’option d' [ \_ indicateurs de \_ demande \_ d’option Internet](/windows) peut prendre l’une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="ecc71-511">The [INTERNET\_OPTION\_REQUEST\_FLAGS](/windows) option can be one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="ecc71-512"><span id="INTERNET_REQFLAG_ASYNC"></span><span id="internet_reqflag_async"></span>INTERNET \_ REQFLAG \_ Async</span><span class="sxs-lookup"><span data-stu-id="ecc71-512"><span id="INTERNET_REQFLAG_ASYNC"></span><span id="internet_reqflag_async"></span>INTERNET\_REQFLAG\_ASYNC</span></span>
</dt> <dd>

<span data-ttu-id="ecc71-513">0x00000002</span><span class="sxs-lookup"><span data-stu-id="ecc71-513">0x00000002</span></span>

<span data-ttu-id="ecc71-514">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="ecc71-514">Not implemented.</span></span>

</dd> <dt>

<span data-ttu-id="ecc71-515"><span id="INTERNET_REQFLAG_CACHE_WRITE_DISABLED"></span><span id="internet_reqflag_cache_write_disabled"></span>\_ \_ écriture du cache Internet REQFLAG \_ \_ désactivée</span><span class="sxs-lookup"><span data-stu-id="ecc71-515"><span id="INTERNET_REQFLAG_CACHE_WRITE_DISABLED"></span><span id="internet_reqflag_cache_write_disabled"></span>INTERNET\_REQFLAG\_CACHE\_WRITE\_DISABLED</span></span>
</dt> <dd>

<span data-ttu-id="ecc71-516">0x00000040</span><span class="sxs-lookup"><span data-stu-id="ecc71-516">0x00000040</span></span>

<span data-ttu-id="ecc71-517">La demande Internet ne peut pas être mise en cache (une requête HTTPs, par exemple).</span><span class="sxs-lookup"><span data-stu-id="ecc71-517">Internet request cannot be cached (an HTTPS request, for example).</span></span>

</dd> <dt>

<span data-ttu-id="ecc71-518"><span id="INTERNET_REQFLAG_FROM_CACHE"></span><span id="internet_reqflag_from_cache"></span>INTERNET \_ REQFLAG \_ à partir du \_ cache</span><span class="sxs-lookup"><span data-stu-id="ecc71-518"><span id="INTERNET_REQFLAG_FROM_CACHE"></span><span id="internet_reqflag_from_cache"></span>INTERNET\_REQFLAG\_FROM\_CACHE</span></span>
</dt> <dd>

<span data-ttu-id="ecc71-519">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ecc71-519">0x00000001</span></span>

<span data-ttu-id="ecc71-520">La réponse provient du cache.</span><span class="sxs-lookup"><span data-stu-id="ecc71-520">Response came from the cache.</span></span>

</dd> <dt>

<span data-ttu-id="ecc71-521"><span id="INTERNET_REQFLAG_NET_TIMEOUT"></span><span id="internet_reqflag_net_timeout"></span>\_ \_ \_ délai d’expiration réseau Internet REQFLAG</span><span class="sxs-lookup"><span data-stu-id="ecc71-521"><span id="INTERNET_REQFLAG_NET_TIMEOUT"></span><span id="internet_reqflag_net_timeout"></span>INTERNET\_REQFLAG\_NET\_TIMEOUT</span></span>
</dt> <dd>

<span data-ttu-id="ecc71-522">0x00000080</span><span class="sxs-lookup"><span data-stu-id="ecc71-522">0x00000080</span></span>

<span data-ttu-id="ecc71-523">Délai d’attente de la demande Internet dépassé.</span><span class="sxs-lookup"><span data-stu-id="ecc71-523">Internet request timed out.</span></span>

</dd> <dt>

<span data-ttu-id="ecc71-524"><span id="INTERNET_REQFLAG_NO_HEADERS"></span><span id="internet_reqflag_no_headers"></span>INTERNET \_ REQFLAG \_ aucun \_ en-tête</span><span class="sxs-lookup"><span data-stu-id="ecc71-524"><span id="INTERNET_REQFLAG_NO_HEADERS"></span><span id="internet_reqflag_no_headers"></span>INTERNET\_REQFLAG\_NO\_HEADERS</span></span>
</dt> <dd>

<span data-ttu-id="ecc71-525">0x00000008</span><span class="sxs-lookup"><span data-stu-id="ecc71-525">0x00000008</span></span>

<span data-ttu-id="ecc71-526">La réponse d’origine ne contenait aucun en-tête.</span><span class="sxs-lookup"><span data-stu-id="ecc71-526">Original response contained no headers.</span></span>

</dd> <dt>

<span data-ttu-id="ecc71-527"><span id="INTERNET_REQFLAG_PASSIVE"></span><span id="internet_reqflag_passive"></span>INTERNET \_ REQFLAG \_ passif</span><span class="sxs-lookup"><span data-stu-id="ecc71-527"><span id="INTERNET_REQFLAG_PASSIVE"></span><span id="internet_reqflag_passive"></span>INTERNET\_REQFLAG\_PASSIVE</span></span>
</dt> <dd>

<span data-ttu-id="ecc71-528">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ecc71-528">0x00000010</span></span>

<span data-ttu-id="ecc71-529">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="ecc71-529">Not implemented.</span></span>

</dd> <dt>

<span data-ttu-id="ecc71-530"><span id="INTERNET_REQFLAG_VIA_PROXY"></span><span id="internet_reqflag_via_proxy"></span>INTERNET \_ REQFLAG \_ via le \_ proxy</span><span class="sxs-lookup"><span data-stu-id="ecc71-530"><span id="INTERNET_REQFLAG_VIA_PROXY"></span><span id="internet_reqflag_via_proxy"></span>INTERNET\_REQFLAG\_VIA\_PROXY</span></span>
</dt> <dd>

<span data-ttu-id="ecc71-531">0x00000004</span><span class="sxs-lookup"><span data-stu-id="ecc71-531">0x00000004</span></span>

<span data-ttu-id="ecc71-532">La demande a été effectuée via un proxy.</span><span class="sxs-lookup"><span data-stu-id="ecc71-532">Request was made through a proxy.</span></span>

</dd> </dl>

</dl> </dd> <dt>

<span data-ttu-id="ecc71-533"><span id="INTERNET_OPTION_REQUEST_PRIORITY"></span><span id="internet_option_request_priority"></span>**priorité de la \_ demande d’option Internet \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ecc71-533"><span id="INTERNET_OPTION_REQUEST_PRIORITY"></span><span id="internet_option_request_priority"></span>**INTERNET\_OPTION\_REQUEST\_PRIORITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-534">58</span><span class="sxs-lookup"><span data-stu-id="ecc71-534">58</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-535">Définit ou récupère une valeur d’entier long non signé qui contient la priorité des demandes qui sont en concurrence pour une connexion sur un handle HTTP.</span><span class="sxs-lookup"><span data-stu-id="ecc71-535">Sets or retrieves an unsigned long integer value that contains the priority of requests that compete for a connection on an HTTP handle.</span></span> <span data-ttu-id="ecc71-536">Utilisé par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) et [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="ecc71-536">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-537"><span id="INTERNET_OPTION_RESET_URLCACHE_SESSION"></span><span id="internet_option_reset_urlcache_session"></span>**\_option Internet \_ Réinitialiser \_ la \_ session URLCACHE**</span><span class="sxs-lookup"><span data-stu-id="ecc71-537"><span id="INTERNET_OPTION_RESET_URLCACHE_SESSION"></span><span id="internet_option_reset_urlcache_session"></span>**INTERNET\_OPTION\_RESET\_URLCACHE\_SESSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-538">60</span><span class="sxs-lookup"><span data-stu-id="ecc71-538">60</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-539">Démarre une nouvelle session de cache pour le processus.</span><span class="sxs-lookup"><span data-stu-id="ecc71-539">Starts a new cache session for the process.</span></span> <span data-ttu-id="ecc71-540">Aucune mémoire tampon n’est requise.</span><span class="sxs-lookup"><span data-stu-id="ecc71-540">No buffer is required.</span></span> <span data-ttu-id="ecc71-541">Utilisé par [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="ecc71-541">This is used by [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="ecc71-542">Cette option est réservée à un usage interne uniquement.</span><span class="sxs-lookup"><span data-stu-id="ecc71-542">This option is reserved for internal use only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-543"><span id="INTERNET_OPTION_SECONDARY_CACHE_KEY"></span><span id="internet_option_secondary_cache_key"></span>**\_clé de \_ \_ cache secondaire \_ de l’option Internet**</span><span class="sxs-lookup"><span data-stu-id="ecc71-543"><span id="INTERNET_OPTION_SECONDARY_CACHE_KEY"></span><span id="internet_option_secondary_cache_key"></span>**INTERNET\_OPTION\_SECONDARY\_CACHE\_KEY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-544">53</span><span class="sxs-lookup"><span data-stu-id="ecc71-544">53</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-545">Définit ou récupère une valeur de chaîne qui contient la clé de cache secondaire.</span><span class="sxs-lookup"><span data-stu-id="ecc71-545">Sets or retrieves a string value that contains the secondary cache key.</span></span> <span data-ttu-id="ecc71-546">Utilisé par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) et [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="ecc71-546">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span> <span data-ttu-id="ecc71-547">Cette option est réservée à un usage interne uniquement.</span><span class="sxs-lookup"><span data-stu-id="ecc71-547">This option is reserved for internal use only.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-548"><span id="INTERNET_OPTION_SECURITY_CERTIFICATE"></span><span id="internet_option_security_certificate"></span>**certificat de sécurité de l' \_ option Internet \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ecc71-548"><span id="INTERNET_OPTION_SECURITY_CERTIFICATE"></span><span id="internet_option_security_certificate"></span>**INTERNET\_OPTION\_SECURITY\_CERTIFICATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-549">35</span><span class="sxs-lookup"><span data-stu-id="ecc71-549">35</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-550">Récupère le certificat pour un serveur de technologie de communications SSL/PCT (SSL (Secure Sockets Layer)/Private) dans une chaîne formatée.</span><span class="sxs-lookup"><span data-stu-id="ecc71-550">Retrieves the certificate for an SSL/PCT (Secure Sockets Layer/Private Communications Technology) server into a formatted string.</span></span> <span data-ttu-id="ecc71-551">Utilisé par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="ecc71-551">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-552"><span id="INTERNET_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="internet_option_security_certificate_struct"></span>**\_structure de \_ certificat de sécurité \_ \_ de l’option Internet**</span><span class="sxs-lookup"><span data-stu-id="ecc71-552"><span id="INTERNET_OPTION_SECURITY_CERTIFICATE_STRUCT"></span><span id="internet_option_security_certificate_struct"></span>**INTERNET\_OPTION\_SECURITY\_CERTIFICATE\_STRUCT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-553">32</span><span class="sxs-lookup"><span data-stu-id="ecc71-553">32</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-554">Récupère le certificat pour un serveur SSL/PCT dans la structure des \_ informations de certificat Internet \_ .</span><span class="sxs-lookup"><span data-stu-id="ecc71-554">Retrieves the certificate for an SSL/PCT server into the INTERNET\_CERTIFICATE\_INFO structure.</span></span> <span data-ttu-id="ecc71-555">Utilisé par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="ecc71-555">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-556"><span id="INTERNET_OPTION_SECURITY_FLAGS"></span><span id="internet_option_security_flags"></span>**indicateurs de sécurité de l' \_ option Internet \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ecc71-556"><span id="INTERNET_OPTION_SECURITY_FLAGS"></span><span id="internet_option_security_flags"></span>**INTERNET\_OPTION\_SECURITY\_FLAGS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-557">31</span><span class="sxs-lookup"><span data-stu-id="ecc71-557">31</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-558">Récupère une valeur d’entier long non signé qui contient les indicateurs de sécurité d’un handle.</span><span class="sxs-lookup"><span data-stu-id="ecc71-558">Retrieves an unsigned long integer value that contains the security flags for a handle.</span></span> <span data-ttu-id="ecc71-559">Cette option est utilisée par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="ecc71-559">This option is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span> <span data-ttu-id="ecc71-560">Il peut s’agir d’une combinaison des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="ecc71-560">It can be a combination of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="ecc71-561"><span id="SECURITY_FLAG_128BIT"></span><span id="security_flag_128bit"></span>Indicateur de sécurité \_ \_ 128 bits</span><span class="sxs-lookup"><span data-stu-id="ecc71-561"><span id="SECURITY_FLAG_128BIT"></span><span id="security_flag_128bit"></span>SECURITY\_FLAG\_128BIT</span></span>
</dt> <dd>

<span data-ttu-id="ecc71-562">0x20000000</span><span class="sxs-lookup"><span data-stu-id="ecc71-562">0x20000000</span></span>

<span data-ttu-id="ecc71-563">Identique à la valeur par défaut intensité de l' [indicateur de sécurité \_ \_ \_ forte](/windows).</span><span class="sxs-lookup"><span data-stu-id="ecc71-563">Identical to the preferred value [SECURITY\_FLAG\_STRENGTH\_STRONG](/windows).</span></span> <span data-ttu-id="ecc71-564">Cela est retourné uniquement dans un appel à [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="ecc71-564">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> <dt>

<span data-ttu-id="ecc71-565"><span id="SECURITY_FLAG_40BIT"></span><span id="security_flag_40bit"></span>Indicateur de sécurité \_ \_ 40BIT</span><span class="sxs-lookup"><span data-stu-id="ecc71-565"><span id="SECURITY_FLAG_40BIT"></span><span id="security_flag_40bit"></span>SECURITY\_FLAG\_40BIT</span></span>
</dt> <dd>

<span data-ttu-id="ecc71-566">0x10000000</span><span class="sxs-lookup"><span data-stu-id="ecc71-566">0x10000000</span></span>

<span data-ttu-id="ecc71-567">Identique à la valeur préférée [force de l’indicateur de sécurité \_ \_ \_ faible](/windows).</span><span class="sxs-lookup"><span data-stu-id="ecc71-567">Identical to the preferred value [SECURITY\_FLAG\_STRENGTH\_WEAK](/windows).</span></span> <span data-ttu-id="ecc71-568">Cela est retourné uniquement dans un appel à [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="ecc71-568">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> <dt>

<span data-ttu-id="ecc71-569"><span id="SECURITY_FLAG_56BIT"></span><span id="security_flag_56bit"></span>Indicateur de sécurité \_ \_ 56BIT</span><span class="sxs-lookup"><span data-stu-id="ecc71-569"><span id="SECURITY_FLAG_56BIT"></span><span id="security_flag_56bit"></span>SECURITY\_FLAG\_56BIT</span></span>
</dt> <dd>

<span data-ttu-id="ecc71-570">0x40000000</span><span class="sxs-lookup"><span data-stu-id="ecc71-570">0x40000000</span></span>

<span data-ttu-id="ecc71-571">Identique au niveau de performance de l’indicateur de sécurité de valeur par défaut. [ \_ \_ \_ ](/windows)</span><span class="sxs-lookup"><span data-stu-id="ecc71-571">Identical to the preferred value [SECURITY\_FLAG\_STRENGTH\_MEDIUM](/windows).</span></span> <span data-ttu-id="ecc71-572">Cela est retourné uniquement dans un appel à [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="ecc71-572">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> <dt>

<span data-ttu-id="ecc71-573"><span id="SECURITY_FLAG_FORTEZZA"></span><span id="security_flag_fortezza"></span>indicateur de sécurité \_ \_ Fortezza</span><span class="sxs-lookup"><span data-stu-id="ecc71-573"><span id="SECURITY_FLAG_FORTEZZA"></span><span id="security_flag_fortezza"></span>SECURITY\_FLAG\_FORTEZZA</span></span>
</dt> <dd>

<span data-ttu-id="ecc71-574">0x08000000</span><span class="sxs-lookup"><span data-stu-id="ecc71-574">0x08000000</span></span>

<span data-ttu-id="ecc71-575">Indique que Fortezza a été utilisé pour assurer le secret, l’authentification et/ou l’intégrité de la connexion spécifiée.</span><span class="sxs-lookup"><span data-stu-id="ecc71-575">Indicates Fortezza has been used to provide secrecy, authentication, and/or integrity for the specified connection.</span></span>

</dd> <dt>

<span data-ttu-id="ecc71-576"><span id="SECURITY_FLAG_IETFSSL4"></span><span id="security_flag_ietfssl4"></span>Indicateur de sécurité \_ \_ IETFSSL4</span><span class="sxs-lookup"><span data-stu-id="ecc71-576"><span id="SECURITY_FLAG_IETFSSL4"></span><span id="security_flag_ietfssl4"></span>SECURITY\_FLAG\_IETFSSL4</span></span>
</dt> <dd>

<span data-ttu-id="ecc71-577">0x00000020</span><span class="sxs-lookup"><span data-stu-id="ecc71-577">0x00000020</span></span>

<span data-ttu-id="ecc71-578">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="ecc71-578">Not implemented.</span></span>

</dd> <dt>

<span data-ttu-id="ecc71-579"><span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>indicateur de sécurité ignorer le nom \_ \_ commun du \_ certificat \_ \_ non valide</span><span class="sxs-lookup"><span data-stu-id="ecc71-579"><span id="SECURITY_FLAG_IGNORE_CERT_CN_INVALID"></span><span id="security_flag_ignore_cert_cn_invalid"></span>SECURITY\_FLAG\_IGNORE\_CERT\_CN\_INVALID</span></span>
</dt> <dd>

<span data-ttu-id="ecc71-580">0x00001000</span><span class="sxs-lookup"><span data-stu-id="ecc71-580">0x00001000</span></span>

<span data-ttu-id="ecc71-581">Ignore le message d’erreur erreur [ \_ \_ \_ \_ \_ non valide du certificat d’Internet s](wininet-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="ecc71-581">Ignores the [ERROR\_INTERNET\_SEC\_CERT\_CN\_INVALID](wininet-errors.md) error message.</span></span>

</dd> <dt>

<span data-ttu-id="ecc71-582"><span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>indicateur de sécurité \_ \_ ignore la \_ Date de certificat \_ \_ non valide</span><span class="sxs-lookup"><span data-stu-id="ecc71-582"><span id="SECURITY_FLAG_IGNORE_CERT_DATE_INVALID"></span><span id="security_flag_ignore_cert_date_invalid"></span>SECURITY\_FLAG\_IGNORE\_CERT\_DATE\_INVALID</span></span>
</dt> <dd>

<span data-ttu-id="ecc71-583">0x00002000</span><span class="sxs-lookup"><span data-stu-id="ecc71-583">0x00002000</span></span>

<span data-ttu-id="ecc71-584">Ignore le message d’erreur [erreur \_ Internet \_ s \_ CERT \_ date \_ non valide](wininet-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="ecc71-584">Ignores the [ERROR\_INTERNET\_SEC\_CERT\_DATE\_INVALID](wininet-errors.md) error message.</span></span>

</dd> <dt>

<span data-ttu-id="ecc71-585"><span id="SECURITY_FLAG_IGNORE_REDIRECT_TO_HTTP"></span><span id="security_flag_ignore_redirect_to_http"></span>\_indicateur \_ de sécurité ignorer \_ la redirection \_ vers \_ http</span><span class="sxs-lookup"><span data-stu-id="ecc71-585"><span id="SECURITY_FLAG_IGNORE_REDIRECT_TO_HTTP"></span><span id="security_flag_ignore_redirect_to_http"></span>SECURITY\_FLAG\_IGNORE\_REDIRECT\_TO\_HTTP</span></span>
</dt> <dd>

<span data-ttu-id="ecc71-586">0x00008000</span><span class="sxs-lookup"><span data-stu-id="ecc71-586">0x00008000</span></span>

<span data-ttu-id="ecc71-587">Ignore l' [erreur \_ Internet \_ https \_ à \_ http \_ sur le message d’erreur de \_ ReDim](wininet-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="ecc71-587">Ignores the [ERROR\_INTERNET\_HTTPS\_TO\_HTTP\_ON\_REDIR](wininet-errors.md) error message.</span></span>

</dd> <dt>

<span data-ttu-id="ecc71-588"><span id="SECURITY_FLAG_IGNORE_REDIRECT_TO_HTTPS"></span><span id="security_flag_ignore_redirect_to_https"></span>\_indicateur \_ de sécurité ignorer \_ la redirection \_ vers \_ https</span><span class="sxs-lookup"><span data-stu-id="ecc71-588"><span id="SECURITY_FLAG_IGNORE_REDIRECT_TO_HTTPS"></span><span id="security_flag_ignore_redirect_to_https"></span>SECURITY\_FLAG\_IGNORE\_REDIRECT\_TO\_HTTPS</span></span>
</dt> <dd>

<span data-ttu-id="ecc71-589">0x00004000</span><span class="sxs-lookup"><span data-stu-id="ecc71-589">0x00004000</span></span>

<span data-ttu-id="ecc71-590">Ignore l' [erreur \_ Internet \_ http \_ à \_ https \_ sur le message d’erreur de \_ ReDim](wininet-errors.md) .</span><span class="sxs-lookup"><span data-stu-id="ecc71-590">Ignores the [ERROR\_INTERNET\_HTTP\_TO\_HTTPS\_ON\_REDIR](wininet-errors.md) error message.</span></span>

</dd> <dt>

<span data-ttu-id="ecc71-591"><span id="SECURITY_FLAG_IGNORE_REVOCATION"></span><span id="security_flag_ignore_revocation"></span>indicateur de sécurité \_ \_ ignore la \_ révocation</span><span class="sxs-lookup"><span data-stu-id="ecc71-591"><span id="SECURITY_FLAG_IGNORE_REVOCATION"></span><span id="security_flag_ignore_revocation"></span>SECURITY\_FLAG\_IGNORE\_REVOCATION</span></span>
</dt> <dd>

<span data-ttu-id="ecc71-592">0x00000080</span><span class="sxs-lookup"><span data-stu-id="ecc71-592">0x00000080</span></span>

<span data-ttu-id="ecc71-593">Ignore les problèmes de révocation de certificat.</span><span class="sxs-lookup"><span data-stu-id="ecc71-593">Ignores certificate revocation problems.</span></span>

</dd> <dt>

<span data-ttu-id="ecc71-594"><span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>indicateur de sécurité \_ \_ ignorer l’autorité de \_ \_ certification inconnue</span><span class="sxs-lookup"><span data-stu-id="ecc71-594"><span id="SECURITY_FLAG_IGNORE_UNKNOWN_CA"></span><span id="security_flag_ignore_unknown_ca"></span>SECURITY\_FLAG\_IGNORE\_UNKNOWN\_CA</span></span>
</dt> <dd>

<span data-ttu-id="ecc71-595">0x00000100</span><span class="sxs-lookup"><span data-stu-id="ecc71-595">0x00000100</span></span>

<span data-ttu-id="ecc71-596">Ignore les problèmes d’autorité de certification inconnus.</span><span class="sxs-lookup"><span data-stu-id="ecc71-596">Ignores unknown certificate authority problems.</span></span>

</dd> <dt>

<span data-ttu-id="ecc71-597"><span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>indicateur de sécurité \_ \_ ignorer la \_ \_ signature faible</span><span class="sxs-lookup"><span data-stu-id="ecc71-597"><span id="SECURITY_FLAG_IGNORE_WEAK_SIGNATURE"></span><span id="security_flag_ignore_weak_signature"></span>SECURITY\_FLAG\_IGNORE\_WEAK\_SIGNATURE</span></span>
</dt> <dd>

<span data-ttu-id="ecc71-598">0x00010000</span><span class="sxs-lookup"><span data-stu-id="ecc71-598">0x00010000</span></span>

<span data-ttu-id="ecc71-599">Ignore les problèmes de signature de certificat faible.</span><span class="sxs-lookup"><span data-stu-id="ecc71-599">Ignores weak certificate signature problems.</span></span>

</dd> <dt>

<span data-ttu-id="ecc71-600"><span id="SECURITY_FLAG_IGNORE_WRONG_USAGE"></span><span id="security_flag_ignore_wrong_usage"></span>indicateur de sécurité \_ \_ ignorant \_ l’utilisation incorrecte \_</span><span class="sxs-lookup"><span data-stu-id="ecc71-600"><span id="SECURITY_FLAG_IGNORE_WRONG_USAGE"></span><span id="security_flag_ignore_wrong_usage"></span>SECURITY\_FLAG\_IGNORE\_WRONG\_USAGE</span></span>
</dt> <dd>

<span data-ttu-id="ecc71-601">0x00000200</span><span class="sxs-lookup"><span data-stu-id="ecc71-601">0x00000200</span></span>

<span data-ttu-id="ecc71-602">Ignore les problèmes d’utilisation incorrects.</span><span class="sxs-lookup"><span data-stu-id="ecc71-602">Ignores incorrect usage problems.</span></span>

</dd> <dt>

<span data-ttu-id="ecc71-603"><span id="SECURITY_FLAG_NORMALBITNESS"></span><span id="security_flag_normalbitness"></span>indicateur de sécurité \_ \_ NORMALBITNESS</span><span class="sxs-lookup"><span data-stu-id="ecc71-603"><span id="SECURITY_FLAG_NORMALBITNESS"></span><span id="security_flag_normalbitness"></span>SECURITY\_FLAG\_NORMALBITNESS</span></span>
</dt> <dd>

<span data-ttu-id="ecc71-604">0x10000000</span><span class="sxs-lookup"><span data-stu-id="ecc71-604">0x10000000</span></span>

<span data-ttu-id="ecc71-605">Identique à la valeur [ \_ \_ \_ faible force](/windows)de l’indicateur de sécurité.</span><span class="sxs-lookup"><span data-stu-id="ecc71-605">Identical to the value [SECURITY\_FLAG\_STRENGTH\_WEAK](/windows).</span></span> <span data-ttu-id="ecc71-606">Cela est retourné uniquement dans un appel à [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="ecc71-606">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> <dt>

<span data-ttu-id="ecc71-607"><span id="SECURITY_FLAG_PCT"></span><span id="security_flag_pct"></span>indicateur de sécurité \_ \_ PCT</span><span class="sxs-lookup"><span data-stu-id="ecc71-607"><span id="SECURITY_FLAG_PCT"></span><span id="security_flag_pct"></span>SECURITY\_FLAG\_PCT</span></span>
</dt> <dd>

<span data-ttu-id="ecc71-608">0x00000008</span><span class="sxs-lookup"><span data-stu-id="ecc71-608">0x00000008</span></span>

<span data-ttu-id="ecc71-609">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="ecc71-609">Not implemented.</span></span>

</dd> <dt>

<span data-ttu-id="ecc71-610"><span id="SECURITY_FLAG_PCT4"></span><span id="security_flag_pct4"></span>Indicateur de sécurité \_ \_ PCT4</span><span class="sxs-lookup"><span data-stu-id="ecc71-610"><span id="SECURITY_FLAG_PCT4"></span><span id="security_flag_pct4"></span>SECURITY\_FLAG\_PCT4</span></span>
</dt> <dd>

<span data-ttu-id="ecc71-611">0x00000010</span><span class="sxs-lookup"><span data-stu-id="ecc71-611">0x00000010</span></span>

<span data-ttu-id="ecc71-612">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="ecc71-612">Not implemented.</span></span>

</dd> <dt>

<span data-ttu-id="ecc71-613"><span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>indicateur de sécurité \_ \_ sécurisé</span><span class="sxs-lookup"><span data-stu-id="ecc71-613"><span id="SECURITY_FLAG_SECURE"></span><span id="security_flag_secure"></span>SECURITY\_FLAG\_SECURE</span></span>
</dt> <dd>

<span data-ttu-id="ecc71-614">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ecc71-614">0x00000001</span></span>

<span data-ttu-id="ecc71-615">Utilise des transferts sécurisés.</span><span class="sxs-lookup"><span data-stu-id="ecc71-615">Uses secure transfers.</span></span> <span data-ttu-id="ecc71-616">Cela est retourné uniquement dans un appel à [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="ecc71-616">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> <dt>

<span data-ttu-id="ecc71-617"><span id="SECURITY_FLAG_SSL"></span><span id="security_flag_ssl"></span>indicateur de sécurité \_ \_ SSL</span><span class="sxs-lookup"><span data-stu-id="ecc71-617"><span id="SECURITY_FLAG_SSL"></span><span id="security_flag_ssl"></span>SECURITY\_FLAG\_SSL</span></span>
</dt> <dd>

<span data-ttu-id="ecc71-618">0x00000002</span><span class="sxs-lookup"><span data-stu-id="ecc71-618">0x00000002</span></span>

<span data-ttu-id="ecc71-619">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="ecc71-619">Not implemented.</span></span>

</dd> <dt>

<span data-ttu-id="ecc71-620"><span id="SECURITY_FLAG_SSL3"></span><span id="security_flag_ssl3"></span>Indicateur de sécurité \_ \_ SSL3</span><span class="sxs-lookup"><span data-stu-id="ecc71-620"><span id="SECURITY_FLAG_SSL3"></span><span id="security_flag_ssl3"></span>SECURITY\_FLAG\_SSL3</span></span>
</dt> <dd>

<span data-ttu-id="ecc71-621">0x00000004</span><span class="sxs-lookup"><span data-stu-id="ecc71-621">0x00000004</span></span>

<span data-ttu-id="ecc71-622">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="ecc71-622">Not implemented.</span></span>

</dd> <dt>

<span data-ttu-id="ecc71-623"><span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>niveau de force de l’indicateur de sécurité \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="ecc71-623"><span id="SECURITY_FLAG_STRENGTH_MEDIUM"></span><span id="security_flag_strength_medium"></span>SECURITY\_FLAG\_STRENGTH\_MEDIUM</span></span>
</dt> <dd>

<span data-ttu-id="ecc71-624">0x40000000</span><span class="sxs-lookup"><span data-stu-id="ecc71-624">0x40000000</span></span>

<span data-ttu-id="ecc71-625">Utilise le chiffrement moyen (56 bits).</span><span class="sxs-lookup"><span data-stu-id="ecc71-625">Uses medium (56-bit) encryption.</span></span> <span data-ttu-id="ecc71-626">Cela est retourné uniquement dans un appel à [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="ecc71-626">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> <dt>

<span data-ttu-id="ecc71-627"><span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>force de l’indicateur de sécurité \_ \_ \_ Strong</span><span class="sxs-lookup"><span data-stu-id="ecc71-627"><span id="SECURITY_FLAG_STRENGTH_STRONG"></span><span id="security_flag_strength_strong"></span>SECURITY\_FLAG\_STRENGTH\_STRONG</span></span>
</dt> <dd>

<span data-ttu-id="ecc71-628">0x20000000</span><span class="sxs-lookup"><span data-stu-id="ecc71-628">0x20000000</span></span>

<span data-ttu-id="ecc71-629">Utilise le chiffrement fort (128 bits).</span><span class="sxs-lookup"><span data-stu-id="ecc71-629">Uses strong (128-bit) encryption.</span></span> <span data-ttu-id="ecc71-630">Cela est retourné uniquement dans un appel à [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="ecc71-630">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> <dt>

<span data-ttu-id="ecc71-631"><span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>force de l’indicateur de sécurité \_ \_ \_ faible</span><span class="sxs-lookup"><span data-stu-id="ecc71-631"><span id="SECURITY_FLAG_STRENGTH_WEAK"></span><span id="security_flag_strength_weak"></span>SECURITY\_FLAG\_STRENGTH\_WEAK</span></span>
</dt> <dd>

<span data-ttu-id="ecc71-632">0x10000000</span><span class="sxs-lookup"><span data-stu-id="ecc71-632">0x10000000</span></span>

<span data-ttu-id="ecc71-633">Utilise un chiffrement faible (40 bits).</span><span class="sxs-lookup"><span data-stu-id="ecc71-633">Uses weak (40-bit) encryption.</span></span> <span data-ttu-id="ecc71-634">Cela est retourné uniquement dans un appel à [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="ecc71-634">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> <dt>

<span data-ttu-id="ecc71-635"><span id="SECURITY_FLAG_UNKNOWNBIT"></span><span id="security_flag_unknownbit"></span>indicateur de sécurité \_ \_ UNKNOWNBIT</span><span class="sxs-lookup"><span data-stu-id="ecc71-635"><span id="SECURITY_FLAG_UNKNOWNBIT"></span><span id="security_flag_unknownbit"></span>SECURITY\_FLAG\_UNKNOWNBIT</span></span>
</dt> <dd>

<span data-ttu-id="ecc71-636">0x80000000</span><span class="sxs-lookup"><span data-stu-id="ecc71-636">0x80000000</span></span>

<span data-ttu-id="ecc71-637">La taille en bits utilisée dans le chiffrement est inconnue.</span><span class="sxs-lookup"><span data-stu-id="ecc71-637">The bit size used in the encryption is unknown.</span></span> <span data-ttu-id="ecc71-638">Cela est retourné uniquement dans un appel à [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="ecc71-638">This is only returned in a call to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>

</dd> </dl>

<span data-ttu-id="ecc71-639">Sachez que les données récupérées de cette façon sont liées à une transaction qui s’est produite, dont le niveau de sécurité ne peut plus être modifié.</span><span class="sxs-lookup"><span data-stu-id="ecc71-639">Be aware that the data retrieved this way relates to a transaction that has occurred, whose security level can no longer be changed.</span></span>

</dl> </dd> <dt>

<span data-ttu-id="ecc71-640"><span id="INTERNET_OPTION_SECURITY_KEY_BITNESS"></span><span id="internet_option_security_key_bitness"></span>**nombre de bits de la clé de sécurité de l' \_ option Internet \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ecc71-640"><span id="INTERNET_OPTION_SECURITY_KEY_BITNESS"></span><span id="internet_option_security_key_bitness"></span>**INTERNET\_OPTION\_SECURITY\_KEY\_BITNESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-641">36</span><span class="sxs-lookup"><span data-stu-id="ecc71-641">36</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-642">Récupère une valeur d’entier long non signé qui contient la taille en bits de la clé de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="ecc71-642">Retrieves an unsigned long integer value that contains the bit size of the encryption key.</span></span> <span data-ttu-id="ecc71-643">Plus le nombre est élevé, plus la force de chiffrement utilisée est élevée.</span><span class="sxs-lookup"><span data-stu-id="ecc71-643">The larger the number, the greater the encryption strength used.</span></span> <span data-ttu-id="ecc71-644">Utilisé par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="ecc71-644">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span> <span data-ttu-id="ecc71-645">Sachez que les données récupérées de cette façon sont liées à une transaction qui s’est déjà produite, dont le niveau de sécurité ne peut plus être modifié.</span><span class="sxs-lookup"><span data-stu-id="ecc71-645">Be aware that the data retrieved this way relates to a transaction that has already occurred, whose security level can no longer be changed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-646"><span id="INTERNET_OPTION_SEND_THROUGHPUT"></span><span id="internet_option_send_throughput"></span>**\_débit d' \_ envoi des options Internet \_**</span><span class="sxs-lookup"><span data-stu-id="ecc71-646"><span id="INTERNET_OPTION_SEND_THROUGHPUT"></span><span id="internet_option_send_throughput"></span>**INTERNET\_OPTION\_SEND\_THROUGHPUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-647">56</span><span class="sxs-lookup"><span data-stu-id="ecc71-647">56</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-648">Non implémenté.</span><span class="sxs-lookup"><span data-stu-id="ecc71-648">Not implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-649"><span id="INTERNET_OPTION_SEND_TIMEOUT"></span><span id="internet_option_send_timeout"></span>**\_ \_ \_ délai d’attente d’envoi des options Internet**</span><span class="sxs-lookup"><span data-stu-id="ecc71-649"><span id="INTERNET_OPTION_SEND_TIMEOUT"></span><span id="internet_option_send_timeout"></span>**INTERNET\_OPTION\_SEND\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-650">5</span><span class="sxs-lookup"><span data-stu-id="ecc71-650">5</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-651">Définit ou récupère une valeur d’entier long non signé, en millisecondes, qui contient la valeur du délai d’attente pour envoyer une demande.</span><span class="sxs-lookup"><span data-stu-id="ecc71-651">Sets or retrieves an unsigned long integer value, in milliseconds, that contains the time-out value to send a request.</span></span> <span data-ttu-id="ecc71-652">Si l’envoi prend plus de temps que cette valeur de délai d’attente, l’envoi est annulé.</span><span class="sxs-lookup"><span data-stu-id="ecc71-652">If the send takes longer than this time-out value, the send is canceled.</span></span> <span data-ttu-id="ecc71-653">Cette option peut être utilisée sur n’importe quel handle [**HINTERNET**](appendix-a-hinternet-handles.md) , y compris un handle **null** .</span><span class="sxs-lookup"><span data-stu-id="ecc71-653">This option can be used on any [**HINTERNET**](appendix-a-hinternet-handles.md) handle, including a **NULL** handle.</span></span> <span data-ttu-id="ecc71-654">Elle est utilisée par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) et [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="ecc71-654">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>

<span data-ttu-id="ecc71-655">Lorsqu’elle est utilisée en référence à une transaction FTP, cette option fait référence au canal de contrôle.</span><span class="sxs-lookup"><span data-stu-id="ecc71-655">When used in reference to an FTP transaction, this option refers to the control channel.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-656"><span id="INTERNET_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="internet_option_server_cert_chain_context"></span>**\_contexte de \_ chaîne du certificat du serveur d’options Internet \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="ecc71-656"><span id="INTERNET_OPTION_SERVER_CERT_CHAIN_CONTEXT"></span><span id="internet_option_server_cert_chain_context"></span>**INTERNET\_OPTION\_SERVER\_CERT\_CHAIN\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-657">105</span><span class="sxs-lookup"><span data-stu-id="ecc71-657">105</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-658">Récupère le contexte de la chaîne de certificats du serveur en tant que [ \_ \_ contexte de chaîne PCCERT](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context)en double.</span><span class="sxs-lookup"><span data-stu-id="ecc71-658">Retrieves the server s certificate-chain context as a duplicated [PCCERT\_CHAIN\_CONTEXT](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context).</span></span> <span data-ttu-id="ecc71-659">Vous pouvez passer ce contexte dupliqué à toute fonction API de chiffrement qui prend [un \_ \_ contexte de chaîne PCCERT](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context).</span><span class="sxs-lookup"><span data-stu-id="ecc71-659">You may pass this duplicated context to any Crypto API function which takes a [PCCERT\_CHAIN\_CONTEXT](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context).</span></span> <span data-ttu-id="ecc71-660">Vous devez appeler [**CertFreeCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatechain) sur le [contexte de \_ chaîne \_ PCCERT](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context) retourné lorsque vous avez terminé avec le contexte de la chaîne de certificats.</span><span class="sxs-lookup"><span data-stu-id="ecc71-660">You must call [**CertFreeCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatechain) on the returned [PCCERT\_CHAIN\_CONTEXT](/windows/win32/api/wincrypt/ns-wincrypt-cert_chain_context) when you are done with the certificate-chain context.</span></span>

<span data-ttu-id="ecc71-661">**Version :** Nécessite Internet Explorer 8,0.</span><span class="sxs-lookup"><span data-stu-id="ecc71-661">**Version:** Requires Internet Explorer 8.0.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-662"><span id="INTERNET_OPTION_SETTINGS_CHANGED"></span><span id="internet_option_settings_changed"></span>**\_paramètres d’option Internet \_ \_ modifiés**</span><span class="sxs-lookup"><span data-stu-id="ecc71-662"><span id="INTERNET_OPTION_SETTINGS_CHANGED"></span><span id="internet_option_settings_changed"></span>**INTERNET\_OPTION\_SETTINGS\_CHANGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-663">39</span><span class="sxs-lookup"><span data-stu-id="ecc71-663">39</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-664">Informe le système que les paramètres du Registre ont été modifiés afin qu’il vérifie les paramètres lors de l’appel suivant à [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="ecc71-664">Notifies the system that the registry settings have been changed so that it verifies the settings on the next call to [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span> <span data-ttu-id="ecc71-665">Utilisé par [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="ecc71-665">This is used by [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-666"><span id="INTERNET_OPTION_SUPPRESS_SERVER_AUTH"></span><span id="internet_option_suppress_server_auth"></span>**\_option Internet \_ supprimer \_ l' \_ authentification du serveur**</span><span class="sxs-lookup"><span data-stu-id="ecc71-666"><span id="INTERNET_OPTION_SUPPRESS_SERVER_AUTH"></span><span id="internet_option_suppress_server_auth"></span>**INTERNET\_OPTION\_SUPPRESS\_SERVER\_AUTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-667">104</span><span class="sxs-lookup"><span data-stu-id="ecc71-667">104</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-668">Définit un objet de requête HTTP de sorte qu’il ne se connecte pas aux serveurs d’origine, mais effectue une ouverture de session automatique sur les serveurs proxy HTTP.</span><span class="sxs-lookup"><span data-stu-id="ecc71-668">Sets an HTTP request object such that it will not logon to origin servers, but will perform automatic logon to HTTP proxy servers.</span></span> <span data-ttu-id="ecc71-669">Cette option diffère de l’indicateur de requête **Internet \_ Flag \_ no \_ auth**, qui empêche l’authentification aux serveurs proxy et aux serveurs d’origine.</span><span class="sxs-lookup"><span data-stu-id="ecc71-669">This option differs from the Request flag **INTERNET\_FLAG\_NO\_AUTH**, which prevents authentication to both proxy servers and origin servers.</span></span>

<span data-ttu-id="ecc71-670">En définissant ce mode, vous supprimez l’utilisation de tout document d’informations d’identification (nom d’utilisateur/mot de passe ou certificat SSL client précédemment fourni) lors de la communication avec un serveur d’origine.</span><span class="sxs-lookup"><span data-stu-id="ecc71-670">Setting this mode will suppress the use of any credential material (either previously provided username/password or client SSL certificate) when communicating with an origin server.</span></span> <span data-ttu-id="ecc71-671">Toutefois, si la demande doit transiter via un proxy d’authentification, WinINet effectue toujours l’authentification automatique sur le proxy HTTP en fonction des paramètres de la zone Intranet de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ecc71-671">However, if the request must transit via an authenticating proxy, WinINet will still perform automatic authentication to the HTTP proxy per the Intranet Zone settings for the user.</span></span> <span data-ttu-id="ecc71-672">Le paramètre de zone Intranet par défaut permet d’autoriser l’ouverture de session automatique à l’aide des informations d’identification par défaut de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="ecc71-672">The default Intranet Zone setting is to permit automatic logon using the user s default credentials.</span></span>

<span data-ttu-id="ecc71-673">Pour garantir la suppression de toutes les informations d’identification, l’appelant doit combiner l' **\_ option Internet option \_ Supprimer l' \_ \_ authentification du serveur** avec l’indicateur de requête **Internet \_ indicateur \_ aucun \_ cookie** .</span><span class="sxs-lookup"><span data-stu-id="ecc71-673">To ensure suppression of all identifying information, the caller should combine **INTERNET\_OPTION\_SUPPRESS\_SERVER\_AUTH** with the **INTERNET\_FLAG\_NO\_COOKIES** request flag.</span></span>

<span data-ttu-id="ecc71-674">Cette option ne peut être définie que sur des objets de requête avant d’être envoyés.</span><span class="sxs-lookup"><span data-stu-id="ecc71-674">This option may only be set on request objects before they have been sent.</span></span> <span data-ttu-id="ecc71-675">Toute tentative de définition de cette option après l’envoi de la demande retourne l' **État d’erreur du \_ \_ \_ handle \_ Internet incorrect**.</span><span class="sxs-lookup"><span data-stu-id="ecc71-675">Attempts to set this option after the request has been sent will return **ERROR\_INTERNET\_INCORRECT\_HANDLE\_STATE**.</span></span>

<span data-ttu-id="ecc71-676">Aucune mémoire tampon n’est requise pour cette option.</span><span class="sxs-lookup"><span data-stu-id="ecc71-676">No buffer is required for this option.</span></span> <span data-ttu-id="ecc71-677">Cela est utilisé par [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) sur les handles retournés par [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) uniquement.</span><span class="sxs-lookup"><span data-stu-id="ecc71-677">This is used by [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) on handles returned by [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta) only.</span></span>

<span data-ttu-id="ecc71-678">**Version :** Nécessite Internet Explorer 8,0 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="ecc71-678">**Version:** Requires Internet Explorer 8.0 or later.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-679"><span id="INTERNET_OPTION_SUPPRESS_BEHAVIOR"></span><span id="internet_option_suppress_behavior"></span>**\_comportement de \_ suppression des options Internet \_**</span><span class="sxs-lookup"><span data-stu-id="ecc71-679"><span id="INTERNET_OPTION_SUPPRESS_BEHAVIOR"></span><span id="internet_option_suppress_behavior"></span>**INTERNET\_OPTION\_SUPPRESS\_BEHAVIOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-680">81</span><span class="sxs-lookup"><span data-stu-id="ecc71-680">81</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-681">Option à usage général utilisée pour supprimer les comportements à l’échelle du processus.</span><span class="sxs-lookup"><span data-stu-id="ecc71-681">A general purpose option that is used to suppress behaviors on a process-wide basis.</span></span> <span data-ttu-id="ecc71-682">Le paramètre *lpBuffer* de la fonction doit être un pointeur vers une valeur DWORD contenant le comportement spécifique à supprimer.</span><span class="sxs-lookup"><span data-stu-id="ecc71-682">The *lpBuffer* parameter of the function must be a pointer to a DWORD containing the specific behavior to suppress.</span></span> <span data-ttu-id="ecc71-683">Cette option ne peut pas être interrogée avec [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="ecc71-683">This option cannot be queried with [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span> <span data-ttu-id="ecc71-684">Les valeurs autorisées sont les suivantes :</span><span class="sxs-lookup"><span data-stu-id="ecc71-684">The permitted values are:</span></span>

<dl> <dt>

<span data-ttu-id="ecc71-685"><span id="INTERNET_SUPPRESS_RESET_ALL"></span><span id="internet_suppress_reset_all"></span>\_suppression Internet \_ Réinitialiser \_ tout</span><span class="sxs-lookup"><span data-stu-id="ecc71-685"><span id="INTERNET_SUPPRESS_RESET_ALL"></span><span id="internet_suppress_reset_all"></span>INTERNET\_SUPPRESS\_RESET\_ALL</span></span>
</dt> <dd>

<span data-ttu-id="ecc71-686">0</span><span class="sxs-lookup"><span data-stu-id="ecc71-686">0</span></span>

<span data-ttu-id="ecc71-687">Désactive toutes les suppressions, réactivation des comportements par défaut et configurés.</span><span class="sxs-lookup"><span data-stu-id="ecc71-687">Disables all suppressions, re-enabling default and configured behavior.</span></span> <span data-ttu-id="ecc71-688">Cette option est équivalente à la configuration de la **\_ \_ \_ \_ réinitialisation** de la stratégie de cookies par Internet et à la **\_ \_ \_ \_ réinitialisation permanente des cookies Internet** .</span><span class="sxs-lookup"><span data-stu-id="ecc71-688">This option is the equivalent of setting **INTERNET\_SUPPRESS\_COOKIE\_POLICY\_RESET** and **INTERNET\_SUPPRESS\_COOKIE\_PERSIST\_RESET** individually.</span></span>

<span data-ttu-id="ecc71-689">**Version :** Nécessite Internet Explorer 6,0 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="ecc71-689">**Version:** Requires Internet Explorer 6.0 or later.</span></span>

</dd> <dt>

<span data-ttu-id="ecc71-690"><span id="INTERNET_SUPPRESS_COOKIE_POLICY_"></span><span id="internet_suppress_cookie_policy_"></span>\_stratégie de \_ cookies supprimée par Internet \_</span><span class="sxs-lookup"><span data-stu-id="ecc71-690"><span id="INTERNET_SUPPRESS_COOKIE_POLICY_"></span><span id="internet_suppress_cookie_policy_"></span>INTERNET\_SUPPRESS\_COOKIE\_POLICY</span></span> 
</dt> <dd>

<span data-ttu-id="ecc71-691">1</span><span class="sxs-lookup"><span data-stu-id="ecc71-691">1</span></span>

<span data-ttu-id="ecc71-692">Ignore toutes les stratégies de cookie configurées et autorise la définition des cookies.</span><span class="sxs-lookup"><span data-stu-id="ecc71-692">Ignores any configured cookie policies and allows cookies to be set.</span></span>

<span data-ttu-id="ecc71-693">**Version :** Nécessite Internet Explorer 6,0 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="ecc71-693">**Version:** Requires Internet Explorer 6.0 or later.</span></span>

</dd> <dt>

<span data-ttu-id="ecc71-694"><span id="INTERNET_SUPPRESS_COOKIE_POLICY_RESET_"></span><span id="internet_suppress_cookie_policy_reset_"></span>suppression d’INTERNET \_ Supprimer la \_ stratégie de cookie \_ \_</span><span class="sxs-lookup"><span data-stu-id="ecc71-694"><span id="INTERNET_SUPPRESS_COOKIE_POLICY_RESET_"></span><span id="internet_suppress_cookie_policy_reset_"></span>INTERNET\_SUPPRESS\_COOKIE\_POLICY\_RESET</span></span> 
</dt> <dd>

<span data-ttu-id="ecc71-695">2</span><span class="sxs-lookup"><span data-stu-id="ecc71-695">2</span></span>

<span data-ttu-id="ecc71-696">Désactive la suppression d' **Internet \_ supprimer \_ la \_ stratégie de cookie** , en autorisant l’évaluation des cookies en fonction de la stratégie de cookie configurée.</span><span class="sxs-lookup"><span data-stu-id="ecc71-696">Disables the **INTERNET\_SUPPRESS\_COOKIE\_POLICY** suppression, permitting the evaluation of cookies according to the configured cookie policy.</span></span>

<span data-ttu-id="ecc71-697">**Version :** Nécessite Internet Explorer 6,0 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="ecc71-697">**Version:** Requires Internet Explorer 6.0 or later.</span></span>

</dd> <dt>

<span data-ttu-id="ecc71-698"><span id="__INTERNET_SUPPRESS_COOKIE_PERSIST"></span><span id="__internet_suppress_cookie_persist"></span> le \_ cookie supprimé par Internet est \_ \_ conservé</span><span class="sxs-lookup"><span data-stu-id="ecc71-698"><span id="__INTERNET_SUPPRESS_COOKIE_PERSIST"></span><span id="__internet_suppress_cookie_persist"></span> INTERNET\_SUPPRESS\_COOKIE\_PERSIST</span></span>
</dt> <dd>

<span data-ttu-id="ecc71-699">3</span><span class="sxs-lookup"><span data-stu-id="ecc71-699">3</span></span>

<span data-ttu-id="ecc71-700">Supprime la persistance des cookies, même si le serveur les a spécifiés comme persistants.</span><span class="sxs-lookup"><span data-stu-id="ecc71-700">Suppresses the persistence of cookies, even if the server has specified them as persistent.</span></span>

<span data-ttu-id="ecc71-701">**Version :** Nécessite Internet Explorer 8,0 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="ecc71-701">**Version:** Requires Internet Explorer 8.0 or later.</span></span>

</dd> <dt>

<span data-ttu-id="ecc71-702"><span id="INTERNET_SUPPRESS_COOKIE_PERSIST_RESET"></span><span id="internet_suppress_cookie_persist_reset"></span>\_ \_ \_ réinitialisation permanente des cookies supprimés d’Internet \_</span><span class="sxs-lookup"><span data-stu-id="ecc71-702"><span id="INTERNET_SUPPRESS_COOKIE_PERSIST_RESET"></span><span id="internet_suppress_cookie_persist_reset"></span>INTERNET\_SUPPRESS\_COOKIE\_PERSIST\_RESET</span></span>
</dt> <dd>

<span data-ttu-id="ecc71-703">4</span><span class="sxs-lookup"><span data-stu-id="ecc71-703">4</span></span>

<span data-ttu-id="ecc71-704">Désactive la suppression de **la \_ \_ \_ conservation de cookie Internet** , réactivation de la persistance des cookies.</span><span class="sxs-lookup"><span data-stu-id="ecc71-704">Disables the **INTERNET\_SUPPRESS\_COOKIE\_PERSIST** suppression, re-enabling the persistence of cookies.</span></span> <span data-ttu-id="ecc71-705">Les cookies précédemment supprimés ne sont pas persistants.</span><span class="sxs-lookup"><span data-stu-id="ecc71-705">Any previously suppressed cookies will not become persistent.</span></span>

<span data-ttu-id="ecc71-706">**Version :** Nécessite Internet Explorer 8,0 ou une version ultérieure.</span><span class="sxs-lookup"><span data-stu-id="ecc71-706">**Version:** Requires Internet Explorer 8.0 or later.</span></span>

</dd> </dl>

</dl> </dd> <dt>

<span data-ttu-id="ecc71-707"><span id="INTERNET_OPTION_URL"></span><span id="internet_option_url"></span>**URL de l' \_ option Internet \_**</span><span class="sxs-lookup"><span data-stu-id="ecc71-707"><span id="INTERNET_OPTION_URL"></span><span id="internet_option_url"></span>**INTERNET\_OPTION\_URL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-708">34</span><span class="sxs-lookup"><span data-stu-id="ecc71-708">34</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-709">Récupère une valeur de chaîne qui contient l’URL complète d’une ressource téléchargée.</span><span class="sxs-lookup"><span data-stu-id="ecc71-709">Retrieves a string value that contains the full URL of a downloaded resource.</span></span> <span data-ttu-id="ecc71-710">Si l’URL d’origine contenait des données supplémentaires, telles que des chaînes ou des ancres de recherche, ou si l’appel a été redirigé, l’URL retournée est différente de l’original.</span><span class="sxs-lookup"><span data-stu-id="ecc71-710">If the original URL contained any extra data, such as search strings or anchors, or if the call was redirected, the URL returned differs from the original.</span></span> <span data-ttu-id="ecc71-711">Cette option est valide sur les handles [**HINTERNET**](appendix-a-hinternet-handles.md) retournés par [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea)ou [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span><span class="sxs-lookup"><span data-stu-id="ecc71-711">This option is valid on [**HINTERNET**](appendix-a-hinternet-handles.md) handles returned by [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla), [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea), [**GopherOpenFile**](/windows/desktop/api/Wininet/nf-wininet-gopheropenfilea), or [**HttpOpenRequest**](/windows/desktop/api/Wininet/nf-wininet-httpopenrequesta).</span></span> <span data-ttu-id="ecc71-712">Elle est utilisée par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="ecc71-712">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-713"><span id="INTERNET_OPTION_USER_AGENT"></span><span id="internet_option_user_agent"></span>**\_option Internet \_ \_ agent utilisateur**</span><span class="sxs-lookup"><span data-stu-id="ecc71-713"><span id="INTERNET_OPTION_USER_AGENT"></span><span id="internet_option_user_agent"></span>**INTERNET\_OPTION\_USER\_AGENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-714">41</span><span class="sxs-lookup"><span data-stu-id="ecc71-714">41</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-715">Définit ou récupère la chaîne de l’agent utilisateur sur les handles fournis par [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) et utilisés dans les fonctions [**HTTPSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) suivantes, à condition qu’elles ne soient pas remplacées par un en-tête ajouté par [**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) ou [**HTTPSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span><span class="sxs-lookup"><span data-stu-id="ecc71-715">Sets or retrieves the user agent string on handles supplied by [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena) and used in subsequent [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta) functions, as long as it is not overridden by a header added by [**HttpAddRequestHeaders**](/windows/desktop/api/Wininet/nf-wininet-httpaddrequestheadersa) or [**HttpSendRequest**](/windows/desktop/api/Wininet/nf-wininet-httpsendrequesta).</span></span> <span data-ttu-id="ecc71-716">Utilisé par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) et [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="ecc71-716">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-717"><span id="INTERNET_OPTION_USERNAME"></span><span id="internet_option_username"></span>**\_ \_ nom d’utilisateur de l’option Internet**</span><span class="sxs-lookup"><span data-stu-id="ecc71-717"><span id="INTERNET_OPTION_USERNAME"></span><span id="internet_option_username"></span>**INTERNET\_OPTION\_USERNAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-718">28</span><span class="sxs-lookup"><span data-stu-id="ecc71-718">28</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-719">Définit ou récupère une chaîne qui contient le nom d’utilisateur associé à un handle retourné par [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span><span class="sxs-lookup"><span data-stu-id="ecc71-719">Sets or retrieves a string that contains the user name associated with a handle returned by [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta).</span></span> <span data-ttu-id="ecc71-720">Utilisé par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) et [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="ecc71-720">This is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-721"><span id="INTERNET_OPTION_VERSION"></span><span id="internet_option_version"></span>**VERSION de l' \_ option Internet \_**</span><span class="sxs-lookup"><span data-stu-id="ecc71-721"><span id="INTERNET_OPTION_VERSION"></span><span id="internet_option_version"></span>**INTERNET\_OPTION\_VERSION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-722">40</span><span class="sxs-lookup"><span data-stu-id="ecc71-722">40</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-723">Récupère une structure **d' \_ \_ informations de version Internet** qui contient le numéro de version de Wininet.dll.</span><span class="sxs-lookup"><span data-stu-id="ecc71-723">Retrieves an **INTERNET\_VERSION\_INFO** structure that contains the version number of Wininet.dll.</span></span> <span data-ttu-id="ecc71-724">Cette option peut être utilisée sur un handle [**HINTERNET**](appendix-a-hinternet-handles.md) **null** par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span><span class="sxs-lookup"><span data-stu-id="ecc71-724">This option can be used on a **NULL**[**HINTERNET**](appendix-a-hinternet-handles.md) handle by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ecc71-725"><span id="INTERNET_OPTION_WRITE_BUFFER_SIZE"></span><span id="internet_option_write_buffer_size"></span>**\_taille de \_ la \_ mémoire tampon d’écriture des options Internet \_**</span><span class="sxs-lookup"><span data-stu-id="ecc71-725"><span id="INTERNET_OPTION_WRITE_BUFFER_SIZE"></span><span id="internet_option_write_buffer_size"></span>**INTERNET\_OPTION\_WRITE\_BUFFER\_SIZE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ecc71-726">13</span><span class="sxs-lookup"><span data-stu-id="ecc71-726">13</span></span>
</dt> <dt>



<span data-ttu-id="ecc71-727">Définit ou récupère une valeur d’entier long non signé qui contient la taille, en octets, de la mémoire tampon d’écriture.</span><span class="sxs-lookup"><span data-stu-id="ecc71-727">Sets or retrieves an unsigned long integer value that contains the size, in bytes, of the write buffer.</span></span> <span data-ttu-id="ecc71-728">Cette option peut être utilisée sur les handles [**HINTERNET**](appendix-a-hinternet-handles.md) retournés par [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) et [**internetconnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) (session FTP uniquement).</span><span class="sxs-lookup"><span data-stu-id="ecc71-728">This option can be used on [**HINTERNET**](appendix-a-hinternet-handles.md) handles returned by [**FtpOpenFile**](/windows/desktop/api/Wininet/nf-wininet-ftpopenfilea) and [**InternetConnect**](/windows/desktop/api/Wininet/nf-wininet-internetconnecta) (FTP session only).</span></span> <span data-ttu-id="ecc71-729">Elle est utilisée par [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) et [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span><span class="sxs-lookup"><span data-stu-id="ecc71-729">It is used by [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) and [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona).</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ecc71-730">Notes</span><span class="sxs-lookup"><span data-stu-id="ecc71-730">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ecc71-731">WinINet ne prend pas en charge les implémentations de serveur.</span><span class="sxs-lookup"><span data-stu-id="ecc71-731">WinINet does not support server implementations.</span></span> <span data-ttu-id="ecc71-732">En outre, il ne doit pas être utilisé à partir d’un service.</span><span class="sxs-lookup"><span data-stu-id="ecc71-732">In addition, it should not be used from a service.</span></span> <span data-ttu-id="ecc71-733">Pour les implémentations de serveur ou les services, utilisez les [services http Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="ecc71-733">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="ecc71-734">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ecc71-734">Requirements</span></span>



| <span data-ttu-id="ecc71-735">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ecc71-735">Requirement</span></span> | <span data-ttu-id="ecc71-736">Valeur</span><span class="sxs-lookup"><span data-stu-id="ecc71-736">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecc71-737">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ecc71-737">Minimum supported client</span></span><br/> | <span data-ttu-id="ecc71-738">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ecc71-738">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                                             |
| <span data-ttu-id="ecc71-739">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ecc71-739">Minimum supported server</span></span><br/> | <span data-ttu-id="ecc71-740">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ecc71-740">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                                   |
| <span data-ttu-id="ecc71-741">En-tête</span><span class="sxs-lookup"><span data-stu-id="ecc71-741">Header</span></span><br/>                   | <dl> <span data-ttu-id="ecc71-742"><dt>Wininet. h ; </dt> <dt>Winineti. h</dt></span><span class="sxs-lookup"><span data-stu-id="ecc71-742"><dt>Wininet.h; </dt> <dt>Winineti.h</dt></span></span> </dl> |



 

