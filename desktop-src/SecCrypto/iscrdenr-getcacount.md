---
description: Retourne le nombre d’autorités de certification (ca) disposé à émettre un certificat basé sur le modèle de certificat spécifié.
ms.assetid: 377121a8-3895-4308-a803-4a62580c6de0
title: 'ISCrdEnr :: getCACount, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCACount
- SCrdEnr.getCACount
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: eb33f6c7345862dedf6c909054d811ff4da470ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106535574"
---
# <a name="iscrdenrgetcacount-method"></a><span data-ttu-id="0a13b-103">ISCrdEnr :: getCACount, méthode</span><span class="sxs-lookup"><span data-stu-id="0a13b-103">ISCrdEnr::getCACount method</span></span>

<span data-ttu-id="0a13b-104">La méthode **getCACount** retourne le nombre d' [*autorités de certification*](../secgloss/c-gly.md) prêtes à émettre un certificat basé sur le modèle de certificat spécifié.</span><span class="sxs-lookup"><span data-stu-id="0a13b-104">The **getCACount** method returns the number of [*certification authorities*](../secgloss/c-gly.md) (CAs) willing to issue a certificate based on the specified certificate template.</span></span>

## <a name="syntax"></a><span data-ttu-id="0a13b-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0a13b-105">Syntax</span></span>


```C++
HRESULT getCACount(
  [in]  BSTR     bstrCertTemplateName,
  [out] LONG *pdwCACount
);
```


```VB

SCrdEnr.getCACount( _
  ByVal bstrCertTemplateName, _
  ByRef pdwCACount _
)
```





## <a name="parameters"></a><span data-ttu-id="0a13b-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="0a13b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a13b-107">*bstrCertTemplateName* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="0a13b-107">*bstrCertTemplateName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0a13b-108">Chaîne qui représente le nom du modèle de certificat.</span><span class="sxs-lookup"><span data-stu-id="0a13b-108">A string that represents the name of the certificate template.</span></span>

</dd> <dt>

<span data-ttu-id="0a13b-109">*pdwCACount* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="0a13b-109">*pdwCACount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a13b-110">Pointeur vers une **valeur de type long** qui retourne le nombre d’autorités de certification disponibles qui émettra un certificat pour le modèle de certificat spécifié dans *bstrCertTemplateName*.</span><span class="sxs-lookup"><span data-stu-id="0a13b-110">A pointer to a **LONG** that returns the number of available CAs that will issue a certificate for the certificate template specified in *bstrCertTemplateName*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0a13b-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="0a13b-111">Return value</span></span>

### <a name="c"></a><span data-ttu-id="0a13b-112">C++</span><span class="sxs-lookup"><span data-stu-id="0a13b-112">C++</span></span>

<span data-ttu-id="0a13b-113">Si la méthode est réussie, la méthode retourne S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0a13b-113">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="0a13b-114">Si la méthode échoue, elle retourne une valeur **HRESULT** qui indique l’erreur.</span><span class="sxs-lookup"><span data-stu-id="0a13b-114">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="0a13b-115">Pour obtenir la liste des codes d’erreur courants, consultez [valeurs HRESULT communes](common-hresult-values.md).</span><span class="sxs-lookup"><span data-stu-id="0a13b-115">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="0a13b-116">VB</span><span class="sxs-lookup"><span data-stu-id="0a13b-116">VB</span></span>

<span data-ttu-id="0a13b-117">Valeur de **type long** qui représente le nombre d’autorités de certification disponibles qui émettra un certificat pour le modèle de certificat spécifié dans *bstrCertTemplateName*.</span><span class="sxs-lookup"><span data-stu-id="0a13b-117">A **Long** value that represents the number of available CAs that will issue a certificate for the certificate template specified in *bstrCertTemplateName*.</span></span>

## <a name="requirements"></a><span data-ttu-id="0a13b-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0a13b-118">Requirements</span></span>



| <span data-ttu-id="0a13b-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0a13b-119">Requirement</span></span> | <span data-ttu-id="0a13b-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="0a13b-120">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a13b-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0a13b-121">Minimum supported client</span></span><br/> | <span data-ttu-id="0a13b-122">Aucun pris en charge</span><span class="sxs-lookup"><span data-stu-id="0a13b-122">None supported</span></span><br/>                                                               |
| <span data-ttu-id="0a13b-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="0a13b-123">Minimum supported server</span></span><br/> | <span data-ttu-id="0a13b-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="0a13b-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="0a13b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="0a13b-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0a13b-126"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0a13b-126"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="0a13b-127">IID</span><span class="sxs-lookup"><span data-stu-id="0a13b-127">IID</span></span><br/>                      | <span data-ttu-id="0a13b-128">IID \_ ISCrdEnr est défini en tant que 753988a1-1357-436D-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="0a13b-128">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="0a13b-129">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="0a13b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a13b-130">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="0a13b-130">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="0a13b-131">**ISCrdEnr::enumCAName**</span><span class="sxs-lookup"><span data-stu-id="0a13b-131">**ISCrdEnr::enumCAName**</span></span>](iscrdenr-enumcaname.md)
</dt> <dt>

[<span data-ttu-id="0a13b-132">**ISCrdEnr::getCAName**</span><span class="sxs-lookup"><span data-stu-id="0a13b-132">**ISCrdEnr::getCAName**</span></span>](iscrdenr-getcaname.md)
</dt> </dl>

 

 
