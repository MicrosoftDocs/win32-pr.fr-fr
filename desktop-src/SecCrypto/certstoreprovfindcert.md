---
description: Énumère ou recherche le premier certificat ou certificat suivant dans un magasin externe qui correspond aux critères spécifiés.
ms.assetid: 1129a372-4d7c-454e-969b-26a1d6037bc0
title: CertStoreProvFindCert fonction de rappel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvFindCert
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 09701991d6b192d27f921642bfc960df819f9140
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319806"
---
# <a name="certstoreprovfindcert-callback-function"></a><span data-ttu-id="7962b-103">CertStoreProvFindCert fonction de rappel</span><span class="sxs-lookup"><span data-stu-id="7962b-103">CertStoreProvFindCert callback function</span></span>

<span data-ttu-id="7962b-104">La fonction de rappel **CertStoreProvFindCert** énumère ou recherche le premier certificat ou le certificat suivant dans un [*magasin externe*](../secgloss/e-gly.md) qui correspond aux critères spécifiés.</span><span class="sxs-lookup"><span data-stu-id="7962b-104">The **CertStoreProvFindCert** callback function enumerates or finds the first or next certificate in an [*external store*](../secgloss/e-gly.md) that matches specified criteria.</span></span>

## <a name="syntax"></a><span data-ttu-id="7962b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7962b-105">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvFindCert(
  _In_    HCERTSTOREPROV              hStoreProv,
  _In_    PCCERT_STORE_PROV_FIND_INFO pFindInfo,
  _In_    PCCERT_CONTEXT              pPrevCertContext,
  _In_    DWORD                       dwFlags,
  _Inout_ void                        **ppvStoreProvFindInfo,
  _Out_   PCCERT_CONTEXT              *ppProvCertContext
);
```



## <a name="parameters"></a><span data-ttu-id="7962b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="7962b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7962b-107">*hStoreProv* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7962b-107">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7962b-108">Handle **HCERTSTOREPROV** vers un [*magasin de certificats*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="7962b-108">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="7962b-109">*pFindInfo* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7962b-109">*pFindInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7962b-110">Pointeur vers un [**magasin de \_ certificats \_ Prov \_ trouve \_**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) une structure contenant tous les paramètres transmis à la fonction [**CertFindCertificateInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore) .</span><span class="sxs-lookup"><span data-stu-id="7962b-110">A pointer to a [**CERT\_STORE\_PROV\_FIND\_INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info) structure containing all the parameters passed to the [**CertFindCertificateInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore) function.</span></span>

</dd> <dt>

<span data-ttu-id="7962b-111">*pPrevCertContext* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7962b-111">*pPrevCertContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7962b-112">Pointeur vers un [**\_ contexte**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) de certificat du certificat trouvé.</span><span class="sxs-lookup"><span data-stu-id="7962b-112">A pointer to a [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) of the certificate found.</span></span> <span data-ttu-id="7962b-113">Lors du premier appel à la fonction, ce paramètre doit avoir la valeur **null**.</span><span class="sxs-lookup"><span data-stu-id="7962b-113">On first call to the function, this parameter should be set to **NULL**.</span></span> <span data-ttu-id="7962b-114">Lors des appels suivants, il doit être défini sur le pointeur retourné dans le paramètre *ppProvCertContext* du dernier appel.</span><span class="sxs-lookup"><span data-stu-id="7962b-114">On subsequent calls, it should be set to the pointer returned in the *ppProvCertContext* parameter on the last call.</span></span> <span data-ttu-id="7962b-115">Un pointeur non **null** passé dans ce paramètre est libéré par la fonction de rappel.</span><span class="sxs-lookup"><span data-stu-id="7962b-115">A non-**NULL** pointer passed in this parameter is freed by the callback function.</span></span>

</dd> <dt>

<span data-ttu-id="7962b-116">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="7962b-116">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7962b-117">Toutes les valeurs d’indicateur nécessaires.</span><span class="sxs-lookup"><span data-stu-id="7962b-117">Any needed flag values.</span></span>

</dd> <dt>

<span data-ttu-id="7962b-118">*ppvStoreProvFindInfo* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="7962b-118">*ppvStoreProvFindInfo* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="7962b-119">Pointeur vers un pointeur vers une mémoire tampon pour retourner les informations du fournisseur de magasin.</span><span class="sxs-lookup"><span data-stu-id="7962b-119">A pointer to a pointer to a buffer to return the store provider information.</span></span> <span data-ttu-id="7962b-120">Le rappel peut éventuellement retourner un pointeur vers des informations de recherche interne dans ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="7962b-120">Optionally, the callback can return a pointer to internal find information in this parameter.</span></span> <span data-ttu-id="7962b-121">Après le premier appel, ce paramètre est défini sur le pointeur retourné par l’appel précédent à la fonction.</span><span class="sxs-lookup"><span data-stu-id="7962b-121">After the first call, this parameter is set to the pointer returned by the previous call to the function.</span></span>

</dd> <dt>

<span data-ttu-id="7962b-122">*ppProvCertContext* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="7962b-122">*ppProvCertContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7962b-123">En cas de recherche réussie, un pointeur vers le certificat trouvé est retourné dans ce paramètre.</span><span class="sxs-lookup"><span data-stu-id="7962b-123">On a successful find, a pointer to the certificate found is returned in this parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7962b-124">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="7962b-124">Return value</span></span>

<span data-ttu-id="7962b-125">Retourne la **valeur true** si la fonction réussit ou **false** en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="7962b-125">Returns **TRUE** if the function succeeds or **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="7962b-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7962b-126">Requirements</span></span>



| <span data-ttu-id="7962b-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7962b-127">Requirement</span></span> | <span data-ttu-id="7962b-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="7962b-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7962b-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7962b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="7962b-130">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7962b-130">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="7962b-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7962b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="7962b-132">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="7962b-132">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7962b-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7962b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7962b-134">**contexte du certificat \_**</span><span class="sxs-lookup"><span data-stu-id="7962b-134">**CERT\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[<span data-ttu-id="7962b-135">**\_informations de \_ \_ recherche Prov \_ . du magasin de certificats**</span><span class="sxs-lookup"><span data-stu-id="7962b-135">**CERT\_STORE\_PROV\_FIND\_INFO**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_store_prov_find_info)
</dt> <dt>

[<span data-ttu-id="7962b-136">**CertFindCertificateInStore**</span><span class="sxs-lookup"><span data-stu-id="7962b-136">**CertFindCertificateInStore**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore)
</dt> </dl>

 

 
