---
description: Signe un hachage à l’aide de la clé privée spécifiée.
ms.assetid: 25e8ebc5-278d-4d1f-977a-c2fab07b790a
title: SslSignHash, fonction (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslSignHash
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 339d0a27cb987557ff90cbd0f489813edb357b77
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484625"
---
# <a name="sslsignhash-function"></a><span data-ttu-id="5b4fb-103">SslSignHash fonction)</span><span class="sxs-lookup"><span data-stu-id="5b4fb-103">SslSignHash function</span></span>

<span data-ttu-id="5b4fb-104">La fonction **SslSignHash** signe un [*hachage*](/windows/desktop/SecGloss/h-gly) à l’aide de la [*clé privée*](/windows/desktop/SecGloss/p-gly)spécifiée.</span><span class="sxs-lookup"><span data-stu-id="5b4fb-104">The **SslSignHash** function signs a [*hash*](/windows/desktop/SecGloss/h-gly) by using the specified [*private key*](/windows/desktop/SecGloss/p-gly).</span></span> <span data-ttu-id="5b4fb-105">Le processus de signature est exécuté sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="5b4fb-105">The signing process is performed on the server.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b4fb-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5b4fb-106">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslSignHash(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  NCRYPT_KEY_HANDLE  hPrivateKey,
  _In_  PBYTE              pbHashValue,
  _In_  DWORD              cbHashValue,
  _Out_ PBYTE              pbSignature,
  _In_  DWORD              cbSignature,
  _Out_ DWORD              *pcbResult,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="5b4fb-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5b4fb-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b4fb-108">*hSslProvider* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5b4fb-108">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b4fb-109">Handle de l’instance du fournisseur de protocole du [*protocole SSL (Secure Sockets Layer)*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="5b4fb-109">The handle to the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="5b4fb-110">*hPrivateKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5b4fb-110">*hPrivateKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b4fb-111">Handle de la clé privée à utiliser pour signer le hachage.</span><span class="sxs-lookup"><span data-stu-id="5b4fb-111">The handle to the private key to use to sign the hash.</span></span>

</dd> <dt>

<span data-ttu-id="5b4fb-112">*pbHashValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5b4fb-112">*pbHashValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b4fb-113">Pointeur vers une mémoire tampon qui contient le hachage à signer.</span><span class="sxs-lookup"><span data-stu-id="5b4fb-113">A pointer to a buffer that contains the hash to sign.</span></span>

</dd> <dt>

<span data-ttu-id="5b4fb-114">*cbHashValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5b4fb-114">*cbHashValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b4fb-115">Taille, en octets, de la mémoire tampon *pbHashValue* .</span><span class="sxs-lookup"><span data-stu-id="5b4fb-115">The size, in bytes, of the *pbHashValue* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="5b4fb-116">*pbSignature* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5b4fb-116">*pbSignature* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5b4fb-117">Adresse d’une mémoire tampon qui reçoit la signature du hachage.</span><span class="sxs-lookup"><span data-stu-id="5b4fb-117">The address of a buffer that receives the signature of the hash.</span></span> <span data-ttu-id="5b4fb-118">Le paramètre *cbSignature* contient la taille de cette mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="5b4fb-118">The *cbSignature* parameter contains the size of this buffer.</span></span> <span data-ttu-id="5b4fb-119">Pour déterminer la taille de mémoire tampon requise, affectez la valeur **null** au paramètre *pbSignature* .</span><span class="sxs-lookup"><span data-stu-id="5b4fb-119">To determine the required sized size of the buffer, set the *pbSignature* parameter to **NULL**.</span></span> <span data-ttu-id="5b4fb-120">La taille requise de la mémoire tampon est retournée dans le paramètre *pcbResult* .</span><span class="sxs-lookup"><span data-stu-id="5b4fb-120">The required size of the buffer will be returned in the *pcbResult* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="5b4fb-121">*cbSignature* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5b4fb-121">*cbSignature* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b4fb-122">Taille, en octets, de la mémoire tampon *pbSignature* .</span><span class="sxs-lookup"><span data-stu-id="5b4fb-122">The size, in bytes, of the *pbSignature* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="5b4fb-123">*pcbResult* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5b4fb-123">*pcbResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5b4fb-124">Pointeur vers une valeur qui, une fois terminée, contient le nombre réel d’octets écrits dans la mémoire tampon *pbSignature* .</span><span class="sxs-lookup"><span data-stu-id="5b4fb-124">A pointer to a value that, upon completion, contains the actual number of bytes written to the *pbSignature* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="5b4fb-125">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5b4fb-125">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b4fb-126">Ce paramètre est réservé à un usage futur.</span><span class="sxs-lookup"><span data-stu-id="5b4fb-126">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b4fb-127">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5b4fb-127">Return value</span></span>

<span data-ttu-id="5b4fb-128">Si la fonction est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="5b4fb-128">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="5b4fb-129">Si la fonction échoue, elle retourne une valeur d’erreur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="5b4fb-129">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="5b4fb-130">Les codes de retour possibles incluent, mais ne sont pas limités à, les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="5b4fb-130">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="5b4fb-131">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="5b4fb-131">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="5b4fb-132">Description</span><span class="sxs-lookup"><span data-stu-id="5b4fb-132">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="5b4fb-133"><dt>**NPD \_ \_Handle 0X80090026L non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="5b4fb-133"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="5b4fb-134">L’un des handles fournis n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="5b4fb-134">One of the provided handles is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="5b4fb-135">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5b4fb-135">Requirements</span></span>



| <span data-ttu-id="5b4fb-136">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5b4fb-136">Requirement</span></span> | <span data-ttu-id="5b4fb-137">Valeur</span><span class="sxs-lookup"><span data-stu-id="5b4fb-137">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5b4fb-138">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5b4fb-138">Minimum supported client</span></span><br/> | <span data-ttu-id="5b4fb-139">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5b4fb-139">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="5b4fb-140">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5b4fb-140">Minimum supported server</span></span><br/> | <span data-ttu-id="5b4fb-141">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5b4fb-141">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="5b4fb-142">En-tête</span><span class="sxs-lookup"><span data-stu-id="5b4fb-142">Header</span></span><br/>                   | <dl> <span data-ttu-id="5b4fb-143"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="5b4fb-143"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="5b4fb-144">DLL</span><span class="sxs-lookup"><span data-stu-id="5b4fb-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b4fb-145"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b4fb-145"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

