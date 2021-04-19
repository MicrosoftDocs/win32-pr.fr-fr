---
description: Envoie une commande à un périphérique matériel WIA (Windows Image Acquisition) 2,0.
ms.assetid: a077448f-2029-4fd3-8bce-c0291afd0b79
title: IWiaItem2 ::D méthode eviceCommand (WIA. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaItem2.DeviceCommand
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 2961a3c0e0d1b75a487b9bf112e76bee8c937a72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106541185"
---
# <a name="iwiaitem2devicecommand-method"></a><span data-ttu-id="97f9d-103">IWiaItem2 ::D méthode eviceCommand</span><span class="sxs-lookup"><span data-stu-id="97f9d-103">IWiaItem2::DeviceCommand method</span></span>

<span data-ttu-id="97f9d-104">Envoie une commande à un périphérique matériel WIA (Windows Image Acquisition) 2,0.</span><span class="sxs-lookup"><span data-stu-id="97f9d-104">Issues a command to a Windows Image Acquisition (WIA) 2.0 hardware device.</span></span>

## <a name="syntax"></a><span data-ttu-id="97f9d-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="97f9d-105">Syntax</span></span>


```C++
HRESULT DeviceCommand(
  [in]            LONG      lFlags,
  [in]      const GUID      *pCmdGUID,
  [in, out]       IWiaItem2 **ppIWiaItem2
);
```



## <a name="parameters"></a><span data-ttu-id="97f9d-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="97f9d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97f9d-107">*lFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="97f9d-107">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97f9d-108">Type : **long**</span><span class="sxs-lookup"><span data-stu-id="97f9d-108">Type: **LONG**</span></span>

<span data-ttu-id="97f9d-109">Actuellement inutilisé.</span><span class="sxs-lookup"><span data-stu-id="97f9d-109">Currently unused.</span></span> <span data-ttu-id="97f9d-110">Doit être défini sur zéro (0).</span><span class="sxs-lookup"><span data-stu-id="97f9d-110">Should be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="97f9d-111">*pCmdGUID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="97f9d-111">*pCmdGUID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97f9d-112">Type : \* #*const \* GUID* _</span><span class="sxs-lookup"><span data-stu-id="97f9d-112">Type: \**const GUID\** _</span></span>

<span data-ttu-id="97f9d-113">Spécifie la commande à envoyer à l’appareil WIA 2,0.</span><span class="sxs-lookup"><span data-stu-id="97f9d-113">Specifies the command to send to the WIA 2.0 device.</span></span> <span data-ttu-id="97f9d-114">Consultez [les *commandes* \* de l’appareil _ WIA](-wia-wia-device-commands.md).</span><span class="sxs-lookup"><span data-stu-id="97f9d-114">See [_ *WIA Device Commands*\*](-wia-wia-device-commands.md).</span></span>

</dd> <dt>

<span data-ttu-id="97f9d-115">*ppIWiaItem2* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="97f9d-115">*ppIWiaItem2* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="97f9d-116">Type : **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="97f9d-116">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="97f9d-117">Reçoit l’adresse d’un pointeur vers l’élément [**IWiaItem2**](-wia-iwiaitem2.md) créé par la commande, le cas échéant.</span><span class="sxs-lookup"><span data-stu-id="97f9d-117">Receives the address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) item created by the command, if any.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97f9d-118">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="97f9d-118">Return value</span></span>

<span data-ttu-id="97f9d-119">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="97f9d-119">Type: **HRESULT**</span></span>

<span data-ttu-id="97f9d-120">En plus des codes d’erreur COM standard, la méthode peut retourner la valeur suivante.</span><span class="sxs-lookup"><span data-stu-id="97f9d-120">In addition to the standard COM error codes, the method may return the following value.</span></span>



| <span data-ttu-id="97f9d-121">Code de retour</span><span class="sxs-lookup"><span data-stu-id="97f9d-121">Return code</span></span>                                                                                       | <span data-ttu-id="97f9d-122">Description</span><span class="sxs-lookup"><span data-stu-id="97f9d-122">Description</span></span>                                                                                                                                                                          |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="97f9d-123"><dt>**\_CMDNOTSUPPORTED E**</dt></span><span class="sxs-lookup"><span data-stu-id="97f9d-123"><dt>**E\_CMDNOTSUPPORTED**</dt></span></span> </dl> | <span data-ttu-id="97f9d-124">La commande n’est pas implémentée pour l’interface [**IWiaItem2**](-wia-iwiaitem2.md) sur laquelle la méthode est appelée.</span><span class="sxs-lookup"><span data-stu-id="97f9d-124">The command is not implemented for the [**IWiaItem2**](-wia-iwiaitem2.md) interface on which the method is called.</span></span> <span data-ttu-id="97f9d-125">La valeur numérique de cette erreur n’est pas encore définie.</span><span class="sxs-lookup"><span data-stu-id="97f9d-125">The numeric value for this error is not yet defined.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="97f9d-126">Notes</span><span class="sxs-lookup"><span data-stu-id="97f9d-126">Remarks</span></span>

<span data-ttu-id="97f9d-127">Le comportement de cette méthode est différent selon la catégorie du nœud sur lequel la méthode est appelée.</span><span class="sxs-lookup"><span data-stu-id="97f9d-127">The behavior of this method is different depending on the category of the node on which the method is called.</span></span>

<span data-ttu-id="97f9d-128">Lorsque l’application envoie la commande [**WIA \_ cmd \_ Take \_ image**](-wia-wia-device-commands.md) à l’appareil à l’aide de la méthode **IWiaItem2 ::D EVICECOMMAND** , le système d’exécution WIA 2,0 crée un objet [**IWiaItem2**](-wia-iwiaitem2.md) pour représenter l’image.</span><span class="sxs-lookup"><span data-stu-id="97f9d-128">When the application sends the [**WIA\_CMD\_TAKE\_PICTURE**](-wia-wia-device-commands.md) command to the device using the **IWiaItem2::DeviceCommand** method, the WIA 2.0 run-time system creates an [**IWiaItem2**](-wia-iwiaitem2.md) object to represent the image.</span></span> <span data-ttu-id="97f9d-129">La méthode **IWiaItem2 ::D evicecommand** stocke l’adresse de l’interface dans le paramètre *ppIWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="97f9d-129">The **IWiaItem2::DeviceCommand** method stores the address of the interface in the *ppIWiaItem2* parameter.</span></span>

<span data-ttu-id="97f9d-130">Les applications doivent appeler la méthode [IUnknown :: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sur les pointeurs d’interface qu’elles reçoivent via le paramètre *ppIWiaItem2* .</span><span class="sxs-lookup"><span data-stu-id="97f9d-130">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppIWiaItem2* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="97f9d-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="97f9d-131">Requirements</span></span>



| <span data-ttu-id="97f9d-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="97f9d-132">Requirement</span></span> | <span data-ttu-id="97f9d-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="97f9d-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="97f9d-134">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="97f9d-134">Minimum supported client</span></span><br/> | <span data-ttu-id="97f9d-135">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="97f9d-135">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="97f9d-136">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="97f9d-136">Minimum supported server</span></span><br/> | <span data-ttu-id="97f9d-137">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="97f9d-137">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="97f9d-138">En-tête</span><span class="sxs-lookup"><span data-stu-id="97f9d-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="97f9d-139"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="97f9d-139"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="97f9d-140">MIDL</span><span class="sxs-lookup"><span data-stu-id="97f9d-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="97f9d-141"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="97f9d-141"><dt>Wia.idl</dt></span></span> </dl> |



 

 
