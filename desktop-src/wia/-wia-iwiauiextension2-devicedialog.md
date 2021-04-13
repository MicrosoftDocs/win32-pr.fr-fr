---
description: Fournit une interface utilisateur personnalisée qui remplace l’interface utilisateur système par défaut.
ms.assetid: 0d70392d-294a-42bf-adc5-1006f83d7e21
title: IWiaUIExtension2 ::D méthode eviceDialog (Wiadevd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension2.DeviceDialog
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: 142ec77572708063e24b38d342fb49f69c7651c5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104201487"
---
# <a name="iwiauiextension2devicedialog-method"></a><span data-ttu-id="b98d1-103">IWiaUIExtension2 ::D méthode eviceDialog</span><span class="sxs-lookup"><span data-stu-id="b98d1-103">IWiaUIExtension2::DeviceDialog method</span></span>

<span data-ttu-id="b98d1-104">Fournit une interface utilisateur personnalisée qui remplace l’interface utilisateur système par défaut.</span><span class="sxs-lookup"><span data-stu-id="b98d1-104">Provides a custom user interface that replaces the default system user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="b98d1-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="b98d1-105">Syntax</span></span>


```C++
HRESULT DeviceDialog(
  [in] PDEVICEDIALOGDATA2 *pDeviceDialogData
);
```



## <a name="parameters"></a><span data-ttu-id="b98d1-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="b98d1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b98d1-107">*pDeviceDialogData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="b98d1-107">*pDeviceDialogData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b98d1-108">Tapez : \**PDEVICEDIALOGDATA2 \** _</span><span class="sxs-lookup"><span data-stu-id="b98d1-108">Type: \**PDEVICEDIALOGDATA2\** _</span></span>

<span data-ttu-id="b98d1-109">Pointe vers une structure [_ *DEVICEDIALOGDATA2* \*](-wia-devicedialogdata2.md) qui contient toutes les données nécessaires pour implémenter la boîte de dialogue de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="b98d1-109">Points to a [_ *DEVICEDIALOGDATA2*\*](-wia-devicedialogdata2.md) structure that contains all of the data needed to implement the device dialog.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b98d1-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="b98d1-110">Return value</span></span>

<span data-ttu-id="b98d1-111">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="b98d1-111">Type: **HRESULT**</span></span>

<span data-ttu-id="b98d1-112">Si la méthode est réussie, elle retourne la valeur \_ OK.</span><span class="sxs-lookup"><span data-stu-id="b98d1-112">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="b98d1-113">Si l’utilisateur annule la boîte de dialogue, la méthode retourne S \_ false.</span><span class="sxs-lookup"><span data-stu-id="b98d1-113">If the user cancels the dialog, the method returns S\_FALSE.</span></span> <span data-ttu-id="b98d1-114">Si la méthode échoue, elle retourne un code d’erreur approprié.</span><span class="sxs-lookup"><span data-stu-id="b98d1-114">If the method fails, it returns an appropriate error code.</span></span> <span data-ttu-id="b98d1-115">Le tableau suivant présente certains des codes d’état de retour possibles.</span><span class="sxs-lookup"><span data-stu-id="b98d1-115">The following table shows some of the possible return status codes.</span></span>



| <span data-ttu-id="b98d1-116">Code d'erreur</span><span class="sxs-lookup"><span data-stu-id="b98d1-116">Error code</span></span>    | <span data-ttu-id="b98d1-117">Description</span><span class="sxs-lookup"><span data-stu-id="b98d1-117">Description</span></span>                              |
|---------------|------------------------------------------|
| <span data-ttu-id="b98d1-118">E \_ INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="b98d1-118">E\_INVALIDARG</span></span> | <span data-ttu-id="b98d1-119">Le paramètre pDeviceDialogData a la **valeur null**.</span><span class="sxs-lookup"><span data-stu-id="b98d1-119">Parameter pDeviceDialogData is **NULL**.</span></span> |
| <span data-ttu-id="b98d1-120">\_NOTIMPL E</span><span class="sxs-lookup"><span data-stu-id="b98d1-120">E\_NOTIMPL</span></span>    | <span data-ttu-id="b98d1-121">Cette méthode n'est pas implémentée.</span><span class="sxs-lookup"><span data-stu-id="b98d1-121">The method is not implemented.</span></span>           |



 

## <a name="remarks"></a><span data-ttu-id="b98d1-122">Notes</span><span class="sxs-lookup"><span data-stu-id="b98d1-122">Remarks</span></span>

<span data-ttu-id="b98d1-123">Si vous implémentez l’interface [**IWiaUIExtension2**](-wia-iwiauiextension2.md) et que vous ne souhaitez pas remplacer l’interface utilisateur système, cette méthode doit encore être implémentée, mais elle ne doit rien faire d’autre que retourner E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="b98d1-123">If you implement the [**IWiaUIExtension2**](-wia-iwiauiextension2.md) interface and do not want to replace the system user interface, this method must still be implemented, but it should do nothing more than return E\_NOTIMPL.</span></span>

## <a name="requirements"></a><span data-ttu-id="b98d1-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="b98d1-124">Requirements</span></span>



| <span data-ttu-id="b98d1-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="b98d1-125">Requirement</span></span> | <span data-ttu-id="b98d1-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="b98d1-126">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b98d1-127">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b98d1-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b98d1-128">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b98d1-128">Windows Vista \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="b98d1-129">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="b98d1-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b98d1-130">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="b98d1-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b98d1-131">En-tête</span><span class="sxs-lookup"><span data-stu-id="b98d1-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="b98d1-132"><dt>Wiadevd. h</dt></span><span class="sxs-lookup"><span data-stu-id="b98d1-132"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 




