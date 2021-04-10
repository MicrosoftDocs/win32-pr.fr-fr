---
description: Calcule le hachage envoyé dans le message terminé de la négociation SSL (SSL (Secure Sockets Layer) Protocol).
ms.assetid: 82dfeb1d-c141-40c9-b692-daad78ab6d55
title: SslComputeFinishedHash, fonction (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslComputeFinishedHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 365f3c849b0a499d2bd875c8d234bbda1911eb71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951681"
---
# <a name="sslcomputefinishedhash-function"></a><span data-ttu-id="885c2-103">SslComputeFinishedHash fonction)</span><span class="sxs-lookup"><span data-stu-id="885c2-103">SslComputeFinishedHash function</span></span>

<span data-ttu-id="885c2-104">La fonction **SslComputeFinishedHash** calcule le [*hachage*](/windows/desktop/SecGloss/h-gly) envoyé dans le message terminé de la négociation du [*protocole SSL (Secure Sockets Layer)*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="885c2-104">The **SslComputeFinishedHash** function computes the [*hash*](/windows/desktop/SecGloss/h-gly) sent in the finished message of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) handshake.</span></span> <span data-ttu-id="885c2-105">Pour plus d’informations sur la séquence de négociation SSL, consultez [Description du protocole de transfert de SSL (Secure Sockets Layer) (SSL)](https://support.microsoft.com/kb/257591).</span><span class="sxs-lookup"><span data-stu-id="885c2-105">For more information about the SSL handshake sequence, see [Description of the Secure Sockets Layer (SSL) Handshake](https://support.microsoft.com/kb/257591).</span></span>

## <a name="syntax"></a><span data-ttu-id="885c2-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="885c2-106">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslComputeFinishedHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hMasterKey,
  _In_  NCRYPT_HASH_HANDLE hHandshakeHash,
  _Out_ PBYTE              pbOutput,
  _In_  DWORD              cbOutput,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="885c2-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="885c2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="885c2-108">*hSslProvider* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="885c2-108">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="885c2-109">Handle de l’instance du fournisseur de protocole SSL.</span><span class="sxs-lookup"><span data-stu-id="885c2-109">The handle of the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="885c2-110">*hMasterKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="885c2-110">*hMasterKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="885c2-111">Handle de l’objet de [*clé principale*](/windows/desktop/SecGloss/m-gly) .</span><span class="sxs-lookup"><span data-stu-id="885c2-111">The handle of the [*master key*](/windows/desktop/SecGloss/m-gly) object.</span></span>

</dd> <dt>

<span data-ttu-id="885c2-112">*hHandshakeHash* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="885c2-112">*hHandshakeHash* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="885c2-113">Handle du hachage des messages de négociation.</span><span class="sxs-lookup"><span data-stu-id="885c2-113">The handle of the hash of the handshake messages.</span></span>

</dd> <dt>

<span data-ttu-id="885c2-114">*pbOutput* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="885c2-114">*pbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="885c2-115">Pointeur vers une mémoire tampon qui reçoit le hachage pour le message de fin.</span><span class="sxs-lookup"><span data-stu-id="885c2-115">A pointer to a buffer that receives the hash for the finish message.</span></span>

</dd> <dt>

<span data-ttu-id="885c2-116">*cbOutput* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="885c2-116">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="885c2-117">Longueur, en octets, de la mémoire tampon *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="885c2-117">The length, in bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="885c2-118">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="885c2-118">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="885c2-119">Une des constantes suivantes.</span><span class="sxs-lookup"><span data-stu-id="885c2-119">One of the following constants.</span></span>



| <span data-ttu-id="885c2-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="885c2-120">Value</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="885c2-121">Signification</span><span class="sxs-lookup"><span data-stu-id="885c2-121">Meaning</span></span>                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="NCRYPT_SSL_CLIENT_FLAG"></span><span id="ncrypt_ssl_client_flag"></span><dl> <span data-ttu-id="885c2-122"><dt>**NCRYPT \_ \_ \_ Indicateur client SSL**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="885c2-122"><dt>**NCRYPT\_SSL\_CLIENT\_FLAG**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="885c2-123">Spécifie qu’il s’agit d’un appel client.</span><span class="sxs-lookup"><span data-stu-id="885c2-123">Specifies that this is a client call.</span></span><br/> |
| <span id="NCRYPT_SSL_SERVER_FLAG"></span><span id="ncrypt_ssl_server_flag"></span><dl> <span data-ttu-id="885c2-124"><dt>**NCRYPT \_ \_ \_ Indicateur de serveur SSL**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="885c2-124"><dt>**NCRYPT\_SSL\_SERVER\_FLAG**</dt> <dt>0x00000002</dt></span></span> </dl> | <span data-ttu-id="885c2-125">Spécifie qu’il s’agit d’un appel de serveur.</span><span class="sxs-lookup"><span data-stu-id="885c2-125">Specifies that this is a server call.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="885c2-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="885c2-126">Return value</span></span>

<span data-ttu-id="885c2-127">Si la fonction est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="885c2-127">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="885c2-128">Si la fonction échoue, elle retourne une valeur d’erreur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="885c2-128">If the function fails, it returns a nonzero error value.</span></span>



| <span data-ttu-id="885c2-129">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="885c2-129">Return code/value</span></span>                                                                                                                                                                | <span data-ttu-id="885c2-130">Description</span><span class="sxs-lookup"><span data-stu-id="885c2-130">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="885c2-131"><dt>**NPD \_ \_HANDLE 2148073510 non valide**</dt> <dt>(0x80090026)</dt></span><span class="sxs-lookup"><span data-stu-id="885c2-131"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>2148073510 (0x80090026)</dt></span></span> </dl> | <span data-ttu-id="885c2-132">L’un des handles fournis n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="885c2-132">One of the supplied handles is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="885c2-133">Notes</span><span class="sxs-lookup"><span data-stu-id="885c2-133">Remarks</span></span>

<span data-ttu-id="885c2-134">La fonction **SslComputeFinishedHash** est l’une des trois fonctions utilisées pour générer un hachage à utiliser pendant la négociation SSL.</span><span class="sxs-lookup"><span data-stu-id="885c2-134">The **SslComputeFinishedHash** function is one of three functions used to generate a hash to use during the SSL handshake.</span></span>

1.  <span data-ttu-id="885c2-135">La fonction [**SslCreateHandshakeHash**](sslcreatehandshakehash.md) est appelée pour obtenir un handle de hachage.</span><span class="sxs-lookup"><span data-stu-id="885c2-135">The [**SslCreateHandshakeHash**](sslcreatehandshakehash.md) function is called to obtain a hash handle.</span></span>
2.  <span data-ttu-id="885c2-136">La fonction [**SslHashHandshake**](sslhashhandshake.md) est appelée un nombre quelconque de fois avec le handle de hachage pour ajouter des données au hachage.</span><span class="sxs-lookup"><span data-stu-id="885c2-136">The [**SslHashHandshake**](sslhashhandshake.md) function is called any number of times with the hash handle to add data to the hash.</span></span>
3.  <span data-ttu-id="885c2-137">La fonction **SslComputeFinishedHash** est appelée avec le descripteur de hachage pour obtenir le condensé des données hachées.</span><span class="sxs-lookup"><span data-stu-id="885c2-137">The **SslComputeFinishedHash** function is called with the hash handle to obtain the digest of the hashed data.</span></span>

<span data-ttu-id="885c2-138">La valeur de hachage est calculée en hachant le secret principal avec un hachage de tous les messages de négociation précédents envoyés ou reçus.</span><span class="sxs-lookup"><span data-stu-id="885c2-138">The hash value is computed by hashing the master secret with a hash of all previous handshake messages sent or received.</span></span>

<span data-ttu-id="885c2-139">La valeur de *cbOutput* détermine la longueur des données de hachage.</span><span class="sxs-lookup"><span data-stu-id="885c2-139">The value of *cbOutput* determines the length of the hash data.</span></span> <span data-ttu-id="885c2-140">Lorsque le protocole TLS ( [*Transport Layer Security*](/windows/desktop/SecGloss/t-gly) ) 1,0 est utilisé, il doit toujours être de 12 (octets).</span><span class="sxs-lookup"><span data-stu-id="885c2-140">When the [*Transport Layer Security protocol*](/windows/desktop/SecGloss/t-gly) (TLS) 1.0 protocol is used, this should always be 12 (bytes).</span></span> <span data-ttu-id="885c2-141">Pour plus d’informations, consultez [la Version 1,0 du protocole TLS](https://www.ietf.org/rfc/rfc2246.txt).</span><span class="sxs-lookup"><span data-stu-id="885c2-141">For more information, see [The TLS Protocol Version 1.0](https://www.ietf.org/rfc/rfc2246.txt).</span></span>

## <a name="requirements"></a><span data-ttu-id="885c2-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="885c2-142">Requirements</span></span>



| <span data-ttu-id="885c2-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="885c2-143">Requirement</span></span> | <span data-ttu-id="885c2-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="885c2-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="885c2-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="885c2-145">Minimum supported client</span></span><br/> | <span data-ttu-id="885c2-146">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="885c2-146">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="885c2-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="885c2-147">Minimum supported server</span></span><br/> | <span data-ttu-id="885c2-148">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="885c2-148">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="885c2-149">En-tête</span><span class="sxs-lookup"><span data-stu-id="885c2-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="885c2-150"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="885c2-150"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="885c2-151">DLL</span><span class="sxs-lookup"><span data-stu-id="885c2-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="885c2-152"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="885c2-152"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

