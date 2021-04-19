---
description: Effectue une opération d’échange de clés SSL (Server-Side SSL (Secure Sockets Layer) Protocol).
ms.assetid: 052e38ee-658c-47dc-8098-c9a1fd359e1c
title: SslImportMasterKey, fonction (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslImportMasterKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: e21c4cd0f6e51662124e02881b82c905dba68c9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106534257"
---
# <a name="sslimportmasterkey-function"></a><span data-ttu-id="dc5a4-103">SslImportMasterKey fonction)</span><span class="sxs-lookup"><span data-stu-id="dc5a4-103">SslImportMasterKey function</span></span>

<span data-ttu-id="dc5a4-104">La fonction **SslImportMasterKey** effectue une opération d’échange de clés SSL (Server-Side [*SSL (Secure Sockets Layer) Protocol*](/windows/desktop/SecGloss/s-gly) ).</span><span class="sxs-lookup"><span data-stu-id="dc5a4-104">The **SslImportMasterKey** function performs a server-side [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) key exchange operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc5a4-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dc5a4-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslImportMasterKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hPrivateKey,
  _Out_ NCRYPT_KEY_HANDLE  *phMasterKey,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  PNCryptBufferDesc  pParameterList,
  _In_  PBYTE              pbEncryptedKey,
  _In_  DWORD              cbEncryptedKey,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="dc5a4-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dc5a4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dc5a4-107">*hSslProvider* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dc5a4-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc5a4-108">Handle de l’instance du fournisseur de protocole SSL.</span><span class="sxs-lookup"><span data-stu-id="dc5a4-108">The handle to the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="dc5a4-109">*hPrivateKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dc5a4-109">*hPrivateKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc5a4-110">Handle de la [*clé privée*](/windows/desktop/SecGloss/p-gly) utilisée dans l’échange.</span><span class="sxs-lookup"><span data-stu-id="dc5a4-110">The handle to the [*private key*](/windows/desktop/SecGloss/p-gly) used in the exchange.</span></span>

</dd> <dt>

<span data-ttu-id="dc5a4-111">*phMasterKey* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="dc5a4-111">*phMasterKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dc5a4-112">Pointeur vers le handle pour recevoir la [*clé principale*](/windows/desktop/SecGloss/m-gly).</span><span class="sxs-lookup"><span data-stu-id="dc5a4-112">A pointer to the handle to receive the [*master key*](/windows/desktop/SecGloss/m-gly).</span></span>

</dd> <dt>

<span data-ttu-id="dc5a4-113">*dwProtocol* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dc5a4-113">*dwProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc5a4-114">L’une des valeurs d' [**identificateur de protocole du fournisseur SSL CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="dc5a4-114">One of the [**CNG SSL Provider Protocol Identifier**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="dc5a4-115">*dwCipherSuite* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dc5a4-115">*dwCipherSuite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc5a4-116">L’un des valeurs d' [**identificateurs de la suite de chiffrement du fournisseur SSL CNG**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="dc5a4-116">One of the [**CNG SSL Provider Cipher Suite Identifiers**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="dc5a4-117">*pParameterList* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dc5a4-117">*pParameterList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc5a4-118">Pointeur vers un tableau de mémoires tampons [**NCryptBuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) qui contiennent des informations utilisées dans le cadre de l’opération d’échange de clés.</span><span class="sxs-lookup"><span data-stu-id="dc5a4-118">A pointer to an array of [**NCryptBuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) buffers that contain information used as part of the key exchange operation.</span></span> <span data-ttu-id="dc5a4-119">L’ensemble précis de mémoires tampons dépend du protocole et de la suite de chiffrement utilisés.</span><span class="sxs-lookup"><span data-stu-id="dc5a4-119">The precise set of buffers is dependent on the protocol and cipher suite that is used.</span></span> <span data-ttu-id="dc5a4-120">Au minimum, la liste contient des mémoires tampons qui contiennent les valeurs aléatoires fournies par le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="dc5a4-120">At the minimum, the list will contain buffers that contain the client and server supplied random values.</span></span>

</dd> <dt>

<span data-ttu-id="dc5a4-121">*pbEncryptedKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dc5a4-121">*pbEncryptedKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc5a4-122">Pointeur vers une mémoire tampon qui contient la clé secrète de prémaster chiffrée chiffrée avec la [*clé publique*](/windows/desktop/SecGloss/p-gly) du serveur.</span><span class="sxs-lookup"><span data-stu-id="dc5a4-122">A pointer to a buffer that contains the encrypted premaster secret key encrypted with the [*public key*](/windows/desktop/SecGloss/p-gly) of the server.</span></span>

</dd> <dt>

<span data-ttu-id="dc5a4-123">*cbEncryptedKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dc5a4-123">*cbEncryptedKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc5a4-124">Taille, en octets, de la mémoire tampon *pbEncryptedKey* .</span><span class="sxs-lookup"><span data-stu-id="dc5a4-124">The size, in bytes, of the *pbEncryptedKey* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="dc5a4-125">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dc5a4-125">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dc5a4-126">Définissez ce paramètre sur **l' \_ \_ \_ indicateur de serveur SSL NCRYPT** pour indiquer qu’il s’agit d’un appel de serveur.</span><span class="sxs-lookup"><span data-stu-id="dc5a4-126">Set this parameter to **NCRYPT\_SSL\_SERVER\_FLAG** to indicate that this is a server call.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dc5a4-127">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dc5a4-127">Return value</span></span>

<span data-ttu-id="dc5a4-128">Si la fonction est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="dc5a4-128">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="dc5a4-129">Si la fonction échoue, elle retourne une valeur d’erreur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="dc5a4-129">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="dc5a4-130">Les codes de retour possibles incluent, mais ne sont pas limités à, les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="dc5a4-130">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="dc5a4-131">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="dc5a4-131">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="dc5a4-132">Description</span><span class="sxs-lookup"><span data-stu-id="dc5a4-132">Description</span></span>                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="dc5a4-133"><dt>**NPD \_ AUCUNE \_ mémoire**</dt> <dt>0x8009000EL</dt></span><span class="sxs-lookup"><span data-stu-id="dc5a4-133"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="dc5a4-134">La mémoire disponible est insuffisante pour allouer les tampons nécessaires.</span><span class="sxs-lookup"><span data-stu-id="dc5a4-134">Not enough memory is available to allocate necessary buffers.</span></span><br/> |
| <dl> <span data-ttu-id="dc5a4-135"><dt>**NPD \_ \_Handle 0X80090026L non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="dc5a4-135"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="dc5a4-136">L’un des handles fournis n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="dc5a4-136">One of the provided handles is not valid.</span></span><br/>                     |
| <dl> <span data-ttu-id="dc5a4-137"><dt>**NPD \_ \_Paramètre 0X80090027L non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="dc5a4-137"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="dc5a4-138">Le paramètre *phMasterKey* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="dc5a4-138">The *phMasterKey* parameter is **NULL**.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="dc5a4-139">Notes</span><span class="sxs-lookup"><span data-stu-id="dc5a4-139">Remarks</span></span>

<span data-ttu-id="dc5a4-140">Cette fonction déchiffre le secret de prémaster, calcule le secret principal SSL et retourne un handle vers cet objet à l’appelant.</span><span class="sxs-lookup"><span data-stu-id="dc5a4-140">This function decrypts the premaster secret, computes the SSL master secret, and returns a handle to this object to the caller.</span></span> <span data-ttu-id="dc5a4-141">Cette clé principale peut ensuite être utilisée pour dériver la clé de session SSL et terminer le protocole de transfert SSL.</span><span class="sxs-lookup"><span data-stu-id="dc5a4-141">This master key can then be used to derive the SSL session key and finish the SSL handshake.</span></span>

> [!Note]  
> <span data-ttu-id="dc5a4-142">Cette fonction est utilisée lorsque l’algorithme d’échange de clés [*RSA*](/windows/desktop/SecGloss/r-gly) est utilisé.</span><span class="sxs-lookup"><span data-stu-id="dc5a4-142">This function is used when the [*RSA*](/windows/desktop/SecGloss/r-gly) key exchange algorithm is being used.</span></span> <span data-ttu-id="dc5a4-143">Lorsque [*DH*](/windows/desktop/SecGloss/d-gly) est utilisé, le code serveur appelle [**SslGenerateMasterKey**](sslgeneratemasterkey.md) à la place.</span><span class="sxs-lookup"><span data-stu-id="dc5a4-143">When [*DH*](/windows/desktop/SecGloss/d-gly) is used, then the server code calls [**SslGenerateMasterKey**](sslgeneratemasterkey.md) instead.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="dc5a4-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dc5a4-144">Requirements</span></span>



| <span data-ttu-id="dc5a4-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dc5a4-145">Requirement</span></span> | <span data-ttu-id="dc5a4-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="dc5a4-146">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="dc5a4-147">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dc5a4-147">Minimum supported client</span></span><br/> | <span data-ttu-id="dc5a4-148">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dc5a4-148">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="dc5a4-149">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dc5a4-149">Minimum supported server</span></span><br/> | <span data-ttu-id="dc5a4-150">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dc5a4-150">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="dc5a4-151">En-tête</span><span class="sxs-lookup"><span data-stu-id="dc5a4-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="dc5a4-152"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="dc5a4-152"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="dc5a4-153">DLL</span><span class="sxs-lookup"><span data-stu-id="dc5a4-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dc5a4-154"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dc5a4-154"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

