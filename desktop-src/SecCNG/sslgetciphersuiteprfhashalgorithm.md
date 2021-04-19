---
description: 'Retourne l’identificateur d’algorithme CNG (Cryptography API : Next Generation) de l’algorithme de hachage utilisé pour la fonction Pseudo-aléatoire (PRF) TLS (Transport Layer Security Protocol) pour le protocole d’entrée, la suite de chiffrement et le type de clé.'
ms.assetid: 8d20b2da-390e-458e-b122-f5ef3722ad87
title: SslGetCipherSuitePRFHashAlgorithm, fonction (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGetCipherSuitePRFHashAlgorithm
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 452cb7b36b20697a95b2c2abae7d8cd3b4180050
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535718"
---
# <a name="sslgetciphersuiteprfhashalgorithm-function"></a><span data-ttu-id="5c772-103">SslGetCipherSuitePRFHashAlgorithm fonction)</span><span class="sxs-lookup"><span data-stu-id="5c772-103">SslGetCipherSuitePRFHashAlgorithm function</span></span>

<span data-ttu-id="5c772-104">La fonction **SslGetCipherSuitePRFHashAlgorithm** retourne l’identificateur d’ALGORITHMe CNG (Cryptography API : Next Generation) de l' [*algorithme de hachage*](/windows/desktop/SecGloss/h-gly) utilisé pour la [*fonction Pseudo-aléatoire*](/windows/desktop/SecGloss/p-gly) (PRF) TLS ( [*Transport Layer Security Protocol*](/windows/desktop/SecGloss/t-gly) ) pour le protocole d’entrée, la suite de chiffrement et le type de clé.</span><span class="sxs-lookup"><span data-stu-id="5c772-104">The **SslGetCipherSuitePRFHashAlgorithm** function returns the Cryptography API: Next Generation (CNG) Algorithm Identifier of the [*hashing algorithm*](/windows/desktop/SecGloss/h-gly) that is used for the [*Transport Layer Security protocol*](/windows/desktop/SecGloss/t-gly) (TLS) [*pseudo-random function*](/windows/desktop/SecGloss/p-gly) (PRF) for the input protocol, cipher suite, and key type.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c772-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="5c772-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslGetCipherSuitePRFHashAlgorithm(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _In_  DWORD              dwProtocol,
  _In_  DWORD              dwCipherSuite,
  _In_  DWORD              dwKeyType,
  _Out_ WCHAR              szPRFHash[NCRYPT_SSL_MAX_NAME_SIZE],
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="5c772-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="5c772-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5c772-107">*hSslProvider* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5c772-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c772-108">Handle de l’instance du fournisseur de protocole du [*protocole SSL (Secure Sockets Layer)*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="5c772-108">The handle of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="5c772-109">*dwProtocol* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5c772-109">*dwProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c772-110">L’une des valeurs d' [**identificateur de protocole du fournisseur SSL CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="5c772-110">One of the [**CNG SSL Provider Protocol Identifier**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="5c772-111">*dwCipherSuite* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5c772-111">*dwCipherSuite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c772-112">L’une des valeurs d’identificateur de la [**suite de chiffrement du fournisseur SSL CNG**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="5c772-112">One of the [**CNG SSL Provider Cipher Suite Identifier**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="5c772-113">*dwKeyType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5c772-113">*dwKeyType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c772-114">L’une des valeurs d' [**identificateur de type de clé du fournisseur SSL CNG**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="5c772-114">One of the [**CNG SSL Provider Key Type Identifier**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) values.</span></span> <span data-ttu-id="5c772-115">Pour les types de clés qui ne sont pas du [*chiffrement à courbe elliptique*](/windows/desktop/SecGloss/e-gly) (ECC), définissez ce paramètre sur zéro.</span><span class="sxs-lookup"><span data-stu-id="5c772-115">For key types that are not [*elliptic curve cryptography*](/windows/desktop/SecGloss/e-gly) (ECC), set this parameter to zero.</span></span>

</dd> <dt>

<span data-ttu-id="5c772-116">*szPRFHash* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="5c772-116">*szPRFHash* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5c772-117">Un des [**identificateurs d’algorithme CNG**](cng-algorithm-identifiers.md) pour le hachage qui sera utilisé pour le PRF TLS.</span><span class="sxs-lookup"><span data-stu-id="5c772-117">One of the [**CNG Algorithm Identifiers**](cng-algorithm-identifiers.md) for the hash that will be used for the TLS PRF.</span></span>

</dd> <dt>

<span data-ttu-id="5c772-118">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="5c772-118">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5c772-119">Ce paramètre est réservé pour une utilisation ultérieure et doit être défini à zéro.</span><span class="sxs-lookup"><span data-stu-id="5c772-119">This parameter is reserved for future use and must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5c772-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="5c772-120">Return value</span></span>

<span data-ttu-id="5c772-121">Si la fonction est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="5c772-121">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="5c772-122">Si la fonction échoue, elle retourne une valeur d’erreur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="5c772-122">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="5c772-123">Les codes de retour possibles incluent, mais ne sont pas limités à, les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="5c772-123">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="5c772-124">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="5c772-124">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="5c772-125">Description</span><span class="sxs-lookup"><span data-stu-id="5c772-125">Description</span></span>                                                                                  |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5c772-126"><dt>**NPD \_ \_Handle 0X80090026L non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="5c772-126"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="5c772-127">Le paramètre *hSslProvider* contient un pointeur qui n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="5c772-127">The *hSslProvider* parameter contains a pointer that is not valid.</span></span><br/>                |
| <dl> <span data-ttu-id="5c772-128"><dt>**NPD \_ \_Paramètre 0X80090027L non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="5c772-128"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="5c772-129">Le paramètre *szPRFHash* a la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="5c772-129">The *szPRFHash* parameter is set to **NULL**.</span></span><br/>                                     |
| <dl> <span data-ttu-id="5c772-130"><dt>**NPD \_ 0x80090029L non \_ pris en charge**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="5c772-130"><dt>**NTE\_NOT\_SUPPORTED**</dt> <dt>0x80090029L</dt></span></span> </dl>     | <span data-ttu-id="5c772-131">La fonction sélectionnée n’est pas prise en charge dans la version spécifiée de l’interface.</span><span class="sxs-lookup"><span data-stu-id="5c772-131">The selected function is not supported in the specified version of the interface.</span></span><br/> |
| <dl> <span data-ttu-id="5c772-132"><dt>**NPD \_ \_Indicateurs INcorrects**</dt> <dt>0x80090009L</dt></span><span class="sxs-lookup"><span data-stu-id="5c772-132"><dt>**NTE\_BAD\_FLAGS**</dt> <dt>0x80090009L</dt></span></span> </dl>         | <span data-ttu-id="5c772-133">Le paramètre *dwFlags* doit avoir la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="5c772-133">The *dwFlags* parameter must be set to zero.</span></span><br/>                                      |



 

## <a name="remarks"></a><span data-ttu-id="5c772-134">Notes</span><span class="sxs-lookup"><span data-stu-id="5c772-134">Remarks</span></span>

<span data-ttu-id="5c772-135">Cette fonction **SslGetCipherSuitePRFHashAlgorithm** est appelée pour les conversations TLS 1,2 ou ultérieures pour interroger l’algorithme de hachage qui sera utilisé dans le PRF TLS.</span><span class="sxs-lookup"><span data-stu-id="5c772-135">This **SslGetCipherSuitePRFHashAlgorithm** function is called for TLS 1.2 or later conversations to query the hashing algorithm that will be used in the TLS PRF.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c772-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5c772-136">Requirements</span></span>



| <span data-ttu-id="5c772-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5c772-137">Requirement</span></span> | <span data-ttu-id="5c772-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="5c772-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c772-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5c772-139">Minimum supported client</span></span><br/> | <span data-ttu-id="5c772-140">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5c772-140">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="5c772-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="5c772-141">Minimum supported server</span></span><br/> | <span data-ttu-id="5c772-142">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="5c772-142">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="5c772-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="5c772-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="5c772-144"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="5c772-144"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="5c772-145">DLL</span><span class="sxs-lookup"><span data-stu-id="5c772-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c772-146"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c772-146"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

