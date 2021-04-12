---
description: Récupère le nom du modèle de certificat.
ms.assetid: 26fd758a-b348-4efb-841b-c8f2ab88efea
title: 'ISCrdEnr :: getCertTemplateName, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCertTemplateName
- SCrdEnr.getCertTemplateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 4eee84140e0a23b8a0dd5d26099ca61b868a90fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210243"
---
# <a name="iscrdenrgetcerttemplatename-method"></a><span data-ttu-id="fb866-103">ISCrdEnr :: getCertTemplateName, méthode</span><span class="sxs-lookup"><span data-stu-id="fb866-103">ISCrdEnr::getCertTemplateName method</span></span>

<span data-ttu-id="fb866-104">La méthode **getCertTemplateName** récupère le nom du modèle de certificat.</span><span class="sxs-lookup"><span data-stu-id="fb866-104">The **getCertTemplateName** method retrieves the name of the certificate template.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb866-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fb866-105">Syntax</span></span>


```C++
HRESULT getCertTemplateName(
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrCertTemplateName
);
```


```VB

SCrdEnr.getCertTemplateName( _
  ByVal dwFlags, _
  ByRef pbstrCertTemplateName _
)
```





## <a name="parameters"></a><span data-ttu-id="fb866-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fb866-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb866-107">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="fb866-107">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb866-108">Valeur qui détermine si le nom réel ou le nom complet du modèle de certificat est retourné.</span><span class="sxs-lookup"><span data-stu-id="fb866-108">A value that determines whether the certificate template's real name or display name is returned.</span></span> <span data-ttu-id="fb866-109">Si la valeur de *dwFlags* est le \_ \_ \_ nom complet du \_ modèle \_ de certificat d’inscription au nouveau, le nom complet du modèle de certificat est récupéré ; sinon, le nom réel du modèle de certificat s’affiche.</span><span class="sxs-lookup"><span data-stu-id="fb866-109">If *dwFlags* has the value SCARD\_ENROLL\_CERT\_TEMPLATE\_DISPLAY\_NAME, the certificate template's display name is retrieved; otherwise, the real name of the certificate template is displayed.</span></span>

</dd> <dt>

<span data-ttu-id="fb866-110">*pbstrCertTemplateName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="fb866-110">*pbstrCertTemplateName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb866-111">Pointeur vers une chaîne qui retourne le nom du modèle de certificat qui sera utilisé dans la demande de [*certificat*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="fb866-111">A pointer to a string that returns the name of the certificate template which will be used in the [*certificate request*](../secgloss/c-gly.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb866-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fb866-112">Return value</span></span>

### <a name="c"></a><span data-ttu-id="fb866-113">C++</span><span class="sxs-lookup"><span data-stu-id="fb866-113">C++</span></span>

<span data-ttu-id="fb866-114">Si la méthode est réussie, la méthode retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="fb866-114">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="fb866-115">Si la méthode échoue, elle retourne une valeur **HRESULT** qui indique l’erreur.</span><span class="sxs-lookup"><span data-stu-id="fb866-115">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="fb866-116">Pour obtenir la liste des codes d’erreur courants, consultez [valeurs HRESULT communes](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="fb866-116">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="fb866-117">VB</span><span class="sxs-lookup"><span data-stu-id="fb866-117">VB</span></span>

<span data-ttu-id="fb866-118">Chaîne qui représente le nom du modèle de certificat qui sera utilisé dans la demande de [*certificat*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="fb866-118">A string that represents the name of the certificate template which will be used in the [*certificate request*](../secgloss/c-gly.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fb866-119">Notes</span><span class="sxs-lookup"><span data-stu-id="fb866-119">Remarks</span></span>

<span data-ttu-id="fb866-120">Si vous ne définissez pas le nom du modèle de certificat en appelant [**ISCrdEnr :: setCertTemplateName**](iscrdenr-setcerttemplatename.md), le nom par défaut est le prénom dans la liste des modèles de certificats disponibles.</span><span class="sxs-lookup"><span data-stu-id="fb866-120">If you do not set the certificate template name by calling [**ISCrdEnr::setCertTemplateName**](iscrdenr-setcerttemplatename.md), the name defaults to the first name in the list of available certificate templates.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb866-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fb866-121">Requirements</span></span>



| <span data-ttu-id="fb866-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fb866-122">Requirement</span></span> | <span data-ttu-id="fb866-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="fb866-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb866-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fb866-124">Minimum supported client</span></span><br/> | <span data-ttu-id="fb866-125">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="fb866-125">None supported</span></span><br/>                                                               |
| <span data-ttu-id="fb866-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="fb866-126">Minimum supported server</span></span><br/> | <span data-ttu-id="fb866-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="fb866-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="fb866-128">DLL</span><span class="sxs-lookup"><span data-stu-id="fb866-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb866-129"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fb866-129"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="fb866-130">IID</span><span class="sxs-lookup"><span data-stu-id="fb866-130">IID</span></span><br/>                      | <span data-ttu-id="fb866-131">IID \_ ISCrdEnr est défini en tant que 753988a1-1357-436D-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="fb866-131">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="fb866-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fb866-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb866-133">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="fb866-133">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="fb866-134">**ISCrdEnr::setCertTemplateName**</span><span class="sxs-lookup"><span data-stu-id="fb866-134">**ISCrdEnr::setCertTemplateName**</span></span>](iscrdenr-setcerttemplatename.md)
</dt> </dl>

 

 
