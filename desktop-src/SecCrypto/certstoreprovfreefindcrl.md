---
description: Appelé lorsque le certificat retourné par le rappel CertStoreProvFindCRL n’a pas été utilisé, et par conséquent libéré, dans un appel ultérieur à CertStoreProvFindCRL.
ms.assetid: e90609f6-63cd-40eb-bd5a-289473daa5bb
title: CertStoreProvFreeFindCRL fonction de rappel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFreeFindCRL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: b5f5443d58a86c8bab979d17d64dc693d94ae373
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867169"
---
# <a name="certstoreprovfreefindcrl-callback-function"></a><span data-ttu-id="ebf5b-103">CertStoreProvFreeFindCRL fonction de rappel</span><span class="sxs-lookup"><span data-stu-id="ebf5b-103">CertStoreProvFreeFindCRL callback function</span></span>

<span data-ttu-id="ebf5b-104">La fonction de rappel **CertStoreProvFreeFindCRL** est appelée lorsque le certificat retourné par le rappel [**CertStoreProvFindCRL**](certstoreprovfindcrl.md) n’a pas été utilisé, et par conséquent libéré, dans un appel ultérieur à **CertStoreProvFindCRL**.</span><span class="sxs-lookup"><span data-stu-id="ebf5b-104">The **CertStoreProvFreeFindCRL** callback function is called when the certificate returned by the [**CertStoreProvFindCRL**](certstoreprovfindcrl.md) callback was not used, and thus released, in a subsequent call to **CertStoreProvFindCRL**.</span></span> <span data-ttu-id="ebf5b-105">Avant d’appeler le rappel de fermeture, tous les certificats retournés par le rappel [**CertStoreProvFindCRL**](certstoreprovfindcrl.md) doivent être libérés par le fournisseur à l’aide de **CertStoreProvFindCRL** ou **CertStoreProvFreeFindCRL**.</span><span class="sxs-lookup"><span data-stu-id="ebf5b-105">Before the CLOSE callback is called, all certificates returned by the [**CertStoreProvFindCRL**](certstoreprovfindcrl.md) callback must be released by the provider using **CertStoreProvFindCRL** or **CertStoreProvFreeFindCRL**.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebf5b-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="ebf5b-106">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvFreeFindCRL(
  _In_ HCERTSTOREPROV hStoreProv,
  _In_ PCCRL_CONTEXT  pCrlContext,
  _In_ void           *pvStoreProvFindInfo,
  _In_ DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="ebf5b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="ebf5b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebf5b-108">*hStoreProv* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ebf5b-108">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebf5b-109">Handle **HCERTSTOREPROV** vers un [*magasin de certificats*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="ebf5b-109">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="ebf5b-110">*pCrlContext* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ebf5b-110">*pCrlContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebf5b-111">Pointeur vers un [**\_ contexte de liste de révocation de certificats**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context).</span><span class="sxs-lookup"><span data-stu-id="ebf5b-111">A pointer to a [**CRL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context).</span></span>

</dd> <dt>

<span data-ttu-id="ebf5b-112">*pvStoreProvFindInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ebf5b-112">*pvStoreProvFindInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebf5b-113">Pointeur vers une mémoire tampon qui contient des informations de recherche.</span><span class="sxs-lookup"><span data-stu-id="ebf5b-113">A pointer to a buffer containing find information.</span></span>

</dd> <dt>

<span data-ttu-id="ebf5b-114">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="ebf5b-114">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebf5b-115">Toutes les valeurs d’indicateur nécessaires.</span><span class="sxs-lookup"><span data-stu-id="ebf5b-115">Any needed flag values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebf5b-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="ebf5b-116">Return value</span></span>

<span data-ttu-id="ebf5b-117">Retourne la **valeur true** si la fonction réussit ou **false** en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="ebf5b-117">Returns **TRUE** if the function succeeds or **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebf5b-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="ebf5b-118">Requirements</span></span>



| <span data-ttu-id="ebf5b-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="ebf5b-119">Requirement</span></span> | <span data-ttu-id="ebf5b-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="ebf5b-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ebf5b-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ebf5b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ebf5b-122">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ebf5b-122">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="ebf5b-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="ebf5b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ebf5b-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="ebf5b-124">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ebf5b-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="ebf5b-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebf5b-126">**CertStoreProvFindCRL**</span><span class="sxs-lookup"><span data-stu-id="ebf5b-126">**CertStoreProvFindCRL**</span></span>](certstoreprovfindcrl.md)
</dt> <dt>

[<span data-ttu-id="ebf5b-127">**\_contexte CRL**</span><span class="sxs-lookup"><span data-stu-id="ebf5b-127">**CRL\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> </dl>

 

 
