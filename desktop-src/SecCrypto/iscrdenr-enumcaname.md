---
description: Énumère le nom des autorités de certification (ca) pour un nom de modèle de certificat donné.
ms.assetid: 82cc3346-a8b9-4abd-933a-c212a37a373e
title: 'ISCrdEnr :: enumCAName, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.enumCAName
- SCrdEnr.enumCAName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: c23df2f74cdf3791f1280e38cbff8ddd48f924b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518899"
---
# <a name="iscrdenrenumcaname-method"></a><span data-ttu-id="dccb8-103">ISCrdEnr :: enumCAName, méthode</span><span class="sxs-lookup"><span data-stu-id="dccb8-103">ISCrdEnr::enumCAName method</span></span>

<span data-ttu-id="dccb8-104">La méthode **enumCAName** énumère le nom des autorités de [*certification*](../secgloss/c-gly.md) (ca) pour un nom de modèle de certificat donné.</span><span class="sxs-lookup"><span data-stu-id="dccb8-104">The **enumCAName** method enumerates the name of the [*certification authorities*](../secgloss/c-gly.md) (CAs) for a given certificate template name.</span></span>

## <a name="syntax"></a><span data-ttu-id="dccb8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="dccb8-105">Syntax</span></span>


```C++
HRESULT enumCAName(
  [in]  DWORD     dwIndex,
  [in]  DWORD     dwFlags,
  [in]  BSTR     bstrCertTemplateName,
  [out] BSTR *pbstrCAName
);
```


```VB

SCrdEnr.enumCAName( _
  ByVal dwIndex, _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName, _
  ByRef pbstrCAName _
)
```





## <a name="parameters"></a><span data-ttu-id="dccb8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="dccb8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dccb8-107">*dwIndex* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dccb8-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dccb8-108">Index de base zéro de la séquence d’énumération.</span><span class="sxs-lookup"><span data-stu-id="dccb8-108">The zero-based index for the enumeration sequence.</span></span>

</dd> <dt>

<span data-ttu-id="dccb8-109">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dccb8-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dccb8-110">Valeur qui détermine si le nom fait référence au nom de l’autorité de certification ou au nom de l’ordinateur de l’autorité de certification.</span><span class="sxs-lookup"><span data-stu-id="dccb8-110">A value that determines whether the name refers to the CA name or the CA's machine name.</span></span> <span data-ttu-id="dccb8-111">Si cette valeur est un \_ \_ \_ nom d’ordinateur de \_ l’autorité de certification d’inscription au format 0x01 (défini comme 0x01), le nom fait référence au nom de l’ordinateur de l’autorité de certification.</span><span class="sxs-lookup"><span data-stu-id="dccb8-111">If this value is SCARD\_ENROLL\_CA\_MACHINE\_NAME (defined as 0x01), the name refers to the CA's machine name.</span></span> <span data-ttu-id="dccb8-112">Dans le cas contraire, le nom fait référence au nom de l’autorité de certification.</span><span class="sxs-lookup"><span data-stu-id="dccb8-112">Otherwise the name refers to the CA name.</span></span>

</dd> <dt>

<span data-ttu-id="dccb8-113">*bstrCertTemplateName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="dccb8-113">*bstrCertTemplateName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dccb8-114">Nom du modèle de certificat.</span><span class="sxs-lookup"><span data-stu-id="dccb8-114">The name of the certificate template.</span></span>

</dd> <dt>

<span data-ttu-id="dccb8-115">*pbstrCAName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="dccb8-115">*pbstrCAName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dccb8-116">Pointeur vers une chaîne qui retourne le nom de l’autorité de certification.</span><span class="sxs-lookup"><span data-stu-id="dccb8-116">A pointer to a string that returns the name of the CA.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dccb8-117">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="dccb8-117">Return value</span></span>

### <a name="c"></a><span data-ttu-id="dccb8-118">C++</span><span class="sxs-lookup"><span data-stu-id="dccb8-118">C++</span></span>

<span data-ttu-id="dccb8-119">Si la méthode est réussie, la méthode retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="dccb8-119">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="dccb8-120">Si la méthode échoue, elle retourne une valeur **HRESULT** qui indique l’erreur.</span><span class="sxs-lookup"><span data-stu-id="dccb8-120">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="dccb8-121">Pour obtenir la liste des codes d’erreur courants, consultez [valeurs HRESULT communes](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="dccb8-121">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="dccb8-122">VB</span><span class="sxs-lookup"><span data-stu-id="dccb8-122">VB</span></span>

<span data-ttu-id="dccb8-123">Chaîne qui représente le nom de l’autorité de certification.</span><span class="sxs-lookup"><span data-stu-id="dccb8-123">A string that represents the name of the CA.</span></span>

## <a name="requirements"></a><span data-ttu-id="dccb8-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="dccb8-124">Requirements</span></span>



| <span data-ttu-id="dccb8-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="dccb8-125">Requirement</span></span> | <span data-ttu-id="dccb8-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="dccb8-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dccb8-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dccb8-127">Minimum supported client</span></span><br/> | <span data-ttu-id="dccb8-128">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="dccb8-128">None supported</span></span><br/>                                                               |
| <span data-ttu-id="dccb8-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="dccb8-129">Minimum supported server</span></span><br/> | <span data-ttu-id="dccb8-130">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="dccb8-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="dccb8-131">DLL</span><span class="sxs-lookup"><span data-stu-id="dccb8-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dccb8-132"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dccb8-132"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="dccb8-133">IID</span><span class="sxs-lookup"><span data-stu-id="dccb8-133">IID</span></span><br/>                      | <span data-ttu-id="dccb8-134">IID \_ ISCrdEnr est défini en tant que 753988a1-1357-436D-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="dccb8-134">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="dccb8-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="dccb8-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dccb8-136">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="dccb8-136">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="dccb8-137">**ISCrdEnr::getCACount**</span><span class="sxs-lookup"><span data-stu-id="dccb8-137">**ISCrdEnr::getCACount**</span></span>](iscrdenr-getcacount.md)
</dt> <dt>

[<span data-ttu-id="dccb8-138">**ISCrdEnr::getCAName**</span><span class="sxs-lookup"><span data-stu-id="dccb8-138">**ISCrdEnr::getCAName**</span></span>](iscrdenr-getcaname.md)
</dt> <dt>

[<span data-ttu-id="dccb8-139">**ISCrdEnr::setCAName**</span><span class="sxs-lookup"><span data-stu-id="dccb8-139">**ISCrdEnr::setCAName**</span></span>](iscrdenr-setcaname.md)
</dt> </dl>

 

 
