---
description: Affiche une interface utilisateur de sélection, qui permet de sélectionner un nom d’utilisateur.
ms.assetid: 0a02d9e5-b2cf-4818-a2e1-89e6019e53d4
title: 'ISCrdEnr :: selectUserName, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.selectUserName
- SCrdEnr.selectUserName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 13059775abc8520c39a0ad3dea2d604fc8d65455
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106522725"
---
# <a name="iscrdenrselectusername-method"></a><span data-ttu-id="b0e58-103">ISCrdEnr :: selectUserName, méthode</span><span class="sxs-lookup"><span data-stu-id="b0e58-103">ISCrdEnr::selectUserName method</span></span>

<span data-ttu-id="b0e58-104">La méthode **selectUserName** affiche une interface **utilisateur Select** , qui permet de sélectionner un nom d’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b0e58-104">The **selectUserName** method displays a **Select User** interface, allowing a user name to be selected.</span></span>

<span data-ttu-id="b0e58-105">Le nom d’utilisateur s’applique à l’utilisateur au nom duquel l’inscription de certificat est prévue.</span><span class="sxs-lookup"><span data-stu-id="b0e58-105">The user name applies to the user on whose behalf the certificate enrollment is intended.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0e58-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b0e58-106">Syntax</span></span>


```C++
HRESULT selectUserName(
  [in] DWORD dwFlags
);
```


```VB

SCrdEnr.selectUserName( _
  ByVal dwFlags _
)
```





## <a name="parameters"></a><span data-ttu-id="b0e58-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b0e58-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0e58-108">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b0e58-108">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b0e58-109">Réservé pour un usage futur.</span><span class="sxs-lookup"><span data-stu-id="b0e58-109">Reserved for future use.</span></span> <span data-ttu-id="b0e58-110">Définissez cette valeur sur zéro.</span><span class="sxs-lookup"><span data-stu-id="b0e58-110">Set this value to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0e58-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b0e58-111">Return value</span></span>

### <a name="vb"></a><span data-ttu-id="b0e58-112">VB</span><span class="sxs-lookup"><span data-stu-id="b0e58-112">VB</span></span>

<span data-ttu-id="b0e58-113">Si la méthode est réussie, la méthode retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b0e58-113">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="b0e58-114">Si la méthode échoue, elle retourne une valeur **HRESULT** qui indique l’erreur.</span><span class="sxs-lookup"><span data-stu-id="b0e58-114">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="b0e58-115">Pour obtenir la liste des codes d’erreur courants, consultez [valeurs HRESULT communes](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="b0e58-115">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b0e58-116">Notes</span><span class="sxs-lookup"><span data-stu-id="b0e58-116">Remarks</span></span>

<span data-ttu-id="b0e58-117">Utilisez cette méthode pour sélectionner le nom de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="b0e58-117">Use this method to select the name of the user.</span></span> <span data-ttu-id="b0e58-118">Une fois qu’un nom d’utilisateur a été sélectionné, sa valeur peut être récupérée en appelant la méthode [**ISCrdEnr :: GetUserName**](iscrdenr-getusername.md) .</span><span class="sxs-lookup"><span data-stu-id="b0e58-118">After a user name has been selected, its value can be retrieved by calling the [**ISCrdEnr::getUserName**](iscrdenr-getusername.md) method.</span></span>

<span data-ttu-id="b0e58-119">Une alternative à l’utilisation de l’interface « Select User » consiste à spécifier un utilisateur en appelant la méthode [**ISCrdEnr :: setUserName**](iscrdenr-setusername.md) .</span><span class="sxs-lookup"><span data-stu-id="b0e58-119">An alternative to using the 'Select User' interface is to specify a user by calling the [**ISCrdEnr::setUserName**](iscrdenr-setusername.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0e58-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b0e58-120">Requirements</span></span>



| <span data-ttu-id="b0e58-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b0e58-121">Requirement</span></span> | <span data-ttu-id="b0e58-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="b0e58-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b0e58-123">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b0e58-123">Minimum supported client</span></span><br/> | <span data-ttu-id="b0e58-124">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="b0e58-124">None supported</span></span><br/>                                                               |
| <span data-ttu-id="b0e58-125">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b0e58-125">Minimum supported server</span></span><br/> | <span data-ttu-id="b0e58-126">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b0e58-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="b0e58-127">DLL</span><span class="sxs-lookup"><span data-stu-id="b0e58-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0e58-128"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0e58-128"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="b0e58-129">IID</span><span class="sxs-lookup"><span data-stu-id="b0e58-129">IID</span></span><br/>                      | <span data-ttu-id="b0e58-130">IID \_ ISCrdEnr est défini en tant que 753988a1-1357-436D-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="b0e58-130">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="b0e58-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="b0e58-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0e58-132">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="b0e58-132">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="b0e58-133">**ISCrdEnr :: getUserName**</span><span class="sxs-lookup"><span data-stu-id="b0e58-133">**ISCrdEnr::getUserName**</span></span>](iscrdenr-getusername.md)
</dt> <dt>

[<span data-ttu-id="b0e58-134">**ISCrdEnr::resetUser**</span><span class="sxs-lookup"><span data-stu-id="b0e58-134">**ISCrdEnr::resetUser**</span></span>](iscrdenr-resetuser.md)
</dt> <dt>

[<span data-ttu-id="b0e58-135">**ISCrdEnr :: setUserName**</span><span class="sxs-lookup"><span data-stu-id="b0e58-135">**ISCrdEnr::setUserName**</span></span>](iscrdenr-setusername.md)
</dt> </dl>

 

 




