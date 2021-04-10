---
description: Récupère le nombre de modèles de certificats.
ms.assetid: f56e6e72-1562-4c53-b0da-b4bc69511559
title: 'ISCrdEnr :: getCertTemplateCount, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCertTemplateCount
- SCrdEnr.getCertTemplateCount
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 86a78f03929bc6cdcfc7b611944b81c59a1c9fc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868209"
---
# <a name="iscrdenrgetcerttemplatecount-method"></a><span data-ttu-id="65449-103">ISCrdEnr :: getCertTemplateCount, méthode</span><span class="sxs-lookup"><span data-stu-id="65449-103">ISCrdEnr::getCertTemplateCount method</span></span>

<span data-ttu-id="65449-104">La méthode **getCertTemplateCount** récupère le nombre de modèles de certificats.</span><span class="sxs-lookup"><span data-stu-id="65449-104">The **getCertTemplateCount** method retrieves the number of certificate templates.</span></span>

## <a name="syntax"></a><span data-ttu-id="65449-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="65449-105">Syntax</span></span>


```C++
HRESULT getCertTemplateCount(
  [in]  DWORD     dwFlags,
  [out] LONG *pdwCertTemplateCount
);
```


```VB

SCrdEnr.getCertTemplateCount( _
  ByVal dwFlags, _
  ByRef pdwCertTemplateCount _
)
```





## <a name="parameters"></a><span data-ttu-id="65449-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="65449-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65449-107">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="65449-107">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="65449-108">Valeur qui détermine si le modèle est pour les certificats d’utilisateur ou d’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="65449-108">A value that determines whether the template is for user or machine certificates.</span></span> <span data-ttu-id="65449-109">Si cette valeur est \_ \_ \_ \_ un modèle de certificat de l’utilisateur avec un quota d’utilisateurs cicatrices (défini sur 1), le nombre renvoyé sera pour les modèles de certificats utilisateur.</span><span class="sxs-lookup"><span data-stu-id="65449-109">If this value is SCARD\_ENROLL\_USER\_CERT\_TEMPLATE (defined as 1) then the returned count will be for user certificate templates.</span></span> <span data-ttu-id="65449-110">Si cette valeur est \_ \_ \_ \_ un modèle de certificat d’ordinateur d’inscription cicatrice (défini sur 2), le nombre retourné sera pour les modèles de certificat d’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="65449-110">If this value is SCARD\_ENROLL\_MACHINE\_CERT\_TEMPLATE (defined as 2) then the returned count will be for machine certificate templates.</span></span>

</dd> <dt>

<span data-ttu-id="65449-111">*pdwCertTemplateCount* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="65449-111">*pdwCertTemplateCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="65449-112">Pointeur vers une **valeur de type long** qui retourne le nombre de modèles de certificats.</span><span class="sxs-lookup"><span data-stu-id="65449-112">A pointer to a **LONG** that returns the number of certificate templates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65449-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="65449-113">Return value</span></span>

### <a name="c"></a><span data-ttu-id="65449-114">C++</span><span class="sxs-lookup"><span data-stu-id="65449-114">C++</span></span>

<span data-ttu-id="65449-115">Si la méthode est réussie, la méthode retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="65449-115">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="65449-116">Si la méthode échoue, elle retourne une valeur **HRESULT** qui indique l’erreur.</span><span class="sxs-lookup"><span data-stu-id="65449-116">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="65449-117">Pour obtenir la liste des codes d’erreur courants, consultez [valeurs HRESULT communes](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="65449-117">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="65449-118">VB</span><span class="sxs-lookup"><span data-stu-id="65449-118">VB</span></span>

<span data-ttu-id="65449-119">Valeur de **type long** qui représente le nombre de modèles de certificats.</span><span class="sxs-lookup"><span data-stu-id="65449-119">A **Long** value that represents the number of certificate templates.</span></span>

## <a name="requirements"></a><span data-ttu-id="65449-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="65449-120">Requirements</span></span>



| <span data-ttu-id="65449-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="65449-121">Requirement</span></span> | <span data-ttu-id="65449-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="65449-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="65449-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65449-123">Minimum supported client</span></span><br/> | <span data-ttu-id="65449-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="65449-124">None supported</span></span><br/>                                                               |
| <span data-ttu-id="65449-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="65449-125">Minimum supported server</span></span><br/> | <span data-ttu-id="65449-126">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="65449-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="65449-127">DLL</span><span class="sxs-lookup"><span data-stu-id="65449-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="65449-128"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="65449-128"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="65449-129">IID</span><span class="sxs-lookup"><span data-stu-id="65449-129">IID</span></span><br/>                      | <span data-ttu-id="65449-130">IID \_ ISCrdEnr est défini en tant que 753988a1-1357-436D-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="65449-130">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="65449-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="65449-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65449-132">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="65449-132">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="65449-133">**ISCrdEnr::enumCertTemplateName**</span><span class="sxs-lookup"><span data-stu-id="65449-133">**ISCrdEnr::enumCertTemplateName**</span></span>](iscrdenr-enumcerttemplatename.md)
</dt> </dl>

 

 




