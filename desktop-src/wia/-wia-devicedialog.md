---
description: Utilisé par les applications pour afficher une boîte de dialogue d’appareil à l’utilisateur.
ms.assetid: 3b486220-32ab-4d6c-872c-684f9d1ee660
title: DeviceDialog, fonction (Wiadevd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceDialog
api_type:
- LibDef
api_location:
- Wiaguid.lib
- Wiaguid.dll
ms.openlocfilehash: 7389b0466dadf530da6fb7cd386d8a57d92cf1c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533904"
---
# <a name="devicedialog-function"></a><span data-ttu-id="e7bd6-103">DeviceDialog fonction)</span><span class="sxs-lookup"><span data-stu-id="e7bd6-103">DeviceDialog function</span></span>

<span data-ttu-id="e7bd6-104">Utilisé par les applications pour afficher une boîte de dialogue d’appareil à l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="e7bd6-104">Used by applications to display a device dialog box to the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="e7bd6-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e7bd6-105">Syntax</span></span>


```C++
HRESULT WINAPI DeviceDialog(
  _In_ PDEVICEDIALOGDATA pDeviceDialogData
);
```



## <a name="parameters"></a><span data-ttu-id="e7bd6-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e7bd6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7bd6-107">*pDeviceDialogData* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e7bd6-107">*pDeviceDialogData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e7bd6-108">Type : **PDEVICEDIALOGDATA**</span><span class="sxs-lookup"><span data-stu-id="e7bd6-108">Type: **PDEVICEDIALOGDATA**</span></span>

<span data-ttu-id="e7bd6-109">[**DEVICEDIALOGDATA**](-wia-devicedialogdata.md) à utiliser pour créer la boîte de dialogue de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="e7bd6-109">The [**DEVICEDIALOGDATA**](-wia-devicedialogdata.md) to use to create the device dialog.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e7bd6-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e7bd6-110">Return value</span></span>

<span data-ttu-id="e7bd6-111">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e7bd6-111">Type: **HRESULT**</span></span>

<span data-ttu-id="e7bd6-112">Si cette fonction est correctement exécutée, elle retourne la valeur **\_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e7bd6-112">If this function succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e7bd6-113">Sinon, elle retourne un code d’erreur **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e7bd6-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7bd6-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e7bd6-114">Requirements</span></span>



| <span data-ttu-id="e7bd6-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e7bd6-115">Requirement</span></span> | <span data-ttu-id="e7bd6-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="e7bd6-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e7bd6-117">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7bd6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e7bd6-118">Applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e7bd6-118">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="e7bd6-119">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e7bd6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e7bd6-120">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e7bd6-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e7bd6-121">En-tête</span><span class="sxs-lookup"><span data-stu-id="e7bd6-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e7bd6-122"><dt>Wiadevd. h</dt></span><span class="sxs-lookup"><span data-stu-id="e7bd6-122"><dt>Wiadevd.h</dt></span></span> </dl>   |
| <span data-ttu-id="e7bd6-123">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="e7bd6-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="e7bd6-124"><dt>Wiaguid. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e7bd6-124"><dt>Wiaguid.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7bd6-125">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="e7bd6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7bd6-126">**DEVICEDIALOGDATA**</span><span class="sxs-lookup"><span data-stu-id="e7bd6-126">**DEVICEDIALOGDATA**</span></span>](-wia-devicedialogdata.md)
</dt> </dl>

 

 




