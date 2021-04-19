---
description: Obtient un handle de hachage utilisé pour hacher les messages de négociation.
ms.assetid: 31390584-9d23-41d1-8604-b84a5e52ecde
title: SslCreateHandshakeHash, fonction (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslCreateHandshakeHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 8affda999278ce2d4a740293a7532643a6c564ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524608"
---
# <a name="sslcreatehandshakehash-function"></a><span data-ttu-id="bf03b-103">SslCreateHandshakeHash fonction)</span><span class="sxs-lookup"><span data-stu-id="bf03b-103">SslCreateHandshakeHash function</span></span>

<span data-ttu-id="bf03b-104">La fonction **SslCreateHandshakeHash** obtient un descripteur de hachage utilisé pour hacher les messages de négociation.</span><span class="sxs-lookup"><span data-stu-id="bf03b-104">The **SslCreateHandshakeHash** function obtains a hash handle that is used to hash handshake messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf03b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="bf03b-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslCreateHandshakeHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_HASH_HANDLE *phHandshakeHash,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="bf03b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="bf03b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf03b-107">*hSslProvider* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bf03b-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf03b-108">Handle de l’instance du fournisseur de protocole du [*protocole SSL (Secure Sockets Layer)*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="bf03b-108">The handle of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="bf03b-109">*phHandshakeHash* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="bf03b-109">*phHandshakeHash* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bf03b-110">Handle de hachage qui peut être passé à d’autres fonctions du fournisseur SSL.</span><span class="sxs-lookup"><span data-stu-id="bf03b-110">A hash handle that can be passed to other SSL provider functions.</span></span>

</dd> <dt>

<span data-ttu-id="bf03b-111">*dwProtocol* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bf03b-111">*dwProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf03b-112">L’une des valeurs d' [**identificateur de protocole du fournisseur SSL CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="bf03b-112">One of the [**CNG SSL Provider Protocol Identifier**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) values.</span></span>

> [!Note]  
> <span data-ttu-id="bf03b-113">Cette fonction n’est pas utilisée avec le protocole SSL 2,0.</span><span class="sxs-lookup"><span data-stu-id="bf03b-113">This function is not used with the SSL 2.0 protocol.</span></span>

 

</dd> <dt>

<span data-ttu-id="bf03b-114">*dwCipherSuite* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bf03b-114">*dwCipherSuite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf03b-115">L’une des valeurs d’identificateur de la [**suite de chiffrement du fournisseur SSL CNG**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="bf03b-115">One of the [**CNG SSL Provider Cipher Suite Identifier**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="bf03b-116">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="bf03b-116">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bf03b-117">Ce paramètre est réservé à un usage futur.</span><span class="sxs-lookup"><span data-stu-id="bf03b-117">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf03b-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="bf03b-118">Return value</span></span>

<span data-ttu-id="bf03b-119">Si la fonction est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="bf03b-119">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="bf03b-120">Si la fonction échoue, elle retourne une valeur d’erreur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="bf03b-120">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="bf03b-121">Les codes de retour possibles incluent, mais ne sont pas limités à, les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="bf03b-121">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="bf03b-122">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="bf03b-122">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="bf03b-123">Description</span><span class="sxs-lookup"><span data-stu-id="bf03b-123">Description</span></span>                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="bf03b-124"><dt>**NPD \_ AUCUNE \_ mémoire**</dt> <dt>0x8009000EL</dt></span><span class="sxs-lookup"><span data-stu-id="bf03b-124"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="bf03b-125">La mémoire est insuffisante pour allouer la mémoire tampon de hachage.</span><span class="sxs-lookup"><span data-stu-id="bf03b-125">There is insufficient memory to allocate the hash buffer.</span></span><br/> |
| <dl> <span data-ttu-id="bf03b-126"><dt>**NPD \_ \_Handle 0X80090026L non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="bf03b-126"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="bf03b-127">Le descripteur *hSslProvider* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="bf03b-127">The *hSslProvider* handle is not valid.</span></span><br/>                   |
| <dl> <span data-ttu-id="bf03b-128"><dt>**NPD \_ \_Paramètre 0X80090027L non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="bf03b-128"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="bf03b-129">*PhHandshakeHash* a la valeur null.</span><span class="sxs-lookup"><span data-stu-id="bf03b-129">The *phHandshakeHash* is null.</span></span><br/>                            |



 

## <a name="remarks"></a><span data-ttu-id="bf03b-130">Notes</span><span class="sxs-lookup"><span data-stu-id="bf03b-130">Remarks</span></span>

<span data-ttu-id="bf03b-131">La fonction **SslCreateHandshakeHash** est l’une des trois fonctions utilisées pour générer un hachage à utiliser pendant la négociation SSL.</span><span class="sxs-lookup"><span data-stu-id="bf03b-131">The **SslCreateHandshakeHash** function is one of three functions used to generate a hash to use during the SSL handshake.</span></span>

1.  <span data-ttu-id="bf03b-132">La fonction **SslCreateHandshakeHash** est appelée pour obtenir un handle de hachage.</span><span class="sxs-lookup"><span data-stu-id="bf03b-132">The **SslCreateHandshakeHash** function is called to obtain a hash handle.</span></span>
2.  <span data-ttu-id="bf03b-133">La fonction [**SslHashHandshake**](sslhashhandshake.md) est appelée un nombre quelconque de fois avec le handle de hachage pour ajouter des données au hachage.</span><span class="sxs-lookup"><span data-stu-id="bf03b-133">The [**SslHashHandshake**](sslhashhandshake.md) function is called any number of times with the hash handle to add data to the hash.</span></span>
3.  <span data-ttu-id="bf03b-134">La fonction [**SslComputeFinishedHash**](sslcomputefinishedhash.md) est appelée avec le descripteur de hachage pour obtenir le condensé des données hachées.</span><span class="sxs-lookup"><span data-stu-id="bf03b-134">The [**SslComputeFinishedHash**](sslcomputefinishedhash.md) function is called with the hash handle to obtain the digest of the hashed data.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf03b-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="bf03b-135">Requirements</span></span>



| <span data-ttu-id="bf03b-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="bf03b-136">Requirement</span></span> | <span data-ttu-id="bf03b-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="bf03b-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf03b-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf03b-138">Minimum supported client</span></span><br/> | <span data-ttu-id="bf03b-139">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bf03b-139">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="bf03b-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="bf03b-140">Minimum supported server</span></span><br/> | <span data-ttu-id="bf03b-141">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="bf03b-141">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="bf03b-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="bf03b-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf03b-143"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf03b-143"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="bf03b-144">DLL</span><span class="sxs-lookup"><span data-stu-id="bf03b-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf03b-145"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf03b-145"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

