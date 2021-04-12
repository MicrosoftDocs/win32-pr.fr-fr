---
title: TLSKeyPackEnumNext fonction)
description: Continue à partir d’un appel précédent à la fonction TLSKeyPackEnumBegin et retourne le prochain Pack de clés installé sur un serveur de licences Bureau à distance qui correspond aux critères de recherche.
ms.assetid: 2614eb7a-df57-42a6-ad34-0a3211a6b8c3
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la fonction TLSKeyPackEnumNext
topic_type:
- apiref
api_name:
- TLSKeyPackEnumNext
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 897874f333ed7933ea1616f7f5ba5f1686736d0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032454"
---
# <a name="tlskeypackenumnext-function"></a><span data-ttu-id="d7d96-104">TLSKeyPackEnumNext fonction)</span><span class="sxs-lookup"><span data-stu-id="d7d96-104">TLSKeyPackEnumNext function</span></span>

<span data-ttu-id="d7d96-105">Continue à partir d’un appel précédent à la fonction [**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) et retourne le prochain Pack de clés installé sur un serveur de licences bureau à distance qui correspond aux critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="d7d96-105">Continues from a previous call to the [**TLSKeyPackEnumBegin**](tlskeypackenumbegin.md) function and returns the next key pack that is installed on a Remote Desktop license server that matches the search criteria.</span></span>

> [!Note]  
> <span data-ttu-id="d7d96-106">Cette fonction n’a aucun fichier d’en-tête ou bibliothèque d’importation associé.</span><span class="sxs-lookup"><span data-stu-id="d7d96-106">This function has no associated header file or import library.</span></span> <span data-ttu-id="d7d96-107">Pour appeler cette fonction, vous devez créer un fichier d’en-tête défini par l’utilisateur et utiliser les fonctions [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Mstlsapi.dll.</span><span class="sxs-lookup"><span data-stu-id="d7d96-107">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mstlsapi.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="d7d96-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d7d96-108">Syntax</span></span>


```C++
DWORD WINAPI TLSKeyPackEnumNext(
  _In_  TLS_HANDLE hHandle,
  _In_  LsKeyPack  *lpKeyPack,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a><span data-ttu-id="d7d96-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d7d96-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7d96-110">*hHandle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d7d96-110">*hHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7d96-111">Handle vers un serveur de licences Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="d7d96-111">Handle to a Remote Desktop license server.</span></span> <span data-ttu-id="d7d96-112">Spécifiez un descripteur ouvert par la fonction [**TLSConnectToLsServer**](tlsconnecttolsserver.md) .</span><span class="sxs-lookup"><span data-stu-id="d7d96-112">Specify a handle that is opened by the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="d7d96-113">*lpKeyPack* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d7d96-113">*lpKeyPack* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7d96-114">Pointeur vers une structure [**LSKeyPack**](lskeypack.md) qui reçoit le prochain Pack de clés qui correspond aux critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="d7d96-114">Pointer to a [**LSKeyPack**](lskeypack.md) structure that receives the next key pack that matches the search criteria.</span></span>

</dd> <dt>

<span data-ttu-id="d7d96-115">*pdwErrCode* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d7d96-115">*pdwErrCode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d7d96-116">Pointeur vers une variable qui reçoit l’un des codes d’erreur suivants au retour.</span><span class="sxs-lookup"><span data-stu-id="d7d96-116">Pointer to a variable that receives one of the following error codes on return.</span></span>

<dt>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>

<span data-ttu-id="d7d96-117"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**Lserver \_ \_Réussite S** (0)</span><span class="sxs-lookup"><span data-stu-id="d7d96-117"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER\_S\_SUCCESS** (0)</span></span>


</dt> <dd>

<span data-ttu-id="d7d96-118">L’appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="d7d96-118">Call is successful.</span></span>

</dd> <dt>

<span id="LSERVER_I_NO_MORE_DATA"></span><span id="lserver_i_no_more_data"></span>

<span data-ttu-id="d7d96-119"><span id="LSERVER_I_NO_MORE_DATA"></span><span id="lserver_i_no_more_data"></span>**Lserver \_ Je \_ n’ai \_ plus de \_ données** (4001)</span><span class="sxs-lookup"><span data-stu-id="d7d96-119"><span id="LSERVER_I_NO_MORE_DATA"></span><span id="lserver_i_no_more_data"></span>**LSERVER\_I\_NO\_MORE\_DATA** (4001)</span></span>


</dt> <dd>

<span data-ttu-id="d7d96-120">Aucun autre pack de clés ne correspond aux critères de recherche.</span><span class="sxs-lookup"><span data-stu-id="d7d96-120">No more key packs match the search criteria.</span></span>

</dd> <dt>

<span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>

<span data-ttu-id="d7d96-121"><span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**Lserver \_ \_ \_ Erreur interne E** (5001)</span><span class="sxs-lookup"><span data-stu-id="d7d96-121"><span id="LSERVER_E_INTERNAL_ERROR"></span><span id="lserver_e_internal_error"></span>**LSERVER\_E\_INTERNAL\_ERROR** (5001)</span></span>


</dt> <dd>

<span data-ttu-id="d7d96-122">Erreur interne dans le serveur de licences.</span><span class="sxs-lookup"><span data-stu-id="d7d96-122">Internal error in license server.</span></span>

</dd> <dt>

<span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>

<span data-ttu-id="d7d96-123"><span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**Lserver \_ \_ \_ Séquence E non valide** (5006)</span><span class="sxs-lookup"><span data-stu-id="d7d96-123"><span id="LSERVER_E_INVALID_SEQUENCE"></span><span id="lserver_e_invalid_sequence"></span>**LSERVER\_E\_INVALID\_SEQUENCE** (5006)</span></span>


</dt> <dd>

<span data-ttu-id="d7d96-124">La séquence d’appel n’était pas valide.</span><span class="sxs-lookup"><span data-stu-id="d7d96-124">The calling sequence was not valid.</span></span> <span data-ttu-id="d7d96-125">Vous devez appeler la fonction [**TLSKeyPackEnumBegin ()**](tlskeypackenumbegin.md) avant cela.</span><span class="sxs-lookup"><span data-stu-id="d7d96-125">Must call the [**TLSKeyPackEnumBegin()**](tlskeypackenumbegin.md) function before this.</span></span>

</dd> <dt>

<span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>

<span data-ttu-id="d7d96-126"><span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**Lserver \_ E \_ serveur \_ occupé** (5007)</span><span class="sxs-lookup"><span data-stu-id="d7d96-126"><span id="LSERVER_E_SERVER_BUSY"></span><span id="lserver_e_server_busy"></span>**LSERVER\_E\_SERVER\_BUSY** (5007)</span></span>


</dt> <dd>

<span data-ttu-id="d7d96-127">Le serveur de licences est trop occupé pour traiter la demande.</span><span class="sxs-lookup"><span data-stu-id="d7d96-127">License server is too busy to process the request.</span></span>

</dd> <dt>

<span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>

<span data-ttu-id="d7d96-128"><span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**Lserver \_ E \_ OUTOFMEMORY** (5008)</span><span class="sxs-lookup"><span data-stu-id="d7d96-128"><span id="LSERVER_E_OUTOFMEMORY"></span><span id="lserver_e_outofmemory"></span>**LSERVER\_E\_OUTOFMEMORY** (5008)</span></span>


</dt> <dd>

<span data-ttu-id="d7d96-129">Impossible de traiter la requête en raison d’une mémoire insuffisante.</span><span class="sxs-lookup"><span data-stu-id="d7d96-129">Cannot process the request because of insufficient memory.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7d96-130">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d7d96-130">Return value</span></span>

<span data-ttu-id="d7d96-131">Cette fonction retourne les valeurs de retour possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="d7d96-131">This function returns the following possible return values.</span></span>

<dl> <dt>

<span data-ttu-id="d7d96-132">**RPC \_ S \_ OK**</span><span class="sxs-lookup"><span data-stu-id="d7d96-132">**RPC\_S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="d7d96-133">L’appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="d7d96-133">The call succeeded.</span></span> <span data-ttu-id="d7d96-134">Vérifiez la valeur du paramètre *pdwErrCode* pour obtenir le code de retour de l’appel.</span><span class="sxs-lookup"><span data-stu-id="d7d96-134">Check the value of the *pdwErrCode* parameter to get the return code for the call.</span></span>

</dd> <dt>

<span data-ttu-id="d7d96-135">**\_argument RPC \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="d7d96-135">**RPC\_S\_INVALID\_ARG**</span></span>
</dt> <dd>

<span data-ttu-id="d7d96-136">L’argument n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="d7d96-136">The argument was not valid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d7d96-137">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d7d96-137">Requirements</span></span>



| <span data-ttu-id="d7d96-138">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d7d96-138">Requirement</span></span> | <span data-ttu-id="d7d96-139">Valeur</span><span class="sxs-lookup"><span data-stu-id="d7d96-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d7d96-140">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7d96-140">Minimum supported client</span></span><br/> | <span data-ttu-id="d7d96-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d7d96-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d7d96-142">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d7d96-142">Minimum supported server</span></span><br/> | <span data-ttu-id="d7d96-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d7d96-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d7d96-144">DLL</span><span class="sxs-lookup"><span data-stu-id="d7d96-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7d96-145"><dt>Mstlsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7d96-145"><dt>Mstlsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7d96-146">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d7d96-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7d96-147">**LSKeyPack**</span><span class="sxs-lookup"><span data-stu-id="d7d96-147">**LSKeyPack**</span></span>](lskeypack.md)
</dt> <dt>

[<span data-ttu-id="d7d96-148">**TLSConnectToLsServer**</span><span class="sxs-lookup"><span data-stu-id="d7d96-148">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> <dt>

[<span data-ttu-id="d7d96-149">**TLSKeyPackEnumBegin**</span><span class="sxs-lookup"><span data-stu-id="d7d96-149">**TLSKeyPackEnumBegin**</span></span>](tlskeypackenumbegin.md)
</dt> <dt>

[<span data-ttu-id="d7d96-150">**TLSKeyPackEnumEnd**</span><span class="sxs-lookup"><span data-stu-id="d7d96-150">**TLSKeyPackEnumEnd**</span></span>](tlskeypackenumend.md)
</dt> </dl>

 

