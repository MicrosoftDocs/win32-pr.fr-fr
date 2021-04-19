---
description: La méthode ReleaseFormat libère la structure associée au format.
ms.assetid: 67181773-5a04-4e20-9814-b004d3b549f5
title: 'ITFormatControl :: ReleaseFormat, méthode (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c91b3eb2a84149054d7ff364cf05290946bca975
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542420"
---
# <a name="itformatcontrolreleaseformat-method"></a><span data-ttu-id="f1289-103">ITFormatControl :: ReleaseFormat, méthode</span><span class="sxs-lookup"><span data-stu-id="f1289-103">ITFormatControl::ReleaseFormat method</span></span>

<span data-ttu-id="f1289-104">\[ Cette méthode n’est pas disponible pour une utilisation dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="f1289-104">\[ This method is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="f1289-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="f1289-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="f1289-106">La méthode **ReleaseFormat** libère la structure associée au format.</span><span class="sxs-lookup"><span data-stu-id="f1289-106">The **ReleaseFormat** method releases the structure associated with the format.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1289-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f1289-107">Syntax</span></span>


```C++
HRESULT ReleaseFormat(
  [in] AM_MEDIA_TYPE *pMediaType
);
```



## <a name="parameters"></a><span data-ttu-id="f1289-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="f1289-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1289-109">*pMediaType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="f1289-109">*pMediaType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1289-110">Pointeur vers un descripteur de **\_ \_ type de média am** du format terminal.</span><span class="sxs-lookup"><span data-stu-id="f1289-110">Pointer to an **AM\_MEDIA\_TYPE** descriptor of the terminal format.</span></span> <span data-ttu-id="f1289-111">Pour plus d’informations sur le **\_ \_ type de média am**, consultez la documentation de DirectX.</span><span class="sxs-lookup"><span data-stu-id="f1289-111">For more information on **AM\_MEDIA\_TYPE**, see the DirectX documentation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1289-112">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="f1289-112">Return value</span></span>

<span data-ttu-id="f1289-113">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="f1289-113">This method can return one of these values.</span></span>



| <span data-ttu-id="f1289-114">Code de retour</span><span class="sxs-lookup"><span data-stu-id="f1289-114">Return code</span></span>                                                                                   | <span data-ttu-id="f1289-115">Description</span><span class="sxs-lookup"><span data-stu-id="f1289-115">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="f1289-116"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f1289-116"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="f1289-117">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="f1289-117">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="f1289-118"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="f1289-118"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="f1289-119">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="f1289-119">Insufficient memory exists to perform the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f1289-120">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f1289-120">Requirements</span></span>



| <span data-ttu-id="f1289-121">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f1289-121">Requirement</span></span> | <span data-ttu-id="f1289-122">Valeur</span><span class="sxs-lookup"><span data-stu-id="f1289-122">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="f1289-123">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="f1289-123">TAPI version</span></span><br/> | <span data-ttu-id="f1289-124">Nécessite TAPI 3,1</span><span class="sxs-lookup"><span data-stu-id="f1289-124">Requires TAPI 3.1</span></span><br/>                                                         |
| <span data-ttu-id="f1289-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="f1289-125">Header</span></span><br/>       | <dl> <span data-ttu-id="f1289-126"><dt>Ipmsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="f1289-126"><dt>Ipmsp.h</dt></span></span> </dl>   |
| <span data-ttu-id="f1289-127">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="f1289-127">Library</span></span><br/>      | <dl> <span data-ttu-id="f1289-128"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="f1289-128"><dt>Uuid.lib</dt></span></span> </dl>  |
| <span data-ttu-id="f1289-129">DLL</span><span class="sxs-lookup"><span data-stu-id="f1289-129">DLL</span></span><br/>          | <dl> <span data-ttu-id="f1289-130"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1289-130"><dt>Tapi3.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1289-131">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f1289-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1289-132">**ITFormatControl**</span><span class="sxs-lookup"><span data-stu-id="f1289-132">**ITFormatControl**</span></span>](itformatcontrol.md)
</dt> </dl>

 

 




