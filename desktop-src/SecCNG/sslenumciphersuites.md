---
description: Énumère les suites de chiffrement prises en charge par un fournisseur de protocole de protocole SSL (Secure Sockets Layer) (SSL).
ms.assetid: c12bc422-71c9-44f4-abf7-76902b19d3bd
title: SslEnumCipherSuites, fonction (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslEnumCipherSuites
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 8991842f38f3d3dc3d721cd30ebfb857ad20308a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318993"
---
# <a name="sslenumciphersuites-function"></a><span data-ttu-id="258e7-103">SslEnumCipherSuites fonction)</span><span class="sxs-lookup"><span data-stu-id="258e7-103">SslEnumCipherSuites function</span></span>

<span data-ttu-id="258e7-104">La fonction **SslEnumCipherSuites** énumère les suites de chiffrement prises en charge par un fournisseur de protocole de [*protocole SSL (Secure Sockets Layer)*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="258e7-104">The **SslEnumCipherSuites** function enumerates the cipher suites supported by a [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="258e7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="258e7-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslEnumCipherSuites(
  _In_     NCRYPT_PROV_HANDLE      hSslProvider,
  _In_opt_ NCRYPT_KEY_HANDLE       hPrivateKey,
  _Out_    NCRYPT_SSL_CIPHER_SUITE **ppCipherSuite,
  _Inout_  PVOID                   *ppEnumState,
  _In_     DWORD                   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="258e7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="258e7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="258e7-107">*hSslProvider* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="258e7-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="258e7-108">Handle de l’instance du fournisseur de protocole SSL.</span><span class="sxs-lookup"><span data-stu-id="258e7-108">The handle of the SSL protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="258e7-109">*hPrivateKey* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="258e7-109">*hPrivateKey* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="258e7-110">Handle d’une [*clé privée*](/windows/desktop/SecGloss/p-gly).</span><span class="sxs-lookup"><span data-stu-id="258e7-110">The handle of a [*private key*](/windows/desktop/SecGloss/p-gly).</span></span> <span data-ttu-id="258e7-111">Lorsqu’une clé privée est spécifiée, **SslEnumCipherSuites** énumère les suites de chiffrement qui sont compatibles avec la clé privée.</span><span class="sxs-lookup"><span data-stu-id="258e7-111">When a private key is specified, **SslEnumCipherSuites** enumerates the cipher suites that are compatible with the private key.</span></span> <span data-ttu-id="258e7-112">Par exemple, si la clé privée est une clé DSS, seules les suites de \_ chiffrement DSS dhe sont retournées.</span><span class="sxs-lookup"><span data-stu-id="258e7-112">For example, if the private key is a DSS key, then only the DSS\_DHE cipher suites are returned.</span></span> <span data-ttu-id="258e7-113">Si la clé privée est une clé RSA, mais ne prend pas en charge les opérations de déchiffrement brut, les suites de chiffrement SSL2 ne sont pas retournées.</span><span class="sxs-lookup"><span data-stu-id="258e7-113">If the private key is an RSA key, but it does not support raw decryption operations, then the SSL2 cipher suites are not returned.</span></span>

<span data-ttu-id="258e7-114">Affectez la valeur **null** à ce paramètre lorsque vous ne spécifiez pas de clé privée.</span><span class="sxs-lookup"><span data-stu-id="258e7-114">Set this parameter to **NULL** when you are not specifying a private key.</span></span>

> [!Note]  
> <span data-ttu-id="258e7-115">Un descripteur *hPrivateKey* est obtenu en appelant la fonction [**SslOpenPrivateKey**](sslopenprivatekey.md) .</span><span class="sxs-lookup"><span data-stu-id="258e7-115">A *hPrivateKey* handle is obtained by calling the [**SslOpenPrivateKey**](sslopenprivatekey.md) function.</span></span> <span data-ttu-id="258e7-116">Les handles obtenus à partir de la fonction [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) ne sont pas pris en charge.</span><span class="sxs-lookup"><span data-stu-id="258e7-116">Handles obtained from the [**NCryptOpenKey**](/windows/desktop/api/Ncrypt/nf-ncrypt-ncryptopenkey) function are not supported.</span></span>

 

</dd> <dt>

<span data-ttu-id="258e7-117">*ppCipherSuite* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="258e7-117">*ppCipherSuite* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="258e7-118">Pointeur vers une structure [**de \_ \_ \_ suite de chiffrement SSL NCRYPT**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_SUITE**) pour recevoir l’adresse de la suite de chiffrement suivante dans la liste.</span><span class="sxs-lookup"><span data-stu-id="258e7-118">A pointer to a [**NCRYPT\_SSL\_CIPHER\_SUITE**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_SUITE**) structure to receive the address of the next cipher suite in the list.</span></span>

</dd> <dt>

<span data-ttu-id="258e7-119">*ppEnumState* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="258e7-119">*ppEnumState* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="258e7-120">Pointeur vers une mémoire tampon qui indique la position actuelle dans la liste de suites de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="258e7-120">A pointer to a buffer that indicates the current position in the list of cipher suites.</span></span>

<span data-ttu-id="258e7-121">Affectez au pointeur la **valeur null** lors du premier appel à **SslEnumCipherSuites**.</span><span class="sxs-lookup"><span data-stu-id="258e7-121">Set the pointer to **NULL** on the first call to **SslEnumCipherSuites**.</span></span> <span data-ttu-id="258e7-122">À chaque appel suivant, repassez la valeur non modifiée à **SslEnumCipherSuites**.</span><span class="sxs-lookup"><span data-stu-id="258e7-122">On each subsequent call, pass the unmodified value back to **SslEnumCipherSuites**.</span></span>

<span data-ttu-id="258e7-123">Lorsqu’il n’y a plus de suites de chiffrement disponibles, vous devez libérer *ppEnumState* en appelant la fonction [**SslFreeBuffer**](sslfreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="258e7-123">When there are no more cipher suites available, you should free *ppEnumState* by calling the [**SslFreeBuffer**](sslfreebuffer.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="258e7-124">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="258e7-124">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="258e7-125">Ce paramètre est réservé à un usage futur.</span><span class="sxs-lookup"><span data-stu-id="258e7-125">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="258e7-126">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="258e7-126">Return value</span></span>

<span data-ttu-id="258e7-127">Si la fonction est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="258e7-127">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="258e7-128">Si la fonction échoue, elle retourne une valeur d’erreur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="258e7-128">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="258e7-129">Les codes de retour possibles incluent, mais ne sont pas limités à, les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="258e7-129">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="258e7-130">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="258e7-130">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="258e7-131">Description</span><span class="sxs-lookup"><span data-stu-id="258e7-131">Description</span></span>                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="258e7-132"><dt>**NPD \_ AUCUNE \_ mémoire**</dt> <dt>0x8009000EL</dt></span><span class="sxs-lookup"><span data-stu-id="258e7-132"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>      | <span data-ttu-id="258e7-133">La mémoire disponible est insuffisante pour allouer les tampons nécessaires.</span><span class="sxs-lookup"><span data-stu-id="258e7-133">Not enough memory is available to allocate necessary buffers.</span></span><br/> |
| <dl> <span data-ttu-id="258e7-134"><dt>**NPD \_ \_Handle 0X80090026L non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="258e7-134"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="258e7-135">L’un des handles fournis n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="258e7-135">One of the provided handles is not valid.</span></span><br/>                     |
| <dl> <span data-ttu-id="258e7-136"><dt>**NPD \_ AUCUN \_ autre \_ élément**</dt> <dt>0x8009002AL</dt></span><span class="sxs-lookup"><span data-stu-id="258e7-136"><dt>**NTE\_NO\_MORE\_ITEMS**</dt> <dt>0x8009002AL</dt></span></span> </dl> | <span data-ttu-id="258e7-137">Aucune suite de chiffrement supplémentaire n’est prise en charge.</span><span class="sxs-lookup"><span data-stu-id="258e7-137">No additional cipher suites are supported.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="258e7-138">Notes</span><span class="sxs-lookup"><span data-stu-id="258e7-138">Remarks</span></span>

<span data-ttu-id="258e7-139">Pour énumérer toutes les suites de chiffrement prises en charge par le fournisseur SSL, appelez la fonction **SslEnumCipherSuites** dans une boucle jusqu’à **NPD, \_ aucun \_ autre \_ élément** n’est retourné.</span><span class="sxs-lookup"><span data-stu-id="258e7-139">To enumerate all cipher suites supported by the SSL provider, call the **SslEnumCipherSuites** function in a loop until **NTE\_NO\_MORE\_ITEMS** is returned.</span></span>

## <a name="requirements"></a><span data-ttu-id="258e7-140">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="258e7-140">Requirements</span></span>



| <span data-ttu-id="258e7-141">Condition requise</span><span class="sxs-lookup"><span data-stu-id="258e7-141">Requirement</span></span> | <span data-ttu-id="258e7-142">Valeur</span><span class="sxs-lookup"><span data-stu-id="258e7-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="258e7-143">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="258e7-143">Minimum supported client</span></span><br/> | <span data-ttu-id="258e7-144">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="258e7-144">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="258e7-145">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="258e7-145">Minimum supported server</span></span><br/> | <span data-ttu-id="258e7-146">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="258e7-146">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="258e7-147">En-tête</span><span class="sxs-lookup"><span data-stu-id="258e7-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="258e7-148"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="258e7-148"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="258e7-149">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="258e7-149">Library</span></span><br/>                  | <dl> <span data-ttu-id="258e7-150"><dt>Ncrypt. lib</dt></span><span class="sxs-lookup"><span data-stu-id="258e7-150"><dt>Ncrypt.lib</dt></span></span> </dl>    |
| <span data-ttu-id="258e7-151">DLL</span><span class="sxs-lookup"><span data-stu-id="258e7-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="258e7-152"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="258e7-152"><dt>Ncrypt.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="258e7-153">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="258e7-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="258e7-154">**\_suite de \_ chiffrement SSL NCRYPT \_**</span><span class="sxs-lookup"><span data-stu-id="258e7-154">**NCRYPT\_SSL\_CIPHER\_SUITE**</span></span>](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_SUITE**)
</dt> </dl>

 

