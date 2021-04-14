---
description: Calcule la clé de secret principal du protocole SSL (Secure Sockets Layer) (SSL).
ms.assetid: c9408eb3-711d-42c3-a4ba-e388689da34e
title: SslGenerateMasterKey, fonction (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGenerateMasterKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: ae8b357743cabf652721d3666c177990568718e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104393807"
---
# <a name="sslgeneratemasterkey-function"></a><span data-ttu-id="91a56-103">SslGenerateMasterKey fonction)</span><span class="sxs-lookup"><span data-stu-id="91a56-103">SslGenerateMasterKey function</span></span>

<span data-ttu-id="91a56-104">La fonction **SslGenerateMasterKey** calcule la clé de secret principal du [*protocole SSL (Secure Sockets Layer)*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="91a56-104">The **SslGenerateMasterKey** function computes the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) master secret key.</span></span>

## <a name="syntax"></a><span data-ttu-id="91a56-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="91a56-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslGenerateMasterKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hPrivateKey,
  _In_  NCRYPT_KEY_HANDLE  hPublicKey,
  _Out_ NCRYPT_KEY_HANDLE  *phMasterKey,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  PNCryptBufferDesc  pParameterList,
  _Out_ PBYTE              pbOutput,
  _In_  DWORD              cbOutput,
  _Out_ DWORD              *pcbResult,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="91a56-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="91a56-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91a56-107">*hSslProvider* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="91a56-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91a56-108">Handle de l’instance du fournisseur de protocole SSL.</span><span class="sxs-lookup"><span data-stu-id="91a56-108">The handle to the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="91a56-109">*hPrivateKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="91a56-109">*hPrivateKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91a56-110">Handle de la [*clé privée*](/windows/desktop/SecGloss/p-gly) utilisée dans l’échange.</span><span class="sxs-lookup"><span data-stu-id="91a56-110">The handle to the [*private key*](/windows/desktop/SecGloss/p-gly) used in the exchange.</span></span>

</dd> <dt>

<span data-ttu-id="91a56-111">*hPublicKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="91a56-111">*hPublicKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91a56-112">Handle de la [*clé publique*](/windows/desktop/SecGloss/p-gly) utilisée dans l’échange.</span><span class="sxs-lookup"><span data-stu-id="91a56-112">The handle to the [*public key*](/windows/desktop/SecGloss/p-gly) used in the exchange.</span></span>

</dd> <dt>

<span data-ttu-id="91a56-113">*phMasterKey* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="91a56-113">*phMasterKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="91a56-114">Pointeur vers le handle de la [*clé principale*](/windows/desktop/SecGloss/m-gly)générée.</span><span class="sxs-lookup"><span data-stu-id="91a56-114">A pointer to the handle to the generated [*master key*](/windows/desktop/SecGloss/m-gly).</span></span>

</dd> <dt>

<span data-ttu-id="91a56-115">*dwProtocol* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="91a56-115">*dwProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91a56-116">L’une des valeurs d' [**identificateur de protocole du fournisseur SSL CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="91a56-116">One of the [**CNG SSL Provider Protocol Identifier**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="91a56-117">*dwCipherSuite* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="91a56-117">*dwCipherSuite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91a56-118">L’une des valeurs d’identificateur de la [**suite de chiffrement du fournisseur SSL CNG**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="91a56-118">One of the [**CNG SSL Provider Cipher Suite Identifier**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="91a56-119">*pParameterList* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="91a56-119">*pParameterList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91a56-120">Pointeur vers un tableau de mémoires tampons [**NCryptBuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) qui contiennent des informations utilisées dans le cadre de l’opération d’échange de clés.</span><span class="sxs-lookup"><span data-stu-id="91a56-120">A pointer to an array of [**NCryptBuffer**](https://msdn.microsoft.com/library/Aa376245(v=VS.85).aspx) buffers that contain information used as part of the key exchange operation.</span></span> <span data-ttu-id="91a56-121">L’ensemble précis de mémoires tampons dépend du protocole et de la suite de chiffrement utilisés.</span><span class="sxs-lookup"><span data-stu-id="91a56-121">The precise set of buffers is dependent on the protocol and cipher suite that is used.</span></span> <span data-ttu-id="91a56-122">Au minimum, la liste contient des mémoires tampons qui contiennent les valeurs aléatoires fournies par le client et le serveur.</span><span class="sxs-lookup"><span data-stu-id="91a56-122">At the minimum, the list will contain buffers that contain the client and server supplied random values.</span></span>

</dd> <dt>

<span data-ttu-id="91a56-123">*pbOutput* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="91a56-123">*pbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="91a56-124">Adresse d’une mémoire tampon qui reçoit le secret de prémaster chiffré avec la clé publique du serveur.</span><span class="sxs-lookup"><span data-stu-id="91a56-124">The address of a buffer that receives the premaster secret encrypted with the public key of the server.</span></span> <span data-ttu-id="91a56-125">Le paramètre *cbOutput* contient la taille de cette mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="91a56-125">The *cbOutput* parameter contains the size of this buffer.</span></span> <span data-ttu-id="91a56-126">Si ce paramètre a la **valeur null**, cette fonction retourne la taille requise, en octets, dans la **valeur DWORD** pointée par le paramètre *pcbResult* .</span><span class="sxs-lookup"><span data-stu-id="91a56-126">If this parameter is **NULL**, this function returns the required size, in bytes, in the **DWORD** pointed to by the *pcbResult* parameter.</span></span>

> [!Note]  
> <span data-ttu-id="91a56-127">Ce tampon est utilisé lors de l’exécution d’un échange de clés RSA.</span><span class="sxs-lookup"><span data-stu-id="91a56-127">This buffer is used when performing a RSA key exchange.</span></span>

 

</dd> <dt>

<span data-ttu-id="91a56-128">*cbOutput* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="91a56-128">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91a56-129">Taille, en octets, de la mémoire tampon *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="91a56-129">The size, in bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="91a56-130">*pcbResult* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="91a56-130">*pcbResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="91a56-131">Pointeur vers une valeur **DWORD** dans laquelle placer le nombre d’octets écrits dans la mémoire tampon *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="91a56-131">A pointer to a **DWORD** value in which to place number of bytes written to the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="91a56-132">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="91a56-132">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="91a56-133">Spécifie si cette fonction est utilisée pour l’échange de clés côté client ou côté serveur.</span><span class="sxs-lookup"><span data-stu-id="91a56-133">Specifies whether this function is being used for client-side or server-side key exchange.</span></span>



| <span data-ttu-id="91a56-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="91a56-134">Value</span></span>                                                                                                                                                                                                                                                      | <span data-ttu-id="91a56-135">Signification</span><span class="sxs-lookup"><span data-stu-id="91a56-135">Meaning</span></span>                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <span id="NCRYPT_SSL_CLIENT_FLAG"></span><span id="ncrypt_ssl_client_flag"></span><dl> <span data-ttu-id="91a56-136"><dt>**NCRYPT \_ \_ \_ Indicateur client SSL**</dt> <dt>0x00000001</dt></span><span class="sxs-lookup"><span data-stu-id="91a56-136"><dt>**NCRYPT\_SSL\_CLIENT\_FLAG**</dt> <dt>0x00000001</dt></span></span> </dl> | <span data-ttu-id="91a56-137">Spécifie un échange de clés côté client.</span><span class="sxs-lookup"><span data-stu-id="91a56-137">Specifies a client-side key exchange.</span></span><br/> |
| <span id="NCRYPT_SSL_SERVER_FLAG"></span><span id="ncrypt_ssl_server_flag"></span><dl> <span data-ttu-id="91a56-138"><dt>**NCRYPT \_ \_ \_ Indicateur de serveur SSL**</dt> <dt>0x00000002</dt></span><span class="sxs-lookup"><span data-stu-id="91a56-138"><dt>**NCRYPT\_SSL\_SERVER\_FLAG**</dt> <dt>0x00000002</dt></span></span> </dl> | <span data-ttu-id="91a56-139">Spécifie un échange de clés côté serveur.</span><span class="sxs-lookup"><span data-stu-id="91a56-139">Specifies a server-side key exchange.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="91a56-140">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="91a56-140">Return value</span></span>

<span data-ttu-id="91a56-141">Si la fonction est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="91a56-141">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="91a56-142">Si la fonction échoue, elle retourne une valeur d’erreur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="91a56-142">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="91a56-143">Les codes de retour possibles incluent, mais ne sont pas limités à, les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="91a56-143">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="91a56-144">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="91a56-144">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="91a56-145">Description</span><span class="sxs-lookup"><span data-stu-id="91a56-145">Description</span></span>                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="91a56-146"><dt>**NPD \_ AUCUNE \_ mémoire**</dt> <dt>0x8009000EL</dt></span><span class="sxs-lookup"><span data-stu-id="91a56-146"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="91a56-147">La mémoire disponible est insuffisante pour allouer les tampons nécessaires.</span><span class="sxs-lookup"><span data-stu-id="91a56-147">Not enough memory is available to allocate necessary buffers.</span></span><br/> |
| <dl> <span data-ttu-id="91a56-148"><dt>**NPD \_ \_Handle 0X80090026L non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="91a56-148"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="91a56-149">L’un des handles fournis n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="91a56-149">One of the provided handles is not valid.</span></span><br/>                     |
| <dl> <span data-ttu-id="91a56-150"><dt>**NPD \_ \_Paramètre 0X80090027L non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="91a56-150"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="91a56-151">Le paramètre *phMasterKey* ou *hPublicKey* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="91a56-151">The *phMasterKey* or *hPublicKey* parameter is not valid.</span></span><br/>     |



 

## <a name="requirements"></a><span data-ttu-id="91a56-152">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="91a56-152">Requirements</span></span>



| <span data-ttu-id="91a56-153">Condition requise</span><span class="sxs-lookup"><span data-stu-id="91a56-153">Requirement</span></span> | <span data-ttu-id="91a56-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="91a56-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="91a56-155">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91a56-155">Minimum supported client</span></span><br/> | <span data-ttu-id="91a56-156">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="91a56-156">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="91a56-157">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="91a56-157">Minimum supported server</span></span><br/> | <span data-ttu-id="91a56-158">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="91a56-158">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="91a56-159">En-tête</span><span class="sxs-lookup"><span data-stu-id="91a56-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="91a56-160"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="91a56-160"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="91a56-161">DLL</span><span class="sxs-lookup"><span data-stu-id="91a56-161">DLL</span></span><br/>                      | <dl> <span data-ttu-id="91a56-162"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="91a56-162"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

