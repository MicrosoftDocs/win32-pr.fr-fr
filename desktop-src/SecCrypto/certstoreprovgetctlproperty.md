---
description: Récupère une propriété spécifiée d’une liste de certificats de confiance (CTL).
ms.assetid: 65309715-65b4-4608-960d-3404e68800a2
title: CertStoreProvGetCTLProperty fonction de rappel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvGetCTLProperty
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: e30a9e735d44fc5681d5cd3932baaf3cc90aa30d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528262"
---
# <a name="certstoreprovgetctlproperty-callback-function"></a><span data-ttu-id="174ab-103">CertStoreProvGetCTLProperty fonction de rappel</span><span class="sxs-lookup"><span data-stu-id="174ab-103">CertStoreProvGetCTLProperty callback function</span></span>

<span data-ttu-id="174ab-104">La fonction de rappel **CertStoreProvGetCTLProperty** récupère une propriété spécifiée d’une [*liste de certificats de confiance*](../secgloss/c-gly.md) (CTL).</span><span class="sxs-lookup"><span data-stu-id="174ab-104">The **CertStoreProvGetCTLProperty** callback function retrieves a specified property of a [*certificate trust list*](../secgloss/c-gly.md) (CTL).</span></span>

## <a name="syntax"></a><span data-ttu-id="174ab-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="174ab-105">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvGetCTLProperty(
  _In_    HCERTSTOREPROV hStoreProv,
  _In_    PCCTL_CONTEXT  pCtlContext,
  _In_    DWORD          dwPropId,
  _In_    DWORD          dwFlags,
  _Out_   void           *pvData,
  _Inout_ DWORD          *pcbData
);
```



## <a name="parameters"></a><span data-ttu-id="174ab-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="174ab-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="174ab-107">*hStoreProv* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="174ab-107">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="174ab-108">Handle **HCERTSTOREPROV** vers un [*magasin de certificats*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="174ab-108">A **HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="174ab-109">*pCtlContext* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="174ab-109">*pCtlContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="174ab-110">Pointeur vers une structure [**de \_ contexte CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) .</span><span class="sxs-lookup"><span data-stu-id="174ab-110">A pointer to a [**CTL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) structure.</span></span>

</dd> <dt>

<span data-ttu-id="174ab-111">*dwPropId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="174ab-111">*dwPropId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="174ab-112">Indique un identificateur de propriété.</span><span class="sxs-lookup"><span data-stu-id="174ab-112">Indicates a property identifier.</span></span>

</dd> <dt>

<span data-ttu-id="174ab-113">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="174ab-113">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="174ab-114">Toutes les valeurs d’indicateur nécessaires.</span><span class="sxs-lookup"><span data-stu-id="174ab-114">Any needed flag values.</span></span>

</dd> <dt>

<span data-ttu-id="174ab-115">*pvData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="174ab-115">*pvData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="174ab-116">Pointeur vers une mémoire tampon destinée à contenir le pointeur vers une structure de [**\_ contexte CTL**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) devant être retournée par la fonction.</span><span class="sxs-lookup"><span data-stu-id="174ab-116">A pointer to a buffer to contain the pointer to a [**CTL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context) structure to be returned by the function.</span></span> <span data-ttu-id="174ab-117">Pour obtenir la valeur de *pcbData* avant d’allouer de la mémoire pour la mémoire tampon, ce paramètre peut avoir la valeur **null** lors d’un premier appel à la fonction.</span><span class="sxs-lookup"><span data-stu-id="174ab-117">To get the value of *pcbData* before allocating memory for the buffer, this parameter can be set to **NULL** on a first call to the function.</span></span>

</dd> <dt>

<span data-ttu-id="174ab-118">*pcbData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="174ab-118">*pcbData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="174ab-119">Pointeur vers une **valeur DWORD** qui indique la longueur de la mémoire tampon *pvData* .</span><span class="sxs-lookup"><span data-stu-id="174ab-119">A pointer to a **DWORD** that indicates the length of the *pvData* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="174ab-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="174ab-120">Return value</span></span>

<span data-ttu-id="174ab-121">Si la fonction est réussie, la fonction retourne une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="174ab-121">If the function succeeds, the function returns nonzero.</span></span>

<span data-ttu-id="174ab-122">Si la fonction échoue, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="174ab-122">If the function fails, it returns zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="174ab-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="174ab-123">Requirements</span></span>



| <span data-ttu-id="174ab-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="174ab-124">Requirement</span></span> | <span data-ttu-id="174ab-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="174ab-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="174ab-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="174ab-126">Minimum supported client</span></span><br/> | <span data-ttu-id="174ab-127">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="174ab-127">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="174ab-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="174ab-128">Minimum supported server</span></span><br/> | <span data-ttu-id="174ab-129">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="174ab-129">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="174ab-130">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="174ab-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="174ab-131">**\_contexte CTL**</span><span class="sxs-lookup"><span data-stu-id="174ab-131">**CTL\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-ctl_context)
</dt> </dl>

 

 
