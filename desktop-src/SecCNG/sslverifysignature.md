---
description: Vérifie la signature spécifiée à l’aide du hachage et de la clé publique fournis.
ms.assetid: fa274851-15f2-4be0-9e2f-4cdced36daff
title: SslVerifySignature, fonction (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslVerifySignature
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: cb2a50a7f16062f271a89b6061e3f2fa2dd16685
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862322"
---
# <a name="sslverifysignature-function"></a><span data-ttu-id="ce3a0-103">SslVerifySignature fonction)</span><span class="sxs-lookup"><span data-stu-id="ce3a0-103">SslVerifySignature function</span></span>

<span data-ttu-id="ce3a0-104">La fonction **SslVerifySignature** vérifie la signature spécifiée à l’aide du [*hachage*](/windows/desktop/SecGloss/h-gly) fourni et de la [*clé publique*](/windows/desktop/SecGloss/p-gly).</span><span class="sxs-lookup"><span data-stu-id="ce3a0-104">The **SslVerifySignature** function verifies the specified signature by using the supplied [*hash*](/windows/desktop/SecGloss/h-gly) and the [*public key*](/windows/desktop/SecGloss/p-gly).</span></span>

## <a name="syntax"></a><span data-ttu-id="ce3a0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ce3a0-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslVerifySignature(
  _In_ NCRYPT_PROV_HANDLE hSslProvider,
  _In_ NCRYPT_KEY_HANDLE  hPublicKey,
  _In_ PBYTE              pbHashValue,
  _In_ DWORD              cbHashValue,
  _In_ PBYTE              pbSignature,
  _In_ DWORD              cbSignature,
  _In_ DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="ce3a0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ce3a0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce3a0-107">*hSslProvider* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ce3a0-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce3a0-108">Handle de l’instance du fournisseur de protocole du [*protocole SSL (Secure Sockets Layer)*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="ce3a0-108">The handle to the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="ce3a0-109">*hPublicKey* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ce3a0-109">*hPublicKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce3a0-110">Handle de la clé publique.</span><span class="sxs-lookup"><span data-stu-id="ce3a0-110">The handle to the public key.</span></span>

</dd> <dt>

<span data-ttu-id="ce3a0-111">*pbHashValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ce3a0-111">*pbHashValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce3a0-112">Pointeur vers une mémoire tampon qui contient le hachage à utiliser pour vérifier la signature.</span><span class="sxs-lookup"><span data-stu-id="ce3a0-112">A pointer to a buffer that contains the hash to use to verify the signature.</span></span>

</dd> <dt>

<span data-ttu-id="ce3a0-113">*cbHashValue* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ce3a0-113">*cbHashValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce3a0-114">Taille, en octets, de la mémoire tampon *pbHashValue* .</span><span class="sxs-lookup"><span data-stu-id="ce3a0-114">The size, in bytes, of the *pbHashValue* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="ce3a0-115">*pbSignature* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ce3a0-115">*pbSignature* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce3a0-116">Pointeur vers une mémoire tampon qui contient la signature à vérifier.</span><span class="sxs-lookup"><span data-stu-id="ce3a0-116">A pointer to a buffer that contains the signature to verify.</span></span>

</dd> <dt>

<span data-ttu-id="ce3a0-117">*cbSignature* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ce3a0-117">*cbSignature* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce3a0-118">Taille, en octets, de la mémoire tampon *pbSignature* .</span><span class="sxs-lookup"><span data-stu-id="ce3a0-118">The size, in bytes, of the *pbSignature* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="ce3a0-119">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ce3a0-119">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce3a0-120">Ce paramètre est réservé à un usage futur.</span><span class="sxs-lookup"><span data-stu-id="ce3a0-120">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce3a0-121">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ce3a0-121">Return value</span></span>

<span data-ttu-id="ce3a0-122">Si la fonction est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="ce3a0-122">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="ce3a0-123">Si la fonction échoue, elle retourne une valeur d’erreur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="ce3a0-123">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="ce3a0-124">Les codes de retour possibles incluent, mais ne sont pas limités à, les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="ce3a0-124">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="ce3a0-125">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="ce3a0-125">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="ce3a0-126">Description</span><span class="sxs-lookup"><span data-stu-id="ce3a0-126">Description</span></span>                                          |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <span data-ttu-id="ce3a0-127"><dt>**NPD \_ \_Handle 0X80090026L non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="ce3a0-127"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="ce3a0-128">L’un des handles fournis n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="ce3a0-128">One of the provided handles is not valid.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="ce3a0-129">Notes</span><span class="sxs-lookup"><span data-stu-id="ce3a0-129">Remarks</span></span>

<span data-ttu-id="ce3a0-130">La fonction **SslVerifySignature** n’est pas appelée actuellement par Windows.</span><span class="sxs-lookup"><span data-stu-id="ce3a0-130">The **SslVerifySignature** function is not currently called by Windows.</span></span> <span data-ttu-id="ce3a0-131">Cette fonction est une partie obligatoire de l’interface du fournisseur SSL et doit être entièrement implémentée pour garantir la compatibilité ascendante.</span><span class="sxs-lookup"><span data-stu-id="ce3a0-131">This function is a required part of the SSL Provider interface and should be fully implemented to ensure forward compatibility.</span></span>

<span data-ttu-id="ce3a0-132">Les implémentations actuelles du côté serveur de la connexion TLS ( [*Transport Layer Security Protocol*](/windows/desktop/SecGloss/t-gly) ) appellent la fonction [**NCryptVerifySignature**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptverifysignature) lors de l’authentification du client pour traiter le message de vérification du certificat.</span><span class="sxs-lookup"><span data-stu-id="ce3a0-132">Current implementations of the server side of the [*Transport Layer Security protocol*](/windows/desktop/SecGloss/t-gly) (TLS) connection call the [**NCryptVerifySignature**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptverifysignature) function during the client authentication to process the certificate verify message.</span></span>

## <a name="requirements"></a><span data-ttu-id="ce3a0-133">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ce3a0-133">Requirements</span></span>



| <span data-ttu-id="ce3a0-134">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ce3a0-134">Requirement</span></span> | <span data-ttu-id="ce3a0-135">Valeur</span><span class="sxs-lookup"><span data-stu-id="ce3a0-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce3a0-136">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ce3a0-136">Minimum supported client</span></span><br/> | <span data-ttu-id="ce3a0-137">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ce3a0-137">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ce3a0-138">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ce3a0-138">Minimum supported server</span></span><br/> | <span data-ttu-id="ce3a0-139">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ce3a0-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ce3a0-140">En-tête</span><span class="sxs-lookup"><span data-stu-id="ce3a0-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce3a0-141"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="ce3a0-141"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="ce3a0-142">DLL</span><span class="sxs-lookup"><span data-stu-id="ce3a0-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ce3a0-143"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ce3a0-143"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

