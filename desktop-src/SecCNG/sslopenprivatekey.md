---
description: Ouvre un handle vers une clé privée.
ms.assetid: 2406be2c-121c-4475-b193-d370a88641da
title: SslOpenPrivateKey, fonction (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslOpenPrivateKey
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 6fd5c10ce6385e377c72d21f4557d27d2345737d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112687"
---
# <a name="sslopenprivatekey-function"></a><span data-ttu-id="7bbe1-103">SslOpenPrivateKey fonction)</span><span class="sxs-lookup"><span data-stu-id="7bbe1-103">SslOpenPrivateKey function</span></span>

<span data-ttu-id="7bbe1-104">La fonction **SslOpenPrivateKey** ouvre un handle vers une [*clé privée*](/windows/desktop/SecGloss/p-gly).</span><span class="sxs-lookup"><span data-stu-id="7bbe1-104">The **SslOpenPrivateKey** function opens a handle to a [*private key*](/windows/desktop/SecGloss/p-gly).</span></span>

## <a name="syntax"></a><span data-ttu-id="7bbe1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7bbe1-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslOpenPrivateKey(
  _In_  NCRYPT_PROV_HANDLE hSslProvider,
  _Out_ NCRYPT_KEY_HANDLE  *phPrivateKey,
  _In_  PCCERT_CONTEXT     pCertContext,
  _In_  DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="7bbe1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7bbe1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7bbe1-107">*hSslProvider* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7bbe1-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7bbe1-108">Handle de l’instance du fournisseur de protocole du [*protocole SSL (Secure Sockets Layer)*](/windows/desktop/SecGloss/s-gly) (SSL).</span><span class="sxs-lookup"><span data-stu-id="7bbe1-108">The handle to the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) protocol provider instance.</span></span>

</dd> <dt>

<span data-ttu-id="7bbe1-109">*phPrivateKey* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7bbe1-109">*phPrivateKey* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7bbe1-110">Adresse d’une mémoire tampon dans laquelle écrire le descripteur de la clé privée.</span><span class="sxs-lookup"><span data-stu-id="7bbe1-110">The address of a buffer in which to write the handle to the private key.</span></span>

<span data-ttu-id="7bbe1-111">Lorsque vous avez fini d’utiliser la clé, vous devez libérer *phPrivateKey* en appelant la fonction [**SslFreeObject**](sslfreeobject.md) .</span><span class="sxs-lookup"><span data-stu-id="7bbe1-111">When you have finished using the key, you should free *phPrivateKey* by calling the [**SslFreeObject**](sslfreeobject.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="7bbe1-112">*pCertContext* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7bbe1-112">*pCertContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7bbe1-113">Adresse du certificat à partir duquel obtenir la clé privée.</span><span class="sxs-lookup"><span data-stu-id="7bbe1-113">The address of the certificate from which to obtain the private key.</span></span>

</dd> <dt>

<span data-ttu-id="7bbe1-114">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7bbe1-114">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7bbe1-115">Ce paramètre est réservé à un usage futur.</span><span class="sxs-lookup"><span data-stu-id="7bbe1-115">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7bbe1-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7bbe1-116">Return value</span></span>

<span data-ttu-id="7bbe1-117">Si la fonction est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="7bbe1-117">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="7bbe1-118">Si la fonction échoue, elle retourne une valeur d’erreur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="7bbe1-118">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="7bbe1-119">Les codes de retour possibles incluent, mais ne sont pas limités à, les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="7bbe1-119">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="7bbe1-120">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="7bbe1-120">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="7bbe1-121">Description</span><span class="sxs-lookup"><span data-stu-id="7bbe1-121">Description</span></span>                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7bbe1-122"><dt>**NPD \_ AUCUNE \_ mémoire**</dt> <dt>0x8009000EL</dt></span><span class="sxs-lookup"><span data-stu-id="7bbe1-122"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="7bbe1-123">La mémoire disponible est insuffisante pour allouer les tampons nécessaires.</span><span class="sxs-lookup"><span data-stu-id="7bbe1-123">Not enough memory is available to allocate necessary buffers.</span></span><br/> |
| <dl> <span data-ttu-id="7bbe1-124"><dt>**NPD \_ \_Handle 0X80090026L non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="7bbe1-124"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="7bbe1-125">Le descripteur *hSslProvider* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="7bbe1-125">The *hSslProvider* handle is not valid.</span></span><br/>                       |
| <dl> <span data-ttu-id="7bbe1-126"><dt>**NPD \_ \_Paramètre 0X80090027L non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="7bbe1-126"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="7bbe1-127">Le paramètre *phPrivateKey* ou *PCertContext* a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="7bbe1-127">The *phPrivateKey* or *pCertContext* parameter is **NULL**.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="7bbe1-128">Notes</span><span class="sxs-lookup"><span data-stu-id="7bbe1-128">Remarks</span></span>

<span data-ttu-id="7bbe1-129">La clé privée obtenue fait partie d’une [*paire de clés publique/privée*](/windows/desktop/SecGloss/p-gly) au sein d’un [*certificat*](/windows/desktop/SecGloss/c-gly).</span><span class="sxs-lookup"><span data-stu-id="7bbe1-129">The private key obtained is part of a [*public/private key pair*](/windows/desktop/SecGloss/p-gly) within a [*certificate*](/windows/desktop/SecGloss/c-gly).</span></span> <span data-ttu-id="7bbe1-130">Cette fonction extrait simplement la clé privée du certificat spécifié par le paramètre *pCertContext* .</span><span class="sxs-lookup"><span data-stu-id="7bbe1-130">This function merely extracts the private key from the certificate specified by the *pCertContext* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="7bbe1-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7bbe1-131">Requirements</span></span>



| <span data-ttu-id="7bbe1-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7bbe1-132">Requirement</span></span> | <span data-ttu-id="7bbe1-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="7bbe1-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bbe1-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7bbe1-134">Minimum supported client</span></span><br/> | <span data-ttu-id="7bbe1-135">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7bbe1-135">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="7bbe1-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7bbe1-136">Minimum supported server</span></span><br/> | <span data-ttu-id="7bbe1-137">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7bbe1-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="7bbe1-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="7bbe1-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="7bbe1-139"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="7bbe1-139"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="7bbe1-140">DLL</span><span class="sxs-lookup"><span data-stu-id="7bbe1-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7bbe1-141"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7bbe1-141"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

