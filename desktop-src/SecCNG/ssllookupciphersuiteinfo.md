---
description: Récupère les informations de la suite de chiffrement pour un protocole spécifié, une suite de chiffrement et un ensemble de types de clés.
ms.assetid: ab995d9a-48fa-491a-95b1-d15c5b92f1da
title: SslLookupCipherSuiteInfo, fonction (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslLookupCipherSuiteInfo
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 7aff6c9e08351ce771669535a98ec817bfc4aaf5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869017"
---
# <a name="ssllookupciphersuiteinfo-function"></a><span data-ttu-id="c9863-103">SslLookupCipherSuiteInfo fonction)</span><span class="sxs-lookup"><span data-stu-id="c9863-103">SslLookupCipherSuiteInfo function</span></span>

<span data-ttu-id="c9863-104">La fonction **SslLookupCipherSuiteInfo** récupère les informations de la suite de chiffrement pour un protocole spécifié, une suite de chiffrement et un ensemble de types de clés.</span><span class="sxs-lookup"><span data-stu-id="c9863-104">The **SslLookupCipherSuiteInfo** function retrieves the cipher suite information for a specified protocol, cipher suite, and key type set.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9863-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c9863-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslLookupCipherSuiteInfo(
  _In_  NCRYPT_PROV_HANDLE      hSslProvider,
  _In_  DWORD                   dwProtocol,
  _In_  DWORD                   dwCipherSuite,
  _In_  DWORD                   dwKeyType,
  _Out_ NCRYPT_SSL_CIPHER_SUITE *pCipherSuite,
  _In_  DWORD                   dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="c9863-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c9863-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c9863-107">*hSslProvider* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c9863-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9863-108">Handle de l’instance du fournisseur de protocole du [*protocole SSL (Secure Sockets Layer)*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="c9863-108">The handle to the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="c9863-109">*dwProtocol* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c9863-109">*dwProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9863-110">L’une des valeurs d' [**identificateur de protocole du fournisseur SSL CNG**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="c9863-110">One of the [**CNG SSL Provider Protocol Identifier**](https://msdn.microsoft.com/library/Hh971257(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="c9863-111">*dwCipherSuite* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c9863-111">*dwCipherSuite* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9863-112">L’un des valeurs d' [**identificateurs de la suite de chiffrement du fournisseur SSL CNG**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="c9863-112">One of the [**CNG SSL Provider Cipher Suite Identifiers**](https://msdn.microsoft.com/library/Hh971253(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="c9863-113">*dwKeyType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c9863-113">*dwKeyType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9863-114">L’un des valeurs des [**identificateurs de type de clé du fournisseur SSL CNG**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) .</span><span class="sxs-lookup"><span data-stu-id="c9863-114">One of the [**CNG SSL Provider Key Type Identifiers**](https://msdn.microsoft.com/library/Hh971256(v=VS.85).aspx) values.</span></span>

</dd> <dt>

<span data-ttu-id="c9863-115">*pCipherSuite* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="c9863-115">*pCipherSuite* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c9863-116">Adresse d’une mémoire tampon qui contient une structure de [**\_ \_ \_ suite de chiffrement SSL NCRYPT**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_SUITE**) dans laquelle écrire les informations de la suite de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="c9863-116">The address of a buffer that contains a [**NCRYPT\_SSL\_CIPHER\_SUITE**](https://www.bing.com/search?q=**NCRYPT\_SSL\_CIPHER\_SUITE**) structure in which to write the cipher suite information.</span></span>

</dd> <dt>

<span data-ttu-id="c9863-117">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c9863-117">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c9863-118">Ce paramètre est réservé à un usage futur.</span><span class="sxs-lookup"><span data-stu-id="c9863-118">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c9863-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c9863-119">Return value</span></span>

<span data-ttu-id="c9863-120">Si la fonction est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="c9863-120">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="c9863-121">Si la fonction échoue, elle retourne une valeur d’erreur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="c9863-121">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="c9863-122">Les codes de retour possibles incluent, mais ne sont pas limités à, les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="c9863-122">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="c9863-123">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="c9863-123">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="c9863-124">Description</span><span class="sxs-lookup"><span data-stu-id="c9863-124">Description</span></span>                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="c9863-125"><dt>**NPD \_ \_Handle 0X80090026L non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="c9863-125"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="c9863-126">Le descripteur *hSslProvider* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="c9863-126">The *hSslProvider* handle is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="c9863-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c9863-127">Requirements</span></span>



| <span data-ttu-id="c9863-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c9863-128">Requirement</span></span> | <span data-ttu-id="c9863-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="c9863-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c9863-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9863-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c9863-131">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c9863-131">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c9863-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c9863-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c9863-133">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c9863-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c9863-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="c9863-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9863-135"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="c9863-135"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="c9863-136">DLL</span><span class="sxs-lookup"><span data-stu-id="c9863-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9863-137"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9863-137"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

