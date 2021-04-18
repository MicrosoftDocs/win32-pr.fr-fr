---
description: Spécifie un certificat de signature (également connu sous le nom de certificat de l’agent d’inscription).
ms.assetid: db2437a9-46f6-48c3-9630-82ec556df645
title: 'ISCrdEnr :: setSigningCertificate, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.setSigningCertificate
- SCrdEnr.setSigningCertificate
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: dd00ba19872cb0ba2b21981c79e8f7be03aa4937
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522828"
---
# <a name="iscrdenrsetsigningcertificate-method"></a><span data-ttu-id="c7301-103">ISCrdEnr :: setSigningCertificate, méthode</span><span class="sxs-lookup"><span data-stu-id="c7301-103">ISCrdEnr::setSigningCertificate method</span></span>

<span data-ttu-id="c7301-104">La méthode **setSigningCertificate** spécifie un certificat de signature (également appelé *certificat* de l’agent d’inscription).</span><span class="sxs-lookup"><span data-stu-id="c7301-104">The **setSigningCertificate** method specifies a signing certificate (also known as the *enrollment agent certificate*).</span></span>

<span data-ttu-id="c7301-105">Avant de procéder à l’inscription au nom des utilisateurs, vous devez sélectionner ou définir un certificat de signature.</span><span class="sxs-lookup"><span data-stu-id="c7301-105">Before enrolling on behalf of users, you must select or set a signing certificate.</span></span> <span data-ttu-id="c7301-106">La [*clé privée*](../secgloss/p-gly.md) associée à ce certificat de signature est utilisée pour signer une \# demande PKCS 7.</span><span class="sxs-lookup"><span data-stu-id="c7301-106">The [*private key*](../secgloss/p-gly.md) associated with this signing certificate is used to sign a PKCS \#7 request.</span></span> <span data-ttu-id="c7301-107">Le PKCS \# 7, quant à lui, contient la requête PKCS 10 de l’utilisateur \# (qui est signée avec la clé privée de l’utilisateur).</span><span class="sxs-lookup"><span data-stu-id="c7301-107">The PKCS \#7, in turn, contains the user's PKCS \#10 request (which is signed with the user's private key).</span></span>

## <a name="syntax"></a><span data-ttu-id="c7301-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c7301-108">Syntax</span></span>


```C++
HRESULT setSigningCertificate(
  [in] DWORD dwFlags,
  [in] BSTR bstrCertTemplateName
);
```


```VB

SCrdEnr.setSigningCertificate( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName _
)
```





## <a name="parameters"></a><span data-ttu-id="c7301-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="c7301-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c7301-110">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c7301-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7301-111">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="c7301-111">Reserved for future use.</span></span> <span data-ttu-id="c7301-112">Définissez cette valeur sur zéro.</span><span class="sxs-lookup"><span data-stu-id="c7301-112">Set this value to zero.</span></span>

</dd> <dt>

<span data-ttu-id="c7301-113">*bstrCertTemplateName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="c7301-113">*bstrCertTemplateName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c7301-114">Nom du modèle de certificat pour le certificat de signature.</span><span class="sxs-lookup"><span data-stu-id="c7301-114">Name of the certificate template for the signing certificate.</span></span> <span data-ttu-id="c7301-115">Vous pouvez utiliser la valeur « EnrollmentAgent » si vous avez obtenu un certificat EnrollmentAgent.</span><span class="sxs-lookup"><span data-stu-id="c7301-115">You can use the value "EnrollmentAgent" if you have obtained an EnrollmentAgent certificate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c7301-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="c7301-116">Return value</span></span>

### <a name="vb"></a><span data-ttu-id="c7301-117">VB</span><span class="sxs-lookup"><span data-stu-id="c7301-117">VB</span></span>

<span data-ttu-id="c7301-118">Si la méthode est réussie, la méthode retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c7301-118">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="c7301-119">Si la méthode échoue, elle retourne une valeur **HRESULT** qui indique l’erreur.</span><span class="sxs-lookup"><span data-stu-id="c7301-119">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="c7301-120">Pour obtenir la liste des codes d’erreur courants, consultez [valeurs HRESULT communes](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="c7301-120">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="c7301-121">Notes</span><span class="sxs-lookup"><span data-stu-id="c7301-121">Remarks</span></span>

<span data-ttu-id="c7301-122">Avant de procéder à l’inscription pour le compte d’un utilisateur, vous devez d’abord obtenir un certificat de signature.</span><span class="sxs-lookup"><span data-stu-id="c7301-122">Before enrolling on behalf of a user, you must first obtain a signing certificate.</span></span> <span data-ttu-id="c7301-123">Vous pouvez obtenir un certificat de signature à l’aide du composant logiciel enfichable MMC du gestionnaire de certificats.</span><span class="sxs-lookup"><span data-stu-id="c7301-123">You can obtain a signing certificate by using the Certificate Manager MMC snap-in.</span></span> <span data-ttu-id="c7301-124">La méthode **setSigningCertificate** n’obtient pas le certificat de signature, mais informe le contrôle d’inscription de carte à puce qui a précédemment obtenu le certificat de signature à utiliser.</span><span class="sxs-lookup"><span data-stu-id="c7301-124">The **setSigningCertificate** method does not obtain the signing certificate but informs the Smart Card Enrollment Control which previously obtained signing certificate to use.</span></span> <span data-ttu-id="c7301-125">La méthode **setSigningCertificate** recherche le certificat de signature le plus récent correspondant au modèle de certificat spécifié par *bstrCertTemplateName* dans le magasin My de l’appelant.</span><span class="sxs-lookup"><span data-stu-id="c7301-125">The **setSigningCertificate** method searches the caller's "My" store for the most recent signing certificate corresponding to the certificate template specified by *bstrCertTemplateName*.</span></span>

<span data-ttu-id="c7301-126">Une alternative à **setSigningCertificate** est **ISCrdEnr :: setSigningCertificate**.</span><span class="sxs-lookup"><span data-stu-id="c7301-126">An alternative to **setSigningCertificate** is **ISCrdEnr::setSigningCertificate**.</span></span>

<span data-ttu-id="c7301-127">Une fois le certificat de signature défini, son nom peut être récupéré en appelant [**ISCrdEnr :: getSigningCertificateName**](iscrdenr-getsigningcertificatename.md).</span><span class="sxs-lookup"><span data-stu-id="c7301-127">After a signing certificate is set, its name can be retrieved by calling [**ISCrdEnr::getSigningCertificateName**](iscrdenr-getsigningcertificatename.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c7301-128">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c7301-128">Requirements</span></span>



| <span data-ttu-id="c7301-129">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c7301-129">Requirement</span></span> | <span data-ttu-id="c7301-130">Valeur</span><span class="sxs-lookup"><span data-stu-id="c7301-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c7301-131">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7301-131">Minimum supported client</span></span><br/> | <span data-ttu-id="c7301-132">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7301-132">None supported</span></span><br/>                                                               |
| <span data-ttu-id="c7301-133">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c7301-133">Minimum supported server</span></span><br/> | <span data-ttu-id="c7301-134">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c7301-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c7301-135">DLL</span><span class="sxs-lookup"><span data-stu-id="c7301-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7301-136"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7301-136"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="c7301-137">IID</span><span class="sxs-lookup"><span data-stu-id="c7301-137">IID</span></span><br/>                      | <span data-ttu-id="c7301-138">IID \_ ISCrdEnr est défini en tant que 753988a1-1357-436D-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="c7301-138">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="c7301-139">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c7301-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7301-140">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="c7301-140">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="c7301-141">**ISCrdEnr::getSigningCertificateName**</span><span class="sxs-lookup"><span data-stu-id="c7301-141">**ISCrdEnr::getSigningCertificateName**</span></span>](iscrdenr-getsigningcertificatename.md)
</dt> </dl>

 

 
