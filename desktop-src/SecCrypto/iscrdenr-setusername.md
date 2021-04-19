---
description: Spécifie le nom de l’utilisateur au nom duquel l’inscription de certificat est prévue.
ms.assetid: e088af63-5064-4b1b-976f-047f52e56af8
title: 'ISCrdEnr :: setUserName, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.setUserName
- SCrdEnr.setUserName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: cc2d3157e41fc7ffd9fc0bf7f607de137559e751
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531196"
---
# <a name="iscrdenrsetusername-method"></a><span data-ttu-id="52cc6-103">ISCrdEnr :: setUserName, méthode</span><span class="sxs-lookup"><span data-stu-id="52cc6-103">ISCrdEnr::setUserName method</span></span>

<span data-ttu-id="52cc6-104">La méthode **setUserName** spécifie le nom de l’utilisateur au nom duquel l’inscription de certificat est prévue.</span><span class="sxs-lookup"><span data-stu-id="52cc6-104">The **setUserName** method specifies the name of the user on whose behalf the certificate enrollment is intended.</span></span>

## <a name="syntax"></a><span data-ttu-id="52cc6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="52cc6-105">Syntax</span></span>


```C++
HRESULT setUserName(
  [in] DWORD dwFlags,
  [in] BSTR bstrUserName
);
```


```VB

SCrdEnr.setUserName( _
  ByVal dwFlags, _
  ByVal bstrUserName _
)
```





## <a name="parameters"></a><span data-ttu-id="52cc6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="52cc6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="52cc6-107">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="52cc6-107">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52cc6-108">Cette valeur doit être un \_ nom UPN d’inscription cicatrice \_ \_ (défini comme 1) ou un \_ \_ \_ nom compatible avec l’inscription \_ au Sam (défini sur 2).</span><span class="sxs-lookup"><span data-stu-id="52cc6-108">This value must be either SCARD\_ENROLL\_UPN\_NAME (defined as 1) or SCARD\_ENROLL\_SAM\_COMPATIBLE\_NAME (defined as 2).</span></span>

<span data-ttu-id="52cc6-109">Définissez cette valeur sur \_ le nom UPN de l’inscription à l’utilisation de cicatrices \_ \_ , si le nom spécifié dans *bstrUserName* est le nom de principal universel de l’utilisateur, tel que « someone@example.com ».</span><span class="sxs-lookup"><span data-stu-id="52cc6-109">Set this value to SCARD\_ENROLL\_UPN\_NAME, if the name specified in *bstrUserName* is the user's Universal Principal Name, such as "someone@example.com".</span></span> <span data-ttu-id="52cc6-110">Le nom UPN de l’utilisateur doit correspondre à un nom SAM (Security Access Manager) existant.</span><span class="sxs-lookup"><span data-stu-id="52cc6-110">The user's UPN name must correspond to an existing security access manager (SAM) name.</span></span>

<span data-ttu-id="52cc6-111">Définissez cette valeur sur \_ inscrire \_ \_ un nom compatible sam \_ en cours d’inscription. Si le nom spécifié dans *bstrUserName* est le nom Sam de l’utilisateur au format « utilisateur du domaine \\ ».</span><span class="sxs-lookup"><span data-stu-id="52cc6-111">Set this value to SCARD\_ENROLL\_SAM\_COMPATIBLE\_NAME, if the name specified in *bstrUserName* is the user's SAM name in the format of "DOMAIN\\USER".</span></span>

</dd> <dt>

<span data-ttu-id="52cc6-112">*bstrUserName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="52cc6-112">*bstrUserName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="52cc6-113">Nom de l'utilisateur.</span><span class="sxs-lookup"><span data-stu-id="52cc6-113">Name of the user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="52cc6-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="52cc6-114">Return value</span></span>

### <a name="vb"></a><span data-ttu-id="52cc6-115">VB</span><span class="sxs-lookup"><span data-stu-id="52cc6-115">VB</span></span>

<span data-ttu-id="52cc6-116">Si la méthode est réussie, la méthode retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="52cc6-116">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="52cc6-117">Si la méthode échoue, elle retourne une valeur **HRESULT** qui indique l’erreur.</span><span class="sxs-lookup"><span data-stu-id="52cc6-117">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="52cc6-118">Pour obtenir la liste des codes d’erreur courants, consultez [valeurs HRESULT communes](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="52cc6-118">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="52cc6-119">Notes</span><span class="sxs-lookup"><span data-stu-id="52cc6-119">Remarks</span></span>

<span data-ttu-id="52cc6-120">Appelez cette méthode pour spécifier le nom d’utilisateur à émettre pour la [*carte à puce*](../secgloss/s-gly.md).</span><span class="sxs-lookup"><span data-stu-id="52cc6-120">Call this method to specify the user name to be issued the [*smart card*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="52cc6-121">Une alternative à **setUserName** est [**ISCrdEnr :: selectUserName**](iscrdenr-selectusername.md).</span><span class="sxs-lookup"><span data-stu-id="52cc6-121">An alternative to **setUserName** is [**ISCrdEnr::selectUserName**](iscrdenr-selectusername.md).</span></span>

<span data-ttu-id="52cc6-122">Une fois qu’un nom d’utilisateur a été spécifié, sa valeur peut être récupérée en appelant [**getUserName**](iscrdenr-getusername.md).</span><span class="sxs-lookup"><span data-stu-id="52cc6-122">After a user name has been specified, its value can be retrieved by calling [**getUserName**](iscrdenr-getusername.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="52cc6-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="52cc6-123">Requirements</span></span>



| <span data-ttu-id="52cc6-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="52cc6-124">Requirement</span></span> | <span data-ttu-id="52cc6-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="52cc6-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="52cc6-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="52cc6-126">Minimum supported client</span></span><br/> | <span data-ttu-id="52cc6-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="52cc6-127">None supported</span></span><br/>                                                               |
| <span data-ttu-id="52cc6-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="52cc6-128">Minimum supported server</span></span><br/> | <span data-ttu-id="52cc6-129">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="52cc6-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="52cc6-130">DLL</span><span class="sxs-lookup"><span data-stu-id="52cc6-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="52cc6-131"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="52cc6-131"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="52cc6-132">IID</span><span class="sxs-lookup"><span data-stu-id="52cc6-132">IID</span></span><br/>                      | <span data-ttu-id="52cc6-133">IID \_ ISCrdEnr est défini en tant que 753988a1-1357-436D-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="52cc6-133">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="52cc6-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="52cc6-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52cc6-135">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="52cc6-135">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="52cc6-136">**ISCrdEnr :: getUserName**</span><span class="sxs-lookup"><span data-stu-id="52cc6-136">**ISCrdEnr::getUserName**</span></span>](iscrdenr-getusername.md)
</dt> <dt>

[<span data-ttu-id="52cc6-137">**ISCrdEnr::resetUser**</span><span class="sxs-lookup"><span data-stu-id="52cc6-137">**ISCrdEnr::resetUser**</span></span>](iscrdenr-resetuser.md)
</dt> <dt>

[<span data-ttu-id="52cc6-138">**ISCrdEnr::selectUserName**</span><span class="sxs-lookup"><span data-stu-id="52cc6-138">**ISCrdEnr::selectUserName**</span></span>](iscrdenr-selectusername.md)
</dt> </dl>

 

 
