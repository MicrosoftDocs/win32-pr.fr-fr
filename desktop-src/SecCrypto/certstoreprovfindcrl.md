---
description: Énumère ou recherche la première liste de révocation de certificats ou la prochaine dans un magasin externe qui correspond aux critères spécifiés.
ms.assetid: caf218f5-f379-4cb6-bb4b-4767b846d45c
title: CertStoreProvFindCRL fonction de rappel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFindCRL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: b20b7a4b677356e59be9f2f6df47b260c12d2f64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529710"
---
# <a name="certstoreprovfindcrl-callback-function"></a><span data-ttu-id="14dcd-103">CertStoreProvFindCRL fonction de rappel</span><span class="sxs-lookup"><span data-stu-id="14dcd-103">CertStoreProvFindCRL callback function</span></span>

<span data-ttu-id="14dcd-104">La fonction de rappel **CertStoreProvFindCRL** énumère ou recherche la première ou la nouvelle [*liste de révocation de certificats*](../secgloss/c-gly.md) dans un [*magasin*](../secgloss/e-gly.md) externe qui correspond aux critères spécifiés.</span><span class="sxs-lookup"><span data-stu-id="14dcd-104">The **CertStoreProvFindCRL** callback function enumerates or finds the first or next [*CRL*](../secgloss/c-gly.md) in an external [*store*](../secgloss/e-gly.md) that matches specified criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="14dcd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="14dcd-105">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvFindCRL(
  _In_    HCERTSTOREPROV              hStoreProv,
  _In_    PCCERT_STORE_PROV_FIND_INFO pFindInfo,
  _In_    PCCRL_CONTEXT               pPrevCrlContext,
  _In_    DWORD                       dwFlags,
  _Inout_ void                        **ppvStoreProvFindInfo,
  _Out_   PCCRL_CONTEXT               *ppProvCrlContext
);
```



## <a name="parameters"></a><span data-ttu-id="14dcd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="14dcd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14dcd-107">*hStoreProv* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="14dcd-107">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14dcd-108">Handle **HCERTSTOREPROV** vers un [*magasin de certificats*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="14dcd-108">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="14dcd-109">*pFindInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="14dcd-109">*pFindInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14dcd-110">Pointeur vers un [**magasin de \_ certificats \_ Prov \_ trouve \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) une structure contenant tous les paramètres transmis à la fonction [**CertFindCRLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcrlinstore) .</span><span class="sxs-lookup"><span data-stu-id="14dcd-110">A pointer to a [**CERT\_STORE\_PROV\_FIND\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) structure containing all the parameters passed to the [**CertFindCRLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcrlinstore) function.</span></span>

</dd> <dt>

<span data-ttu-id="14dcd-111">*pPrevCrlContext* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="14dcd-111">*pPrevCrlContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14dcd-112">Pointeur vers une structure [**de \_ contexte de liste de révocation**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) de certificats de la dernière liste de révocation de certificats trouvée.</span><span class="sxs-lookup"><span data-stu-id="14dcd-112">A pointer to a [**CRL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) structure of the last CRL found.</span></span> <span data-ttu-id="14dcd-113">Lors du premier appel à la fonction, ce paramètre doit avoir la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="14dcd-113">On first call to the function, this parameter should be set to **NULL**.</span></span> <span data-ttu-id="14dcd-114">Lors des appels suivants, il doit être défini sur le pointeur retourné dans le paramètre *ppProvCRLContext* du dernier appel.</span><span class="sxs-lookup"><span data-stu-id="14dcd-114">On subsequent calls, it should be set to the pointer returned in the *ppProvCRLContext* parameter on the last call.</span></span> <span data-ttu-id="14dcd-115">Un pointeur non **null** passé dans ce paramètre est libéré par la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="14dcd-115">A non-**NULL** pointer passed in this parameter is freed by the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="14dcd-116">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="14dcd-116">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14dcd-117">Toutes les valeurs d’indicateur nécessaires.</span><span class="sxs-lookup"><span data-stu-id="14dcd-117">Any needed flag values.</span></span>

</dd> <dt>

<span data-ttu-id="14dcd-118">*ppvStoreProvFindInfo* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="14dcd-118">*ppvStoreProvFindInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="14dcd-119">Pointeur vers un pointeur vers une mémoire tampon pour retourner les informations du fournisseur de magasin.</span><span class="sxs-lookup"><span data-stu-id="14dcd-119">A pointer to a pointer to a buffer to return the store provider information.</span></span> <span data-ttu-id="14dcd-120">Le rappel peut éventuellement retourner un pointeur vers des informations de recherche interne dans ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="14dcd-120">Optionally, the callback can return a pointer to internal find information in this parameter.</span></span> <span data-ttu-id="14dcd-121">Après le premier appel, ce paramètre est défini sur le pointeur retourné par l’appel précédent à la fonction.</span><span class="sxs-lookup"><span data-stu-id="14dcd-121">After the first call, this parameter is set to the pointer returned by the previous call to the function.</span></span>

</dd> <dt>

<span data-ttu-id="14dcd-122">*ppProvCrlContext* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="14dcd-122">*ppProvCrlContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="14dcd-123">En cas de recherche réussie, un pointeur vers la liste de révocation de certificats trouvée est retourné dans ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="14dcd-123">On a successful find, a pointer to the CRL found is returned in this parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14dcd-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="14dcd-124">Return value</span></span>

<span data-ttu-id="14dcd-125">Retourne la **valeur true** si la fonction réussit ou **false** en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="14dcd-125">Returns **TRUE** if the function succeeds or **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="14dcd-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="14dcd-126">Requirements</span></span>



| <span data-ttu-id="14dcd-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="14dcd-127">Requirement</span></span> | <span data-ttu-id="14dcd-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="14dcd-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="14dcd-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="14dcd-129">Minimum supported client</span></span><br/> | <span data-ttu-id="14dcd-130">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="14dcd-130">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="14dcd-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="14dcd-131">Minimum supported server</span></span><br/> | <span data-ttu-id="14dcd-132">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="14dcd-132">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="14dcd-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="14dcd-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14dcd-134">**\_informations de \_ \_ recherche Prov \_ . du magasin de certificats**</span><span class="sxs-lookup"><span data-stu-id="14dcd-134">**CERT\_STORE\_PROV\_FIND\_INFO**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info)
</dt> <dt>

[<span data-ttu-id="14dcd-135">**CertFindCRLInStore**</span><span class="sxs-lookup"><span data-stu-id="14dcd-135">**CertFindCRLInStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcrlinstore)
</dt> <dt>

[<span data-ttu-id="14dcd-136">**\_contexte CRL**</span><span class="sxs-lookup"><span data-stu-id="14dcd-136">**CRL\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context)
</dt> </dl>

 

 
