---
description: Récupère un handle vers le hachage de négociation utilisé pour l’authentification du client.
ms.assetid: 55007ce0-4bf1-4605-9b34-2931935762aa
title: SslCreateClientAuthHash, fonction (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslCreateClientAuthHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 4ac83d6d8aeea8429812d80b7bf66de7c87062a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533844"
---
# <a name="sslcreateclientauthhash-function"></a><span data-ttu-id="8d95c-103">SslCreateClientAuthHash fonction)</span><span class="sxs-lookup"><span data-stu-id="8d95c-103">SslCreateClientAuthHash function</span></span>

<span data-ttu-id="8d95c-104">La fonction **SslCreateClientAuthHash** récupère un handle vers le [*hachage*](/windows/desktop/SecGloss/h-gly) de négociation utilisé pour l’authentification du client.</span><span class="sxs-lookup"><span data-stu-id="8d95c-104">The **SslCreateClientAuthHash** function retrieves a handle to the handshake [*hash*](/windows/desktop/SecGloss/h-gly) that is used for client authentication.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d95c-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8d95c-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslCreateClientAuthHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_HASH_HANDLE *phHandshakeHash,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  LPCWSTR            pszHashAlgId,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="8d95c-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8d95c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8d95c-107">*hSslProvider* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8d95c-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d95c-108">Handle de l’instance du fournisseur de protocole du [*protocole SSL (Secure Sockets Layer)*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="8d95c-108">The handle of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="8d95c-109">*phHandshakeHash* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="8d95c-109">*phHandshakeHash* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8d95c-110">Pointeur vers une variable **de \_ \_ handle de hachage NCRYPT** pour recevoir le descripteur de hachage.</span><span class="sxs-lookup"><span data-stu-id="8d95c-110">A pointer to an **NCRYPT\_HASH\_HANDLE** variable to receive the hash handle.</span></span>

</dd> <dt>

<span data-ttu-id="8d95c-111">*dwProtocol* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8d95c-111">*dwProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d95c-112">L’une des valeurs d' [**identificateur de protocole du fournisseur SSL CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="8d95c-112">One of the [**CNG SSL Provider Protocol Identifier**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="8d95c-113">*dwCipherSuite* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8d95c-113">*dwCipherSuite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d95c-114">L’une des valeurs d’identificateur de la [**suite de chiffrement du fournisseur SSL CNG**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="8d95c-114">One of the [**CNG SSL Provider Cipher Suite Identifier**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="8d95c-115">*pszHashAlgId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8d95c-115">*pszHashAlgId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d95c-116">L’un des valeurs des [**identificateurs d’algorithme CNG**](cng-algorithm-identifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="8d95c-116">One of the [**CNG Algorithm Identifiers**](cng-algorithm-identifiers.md) values.</span></span>

</dd> <dt>

<span data-ttu-id="8d95c-117">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8d95c-117">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8d95c-118">Ce paramètre est réservé pour une utilisation ultérieure et doit être défini à zéro.</span><span class="sxs-lookup"><span data-stu-id="8d95c-118">This parameter is reserved for future use and must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8d95c-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8d95c-119">Return value</span></span>

<span data-ttu-id="8d95c-120">Si la fonction est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="8d95c-120">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="8d95c-121">Si la fonction échoue, elle retourne une valeur d’erreur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="8d95c-121">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="8d95c-122">Les codes de retour possibles incluent, mais ne sont pas limités à, les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="8d95c-122">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="8d95c-123">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="8d95c-123">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="8d95c-124">Description</span><span class="sxs-lookup"><span data-stu-id="8d95c-124">Description</span></span>                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8d95c-125"><dt>**NPD \_ \_Handle 0X80090026L non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="8d95c-125"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="8d95c-126">Le paramètre *hSslProvider* contient un pointeur qui n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="8d95c-126">The *hSslProvider* parameter contains a pointer that is not valid.</span></span><br/>                |
| <dl> <span data-ttu-id="8d95c-127"><dt>**NPD \_ \_Paramètre 0X80090027L non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="8d95c-127"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="8d95c-128">Le paramètre *phHandshakeHash* a la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="8d95c-128">The *phHandshakeHash* parameter is set to **NULL**.</span></span><br/>                               |
| <dl> <span data-ttu-id="8d95c-129"><dt>**NPD \_ 0x80090029L non \_ pris en charge**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="8d95c-129"><dt>**NTE\_NOT\_SUPPORTED**</dt> <dt>0x80090029L</dt></span></span> </dl>     | <span data-ttu-id="8d95c-130">La fonction sélectionnée n’est pas prise en charge dans la version spécifiée de l’interface.</span><span class="sxs-lookup"><span data-stu-id="8d95c-130">The selected function is not supported in the specified version of the interface.</span></span><br/> |
| <dl> <span data-ttu-id="8d95c-131"><dt>**NPD \_ AUCUNE \_ mémoire**</dt> <dt>0x8009000EL</dt></span><span class="sxs-lookup"><span data-stu-id="8d95c-131"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="8d95c-132">Mémoire insuffisante pour allouer des tampons.</span><span class="sxs-lookup"><span data-stu-id="8d95c-132">Insufficient memory to allocate buffers.</span></span><br/>                                          |
| <dl> <span data-ttu-id="8d95c-133"><dt>**NPD \_ \_Indicateurs INcorrects**</dt> <dt>0x80090009L</dt></span><span class="sxs-lookup"><span data-stu-id="8d95c-133"><dt>**NTE\_BAD\_FLAGS**</dt> <dt>0x80090009L</dt></span></span> </dl>         | <span data-ttu-id="8d95c-134">Le paramètre *dwFlags* doit avoir la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="8d95c-134">The *dwFlags* parameter must be set to zero.</span></span><br/>                                      |



 

## <a name="remarks"></a><span data-ttu-id="8d95c-135">Notes</span><span class="sxs-lookup"><span data-stu-id="8d95c-135">Remarks</span></span>

<span data-ttu-id="8d95c-136">La fonction **SslCreateClientAuthHash** est appelée pour les conversations TLS ( [*Transport Layer Security Protocol*](/windows/desktop/SecGloss/t-gly) ) 1,2 ou ultérieures pour créer des objets de hachage utilisés pour hacher les messages de négociation.</span><span class="sxs-lookup"><span data-stu-id="8d95c-136">The **SslCreateClientAuthHash** function is called for [*Transport Layer Security protocol*](/windows/desktop/SecGloss/t-gly) (TLS) 1.2 or later conversations to create hash objects that are used to hash handshake messages.</span></span> <span data-ttu-id="8d95c-137">Elle est appelée une fois pour chaque [*algorithme de hachage*](/windows/desktop/SecGloss/h-gly) possible qui peut être utilisé dans la signature d’authentification du client.</span><span class="sxs-lookup"><span data-stu-id="8d95c-137">It is called once for each possible [*hashing algorithm*](/windows/desktop/SecGloss/h-gly) that can be used in the client authentication signature.</span></span>

## <a name="requirements"></a><span data-ttu-id="8d95c-138">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8d95c-138">Requirements</span></span>



| <span data-ttu-id="8d95c-139">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8d95c-139">Requirement</span></span> | <span data-ttu-id="8d95c-140">Valeur</span><span class="sxs-lookup"><span data-stu-id="8d95c-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8d95c-141">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8d95c-141">Minimum supported client</span></span><br/> | <span data-ttu-id="8d95c-142">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8d95c-142">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="8d95c-143">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8d95c-143">Minimum supported server</span></span><br/> | <span data-ttu-id="8d95c-144">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8d95c-144">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="8d95c-145">En-tête</span><span class="sxs-lookup"><span data-stu-id="8d95c-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="8d95c-146"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="8d95c-146"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="8d95c-147">DLL</span><span class="sxs-lookup"><span data-stu-id="8d95c-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8d95c-148"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8d95c-148"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

