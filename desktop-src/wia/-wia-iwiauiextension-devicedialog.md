---
description: IWiaUIExtension ::D méthode eviceDialog-fournit une interface utilisateur personnalisée qui remplace l’interface utilisateur système par défaut.
ms.assetid: 5dbcacde-5bbe-459d-804f-5ce7eb1cd8d8
title: IWiaUIExtension ::D méthode eviceDialog (Wiadevd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaUIExtension.DeviceDialog
api_type:
- COM
api_location:
- Wiadevd.h
ms.openlocfilehash: d467769308707032b8e92b4ac7877488991356dd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108116707"
---
# <a name="iwiauiextensiondevicedialog-method"></a><span data-ttu-id="e9c26-103">IWiaUIExtension ::D méthode eviceDialog</span><span class="sxs-lookup"><span data-stu-id="e9c26-103">IWiaUIExtension::DeviceDialog method</span></span>

<span data-ttu-id="e9c26-104">Fournit une interface utilisateur personnalisée qui remplace l’interface utilisateur système par défaut.</span><span class="sxs-lookup"><span data-stu-id="e9c26-104">Provides a custom user interface that replaces the default system user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9c26-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e9c26-105">Syntax</span></span>


```C++
HRESULT DeviceDialog(
  [in] PDEVICEDIALOGDATA *pDeviceDialogData
);
```



## <a name="parameters"></a><span data-ttu-id="e9c26-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e9c26-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9c26-107">*pDeviceDialogData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e9c26-107">*pDeviceDialogData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e9c26-108">Type : **PDEVICEDIALOGDATA \***</span><span class="sxs-lookup"><span data-stu-id="e9c26-108">Type: **PDEVICEDIALOGDATA\***</span></span>

<span data-ttu-id="e9c26-109">Pointe vers une structure [**DEVICEDIALOGDATA**](-wia-devicedialogdata.md) qui contient toutes les données nécessaires pour implémenter la boîte de dialogue de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e9c26-109">Points to a [**DEVICEDIALOGDATA**](-wia-devicedialogdata.md) structure that contains all of the data needed to implement the device dialog.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9c26-110">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="e9c26-110">Return value</span></span>

<span data-ttu-id="e9c26-111">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e9c26-111">Type: **HRESULT**</span></span>

<span data-ttu-id="e9c26-112">Si la méthode est réussie, elle retourne la valeur \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e9c26-112">If the method succeeds, it returns S\_OK.</span></span> <span data-ttu-id="e9c26-113">Si l’utilisateur annule la boîte de dialogue, la méthode retourne S \_ false.</span><span class="sxs-lookup"><span data-stu-id="e9c26-113">If the user cancels the dialog, the method returns S\_FALSE.</span></span> <span data-ttu-id="e9c26-114">Si la méthode n’est pas implémentée, elle retourne E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="e9c26-114">If the method is not implemented, it returns E\_NOTIMPL.</span></span> <span data-ttu-id="e9c26-115">Si la méthode échoue, elle retourne un code d’erreur COM standard.</span><span class="sxs-lookup"><span data-stu-id="e9c26-115">If the method fails, it returns a standard COM error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9c26-116">Notes </span><span class="sxs-lookup"><span data-stu-id="e9c26-116">Remarks</span></span>

<span data-ttu-id="e9c26-117">Si vous implémentez l’interface [**IWiaUIExtension**](-wia-iwiauiextension.md) et que vous ne souhaitez pas remplacer l’interface utilisateur système, cette méthode doit encore être implémentée, mais elle ne doit rien faire d’autre que retourner E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="e9c26-117">If you implement the [**IWiaUIExtension**](-wia-iwiauiextension.md) interface and do not want to replace the system user interface, this method must still be implemented, but it should do nothing more than return E\_NOTIMPL.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9c26-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e9c26-118">Requirements</span></span>



| <span data-ttu-id="e9c26-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e9c26-119">Requirement</span></span> | <span data-ttu-id="e9c26-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="e9c26-120">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e9c26-121">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e9c26-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e9c26-122">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e9c26-122">Windows XP \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="e9c26-123">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e9c26-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e9c26-124">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e9c26-124">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e9c26-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="e9c26-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9c26-126"><dt>Wiadevd. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9c26-126"><dt>Wiadevd.h</dt></span></span> </dl> |



 

 




