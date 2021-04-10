---
description: Retourne une \_ \_ \_ structure de longueurs de chiffrement SSL NCRYPT qui contient les longueurs d’en-tête et de code de fin du protocole d’entrée, de la suite de chiffrement et du type de clé.
ms.assetid: 44d0d803-16d7-4bdf-9638-afbdaf9e1802
title: SslLookupCipherLengths, fonction (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslLookupCipherLengths
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: e756fb84d47ed877ffe4afcd54ce93c53a768e69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951629"
---
# <a name="ssllookupcipherlengths-function"></a><span data-ttu-id="a2ee0-103">SslLookupCipherLengths fonction)</span><span class="sxs-lookup"><span data-stu-id="a2ee0-103">SslLookupCipherLengths function</span></span>

<span data-ttu-id="a2ee0-104">La fonction **SslLookupCipherLengths** retourne une structure de [**\_ \_ \_ longueurs de chiffrement SSL NCRYPT**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_LENGTHS**) qui contient les longueurs d’en-tête et de code de fin du protocole d’entrée, de la suite de chiffrement et du type de clé.</span><span class="sxs-lookup"><span data-stu-id="a2ee0-104">The **SslLookupCipherLengths** function returns an [**NCRYPT\_SSL\_CIPHER\_LENGTHS**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_LENGTHS**) structure that contains the header and trailer lengths of the input protocol, cipher suite, and key type.</span></span>

## <a name="syntax"></a><span data-ttu-id="a2ee0-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a2ee0-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslLookupCipherLengths(
  _In_  NCRYPT_PROV_HANDLE        hSslProvider,
  _In_  DWORD                     dwProtocol,
  _In_  DWORD                     dwCipherSuite,
  _In_  DWORD                     dwKeyType,
  _Out_ NCRYPT_SSL_CIPHER_LENGTHS *pCipherLengths,
  _In_  DWORD                     cbCipherLengths,
  _In_  DWORD                     dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="a2ee0-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a2ee0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a2ee0-107">*hSslProvider* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a2ee0-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2ee0-108">Handle de l’instance du fournisseur de protocole du [*protocole SSL (Secure Sockets Layer)*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="a2ee0-108">The handle of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="a2ee0-109">*dwProtocol* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a2ee0-109">*dwProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2ee0-110">L’une des valeurs d' [**identificateur de protocole du fournisseur SSL CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="a2ee0-110">One of the [**CNG SSL Provider Protocol Identifier**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="a2ee0-111">*dwCipherSuite* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a2ee0-111">*dwCipherSuite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2ee0-112">L’une des valeurs d’identificateur de la [**suite de chiffrement du fournisseur SSL CNG**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="a2ee0-112">One of the [**CNG SSL Provider Cipher Suite Identifier**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="a2ee0-113">*dwKeyType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a2ee0-113">*dwKeyType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2ee0-114">L’une des valeurs d' [**identificateur de type de clé du fournisseur SSL CNG**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="a2ee0-114">One of the [**CNG SSL Provider Key Type Identifier**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) values.</span></span> <span data-ttu-id="a2ee0-115">Pour les types de clés qui ne sont pas du [*chiffrement à courbe elliptique*](/windows/desktop/SecGloss/e-gly) (ECC), définissez ce paramètre sur zéro.</span><span class="sxs-lookup"><span data-stu-id="a2ee0-115">For key types that are not [*elliptic curve cryptography*](/windows/desktop/SecGloss/e-gly) (ECC), set this parameter to zero.</span></span>

</dd> <dt>

<span data-ttu-id="a2ee0-116">*pCipherLengths* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a2ee0-116">*pCipherLengths* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a2ee0-117">Pointeur vers une mémoire tampon destinée à recevoir la structure des [**\_ \_ \_ longueurs de chiffrement SSL NCRYPT**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_LENGTHS**) .</span><span class="sxs-lookup"><span data-stu-id="a2ee0-117">A pointer to a buffer to receive the [**NCRYPT\_SSL\_CIPHER\_LENGTHS**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_LENGTHS**) structure.</span></span>

</dd> <dt>

<span data-ttu-id="a2ee0-118">*cbCipherLengths* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a2ee0-118">*cbCipherLengths* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2ee0-119">Longueur, en octets, de la mémoire tampon vers laquelle pointe le paramètre *pCipherLengths* .</span><span class="sxs-lookup"><span data-stu-id="a2ee0-119">The length, in bytes, of the buffer pointed to by the *pCipherLengths* parameter.</span></span>

</dd> <dt>

<span data-ttu-id="a2ee0-120">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a2ee0-120">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a2ee0-121">Ce paramètre est réservé pour une utilisation ultérieure et doit être défini à zéro.</span><span class="sxs-lookup"><span data-stu-id="a2ee0-121">This parameter is reserved for future use and must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a2ee0-122">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a2ee0-122">Return value</span></span>

<span data-ttu-id="a2ee0-123">Si la fonction est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="a2ee0-123">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="a2ee0-124">Si la fonction échoue, elle retourne une valeur d’erreur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="a2ee0-124">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="a2ee0-125">Les codes de retour possibles incluent, mais ne sont pas limités à, les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="a2ee0-125">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="a2ee0-126">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="a2ee0-126">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="a2ee0-127">Description</span><span class="sxs-lookup"><span data-stu-id="a2ee0-127">Description</span></span>                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a2ee0-128"><dt>**NPD \_ \_Handle 0X80090026L non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="a2ee0-128"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="a2ee0-129">Le paramètre *hSslProvider* contient un pointeur qui n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="a2ee0-129">The *hSslProvider* parameter contains a pointer that is not valid.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="a2ee0-130"><dt>**NPD \_ \_Paramètre 0X80090027L non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="a2ee0-130"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="a2ee0-131">Le paramètre *pCipherLengths* a la valeur **null** ou la longueur de la mémoire tampon spécifiée par le *cbCipherLengths* est trop petite.</span><span class="sxs-lookup"><span data-stu-id="a2ee0-131">The *pCipherLengths* parameter is set to **NULL** or the buffer length specified by the *cbCipherLengths* is too short.</span></span><br/> |
| <dl> <span data-ttu-id="a2ee0-132"><dt>**NPD \_ \_Indicateurs INcorrects**</dt> <dt>0x80090009L</dt></span><span class="sxs-lookup"><span data-stu-id="a2ee0-132"><dt>**NTE\_BAD\_FLAGS**</dt> <dt>0x80090009L</dt></span></span> </dl>         | <span data-ttu-id="a2ee0-133">Le paramètre *dwFlags* doit avoir la valeur zéro.</span><span class="sxs-lookup"><span data-stu-id="a2ee0-133">The *dwFlags* parameter must be set to zero.</span></span><br/>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="a2ee0-134">Notes</span><span class="sxs-lookup"><span data-stu-id="a2ee0-134">Remarks</span></span>

<span data-ttu-id="a2ee0-135">La fonction **SslLookupCipherLengths** est appelée pour les conversations TLS ( [*Transport Layer Security Protocol*](/windows/desktop/SecGloss/t-gly) ) 1,1 ou ultérieures pour interroger les longueurs d’en-tête et de code de fin pour le protocole, la suite de chiffrement et le type de clé demandés.</span><span class="sxs-lookup"><span data-stu-id="a2ee0-135">The **SslLookupCipherLengths** function is called for [*Transport Layer Security protocol*](/windows/desktop/SecGloss/t-gly) (TLS) 1.1 or later conversations to query the header and trailer lengths for the requested protocol, cipher suite, and key type.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2ee0-136">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a2ee0-136">Requirements</span></span>



| <span data-ttu-id="a2ee0-137">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a2ee0-137">Requirement</span></span> | <span data-ttu-id="a2ee0-138">Valeur</span><span class="sxs-lookup"><span data-stu-id="a2ee0-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2ee0-139">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a2ee0-139">Minimum supported client</span></span><br/> | <span data-ttu-id="a2ee0-140">Applications de \[ Bureau Windows 7 uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a2ee0-140">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="a2ee0-141">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a2ee0-141">Minimum supported server</span></span><br/> | <span data-ttu-id="a2ee0-142">Applications de bureau Windows Server 2008 R2 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a2ee0-142">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a2ee0-143">En-tête</span><span class="sxs-lookup"><span data-stu-id="a2ee0-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="a2ee0-144"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="a2ee0-144"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="a2ee0-145">DLL</span><span class="sxs-lookup"><span data-stu-id="a2ee0-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a2ee0-146"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a2ee0-146"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

