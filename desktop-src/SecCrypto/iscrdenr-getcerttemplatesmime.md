---
description: Utilisé pour déterminer si un modèle de certificat contient l' \_ utilisation de la clé de protection de messagerie szOID PKIX \_ \_ \_ .
ms.assetid: 1f0512e0-68b6-4b79-84bd-614babb4151d
title: 'ISCrdEnr :: getCertTemplateSMIME, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCertTemplateSMIME
- SCrdEnr.getCertTemplateSMIME
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 4ed66af6a8a91855fbfc5a972a8bf00358314663
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867398"
---
# <a name="iscrdenrgetcerttemplatesmime-method"></a><span data-ttu-id="d75b0-103">ISCrdEnr :: getCertTemplateSMIME, méthode</span><span class="sxs-lookup"><span data-stu-id="d75b0-103">ISCrdEnr::getCertTemplateSMIME method</span></span>

<span data-ttu-id="d75b0-104">La méthode **getCertTemplateSMIME** est utilisée pour déterminer si un modèle de certificat contient l' \_ utilisation de la clé de protection de \_ \_ courrier électronique szOID PKIX \_ .</span><span class="sxs-lookup"><span data-stu-id="d75b0-104">The **getCertTemplateSMIME** method is used to determine whether a certificate template contains the szOID\_PKIX\_KP\_EMAIL\_PROTECTION key usage.</span></span>

<span data-ttu-id="d75b0-105">Si l’utilisation de la clé fait partie du modèle de certificat, le modèle de certificat prend en charge les opérations S/MIME ( [*Secure/Multipurpose Internet Mail Extensions*](../secgloss/s-gly.md) ).</span><span class="sxs-lookup"><span data-stu-id="d75b0-105">If this key usage is part of the certificate template, the certificate template supports [*Secure/Multipurpose Internet Mail Extensions*](../secgloss/s-gly.md) (S/MIME) operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="d75b0-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d75b0-106">Syntax</span></span>


```C++
HRESULT getCertTemplateSMIME(
  [in]  BSTR      bstrCertTemplateName,
  [out] DWORD *pdwCertTemplateSMIME
);
```


```VB

SCrdEnr.getCertTemplateSMIME( _
  ByVal bstrCertTemplateName, _
  ByRef pdwCertTemplateSMIME _
)
```





## <a name="parameters"></a><span data-ttu-id="d75b0-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d75b0-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d75b0-108">*bstrCertTemplateName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d75b0-108">*bstrCertTemplateName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d75b0-109">Nom du certificat interrogé pour l’utilisation de la clé S/MIME.</span><span class="sxs-lookup"><span data-stu-id="d75b0-109">The name of the certificate being queried for the S/MIME key usage.</span></span>

</dd> <dt>

<span data-ttu-id="d75b0-110">*pdwCertTemplateSMIME* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="d75b0-110">*pdwCertTemplateSMIME* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d75b0-111">Pointeur vers une valeur **DWORD** qui retourne la valeur un si *bstrCertTemplateName* prend en charge S/MIME ; Sinon, elle retourne zéro.</span><span class="sxs-lookup"><span data-stu-id="d75b0-111">A pointer to a **DWORD** that returns a value of one if *bstrCertTemplateName* supports S/MIME; otherwise it returns zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d75b0-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d75b0-112">Return value</span></span>

### <a name="c"></a><span data-ttu-id="d75b0-113">C++</span><span class="sxs-lookup"><span data-stu-id="d75b0-113">C++</span></span>

<span data-ttu-id="d75b0-114">Si la méthode est réussie, la méthode retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d75b0-114">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="d75b0-115">Si la méthode échoue, elle retourne une valeur **HRESULT** qui indique l’erreur.</span><span class="sxs-lookup"><span data-stu-id="d75b0-115">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="d75b0-116">Pour obtenir la liste des codes d’erreur courants, consultez [valeurs HRESULT communes](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="d75b0-116">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="d75b0-117">VB</span><span class="sxs-lookup"><span data-stu-id="d75b0-117">VB</span></span>

<span data-ttu-id="d75b0-118">Valeur **longue** d’une si *bstrCertTemplateName* prend en charge S/MIME ; Sinon, zéro.</span><span class="sxs-lookup"><span data-stu-id="d75b0-118">**Long** value of one if *bstrCertTemplateName* supports S/MIME; otherwise zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="d75b0-119">Notes</span><span class="sxs-lookup"><span data-stu-id="d75b0-119">Remarks</span></span>

<span data-ttu-id="d75b0-120">La constante pour la \_ protection de la \_ messagerie électronique szOID PKIX \_ \_ est définie dans wincrypt. h.</span><span class="sxs-lookup"><span data-stu-id="d75b0-120">The constant for szOID\_PKIX\_KP\_EMAIL\_PROTECTION is defined in Wincrypt.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="d75b0-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d75b0-121">Requirements</span></span>



| <span data-ttu-id="d75b0-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d75b0-122">Requirement</span></span> | <span data-ttu-id="d75b0-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="d75b0-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d75b0-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d75b0-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d75b0-125">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="d75b0-125">None supported</span></span><br/>                                                               |
| <span data-ttu-id="d75b0-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d75b0-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d75b0-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d75b0-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d75b0-128">DLL</span><span class="sxs-lookup"><span data-stu-id="d75b0-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d75b0-129"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d75b0-129"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="d75b0-130">IID</span><span class="sxs-lookup"><span data-stu-id="d75b0-130">IID</span></span><br/>                      | <span data-ttu-id="d75b0-131">IID \_ ISCrdEnr est défini en tant que 753988a1-1357-436D-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="d75b0-131">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="d75b0-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d75b0-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d75b0-133">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="d75b0-133">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

<span data-ttu-id="d75b0-134">[**ISCrdEnr :: inscrire**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d75b0-134">[**ISCrdEnr::enroll**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))</span></span>
</dt> </dl>

 

 
