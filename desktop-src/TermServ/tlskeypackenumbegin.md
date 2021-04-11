---
title: TLSKeyPackEnumBegin fonction)
description: Commence l’énumération par le biais de tous les jeux de clés installés sur un serveur de licences Bureau à distance en fonction des critères de recherche.
ms.assetid: 2d847fe4-66ab-42df-8213-651e14257590
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la fonction TLSKeyPackEnumBegin
topic_type:
- apiref
api_name:
- TLSKeyPackEnumBegin
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: db8f61197e3c08f5608be954a9288ea54cad5586
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317478"
---
# <a name="tlskeypackenumbegin-function"></a><span data-ttu-id="bcc92-104">TLSKeyPackEnumBegin fonction)</span><span class="sxs-lookup"><span data-stu-id="bcc92-104">TLSKeyPackEnumBegin function</span></span>

<span data-ttu-id="bcc92-105">Commence l’énumération par le biais de tous les jeux de clés installés sur un serveur de licences Bureau à distance en fonction des critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="bcc92-105">Begins enumeration through all key packs that are installed on a Remote Desktop license server based on search criteria.</span></span>

> [!Note]  
> <span data-ttu-id="bcc92-106">Cette fonction n’a aucun fichier d’en-tête ou bibliothèque d’importation associé.</span><span class="sxs-lookup"><span data-stu-id="bcc92-106">This function has no associated header file or import library.</span></span> <span data-ttu-id="bcc92-107">Pour appeler cette fonction, vous devez créer un fichier d’en-tête défini par l’utilisateur et utiliser les fonctions [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Mstlsapi.dll.</span><span class="sxs-lookup"><span data-stu-id="bcc92-107">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mstlsapi.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="bcc92-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bcc92-108">Syntax</span></span>


```C++
DWORD WINAPI TLSKeyPackEnumBegin(
  _In_  TLS_HANDLE hHandle,
  _In_  DWORD      dwSearchParm,
  _In_  BOOL       bMatchAll,
  _In_  LSKeyPack  *lpSearchParm,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a><span data-ttu-id="bcc92-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bcc92-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcc92-110">*hHandle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bcc92-110">*hHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcc92-111">Handle vers un serveur de licences Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="bcc92-111">Handle to a Remote Desktop license server.</span></span> <span data-ttu-id="bcc92-112">Spécifiez un descripteur ouvert par la fonction [**TLSConnectToLsServer**](tlsconnecttolsserver.md) .</span><span class="sxs-lookup"><span data-stu-id="bcc92-112">Specify a handle that is opened by the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="bcc92-113">*dwSearchParm* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bcc92-113">*dwSearchParm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcc92-114">Spécifie les critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="bcc92-114">Specifies the search criteria.</span></span> <span data-ttu-id="bcc92-115">Ce paramètre est réservé pour une utilisation ultérieure et doit contenir 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="bcc92-115">This parameter is reserved for future use and must contain 0xFFFFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="bcc92-116">*bMatchAll* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bcc92-116">*bMatchAll* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcc92-117">Spécifie si toutes les valeurs de recherche doivent être mises en correspondance.</span><span class="sxs-lookup"><span data-stu-id="bcc92-117">Specifies whether to match all search values.</span></span>

</dd> <dt>

<span data-ttu-id="bcc92-118">*lpSearchParm* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bcc92-118">*lpSearchParm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcc92-119">Pointeur vers une structure [**LSKeyPack**](lskeypack.md) qui spécifie les paramètres de recherche à rechercher.</span><span class="sxs-lookup"><span data-stu-id="bcc92-119">Pointer to a [**LSKeyPack**](lskeypack.md) structure that specifies the search parameters to look for.</span></span>

</dd> <dt>

<span data-ttu-id="bcc92-120">*pdwErrCode* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="bcc92-120">*pdwErrCode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bcc92-121">Pointeur vers une variable qui reçoit l’un des codes d’erreur suivants au retour.</span><span class="sxs-lookup"><span data-stu-id="bcc92-121">Pointer to a variable that receives one of the following error codes on return.</span></span>

<dt>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>

<span data-ttu-id="bcc92-122"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**Lserver \_ \_Réussite S** (0)</span><span class="sxs-lookup"><span data-stu-id="bcc92-122"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER\_S\_SUCCESS** (0)</span></span>


</dt> <dd>

<span data-ttu-id="bcc92-123">L’appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="bcc92-123">Call is successful.</span></span>

</dd> <dt>

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>

<span data-ttu-id="bcc92-124"><span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**Lserver \_ \_ \_ Erreur interne E** (5001)</span><span class="sxs-lookup"><span data-stu-id="bcc92-124"><span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**LSERVER\_E\_INTERNAL\_ERROR** (5001)</span></span>


</dt> <dd>

<span data-ttu-id="bcc92-125">Erreur interne dans le serveur de licences.</span><span class="sxs-lookup"><span data-stu-id="bcc92-125">Internal error in license server.</span></span>

</dd> <dt>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>

<span data-ttu-id="bcc92-126"><span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**Lserver \_ \_ \_ Séquence E non valide** (5006)</span><span class="sxs-lookup"><span data-stu-id="bcc92-126"><span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**LSERVER\_E\_INVALID\_SEQUENCE** (5006)</span></span>


</dt> <dd>

<span data-ttu-id="bcc92-127">La séquence d’appel n’était pas valide.</span><span class="sxs-lookup"><span data-stu-id="bcc92-127">The calling sequence was not valid.</span></span> <span data-ttu-id="bcc92-128">Probablement, une énumération précédente ne s’est pas terminée.</span><span class="sxs-lookup"><span data-stu-id="bcc92-128">Most likely, a previous enumeration has not ended.</span></span>

</dd> <dt>

<span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>

<span data-ttu-id="bcc92-129"><span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**Lserver \_ E \_ serveur \_ occupé** (5007)</span><span class="sxs-lookup"><span data-stu-id="bcc92-129"><span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**LSERVER\_E\_SERVER\_BUSY** (5007)</span></span>


</dt> <dd>

<span data-ttu-id="bcc92-130">Le serveur de licences est trop occupé pour traiter la demande.</span><span class="sxs-lookup"><span data-stu-id="bcc92-130">License server is too busy to process the request.</span></span>

</dd> <dt>

<span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>

<span data-ttu-id="bcc92-131"><span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**Lserver \_ E \_ OUTOFMEMORY** (5008)</span><span class="sxs-lookup"><span data-stu-id="bcc92-131"><span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**LSERVER\_E\_OUTOFMEMORY** (5008)</span></span>


</dt> <dd>

<span data-ttu-id="bcc92-132">Impossible de traiter la requête en raison d’une mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="bcc92-132">Cannot process the request because of insufficient memory.</span></span>

</dd> <dt>

<span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>

<span data-ttu-id="bcc92-133"><span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>**Lserver \_ E \_ \_ données non valides** (5009)</span><span class="sxs-lookup"><span data-stu-id="bcc92-133"><span id="LSERVER_E_INVALID_DATA"></span><span id="lserver_e_invalid_data"></span>**LSERVER\_E\_INVALID\_DATA** (5009)</span></span>


</dt> <dd>

<span data-ttu-id="bcc92-134">Les données du paramètre de recherche ne sont pas valides.</span><span class="sxs-lookup"><span data-stu-id="bcc92-134">Data in the search parameter is not valid.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bcc92-135">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bcc92-135">Return value</span></span>

<span data-ttu-id="bcc92-136">Cette fonction retourne les valeurs de retour possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="bcc92-136">This function returns the following possible return values.</span></span>

<dl> <dt>

<span data-ttu-id="bcc92-137">**RPC \_ S \_ OK**</span><span class="sxs-lookup"><span data-stu-id="bcc92-137">**RPC\_S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="bcc92-138">L’appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="bcc92-138">The call succeeded.</span></span> <span data-ttu-id="bcc92-139">Vérifiez la valeur du paramètre *pdwErrCode* pour obtenir le code de retour de l’appel.</span><span class="sxs-lookup"><span data-stu-id="bcc92-139">Check the value of the *pdwErrCode* parameter to get the return code for the call.</span></span>

</dd> <dt>

<span data-ttu-id="bcc92-140">**\_argument RPC \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="bcc92-140">**RPC\_S\_INVALID\_ARG**</span></span>
</dt> <dd>

<span data-ttu-id="bcc92-141">L’argument n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="bcc92-141">The argument was not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="bcc92-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bcc92-142">Requirements</span></span>



| <span data-ttu-id="bcc92-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bcc92-143">Requirement</span></span> | <span data-ttu-id="bcc92-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="bcc92-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="bcc92-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bcc92-145">Minimum supported client</span></span><br/> | <span data-ttu-id="bcc92-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bcc92-146">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="bcc92-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bcc92-147">Minimum supported server</span></span><br/> | <span data-ttu-id="bcc92-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bcc92-148">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="bcc92-149">DLL</span><span class="sxs-lookup"><span data-stu-id="bcc92-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bcc92-150"><dt>Mstlsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bcc92-150"><dt>Mstlsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bcc92-151">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="bcc92-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcc92-152">**LSKeyPack**</span><span class="sxs-lookup"><span data-stu-id="bcc92-152">**LSKeyPack**</span></span>](lskeypack.md)
</dt> <dt>

[<span data-ttu-id="bcc92-153">**TLSConnectToLsServer**</span><span class="sxs-lookup"><span data-stu-id="bcc92-153">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> <dt>

[<span data-ttu-id="bcc92-154">**TLSKeyPackEnumNext**</span><span class="sxs-lookup"><span data-stu-id="bcc92-154">**TLSKeyPackEnumNext**</span></span>](tlskeypackenumnext.md)
</dt> <dt>

[<span data-ttu-id="bcc92-155">**TLSKeyPackEnumEnd**</span><span class="sxs-lookup"><span data-stu-id="bcc92-155">**TLSKeyPackEnumEnd**</span></span>](tlskeypackenumend.md)
</dt> </dl>

 

