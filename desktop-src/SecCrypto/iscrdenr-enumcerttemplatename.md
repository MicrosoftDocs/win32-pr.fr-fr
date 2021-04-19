---
description: Énumère les noms de modèles de certificats.
ms.assetid: 4741eb0d-b8e0-468c-8a00-9ccacb52a9a7
title: 'ISCrdEnr :: enumCertTemplateName, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.enumCertTemplateName
- SCrdEnr.enumCertTemplateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: a0a4850143cac48ef9b9b853f99153d4daeb4366
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106534097"
---
# <a name="iscrdenrenumcerttemplatename-method"></a><span data-ttu-id="a7fbd-103">ISCrdEnr :: enumCertTemplateName, méthode</span><span class="sxs-lookup"><span data-stu-id="a7fbd-103">ISCrdEnr::enumCertTemplateName method</span></span>

<span data-ttu-id="a7fbd-104">La méthode **enumCertTemplateName** énumère les noms de modèles de certificats.</span><span class="sxs-lookup"><span data-stu-id="a7fbd-104">The **enumCertTemplateName** method enumerates the certificate template names.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7fbd-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="a7fbd-105">Syntax</span></span>


```C++
HRESULT enumCertTemplateName(
  [in]  DWORD     dwIndex,
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrCertTemplateName
);
```


```VB

SCrdEnr.enumCertTemplateName( _
  ByVal dwIndex, _
  ByVal dwFlags, _
  ByRef pbstrCertTemplateName _
)
```





## <a name="parameters"></a><span data-ttu-id="a7fbd-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="a7fbd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a7fbd-107">*dwIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a7fbd-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7fbd-108">Index de base zéro de la séquence d’énumération.</span><span class="sxs-lookup"><span data-stu-id="a7fbd-108">The zero-based index for the enumeration sequence.</span></span>

</dd> <dt>

<span data-ttu-id="a7fbd-109">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="a7fbd-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a7fbd-110">Valeur qui détermine si le modèle de certificat énuméré s’applique aux certificats de l’utilisateur ou de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="a7fbd-110">A value that determines whether the enumerated certificate template applies to user or machine certificates.</span></span> <span data-ttu-id="a7fbd-111">Si cette valeur est \_ \_ \_ \_ un modèle de certificat d’utilisateur à l’utilisation infinie (défini comme 1), l’énumération s’applique aux modèles de certificats utilisateur.</span><span class="sxs-lookup"><span data-stu-id="a7fbd-111">If this value is SCARD\_ENROLL\_USER\_CERT\_TEMPLATE (defined as 1), the enumeration applies to user certificate templates.</span></span> <span data-ttu-id="a7fbd-112">Si cette valeur est \_ \_ \_ \_ un modèle de certificat d’ordinateur d’inscription cicatrice (défini sur 2), l’énumération s’applique aux modèles de certificat d’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="a7fbd-112">If this value is SCARD\_ENROLL\_MACHINE\_CERT\_TEMPLATE (defined as 2), the enumeration applies to machine certificate templates.</span></span>

</dd> <dt>

<span data-ttu-id="a7fbd-113">*pbstrCertTemplateName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="a7fbd-113">*pbstrCertTemplateName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a7fbd-114">Pointeur vers une chaîne qui retourne le nom du modèle de certificat énuméré.</span><span class="sxs-lookup"><span data-stu-id="a7fbd-114">A pointer to a string that returns the name of the enumerated certificate template.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a7fbd-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="a7fbd-115">Return value</span></span>

### <a name="c"></a><span data-ttu-id="a7fbd-116">C++</span><span class="sxs-lookup"><span data-stu-id="a7fbd-116">C++</span></span>

<span data-ttu-id="a7fbd-117">Si la méthode est réussie, la méthode retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="a7fbd-117">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="a7fbd-118">Si la méthode échoue, elle retourne une valeur **HRESULT** qui indique l’erreur.</span><span class="sxs-lookup"><span data-stu-id="a7fbd-118">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="a7fbd-119">Pour obtenir la liste des codes d’erreur courants, consultez [valeurs HRESULT communes](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="a7fbd-119">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="a7fbd-120">VB</span><span class="sxs-lookup"><span data-stu-id="a7fbd-120">VB</span></span>

<span data-ttu-id="a7fbd-121">Chaîne qui contient le nom du modèle de certificat énuméré.</span><span class="sxs-lookup"><span data-stu-id="a7fbd-121">A string that contains the name of the enumerated certificate template.</span></span>

## <a name="requirements"></a><span data-ttu-id="a7fbd-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="a7fbd-122">Requirements</span></span>



| <span data-ttu-id="a7fbd-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="a7fbd-123">Requirement</span></span> | <span data-ttu-id="a7fbd-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="a7fbd-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a7fbd-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a7fbd-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a7fbd-126">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="a7fbd-126">None supported</span></span><br/>                                                               |
| <span data-ttu-id="a7fbd-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="a7fbd-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a7fbd-128">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="a7fbd-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="a7fbd-129">DLL</span><span class="sxs-lookup"><span data-stu-id="a7fbd-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a7fbd-130"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a7fbd-130"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="a7fbd-131">IID</span><span class="sxs-lookup"><span data-stu-id="a7fbd-131">IID</span></span><br/>                      | <span data-ttu-id="a7fbd-132">IID \_ ISCrdEnr est défini en tant que 753988a1-1357-436D-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="a7fbd-132">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="a7fbd-133">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="a7fbd-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7fbd-134">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="a7fbd-134">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="a7fbd-135">**ISCrdEnr::getCertTemplateCount**</span><span class="sxs-lookup"><span data-stu-id="a7fbd-135">**ISCrdEnr::getCertTemplateCount**</span></span>](iscrdenr-getcerttemplatecount.md)
</dt> <dt>

[<span data-ttu-id="a7fbd-136">**ISCrdEnr::getCertTemplateName**</span><span class="sxs-lookup"><span data-stu-id="a7fbd-136">**ISCrdEnr::getCertTemplateName**</span></span>](iscrdenr-getcerttemplatename.md)
</dt> <dt>

[<span data-ttu-id="a7fbd-137">**ISCrdEnr::setCertTemplateName**</span><span class="sxs-lookup"><span data-stu-id="a7fbd-137">**ISCrdEnr::setCertTemplateName**</span></span>](iscrdenr-setcerttemplatename.md)
</dt> </dl>

 

 




