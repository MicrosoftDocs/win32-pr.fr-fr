---
title: Messages d’erreur (Wininet. h)
description: Les fonctions WinINet renvoient des codes d’erreur le cas échéant. Les erreurs suivantes sont spécifiques aux fonctions WinINet.
ms.assetid: 338bf65f-ebe5-4434-8407-9ab2a4c8d381
topic_type:
- apiref
api_name:
- ERROR_FTP_DROPPED
- ERROR_FTP_NO_PASSIVE_MODE
- ERROR_FTP_TRANSFER_IN_PROGRESS
- ERROR_GOPHER_ATTRIBUTE_NOT_FOUND
- ERROR_GOPHER_DATA_ERROR
- ERROR_GOPHER_END_OF_DATA
- ERROR_GOPHER_INCORRECT_LOCATOR_TYPE
- ERROR_GOPHER_INVALID_LOCATOR
- ERROR_GOPHER_NOT_FILE
- ERROR_GOPHER_NOT_GOPHER_PLUS
- ERROR_GOPHER_PROTOCOL_ERROR
- ERROR_GOPHER_UNKNOWN_LOCATOR
- ERROR_HTTP_COOKIE_DECLINED
- ERROR_HTTP_COOKIE_NEEDS_CONFIRMATION
- ERROR_HTTP_DOWNLEVEL_SERVER
- ERROR_HTTP_HEADER_ALREADY_EXISTS
- ERROR_HTTP_HEADER_NOT_FOUND
- ERROR_HTTP_INVALID_HEADER
- ERROR_HTTP_INVALID_QUERY_REQUEST
- ERROR_HTTP_INVALID_SERVER_RESPONSE
- ERROR_HTTP_NOT_REDIRECTED
- ERROR_HTTP_REDIRECT_FAILED
- ERROR_HTTP_REDIRECT_NEEDS_CONFIRMATION
- ERROR_INTERNET_ASYNC_THREAD_FAILED
- ERROR_INTERNET_BAD_AUTO_PROXY_SCRIPT
- ERROR_INTERNET_BAD_OPTION_LENGTH
- ERROR_INTERNET_BAD_REGISTRY_PARAMETER
- ERROR_INTERNET_CANNOT_CONNECT
- ERROR_INTERNET_CHG_POST_IS_NON_SECURE
- ERROR_INTERNET_CLIENT_AUTH_CERT_NEEDED
- ERROR_INTERNET_CLIENT_AUTH_NOT_SETUP
- ERROR_INTERNET_CONNECTION_ABORTED
- ERROR_INTERNET_CONNECTION_RESET
- ERROR_INTERNET_DECODING_FAILED
- ERROR_INTERNET_DIALOG_PENDING
- ERROR_INTERNET_DISCONNECTED
- ERROR_INTERNET_EXTENDED_ERROR
- ERROR_INTERNET_FAILED_DUETOSECURITYCHECK
- ERROR_INTERNET_FORCE_RETRY
- ERROR_INTERNET_FORTEZZA_LOGIN_NEEDED
- ERROR_INTERNET_HANDLE_EXISTS
- ERROR_INTERNET_HTTP_TO_HTTPS_ON_REDIR
- ERROR_INTERNET_HTTPS_HTTP_SUBMIT_REDIR
- ERROR_INTERNET_HTTPS_TO_HTTP_ON_REDIR
- ERROR_INTERNET_INCORRECT_FORMAT
- ERROR_INTERNET_INCORRECT_HANDLE_STATE
- ERROR_INTERNET_INCORRECT_HANDLE_TYPE
- ERROR_INTERNET_INCORRECT_PASSWORD
- ERROR_INTERNET_INCORRECT_USER_NAME
- ERROR_INTERNET_INSERT_CDROM
- ERROR_INTERNET_INTERNAL_ERROR
- ERROR_INTERNET_INVALID_CA
- ERROR_INTERNET_INVALID_OPERATION
- ERROR_INTERNET_INVALID_OPTION
- ERROR_INTERNET_INVALID_PROXY_REQUEST
- ERROR_INTERNET_INVALID_URL
- ERROR_INTERNET_ITEM_NOT_FOUND
- ERROR_INTERNET_LOGIN_FAILURE
- ERROR_INTERNET_LOGIN_FAILURE_DISPLAY_ENTITY_BODY
- ERROR_INTERNET_MIXED_SECURITY
- ERROR_INTERNET_NAME_NOT_RESOLVED
- ERROR_INTERNET_NEED_MSN_SSPI_PKG
- ERROR_INTERNET_NEED_UI
- ERROR_INTERNET_NO_CALLBACK
- ERROR_INTERNET_NO_CONTEXT
- ERROR_INTERNET_NO_DIRECT_ACCESS
- ERROR_INTERNET_NOT_INITIALIZED
- ERROR_INTERNET_NOT_PROXY_REQUEST
- ERROR_INTERNET_OPERATION_CANCELLED
- ERROR_INTERNET_OPTION_NOT_SETTABLE
- ERROR_INTERNET_OUT_OF_HANDLES
- ERROR_INTERNET_POST_IS_NON_SECURE
- ERROR_INTERNET_PROTOCOL_NOT_FOUND
- ERROR_INTERNET_PROXY_SERVER_UNREACHABLE
- ERROR_INTERNET_REDIRECT_SCHEME_CHANGE
- ERROR_INTERNET_REGISTRY_VALUE_NOT_FOUND
- ERROR_INTERNET_REQUEST_PENDING
- ERROR_INTERNET_RETRY_DIALOG
- ERROR_INTERNET_SEC_CERT_CN_INVALID
- ERROR_INTERNET_SEC_CERT_DATE_INVALID
- ERROR_INTERNET_SEC_CERT_ERRORS
- ERROR_INTERNET_SEC_CERT_NO_REV
- ERROR_INTERNET_SEC_CERT_REV_FAILED
- ERROR_INTERNET_SEC_CERT_REVOKED
- ERROR_INTERNET_SEC_INVALID_CERT
- ERROR_INTERNET_SECURITY_CHANNEL_ERROR
- ERROR_INTERNET_SERVER_UNREACHABLE
- ERROR_INTERNET_SHUTDOWN
- ERROR_INTERNET_TCPIP_NOT_INSTALLED
- ERROR_INTERNET_TIMEOUT
- ERROR_INTERNET_UNABLE_TO_CACHE_FILE
- ERROR_INTERNET_UNABLE_TO_DOWNLOAD_SCRIPT
- ERROR_INTERNET_UNRECOGNIZED_SCHEME
- ERROR_INVALID_HANDLE
- ERROR_MORE_DATA
- ERROR_NO_MORE_FILES
- ERROR_NO_MORE_ITEMS
api_location:
- Wininet.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d43fcaba7f0404ad002d2a94ac8291c95b0f7440
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106459"
---
# <a name="error-messages-winineth"></a><span data-ttu-id="592b4-104">Messages d’erreur (Wininet. h)</span><span class="sxs-lookup"><span data-stu-id="592b4-104">Error Messages (Wininet.h)</span></span>

<span data-ttu-id="592b4-105">Les fonctions WinINet renvoient des codes d’erreur le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="592b4-105">The WinINet functions return error codes where appropriate.</span></span> <span data-ttu-id="592b4-106">Les erreurs suivantes sont spécifiques aux fonctions WinINet.</span><span class="sxs-lookup"><span data-stu-id="592b4-106">The following errors are specific to the WinINet functions.</span></span>

<dl> <dt>

<span data-ttu-id="592b4-107"><span id="ERROR_FTP_DROPPED"></span><span id="error_ftp_dropped"></span>**ERREUR \_ FTP \_ supprimée**</span><span class="sxs-lookup"><span data-stu-id="592b4-107"><span id="ERROR_FTP_DROPPED"></span><span id="error_ftp_dropped"></span>**ERROR\_FTP\_DROPPED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-108">12111</span><span class="sxs-lookup"><span data-stu-id="592b4-108">12111</span></span>
</dt> <dt>



<span data-ttu-id="592b4-109">L’opération FTP n’a pas été effectuée car la session a été abandonnée.</span><span class="sxs-lookup"><span data-stu-id="592b4-109">The FTP operation was not completed because the session was aborted.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-110"><span id="ERROR_FTP_NO_PASSIVE_MODE"></span><span id="error_ftp_no_passive_mode"></span>**ERREUR \_ FTP \_ aucun \_ \_ mode passif**</span><span class="sxs-lookup"><span data-stu-id="592b4-110"><span id="ERROR_FTP_NO_PASSIVE_MODE"></span><span id="error_ftp_no_passive_mode"></span>**ERROR\_FTP\_NO\_PASSIVE\_MODE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-111">12112</span><span class="sxs-lookup"><span data-stu-id="592b4-111">12112</span></span>
</dt> <dt>



<span data-ttu-id="592b4-112">Le mode passif n’est pas disponible sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="592b4-112">Passive mode is not available on the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-113"><span id="ERROR_FTP_TRANSFER_IN_PROGRESS"></span><span id="error_ftp_transfer_in_progress"></span>**ERREUR \_ \_ de transfert FTP \_ en \_ cours**</span><span class="sxs-lookup"><span data-stu-id="592b4-113"><span id="ERROR_FTP_TRANSFER_IN_PROGRESS"></span><span id="error_ftp_transfer_in_progress"></span>**ERROR\_FTP\_TRANSFER\_IN\_PROGRESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-114">12110</span><span class="sxs-lookup"><span data-stu-id="592b4-114">12110</span></span>
</dt> <dt>



<span data-ttu-id="592b4-115">L’opération demandée ne peut pas être effectuée sur le descripteur de session FTP, car une opération est déjà en cours.</span><span class="sxs-lookup"><span data-stu-id="592b4-115">The requested operation cannot be made on the FTP session handle because an operation is already in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-116"><span id="ERROR_GOPHER_ATTRIBUTE_NOT_FOUND"></span><span id="error_gopher_attribute_not_found"></span>**ERREUR \_ Gopher \_ \_ non \_ trouvée**</span><span class="sxs-lookup"><span data-stu-id="592b4-116"><span id="ERROR_GOPHER_ATTRIBUTE_NOT_FOUND"></span><span id="error_gopher_attribute_not_found"></span>**ERROR\_GOPHER\_ATTRIBUTE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-117">12137</span><span class="sxs-lookup"><span data-stu-id="592b4-117">12137</span></span>
</dt> <dt>



<span data-ttu-id="592b4-118">L’attribut demandé est introuvable.</span><span class="sxs-lookup"><span data-stu-id="592b4-118">The requested attribute could not be located.</span></span>

> [!Note]  
> <span data-ttu-id="592b4-119">Windows XP et Windows Server 2003 R2 et versions antérieures uniquement.</span><span class="sxs-lookup"><span data-stu-id="592b4-119">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-120"><span id="ERROR_GOPHER_DATA_ERROR"></span><span id="error_gopher_data_error"></span>**erreur \_ de \_ données \_ Gopher**</span><span class="sxs-lookup"><span data-stu-id="592b4-120"><span id="ERROR_GOPHER_DATA_ERROR"></span><span id="error_gopher_data_error"></span>**ERROR\_GOPHER\_DATA\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-121">12132</span><span class="sxs-lookup"><span data-stu-id="592b4-121">12132</span></span>
</dt> <dt>



<span data-ttu-id="592b4-122">Une erreur a été détectée lors de la réception des données du serveur Gopher.</span><span class="sxs-lookup"><span data-stu-id="592b4-122">An error was detected while receiving data from the Gopher server.</span></span>

> [!Note]  
> <span data-ttu-id="592b4-123">Windows XP et Windows Server 2003 R2 et versions antérieures uniquement.</span><span class="sxs-lookup"><span data-stu-id="592b4-123">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-124"><span id="ERROR_GOPHER_END_OF_DATA"></span><span id="error_gopher_end_of_data"></span>**ERREUR \_ Gopher \_ de la fin \_ des \_ données**</span><span class="sxs-lookup"><span data-stu-id="592b4-124"><span id="ERROR_GOPHER_END_OF_DATA"></span><span id="error_gopher_end_of_data"></span>**ERROR\_GOPHER\_END\_OF\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-125">12133</span><span class="sxs-lookup"><span data-stu-id="592b4-125">12133</span></span>
</dt> <dt>



<span data-ttu-id="592b4-126">La fin des données a été atteinte.</span><span class="sxs-lookup"><span data-stu-id="592b4-126">The end of the data has been reached.</span></span>

> [!Note]  
> <span data-ttu-id="592b4-127">Windows XP et Windows Server 2003 R2 et versions antérieures uniquement.</span><span class="sxs-lookup"><span data-stu-id="592b4-127">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-128"><span id="ERROR_GOPHER_INCORRECT_LOCATOR_TYPE"></span><span id="error_gopher_incorrect_locator_type"></span>**ERREUR \_ Gopher \_ \_ type de localisateur incorrect \_**</span><span class="sxs-lookup"><span data-stu-id="592b4-128"><span id="ERROR_GOPHER_INCORRECT_LOCATOR_TYPE"></span><span id="error_gopher_incorrect_locator_type"></span>**ERROR\_GOPHER\_INCORRECT\_LOCATOR\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-129">12135</span><span class="sxs-lookup"><span data-stu-id="592b4-129">12135</span></span>
</dt> <dt>



<span data-ttu-id="592b4-130">Le type du localisateur n’est pas correct pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="592b4-130">The type of the locator is not correct for this operation.</span></span>

> [!Note]  
> <span data-ttu-id="592b4-131">Windows XP et Windows Server 2003 R2 et versions antérieures uniquement.</span><span class="sxs-lookup"><span data-stu-id="592b4-131">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-132"><span id="ERROR_GOPHER_INVALID_LOCATOR"></span><span id="error_gopher_invalid_locator"></span>**ERREUR \_ Gopher \_ - \_ localisateur non valide**</span><span class="sxs-lookup"><span data-stu-id="592b4-132"><span id="ERROR_GOPHER_INVALID_LOCATOR"></span><span id="error_gopher_invalid_locator"></span>**ERROR\_GOPHER\_INVALID\_LOCATOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-133">12134</span><span class="sxs-lookup"><span data-stu-id="592b4-133">12134</span></span>
</dt> <dt>



<span data-ttu-id="592b4-134">Le localisateur fourni n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="592b4-134">The supplied locator is not valid.</span></span>

> [!Note]  
> <span data-ttu-id="592b4-135">Windows XP et Windows Server 2003 R2 et versions antérieures uniquement.</span><span class="sxs-lookup"><span data-stu-id="592b4-135">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-136"><span id="ERROR_GOPHER_NOT_FILE"></span><span id="error_gopher_not_file"></span>**ERREUR \_ Gopher \_ not \_ file**</span><span class="sxs-lookup"><span data-stu-id="592b4-136"><span id="ERROR_GOPHER_NOT_FILE"></span><span id="error_gopher_not_file"></span>**ERROR\_GOPHER\_NOT\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-137">12131</span><span class="sxs-lookup"><span data-stu-id="592b4-137">12131</span></span>
</dt> <dt>



<span data-ttu-id="592b4-138">La demande doit être effectuée pour un localisateur de fichier.</span><span class="sxs-lookup"><span data-stu-id="592b4-138">The request must be made for a file locator.</span></span>

> [!Note]  
> <span data-ttu-id="592b4-139">Windows XP et Windows Server 2003 R2 et versions antérieures uniquement.</span><span class="sxs-lookup"><span data-stu-id="592b4-139">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-140"><span id="ERROR_GOPHER_NOT_GOPHER_PLUS"></span><span id="error_gopher_not_gopher_plus"></span>**ERREUR \_ Gopher \_ non \_ Gopher \_ plus**</span><span class="sxs-lookup"><span data-stu-id="592b4-140"><span id="ERROR_GOPHER_NOT_GOPHER_PLUS"></span><span id="error_gopher_not_gopher_plus"></span>**ERROR\_GOPHER\_NOT\_GOPHER\_PLUS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-141">12136</span><span class="sxs-lookup"><span data-stu-id="592b4-141">12136</span></span>
</dt> <dt>



<span data-ttu-id="592b4-142">L’opération demandée ne peut être effectuée que sur un serveur Gopher +, ou avec un localisateur qui spécifie une opération Gopher +.</span><span class="sxs-lookup"><span data-stu-id="592b4-142">The requested operation can be made only against a Gopher+ server, or with a locator that specifies a Gopher+ operation.</span></span>

> [!Note]  
> <span data-ttu-id="592b4-143">Windows XP et Windows Server 2003 R2 et versions antérieures uniquement.</span><span class="sxs-lookup"><span data-stu-id="592b4-143">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-144"><span id="ERROR_GOPHER_PROTOCOL_ERROR"></span><span id="error_gopher_protocol_error"></span>**erreur \_ de \_ protocole \_ Gopher**</span><span class="sxs-lookup"><span data-stu-id="592b4-144"><span id="ERROR_GOPHER_PROTOCOL_ERROR"></span><span id="error_gopher_protocol_error"></span>**ERROR\_GOPHER\_PROTOCOL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-145">12130</span><span class="sxs-lookup"><span data-stu-id="592b4-145">12130</span></span>
</dt> <dt>



<span data-ttu-id="592b4-146">Une erreur a été détectée lors de l’analyse des données retournées par le serveur Gopher.</span><span class="sxs-lookup"><span data-stu-id="592b4-146">An error was detected while parsing data returned from the Gopher server.</span></span>

> [!Note]  
> <span data-ttu-id="592b4-147">Windows XP et Windows Server 2003 R2 et versions antérieures uniquement.</span><span class="sxs-lookup"><span data-stu-id="592b4-147">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-148"><span id="ERROR_GOPHER_UNKNOWN_LOCATOR"></span><span id="error_gopher_unknown_locator"></span>**ERREUR \_ Gopher \_ - \_ localisateur inconnu**</span><span class="sxs-lookup"><span data-stu-id="592b4-148"><span id="ERROR_GOPHER_UNKNOWN_LOCATOR"></span><span id="error_gopher_unknown_locator"></span>**ERROR\_GOPHER\_UNKNOWN\_LOCATOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-149">12138</span><span class="sxs-lookup"><span data-stu-id="592b4-149">12138</span></span>
</dt> <dt>



<span data-ttu-id="592b4-150">Le type de localisateur est inconnu.</span><span class="sxs-lookup"><span data-stu-id="592b4-150">The locator type is unknown.</span></span>

> [!Note]  
> <span data-ttu-id="592b4-151">Windows XP et Windows Server 2003 R2 et versions antérieures uniquement.</span><span class="sxs-lookup"><span data-stu-id="592b4-151">Windows XP and Windows Server 2003 R2 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-152"><span id="ERROR_HTTP_COOKIE_DECLINED"></span><span id="error_http_cookie_declined"></span>**ERREUR \_ \_ cookie HTTP \_ refusé**</span><span class="sxs-lookup"><span data-stu-id="592b4-152"><span id="ERROR_HTTP_COOKIE_DECLINED"></span><span id="error_http_cookie_declined"></span>**ERROR\_HTTP\_COOKIE\_DECLINED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-153">12162</span><span class="sxs-lookup"><span data-stu-id="592b4-153">12162</span></span>
</dt> <dt>



<span data-ttu-id="592b4-154">Le cookie HTTP a été refusé par le serveur.</span><span class="sxs-lookup"><span data-stu-id="592b4-154">The HTTP cookie was declined by the server.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-155"><span id="ERROR_HTTP_COOKIE_NEEDS_CONFIRMATION"></span><span id="error_http_cookie_needs_confirmation"></span>**ERREUR \_ de \_ confirmation du cookie HTTP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="592b4-155"><span id="ERROR_HTTP_COOKIE_NEEDS_CONFIRMATION"></span><span id="error_http_cookie_needs_confirmation"></span>**ERROR\_HTTP\_COOKIE\_NEEDS\_CONFIRMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-156">12161</span><span class="sxs-lookup"><span data-stu-id="592b4-156">12161</span></span>
</dt> <dt>



<span data-ttu-id="592b4-157">Le cookie HTTP nécessite une confirmation.</span><span class="sxs-lookup"><span data-stu-id="592b4-157">The HTTP cookie requires confirmation.</span></span>

> [!Note]  
> <span data-ttu-id="592b4-158">Windows Vista et Windows Server 2008 et versions antérieures uniquement.</span><span class="sxs-lookup"><span data-stu-id="592b4-158">Windows Vista and Windows Server 2008 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-159"><span id="ERROR_HTTP_DOWNLEVEL_SERVER"></span><span id="error_http_downlevel_server"></span>**ERREUR \_ \_ serveur de niveau inférieur http \_**</span><span class="sxs-lookup"><span data-stu-id="592b4-159"><span id="ERROR_HTTP_DOWNLEVEL_SERVER"></span><span id="error_http_downlevel_server"></span>**ERROR\_HTTP\_DOWNLEVEL\_SERVER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-160">12151</span><span class="sxs-lookup"><span data-stu-id="592b4-160">12151</span></span>
</dt> <dt>



<span data-ttu-id="592b4-161">Le serveur n’a retourné aucun en-tête.</span><span class="sxs-lookup"><span data-stu-id="592b4-161">The server did not return any headers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-162"><span id="ERROR_HTTP_HEADER_ALREADY_EXISTS"></span><span id="error_http_header_already_exists"></span>**l' \_ \_ en-tête http d’erreur \_ \_ existe déjà**</span><span class="sxs-lookup"><span data-stu-id="592b4-162"><span id="ERROR_HTTP_HEADER_ALREADY_EXISTS"></span><span id="error_http_header_already_exists"></span>**ERROR\_HTTP\_HEADER\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-163">12155</span><span class="sxs-lookup"><span data-stu-id="592b4-163">12155</span></span>
</dt> <dt>



<span data-ttu-id="592b4-164">Impossible d’ajouter l’en-tête, car il existe déjà.</span><span class="sxs-lookup"><span data-stu-id="592b4-164">The header could not be added because it already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-165"><span id="ERROR_HTTP_HEADER_NOT_FOUND"></span><span id="error_http_header_not_found"></span>**l' \_ en-tête http de l’erreur est \_ \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="592b4-165"><span id="ERROR_HTTP_HEADER_NOT_FOUND"></span><span id="error_http_header_not_found"></span>**ERROR\_HTTP\_HEADER\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-166">12150</span><span class="sxs-lookup"><span data-stu-id="592b4-166">12150</span></span>
</dt> <dt>



<span data-ttu-id="592b4-167">L’en-tête demandé est introuvable.</span><span class="sxs-lookup"><span data-stu-id="592b4-167">The requested header could not be located.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-168"><span id="ERROR_HTTP_INVALID_HEADER"></span><span id="error_http_invalid_header"></span>**ERREUR \_ http \_ \_ -en-tête non valide**</span><span class="sxs-lookup"><span data-stu-id="592b4-168"><span id="ERROR_HTTP_INVALID_HEADER"></span><span id="error_http_invalid_header"></span>**ERROR\_HTTP\_INVALID\_HEADER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-169">12153</span><span class="sxs-lookup"><span data-stu-id="592b4-169">12153</span></span>
</dt> <dt>



<span data-ttu-id="592b4-170">L’en-tête fourni n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="592b4-170">The supplied header is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-171"><span id="ERROR_HTTP_INVALID_QUERY_REQUEST"></span><span id="error_http_invalid_query_request"></span>**ERREUR \_ de \_ \_ requête de requête non valide http \_**</span><span class="sxs-lookup"><span data-stu-id="592b4-171"><span id="ERROR_HTTP_INVALID_QUERY_REQUEST"></span><span id="error_http_invalid_query_request"></span>**ERROR\_HTTP\_INVALID\_QUERY\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-172">12154</span><span class="sxs-lookup"><span data-stu-id="592b4-172">12154</span></span>
</dt> <dt>



<span data-ttu-id="592b4-173">La demande adressée à [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="592b4-173">The request made to [**HttpQueryInfo**](/windows/desktop/api/Wininet/nf-wininet-httpqueryinfoa) is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-174"><span id="ERROR_HTTP_INVALID_SERVER_RESPONSE"></span><span id="error_http_invalid_server_response"></span>**ERREUR \_ de \_ \_ réponse du serveur http non valide \_**</span><span class="sxs-lookup"><span data-stu-id="592b4-174"><span id="ERROR_HTTP_INVALID_SERVER_RESPONSE"></span><span id="error_http_invalid_server_response"></span>**ERROR\_HTTP\_INVALID\_SERVER\_RESPONSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-175">12152</span><span class="sxs-lookup"><span data-stu-id="592b4-175">12152</span></span>
</dt> <dt>



<span data-ttu-id="592b4-176">La réponse du serveur n’a pas pu être analysée.</span><span class="sxs-lookup"><span data-stu-id="592b4-176">The server response could not be parsed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-177"><span id="ERROR_HTTP_NOT_REDIRECTED"></span><span id="error_http_not_redirected"></span>**ERREUR \_ http \_ non \_ redirigée**</span><span class="sxs-lookup"><span data-stu-id="592b4-177"><span id="ERROR_HTTP_NOT_REDIRECTED"></span><span id="error_http_not_redirected"></span>**ERROR\_HTTP\_NOT\_REDIRECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-178">12160</span><span class="sxs-lookup"><span data-stu-id="592b4-178">12160</span></span>
</dt> <dt>



<span data-ttu-id="592b4-179">La requête HTTP n’a pas été redirigée.</span><span class="sxs-lookup"><span data-stu-id="592b4-179">The HTTP request was not redirected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-180"><span id="ERROR_HTTP_REDIRECT_FAILED"></span><span id="error_http_redirect_failed"></span>**ERREUR \_ de \_ redirection \_ http**</span><span class="sxs-lookup"><span data-stu-id="592b4-180"><span id="ERROR_HTTP_REDIRECT_FAILED"></span><span id="error_http_redirect_failed"></span>**ERROR\_HTTP\_REDIRECT\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-181">12156</span><span class="sxs-lookup"><span data-stu-id="592b4-181">12156</span></span>
</dt> <dt>



<span data-ttu-id="592b4-182">La redirection a échoué, car le schéma a changé (par exemple, HTTP en FTP) ou toutes les tentatives effectuées pour la redirection ont échoué (cinq tentatives par défaut).</span><span class="sxs-lookup"><span data-stu-id="592b4-182">The redirection failed because either the scheme changed (for example, HTTP to FTP) or all attempts made to redirect failed (default is five attempts).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-183"><span id="ERROR_HTTP_REDIRECT_NEEDS_CONFIRMATION"></span><span id="error_http_redirect_needs_confirmation"></span>**l’erreur de \_ \_ redirection http \_ nécessite une \_ confirmation**</span><span class="sxs-lookup"><span data-stu-id="592b4-183"><span id="ERROR_HTTP_REDIRECT_NEEDS_CONFIRMATION"></span><span id="error_http_redirect_needs_confirmation"></span>**ERROR\_HTTP\_REDIRECT\_NEEDS\_CONFIRMATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-184">12168</span><span class="sxs-lookup"><span data-stu-id="592b4-184">12168</span></span>
</dt> <dt>



<span data-ttu-id="592b4-185">La redirection requiert la confirmation de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="592b4-185">The redirection requires user confirmation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-186"><span id="ERROR_INTERNET_ASYNC_THREAD_FAILED"></span><span id="error_internet_async_thread_failed"></span>**ERREUR \_ \_ échec du \_ thread \_ asynchrone Internet**</span><span class="sxs-lookup"><span data-stu-id="592b4-186"><span id="ERROR_INTERNET_ASYNC_THREAD_FAILED"></span><span id="error_internet_async_thread_failed"></span>**ERROR\_INTERNET\_ASYNC\_THREAD\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-187">12047</span><span class="sxs-lookup"><span data-stu-id="592b4-187">12047</span></span>
</dt> <dt>



<span data-ttu-id="592b4-188">L’application n’a pas pu démarrer un thread asynchrone.</span><span class="sxs-lookup"><span data-stu-id="592b4-188">The application could not start an asynchronous thread.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-189"><span id="ERROR_INTERNET_BAD_AUTO_PROXY_SCRIPT"></span><span id="error_internet_bad_auto_proxy_script"></span>**ERREUR \_ Internet \_ mauvais \_ \_ script de proxy automatique \_**</span><span class="sxs-lookup"><span data-stu-id="592b4-189"><span id="ERROR_INTERNET_BAD_AUTO_PROXY_SCRIPT"></span><span id="error_internet_bad_auto_proxy_script"></span>**ERROR\_INTERNET\_BAD\_AUTO\_PROXY\_SCRIPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-190">12166</span><span class="sxs-lookup"><span data-stu-id="592b4-190">12166</span></span>
</dt> <dt>



<span data-ttu-id="592b4-191">Une erreur s’est produite dans le script de configuration automatique du proxy.</span><span class="sxs-lookup"><span data-stu-id="592b4-191">There was an error in the automatic proxy configuration script.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-192"><span id="ERROR_INTERNET_BAD_OPTION_LENGTH"></span><span id="error_internet_bad_option_length"></span>**ERREUR \_ Internet-longueur de l' \_ option incorrecte \_ \_**</span><span class="sxs-lookup"><span data-stu-id="592b4-192"><span id="ERROR_INTERNET_BAD_OPTION_LENGTH"></span><span id="error_internet_bad_option_length"></span>**ERROR\_INTERNET\_BAD\_OPTION\_LENGTH**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-193">12010</span><span class="sxs-lookup"><span data-stu-id="592b4-193">12010</span></span>
</dt> <dt>



<span data-ttu-id="592b4-194">La longueur d’une option fournie à [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) ou [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) est incorrecte pour le type d’option spécifié.</span><span class="sxs-lookup"><span data-stu-id="592b4-194">The length of an option supplied to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) or [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) is incorrect for the type of option specified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-195"><span id="ERROR_INTERNET_BAD_REGISTRY_PARAMETER"></span><span id="error_internet_bad_registry_parameter"></span>**ERREUR \_ de \_ \_ paramètre de registre Internet incorrect \_**</span><span class="sxs-lookup"><span data-stu-id="592b4-195"><span id="ERROR_INTERNET_BAD_REGISTRY_PARAMETER"></span><span id="error_internet_bad_registry_parameter"></span>**ERROR\_INTERNET\_BAD\_REGISTRY\_PARAMETER**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-196">12022</span><span class="sxs-lookup"><span data-stu-id="592b4-196">12022</span></span>
</dt> <dt>



<span data-ttu-id="592b4-197">Une valeur de registre requise a été trouvée, mais son type est incorrect ou sa valeur n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="592b4-197">A required registry value was located but is an incorrect type or has an invalid value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-198"><span id="ERROR_INTERNET_CANNOT_CONNECT"></span><span id="error_internet_cannot_connect"></span>**ERREUR \_ Internet \_ ne peut pas \_ se connecter**</span><span class="sxs-lookup"><span data-stu-id="592b4-198"><span id="ERROR_INTERNET_CANNOT_CONNECT"></span><span id="error_internet_cannot_connect"></span>**ERROR\_INTERNET\_CANNOT\_CONNECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-199">12029</span><span class="sxs-lookup"><span data-stu-id="592b4-199">12029</span></span>
</dt> <dt>



<span data-ttu-id="592b4-200">La tentative de connexion au serveur a échoué.</span><span class="sxs-lookup"><span data-stu-id="592b4-200">The attempt to connect to the server failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-201"><span id="ERROR_INTERNET_CHG_POST_IS_NON_SECURE"></span><span id="error_internet_chg_post_is_non_secure"></span>**ERREUR \_ la \_ publication d’Internet CHG \_ \_ n’est \_ pas \_ sécurisée**</span><span class="sxs-lookup"><span data-stu-id="592b4-201"><span id="ERROR_INTERNET_CHG_POST_IS_NON_SECURE"></span><span id="error_internet_chg_post_is_non_secure"></span>**ERROR\_INTERNET\_CHG\_POST\_IS\_NON\_SECURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-202">12042</span><span class="sxs-lookup"><span data-stu-id="592b4-202">12042</span></span>
</dt> <dt>



<span data-ttu-id="592b4-203">L’application publie et tente de modifier plusieurs lignes de texte sur un serveur qui n’est pas sécurisé.</span><span class="sxs-lookup"><span data-stu-id="592b4-203">The application is posting and attempting to change multiple lines of text on a server that is not secure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-204"><span id="ERROR_INTERNET_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_internet_client_auth_cert_needed"></span>**ERREUR \_ de \_ certificat d’authentification du client Internet \_ \_ \_ requis**</span><span class="sxs-lookup"><span data-stu-id="592b4-204"><span id="ERROR_INTERNET_CLIENT_AUTH_CERT_NEEDED"></span><span id="error_internet_client_auth_cert_needed"></span>**ERROR\_INTERNET\_CLIENT\_AUTH\_CERT\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-205">12044</span><span class="sxs-lookup"><span data-stu-id="592b4-205">12044</span></span>
</dt> <dt>



<span data-ttu-id="592b4-206">Le serveur demande l’authentification du client.</span><span class="sxs-lookup"><span data-stu-id="592b4-206">The server is requesting client authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-207"><span id="ERROR_INTERNET_CLIENT_AUTH_NOT_SETUP"></span><span id="error_internet_client_auth_not_setup"></span>**ERREUR \_ \_ d’authentification du client Internet \_ \_ non \_ configurée**</span><span class="sxs-lookup"><span data-stu-id="592b4-207"><span id="ERROR_INTERNET_CLIENT_AUTH_NOT_SETUP"></span><span id="error_internet_client_auth_not_setup"></span>**ERROR\_INTERNET\_CLIENT\_AUTH\_NOT\_SETUP**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-208">12046</span><span class="sxs-lookup"><span data-stu-id="592b4-208">12046</span></span>
</dt> <dt>



<span data-ttu-id="592b4-209">L’autorisation du client n’est pas configurée sur cet ordinateur.</span><span class="sxs-lookup"><span data-stu-id="592b4-209">Client authorization is not set up on this computer.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-210"><span id="ERROR_INTERNET_CONNECTION_ABORTED"></span><span id="error_internet_connection_aborted"></span>**ERREUR \_ de \_ connexion Internet \_ abandonnée**</span><span class="sxs-lookup"><span data-stu-id="592b4-210"><span id="ERROR_INTERNET_CONNECTION_ABORTED"></span><span id="error_internet_connection_aborted"></span>**ERROR\_INTERNET\_CONNECTION\_ABORTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-211">12030</span><span class="sxs-lookup"><span data-stu-id="592b4-211">12030</span></span>
</dt> <dt>



<span data-ttu-id="592b4-212">La connexion avec le serveur a été arrêtée.</span><span class="sxs-lookup"><span data-stu-id="592b4-212">The connection with the server has been terminated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-213"><span id="ERROR_INTERNET_CONNECTION_RESET"></span><span id="error_internet_connection_reset"></span>**ERREUR \_ de \_ réinitialisation de la connexion Internet \_**</span><span class="sxs-lookup"><span data-stu-id="592b4-213"><span id="ERROR_INTERNET_CONNECTION_RESET"></span><span id="error_internet_connection_reset"></span>**ERROR\_INTERNET\_CONNECTION\_RESET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-214">12031</span><span class="sxs-lookup"><span data-stu-id="592b4-214">12031</span></span>
</dt> <dt>



<span data-ttu-id="592b4-215">La connexion avec le serveur a été réinitialisée.</span><span class="sxs-lookup"><span data-stu-id="592b4-215">The connection with the server has been reset.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-216"><span id="ERROR_INTERNET_DECODING_FAILED"></span><span id="error_internet_decoding_failed"></span>**ERREUR lors du \_ \_ décodage Internet \_**</span><span class="sxs-lookup"><span data-stu-id="592b4-216"><span id="ERROR_INTERNET_DECODING_FAILED"></span><span id="error_internet_decoding_failed"></span>**ERROR\_INTERNET\_DECODING\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-217">12175</span><span class="sxs-lookup"><span data-stu-id="592b4-217">12175</span></span>
</dt> <dt>



<span data-ttu-id="592b4-218">WinINet n’a pas pu effectuer le décodage du contenu sur la réponse.</span><span class="sxs-lookup"><span data-stu-id="592b4-218">WinINet failed to perform content decoding on the response.</span></span> <span data-ttu-id="592b4-219">Pour plus d’informations, consultez la rubrique relative à l' [**encodage du contenu**](content-encoding.md) .</span><span class="sxs-lookup"><span data-stu-id="592b4-219">For more information, see the [**Content Encoding**](content-encoding.md) topic.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-220"><span id="ERROR_INTERNET_DIALOG_PENDING"></span><span id="error_internet_dialog_pending"></span>**boîte de dialogue d’erreur \_ Internet \_ \_ en attente**</span><span class="sxs-lookup"><span data-stu-id="592b4-220"><span id="ERROR_INTERNET_DIALOG_PENDING"></span><span id="error_internet_dialog_pending"></span>**ERROR\_INTERNET\_DIALOG\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-221">12049</span><span class="sxs-lookup"><span data-stu-id="592b4-221">12049</span></span>
</dt> <dt>



<span data-ttu-id="592b4-222">Une boîte de dialogue de mot de passe est en cours pour un autre thread.</span><span class="sxs-lookup"><span data-stu-id="592b4-222">Another thread has a password dialog box in progress.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-223"><span id="ERROR_INTERNET_DISCONNECTED"></span><span id="error_internet_disconnected"></span>**ERREUR \_ Internet \_ déconnectée**</span><span class="sxs-lookup"><span data-stu-id="592b4-223"><span id="ERROR_INTERNET_DISCONNECTED"></span><span id="error_internet_disconnected"></span>**ERROR\_INTERNET\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-224">12163</span><span class="sxs-lookup"><span data-stu-id="592b4-224">12163</span></span>
</dt> <dt>



<span data-ttu-id="592b4-225">La connexion Internet a été perdue.</span><span class="sxs-lookup"><span data-stu-id="592b4-225">The Internet connection has been lost.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-226"><span id="ERROR_INTERNET_EXTENDED_ERROR"></span><span id="error_internet_extended_error"></span>**erreur \_ \_ étendue Internet \_**</span><span class="sxs-lookup"><span data-stu-id="592b4-226"><span id="ERROR_INTERNET_EXTENDED_ERROR"></span><span id="error_internet_extended_error"></span>**ERROR\_INTERNET\_EXTENDED\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-227">12003</span><span class="sxs-lookup"><span data-stu-id="592b4-227">12003</span></span>
</dt> <dt>



<span data-ttu-id="592b4-228">Une erreur étendue a été retournée par le serveur.</span><span class="sxs-lookup"><span data-stu-id="592b4-228">An extended error was returned from the server.</span></span> <span data-ttu-id="592b4-229">Il s’agit généralement d’une chaîne ou d’une mémoire tampon contenant un message d’erreur détaillé.</span><span class="sxs-lookup"><span data-stu-id="592b4-229">This is typically a string or buffer containing a verbose error message.</span></span> <span data-ttu-id="592b4-230">Appelez [**InternetGetLastResponseInfo**](/windows/desktop/api/Wininet/nf-wininet-internetgetlastresponseinfoa) pour récupérer le texte d’erreur.</span><span class="sxs-lookup"><span data-stu-id="592b4-230">Call [**InternetGetLastResponseInfo**](/windows/desktop/api/Wininet/nf-wininet-internetgetlastresponseinfoa) to retrieve the error text.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-231"><span id="ERROR_INTERNET_FAILED_DUETOSECURITYCHECK"></span><span id="error_internet_failed_duetosecuritycheck"></span>**ERREUR \_ Internet \_ failed \_ DUETOSECURITYCHECK**</span><span class="sxs-lookup"><span data-stu-id="592b4-231"><span id="ERROR_INTERNET_FAILED_DUETOSECURITYCHECK"></span><span id="error_internet_failed_duetosecuritycheck"></span>**ERROR\_INTERNET\_FAILED\_DUETOSECURITYCHECK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-232">12171</span><span class="sxs-lookup"><span data-stu-id="592b4-232">12171</span></span>
</dt> <dt>



<span data-ttu-id="592b4-233">La fonction a échoué en raison d’une vérification de sécurité.</span><span class="sxs-lookup"><span data-stu-id="592b4-233">The function failed due to a security check.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-234"><span id="ERROR_INTERNET_FORCE_RETRY"></span><span id="error_internet_force_retry"></span>**ERREUR \_ de \_ tentative Internet forcée \_**</span><span class="sxs-lookup"><span data-stu-id="592b4-234"><span id="ERROR_INTERNET_FORCE_RETRY"></span><span id="error_internet_force_retry"></span>**ERROR\_INTERNET\_FORCE\_RETRY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-235">12032</span><span class="sxs-lookup"><span data-stu-id="592b4-235">12032</span></span>
</dt> <dt>



<span data-ttu-id="592b4-236">La fonction doit rétablir la requête.</span><span class="sxs-lookup"><span data-stu-id="592b4-236">The function needs to redo the request.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-237"><span id="ERROR_INTERNET_FORTEZZA_LOGIN_NEEDED"></span><span id="error_internet_fortezza_login_needed"></span>**ERREUR \_ de \_ connexion Internet Fortezza \_ \_ nécessaire**</span><span class="sxs-lookup"><span data-stu-id="592b4-237"><span id="ERROR_INTERNET_FORTEZZA_LOGIN_NEEDED"></span><span id="error_internet_fortezza_login_needed"></span>**ERROR\_INTERNET\_FORTEZZA\_LOGIN\_NEEDED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-238">12054</span><span class="sxs-lookup"><span data-stu-id="592b4-238">12054</span></span>
</dt> <dt>



<span data-ttu-id="592b4-239">La ressource demandée requiert une authentification Fortezza.</span><span class="sxs-lookup"><span data-stu-id="592b4-239">The requested resource requires Fortezza authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-240"><span id="ERROR_INTERNET_HANDLE_EXISTS"></span><span id="error_internet_handle_exists"></span>**ERREUR \_ de \_ descripteur Internet \_**</span><span class="sxs-lookup"><span data-stu-id="592b4-240"><span id="ERROR_INTERNET_HANDLE_EXISTS"></span><span id="error_internet_handle_exists"></span>**ERROR\_INTERNET\_HANDLE\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-241">12036</span><span class="sxs-lookup"><span data-stu-id="592b4-241">12036</span></span>
</dt> <dt>



<span data-ttu-id="592b4-242">La requête a échoué, car le handle existe déjà.</span><span class="sxs-lookup"><span data-stu-id="592b4-242">The request failed because the handle already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-243"><span id="ERROR_INTERNET_HTTP_TO_HTTPS_ON_REDIR"></span><span id="error_internet_http_to_https_on_redir"></span>**ERREUR \_ Internet \_ http \_ à \_ https \_ sur le \_ ReDim**</span><span class="sxs-lookup"><span data-stu-id="592b4-243"><span id="ERROR_INTERNET_HTTP_TO_HTTPS_ON_REDIR"></span><span id="error_internet_http_to_https_on_redir"></span>**ERROR\_INTERNET\_HTTP\_TO\_HTTPS\_ON\_REDIR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-244">12039</span><span class="sxs-lookup"><span data-stu-id="592b4-244">12039</span></span>
</dt> <dt>



<span data-ttu-id="592b4-245">L’application est déplacée d’une connexion non-SSL vers une connexion SSL en raison d’une redirection.</span><span class="sxs-lookup"><span data-stu-id="592b4-245">The application is moving from a non-SSL to an SSL connection because of a redirect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-246"><span id="ERROR_INTERNET_HTTPS_HTTP_SUBMIT_REDIR"></span><span id="error_internet_https_http_submit_redir"></span>**ERREUR \_ d' \_ envoi de \_ l' \_ \_ instruction http https http à Internet**</span><span class="sxs-lookup"><span data-stu-id="592b4-246"><span id="ERROR_INTERNET_HTTPS_HTTP_SUBMIT_REDIR"></span><span id="error_internet_https_http_submit_redir"></span>**ERROR\_INTERNET\_HTTPS\_HTTP\_SUBMIT\_REDIR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-247">12052</span><span class="sxs-lookup"><span data-stu-id="592b4-247">12052</span></span>
</dt> <dt>



<span data-ttu-id="592b4-248">Les données soumises à une connexion SSL sont redirigées vers une connexion non-SSL.</span><span class="sxs-lookup"><span data-stu-id="592b4-248">The data being submitted to an SSL connection is being redirected to a non-SSL connection.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-249"><span id="ERROR_INTERNET_HTTPS_TO_HTTP_ON_REDIR"></span><span id="error_internet_https_to_http_on_redir"></span>**ERREUR \_ Internet \_ https \_ à \_ http \_ sur le \_ ReDim**</span><span class="sxs-lookup"><span data-stu-id="592b4-249"><span id="ERROR_INTERNET_HTTPS_TO_HTTP_ON_REDIR"></span><span id="error_internet_https_to_http_on_redir"></span>**ERROR\_INTERNET\_HTTPS\_TO\_HTTP\_ON\_REDIR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-250">12040</span><span class="sxs-lookup"><span data-stu-id="592b4-250">12040</span></span>
</dt> <dt>



<span data-ttu-id="592b4-251">L’application est déplacée d’une connexion SSL vers une connexion non-SSL en raison d’une redirection.</span><span class="sxs-lookup"><span data-stu-id="592b4-251">The application is moving from an SSL to an non-SSL connection because of a redirect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-252"><span id="ERROR_INTERNET_INCORRECT_FORMAT"></span><span id="error_internet_incorrect_format"></span>**ERREUR \_ de \_ format incorrect Internet \_**</span><span class="sxs-lookup"><span data-stu-id="592b4-252"><span id="ERROR_INTERNET_INCORRECT_FORMAT"></span><span id="error_internet_incorrect_format"></span>**ERROR\_INTERNET\_INCORRECT\_FORMAT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-253">12027</span><span class="sxs-lookup"><span data-stu-id="592b4-253">12027</span></span>
</dt> <dt>



<span data-ttu-id="592b4-254">Le format de la demande n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="592b4-254">The format of the request is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-255"><span id="ERROR_INTERNET_INCORRECT_HANDLE_STATE"></span><span id="error_internet_incorrect_handle_state"></span>**ERREUR \_ d' \_ \_ État de handle incorrect Internet \_**</span><span class="sxs-lookup"><span data-stu-id="592b4-255"><span id="ERROR_INTERNET_INCORRECT_HANDLE_STATE"></span><span id="error_internet_incorrect_handle_state"></span>**ERROR\_INTERNET\_INCORRECT\_HANDLE\_STATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-256">12019</span><span class="sxs-lookup"><span data-stu-id="592b4-256">12019</span></span>
</dt> <dt>



<span data-ttu-id="592b4-257">Impossible d’effectuer l’opération demandée, car le handle fourni n’est pas dans l’état correct.</span><span class="sxs-lookup"><span data-stu-id="592b4-257">The requested operation cannot be carried out because the handle supplied is not in the correct state.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-258"><span id="ERROR_INTERNET_INCORRECT_HANDLE_TYPE"></span><span id="error_internet_incorrect_handle_type"></span>**ERREUR \_ de \_ \_ type de descripteur incorrect Internet \_**</span><span class="sxs-lookup"><span data-stu-id="592b4-258"><span id="ERROR_INTERNET_INCORRECT_HANDLE_TYPE"></span><span id="error_internet_incorrect_handle_type"></span>**ERROR\_INTERNET\_INCORRECT\_HANDLE\_TYPE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-259">12018</span><span class="sxs-lookup"><span data-stu-id="592b4-259">12018</span></span>
</dt> <dt>



<span data-ttu-id="592b4-260">Le type de handle fourni est incorrect pour cette opération.</span><span class="sxs-lookup"><span data-stu-id="592b4-260">The type of handle supplied is incorrect for this operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-261"><span id="ERROR_INTERNET_INCORRECT_PASSWORD"></span><span id="error_internet_incorrect_password"></span>**ERREUR \_ \_ \_ de mot de passe incorrect Internet**</span><span class="sxs-lookup"><span data-stu-id="592b4-261"><span id="ERROR_INTERNET_INCORRECT_PASSWORD"></span><span id="error_internet_incorrect_password"></span>**ERROR\_INTERNET\_INCORRECT\_PASSWORD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-262">12014</span><span class="sxs-lookup"><span data-stu-id="592b4-262">12014</span></span>
</dt> <dt>



<span data-ttu-id="592b4-263">La demande de connexion et d’ouverture de session sur un serveur FTP n’a pas pu aboutir car le mot de passe fourni est incorrect.</span><span class="sxs-lookup"><span data-stu-id="592b4-263">The request to connect and log on to an FTP server could not be completed because the supplied password is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-264"><span id="ERROR_INTERNET_INCORRECT_USER_NAME"></span><span id="error_internet_incorrect_user_name"></span>**ERREUR \_ Internet \_ \_ nom d’utilisateur incorrect \_**</span><span class="sxs-lookup"><span data-stu-id="592b4-264"><span id="ERROR_INTERNET_INCORRECT_USER_NAME"></span><span id="error_internet_incorrect_user_name"></span>**ERROR\_INTERNET\_INCORRECT\_USER\_NAME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-265">12013</span><span class="sxs-lookup"><span data-stu-id="592b4-265">12013</span></span>
</dt> <dt>



<span data-ttu-id="592b4-266">La demande de connexion et d’ouverture de session sur un serveur FTP n’a pas pu aboutir car le nom d’utilisateur fourni est incorrect.</span><span class="sxs-lookup"><span data-stu-id="592b4-266">The request to connect and log on to an FTP server could not be completed because the supplied user name is incorrect.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-267"><span id="ERROR_INTERNET_INSERT_CDROM"></span><span id="error_internet_insert_cdrom"></span>**ERREUR d' \_ insertion Internet dans le \_ \_ cdrom**</span><span class="sxs-lookup"><span data-stu-id="592b4-267"><span id="ERROR_INTERNET_INSERT_CDROM"></span><span id="error_internet_insert_cdrom"></span>**ERROR\_INTERNET\_INSERT\_CDROM**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-268">12053</span><span class="sxs-lookup"><span data-stu-id="592b4-268">12053</span></span>
</dt> <dt>



<span data-ttu-id="592b4-269">La demande nécessite l’insertion d’un CD-ROM dans le lecteur de CD-ROM pour localiser la ressource demandée.</span><span class="sxs-lookup"><span data-stu-id="592b4-269">The request requires a CD-ROM to be inserted in the CD-ROM drive to locate the resource requested.</span></span>

> [!Note]  
> <span data-ttu-id="592b4-270">Windows Vista et Windows Server 2008 et versions antérieures uniquement.</span><span class="sxs-lookup"><span data-stu-id="592b4-270">Windows Vista and Windows Server 2008 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-271"><span id="ERROR_INTERNET_INTERNAL_ERROR"></span><span id="error_internet_internal_error"></span>**erreur \_ \_ interne Internet \_**</span><span class="sxs-lookup"><span data-stu-id="592b4-271"><span id="ERROR_INTERNET_INTERNAL_ERROR"></span><span id="error_internet_internal_error"></span>**ERROR\_INTERNET\_INTERNAL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-272">12004</span><span class="sxs-lookup"><span data-stu-id="592b4-272">12004</span></span>
</dt> <dt>



<span data-ttu-id="592b4-273">Une erreur interne s'est produite.</span><span class="sxs-lookup"><span data-stu-id="592b4-273">An internal error has occurred.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-274"><span id="ERROR_INTERNET_INVALID_CA"></span><span id="error_internet_invalid_ca"></span>**ERREUR \_ Internet \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="592b4-274"><span id="ERROR_INTERNET_INVALID_CA"></span><span id="error_internet_invalid_ca"></span>**ERROR\_INTERNET\_INVALID\_CA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-275">12045</span><span class="sxs-lookup"><span data-stu-id="592b4-275">12045</span></span>
</dt> <dt>



<span data-ttu-id="592b4-276">La fonction ne connaît pas l’autorité de certification qui a généré le certificat du serveur.</span><span class="sxs-lookup"><span data-stu-id="592b4-276">The function is unfamiliar with the Certificate Authority that generated the server's certificate.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-277"><span id="ERROR_INTERNET_INVALID_OPERATION"></span><span id="error_internet_invalid_operation"></span>**ERREUR \_ Internet \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="592b4-277"><span id="ERROR_INTERNET_INVALID_OPERATION"></span><span id="error_internet_invalid_operation"></span>**ERROR\_INTERNET\_INVALID\_OPERATION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-278">12016</span><span class="sxs-lookup"><span data-stu-id="592b4-278">12016</span></span>
</dt> <dt>



<span data-ttu-id="592b4-279">L’opération demandée n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="592b4-279">The requested operation is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-280"><span id="ERROR_INTERNET_INVALID_OPTION"></span><span id="error_internet_invalid_option"></span>**\_option Internet \_ non valide \_ d’erreur**</span><span class="sxs-lookup"><span data-stu-id="592b4-280"><span id="ERROR_INTERNET_INVALID_OPTION"></span><span id="error_internet_invalid_option"></span>**ERROR\_INTERNET\_INVALID\_OPTION**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-281">12009</span><span class="sxs-lookup"><span data-stu-id="592b4-281">12009</span></span>
</dt> <dt>



<span data-ttu-id="592b4-282">Une requête à [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) ou [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) A spécifié une valeur d’option non valide.</span><span class="sxs-lookup"><span data-stu-id="592b4-282">A request to [**InternetQueryOption**](/windows/desktop/api/Wininet/nf-wininet-internetqueryoptiona) or [**InternetSetOption**](/windows/desktop/api/Wininet/nf-wininet-internetsetoptiona) specified an invalid option value.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-283"><span id="ERROR_INTERNET_INVALID_PROXY_REQUEST"></span><span id="error_internet_invalid_proxy_request"></span>**ERREUR \_ de \_ \_ demande de proxy non valide Internet \_**</span><span class="sxs-lookup"><span data-stu-id="592b4-283"><span id="ERROR_INTERNET_INVALID_PROXY_REQUEST"></span><span id="error_internet_invalid_proxy_request"></span>**ERROR\_INTERNET\_INVALID\_PROXY\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-284">12033</span><span class="sxs-lookup"><span data-stu-id="592b4-284">12033</span></span>
</dt> <dt>



<span data-ttu-id="592b4-285">La demande adressée au proxy n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="592b4-285">The request to the proxy was invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-286"><span id="ERROR_INTERNET_INVALID_URL"></span><span id="error_internet_invalid_url"></span>**ERREUR \_ \_ URL non valide Internet \_**</span><span class="sxs-lookup"><span data-stu-id="592b4-286"><span id="ERROR_INTERNET_INVALID_URL"></span><span id="error_internet_invalid_url"></span>**ERROR\_INTERNET\_INVALID\_URL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-287">12005</span><span class="sxs-lookup"><span data-stu-id="592b4-287">12005</span></span>
</dt> <dt>



<span data-ttu-id="592b4-288">L’URL n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="592b4-288">The URL is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-289"><span id="ERROR_INTERNET_ITEM_NOT_FOUND"></span><span id="error_internet_item_not_found"></span>**ERREUR \_ Internet \_ élément \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="592b4-289"><span id="ERROR_INTERNET_ITEM_NOT_FOUND"></span><span id="error_internet_item_not_found"></span>**ERROR\_INTERNET\_ITEM\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-290">12028</span><span class="sxs-lookup"><span data-stu-id="592b4-290">12028</span></span>
</dt> <dt>



<span data-ttu-id="592b4-291">L’élément demandé est introuvable.</span><span class="sxs-lookup"><span data-stu-id="592b4-291">The requested item could not be located.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-292"><span id="ERROR_INTERNET_LOGIN_FAILURE"></span><span id="error_internet_login_failure"></span>**ERREUR \_ de \_ connexion \_ Internet**</span><span class="sxs-lookup"><span data-stu-id="592b4-292"><span id="ERROR_INTERNET_LOGIN_FAILURE"></span><span id="error_internet_login_failure"></span>**ERROR\_INTERNET\_LOGIN\_FAILURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-293">12015</span><span class="sxs-lookup"><span data-stu-id="592b4-293">12015</span></span>
</dt> <dt>



<span data-ttu-id="592b4-294">La demande de connexion et d’ouverture de session sur un serveur FTP a échoué.</span><span class="sxs-lookup"><span data-stu-id="592b4-294">The request to connect and log on to an FTP server failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-295"><span id="ERROR_INTERNET_LOGIN_FAILURE_DISPLAY_ENTITY_BODY"></span><span id="error_internet_login_failure_display_entity_body"></span>**ERREUR \_ de \_ connexion \_ Internet \_ afficher \_ le \_ corps de l’entité**</span><span class="sxs-lookup"><span data-stu-id="592b4-295"><span id="ERROR_INTERNET_LOGIN_FAILURE_DISPLAY_ENTITY_BODY"></span><span id="error_internet_login_failure_display_entity_body"></span>**ERROR\_INTERNET\_LOGIN\_FAILURE\_DISPLAY\_ENTITY\_BODY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-296">12174</span><span class="sxs-lookup"><span data-stu-id="592b4-296">12174</span></span>
</dt> <dt>



<span data-ttu-id="592b4-297">L’en-tête Digest MS-Logoff a été retourné à partir du site Web.</span><span class="sxs-lookup"><span data-stu-id="592b4-297">The MS-Logoff digest header has been returned from the website.</span></span> <span data-ttu-id="592b4-298">Cet en-tête demande spécifiquement au package de résumé de purger les informations d’identification du domaine associé.</span><span class="sxs-lookup"><span data-stu-id="592b4-298">This header specifically instructs the digest package to purge credentials for the associated realm.</span></span> <span data-ttu-id="592b4-299">Cette erreur est renvoyée uniquement si l’option le corps d’entité de l' [échec de connexion de \_ masque d’erreur \_ \_ \_ \_ \_ \_ Internet](option-flags.md) est définie ; sinon, l' **erreur de \_ \_ connexion Internet \_** est retournée.</span><span class="sxs-lookup"><span data-stu-id="592b4-299">This error will only be returned if [INTERNET\_ERROR\_MASK\_LOGIN\_FAILURE\_DISPLAY\_ENTITY\_BODY](option-flags.md) option has been set; otherwise, **ERROR\_INTERNET\_LOGIN\_FAILURE** is returned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-300"><span id="ERROR_INTERNET_MIXED_SECURITY"></span><span id="error_internet_mixed_security"></span>**ERREUR \_ de \_ sécurité mixte Internet \_**</span><span class="sxs-lookup"><span data-stu-id="592b4-300"><span id="ERROR_INTERNET_MIXED_SECURITY"></span><span id="error_internet_mixed_security"></span>**ERROR\_INTERNET\_MIXED\_SECURITY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-301">12041</span><span class="sxs-lookup"><span data-stu-id="592b4-301">12041</span></span>
</dt> <dt>



<span data-ttu-id="592b4-302">Le contenu n’est pas entièrement sécurisé.</span><span class="sxs-lookup"><span data-stu-id="592b4-302">The content is not entirely secure.</span></span> <span data-ttu-id="592b4-303">Une partie du contenu affiché peut provenir de serveurs non sécurisés.</span><span class="sxs-lookup"><span data-stu-id="592b4-303">Some of the content being viewed may have come from unsecured servers.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-304"><span id="ERROR_INTERNET_NAME_NOT_RESOLVED"></span><span id="error_internet_name_not_resolved"></span>**ERREUR \_ de \_ nom Internet \_ non \_ résolu**</span><span class="sxs-lookup"><span data-stu-id="592b4-304"><span id="ERROR_INTERNET_NAME_NOT_RESOLVED"></span><span id="error_internet_name_not_resolved"></span>**ERROR\_INTERNET\_NAME\_NOT\_RESOLVED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-305">12007</span><span class="sxs-lookup"><span data-stu-id="592b4-305">12007</span></span>
</dt> <dt>



<span data-ttu-id="592b4-306">Impossible de résoudre le nom du serveur.</span><span class="sxs-lookup"><span data-stu-id="592b4-306">The server name could not be resolved.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-307"><span id="ERROR_INTERNET_NEED_MSN_SSPI_PKG"></span><span id="error_internet_need_msn_sspi_pkg"></span>**ERREUR \_ Internet \_ besoin de \_ MSN \_ SSPI \_ pkg**</span><span class="sxs-lookup"><span data-stu-id="592b4-307"><span id="ERROR_INTERNET_NEED_MSN_SSPI_PKG"></span><span id="error_internet_need_msn_sspi_pkg"></span>**ERROR\_INTERNET\_NEED\_MSN\_SSPI\_PKG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-308">12173</span><span class="sxs-lookup"><span data-stu-id="592b4-308">12173</span></span>
</dt> <dt>



<span data-ttu-id="592b4-309">Actuellement non implémenté.</span><span class="sxs-lookup"><span data-stu-id="592b4-309">Not currently implemented.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-310"><span id="ERROR_INTERNET_NEED_UI"></span><span id="error_internet_need_ui"></span>**ERREUR \_ Internet \_ nécessitant une \_ interface utilisateur**</span><span class="sxs-lookup"><span data-stu-id="592b4-310"><span id="ERROR_INTERNET_NEED_UI"></span><span id="error_internet_need_ui"></span>**ERROR\_INTERNET\_NEED\_UI**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-311">12034</span><span class="sxs-lookup"><span data-stu-id="592b4-311">12034</span></span>
</dt> <dt>



<span data-ttu-id="592b4-312">Une interface utilisateur ou une autre opération de blocage a été demandée.</span><span class="sxs-lookup"><span data-stu-id="592b4-312">A user interface or other blocking operation has been requested.</span></span>

> [!Note]  
> <span data-ttu-id="592b4-313">Windows Vista et Windows Server 2008 et versions antérieures uniquement.</span><span class="sxs-lookup"><span data-stu-id="592b4-313">Windows Vista and Windows Server 2008 and earlier only.</span></span>

 


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-314"><span id="ERROR_INTERNET_NO_CALLBACK"></span><span id="error_internet_no_callback"></span>**ERREUR \_ Internet \_ aucun \_ rappel**</span><span class="sxs-lookup"><span data-stu-id="592b4-314"><span id="ERROR_INTERNET_NO_CALLBACK"></span><span id="error_internet_no_callback"></span>**ERROR\_INTERNET\_NO\_CALLBACK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-315">12025</span><span class="sxs-lookup"><span data-stu-id="592b4-315">12025</span></span>
</dt> <dt>



<span data-ttu-id="592b4-316">Une requête asynchrone n’a pas pu être effectuée, car aucune fonction de rappel n’a été définie.</span><span class="sxs-lookup"><span data-stu-id="592b4-316">An asynchronous request could not be made because a callback function has not been set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-317"><span id="ERROR_INTERNET_NO_CONTEXT"></span><span id="error_internet_no_context"></span>**ERREUR \_ Internet \_ aucun \_ contexte**</span><span class="sxs-lookup"><span data-stu-id="592b4-317"><span id="ERROR_INTERNET_NO_CONTEXT"></span><span id="error_internet_no_context"></span>**ERROR\_INTERNET\_NO\_CONTEXT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-318">12024</span><span class="sxs-lookup"><span data-stu-id="592b4-318">12024</span></span>
</dt> <dt>



<span data-ttu-id="592b4-319">Une requête asynchrone n’a pas pu être effectuée, car une valeur de contexte zéro a été fournie.</span><span class="sxs-lookup"><span data-stu-id="592b4-319">An asynchronous request could not be made because a zero context value was supplied.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-320"><span id="ERROR_INTERNET_NO_DIRECT_ACCESS"></span><span id="error_internet_no_direct_access"></span>**ERREUR \_ Internet \_ aucun \_ \_ accès direct**</span><span class="sxs-lookup"><span data-stu-id="592b4-320"><span id="ERROR_INTERNET_NO_DIRECT_ACCESS"></span><span id="error_internet_no_direct_access"></span>**ERROR\_INTERNET\_NO\_DIRECT\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-321">12023</span><span class="sxs-lookup"><span data-stu-id="592b4-321">12023</span></span>
</dt> <dt>



<span data-ttu-id="592b4-322">L’accès direct au réseau ne peut pas être effectué pour le moment.</span><span class="sxs-lookup"><span data-stu-id="592b4-322">Direct network access cannot be made at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-323"><span id="ERROR_INTERNET_NOT_INITIALIZED"></span><span id="error_internet_not_initialized"></span>**ERREUR \_ Internet \_ non \_ initialisée**</span><span class="sxs-lookup"><span data-stu-id="592b4-323"><span id="ERROR_INTERNET_NOT_INITIALIZED"></span><span id="error_internet_not_initialized"></span>**ERROR\_INTERNET\_NOT\_INITIALIZED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-324">12172</span><span class="sxs-lookup"><span data-stu-id="592b4-324">12172</span></span>
</dt> <dt>



<span data-ttu-id="592b4-325">L’initialisation de l’API WinINet n’a pas eu lieu.</span><span class="sxs-lookup"><span data-stu-id="592b4-325">Initialization of the WinINet API has not occurred.</span></span> <span data-ttu-id="592b4-326">Indique qu’une fonction de niveau supérieur, telle que [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena), n’a pas encore été appelée.</span><span class="sxs-lookup"><span data-stu-id="592b4-326">Indicates that a higher-level function, such as [**InternetOpen**](/windows/desktop/api/Wininet/nf-wininet-internetopena), has not been called yet.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-327"><span id="ERROR_INTERNET_NOT_PROXY_REQUEST"></span><span id="error_internet_not_proxy_request"></span>**ERREUR \_ Internet \_ not \_ proxy \_**</span><span class="sxs-lookup"><span data-stu-id="592b4-327"><span id="ERROR_INTERNET_NOT_PROXY_REQUEST"></span><span id="error_internet_not_proxy_request"></span>**ERROR\_INTERNET\_NOT\_PROXY\_REQUEST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-328">12020</span><span class="sxs-lookup"><span data-stu-id="592b4-328">12020</span></span>
</dt> <dt>



<span data-ttu-id="592b4-329">La demande ne peut pas être effectuée via un proxy.</span><span class="sxs-lookup"><span data-stu-id="592b4-329">The request cannot be made via a proxy.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-330"><span id="ERROR_INTERNET_OPERATION_CANCELLED"></span><span id="error_internet_operation_cancelled"></span>**ERREUR de l' \_ \_ opération Internet \_ annulée**</span><span class="sxs-lookup"><span data-stu-id="592b4-330"><span id="ERROR_INTERNET_OPERATION_CANCELLED"></span><span id="error_internet_operation_cancelled"></span>**ERROR\_INTERNET\_OPERATION\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-331">12017</span><span class="sxs-lookup"><span data-stu-id="592b4-331">12017</span></span>
</dt> <dt>



<span data-ttu-id="592b4-332">L’opération a été annulée, généralement parce que le descripteur sur lequel la demande a été exécutée a été fermé avant la fin de l’opération.</span><span class="sxs-lookup"><span data-stu-id="592b4-332">The operation was canceled, usually because the handle on which the request was operating was closed before the operation completed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-333"><span id="ERROR_INTERNET_OPTION_NOT_SETTABLE"></span><span id="error_internet_option_not_settable"></span>**ERREUR \_ Internet \_ \_ non \_ définissable**</span><span class="sxs-lookup"><span data-stu-id="592b4-333"><span id="ERROR_INTERNET_OPTION_NOT_SETTABLE"></span><span id="error_internet_option_not_settable"></span>**ERROR\_INTERNET\_OPTION\_NOT\_SETTABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-334">12011</span><span class="sxs-lookup"><span data-stu-id="592b4-334">12011</span></span>
</dt> <dt>



<span data-ttu-id="592b4-335">L’option demandée ne peut pas être définie, uniquement interrogée.</span><span class="sxs-lookup"><span data-stu-id="592b4-335">The requested option cannot be set, only queried.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-336"><span id="ERROR_INTERNET_OUT_OF_HANDLES"></span><span id="error_internet_out_of_handles"></span>**ERREUR \_ Internet \_ hors \_ des \_ Handles**</span><span class="sxs-lookup"><span data-stu-id="592b4-336"><span id="ERROR_INTERNET_OUT_OF_HANDLES"></span><span id="error_internet_out_of_handles"></span>**ERROR\_INTERNET\_OUT\_OF\_HANDLES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-337">12001</span><span class="sxs-lookup"><span data-stu-id="592b4-337">12001</span></span>
</dt> <dt>



<span data-ttu-id="592b4-338">Aucun autre handle n’a pu être généré pour l’instant.</span><span class="sxs-lookup"><span data-stu-id="592b4-338">No more handles could be generated at this time.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-339"><span id="ERROR_INTERNET_POST_IS_NON_SECURE"></span><span id="error_internet_post_is_non_secure"></span>**ERREUR \_ Internet \_ poster \_ \_ non \_ sécurisée**</span><span class="sxs-lookup"><span data-stu-id="592b4-339"><span id="ERROR_INTERNET_POST_IS_NON_SECURE"></span><span id="error_internet_post_is_non_secure"></span>**ERROR\_INTERNET\_POST\_IS\_NON\_SECURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-340">12043</span><span class="sxs-lookup"><span data-stu-id="592b4-340">12043</span></span>
</dt> <dt>



<span data-ttu-id="592b4-341">L’application publie des données sur un serveur qui n’est pas sécurisé.</span><span class="sxs-lookup"><span data-stu-id="592b4-341">The application is posting data to a server that is not secure.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-342"><span id="ERROR_INTERNET_PROTOCOL_NOT_FOUND"></span><span id="error_internet_protocol_not_found"></span>**ERREUR \_ \_ protocole Internet \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="592b4-342"><span id="ERROR_INTERNET_PROTOCOL_NOT_FOUND"></span><span id="error_internet_protocol_not_found"></span>**ERROR\_INTERNET\_PROTOCOL\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-343">12008</span><span class="sxs-lookup"><span data-stu-id="592b4-343">12008</span></span>
</dt> <dt>



<span data-ttu-id="592b4-344">Le protocole demandé est introuvable.</span><span class="sxs-lookup"><span data-stu-id="592b4-344">The requested protocol could not be located.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-345"><span id="ERROR_INTERNET_PROXY_SERVER_UNREACHABLE"></span><span id="error_internet_proxy_server_unreachable"></span>**ERREUR \_ \_ Impossible d' \_ atteindre le serveur proxy Internet \_**</span><span class="sxs-lookup"><span data-stu-id="592b4-345"><span id="ERROR_INTERNET_PROXY_SERVER_UNREACHABLE"></span><span id="error_internet_proxy_server_unreachable"></span>**ERROR\_INTERNET\_PROXY\_SERVER\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-346">12165</span><span class="sxs-lookup"><span data-stu-id="592b4-346">12165</span></span>
</dt> <dt>



<span data-ttu-id="592b4-347">Impossible d’accéder au serveur proxy désigné.</span><span class="sxs-lookup"><span data-stu-id="592b4-347">The designated proxy server cannot be reached.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-348"><span id="ERROR_INTERNET_REDIRECT_SCHEME_CHANGE"></span><span id="error_internet_redirect_scheme_change"></span>**ERREUR \_ de \_ modification du schéma de redirection Internet \_ \_**</span><span class="sxs-lookup"><span data-stu-id="592b4-348"><span id="ERROR_INTERNET_REDIRECT_SCHEME_CHANGE"></span><span id="error_internet_redirect_scheme_change"></span>**ERROR\_INTERNET\_REDIRECT\_SCHEME\_CHANGE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-349">12048</span><span class="sxs-lookup"><span data-stu-id="592b4-349">12048</span></span>
</dt> <dt>



<span data-ttu-id="592b4-350">La fonction n’a pas pu gérer la redirection, car le schéma a changé (par exemple, HTTP vers FTP).</span><span class="sxs-lookup"><span data-stu-id="592b4-350">The function could not handle the redirection, because the scheme changed (for example, HTTP to FTP).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-351"><span id="ERROR_INTERNET_REGISTRY_VALUE_NOT_FOUND"></span><span id="error_internet_registry_value_not_found"></span>**ERREUR de la \_ \_ valeur de registre Internet \_ \_ \_ introuvable**</span><span class="sxs-lookup"><span data-stu-id="592b4-351"><span id="ERROR_INTERNET_REGISTRY_VALUE_NOT_FOUND"></span><span id="error_internet_registry_value_not_found"></span>**ERROR\_INTERNET\_REGISTRY\_VALUE\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-352">12021</span><span class="sxs-lookup"><span data-stu-id="592b4-352">12021</span></span>
</dt> <dt>



<span data-ttu-id="592b4-353">Une valeur de registre requise n’a pas pu être localisée.</span><span class="sxs-lookup"><span data-stu-id="592b4-353">A required registry value could not be located.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-354"><span id="ERROR_INTERNET_REQUEST_PENDING"></span><span id="error_internet_request_pending"></span>**\_requête Internet \_ \_ en attente d’erreur**</span><span class="sxs-lookup"><span data-stu-id="592b4-354"><span id="ERROR_INTERNET_REQUEST_PENDING"></span><span id="error_internet_request_pending"></span>**ERROR\_INTERNET\_REQUEST\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-355">12026</span><span class="sxs-lookup"><span data-stu-id="592b4-355">12026</span></span>
</dt> <dt>



<span data-ttu-id="592b4-356">L’opération requise n’a pas pu aboutir car une ou plusieurs demandes sont en attente.</span><span class="sxs-lookup"><span data-stu-id="592b4-356">The required operation could not be completed because one or more requests are pending.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-357"><span id="ERROR_INTERNET_RETRY_DIALOG"></span><span id="error_internet_retry_dialog"></span>**\_boîte de dialogue erreur Internet de \_ nouvelle tentative \_**</span><span class="sxs-lookup"><span data-stu-id="592b4-357"><span id="ERROR_INTERNET_RETRY_DIALOG"></span><span id="error_internet_retry_dialog"></span>**ERROR\_INTERNET\_RETRY\_DIALOG**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-358">12050</span><span class="sxs-lookup"><span data-stu-id="592b4-358">12050</span></span>
</dt> <dt>



<span data-ttu-id="592b4-359">La boîte de dialogue doit être retentée.</span><span class="sxs-lookup"><span data-stu-id="592b4-359">The dialog box should be retried.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-360"><span id="ERROR_INTERNET_SEC_CERT_CN_INVALID"></span><span id="error_internet_sec_cert_cn_invalid"></span>**ERREUR \_ de \_ certificat CN de l’Internet s \_ \_ \_ non valide**</span><span class="sxs-lookup"><span data-stu-id="592b4-360"><span id="ERROR_INTERNET_SEC_CERT_CN_INVALID"></span><span id="error_internet_sec_cert_cn_invalid"></span>**ERROR\_INTERNET\_SEC\_CERT\_CN\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-361">12038</span><span class="sxs-lookup"><span data-stu-id="592b4-361">12038</span></span>
</dt> <dt>



<span data-ttu-id="592b4-362">Le nom commun du certificat SSL (champ de nom d’hôte) est incorrect. par exemple, si vous avez entré www.server.com et que le nom commun sur le certificat indique www.different.com.</span><span class="sxs-lookup"><span data-stu-id="592b4-362">SSL certificate common name (host name field) is incorrect for example, if you entered www.server.com and the common name on the certificate says www.different.com.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-363"><span id="ERROR_INTERNET_SEC_CERT_DATE_INVALID"></span><span id="error_internet_sec_cert_date_invalid"></span>**ERREUR \_ Internet \_ sec \_ date du certificat \_ \_ non valide**</span><span class="sxs-lookup"><span data-stu-id="592b4-363"><span id="ERROR_INTERNET_SEC_CERT_DATE_INVALID"></span><span id="error_internet_sec_cert_date_invalid"></span>**ERROR\_INTERNET\_SEC\_CERT\_DATE\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-364">12037</span><span class="sxs-lookup"><span data-stu-id="592b4-364">12037</span></span>
</dt> <dt>



<span data-ttu-id="592b4-365">La date de certificat SSL reçue du serveur est incorrecte.</span><span class="sxs-lookup"><span data-stu-id="592b4-365">SSL certificate date that was received from the server is bad.</span></span> <span data-ttu-id="592b4-366">Le certificat a expiré.</span><span class="sxs-lookup"><span data-stu-id="592b4-366">The certificate is expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-367"><span id="ERROR_INTERNET_SEC_CERT_ERRORS"></span><span id="error_internet_sec_cert_errors"></span>**\_Erreurs de \_ certificat Internet s \_ \_**</span><span class="sxs-lookup"><span data-stu-id="592b4-367"><span id="ERROR_INTERNET_SEC_CERT_ERRORS"></span><span id="error_internet_sec_cert_errors"></span>**ERROR\_INTERNET\_SEC\_CERT\_ERRORS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-368">12055</span><span class="sxs-lookup"><span data-stu-id="592b4-368">12055</span></span>
</dt> <dt>



<span data-ttu-id="592b4-369">Le certificat SSL contient des erreurs.</span><span class="sxs-lookup"><span data-stu-id="592b4-369">The SSL certificate contains errors.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-370"><span id="ERROR_INTERNET_SEC_CERT_NO_REV"></span><span id="error_internet_sec_cert_no_rev"></span>**ERREUR \_ Internet \_ s \_ CERT \_ no \_ Rev**</span><span class="sxs-lookup"><span data-stu-id="592b4-370"><span id="ERROR_INTERNET_SEC_CERT_NO_REV"></span><span id="error_internet_sec_cert_no_rev"></span>**ERROR\_INTERNET\_SEC\_CERT\_NO\_REV**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-371">12056</span><span class="sxs-lookup"><span data-stu-id="592b4-371">12056</span></span>
</dt> <dt>



<span data-ttu-id="592b4-372">Le certificat SSL n’a pas été révoqué.</span><span class="sxs-lookup"><span data-stu-id="592b4-372">The SSL certificate was not revoked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-373"><span id="ERROR_INTERNET_SEC_CERT_REV_FAILED"></span><span id="error_internet_sec_cert_rev_failed"></span>**ERREUR \_ Internet \_ seconde le \_ certificat \_ Rev \_ a échoué**</span><span class="sxs-lookup"><span data-stu-id="592b4-373"><span id="ERROR_INTERNET_SEC_CERT_REV_FAILED"></span><span id="error_internet_sec_cert_rev_failed"></span>**ERROR\_INTERNET\_SEC\_CERT\_REV\_FAILED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-374">12057</span><span class="sxs-lookup"><span data-stu-id="592b4-374">12057</span></span>
</dt> <dt>



<span data-ttu-id="592b4-375">Échec de la révocation du certificat SSL.</span><span class="sxs-lookup"><span data-stu-id="592b4-375">Revocation of the SSL certificate failed.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-376"><span id="ERROR_INTERNET_SEC_CERT_REVOKED"></span><span id="error_internet_sec_cert_revoked"></span>**ERREUR \_ Internet \_ sec \_ certificat \_ révoqué**</span><span class="sxs-lookup"><span data-stu-id="592b4-376"><span id="ERROR_INTERNET_SEC_CERT_REVOKED"></span><span id="error_internet_sec_cert_revoked"></span>**ERROR\_INTERNET\_SEC\_CERT\_REVOKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-377">12170</span><span class="sxs-lookup"><span data-stu-id="592b4-377">12170</span></span>
</dt> <dt>



<span data-ttu-id="592b4-378">Le certificat SSL a été révoqué.</span><span class="sxs-lookup"><span data-stu-id="592b4-378">The SSL certificate was revoked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-379"><span id="ERROR_INTERNET_SEC_INVALID_CERT"></span><span id="error_internet_sec_invalid_cert"></span>**ERREUR \_ Internet \_ s \_ certificat non valide \_**</span><span class="sxs-lookup"><span data-stu-id="592b4-379"><span id="ERROR_INTERNET_SEC_INVALID_CERT"></span><span id="error_internet_sec_invalid_cert"></span>**ERROR\_INTERNET\_SEC\_INVALID\_CERT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-380">12169</span><span class="sxs-lookup"><span data-stu-id="592b4-380">12169</span></span>
</dt> <dt>



<span data-ttu-id="592b4-381">Le certificat SSL n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="592b4-381">The SSL certificate is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-382"><span id="ERROR_INTERNET_SECURITY_CHANNEL_ERROR"></span><span id="error_internet_security_channel_error"></span>**erreur \_ de \_ canal de sécurité Internet \_ \_**</span><span class="sxs-lookup"><span data-stu-id="592b4-382"><span id="ERROR_INTERNET_SECURITY_CHANNEL_ERROR"></span><span id="error_internet_security_channel_error"></span>**ERROR\_INTERNET\_SECURITY\_CHANNEL\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-383">12157</span><span class="sxs-lookup"><span data-stu-id="592b4-383">12157</span></span>
</dt> <dt>



<span data-ttu-id="592b4-384">L’application a rencontré une erreur interne lors du chargement des bibliothèques SSL.</span><span class="sxs-lookup"><span data-stu-id="592b4-384">The application experienced an internal error loading the SSL libraries.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-385"><span id="ERROR_INTERNET_SERVER_UNREACHABLE"></span><span id="error_internet_server_unreachable"></span>**ERREUR \_ \_ serveur Internet \_ inaccessible**</span><span class="sxs-lookup"><span data-stu-id="592b4-385"><span id="ERROR_INTERNET_SERVER_UNREACHABLE"></span><span id="error_internet_server_unreachable"></span>**ERROR\_INTERNET\_SERVER\_UNREACHABLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-386">12164</span><span class="sxs-lookup"><span data-stu-id="592b4-386">12164</span></span>
</dt> <dt>



<span data-ttu-id="592b4-387">Le site Web ou le serveur indiqué est inaccessible.</span><span class="sxs-lookup"><span data-stu-id="592b4-387">The website or server indicated is unreachable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-388"><span id="ERROR_INTERNET_SHUTDOWN"></span><span id="error_internet_shutdown"></span>**ERREUR \_ d' \_ arrêt Internet**</span><span class="sxs-lookup"><span data-stu-id="592b4-388"><span id="ERROR_INTERNET_SHUTDOWN"></span><span id="error_internet_shutdown"></span>**ERROR\_INTERNET\_SHUTDOWN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-389">12012</span><span class="sxs-lookup"><span data-stu-id="592b4-389">12012</span></span>
</dt> <dt>



<span data-ttu-id="592b4-390">La prise en charge de WinINet est en cours d’arrêt ou de déchargement.</span><span class="sxs-lookup"><span data-stu-id="592b4-390">WinINet support is being shut down or unloaded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-391"><span id="ERROR_INTERNET_TCPIP_NOT_INSTALLED"></span><span id="error_internet_tcpip_not_installed"></span>**ERREUR \_ Internet \_ tcpip \_ non \_ installée**</span><span class="sxs-lookup"><span data-stu-id="592b4-391"><span id="ERROR_INTERNET_TCPIP_NOT_INSTALLED"></span><span id="error_internet_tcpip_not_installed"></span>**ERROR\_INTERNET\_TCPIP\_NOT\_INSTALLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-392">12159</span><span class="sxs-lookup"><span data-stu-id="592b4-392">12159</span></span>
</dt> <dt>



<span data-ttu-id="592b4-393">La pile de protocoles requise n’est pas chargée et l’application ne peut pas démarrer WinSock.</span><span class="sxs-lookup"><span data-stu-id="592b4-393">The required protocol stack is not loaded and the application cannot start WinSock.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-394"><span id="ERROR_INTERNET_TIMEOUT"></span><span id="error_internet_timeout"></span>**ERREUR \_ \_ d’expiration Internet**</span><span class="sxs-lookup"><span data-stu-id="592b4-394"><span id="ERROR_INTERNET_TIMEOUT"></span><span id="error_internet_timeout"></span>**ERROR\_INTERNET\_TIMEOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-395">12002</span><span class="sxs-lookup"><span data-stu-id="592b4-395">12002</span></span>
</dt> <dt>



<span data-ttu-id="592b4-396">Le délai d'attente de la requête a expiré.</span><span class="sxs-lookup"><span data-stu-id="592b4-396">The request has timed out.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-397"><span id="ERROR_INTERNET_UNABLE_TO_CACHE_FILE"></span><span id="error_internet_unable_to_cache_file"></span>**ERREUR \_ Internet \_ Impossible \_ de mettre \_ en cache le \_ fichier**</span><span class="sxs-lookup"><span data-stu-id="592b4-397"><span id="ERROR_INTERNET_UNABLE_TO_CACHE_FILE"></span><span id="error_internet_unable_to_cache_file"></span>**ERROR\_INTERNET\_UNABLE\_TO\_CACHE\_FILE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-398">12158</span><span class="sxs-lookup"><span data-stu-id="592b4-398">12158</span></span>
</dt> <dt>



<span data-ttu-id="592b4-399">La fonction n’a pas pu mettre en cache le fichier.</span><span class="sxs-lookup"><span data-stu-id="592b4-399">The function was unable to cache the file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-400"><span id="ERROR_INTERNET_UNABLE_TO_DOWNLOAD_SCRIPT"></span><span id="error_internet_unable_to_download_script"></span>**ERREUR \_ Internet \_ Impossible \_ de \_ Télécharger le \_ script**</span><span class="sxs-lookup"><span data-stu-id="592b4-400"><span id="ERROR_INTERNET_UNABLE_TO_DOWNLOAD_SCRIPT"></span><span id="error_internet_unable_to_download_script"></span>**ERROR\_INTERNET\_UNABLE\_TO\_DOWNLOAD\_SCRIPT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-401">12167</span><span class="sxs-lookup"><span data-stu-id="592b4-401">12167</span></span>
</dt> <dt>



<span data-ttu-id="592b4-402">Impossible de télécharger le script de configuration automatique du proxy.</span><span class="sxs-lookup"><span data-stu-id="592b4-402">The automatic proxy configuration script could not be downloaded.</span></span> <span data-ttu-id="592b4-403">L’indicateur \_ de \_ demande de cache Internet doit être \_ \_ défini.</span><span class="sxs-lookup"><span data-stu-id="592b4-403">The INTERNET\_FLAG\_MUST\_CACHE\_REQUEST flag was set.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-404"><span id="ERROR_INTERNET_UNRECOGNIZED_SCHEME"></span><span id="error_internet_unrecognized_scheme"></span>**ERREUR \_ de \_ schéma non reconnu Internet \_**</span><span class="sxs-lookup"><span data-stu-id="592b4-404"><span id="ERROR_INTERNET_UNRECOGNIZED_SCHEME"></span><span id="error_internet_unrecognized_scheme"></span>**ERROR\_INTERNET\_UNRECOGNIZED\_SCHEME**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="592b4-405">12006</span><span class="sxs-lookup"><span data-stu-id="592b4-405">12006</span></span>
</dt> <dt>



<span data-ttu-id="592b4-406">Le schéma d’URL n’a pas pu être reconnu ou n’est pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="592b4-406">The URL scheme could not be recognized, or is not supported.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-407"><span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**HANDLE d’erreur \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="592b4-407"><span id="ERROR_INVALID_HANDLE"></span><span id="error_invalid_handle"></span>**ERROR\_INVALID\_HANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="592b4-408">Le handle qui a été passé à l’API a été invalidé ou fermé.</span><span class="sxs-lookup"><span data-stu-id="592b4-408">The handle that was passed to the API has been either invalidated or closed.</span></span>

<span data-ttu-id="592b4-409">**En-tête :** Déclaré dans Winerror. h</span><span class="sxs-lookup"><span data-stu-id="592b4-409">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-410"><span id="ERROR_MORE_DATA"></span><span id="error_more_data"></span>**ERREUR \_ plus de \_ données**</span><span class="sxs-lookup"><span data-stu-id="592b4-410"><span id="ERROR_MORE_DATA"></span><span id="error_more_data"></span>**ERROR\_MORE\_DATA**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="592b4-411">More data is available.</span><span class="sxs-lookup"><span data-stu-id="592b4-411">More data is available.</span></span>

<span data-ttu-id="592b4-412">**En-tête :** Déclaré dans Winerror. h</span><span class="sxs-lookup"><span data-stu-id="592b4-412">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-413"><span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**ERREUR \_ \_ plus aucun \_ fichier**</span><span class="sxs-lookup"><span data-stu-id="592b4-413"><span id="ERROR_NO_MORE_FILES"></span><span id="error_no_more_files"></span>**ERROR\_NO\_MORE\_FILES**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="592b4-414">Aucun autre fichier n’a été trouvé.</span><span class="sxs-lookup"><span data-stu-id="592b4-414">No more files have been found.</span></span>

<span data-ttu-id="592b4-415">**En-tête :** Déclaré dans Winerror. h</span><span class="sxs-lookup"><span data-stu-id="592b4-415">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="592b4-416"><span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**ERREUR \_ aucun \_ autre \_ élément**</span><span class="sxs-lookup"><span data-stu-id="592b4-416"><span id="ERROR_NO_MORE_ITEMS"></span><span id="error_no_more_items"></span>**ERROR\_NO\_MORE\_ITEMS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="592b4-417">Aucun autre élément n’a été trouvé.</span><span class="sxs-lookup"><span data-stu-id="592b4-417">No more items have been found.</span></span>

<span data-ttu-id="592b4-418">**En-tête :** Déclaré dans Winerror. h</span><span class="sxs-lookup"><span data-stu-id="592b4-418">**Header:** Declared in Winerror.h</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="592b4-419">Notes</span><span class="sxs-lookup"><span data-stu-id="592b4-419">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="592b4-420">WinINet ne prend pas en charge les implémentations de serveur.</span><span class="sxs-lookup"><span data-stu-id="592b4-420">WinINet does not support server implementations.</span></span> <span data-ttu-id="592b4-421">En outre, il ne doit pas être utilisé à partir d’un service.</span><span class="sxs-lookup"><span data-stu-id="592b4-421">In addition, it should not be used from a service.</span></span> <span data-ttu-id="592b4-422">Pour les implémentations de serveur ou les services, utilisez les [services http Microsoft Windows (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span><span class="sxs-lookup"><span data-stu-id="592b4-422">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="592b4-423">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="592b4-423">Requirements</span></span>



| <span data-ttu-id="592b4-424">Condition requise</span><span class="sxs-lookup"><span data-stu-id="592b4-424">Requirement</span></span> | <span data-ttu-id="592b4-425">Valeur</span><span class="sxs-lookup"><span data-stu-id="592b4-425">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="592b4-426">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="592b4-426">Minimum supported client</span></span><br/> | <span data-ttu-id="592b4-427">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="592b4-427">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="592b4-428">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="592b4-428">Minimum supported server</span></span><br/> | <span data-ttu-id="592b4-429">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="592b4-429">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="592b4-430">En-tête</span><span class="sxs-lookup"><span data-stu-id="592b4-430">Header</span></span><br/>                   | <dl> <span data-ttu-id="592b4-431"><dt>Wininet. h</dt></span><span class="sxs-lookup"><span data-stu-id="592b4-431"><dt>Wininet.h</dt></span></span> </dl> |



 

