---
description: Énumère ou recherche la liste CTL First ou Next dans un magasin externe qui correspond aux critères spécifiés.
ms.assetid: 0b465e6e-fb5c-4621-a968-c2cdcab0ea15
title: CertStoreProvFindCTL fonction de rappel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFindCTL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 9454f918c9cbc5b6f90642d46fbb33573b70457f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106530669"
---
# <a name="certstoreprovfindctl-callback-function"></a><span data-ttu-id="e6a2e-103">CertStoreProvFindCTL fonction de rappel</span><span class="sxs-lookup"><span data-stu-id="e6a2e-103">CertStoreProvFindCTL callback function</span></span>

<span data-ttu-id="e6a2e-104">La fonction de rappel **CertStoreProvFindCTL** énumère ou recherche la [*liste CTL*](../secgloss/c-gly.md) First ou Next dans un [*magasin externe*](../secgloss/e-gly.md) qui correspond aux critères spécifiés.</span><span class="sxs-lookup"><span data-stu-id="e6a2e-104">The **CertStoreProvFindCTL** callback function enumerates or finds the first or next [*CTL*](../secgloss/c-gly.md) in an [*external store*](../secgloss/e-gly.md) that matches specified criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6a2e-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e6a2e-105">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvFindCTL(
  _In_    HCERTSTOREPROV              hStoreProv,
  _In_    PCCERT_STORE_PROV_FIND_INFO pFindInfo,
  _In_    PCCTL_CONTEXT               pPrevCtlContext,
  _In_    DWORD                       dwFlags,
  _Inout_ void                        **ppvStoreProvFindInfo,
  _Out_   PCCTL_CONTEXT               *ppProvCtlContext
);
```



## <a name="parameters"></a><span data-ttu-id="e6a2e-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e6a2e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6a2e-107">*hStoreProv* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e6a2e-107">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6a2e-108">Handle **HCERTSTOREPROV** vers un [*magasin de certificats*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="e6a2e-108">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="e6a2e-109">*pFindInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e6a2e-109">*pFindInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6a2e-110">Pointeur vers un [**magasin de \_ certificats \_ Prov \_ trouve \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) la structure des informations contenant tous les paramètres transmis à [**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore).</span><span class="sxs-lookup"><span data-stu-id="e6a2e-110">A pointer to a [**CERT\_STORE\_PROV\_FIND\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) structure containing all the parameters passed to the [**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore).</span></span> <span data-ttu-id="e6a2e-111">CHANGETABLE(CHANGES ...).</span><span class="sxs-lookup"><span data-stu-id="e6a2e-111">function.</span></span>

</dd> <dt>

<span data-ttu-id="e6a2e-112">*pPrevCtlContext* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e6a2e-112">*pPrevCtlContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6a2e-113">Pointeur vers une structure [**de \_ contexte CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) de la dernière liste de certificats de confiance trouvée.</span><span class="sxs-lookup"><span data-stu-id="e6a2e-113">A pointer to a [**CTL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) structure of the last CTL found.</span></span> <span data-ttu-id="e6a2e-114">Lors du premier appel à la fonction, ce paramètre doit avoir la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="e6a2e-114">On first call to the function, this parameter should be set to **NULL**.</span></span> <span data-ttu-id="e6a2e-115">Lors des appels suivants, il doit être défini sur le pointeur retourné dans le paramètre *ppProvCTLContext* du dernier appel.</span><span class="sxs-lookup"><span data-stu-id="e6a2e-115">On subsequent calls, it should be set to the pointer returned in the *ppProvCTLContext* parameter on the last call.</span></span> <span data-ttu-id="e6a2e-116">Un pointeur non **null** passé dans ce paramètre est libéré par la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="e6a2e-116">A non-**NULL** pointer passed in this parameter is freed by the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="e6a2e-117">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e6a2e-117">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6a2e-118">Toutes les valeurs d’indicateur nécessaires.</span><span class="sxs-lookup"><span data-stu-id="e6a2e-118">Any needed flag values.</span></span>

</dd> <dt>

<span data-ttu-id="e6a2e-119">*ppvStoreProvFindInfo* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="e6a2e-119">*ppvStoreProvFindInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="e6a2e-120">Pointeur vers un pointeur vers la mémoire tampon pour retourner les informations du fournisseur de magasin.</span><span class="sxs-lookup"><span data-stu-id="e6a2e-120">A pointer to a pointer to buffer to return the store provider information.</span></span> <span data-ttu-id="e6a2e-121">Le rappel peut éventuellement retourner un pointeur vers des informations de recherche interne dans ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="e6a2e-121">Optionally, the callback can return a pointer to internal find information in this parameter.</span></span> <span data-ttu-id="e6a2e-122">Après le premier appel, ce paramètre est défini sur le pointeur retourné par l’appel précédent à la fonction.</span><span class="sxs-lookup"><span data-stu-id="e6a2e-122">After the first call, this parameter is set to the pointer returned by the previous call to the function.</span></span>

</dd> <dt>

<span data-ttu-id="e6a2e-123">*ppProvCtlContext* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e6a2e-123">*ppProvCtlContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e6a2e-124">En cas de recherche réussie, un pointeur vers la liste CTL trouvée est retourné dans ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="e6a2e-124">On a successful find, a pointer to the CTL found is returned in this parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6a2e-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e6a2e-125">Return value</span></span>

<span data-ttu-id="e6a2e-126">Retourne la **valeur true** si la fonction réussit ou **false** en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="e6a2e-126">Returns **TRUE** if the function succeeds or **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6a2e-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e6a2e-127">Requirements</span></span>



| <span data-ttu-id="e6a2e-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e6a2e-128">Requirement</span></span> | <span data-ttu-id="e6a2e-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="e6a2e-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e6a2e-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e6a2e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="e6a2e-131">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e6a2e-131">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="e6a2e-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e6a2e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="e6a2e-133">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e6a2e-133">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e6a2e-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e6a2e-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6a2e-135">**\_informations de \_ \_ recherche Prov \_ . du magasin de certificats**</span><span class="sxs-lookup"><span data-stu-id="e6a2e-135">**CERT\_STORE\_PROV\_FIND\_INFO**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info)
</dt> <dt>

[<span data-ttu-id="e6a2e-136">**CertFindCTLInStore**</span><span class="sxs-lookup"><span data-stu-id="e6a2e-136">**CertFindCTLInStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore)
</dt> <dt>

[<span data-ttu-id="e6a2e-137">**\_contexte CTL**</span><span class="sxs-lookup"><span data-stu-id="e6a2e-137">**CTL\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context)
</dt> </dl>

 

 
