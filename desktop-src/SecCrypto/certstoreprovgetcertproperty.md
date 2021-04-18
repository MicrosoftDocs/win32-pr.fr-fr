---
description: Récupère la propriété spécifiée d’un certificat.
ms.assetid: 827e0331-1f87-4891-8cc1-de1bcbad2963
title: CertStoreProvGetCertProperty fonction de rappel
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CertStoreProvGetCertProperty
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 50de9a73438e2755e002570f921d15e6086a4b7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533633"
---
# <a name="certstoreprovgetcertproperty-callback-function"></a><span data-ttu-id="83921-103">CertStoreProvGetCertProperty fonction de rappel</span><span class="sxs-lookup"><span data-stu-id="83921-103">CertStoreProvGetCertProperty callback function</span></span>

<span data-ttu-id="83921-104">La fonction de rappel **CertStoreProvGetCertProperty** récupère la propriété spécifiée d’un certificat.</span><span class="sxs-lookup"><span data-stu-id="83921-104">The **CertStoreProvGetCertProperty** callback function retrieves a specified property of a certificate.</span></span>

## <a name="syntax"></a><span data-ttu-id="83921-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="83921-105">Syntax</span></span>


```C++
BOOL WINAPI CertStoreProvGetCertProperty(
  _In_    HCERTSTOREPROV hStoreProv,
  _In_    PCCERT_CONTEXT pCertContext,
  _In_    DWORD          dwPropId,
  _In_    DWORD          dwFlags,
  _Out_   void           *pvData,
  _Inout_ DWORD          *pcbData
);
```



## <a name="parameters"></a><span data-ttu-id="83921-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="83921-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83921-107">*hStoreProv* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="83921-107">*hStoreProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83921-108">Handle **HCERTSTOREPROV** vers un [*magasin de certificats*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="83921-108">**HCERTSTOREPROV** handle to a [*certificate store*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="83921-109">*pCertContext* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="83921-109">*pCertContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83921-110">Pointeur vers une structure [**de \_ contexte de certificat**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) .</span><span class="sxs-lookup"><span data-stu-id="83921-110">A pointer to a [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) structure.</span></span>

</dd> <dt>

<span data-ttu-id="83921-111">*dwPropId* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="83921-111">*dwPropId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83921-112">Indique un identificateur de propriété.</span><span class="sxs-lookup"><span data-stu-id="83921-112">Indicates a property identifier.</span></span>

</dd> <dt>

<span data-ttu-id="83921-113">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="83921-113">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="83921-114">Toutes les valeurs d’indicateur nécessaires.</span><span class="sxs-lookup"><span data-stu-id="83921-114">Any needed flag values.</span></span>

</dd> <dt>

<span data-ttu-id="83921-115">*pvData* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="83921-115">*pvData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="83921-116">Pointeur vers une mémoire tampon destinée à contenir le pointeur vers une structure de [**\_ contexte de certificat**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) qui doit être retournée par la fonction.</span><span class="sxs-lookup"><span data-stu-id="83921-116">A pointer to a buffer to contain the pointer to a [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) structure to be returned by the function.</span></span> <span data-ttu-id="83921-117">Peut avoir la valeur **null** lors d’un premier appel à la fonction pour obtenir la valeur de *pcbData* avant d’allouer de la mémoire pour la mémoire tampon.</span><span class="sxs-lookup"><span data-stu-id="83921-117">May be set to **NULL** on a first call to the function to get the value of *pcbData* before allocating memory for the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="83921-118">*pcbData* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="83921-118">*pcbData* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="83921-119">Pointeur vers une **valeur DWORD** indiquant la longueur de la mémoire tampon *pvData* .</span><span class="sxs-lookup"><span data-stu-id="83921-119">A pointer to a **DWORD** indicating the length of the *pvData* buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83921-120">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="83921-120">Return value</span></span>

<span data-ttu-id="83921-121">Retourne la **valeur true** si la fonction réussit ou **false** en cas d’échec.</span><span class="sxs-lookup"><span data-stu-id="83921-121">Returns **TRUE** if the function succeeds or **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="83921-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="83921-122">Requirements</span></span>



| <span data-ttu-id="83921-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="83921-123">Requirement</span></span> | <span data-ttu-id="83921-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="83921-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="83921-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="83921-125">Minimum supported client</span></span><br/> | <span data-ttu-id="83921-126">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="83921-126">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="83921-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="83921-127">Minimum supported server</span></span><br/> | <span data-ttu-id="83921-128">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="83921-128">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="83921-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="83921-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83921-130">**contexte du certificat \_**</span><span class="sxs-lookup"><span data-stu-id="83921-130">**CERT\_CONTEXT**</span></span>](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context)
</dt> </dl>

 

 
