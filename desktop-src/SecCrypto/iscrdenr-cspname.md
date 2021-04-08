---
description: Définit ou récupère le nom du fournisseur de services de chiffrement (CSP).
ms.assetid: 34fde7b0-747d-4592-a89a-207f82369f52
title: 'ISCrdEnr :: CSPName, propriété'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.CSPName
- ISCrdEnr.get_CSPName
- ISCrdEnr.put_CSPName
- SCrdEnr.CSPName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 363f2f9120d3b0a202335d0e8e450464cbc1f118
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104035162"
---
# <a name="iscrdenrcspname-property"></a><span data-ttu-id="54cfa-103">ISCrdEnr :: CSPName, propriété</span><span class="sxs-lookup"><span data-stu-id="54cfa-103">ISCrdEnr::CSPName property</span></span>

<span data-ttu-id="54cfa-104">La propriété **CSPName** définit ou récupère le nom du fournisseur de [*services de chiffrement*](../secgloss/c-gly.md) (CSP).</span><span class="sxs-lookup"><span data-stu-id="54cfa-104">The **CSPName** property sets or retrieves the name of the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP).</span></span>

<span data-ttu-id="54cfa-105">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="54cfa-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="54cfa-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="54cfa-106">Syntax</span></span>


```C++
HRESULT put_CSPName(
   BSTR newVal
);

HRESULT get_CSPName(
   BSTR *pVal
);
```



## <a name="property-value"></a><span data-ttu-id="54cfa-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="54cfa-107">Property value</span></span>

<span data-ttu-id="54cfa-108">Nom du fournisseur de services de chiffrement.</span><span class="sxs-lookup"><span data-stu-id="54cfa-108">The name of the CSP.</span></span>

## <a name="error-codes"></a><span data-ttu-id="54cfa-109">Codes d’erreur</span><span class="sxs-lookup"><span data-stu-id="54cfa-109">Error codes</span></span>

<span data-ttu-id="54cfa-110">Si la méthode est réussie, la méthode retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="54cfa-110">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="54cfa-111">Si la méthode échoue, elle retourne une valeur **HRESULT** qui indique l’erreur.</span><span class="sxs-lookup"><span data-stu-id="54cfa-111">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="54cfa-112">Pour obtenir la liste des codes d’erreur courants, consultez [valeurs HRESULT communes](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="54cfa-112">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="54cfa-113">Notes</span><span class="sxs-lookup"><span data-stu-id="54cfa-113">Remarks</span></span>

<span data-ttu-id="54cfa-114">Définissez cette propriété pour spécifier le nom du fournisseur de services de chiffrement à utiliser avec le contrôle d’inscription de carte à puce.</span><span class="sxs-lookup"><span data-stu-id="54cfa-114">Set this property to specify the name of the CSP to use with the Smart Card Enrollment Control.</span></span> <span data-ttu-id="54cfa-115">Obtient cette propriété pour récupérer le nom du fournisseur de services de chiffrement spécifié.</span><span class="sxs-lookup"><span data-stu-id="54cfa-115">Get this property to retrieve the name of the specified CSP.</span></span> <span data-ttu-id="54cfa-116">Si vous ne spécifiez pas de valeur pour cette propriété, la propriété **CSPName** est définie par défaut sur le prénom dans la liste des fournisseurs de services de chiffrement disponibles.</span><span class="sxs-lookup"><span data-stu-id="54cfa-116">If you do not specify a value for this property, the **CSPName** property defaults to the first name in the available list of CSPs.</span></span>

## <a name="requirements"></a><span data-ttu-id="54cfa-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="54cfa-117">Requirements</span></span>



| <span data-ttu-id="54cfa-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="54cfa-118">Requirement</span></span> | <span data-ttu-id="54cfa-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="54cfa-119">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="54cfa-120">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="54cfa-120">Minimum supported client</span></span><br/> | <span data-ttu-id="54cfa-121">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="54cfa-121">None supported</span></span><br/>                                                               |
| <span data-ttu-id="54cfa-122">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="54cfa-122">Minimum supported server</span></span><br/> | <span data-ttu-id="54cfa-123">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="54cfa-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="54cfa-124">DLL</span><span class="sxs-lookup"><span data-stu-id="54cfa-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54cfa-125"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54cfa-125"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="54cfa-126">IID</span><span class="sxs-lookup"><span data-stu-id="54cfa-126">IID</span></span><br/>                      | <span data-ttu-id="54cfa-127">IID \_ ISCrdEnr est défini en tant que 753988a1-1357-436D-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="54cfa-127">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="54cfa-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="54cfa-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54cfa-129">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="54cfa-129">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="54cfa-130">**ISCrdEnr::CSPCount**</span><span class="sxs-lookup"><span data-stu-id="54cfa-130">**ISCrdEnr::CSPCount**</span></span>](iscrdenr-cspcount.md)
</dt> <dt>

[<span data-ttu-id="54cfa-131">**ISCrdEnr::enumCSPName**</span><span class="sxs-lookup"><span data-stu-id="54cfa-131">**ISCrdEnr::enumCSPName**</span></span>](iscrdenr-enumcspname.md)
</dt> </dl>

 

 
