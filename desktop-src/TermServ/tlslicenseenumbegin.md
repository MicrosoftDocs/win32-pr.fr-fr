---
title: TLSLicenseEnumBegin fonction)
description: Commence l’énumération des licences émises par le serveur de licences Bureau à distance en fonction des critères de recherche.
ms.assetid: ec575632-b828-49c0-b326-1ab420381875
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la fonction TLSLicenseEnumBegin
topic_type:
- apiref
api_name:
- TLSLicenseEnumBegin
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 95913337de968d0b30780b5898b7f204d947dd4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743605"
---
# <a name="tlslicenseenumbegin-function"></a><span data-ttu-id="48c66-104">TLSLicenseEnumBegin fonction)</span><span class="sxs-lookup"><span data-stu-id="48c66-104">TLSLicenseEnumBegin function</span></span>

<span data-ttu-id="48c66-105">Commence l’énumération des licences émises par le serveur de licences Bureau à distance en fonction des critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="48c66-105">Begins enumeration of licenses that are issued by the Remote Desktop license server based on search criteria.</span></span>

> [!Note]  
> <span data-ttu-id="48c66-106">Cette fonction n’a aucun fichier d’en-tête ou bibliothèque d’importation associé.</span><span class="sxs-lookup"><span data-stu-id="48c66-106">This function has no associated header file or import library.</span></span> <span data-ttu-id="48c66-107">Pour appeler cette fonction, vous devez créer un fichier d’en-tête défini par l’utilisateur et utiliser les fonctions [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Mstlsapi.dll.</span><span class="sxs-lookup"><span data-stu-id="48c66-107">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mstlsapi.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="48c66-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="48c66-108">Syntax</span></span>


```C++
DWORD WINAPI TLSLicenseEnumBegin(
  _In_  TLS_HANDLE hHandle,
  _In_  DWORD      dwSearchParm,
  _In_  BOOL       bMatchAll,
  _In_  LSLicense  *lpSearchParm,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a><span data-ttu-id="48c66-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="48c66-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="48c66-110">*hHandle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="48c66-110">*hHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48c66-111">Handle vers un serveur de licences Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="48c66-111">Handle to a Remote Desktop license server.</span></span> <span data-ttu-id="48c66-112">Spécifiez un descripteur ouvert par la fonction [**TLSConnectToLsServer**](tlsconnecttolsserver.md) .</span><span class="sxs-lookup"><span data-stu-id="48c66-112">Specify a handle that is opened by the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="48c66-113">*dwSearchParm* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="48c66-113">*dwSearchParm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48c66-114">Spécifie les critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="48c66-114">Specifies the search criteria.</span></span> <span data-ttu-id="48c66-115">Le paramètre peut être une ou une combinaison des valeurs qui sont décrites dans la liste suivante.</span><span class="sxs-lookup"><span data-stu-id="48c66-115">The parameter can be one or a combination of the values that are described in the following list.</span></span> <span data-ttu-id="48c66-116">Le paramètre spécifie le type de jeu de clés et le Pack de clés à rechercher.</span><span class="sxs-lookup"><span data-stu-id="48c66-116">The parameter specifies the type of key pack and which key pack to search.</span></span>

<dt>

<span id="LSLICENSE_SEARCH_LICENSEID"></span><span id="lslicense_search_licenseid"></span>

<span data-ttu-id="48c66-117"><span id="LSLICENSE_SEARCH_LICENSEID"></span><span id="lslicense_search_licenseid"></span>**LSLICENSE \_ Rechercher \_ LICENSEID** (0x00000001)</span><span class="sxs-lookup"><span data-stu-id="48c66-117"><span id="LSLICENSE_SEARCH_LICENSEID"></span><span id="lslicense_search_licenseid"></span>**LSLICENSE\_SEARCH\_LICENSEID** (0x00000001)</span></span>


</dt> <dd>

<span data-ttu-id="48c66-118">Recherchez par ID de licence.</span><span class="sxs-lookup"><span data-stu-id="48c66-118">Search by license ID.</span></span>

</dd> <dt>

<span id="LSLICENSE_SEARCH_KEYPACKID"></span><span id="lslicense_search_keypackid"></span>

<span data-ttu-id="48c66-119"><span id="LSLICENSE_SEARCH_KEYPACKID"></span><span id="lslicense_search_keypackid"></span>**LSLICENSE \_ Rechercher \_ KEYPACKID** (0x00000002)</span><span class="sxs-lookup"><span data-stu-id="48c66-119"><span id="LSLICENSE_SEARCH_KEYPACKID"></span><span id="lslicense_search_keypackid"></span>**LSLICENSE\_SEARCH\_KEYPACKID** (0x00000002)</span></span>


</dt> <dd>

<span data-ttu-id="48c66-120">Rechercher par ID de jeu de clés.</span><span class="sxs-lookup"><span data-stu-id="48c66-120">Search by key pack ID.</span></span>

</dd> <dt>

<span id="LSLICENSE_SEARCH_MACHINENAME"></span><span id="lslicense_search_machinename"></span>

<span data-ttu-id="48c66-121"><span id="LSLICENSE_SEARCH_MACHINENAME"></span><span id="lslicense_search_machinename"></span>**LSLICENSE \_ Rechercher \_ MachineName** (0x00000008)</span><span class="sxs-lookup"><span data-stu-id="48c66-121"><span id="LSLICENSE_SEARCH_MACHINENAME"></span><span id="lslicense_search_machinename"></span>**LSLICENSE\_SEARCH\_MACHINENAME** (0x00000008)</span></span>


</dt> <dd>

<span data-ttu-id="48c66-122">Rechercher par nom d’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="48c66-122">Search by machine name.</span></span>

</dd> <dt>

<span id="LSLICENSE_SEARCH_USERNAME"></span><span id="lslicense_search_username"></span>

<span data-ttu-id="48c66-123"><span id="LSLICENSE_SEARCH_USERNAME"></span><span id="lslicense_search_username"></span>**LSLICENSE \_ \_Nom d’utilisateur de recherche** (0x00000010)</span><span class="sxs-lookup"><span data-stu-id="48c66-123"><span id="LSLICENSE_SEARCH_USERNAME"></span><span id="lslicense_search_username"></span>**LSLICENSE\_SEARCH\_USERNAME** (0x00000010)</span></span>


</dt> <dd>

<span data-ttu-id="48c66-124">Rechercher par nom d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="48c66-124">Search by user name.</span></span>

</dd> <dt>

<span id="LSLICENSE_SEARCH_ISSUEDATE"></span><span id="lslicense_search_issuedate"></span>

<span data-ttu-id="48c66-125"><span id="LSLICENSE_SEARCH_ISSUEDATE"></span><span id="lslicense_search_issuedate"></span>**LSLICENSE \_ \_Publication** de la recherche (0x00000080)</span><span class="sxs-lookup"><span data-stu-id="48c66-125"><span id="LSLICENSE_SEARCH_ISSUEDATE"></span><span id="lslicense_search_issuedate"></span>**LSLICENSE\_SEARCH\_ISSUEDATE** (0x00000080)</span></span>


</dt> <dd>

<span data-ttu-id="48c66-126">Rechercher par date d’émission.</span><span class="sxs-lookup"><span data-stu-id="48c66-126">Search by issue date.</span></span>

</dd> <dt>

<span id="LSLICENSE_SEARCH_EXPIREDATE"></span><span id="lslicense_search_expiredate"></span>

<span data-ttu-id="48c66-127"><span id="LSLICENSE_SEARCH_EXPIREDATE"></span><span id="lslicense_search_expiredate"></span>**LSLICENSE \_ \_Expiration** de la recherche (0x00000100)</span><span class="sxs-lookup"><span data-stu-id="48c66-127"><span id="LSLICENSE_SEARCH_EXPIREDATE"></span><span id="lslicense_search_expiredate"></span>**LSLICENSE\_SEARCH\_EXPIREDATE** (0x00000100)</span></span>


</dt> <dd>

<span data-ttu-id="48c66-128">Rechercher par date d’expiration.</span><span class="sxs-lookup"><span data-stu-id="48c66-128">Search by expiration date.</span></span>

</dd> <dt>

<span id="LSLICENSE_SEARCH__NUMLICENSES"></span><span id="lslicense_search__numlicenses"></span>

<span data-ttu-id="48c66-129"><span id="LSLICENSE_SEARCH__NUMLICENSES"></span><span id="lslicense_search__numlicenses"></span>**LSLICENSE \_ Rechercher \_ NUMLICENSES** (0x00000200)</span><span class="sxs-lookup"><span data-stu-id="48c66-129"><span id="LSLICENSE_SEARCH__NUMLICENSES"></span><span id="lslicense_search__numlicenses"></span>**LSLICENSE\_SEARCH\_ NUMLICENSES** (0x00000200)</span></span>


</dt> <dd>

<span data-ttu-id="48c66-130">Recherche par nombre de licences.</span><span class="sxs-lookup"><span data-stu-id="48c66-130">Search by number of licenses.</span></span>

</dd> <dt>

<span id="LSLICENSE_SEARCH___ENTRY_STATUS"></span><span id="lslicense_search___entry_status"></span>

<span data-ttu-id="48c66-131"><span id="LSLICENSE_SEARCH___ENTRY_STATUS"></span><span id="lslicense_search___entry_status"></span>**LSLICENSE \_ \_ \_ État** de l’entrée de recherche (0x20000000)</span><span class="sxs-lookup"><span data-stu-id="48c66-131"><span id="LSLICENSE_SEARCH___ENTRY_STATUS"></span><span id="lslicense_search___entry_status"></span>**LSLICENSE\_SEARCH\_ ENTRY\_STATUS** (0x20000000)</span></span>


</dt> <dd>

<span data-ttu-id="48c66-132">Rechercher par État de l’entrée.</span><span class="sxs-lookup"><span data-stu-id="48c66-132">Search by entry status.</span></span>

</dd> <dt>

<span id="LSLICENSE_EXSEARCH_LICENSESTATUS"></span><span id="lslicense_exsearch_licensestatus"></span>

<span data-ttu-id="48c66-133"><span id="LSLICENSE_EXSEARCH_LICENSESTATUS"></span><span id="lslicense_exsearch_licensestatus"></span>**LSLICENSE \_ Exsearch \_ LICENSESTATUS** (0x00100000)</span><span class="sxs-lookup"><span data-stu-id="48c66-133"><span id="LSLICENSE_EXSEARCH_LICENSESTATUS"></span><span id="lslicense_exsearch_licensestatus"></span>**LSLICENSE\_EXSEARCH\_LICENSESTATUS** (0x00100000)</span></span>


</dt> <dd>

<span data-ttu-id="48c66-134">Rechercher par État de licence.</span><span class="sxs-lookup"><span data-stu-id="48c66-134">Search by license status.</span></span>

</dd> <dt>

<span id="LSKEYPACK_SEARCH_ALL"></span><span id="lskeypack_search_all"></span>

<span data-ttu-id="48c66-135"><span id="LSKEYPACK_SEARCH_ALL"></span><span id="lskeypack_search_all"></span>**LSKEYPACK \_ Rechercher \_ tout** (0xFFFFFFFF)</span><span class="sxs-lookup"><span data-stu-id="48c66-135"><span id="LSKEYPACK_SEARCH_ALL"></span><span id="lskeypack_search_all"></span>**LSKEYPACK\_SEARCH\_ALL** (0xFFFFFFFF)</span></span>


</dt> <dd>

<span data-ttu-id="48c66-136">Recherchez toutes les licences.</span><span class="sxs-lookup"><span data-stu-id="48c66-136">Search all licenses.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="48c66-137">*bMatchAll* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="48c66-137">*bMatchAll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48c66-138">Spécifie si toutes les valeurs de recherche doivent être mises en correspondance.</span><span class="sxs-lookup"><span data-stu-id="48c66-138">Specifies whether to match all search values.</span></span>

</dd> <dt>

<span data-ttu-id="48c66-139">*lpSearchParm* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="48c66-139">*lpSearchParm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="48c66-140">Pointeur vers une structure [**LSLicense**](lslicense.md) qui spécifie les paramètres de recherche à rechercher.</span><span class="sxs-lookup"><span data-stu-id="48c66-140">Pointer to a [**LSLicense**](lslicense.md) structure that specifies the search parameters to look for.</span></span>

</dd> <dt>

<span data-ttu-id="48c66-141">*pdwErrCode* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="48c66-141">*pdwErrCode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="48c66-142">Pointeur vers une variable qui reçoit l’un des codes d’erreur suivants au retour.</span><span class="sxs-lookup"><span data-stu-id="48c66-142">Pointer to a variable that receives one of the following error codes on return.</span></span>

<dt>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>

<span data-ttu-id="48c66-143"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**Lserver \_ \_Réussite S** (0)</span><span class="sxs-lookup"><span data-stu-id="48c66-143"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER\_S\_SUCCESS** (0)</span></span>


</dt> <dd>

<span data-ttu-id="48c66-144">L’appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="48c66-144">Call is successful.</span></span>

</dd> <dt>

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>

<span data-ttu-id="48c66-145"><span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**Lserver \_ \_ \_ Erreur interne E** (5001)</span><span class="sxs-lookup"><span data-stu-id="48c66-145"><span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**LSERVER\_E\_INTERNAL\_ERROR** (5001)</span></span>


</dt> <dd>

<span data-ttu-id="48c66-146">Erreur interne dans le serveur de licences.</span><span class="sxs-lookup"><span data-stu-id="48c66-146">Internal error in license server.</span></span>

</dd> <dt>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>

<span data-ttu-id="48c66-147"><span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**Lserver \_ \_ \_ Séquence E non valide** (5006)</span><span class="sxs-lookup"><span data-stu-id="48c66-147"><span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**LSERVER\_E\_INVALID\_SEQUENCE** (5006)</span></span>


</dt> <dd>

<span data-ttu-id="48c66-148">La séquence d’appel n’était pas valide.</span><span class="sxs-lookup"><span data-stu-id="48c66-148">The calling sequence was not valid.</span></span> <span data-ttu-id="48c66-149">Probablement, une énumération précédente ne s’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="48c66-149">Most likely, a previous enumeration has not ended.</span></span>

</dd> <dt>

<span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>

<span data-ttu-id="48c66-150"><span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**Lserver \_ E \_ serveur \_ occupé** (5007)</span><span class="sxs-lookup"><span data-stu-id="48c66-150"><span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**LSERVER\_E\_SERVER\_BUSY** (5007)</span></span>


</dt> <dd>

<span data-ttu-id="48c66-151">Le serveur de licences est trop occupé pour traiter la demande.</span><span class="sxs-lookup"><span data-stu-id="48c66-151">License server is too busy to process the request.</span></span>

</dd> <dt>

<span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>

<span data-ttu-id="48c66-152"><span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**Lserver \_ E \_ OUTOFMEMORY** (5008)</span><span class="sxs-lookup"><span data-stu-id="48c66-152"><span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**LSERVER\_E\_OUTOFMEMORY** (5008)</span></span>


</dt> <dd>

<span data-ttu-id="48c66-153">Impossible de traiter la requête en raison d’une mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="48c66-153">Cannot process the request because of insufficient memory.</span></span>

</dd> <dt>

<span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>

<span data-ttu-id="48c66-154"><span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>**Lserver \_ E \_ \_ données non valides** (5009)</span><span class="sxs-lookup"><span data-stu-id="48c66-154"><span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>**LSERVER\_E\_INVALID\_DATA** (5009)</span></span>


</dt> <dd>

<span data-ttu-id="48c66-155">Les données du paramètre de recherche ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="48c66-155">Data in the search parameter is not valid.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="48c66-156">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="48c66-156">Return value</span></span>

<span data-ttu-id="48c66-157">Cette fonction retourne les valeurs de retour possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="48c66-157">This function returns the following possible return values.</span></span>

<dl> <dt>

<span data-ttu-id="48c66-158">**RPC \_ S \_ OK**</span><span class="sxs-lookup"><span data-stu-id="48c66-158">**RPC\_S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="48c66-159">L’appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="48c66-159">The call succeeded.</span></span> <span data-ttu-id="48c66-160">Vérifiez la valeur du paramètre *pdwErrCode* pour obtenir le code de retour de l’appel.</span><span class="sxs-lookup"><span data-stu-id="48c66-160">Check the value of the *pdwErrCode* parameter to get the return code for the call.</span></span>

</dd> <dt>

<span data-ttu-id="48c66-161">**\_argument RPC \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="48c66-161">**RPC\_S\_INVALID\_ARG**</span></span>
</dt> <dd>

<span data-ttu-id="48c66-162">L’argument n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="48c66-162">The argument was not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="48c66-163">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="48c66-163">Requirements</span></span>



| <span data-ttu-id="48c66-164">Condition requise</span><span class="sxs-lookup"><span data-stu-id="48c66-164">Requirement</span></span> | <span data-ttu-id="48c66-165">Valeur</span><span class="sxs-lookup"><span data-stu-id="48c66-165">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="48c66-166">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="48c66-166">Minimum supported client</span></span><br/> | <span data-ttu-id="48c66-167">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="48c66-167">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="48c66-168">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="48c66-168">Minimum supported server</span></span><br/> | <span data-ttu-id="48c66-169">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="48c66-169">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="48c66-170">DLL</span><span class="sxs-lookup"><span data-stu-id="48c66-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48c66-171"><dt>Mstlsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48c66-171"><dt>Mstlsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48c66-172">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="48c66-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48c66-173">**LSLicense**</span><span class="sxs-lookup"><span data-stu-id="48c66-173">**LSLicense**</span></span>](lslicense.md)
</dt> <dt>

[<span data-ttu-id="48c66-174">**TLSConnectToLsServer**</span><span class="sxs-lookup"><span data-stu-id="48c66-174">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> <dt>

[<span data-ttu-id="48c66-175">**TLSLicenseEnumNext**</span><span class="sxs-lookup"><span data-stu-id="48c66-175">**TLSLicenseEnumNext**</span></span>](tlslicenseenumnext.md)
</dt> <dt>

[<span data-ttu-id="48c66-176">**TLSLicenseEnumEnd**</span><span class="sxs-lookup"><span data-stu-id="48c66-176">**TLSLicenseEnumEnd**</span></span>](tlslicenseenumend.md)
</dt> </dl>

 

