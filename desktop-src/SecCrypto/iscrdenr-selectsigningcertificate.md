---
description: Affiche une boîte de dialogue Sélectionner un certificat, qui permet de sélectionner un certificat de signature (également appelé certificat de l’agent d’inscription).
ms.assetid: b8198f65-4ffb-4dfa-8286-e62ef483ab16
title: 'ISCrdEnr :: selectSigningCertificate, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.selectSigningCertificate
- SCrdEnr.selectSigningCertificate
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: a4ef3be0ef16797597f57c12e90736ba50109601
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868206"
---
# <a name="iscrdenrselectsigningcertificate-method"></a><span data-ttu-id="6a5d2-103">ISCrdEnr :: selectSigningCertificate, méthode</span><span class="sxs-lookup"><span data-stu-id="6a5d2-103">ISCrdEnr::selectSigningCertificate method</span></span>

<span data-ttu-id="6a5d2-104">La méthode **selectSigningCertificate** affiche une boîte de dialogue **Sélectionner un certificat** , qui permet de sélectionner un certificat de signature (également appelé *certificat de l’agent d’inscription*).</span><span class="sxs-lookup"><span data-stu-id="6a5d2-104">The **selectSigningCertificate** method displays a **Select Certificate** dialog box, allowing a signing certificate (also known as the *enrollment agent certificate*) to be selected.</span></span>

<span data-ttu-id="6a5d2-105">Avant de procéder à l’inscription au nom des utilisateurs, vous devez sélectionner un certificat de signature.</span><span class="sxs-lookup"><span data-stu-id="6a5d2-105">Before enrolling on behalf of users, you must select a signing certificate.</span></span> <span data-ttu-id="6a5d2-106">La [*clé privée*](../secgloss/p-gly.md) associée à ce certificat de signature est utilisée pour signer une \# demande PKCS 7.</span><span class="sxs-lookup"><span data-stu-id="6a5d2-106">The [*private key*](../secgloss/p-gly.md) associated with this signing certificate is used to sign a PKCS \#7 request.</span></span> <span data-ttu-id="6a5d2-107">Le PKCS \# 7, quant à lui, contient la requête PKCS 10 de l’utilisateur \# (qui est signée avec la clé privée de l’utilisateur).</span><span class="sxs-lookup"><span data-stu-id="6a5d2-107">The PKCS \#7, in turn, contains the user's PKCS \#10 request (which is signed with the user's private key).</span></span>

## <a name="syntax"></a><span data-ttu-id="6a5d2-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="6a5d2-108">Syntax</span></span>


```C++
HRESULT selectSigningCertificate(
  [in] DWORD dwFlags,
  [in] BSTR bstrCertTemplateName
);
```


```VB

SCrdEnr.selectSigningCertificate( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName _
)
```





## <a name="parameters"></a><span data-ttu-id="6a5d2-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="6a5d2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6a5d2-110">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6a5d2-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a5d2-111">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="6a5d2-111">Reserved for future use.</span></span> <span data-ttu-id="6a5d2-112">Définissez cette valeur sur zéro.</span><span class="sxs-lookup"><span data-stu-id="6a5d2-112">Set this value to zero.</span></span>

</dd> <dt>

<span data-ttu-id="6a5d2-113">*bstrCertTemplateName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="6a5d2-113">*bstrCertTemplateName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6a5d2-114">Chaîne qui représente le nom du modèle de certificat pour le certificat de signature.</span><span class="sxs-lookup"><span data-stu-id="6a5d2-114">A string that represents the name of the certificate template for the signing certificate.</span></span> <span data-ttu-id="6a5d2-115">Vous pouvez utiliser la valeur « EnrollmentAgent » si vous avez obtenu un certificat EnrollmentAgent.</span><span class="sxs-lookup"><span data-stu-id="6a5d2-115">You can use the value "EnrollmentAgent" if you have obtained an EnrollmentAgent certificate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6a5d2-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="6a5d2-116">Return value</span></span>

### <a name="vb"></a><span data-ttu-id="6a5d2-117">VB</span><span class="sxs-lookup"><span data-stu-id="6a5d2-117">VB</span></span>

<span data-ttu-id="6a5d2-118">Si la méthode est réussie, la méthode retourne **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="6a5d2-118">If the method succeeds, the method returns **S\_OK**.</span></span>

<span data-ttu-id="6a5d2-119">Si la méthode échoue, elle retourne une valeur **HRESULT** qui indique l’erreur.</span><span class="sxs-lookup"><span data-stu-id="6a5d2-119">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="6a5d2-120">Pour obtenir la liste des codes d’erreur courants, consultez [valeurs HRESULT communes](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="6a5d2-120">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6a5d2-121">Notes</span><span class="sxs-lookup"><span data-stu-id="6a5d2-121">Remarks</span></span>

<span data-ttu-id="6a5d2-122">Avant de procéder à l’inscription pour le compte d’un utilisateur, vous devez d’abord obtenir un certificat de signature.</span><span class="sxs-lookup"><span data-stu-id="6a5d2-122">Before enrolling on behalf of a user, you must first obtain a signing certificate.</span></span> <span data-ttu-id="6a5d2-123">Vous pouvez obtenir un certificat de signature à l’aide du composant logiciel enfichable MMC du gestionnaire de certificats.</span><span class="sxs-lookup"><span data-stu-id="6a5d2-123">You can obtain a signing certificate by using the Certificate Manager MMC snap-in.</span></span> <span data-ttu-id="6a5d2-124">La méthode **selectSigningCertificate** n’obtient pas le certificat de signature, mais affiche une boîte de dialogue des certificats de signature précédemment obtenus, ce qui vous permet de choisir le certificat qui sera utilisé pour signer les demandes d’inscription à la place.</span><span class="sxs-lookup"><span data-stu-id="6a5d2-124">The **selectSigningCertificate** method does not obtain the signing certificate but displays a dialog box of previously obtained signing certificates, allowing you to choose which certificate will be used to sign the enroll-on-behalf requests.</span></span>

<span data-ttu-id="6a5d2-125">Une alternative à **selectSigningCertificate** est [**ISCrdEnr :: setSigningCertificate**](iscrdenr-setsigningcertificate.md).</span><span class="sxs-lookup"><span data-stu-id="6a5d2-125">An alternative to **selectSigningCertificate** is [**ISCrdEnr::setSigningCertificate**](iscrdenr-setsigningcertificate.md).</span></span>

<span data-ttu-id="6a5d2-126">Une fois le certificat de signature sélectionné, son nom peut être récupéré en appelant [**ISCrdEnr :: getSigningCertificateName**](iscrdenr-getsigningcertificatename.md).</span><span class="sxs-lookup"><span data-stu-id="6a5d2-126">After a signing certificate is selected, its name can be retrieved by calling [**ISCrdEnr::getSigningCertificateName**](iscrdenr-getsigningcertificatename.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6a5d2-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="6a5d2-127">Requirements</span></span>



| <span data-ttu-id="6a5d2-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="6a5d2-128">Requirement</span></span> | <span data-ttu-id="6a5d2-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="6a5d2-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6a5d2-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a5d2-130">Minimum supported client</span></span><br/> | <span data-ttu-id="6a5d2-131">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a5d2-131">None supported</span></span><br/>                                                               |
| <span data-ttu-id="6a5d2-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="6a5d2-132">Minimum supported server</span></span><br/> | <span data-ttu-id="6a5d2-133">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="6a5d2-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6a5d2-134">DLL</span><span class="sxs-lookup"><span data-stu-id="6a5d2-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6a5d2-135"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6a5d2-135"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="6a5d2-136">IID</span><span class="sxs-lookup"><span data-stu-id="6a5d2-136">IID</span></span><br/>                      | <span data-ttu-id="6a5d2-137">IID \_ ISCrdEnr est défini en tant que 753988a1-1357-436D-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="6a5d2-137">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="6a5d2-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="6a5d2-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a5d2-139">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="6a5d2-139">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="6a5d2-140">**ISCrdEnr::getSigningCertificateName**</span><span class="sxs-lookup"><span data-stu-id="6a5d2-140">**ISCrdEnr::getSigningCertificateName**</span></span>](iscrdenr-getsigningcertificatename.md)
</dt> </dl>

 

 
