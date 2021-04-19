---
description: Retourne une chaîne qui décrit le code d’État.
ms.assetid: d3007f3e-46e1-4ab6-8ce3-c4e38f87ce61
title: 'IWiaErrorHandler :: GetStatusDescription, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaErrorHandler.GetStatusDescription
api_type:
- COM
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: da23e413ee238f43ae577a51b18a542dc1b0768c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106516048"
---
# <a name="iwiaerrorhandlergetstatusdescription-method"></a><span data-ttu-id="9305a-103">IWiaErrorHandler :: GetStatusDescription, méthode</span><span class="sxs-lookup"><span data-stu-id="9305a-103">IWiaErrorHandler::GetStatusDescription method</span></span>

<span data-ttu-id="9305a-104">Retourne une chaîne qui décrit le code d’État.</span><span class="sxs-lookup"><span data-stu-id="9305a-104">Returns a string that describes the status code.</span></span>

## <a name="syntax"></a><span data-ttu-id="9305a-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="9305a-105">Syntax</span></span>


```C++
HRESULT GetStatusDescription(
  [in]  IUnknown *punkItem,
  [in]  HRESULT  hrStatus,
  [in]  LONG     cbResLength,
  [in]  BYTE     *pbData,
  [out] BSTR     *pbstrDescription
);
```



## <a name="parameters"></a><span data-ttu-id="9305a-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="9305a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9305a-107">*punkItem* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9305a-107">*punkItem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9305a-108">Tapez : \**[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _</span><span class="sxs-lookup"><span data-stu-id="9305a-108">Type: \**[IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown)\** _</span></span>

<span data-ttu-id="9305a-109">Pointeur vers le [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) de l’élément en cours de transfert.</span><span class="sxs-lookup"><span data-stu-id="9305a-109">Pointer to the [IUnknown](/windows/win32/api/unknwn/nn-unknwn-iunknown) of the item being transferred.</span></span> <span data-ttu-id="9305a-110">Cet objet implémente au minimum [_ *IWiaItem2* \*](-wia-iwiaitem2.md) et [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer).</span><span class="sxs-lookup"><span data-stu-id="9305a-110">This object minimally implements [_ *IWiaItem2*\*](-wia-iwiaitem2.md) and [**IWiaDataTransfer**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadatatransfer).</span></span>

</dd> <dt>

<span data-ttu-id="9305a-111">*hrStatus* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9305a-111">*hrStatus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9305a-112">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9305a-112">Type: **HRESULT**</span></span>

<span data-ttu-id="9305a-113">**HRESULT** qui correspond au code d’état reçu par [**BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span><span class="sxs-lookup"><span data-stu-id="9305a-113">**HRESULT** that is the status code received by [**BandedDataCallback**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span></span>

</dd> <dt>

<span data-ttu-id="9305a-114">*cbResLength* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9305a-114">*cbResLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9305a-115">Type : **long**</span><span class="sxs-lookup"><span data-stu-id="9305a-115">Type: **LONG**</span></span>

<span data-ttu-id="9305a-116">**Valeur de type long** qui correspond à la taille des données référencées par *pbData*.</span><span class="sxs-lookup"><span data-stu-id="9305a-116">**LONG** that is the size of the data referred to by *pbData*.</span></span>

</dd> <dt>

<span data-ttu-id="9305a-117">*pbData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="9305a-117">*pbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9305a-118">Type : \**Byte \** _</span><span class="sxs-lookup"><span data-stu-id="9305a-118">Type: \**BYTE\** _</span></span>

<span data-ttu-id="9305a-119">Pointeur vers la mémoire tampon de données telle qu’elle a été reçue par [_ *BandedDataCallback* \*](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span><span class="sxs-lookup"><span data-stu-id="9305a-119">Pointer to the data buffer as received by [_ *BandedDataCallback*\*](/windows/desktop/api/wia_xp/nf-wia_xp-iwiadatacallback-bandeddatacallback).</span></span>

</dd> <dt>

<span data-ttu-id="9305a-120">*pbstrDescription* \[ à\]</span><span class="sxs-lookup"><span data-stu-id="9305a-120">*pbstrDescription* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9305a-121">Type : \**BSTR \** _</span><span class="sxs-lookup"><span data-stu-id="9305a-121">Type: \**BSTR\** _</span></span>

<span data-ttu-id="9305a-122">_ *BSTR*\* qui reçoit une description de l’État ou de l’erreur rencontrée pendant le transfert de données.</span><span class="sxs-lookup"><span data-stu-id="9305a-122">_ *BSTR*\* that receives a description of the status or error encountered during the data transfer.</span></span> <span data-ttu-id="9305a-123">Ce paramètre ne peut pas être **null**.</span><span class="sxs-lookup"><span data-stu-id="9305a-123">This parameter cannot be **NULL**.</span></span> <span data-ttu-id="9305a-124">L’appelant doit libérer la chaîne à l’aide de [SysFreeString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring), et l’implémenteur doit allouer la chaîne à l’aide de [SysAllocString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring).</span><span class="sxs-lookup"><span data-stu-id="9305a-124">The caller must free the string using [SysFreeString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring), and the implementor must allocate the string using [SysAllocString](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9305a-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="9305a-125">Return value</span></span>

<span data-ttu-id="9305a-126">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="9305a-126">Type: **HRESULT**</span></span>

<span data-ttu-id="9305a-127">Retourne l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="9305a-127">Returns one of the following values.</span></span>



| <span data-ttu-id="9305a-128">Code de retour</span><span class="sxs-lookup"><span data-stu-id="9305a-128">Return code</span></span>                                                                             | <span data-ttu-id="9305a-129">Description</span><span class="sxs-lookup"><span data-stu-id="9305a-129">Description</span></span>                                                        |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <span data-ttu-id="9305a-130"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="9305a-130"><dt>**S\_OK**</dt></span></span> </dl>    | <span data-ttu-id="9305a-131">*pbstrDescription* contient un pointeur **BSTR** valide.</span><span class="sxs-lookup"><span data-stu-id="9305a-131">*pbstrDescription* contains a valid **BSTR** pointer.</span></span> <br/>  |
| <dl> <span data-ttu-id="9305a-132"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="9305a-132"><dt>**S\_FALSE**</dt></span></span> </dl> | <span data-ttu-id="9305a-133">*hrStatus* est inconnu et aucune description n’est disponible.</span><span class="sxs-lookup"><span data-stu-id="9305a-133">*hrStatus* is unknown and no description is available.</span></span> <br/> |



 

## <a name="requirements"></a><span data-ttu-id="9305a-134">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9305a-134">Requirements</span></span>



| <span data-ttu-id="9305a-135">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9305a-135">Requirement</span></span> | <span data-ttu-id="9305a-136">Valeur</span><span class="sxs-lookup"><span data-stu-id="9305a-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9305a-137">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9305a-137">Minimum supported client</span></span><br/> | <span data-ttu-id="9305a-138">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9305a-138">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="9305a-139">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="9305a-139">Minimum supported server</span></span><br/> | <span data-ttu-id="9305a-140">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="9305a-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9305a-141">En-tête</span><span class="sxs-lookup"><span data-stu-id="9305a-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="9305a-142"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="9305a-142"><dt>Wia.h</dt></span></span> </dl>       |
| <span data-ttu-id="9305a-143">MIDL</span><span class="sxs-lookup"><span data-stu-id="9305a-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9305a-144"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9305a-144"><dt>Wia.idl</dt></span></span> </dl>     |
| <span data-ttu-id="9305a-145">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="9305a-145">Library</span></span><br/>                  | <dl> <span data-ttu-id="9305a-146"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9305a-146"><dt>Wiaguid.lib</dt></span></span> </dl> |



 

 
