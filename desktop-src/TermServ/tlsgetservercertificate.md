---
title: TLSGetServerCertificate fonction)
description: Retourne le certificat du serveur de licences Bureau à distance.
ms.assetid: 7a31e7f9-f6d6-4030-b7db-43be118bb158
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la fonction TLSGetServerCertificate
topic_type:
- apiref
api_name:
- TLSGetServerCertificate
api_location:
- Mstlsapi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3144245863ee4a4316bbce8333f03ca3901cb499
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511749"
---
# <a name="tlsgetservercertificate-function"></a><span data-ttu-id="0142c-104">TLSGetServerCertificate fonction)</span><span class="sxs-lookup"><span data-stu-id="0142c-104">TLSGetServerCertificate function</span></span>

<span data-ttu-id="0142c-105">Retourne le certificat du serveur de licences Bureau à distance.</span><span class="sxs-lookup"><span data-stu-id="0142c-105">Returns the certificate of the Remote Desktop license server.</span></span>

> [!Note]  
> <span data-ttu-id="0142c-106">Cette fonction n’a aucun fichier d’en-tête ou bibliothèque d’importation associé.</span><span class="sxs-lookup"><span data-stu-id="0142c-106">This function has no associated header file or import library.</span></span> <span data-ttu-id="0142c-107">Pour appeler cette fonction, vous devez créer un fichier d’en-tête défini par l’utilisateur et utiliser les fonctions [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) et [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) pour établir une liaison dynamique à Mstlsapi.dll.</span><span class="sxs-lookup"><span data-stu-id="0142c-107">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mstlsapi.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="0142c-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0142c-108">Syntax</span></span>


```C++
DWORD WINAPI TLSGetServerCertificate(
  _In_  TLS_HANDLE hHandle,
  _In_  BOOL       bSignCert,
  _Out_ LPBYTE     *ppbCertBlob,
  _Out_ LPDWORD    lpdwCertBlobLen,
  _Out_ PDWORD     pdwErrCode
);
```



## <a name="parameters"></a><span data-ttu-id="0142c-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0142c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0142c-110">*hHandle* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0142c-110">*hHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0142c-111">Handle vers un serveur de licences Bureau à distance qui est ouvert par un appel à la fonction [**TLSConnectToLsServer**](tlsconnecttolsserver.md) .</span><span class="sxs-lookup"><span data-stu-id="0142c-111">Handle to a Remote Desktop license server that is opened by a call to the [**TLSConnectToLsServer**](tlsconnecttolsserver.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="0142c-112">*bSignCert* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0142c-112">*bSignCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0142c-113">**True** si le certificat de signature est **false** dans le cas d’un certificat Exchange.</span><span class="sxs-lookup"><span data-stu-id="0142c-113">**TRUE** if signature certificate, **FALSE** if exchange certificate.</span></span>

</dd> <dt>

<span data-ttu-id="0142c-114">*ppbCertBlob* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0142c-114">*ppbCertBlob* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0142c-115">Pointeur vers une variable qui reçoit un pointeur vers une mémoire tampon qui contient le certificat.</span><span class="sxs-lookup"><span data-stu-id="0142c-115">Pointer to a variable that receives a pointer to a buffer that contains the certificate.</span></span>

</dd> <dt>

<span data-ttu-id="0142c-116">*lpdwCertBlobLen* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0142c-116">*lpdwCertBlobLen* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0142c-117">Pointeur vers une variable qui reçoit la taille du certificat retourné.</span><span class="sxs-lookup"><span data-stu-id="0142c-117">Pointer to a variable that receives the size of the certificate that is returned.</span></span>

</dd> <dt>

<span data-ttu-id="0142c-118">*pdwErrCode* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0142c-118">*pdwErrCode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0142c-119">Pointeur vers une variable qui reçoit le code d’erreur.</span><span class="sxs-lookup"><span data-stu-id="0142c-119">Pointer to a variable that receives the error code.</span></span>

<dt>

<span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>

<span data-ttu-id="0142c-120"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**Lserver \_ \_Réussite S** (0)</span><span class="sxs-lookup"><span data-stu-id="0142c-120"><span id="LSERVER_S_SUCCESS"></span><span id="lserver_s_success"></span>**LSERVER\_S\_SUCCESS** (0)</span></span>


</dt> <dd>

<span data-ttu-id="0142c-121">L’appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="0142c-121">Call is successful.</span></span>

</dd> <dt>

<span id="TLS_W_SELFSIGN_CERTIFICATE"></span><span id="tls_w_selfsign_certificate"></span>

<span data-ttu-id="0142c-122"><span id="TLS_W_SELFSIGN_CERTIFICATE"></span><span id="tls_w_selfsign_certificate"></span>Protocole **TLS \_ \_SELFSIGN \_ certificat W** (4007)</span><span class="sxs-lookup"><span data-stu-id="0142c-122"><span id="TLS_W_SELFSIGN_CERTIFICATE"></span><span id="tls_w_selfsign_certificate"></span>**TLS\_W\_SELFSIGN\_CERTIFICATE** (4007)</span></span>


</dt> <dd>

<span data-ttu-id="0142c-123">Le certificat retourné est un certificat auto-signé.</span><span class="sxs-lookup"><span data-stu-id="0142c-123">Certificate returned is a self-signed certificate.</span></span>

</dd> <dt>

<span id="TLS_W_TEMP_SELFSIGN_CERT"></span><span id="tls_w_temp_selfsign_cert"></span>

<span data-ttu-id="0142c-124"><span id="TLS_W_TEMP_SELFSIGN_CERT"></span><span id="tls_w_temp_selfsign_cert"></span>Protocole **TLS \_ \_Certificat Temp \_ SELFSIGN \_** (4009)</span><span class="sxs-lookup"><span data-stu-id="0142c-124"><span id="TLS_W_TEMP_SELFSIGN_CERT"></span><span id="tls_w_temp_selfsign_cert"></span>**TLS\_W\_TEMP\_SELFSIGN\_CERT** (4009)</span></span>


</dt> <dd>

<span data-ttu-id="0142c-125">Le certificat retourné est temporaire.</span><span class="sxs-lookup"><span data-stu-id="0142c-125">Certificate returned is temporary.</span></span>

</dd> <dt>

<span id="TLS_E_ACCESS_DENIED"></span><span id="tls_e_access_denied"></span>

<span data-ttu-id="0142c-126"><span id="TLS_E_ACCESS_DENIED"></span><span id="tls_e_access_denied"></span>Protocole **TLS \_ \_Accès E \_ refusé** (5003)</span><span class="sxs-lookup"><span data-stu-id="0142c-126"><span id="TLS_E_ACCESS_DENIED"></span><span id="tls_e_access_denied"></span>**TLS\_E\_ACCESS\_DENIED** (5003)</span></span>


</dt> <dd>

<span data-ttu-id="0142c-127">Accès refusé.</span><span class="sxs-lookup"><span data-stu-id="0142c-127">Access denied.</span></span>

</dd> <dt>

<span id="TLS_E_ALLOCATE_HANDLE"></span><span id="tls_e_allocate_handle"></span>

<span data-ttu-id="0142c-128"><span id="TLS_E_ALLOCATE_HANDLE"></span><span id="tls_e_allocate_handle"></span>Protocole **TLS \_ E \_ allouer un \_ descripteur** (5007)</span><span class="sxs-lookup"><span data-stu-id="0142c-128"><span id="TLS_E_ALLOCATE_HANDLE"></span><span id="tls_e_allocate_handle"></span>**TLS\_E\_ALLOCATE\_HANDLE** (5007)</span></span>


</dt> <dd>

<span data-ttu-id="0142c-129">Le serveur est trop occupé pour traiter la demande.</span><span class="sxs-lookup"><span data-stu-id="0142c-129">Server is too busy to process the request.</span></span>

</dd> <dt>

<span id="TLS_E_NO_CERTIFICATE"></span><span id="tls_e_no_certificate"></span>

<span data-ttu-id="0142c-130"><span id="TLS_E_NO_CERTIFICATE"></span><span id="tls_e_no_certificate"></span>Protocole **TLS \_ E \_ aucun \_ certificat** (5022)</span><span class="sxs-lookup"><span data-stu-id="0142c-130"><span id="TLS_E_NO_CERTIFICATE"></span><span id="tls_e_no_certificate"></span>**TLS\_E\_NO\_CERTIFICATE** (5022)</span></span>


</dt> <dd>

<span data-ttu-id="0142c-131">Impossible de récupérer un certificat.</span><span class="sxs-lookup"><span data-stu-id="0142c-131">Cannot retrieve a certificate.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0142c-132">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0142c-132">Return value</span></span>

<span data-ttu-id="0142c-133">Cette fonction retourne les valeurs de retour possibles suivantes.</span><span class="sxs-lookup"><span data-stu-id="0142c-133">This function returns the following possible return values.</span></span>

<dl> <dt>

<span data-ttu-id="0142c-134">**RPC \_ S \_ OK**</span><span class="sxs-lookup"><span data-stu-id="0142c-134">**RPC\_S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="0142c-135">L’appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="0142c-135">The call succeeded.</span></span> <span data-ttu-id="0142c-136">Vérifiez la valeur du paramètre *pdwErrCode* pour obtenir le code de retour de l’appel.</span><span class="sxs-lookup"><span data-stu-id="0142c-136">Check the value of the *pdwErrCode* parameter to get the return code for the call.</span></span>

</dd> <dt>

<span data-ttu-id="0142c-137">**\_argument RPC \_ non valide \_**</span><span class="sxs-lookup"><span data-stu-id="0142c-137">**RPC\_S\_INVALID\_ARG**</span></span>
</dt> <dd>

<span data-ttu-id="0142c-138">L'argument n'était pas valide.</span><span class="sxs-lookup"><span data-stu-id="0142c-138">The argument was invalid.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0142c-139">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0142c-139">Requirements</span></span>



| <span data-ttu-id="0142c-140">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0142c-140">Requirement</span></span> | <span data-ttu-id="0142c-141">Valeur</span><span class="sxs-lookup"><span data-stu-id="0142c-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0142c-142">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0142c-142">Minimum supported client</span></span><br/> | <span data-ttu-id="0142c-143">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0142c-143">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0142c-144">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0142c-144">Minimum supported server</span></span><br/> | <span data-ttu-id="0142c-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0142c-145">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0142c-146">DLL</span><span class="sxs-lookup"><span data-stu-id="0142c-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0142c-147"><dt>Mstlsapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0142c-147"><dt>Mstlsapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0142c-148">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0142c-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0142c-149">**TLSConnectToLsServer**</span><span class="sxs-lookup"><span data-stu-id="0142c-149">**TLSConnectToLsServer**</span></span>](tlsconnecttolsserver.md)
</dt> </dl>

 

