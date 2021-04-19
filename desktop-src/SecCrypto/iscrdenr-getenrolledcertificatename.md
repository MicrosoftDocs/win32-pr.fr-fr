---
description: 'Récupère le nom du certificat résultant d’un appel antérieur réussi à ISCrdEnr :: Enroll.'
ms.assetid: e33b217a-b717-49bd-b0f3-3ba9229a0696
title: 'ISCrdEnr :: getEnrolledCertificateName, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getEnrolledCertificateName
- SCrdEnr.getEnrolledCertificateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: e3c9640e7719d2b5ac0e576384246cda5e1b2bfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520684"
---
# <a name="iscrdenrgetenrolledcertificatename-method"></a><span data-ttu-id="43a27-103">ISCrdEnr :: getEnrolledCertificateName, méthode</span><span class="sxs-lookup"><span data-stu-id="43a27-103">ISCrdEnr::getEnrolledCertificateName method</span></span>

<span data-ttu-id="43a27-104">La méthode **getEnrolledCertificateName** récupère le nom du certificat résultant d’un appel antérieur réussi à [**ISCrdEnr :: ENROLL**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="43a27-104">The **getEnrolledCertificateName** method retrieves the name of the certificate resulting from an earlier successful call to [**ISCrdEnr::enroll**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85)).</span></span>

<span data-ttu-id="43a27-105">Cette méthode peut également être utilisée pour afficher le certificat dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="43a27-105">This method can also be used to display the certificate in a dialog box.</span></span> <span data-ttu-id="43a27-106">Cette méthode appelle la [](../secgloss/c-gly.md) fonction CryptoAPI [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa).</span><span class="sxs-lookup"><span data-stu-id="43a27-106">This method calls the [*CryptoAPI*](../secgloss/c-gly.md) function [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa).</span></span>

## <a name="syntax"></a><span data-ttu-id="43a27-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="43a27-107">Syntax</span></span>


```C++
HRESULT getEnrolledCertificateName(
  [in]  DWORD     dwFlags,
  [out] BSTR *pBstrCertName
);
```


```VB

SCrdEnr.getEnrolledCertificateName( _
  ByVal dwFlags, _
  ByRef pBstrCertName _
)
```





## <a name="parameters"></a><span data-ttu-id="43a27-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="43a27-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43a27-109">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="43a27-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43a27-110">Valeur qui détermine si le certificat est affiché dans une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="43a27-110">A value that determines whether the certificate is displayed in a dialog box.</span></span> <span data-ttu-id="43a27-111">Si cette valeur est \_ \_ \_ \_ incorrecte inscrire aucun certificat d’affichage (défini comme 0x01), le certificat inscrit n’est pas affiché ; toute autre valeur entraîne l’affichage du certificat inscrit dans la boîte de dialogue **certificat** .</span><span class="sxs-lookup"><span data-stu-id="43a27-111">If this value is SCARD\_ENROLL\_NO\_DISPLAY\_CERT (defined as 0x01), the enrolled certificate is not displayed; any other values cause the enrolled certificate to be displayed in the **Certificate** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="43a27-112">*pBstrCertName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="43a27-112">*pBstrCertName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="43a27-113">Pointeur vers une chaîne qui retourne le nom du certificat récupéré.</span><span class="sxs-lookup"><span data-stu-id="43a27-113">A pointer to a string that returns the retrieved certificate name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43a27-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="43a27-114">Return value</span></span>

### <a name="c"></a><span data-ttu-id="43a27-115">C++</span><span class="sxs-lookup"><span data-stu-id="43a27-115">C++</span></span>

<span data-ttu-id="43a27-116">Si la méthode est réussie, la méthode retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="43a27-116">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="43a27-117">Si la méthode échoue, elle retourne une valeur **HRESULT** qui indique l’erreur.</span><span class="sxs-lookup"><span data-stu-id="43a27-117">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="43a27-118">Pour obtenir la liste des codes d’erreur courants, consultez [valeurs HRESULT communes](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="43a27-118">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="43a27-119">VB</span><span class="sxs-lookup"><span data-stu-id="43a27-119">VB</span></span>

<span data-ttu-id="43a27-120">Chaîne qui représente le nom du certificat récupéré.</span><span class="sxs-lookup"><span data-stu-id="43a27-120">A string that represents the retrieved certificate name.</span></span>

## <a name="remarks"></a><span data-ttu-id="43a27-121">Notes</span><span class="sxs-lookup"><span data-stu-id="43a27-121">Remarks</span></span>

<span data-ttu-id="43a27-122">Étant donné que cette méthode fonctionne sur un certificat existant, vous devez avoir appelé [**ISCrdEnr :: ENROLL**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85)) avant de pouvoir appeler **getEnrolledCertificateName**.</span><span class="sxs-lookup"><span data-stu-id="43a27-122">Because this method operates on an existing certificate, you must have successfully called [**ISCrdEnr::enroll**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85)) before you can call **getEnrolledCertificateName**.</span></span>

<span data-ttu-id="43a27-123">La méthode **getEnrolledCertificateName** appelle la fonction [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa) pour récupérer le nom du certificat en fonction de la séquence décrite pour la \_ \_ \_ valeur de type d’affichage simple du nom de certificat \_ du paramètre *dwType* de **CertGetNameString**.</span><span class="sxs-lookup"><span data-stu-id="43a27-123">The **getEnrolledCertificateName** method calls the [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa) function to retrieve the certificate name according to the sequence described for the CERT\_NAME\_SIMPLE\_DISPLAY\_TYPE value of **CertGetNameString**'s *dwType* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="43a27-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="43a27-124">Requirements</span></span>



| <span data-ttu-id="43a27-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="43a27-125">Requirement</span></span> | <span data-ttu-id="43a27-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="43a27-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="43a27-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="43a27-127">Minimum supported client</span></span><br/> | <span data-ttu-id="43a27-128">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="43a27-128">None supported</span></span><br/>                                                               |
| <span data-ttu-id="43a27-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="43a27-129">Minimum supported server</span></span><br/> | <span data-ttu-id="43a27-130">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="43a27-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="43a27-131">DLL</span><span class="sxs-lookup"><span data-stu-id="43a27-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43a27-132"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43a27-132"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="43a27-133">IID</span><span class="sxs-lookup"><span data-stu-id="43a27-133">IID</span></span><br/>                      | <span data-ttu-id="43a27-134">IID \_ ISCrdEnr est défini en tant que 753988a1-1357-436D-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="43a27-134">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="43a27-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43a27-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43a27-136">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="43a27-136">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

<span data-ttu-id="43a27-137">[**ISCrdEnr :: inscrire**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="43a27-137">[**ISCrdEnr::enroll**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))</span></span>
</dt> </dl>

 

 
