---
description: Récupère le nom de l’autorité de certification (CA) spécifiée pour un modèle de certificat donné.
ms.assetid: e921710a-7c74-4fda-91e1-fbad45889984
title: 'ISCrdEnr :: getCAName, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCAName
- SCrdEnr.getCAName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: b62b0a7e871a29ff0a8edd28eb8cd5e18e97c1a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104210245"
---
# <a name="iscrdenrgetcaname-method"></a><span data-ttu-id="0dedf-103">ISCrdEnr :: getCAName, méthode</span><span class="sxs-lookup"><span data-stu-id="0dedf-103">ISCrdEnr::getCAName method</span></span>

<span data-ttu-id="0dedf-104">La méthode **getCAName** récupère le nom de l’autorité de [*certification*](../secgloss/c-gly.md) (ca) spécifiée pour un modèle de certificat donné.</span><span class="sxs-lookup"><span data-stu-id="0dedf-104">The **getCAName** method retrieves the name of the specified [*certification authority*](../secgloss/c-gly.md) (CA) for a given certificate template.</span></span>

## <a name="syntax"></a><span data-ttu-id="0dedf-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0dedf-105">Syntax</span></span>


```C++
HRESULT getCAName(
  [in]  DWORD     dwFlags,
  [in]  BSTR     bstrCertTemplateName,
  [out] BSTR *pbstrCAName
);
```


```VB

SCrdEnr.getCAName( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName, _
  ByRef pbstrCAName _
)
```





## <a name="parameters"></a><span data-ttu-id="0dedf-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0dedf-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0dedf-107">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0dedf-107">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0dedf-108">Valeur qui détermine si le nom fait référence au nom de l’autorité de certification ou au nom de l’ordinateur de l’autorité de certification.</span><span class="sxs-lookup"><span data-stu-id="0dedf-108">A value that determines whether the name refers to the CA name or the CA's machine name.</span></span> <span data-ttu-id="0dedf-109">Si cette valeur est un \_ \_ \_ \_ nom d’ordinateur d’autorité de certification d’inscription cicatrice (défini comme 0x01), le nom fait référence au nom d’ordinateur de l’autorité de certification ; sinon, le nom fait référence au nom de l’autorité de certification.</span><span class="sxs-lookup"><span data-stu-id="0dedf-109">If this value is SCARD\_ENROLL\_CA\_MACHINE\_NAME (defined as 0x01) then the name refers to the CA's machine name; otherwise the name refers to the CA name.</span></span>

</dd> <dt>

<span data-ttu-id="0dedf-110">*bstrCertTemplateName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0dedf-110">*bstrCertTemplateName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0dedf-111">Nom du modèle de certificat.</span><span class="sxs-lookup"><span data-stu-id="0dedf-111">The name of the certificate template.</span></span>

</dd> <dt>

<span data-ttu-id="0dedf-112">*pbstrCAName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0dedf-112">*pbstrCAName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0dedf-113">Pointeur vers une chaîne qui retourne le nom de l’autorité de certification.</span><span class="sxs-lookup"><span data-stu-id="0dedf-113">A pointer to a string that returns the name of the CA.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0dedf-114">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0dedf-114">Return value</span></span>

### <a name="c"></a><span data-ttu-id="0dedf-115">C++</span><span class="sxs-lookup"><span data-stu-id="0dedf-115">C++</span></span>

<span data-ttu-id="0dedf-116">Si la méthode est réussie, la méthode retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0dedf-116">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="0dedf-117">Si la méthode échoue, elle retourne une valeur **HRESULT** qui indique l’erreur.</span><span class="sxs-lookup"><span data-stu-id="0dedf-117">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="0dedf-118">Pour obtenir la liste des codes d’erreur courants, consultez [valeurs HRESULT communes](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="0dedf-118">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="0dedf-119">VB</span><span class="sxs-lookup"><span data-stu-id="0dedf-119">VB</span></span>

<span data-ttu-id="0dedf-120">Chaîne qui représente le nom de l’autorité de certification.</span><span class="sxs-lookup"><span data-stu-id="0dedf-120">A string that represents the name of the CA.</span></span>

## <a name="remarks"></a><span data-ttu-id="0dedf-121">Notes</span><span class="sxs-lookup"><span data-stu-id="0dedf-121">Remarks</span></span>

<span data-ttu-id="0dedf-122">Le nom de l’autorité de certification par défaut est le prénom dans la liste des autorités de certification disponibles.</span><span class="sxs-lookup"><span data-stu-id="0dedf-122">The default CA name is the first name in the available list of CAs.</span></span>

## <a name="requirements"></a><span data-ttu-id="0dedf-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0dedf-123">Requirements</span></span>



| <span data-ttu-id="0dedf-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0dedf-124">Requirement</span></span> | <span data-ttu-id="0dedf-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="0dedf-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0dedf-126">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0dedf-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0dedf-127">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="0dedf-127">None supported</span></span><br/>                                                               |
| <span data-ttu-id="0dedf-128">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0dedf-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0dedf-129">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0dedf-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0dedf-130">DLL</span><span class="sxs-lookup"><span data-stu-id="0dedf-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0dedf-131"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0dedf-131"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="0dedf-132">IID</span><span class="sxs-lookup"><span data-stu-id="0dedf-132">IID</span></span><br/>                      | <span data-ttu-id="0dedf-133">IID \_ ISCrdEnr est défini en tant que 753988a1-1357-436D-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="0dedf-133">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="0dedf-134">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0dedf-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0dedf-135">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="0dedf-135">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="0dedf-136">**ISCrdEnr::enumCAName**</span><span class="sxs-lookup"><span data-stu-id="0dedf-136">**ISCrdEnr::enumCAName**</span></span>](iscrdenr-enumcaname.md)
</dt> <dt>

[<span data-ttu-id="0dedf-137">**ISCrdEnr::getCACount**</span><span class="sxs-lookup"><span data-stu-id="0dedf-137">**ISCrdEnr::getCACount**</span></span>](iscrdenr-getcacount.md)
</dt> <dt>

[<span data-ttu-id="0dedf-138">**ISCrdEnr::setCAName**</span><span class="sxs-lookup"><span data-stu-id="0dedf-138">**ISCrdEnr::setCAName**</span></span>](iscrdenr-setcaname.md)
</dt> </dl>

 

 
