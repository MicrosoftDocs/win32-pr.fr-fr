---
description: Incrémente le décompte de références à une instance du fournisseur SSL (SSL (Secure Sockets Layer) Protocol).
ms.assetid: 67e7b8b4-b073-4936-b1e0-3fc7c1c011a2
title: SslIncrementProviderReferenceCount, fonction (Sslprovider. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslIncrementProviderReferenceCount
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 862697035d978db082c303c6e1df6f2a444d8be3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545156"
---
# <a name="sslincrementproviderreferencecount-function"></a><span data-ttu-id="67eef-103">SslIncrementProviderReferenceCount fonction)</span><span class="sxs-lookup"><span data-stu-id="67eef-103">SslIncrementProviderReferenceCount function</span></span>

<span data-ttu-id="67eef-104">La fonction **SslIncrementProviderReferenceCount** incrémente le décompte de références à une instance du fournisseur SSL ( [*SSL (Secure Sockets Layer) Protocol*](/windows/desktop/SecGloss/s-gly) ).</span><span class="sxs-lookup"><span data-stu-id="67eef-104">The **SslIncrementProviderReferenceCount** function increments the reference count to a [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) provider instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="67eef-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="67eef-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslIncrementProviderReferenceCount(
  _In_ NCRYPT_PROV_HANDLE hSslProvider
);
```



## <a name="parameters"></a><span data-ttu-id="67eef-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="67eef-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67eef-107">*hSslProvider* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="67eef-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67eef-108">Handle de l’instance du fournisseur de protocole SSL.</span><span class="sxs-lookup"><span data-stu-id="67eef-108">The handle to the SSL protocol provider instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67eef-109">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="67eef-109">Return value</span></span>

<span data-ttu-id="67eef-110">Si la fonction est réussie, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="67eef-110">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="67eef-111">Si la fonction échoue, elle retourne une valeur d’erreur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="67eef-111">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="67eef-112">Les codes de retour possibles incluent, mais ne sont pas limités à, les éléments suivants.</span><span class="sxs-lookup"><span data-stu-id="67eef-112">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="67eef-113">Code/valeur de retour</span><span class="sxs-lookup"><span data-stu-id="67eef-113">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="67eef-114">Description</span><span class="sxs-lookup"><span data-stu-id="67eef-114">Description</span></span>                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="67eef-115"><dt>**NPD \_ \_Handle 0X80090026L non valide**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="67eef-115"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="67eef-116">Le descripteur *hSslProvider* n’est pas valide.</span><span class="sxs-lookup"><span data-stu-id="67eef-116">The *hSslProvider* handle is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="67eef-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="67eef-117">Requirements</span></span>



| <span data-ttu-id="67eef-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="67eef-118">Requirement</span></span> | <span data-ttu-id="67eef-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="67eef-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="67eef-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="67eef-120">Minimum supported client</span></span><br/> | <span data-ttu-id="67eef-121">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="67eef-121">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="67eef-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="67eef-122">Minimum supported server</span></span><br/> | <span data-ttu-id="67eef-123">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="67eef-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="67eef-124">En-tête</span><span class="sxs-lookup"><span data-stu-id="67eef-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="67eef-125"><dt>Sslprovider. h</dt></span><span class="sxs-lookup"><span data-stu-id="67eef-125"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="67eef-126">DLL</span><span class="sxs-lookup"><span data-stu-id="67eef-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67eef-127"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67eef-127"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

