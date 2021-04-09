---
description: Appelée par CertDeleteCTLFromStore avant de supprimer une liste CTL du magasin.
ms.assetid: 6cda772f-7e94-414d-99fc-a90451ac0ccf
title: CertStoreProvDeleteCTL fonction de rappel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvDeleteCTL
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: abeea0fdc3b6d77974b2c057d0e2ea98fe11e63a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864353"
---
# <a name="certstoreprovdeletectl-callback-function"></a><span data-ttu-id="f6fd9-103">CertStoreProvDeleteCTL fonction de rappel</span><span class="sxs-lookup"><span data-stu-id="f6fd9-103">CertStoreProvDeleteCTL callback function</span></span>

<span data-ttu-id="f6fd9-104">La fonction de rappel **CertStoreProvDeleteCTL** est appelée par [**CertDeleteCTLFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletectlfromstore) avant de supprimer une liste CTL du magasin.</span><span class="sxs-lookup"><span data-stu-id="f6fd9-104">The **CertStoreProvDeleteCTL** callback function is called by [**CertDeleteCTLFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletectlfromstore) before deleting a CTL from the store.</span></span> <span data-ttu-id="f6fd9-105">Cette fonction détermine si une liste de certificats de confiance peut être supprimée.</span><span class="sxs-lookup"><span data-stu-id="f6fd9-105">This function determines whether a CTL can be deleted.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6fd9-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f6fd9-106">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvDeleteCTL(
  _In_ HCERTSTOREPROV hStoreProv,
  _In_ PCCTL_CONTEXT  pCtlContext,
  _In_ DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="f6fd9-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f6fd9-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f6fd9-108">*hStoreProv* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f6fd9-108">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6fd9-109">Handle **HCERTSTOREPROV** vers un [*magasin de certificats*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="f6fd9-109">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6fd9-110">*pCtlContext* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f6fd9-110">*pCtlContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6fd9-111">Pointeur vers une structure [**de \_ contexte CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) .</span><span class="sxs-lookup"><span data-stu-id="f6fd9-111">A pointer to a [**CTL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) structure.</span></span>

</dd> <dt>

<span data-ttu-id="f6fd9-112">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f6fd9-112">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f6fd9-113">Toutes les valeurs d’indicateur nécessaires.</span><span class="sxs-lookup"><span data-stu-id="f6fd9-113">Any needed flag values.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f6fd9-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f6fd9-114">Return value</span></span>

<span data-ttu-id="f6fd9-115">Retourne la **valeur true** si une liste de certificats de confiance peut être supprimée du magasin.</span><span class="sxs-lookup"><span data-stu-id="f6fd9-115">Returns **TRUE** if a CTL can be deleted from the store.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6fd9-116">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f6fd9-116">Requirements</span></span>



| <span data-ttu-id="f6fd9-117">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f6fd9-117">Requirement</span></span> | <span data-ttu-id="f6fd9-118">Valeur</span><span class="sxs-lookup"><span data-stu-id="f6fd9-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f6fd9-119">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f6fd9-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f6fd9-120">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f6fd9-120">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="f6fd9-121">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f6fd9-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f6fd9-122">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f6fd9-122">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



 

 
