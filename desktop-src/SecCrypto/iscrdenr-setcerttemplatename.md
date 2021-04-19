---
description: Spécifie le nom du modèle de certificat.
ms.assetid: 15d22130-e614-4505-94e8-83c2efbf6d87
title: 'ISCrdEnr :: setCertTemplateName, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.setCertTemplateName
- SCrdEnr.setCertTemplateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 53ba18626a7d2bb703ed4d11953fb4872cf9257c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531971"
---
# <a name="iscrdenrsetcerttemplatename-method"></a><span data-ttu-id="6ff73-103">ISCrdEnr :: setCertTemplateName, méthode</span><span class="sxs-lookup"><span data-stu-id="6ff73-103">ISCrdEnr::setCertTemplateName method</span></span>

<span data-ttu-id="6ff73-104">La méthode **setCertTemplateName** spécifie le nom du modèle de certificat.</span><span class="sxs-lookup"><span data-stu-id="6ff73-104">The **setCertTemplateName** method specifies the name of the certificate template.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ff73-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6ff73-105">Syntax</span></span>


```C++
HRESULT setCertTemplateName(
  [in] DWORD dwFlags,
  [in] BSTR bstrCertTemplateName
);
```


```VB

SCrdEnr.setCertTemplateName( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName _
)
```





## <a name="parameters"></a><span data-ttu-id="6ff73-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6ff73-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ff73-107">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6ff73-107">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ff73-108">Valeur qui détermine si le nom complet ou le nom réel du modèle de certificat est défini.</span><span class="sxs-lookup"><span data-stu-id="6ff73-108">Value which determines if the certificate template's real name or display name is being set.</span></span> <span data-ttu-id="6ff73-109">Si la valeur de *dwFlags* est le \_ \_ \_ nom complet du \_ modèle \_ de certificat d’inscription infinie, le nom complet du modèle de certificat est défini.</span><span class="sxs-lookup"><span data-stu-id="6ff73-109">If *dwFlags* has the value SCARD\_ENROLL\_CERT\_TEMPLATE\_DISPLAY\_NAME, the certificate template's display name is set.</span></span> <span data-ttu-id="6ff73-110">Dans le cas contraire, le nom réel du modèle de certificat est défini.</span><span class="sxs-lookup"><span data-stu-id="6ff73-110">Otherwise, the real name of the certificate template is set.</span></span>

</dd> <dt>

<span data-ttu-id="6ff73-111">*bstrCertTemplateName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6ff73-111">*bstrCertTemplateName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ff73-112">Nom du modèle de certificat qui sera utilisé dans la demande de certificat.</span><span class="sxs-lookup"><span data-stu-id="6ff73-112">Name of the certificate template which will be used in the certificate request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ff73-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6ff73-113">Return value</span></span>

### <a name="vb"></a><span data-ttu-id="6ff73-114">VB</span><span class="sxs-lookup"><span data-stu-id="6ff73-114">VB</span></span>

<span data-ttu-id="6ff73-115">Si la méthode est réussie, la méthode retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6ff73-115">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="6ff73-116">Si la méthode échoue, elle retourne une valeur **HRESULT** qui indique l’erreur.</span><span class="sxs-lookup"><span data-stu-id="6ff73-116">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="6ff73-117">Pour obtenir la liste des codes d’erreur courants, consultez [valeurs HRESULT communes](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="6ff73-117">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6ff73-118">Notes</span><span class="sxs-lookup"><span data-stu-id="6ff73-118">Remarks</span></span>

<span data-ttu-id="6ff73-119">Si vous ne définissez pas le nom du modèle de certificat en appelant **ISCrdEnr :: setCertTemplateName**, le nom par défaut est le prénom dans la liste des modèles de certificats disponibles.</span><span class="sxs-lookup"><span data-stu-id="6ff73-119">If you do not set the certificate template name by calling **ISCrdEnr::setCertTemplateName**, the name defaults to the first name in the list of available certificate templates.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ff73-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6ff73-120">Requirements</span></span>



| <span data-ttu-id="6ff73-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6ff73-121">Requirement</span></span> | <span data-ttu-id="6ff73-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="6ff73-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ff73-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6ff73-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6ff73-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="6ff73-124">None supported</span></span><br/>                                                               |
| <span data-ttu-id="6ff73-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6ff73-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6ff73-126">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6ff73-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6ff73-127">DLL</span><span class="sxs-lookup"><span data-stu-id="6ff73-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ff73-128"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ff73-128"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="6ff73-129">IID</span><span class="sxs-lookup"><span data-stu-id="6ff73-129">IID</span></span><br/>                      | <span data-ttu-id="6ff73-130">IID \_ ISCrdEnr est défini en tant que 753988a1-1357-436D-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="6ff73-130">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="6ff73-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6ff73-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ff73-132">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="6ff73-132">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="6ff73-133">**ISCrdEnr::getCertTemplateName**</span><span class="sxs-lookup"><span data-stu-id="6ff73-133">**ISCrdEnr::getCertTemplateName**</span></span>](iscrdenr-getcerttemplatename.md)
</dt> </dl>

 

 




