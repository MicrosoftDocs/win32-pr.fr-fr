---
description: Appelé lorsque le certificat retourné par le rappel CertStoreProvFindCTL n’a pas été utilisé, et par conséquent libéré, dans un appel ultérieur à CertStoreProvFindCTL.
ms.assetid: 04e62a4e-4542-4225-8750-fabbda5adf0d
title: CertStoreProvFreeFindCTL fonction de rappel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFreeFindCTL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: ff0c9c3b7be6b8a4cafd759c3411f5096ee8640b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106524172"
---
# <a name="certstoreprovfreefindctl-callback-function"></a><span data-ttu-id="51e5c-103">CertStoreProvFreeFindCTL fonction de rappel</span><span class="sxs-lookup"><span data-stu-id="51e5c-103">CertStoreProvFreeFindCTL callback function</span></span>

<span data-ttu-id="51e5c-104">La fonction de rappel **CertStoreProvFreeFindCTL** est appelée lorsque le certificat retourné par le rappel [**CertStoreProvFindCTL**](certstoreprovfindctl.md) n’a pas été utilisé, et par conséquent libéré, dans un appel ultérieur à **CertStoreProvFindCTL**.</span><span class="sxs-lookup"><span data-stu-id="51e5c-104">The **CertStoreProvFreeFindCTL** callback function is called when the certificate returned by the [**CertStoreProvFindCTL**](certstoreprovfindctl.md) callback was not used, and thus released, in a subsequent call to **CertStoreProvFindCTL**.</span></span> <span data-ttu-id="51e5c-105">Avant d’appeler le rappel de fermeture, tous les certificats retournés par le rappel [**CertStoreProvFindCTL**](certstoreprovfindctl.md) doivent être libérés par le fournisseur à l’aide de **CertStoreProvFindCTL** ou **CertStoreProvFreeFindCTL**.</span><span class="sxs-lookup"><span data-stu-id="51e5c-105">Before the CLOSE callback is called, all certificates returned by the [**CertStoreProvFindCTL**](certstoreprovfindctl.md) callback must be released by the provider using **CertStoreProvFindCTL** or **CertStoreProvFreeFindCTL**.</span></span>

## <a name="syntax"></a><span data-ttu-id="51e5c-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="51e5c-106">Syntax</span></span>


```C++
BOOL CertStoreProvFreeFindCTL(
  _In_ HCERTSTOREPROV hStoreProv,
  _In_ PCCTL_CONTEXT  pCtlContext,
  _In_ void           *pvStoreProvFindInfo,
  _In_ DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="51e5c-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="51e5c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51e5c-108">*hStoreProv* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="51e5c-108">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51e5c-109">Handle **HCERTSTOREPROV** vers un [*magasin de certificats*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="51e5c-109">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="51e5c-110">*pCtlContext* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="51e5c-110">*pCtlContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51e5c-111">Pointeur vers une structure [**de \_ contexte CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) .</span><span class="sxs-lookup"><span data-stu-id="51e5c-111">A pointer to a [**CTL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) structure.</span></span>

</dd> <dt>

<span data-ttu-id="51e5c-112">*pvStoreProvFindInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="51e5c-112">*pvStoreProvFindInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51e5c-113">Pointeur vers une mémoire tampon qui contient des informations de recherche.</span><span class="sxs-lookup"><span data-stu-id="51e5c-113">A pointer to a buffer containing find information.</span></span>

</dd> <dt>

<span data-ttu-id="51e5c-114">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="51e5c-114">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="51e5c-115">Toutes les valeurs d’indicateur nécessaires.</span><span class="sxs-lookup"><span data-stu-id="51e5c-115">Any needed flag values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51e5c-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="51e5c-116">Return value</span></span>

<span data-ttu-id="51e5c-117">Retourne la **valeur true** si la fonction réussit ou **false** en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="51e5c-117">Returns **TRUE** if the function succeeds or **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="51e5c-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="51e5c-118">Requirements</span></span>



| <span data-ttu-id="51e5c-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="51e5c-119">Requirement</span></span> | <span data-ttu-id="51e5c-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="51e5c-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="51e5c-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="51e5c-121">Minimum supported client</span></span><br/> | <span data-ttu-id="51e5c-122">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="51e5c-122">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="51e5c-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="51e5c-123">Minimum supported server</span></span><br/> | <span data-ttu-id="51e5c-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="51e5c-124">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="51e5c-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="51e5c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51e5c-126">**CertStoreProvFindCTL**</span><span class="sxs-lookup"><span data-stu-id="51e5c-126">**CertStoreProvFindCTL**</span></span>](certstoreprovfindctl.md)
</dt> <dt>

[<span data-ttu-id="51e5c-127">**\_contexte CTL**</span><span class="sxs-lookup"><span data-stu-id="51e5c-127">**CTL\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> </dl>

 

 
