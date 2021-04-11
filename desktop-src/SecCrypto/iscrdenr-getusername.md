---
description: Récupère le nom de l’utilisateur au nom duquel l’inscription de certificat est prévue.
ms.assetid: 7bd71944-f7dd-4c92-a71c-ecc5c0afd5b2
title: 'ISCrdEnr :: getUserName, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getUserName
- SCrdEnr.getUserName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 51f551a704f3a98b932e646c95810f928e73bac7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320378"
---
# <a name="iscrdenrgetusername-method"></a><span data-ttu-id="2ce6b-103">ISCrdEnr :: getUserName, méthode</span><span class="sxs-lookup"><span data-stu-id="2ce6b-103">ISCrdEnr::getUserName method</span></span>

<span data-ttu-id="2ce6b-104">La méthode **getUserName** récupère le nom de l’utilisateur au nom duquel l’inscription de certificat est prévue.</span><span class="sxs-lookup"><span data-stu-id="2ce6b-104">The **getUserName** method retrieves the name of the user on whose behalf the certificate enrollment is intended.</span></span>

<span data-ttu-id="2ce6b-105">Avant d’appeler cette méthode, vous devez spécifier le nom d’utilisateur dans un appel à [**ISCrdEnr :: selectUserName**](iscrdenr-selectusername.md) ou [**ISCrdEnr :: setUserName**](iscrdenr-setusername.md).</span><span class="sxs-lookup"><span data-stu-id="2ce6b-105">Before calling this method, you must specify the user name in a call to [**ISCrdEnr::selectUserName**](iscrdenr-selectusername.md) or [**ISCrdEnr::setUserName**](iscrdenr-setusername.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2ce6b-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="2ce6b-106">Syntax</span></span>


```C++
HRESULT getUserName(
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrUserName
);
```


```VB

SCrdEnr.getUserName( _
  ByVal dwFlags, _
  ByRef pbstrUserName _
)
```





## <a name="parameters"></a><span data-ttu-id="2ce6b-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="2ce6b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ce6b-108">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="2ce6b-108">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ce6b-109">Cette valeur doit être égale à zéro (0), \_ nom UPN d’inscription cicatrice \_ \_ ou \_ \_ \_ nom compatible avec l’inscription au sam \_ .</span><span class="sxs-lookup"><span data-stu-id="2ce6b-109">This value must be either zero (0), SCARD\_ENROLL\_UPN\_NAME, or SCARD\_ENROLL\_SAM\_COMPATIBLE\_NAME.</span></span>

<span data-ttu-id="2ce6b-110">Si cette valeur est \_ \_ \_ un nom UPN d’inscription cicatrice, **getUserName** retourne le nom d’utilisateur principal universel (UPN) de l’utilisateur, tel que « someone@example.com ».</span><span class="sxs-lookup"><span data-stu-id="2ce6b-110">If this value is SCARD\_ENROLL\_UPN\_NAME, **getUserName** returns the user's Universal Principal Name (UPN), such as "someone@example.com".</span></span>

<span data-ttu-id="2ce6b-111">Si cette valeur est un \_ \_ \_ nom compatible avec \_ l’inscription en mode Sam, la méthode retourne le nom Sam (Security Access Manager) de l’utilisateur au format « utilisateur de domaine \\ ».</span><span class="sxs-lookup"><span data-stu-id="2ce6b-111">If this value is SCARD\_ENROLL\_SAM\_COMPATIBLE\_NAME, the method returns the user's security access manager (SAM) name in the format "DOMAIN\\USER".</span></span>

<span data-ttu-id="2ce6b-112">Si cette valeur est égale à zéro, la méthode retourne le nom UPN de l’utilisateur, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="2ce6b-112">If this value is zero, the method returns the user's UPN name if it exists.</span></span> <span data-ttu-id="2ce6b-113">Si l’utilisateur n’a pas de nom UPN, la méthode retourne le nom SAM de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2ce6b-113">If the user does not have a UPN name, the method returns the user's SAM name.</span></span>

</dd> <dt>

<span data-ttu-id="2ce6b-114">*pbstrUserName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="2ce6b-114">*pbstrUserName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ce6b-115">Pointeur vers une chaîne qui retourne le nom de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2ce6b-115">A pointer to a string that returns the name of the user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ce6b-116">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="2ce6b-116">Return value</span></span>

### <a name="c"></a><span data-ttu-id="2ce6b-117">C++</span><span class="sxs-lookup"><span data-stu-id="2ce6b-117">C++</span></span>

<span data-ttu-id="2ce6b-118">Si la méthode est réussie, la méthode retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="2ce6b-118">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="2ce6b-119">Si la méthode échoue, elle retourne une valeur **HRESULT** qui indique l’erreur.</span><span class="sxs-lookup"><span data-stu-id="2ce6b-119">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="2ce6b-120">Pour obtenir la liste des codes d’erreur courants, consultez [valeurs HRESULT communes](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="2ce6b-120">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="2ce6b-121">VB</span><span class="sxs-lookup"><span data-stu-id="2ce6b-121">VB</span></span>

<span data-ttu-id="2ce6b-122">Chaîne qui représente le nom de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="2ce6b-122">String that represents the name of the user.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ce6b-123">Notes</span><span class="sxs-lookup"><span data-stu-id="2ce6b-123">Remarks</span></span>

<span data-ttu-id="2ce6b-124">Vous pouvez spécifier le nom de l’utilisateur pour lequel la [*carte à puce*](../secgloss/s-gly.md) est émise en appelant [**ISCrdEnr :: setUserName**](iscrdenr-setusername.md) ou [**ISCrdEnr :: selectUserName**](iscrdenr-selectusername.md).</span><span class="sxs-lookup"><span data-stu-id="2ce6b-124">You can specify the name of the user to whom the [*smart card*](../secgloss/s-gly.md) is issued by calling either [**ISCrdEnr::setUserName**](iscrdenr-setusername.md) or [**ISCrdEnr::selectUserName**](iscrdenr-selectusername.md).</span></span> <span data-ttu-id="2ce6b-125">Une fois qu’un nom d’utilisateur a été spécifié, sa valeur peut être récupérée en appelant **getUserName**.</span><span class="sxs-lookup"><span data-stu-id="2ce6b-125">After a user name has been specified, its value can be retrieved by calling **getUserName**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ce6b-126">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2ce6b-126">Requirements</span></span>



| <span data-ttu-id="2ce6b-127">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2ce6b-127">Requirement</span></span> | <span data-ttu-id="2ce6b-128">Valeur</span><span class="sxs-lookup"><span data-stu-id="2ce6b-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2ce6b-129">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2ce6b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="2ce6b-130">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="2ce6b-130">None supported</span></span><br/>                                                               |
| <span data-ttu-id="2ce6b-131">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="2ce6b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="2ce6b-132">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="2ce6b-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="2ce6b-133">DLL</span><span class="sxs-lookup"><span data-stu-id="2ce6b-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ce6b-134"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ce6b-134"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="2ce6b-135">IID</span><span class="sxs-lookup"><span data-stu-id="2ce6b-135">IID</span></span><br/>                      | <span data-ttu-id="2ce6b-136">IID \_ ISCrdEnr est défini en tant que 753988a1-1357-436D-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="2ce6b-136">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="2ce6b-137">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2ce6b-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ce6b-138">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="2ce6b-138">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="2ce6b-139">**ISCrdEnr::resetUser**</span><span class="sxs-lookup"><span data-stu-id="2ce6b-139">**ISCrdEnr::resetUser**</span></span>](iscrdenr-resetuser.md)
</dt> <dt>

[<span data-ttu-id="2ce6b-140">**ISCrdEnr::selectUserName**</span><span class="sxs-lookup"><span data-stu-id="2ce6b-140">**ISCrdEnr::selectUserName**</span></span>](iscrdenr-selectusername.md)
</dt> <dt>

[<span data-ttu-id="2ce6b-141">**ISCrdEnr :: setUserName**</span><span class="sxs-lookup"><span data-stu-id="2ce6b-141">**ISCrdEnr::setUserName**</span></span>](iscrdenr-setusername.md)
</dt> </dl>

 

 
