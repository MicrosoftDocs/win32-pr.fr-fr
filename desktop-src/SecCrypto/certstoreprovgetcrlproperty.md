---
description: Récupère la propriété spécifiée d’une liste de révocation de certificats.
ms.assetid: b02f4f92-952a-4625-a7d4-6e78e542774e
title: CertStoreProvGetCRLProperty fonction de rappel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvGetCRLProperty
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: bcf69653f03ccfbb52c8247c9ea459000db55e2a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106542931"
---
# <a name="certstoreprovgetcrlproperty-callback-function"></a><span data-ttu-id="0bb97-103">CertStoreProvGetCRLProperty fonction de rappel</span><span class="sxs-lookup"><span data-stu-id="0bb97-103">CertStoreProvGetCRLProperty callback function</span></span>

<span data-ttu-id="0bb97-104">La fonction de rappel **CertStoreProvGetCRLProperty** récupère la propriété spécifiée d’une [*liste de révocation de certificats*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="0bb97-104">The **CertStoreProvGetCRLProperty** callback function retrieves a specified property of a [*CRL*](../secgloss/c-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0bb97-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0bb97-105">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvGetCRLProperty(
  _In_    HCERTSTOREPROV hStoreProv,
  _In_    PCCRL_CONTEXT  pCrlContext,
  _In_    DWORD          dwPropId,
  _In_    DWORD          dwFlags,
  _Out_   void           *pvData,
  _Inout_ DWORD          *pcbData
);
```



## <a name="parameters"></a><span data-ttu-id="0bb97-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0bb97-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bb97-107">*hStoreProv* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0bb97-107">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bb97-108">Handle **HCERTSTOREPROV** vers un [*magasin de certificats*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="0bb97-108">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="0bb97-109">*pCrlContext* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0bb97-109">*pCrlContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bb97-110">Pointeur vers une structure [**de \_ contexte de liste de révocation de certificats**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) .</span><span class="sxs-lookup"><span data-stu-id="0bb97-110">A pointer to a [**CRL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) structure.</span></span>

</dd> <dt>

<span data-ttu-id="0bb97-111">*dwPropId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0bb97-111">*dwPropId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bb97-112">Indique un identificateur de propriété.</span><span class="sxs-lookup"><span data-stu-id="0bb97-112">Indicates a property identifier.</span></span>

</dd> <dt>

<span data-ttu-id="0bb97-113">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0bb97-113">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0bb97-114">Toutes les valeurs d’indicateur nécessaires.</span><span class="sxs-lookup"><span data-stu-id="0bb97-114">Any needed flag values.</span></span>

</dd> <dt>

<span data-ttu-id="0bb97-115">*pvData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0bb97-115">*pvData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0bb97-116">Pointeur vers une mémoire tampon qui contient le pointeur vers une structure de [**\_ contexte de liste de révocation de certificats**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) qui doit être retournée par la fonction.</span><span class="sxs-lookup"><span data-stu-id="0bb97-116">A pointer to a buffer to contain the pointer to a [**CRL\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context) structure to be returned by the function.</span></span> <span data-ttu-id="0bb97-117">Peut avoir la valeur **null** lors d’un premier appel à la fonction pour obtenir la valeur de *pcbData* avant d’allouer de la mémoire pour la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="0bb97-117">May be set to **NULL** on a first call to the function to get the value of *pcbData* before allocating memory for the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="0bb97-118">*pcbData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="0bb97-118">*pcbData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0bb97-119">Pointeur vers une **valeur DWORD** indiquant la longueur de la mémoire tampon *pvData* .</span><span class="sxs-lookup"><span data-stu-id="0bb97-119">A pointer to a **DWORD** indicating the length of the *pvData* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0bb97-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0bb97-120">Return value</span></span>

<span data-ttu-id="0bb97-121">Retourne la **valeur true** si la fonction réussit ou **false** en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="0bb97-121">Returns **TRUE** if the function succeeds or **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bb97-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0bb97-122">Requirements</span></span>



| <span data-ttu-id="0bb97-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0bb97-123">Requirement</span></span> | <span data-ttu-id="0bb97-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="0bb97-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0bb97-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0bb97-125">Minimum supported client</span></span><br/> | <span data-ttu-id="0bb97-126">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0bb97-126">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="0bb97-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0bb97-127">Minimum supported server</span></span><br/> | <span data-ttu-id="0bb97-128">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0bb97-128">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0bb97-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0bb97-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bb97-130">**\_contexte CRL**</span><span class="sxs-lookup"><span data-stu-id="0bb97-130">**CRL\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-crl_context)
</dt> </dl>

 

 
