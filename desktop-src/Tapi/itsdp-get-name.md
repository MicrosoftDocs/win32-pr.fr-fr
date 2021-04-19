---
description: La \_ méthode obtenir le nom obtient le nom de la session.
ms.assetid: 97b44a01-585b-434c-ad59-51c35e8a1ceb
title: 'ITSdp :: get_Name, méthode (sdpblb. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b41d431a76f3d0bb2122847e8ee5c3a4dde3c1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523508"
---
# <a name="itsdpget_name-method"></a><span data-ttu-id="85b26-103">ITSdp :: méthode d’extraction de \_ nom</span><span class="sxs-lookup"><span data-stu-id="85b26-103">ITSdp::get\_Name method</span></span>

<span data-ttu-id="85b26-104">\[ Les interfaces et les contrôles de conférence de téléphonie IP Rendezvous ne peuvent pas être utilisés dans Windows Vista, Windows Server 2008 et les versions ultérieures du système d’exploitation.</span><span class="sxs-lookup"><span data-stu-id="85b26-104">\[ Rendezvous IP Telephony Conferencing controls and interfaces are not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="85b26-105">L’API cliente RTC offre des fonctionnalités similaires.\]</span><span class="sxs-lookup"><span data-stu-id="85b26-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="85b26-106">La méthode **obtenir le \_ nom** obtient le nom de la session.</span><span class="sxs-lookup"><span data-stu-id="85b26-106">The **get\_Name** method gets the session name.</span></span> <span data-ttu-id="85b26-107">Il doit s’agir d’une chaîne convertible ASCII si le jeu de caractères est ASCII.</span><span class="sxs-lookup"><span data-stu-id="85b26-107">This has to be an ASCII convertible string if the character set is ASCII.</span></span> <span data-ttu-id="85b26-108">(Dans le cas contraire, il peut s’agir d’une chaîne **BSTR** .)</span><span class="sxs-lookup"><span data-stu-id="85b26-108">(Otherwise, it can be any **BSTR** string.)</span></span>

## <a name="syntax"></a><span data-ttu-id="85b26-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="85b26-109">Syntax</span></span>


```C++
HRESULT get_Name(
  [out] BSTR *ppName
);
```



## <a name="parameters"></a><span data-ttu-id="85b26-110">Paramètres</span><span class="sxs-lookup"><span data-stu-id="85b26-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="85b26-111">*ppName* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="85b26-111">*ppName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="85b26-112">Pointeur vers un **BSTR** contenant le nom de session.</span><span class="sxs-lookup"><span data-stu-id="85b26-112">Pointer to a **BSTR** containing the session name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="85b26-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="85b26-113">Return value</span></span>

<span data-ttu-id="85b26-114">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="85b26-114">This method can return one of these values.</span></span>



| <span data-ttu-id="85b26-115">Code de retour</span><span class="sxs-lookup"><span data-stu-id="85b26-115">Return code</span></span>                                                                                   | <span data-ttu-id="85b26-116">Description</span><span class="sxs-lookup"><span data-stu-id="85b26-116">Description</span></span>                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="85b26-117"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="85b26-117"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="85b26-118">La méthode a réussi.</span><span class="sxs-lookup"><span data-stu-id="85b26-118">Method succeeded.</span></span><br/>                                    |
| <dl> <span data-ttu-id="85b26-119"><dt>**\_pointeur E**</dt></span><span class="sxs-lookup"><span data-stu-id="85b26-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="85b26-120">Le paramètre *ppName* n’est pas un pointeur valide.</span><span class="sxs-lookup"><span data-stu-id="85b26-120">The *ppName* parameter is not a valid pointer.</span></span><br/>       |
| <dl> <span data-ttu-id="85b26-121"><dt>**\_OUTOFMEMORY E**</dt></span><span class="sxs-lookup"><span data-stu-id="85b26-121"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="85b26-122">La mémoire disponible est insuffisante pour effectuer l’opération.</span><span class="sxs-lookup"><span data-stu-id="85b26-122">Insufficient memory exists to perform the operation.</span></span><br/> |
| <dl> <span data-ttu-id="85b26-123"><dt>**E \_ échec**</dt></span><span class="sxs-lookup"><span data-stu-id="85b26-123"><dt>**E\_FAIL**</dt></span></span> </dl>        | <span data-ttu-id="85b26-124">Erreur non spécifiée.</span><span class="sxs-lookup"><span data-stu-id="85b26-124">Unspecified error.</span></span><br/>                                   |
| <dl> <span data-ttu-id="85b26-125"><dt>**\_NOTIMPL E**</dt></span><span class="sxs-lookup"><span data-stu-id="85b26-125"><dt>**E\_NOTIMPL**</dt></span></span> </dl>     | <span data-ttu-id="85b26-126">Cette méthode n'est pas encore implémentée.</span><span class="sxs-lookup"><span data-stu-id="85b26-126">This method is not yet implemented.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="85b26-127">Notes</span><span class="sxs-lookup"><span data-stu-id="85b26-127">Remarks</span></span>

<span data-ttu-id="85b26-128">L’application doit utiliser [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) pour libérer la mémoire allouée pour le paramètre *ppName* .</span><span class="sxs-lookup"><span data-stu-id="85b26-128">The application must use [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) to free the memory allocated for the *ppName* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="85b26-129">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="85b26-129">Requirements</span></span>



| <span data-ttu-id="85b26-130">Condition requise</span><span class="sxs-lookup"><span data-stu-id="85b26-130">Requirement</span></span> | <span data-ttu-id="85b26-131">Valeur</span><span class="sxs-lookup"><span data-stu-id="85b26-131">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="85b26-132">Version TAPI</span><span class="sxs-lookup"><span data-stu-id="85b26-132">TAPI version</span></span><br/> | <span data-ttu-id="85b26-133">Nécessite TAPI 3,0 ou une version ultérieure</span><span class="sxs-lookup"><span data-stu-id="85b26-133">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="85b26-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="85b26-134">Header</span></span><br/>       | <dl> <span data-ttu-id="85b26-135"><dt>Sdpblb. h</dt></span><span class="sxs-lookup"><span data-stu-id="85b26-135"><dt>Sdpblb.h</dt></span></span> </dl>   |
| <span data-ttu-id="85b26-136">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="85b26-136">Library</span></span><br/>      | <dl> <span data-ttu-id="85b26-137"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="85b26-137"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="85b26-138">DLL</span><span class="sxs-lookup"><span data-stu-id="85b26-138">DLL</span></span><br/>          | <dl> <span data-ttu-id="85b26-139"><dt>Sdpblb.dll</dt></span><span class="sxs-lookup"><span data-stu-id="85b26-139"><dt>Sdpblb.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="85b26-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="85b26-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="85b26-141">**ITSdp**</span><span class="sxs-lookup"><span data-stu-id="85b26-141">**ITSdp**</span></span>](itsdp.md)
</dt> <dt>

[<span data-ttu-id="85b26-142">**ITSdp ::p nom de l’UT \_**</span><span class="sxs-lookup"><span data-stu-id="85b26-142">**ITSdp::put\_Name**</span></span>](itsdp-put-name.md)
</dt> </dl>

 

