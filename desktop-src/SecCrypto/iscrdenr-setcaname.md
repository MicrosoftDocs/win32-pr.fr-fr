---
description: Spécifie le nom de l’autorité de certification.
ms.assetid: 224c2a51-8a25-4b66-b86b-c87531475145
title: 'ISCrdEnr :: setCAName, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.setCAName
- SCrdEnr.setCAName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 46dcd9294337c088b9e1b0ab68bddefe4308ed27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106528291"
---
# <a name="iscrdenrsetcaname-method"></a><span data-ttu-id="f2334-103">ISCrdEnr :: setCAName, méthode</span><span class="sxs-lookup"><span data-stu-id="f2334-103">ISCrdEnr::setCAName method</span></span>

<span data-ttu-id="f2334-104">La méthode **setCAName** spécifie le nom de l' [*autorité de certification*](../secgloss/c-gly.md) (ca).</span><span class="sxs-lookup"><span data-stu-id="f2334-104">The **setCAName** method specifies the name of the [*certification authority*](../secgloss/c-gly.md) (CA).</span></span>

## <a name="syntax"></a><span data-ttu-id="f2334-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f2334-105">Syntax</span></span>


```C++
HRESULT setCAName(
  [in] DWORD dwFlags,
  [in] BSTR bstrCertTemplateName,
  [in] BSTR bstrCAName
);
```


```VB

SCrdEnr.setCAName( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName, _
  ByVal bstrCAName _
)
```





## <a name="parameters"></a><span data-ttu-id="f2334-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f2334-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f2334-107">*dwFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f2334-107">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2334-108">Valeur qui spécifie si le nom fait référence au nom de l’autorité de certification ou au nom de l’ordinateur de l’autorité de certification.</span><span class="sxs-lookup"><span data-stu-id="f2334-108">Value that specifies whether the name refers to the CA name or the CA's machine name.</span></span> <span data-ttu-id="f2334-109">Si cette valeur est un \_ \_ \_ nom d’ordinateur de \_ l’autorité de certification d’inscription au format 0x01 (défini comme 0x01), le nom fait référence au nom de l’ordinateur de l’autorité de certification.</span><span class="sxs-lookup"><span data-stu-id="f2334-109">If this value is SCARD\_ENROLL\_CA\_MACHINE\_NAME (defined as 0x01), the name refers to the CA's machine name.</span></span> <span data-ttu-id="f2334-110">Dans le cas contraire, le nom fait référence au nom de l’autorité de certification.</span><span class="sxs-lookup"><span data-stu-id="f2334-110">Otherwise, the name refers to the CA name.</span></span>

</dd> <dt>

<span data-ttu-id="f2334-111">*bstrCertTemplateName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f2334-111">*bstrCertTemplateName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2334-112">Nom du modèle de certificat.</span><span class="sxs-lookup"><span data-stu-id="f2334-112">Name of the certificate template.</span></span>

</dd> <dt>

<span data-ttu-id="f2334-113">*bstrCAName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f2334-113">*bstrCAName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f2334-114">Nom de l’autorité de certification à utiliser avec le modèle de certificat spécifié par *bstrCertTemplateName*.</span><span class="sxs-lookup"><span data-stu-id="f2334-114">CA name to be used with the certificate template specified by *bstrCertTemplateName*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f2334-115">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f2334-115">Return value</span></span>

### <a name="vb"></a><span data-ttu-id="f2334-116">VB</span><span class="sxs-lookup"><span data-stu-id="f2334-116">VB</span></span>

<span data-ttu-id="f2334-117">La valeur de retour est un **HRESULT**.</span><span class="sxs-lookup"><span data-stu-id="f2334-117">The return value is an **HRESULT**.</span></span> <span data-ttu-id="f2334-118">La valeur S \_ OK indique que l’appel a réussi.</span><span class="sxs-lookup"><span data-stu-id="f2334-118">A value of S\_OK indicates that the call was successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="f2334-119">Notes</span><span class="sxs-lookup"><span data-stu-id="f2334-119">Remarks</span></span>

<span data-ttu-id="f2334-120">Utilisez cette méthode pour spécifier une autorité de certification pour un modèle de certificat.</span><span class="sxs-lookup"><span data-stu-id="f2334-120">Use this method to specify a CA for a certificate template.</span></span>

## <a name="requirements"></a><span data-ttu-id="f2334-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f2334-121">Requirements</span></span>



| <span data-ttu-id="f2334-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f2334-122">Requirement</span></span> | <span data-ttu-id="f2334-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="f2334-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f2334-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2334-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f2334-125">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2334-125">None supported</span></span><br/>                                                               |
| <span data-ttu-id="f2334-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f2334-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f2334-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="f2334-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f2334-128">DLL</span><span class="sxs-lookup"><span data-stu-id="f2334-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2334-129"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f2334-129"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="f2334-130">IID</span><span class="sxs-lookup"><span data-stu-id="f2334-130">IID</span></span><br/>                      | <span data-ttu-id="f2334-131">IID \_ ISCrdEnr est défini en tant que 753988a1-1357-436D-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="f2334-131">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="f2334-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f2334-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2334-133">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="f2334-133">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="f2334-134">**ISCrdEnr::enumCAName**</span><span class="sxs-lookup"><span data-stu-id="f2334-134">**ISCrdEnr::enumCAName**</span></span>](iscrdenr-enumcaname.md)
</dt> <dt>

[<span data-ttu-id="f2334-135">**ISCrdEnr::getCAName**</span><span class="sxs-lookup"><span data-stu-id="f2334-135">**ISCrdEnr::getCAName**</span></span>](iscrdenr-getcaname.md)
</dt> </dl>

 

 
