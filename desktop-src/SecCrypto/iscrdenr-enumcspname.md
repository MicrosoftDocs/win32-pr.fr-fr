---
description: Énumère le nom des fournisseurs de services de chiffrement (CSP) disponibles.
ms.assetid: d0dc8a8a-afff-4ccc-96e0-2c52913c3322
title: 'ISCrdEnr :: enumCSPName, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.enumCSPName
- SCrdEnr.enumCSPName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: e7bba587b56300cd02efd81758288d3b77c65a66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529992"
---
# <a name="iscrdenrenumcspname-method"></a><span data-ttu-id="e9df7-103">ISCrdEnr :: enumCSPName, méthode</span><span class="sxs-lookup"><span data-stu-id="e9df7-103">ISCrdEnr::enumCSPName method</span></span>

<span data-ttu-id="e9df7-104">La méthode **enumCSPName** énumère le nom des [*fournisseurs de services de chiffrement*](../secgloss/c-gly.md) (CSP) disponibles.</span><span class="sxs-lookup"><span data-stu-id="e9df7-104">The **enumCSPName** method enumerates the name of the available [*cryptographic service providers*](../secgloss/c-gly.md) (CSPs).</span></span>

## <a name="syntax"></a><span data-ttu-id="e9df7-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e9df7-105">Syntax</span></span>


```C++
HRESULT enumCSPName(
  [in]  DWORD     dwIndex,
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrCSPName
);
```


```VB

SCrdEnr.enumCSPName( _
  ByVal dwIndex, _
  ByVal dwFlags, _
  ByRef pbstrCSPName _
)
```





## <a name="parameters"></a><span data-ttu-id="e9df7-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e9df7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9df7-107">*dwIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e9df7-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9df7-108">Index de base zéro de la séquence d’énumération.</span><span class="sxs-lookup"><span data-stu-id="e9df7-108">The zero-based index for the enumeration sequence.</span></span>

</dd> <dt>

<span data-ttu-id="e9df7-109">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e9df7-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9df7-110">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="e9df7-110">Reserved for future use.</span></span> <span data-ttu-id="e9df7-111">Définissez cette valeur sur zéro.</span><span class="sxs-lookup"><span data-stu-id="e9df7-111">Set this value to zero.</span></span>

</dd> <dt>

<span data-ttu-id="e9df7-112">*pbstrCSPName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="e9df7-112">*pbstrCSPName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e9df7-113">Pointeur vers une chaîne qui retourne le nom du fournisseur de services de chiffrement énuméré.</span><span class="sxs-lookup"><span data-stu-id="e9df7-113">A pointer to a string that returns the name of the enumerated CSP.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9df7-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e9df7-114">Return value</span></span>

### <a name="c"></a><span data-ttu-id="e9df7-115">C++</span><span class="sxs-lookup"><span data-stu-id="e9df7-115">C++</span></span>

<span data-ttu-id="e9df7-116">Si la méthode est réussie, la méthode retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e9df7-116">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="e9df7-117">Si la méthode échoue, elle retourne une valeur **HRESULT** qui indique l’erreur.</span><span class="sxs-lookup"><span data-stu-id="e9df7-117">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="e9df7-118">Pour obtenir la liste des codes d’erreur courants, consultez [valeurs HRESULT communes](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="e9df7-118">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="e9df7-119">VB</span><span class="sxs-lookup"><span data-stu-id="e9df7-119">VB</span></span>

<span data-ttu-id="e9df7-120">Chaîne qui représente le nom du fournisseur de services de chiffrement énuméré.</span><span class="sxs-lookup"><span data-stu-id="e9df7-120">A string that represents the name of the enumerated CSP.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9df7-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e9df7-121">Requirements</span></span>



| <span data-ttu-id="e9df7-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e9df7-122">Requirement</span></span> | <span data-ttu-id="e9df7-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="e9df7-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e9df7-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e9df7-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e9df7-125">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="e9df7-125">None supported</span></span><br/>                                                               |
| <span data-ttu-id="e9df7-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e9df7-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e9df7-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e9df7-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="e9df7-128">DLL</span><span class="sxs-lookup"><span data-stu-id="e9df7-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e9df7-129"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e9df7-129"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="e9df7-130">IID</span><span class="sxs-lookup"><span data-stu-id="e9df7-130">IID</span></span><br/>                      | <span data-ttu-id="e9df7-131">IID \_ ISCrdEnr est défini en tant que 753988a1-1357-436D-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="e9df7-131">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="e9df7-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e9df7-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9df7-133">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="e9df7-133">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="e9df7-134">**ISCrdEnr::CSPCount**</span><span class="sxs-lookup"><span data-stu-id="e9df7-134">**ISCrdEnr::CSPCount**</span></span>](iscrdenr-cspcount.md)
</dt> <dt>

[<span data-ttu-id="e9df7-135">**ISCrdEnr :: CSPName**</span><span class="sxs-lookup"><span data-stu-id="e9df7-135">**ISCrdEnr::CSPName**</span></span>](iscrdenr-cspname.md)
</dt> </dl>

 

 
