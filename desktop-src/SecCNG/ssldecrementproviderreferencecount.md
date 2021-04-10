---
description: Décrémente les références au fournisseur SSL (SSL (Secure Sockets Layer) Protocol).
ms.assetid: 67bfa4b5-c02c-4a76-871d-93f3bf4e3602
title: SslDecrementProviderReferenceCount, fonction (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslDecrementProviderReferenceCount
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 4d3fe072c02f22b713115dd5191b0b5e0cedbb37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951680"
---
# <a name="ssldecrementproviderreferencecount-function"></a><span data-ttu-id="6d40d-103">SslDecrementProviderReferenceCount fonction)</span><span class="sxs-lookup"><span data-stu-id="6d40d-103">SslDecrementProviderReferenceCount function</span></span>

<span data-ttu-id="6d40d-104">La fonction **SslDecrementProviderReferenceCount** décrémente les références au fournisseur SSL ( [*SSL (Secure Sockets Layer) Protocol*](/windows/desktop/SecGloss/s-gly) ).</span><span class="sxs-lookup"><span data-stu-id="6d40d-104">The **SslDecrementProviderReferenceCount** function decrements the references to the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d40d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6d40d-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslDecrementProviderReferenceCount(
  _In_ NCRYPT_PROV_HANDLE hSslProvider
);
```



## <a name="parameters"></a><span data-ttu-id="6d40d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6d40d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6d40d-107">*hSslProvider* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6d40d-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6d40d-108">Handle de l’instance du fournisseur de protocole SSL.</span><span class="sxs-lookup"><span data-stu-id="6d40d-108">The handle of the SSL protocol provider instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6d40d-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6d40d-109">Return value</span></span>

<span data-ttu-id="6d40d-110">Si la fonction est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="6d40d-110">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="6d40d-111">Si la fonction échoue, elle retourne une valeur d’erreur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="6d40d-111">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="6d40d-112">Les codes de retour possibles incluent, mais ne sont pas limités à, les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="6d40d-112">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="6d40d-113">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="6d40d-113">Return code/value</span></span>                                                                                                                                                        | <span data-ttu-id="6d40d-114">Description</span><span class="sxs-lookup"><span data-stu-id="6d40d-114">Description</span></span>                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="6d40d-115"><dt> **Descripteur d’état \_ non valide \_**</dt> <dt>0xC0000008L</dt></span><span class="sxs-lookup"><span data-stu-id="6d40d-115"><dt>**STATUS\_INVALID\_HANDLE** </dt> <dt>0xC0000008L</dt></span></span> </dl> | <span data-ttu-id="6d40d-116">Le descripteur du fournisseur SSL n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="6d40d-116">The SSL provider handle is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="6d40d-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6d40d-117">Requirements</span></span>



| <span data-ttu-id="6d40d-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6d40d-118">Requirement</span></span> | <span data-ttu-id="6d40d-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="6d40d-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d40d-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d40d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6d40d-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6d40d-121">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="6d40d-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6d40d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6d40d-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6d40d-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="6d40d-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="6d40d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6d40d-125"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="6d40d-125"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="6d40d-126">DLL</span><span class="sxs-lookup"><span data-stu-id="6d40d-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6d40d-127"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6d40d-127"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

