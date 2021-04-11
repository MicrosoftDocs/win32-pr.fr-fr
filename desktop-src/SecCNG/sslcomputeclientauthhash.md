---
description: Calcule un hachage à utiliser pendant l’authentification par certificat.
ms.assetid: f4a12464-8ad6-4bf9-8b6e-49bdf5332b66
title: SslComputeClientAuthHash, fonction (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslComputeClientAuthHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: faea1699657efd92049068e48ff361c48242e9c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202393"
---
# <a name="sslcomputeclientauthhash-function"></a><span data-ttu-id="3430a-103">SslComputeClientAuthHash fonction)</span><span class="sxs-lookup"><span data-stu-id="3430a-103">SslComputeClientAuthHash function</span></span>

<span data-ttu-id="3430a-104">La fonction **SslComputeClientAuthHash** calcule un [*hachage*](/windows/desktop/SecGloss/h-gly) à utiliser pendant l’authentification par [*certificat*](/windows/desktop/SecGloss/c-gly) .</span><span class="sxs-lookup"><span data-stu-id="3430a-104">The **SslComputeClientAuthHash** function computes a [*hash*](/windows/desktop/SecGloss/h-gly) to use during [*certificate*](/windows/desktop/SecGloss/c-gly) authentication.</span></span>

## <a name="syntax"></a><span data-ttu-id="3430a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3430a-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslComputeClientAuthHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hMasterKey,
  _In_  NCRYPT_HASH_HANDLE hHandshakeHash,
  _In_  LPCWSTR            pszAlgId,
  _Out_ PBYTE              pbOutput,
  _In_  DWORD              cbOutput,
  _Out_ DWORD              *pcbResult,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="3430a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3430a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3430a-107">*hSslProvider* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3430a-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3430a-108">Handle de l’instance du fournisseur de protocole du [*protocole SSL (Secure Sockets Layer)*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="3430a-108">The handle of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="3430a-109">*hMasterKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3430a-109">*hMasterKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3430a-110">Handle de l’objet de [*clé principale*](/windows/desktop/SecGloss/m-gly) .</span><span class="sxs-lookup"><span data-stu-id="3430a-110">The handle of the [*master key*](/windows/desktop/SecGloss/m-gly) object.</span></span>

</dd> <dt>

<span data-ttu-id="3430a-111">*hHandshakeHash* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3430a-111">*hHandshakeHash* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3430a-112">Handle du hachage du protocole de transfert calculé jusqu’à présent.</span><span class="sxs-lookup"><span data-stu-id="3430a-112">The handle of the hash of the handshake computed so far.</span></span>

</dd> <dt>

<span data-ttu-id="3430a-113">*pszAlgId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3430a-113">*pszAlgId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3430a-114">Pointeur vers une chaîne Unicode terminée par le caractère null qui identifie l' [*algorithme de chiffrement*](/windows/desktop/SecGloss/c-gly)demandé.</span><span class="sxs-lookup"><span data-stu-id="3430a-114">A pointer to a null-terminated Unicode string that identifies the requested [*cryptographic algorithm*](/windows/desktop/SecGloss/c-gly).</span></span> <span data-ttu-id="3430a-115">Il peut s’agir de l’un des [**identificateurs d’algorithme CNG**](cng-algorithm-identifiers.md) standard ou de l’identificateur d’un autre algorithme inscrit.</span><span class="sxs-lookup"><span data-stu-id="3430a-115">This can be one of the standard [**CNG Algorithm Identifiers**](cng-algorithm-identifiers.md) or the identifier for another registered algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="3430a-116">*pbOutput* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3430a-116">*pbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3430a-117">Adresse d’une mémoire tampon qui reçoit l' [*objet blob de clé*](/windows/desktop/SecGloss/k-gly).</span><span class="sxs-lookup"><span data-stu-id="3430a-117">The address of a buffer that receives the [*key BLOB*](/windows/desktop/SecGloss/k-gly).</span></span> <span data-ttu-id="3430a-118">Le paramètre *cbOutput* contient la taille de cette mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="3430a-118">The *cbOutput* parameter contains the size of this buffer.</span></span> <span data-ttu-id="3430a-119">Si ce paramètre a la **valeur null**, cette fonction place la taille requise, en octets, dans la **valeur DWORD** pointée par le paramètre *pcbResult* .</span><span class="sxs-lookup"><span data-stu-id="3430a-119">If this parameter is **NULL**, this function will place the required size, in bytes, in the **DWORD** pointed to by the *pcbResult* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="3430a-120">*cbOutput* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3430a-120">*cbOutput* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3430a-121">Longueur, en octets, de la mémoire tampon *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="3430a-121">The length, in bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="3430a-122">*pcbResult* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="3430a-122">*pcbResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3430a-123">Pointeur vers une valeur **DWORD** qui spécifie la longueur, en octets, du hachage écrit dans la mémoire tampon *pbOutput* .</span><span class="sxs-lookup"><span data-stu-id="3430a-123">A pointer to a **DWORD** value that specifies the length, in bytes, of the hash written to the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="3430a-124">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3430a-124">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3430a-125">Ce paramètre est réservé à un usage futur.</span><span class="sxs-lookup"><span data-stu-id="3430a-125">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3430a-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="3430a-126">Return value</span></span>

<span data-ttu-id="3430a-127">Si la fonction est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="3430a-127">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="3430a-128">Si la fonction échoue, elle retourne une valeur d’erreur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="3430a-128">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="3430a-129">Les codes de retour possibles incluent, mais ne sont pas limités à, les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="3430a-129">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="3430a-130">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="3430a-130">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="3430a-131">Description</span><span class="sxs-lookup"><span data-stu-id="3430a-131">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="3430a-132"><dt>**NPD \_ \_Handle 0X80090026L non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="3430a-132"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="3430a-133">L’un des handles fournis n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="3430a-133">One of the supplied handles is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="3430a-134">Notes</span><span class="sxs-lookup"><span data-stu-id="3430a-134">Remarks</span></span>

<span data-ttu-id="3430a-135">La fonction **SslComputeClientAuthHash** calcule le hachage qui est envoyé dans le message de vérification du certificat de la négociation SSL.</span><span class="sxs-lookup"><span data-stu-id="3430a-135">The **SslComputeClientAuthHash** function computes the hash that is sent in the certificate verification message of the SSL handshake.</span></span> <span data-ttu-id="3430a-136">La valeur de hachage est calculée en créant un hachage qui contient le secret principal avec un hachage de tous les messages de négociation précédents envoyés ou reçus.</span><span class="sxs-lookup"><span data-stu-id="3430a-136">The hash value is computed by creating a hash that contains the master secret with a hash of all previous handshake messages sent or received.</span></span> <span data-ttu-id="3430a-137">Pour plus d’informations sur la séquence de négociation SSL, consultez [Description du protocole de transfert de SSL (Secure Sockets Layer) (SSL)](https://support.microsoft.com/kb/257591).</span><span class="sxs-lookup"><span data-stu-id="3430a-137">For more information about the SSL handshake sequence, see [Description of the Secure Sockets Layer (SSL) Handshake](https://support.microsoft.com/kb/257591).</span></span>

<span data-ttu-id="3430a-138">La manière dont le hachage est calculé dépend du protocole et de la suite de chiffrement utilisés.</span><span class="sxs-lookup"><span data-stu-id="3430a-138">The manner in which the hash is computed depends on the protocol and cipher suite used.</span></span> <span data-ttu-id="3430a-139">En outre, le hachage dépend du type de clé d’authentification du client utilisé ; le paramètre *pszAlgId* indique le type de clé utilisé pour l’authentification du client.</span><span class="sxs-lookup"><span data-stu-id="3430a-139">In addition, the hash depends on the type of client authentication key used; the *pszAlgId* parameter indicates the type of key used for client authentication.</span></span>

## <a name="requirements"></a><span data-ttu-id="3430a-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3430a-140">Requirements</span></span>



| <span data-ttu-id="3430a-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3430a-141">Requirement</span></span> | <span data-ttu-id="3430a-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="3430a-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3430a-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3430a-143">Minimum supported client</span></span><br/> | <span data-ttu-id="3430a-144">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3430a-144">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3430a-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3430a-145">Minimum supported server</span></span><br/> | <span data-ttu-id="3430a-146">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3430a-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3430a-147">En-tête</span><span class="sxs-lookup"><span data-stu-id="3430a-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="3430a-148"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="3430a-148"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="3430a-149">DLL</span><span class="sxs-lookup"><span data-stu-id="3430a-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3430a-150"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3430a-150"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

