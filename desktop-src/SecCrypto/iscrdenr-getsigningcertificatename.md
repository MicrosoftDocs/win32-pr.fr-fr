---
description: Récupère le nom du sujet à partir du certificat de signature.
ms.assetid: e50b1e12-ec89-4d58-aa57-dc24aa2409ef
title: 'ISCrdEnr :: getSigningCertificateName, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getSigningCertificateName
- SCrdEnr.getSigningCertificateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 8d9a8a84067e82a18e5066721f3e7f39d075c339
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104393692"
---
# <a name="iscrdenrgetsigningcertificatename-method"></a><span data-ttu-id="4f7a3-103">ISCrdEnr :: getSigningCertificateName, méthode</span><span class="sxs-lookup"><span data-stu-id="4f7a3-103">ISCrdEnr::getSigningCertificateName method</span></span>

<span data-ttu-id="4f7a3-104">La méthode **getSigningCertificateName** récupère le nom du sujet à partir du certificat de signature.</span><span class="sxs-lookup"><span data-stu-id="4f7a3-104">The **getSigningCertificateName** method retrieves the subject name from the signing certificate.</span></span>

<span data-ttu-id="4f7a3-105">Cette méthode peut également être utilisée pour afficher le certificat dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="4f7a3-105">This method can also be used to display the certificate in a dialog box.</span></span> <span data-ttu-id="4f7a3-106">Cette méthode appelle la [](../secgloss/c-gly.md) fonction CryptoAPI [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa).</span><span class="sxs-lookup"><span data-stu-id="4f7a3-106">This method calls the [*CryptoAPI*](../secgloss/c-gly.md) function [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa).</span></span>

## <a name="syntax"></a><span data-ttu-id="4f7a3-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="4f7a3-107">Syntax</span></span>


```C++
HRESULT getSigningCertificateName(
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrSigningCertName
);
```


```VB

SCrdEnr.getSigningCertificateName( _
  ByVal dwFlags, _
  ByRef pbstrSigningCertName _
)
```





## <a name="parameters"></a><span data-ttu-id="4f7a3-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="4f7a3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f7a3-109">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="4f7a3-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4f7a3-110">Valeur qui détermine si le certificat est affiché dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="4f7a3-110">A value that determines whether the certificate is displayed in a dialog box.</span></span> <span data-ttu-id="4f7a3-111">Si cette valeur est \_ \_ incorrecte inscrire aucun certificat d' \_ affichage \_ (défini comme 0x01), le certificat de signature n’est pas affiché ; toutes les autres valeurs entraînent l’affichage du certificat de signature dans la boîte de dialogue **certificat** .</span><span class="sxs-lookup"><span data-stu-id="4f7a3-111">If this value is SCARD\_ENROLL\_NO\_DISPLAY\_CERT (defined as 0x01), the signing certificate is not displayed; any other values result in the signing certificate being displayed in the **Certificate** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="4f7a3-112">*pbstrSigningCertName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="4f7a3-112">*pbstrSigningCertName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4f7a3-113">Pointeur vers une chaîne qui retourne le nom du certificat de signature.</span><span class="sxs-lookup"><span data-stu-id="4f7a3-113">A pointer to a string that returns the name of the signing certificate.</span></span> <span data-ttu-id="4f7a3-114">Le certificat de signature est utilisé pour signer la [*demande de certificat*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="4f7a3-114">The signing certificate will be used to sign the [*certificate request*](../secgloss/c-gly.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4f7a3-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="4f7a3-115">Return value</span></span>

### <a name="c"></a><span data-ttu-id="4f7a3-116">C++</span><span class="sxs-lookup"><span data-stu-id="4f7a3-116">C++</span></span>

<span data-ttu-id="4f7a3-117">Si la méthode est réussie, la méthode retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="4f7a3-117">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="4f7a3-118">Si la méthode échoue, elle retourne une valeur **HRESULT** qui indique l’erreur.</span><span class="sxs-lookup"><span data-stu-id="4f7a3-118">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="4f7a3-119">Pour obtenir la liste des codes d’erreur courants, consultez [valeurs HRESULT communes](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="4f7a3-119">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="4f7a3-120">VB</span><span class="sxs-lookup"><span data-stu-id="4f7a3-120">VB</span></span>

<span data-ttu-id="4f7a3-121">Chaîne qui représente le nom du certificat de signature.</span><span class="sxs-lookup"><span data-stu-id="4f7a3-121">A string that represents the name of the signing certificate.</span></span> <span data-ttu-id="4f7a3-122">Le certificat de signature est utilisé pour signer la [*demande de certificat*](../secgloss/c-gly.md).</span><span class="sxs-lookup"><span data-stu-id="4f7a3-122">The signing certificate will be used to sign the [*certificate request*](../secgloss/c-gly.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="4f7a3-123">Notes</span><span class="sxs-lookup"><span data-stu-id="4f7a3-123">Remarks</span></span>

<span data-ttu-id="4f7a3-124">La méthode **getSigningCertificateName** retourne le nom du sujet du certificat que vous (ou un autre administrateur) avez sélectionné lors d’un appel précédent réussi à [**ISCrdEnr :: selectSigningCertificate**](iscrdenr-selectsigningcertificate.md) ou [**ISCrdEnr :: setSigningCertificate**](iscrdenr-setsigningcertificate.md).</span><span class="sxs-lookup"><span data-stu-id="4f7a3-124">The **getSigningCertificateName** method returns the subject name of the certificate you (or another administrator) have selected in a previous successful call to [**ISCrdEnr::selectSigningCertificate**](iscrdenr-selectsigningcertificate.md) or [**ISCrdEnr::setSigningCertificate**](iscrdenr-setsigningcertificate.md).</span></span> <span data-ttu-id="4f7a3-125">Cette méthode appelle la fonction [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa) pour récupérer le nom de l’objet en fonction de la séquence décrite pour la \_ \_ \_ \_ valeur de type d’affichage simple du nom de certificat du paramètre *dwType* de **CertGetNameString**.</span><span class="sxs-lookup"><span data-stu-id="4f7a3-125">This method calls the [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa) function to retrieve the subject name according to the sequence described for the CERT\_NAME\_SIMPLE\_DISPLAY\_TYPE value of **CertGetNameString**'s *dwType* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f7a3-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="4f7a3-126">Requirements</span></span>



| <span data-ttu-id="4f7a3-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="4f7a3-127">Requirement</span></span> | <span data-ttu-id="4f7a3-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="4f7a3-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f7a3-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f7a3-129">Minimum supported client</span></span><br/> | <span data-ttu-id="4f7a3-130">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f7a3-130">None supported</span></span><br/>                                                               |
| <span data-ttu-id="4f7a3-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="4f7a3-131">Minimum supported server</span></span><br/> | <span data-ttu-id="4f7a3-132">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="4f7a3-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4f7a3-133">DLL</span><span class="sxs-lookup"><span data-stu-id="4f7a3-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f7a3-134"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f7a3-134"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="4f7a3-135">IID</span><span class="sxs-lookup"><span data-stu-id="4f7a3-135">IID</span></span><br/>                      | <span data-ttu-id="4f7a3-136">IID \_ ISCrdEnr est défini en tant que 753988a1-1357-436D-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="4f7a3-136">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="4f7a3-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="4f7a3-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f7a3-138">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="4f7a3-138">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="4f7a3-139">**ISCrdEnr::selectSigningCertificate**</span><span class="sxs-lookup"><span data-stu-id="4f7a3-139">**ISCrdEnr::selectSigningCertificate**</span></span>](iscrdenr-selectsigningcertificate.md)
</dt> </dl>

 

 
