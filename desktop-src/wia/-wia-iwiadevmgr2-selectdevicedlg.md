---
description: 'IWiaDevMgr2 :: SelectDeviceDlg, méthode-affiche une boîte de dialogue qui permet à l’utilisateur de sélectionner un périphérique matériel pour l’acquisition d’images.'
ms.assetid: cd020dc6-fddf-4d7f-aa57-eae94953ef4e
title: 'IWiaDevMgr2 :: SelectDeviceDlg, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.SelectDeviceDlg
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 60ec24f264b8fe0424f17fc32deaf803e55c3346
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108091257"
---
# <a name="iwiadevmgr2selectdevicedlg-method"></a><span data-ttu-id="3d8a8-103">IWiaDevMgr2 :: SelectDeviceDlg, méthode</span><span class="sxs-lookup"><span data-stu-id="3d8a8-103">IWiaDevMgr2::SelectDeviceDlg method</span></span>

<span data-ttu-id="3d8a8-104">Affiche une boîte de dialogue qui permet à l’utilisateur de sélectionner un périphérique matériel pour l’acquisition d’images.</span><span class="sxs-lookup"><span data-stu-id="3d8a8-104">Displays a dialog box that enables the user to select a hardware device for image acquisition.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d8a8-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3d8a8-105">Syntax</span></span>


```C++
HRESULT SelectDeviceDlg(
  [in]          HWND      hwndParent,
  [in]          LONG      lDeviceType,
  [in]          LONG      lFlags,
  [in, out]     BSTR      *pbstrDeviceID,
  [out, retval] IWiaItem2 **ppItemRoot
);
```



## <a name="parameters"></a><span data-ttu-id="3d8a8-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="3d8a8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d8a8-107">*hwndParent* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3d8a8-107">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d8a8-108">Type : **HWND**</span><span class="sxs-lookup"><span data-stu-id="3d8a8-108">Type: **HWND**</span></span>

<span data-ttu-id="3d8a8-109">Spécifie la fenêtre parente de la boîte de dialogue **Sélectionner un périphérique** .</span><span class="sxs-lookup"><span data-stu-id="3d8a8-109">Specifies the parent window of the **Select Device** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="3d8a8-110">*lDeviceType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3d8a8-110">*lDeviceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d8a8-111">Type : **long**</span><span class="sxs-lookup"><span data-stu-id="3d8a8-111">Type: **LONG**</span></span>

<span data-ttu-id="3d8a8-112">Spécifie le type d’appareil WIA 2,0 à utiliser.</span><span class="sxs-lookup"><span data-stu-id="3d8a8-112">Specifies which type of WIA 2.0 device to use.</span></span> <span data-ttu-id="3d8a8-113">Pour obtenir la liste des valeurs possibles, consultez [spécificateurs de type d’appareil WIA](-wia-wia-device-type-specifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="3d8a8-113">See [WIA Device Type Specifiers](-wia-wia-device-type-specifiers.md) for a list of possible values.</span></span>

</dd> <dt>

<span data-ttu-id="3d8a8-114">*lFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="3d8a8-114">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3d8a8-115">Type : **long**</span><span class="sxs-lookup"><span data-stu-id="3d8a8-115">Type: **LONG**</span></span>

<span data-ttu-id="3d8a8-116">Spécifie le comportement de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="3d8a8-116">Specifies the behavior of the dialog box.</span></span> <span data-ttu-id="3d8a8-117">La valeur peut être l’une des suivantes.</span><span class="sxs-lookup"><span data-stu-id="3d8a8-117">The value can be one of the following.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="3d8a8-118"><span id="0"></span>**entre**</span><span class="sxs-lookup"><span data-stu-id="3d8a8-118"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="3d8a8-119">Utiliser le comportement par défaut.</span><span class="sxs-lookup"><span data-stu-id="3d8a8-119">Use the default behavior.</span></span>

</dd> <dt>

<span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>

<span data-ttu-id="3d8a8-120"><span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>**WIA- \_ Sélectionner un \_ appareil \_ par défaut**</span><span class="sxs-lookup"><span data-stu-id="3d8a8-120"><span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>**WIA\_SELECT\_DEVICE\_NODEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="3d8a8-121">Affiche la boîte de dialogue même s’il n’y a qu’un seul appareil correspondant.</span><span class="sxs-lookup"><span data-stu-id="3d8a8-121">Display the dialog box even though there is only one matching device.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="3d8a8-122">*pbstrDeviceID* \[ in, out\]</span><span class="sxs-lookup"><span data-stu-id="3d8a8-122">*pbstrDeviceID* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="3d8a8-123">Type : **BSTR \***</span><span class="sxs-lookup"><span data-stu-id="3d8a8-123">Type: **BSTR\***</span></span>

<span data-ttu-id="3d8a8-124">Lors de la sortie, reçoit une chaîne qui contient la chaîne d’identificateur de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="3d8a8-124">On output, receives a string which contains the device's identifier string.</span></span> <span data-ttu-id="3d8a8-125">En entrée, transmettez l’adresse d’un pointeur si ces informations sont nécessaires, ou la **valeur null** si elle n’est pas nécessaire.</span><span class="sxs-lookup"><span data-stu-id="3d8a8-125">On input, pass the address of a pointer if this information is needed, or **NULL** if it is not needed.</span></span>

</dd> <dt>

<span data-ttu-id="3d8a8-126">*ppItemRoot* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="3d8a8-126">*ppItemRoot* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="3d8a8-127">Type : **[ **IWiaItem2**](-wia-iwiaitem2.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="3d8a8-127">Type: **[**IWiaItem2**](-wia-iwiaitem2.md)\*\***</span></span>

<span data-ttu-id="3d8a8-128">Reçoit l’adresse d’un pointeur vers l’interface [**IWiaItem2**](-wia-iwiaitem2.md) de l’élément racine de l’arborescence hiérarchique qui représente l’appareil WIA 2,0 sélectionné.</span><span class="sxs-lookup"><span data-stu-id="3d8a8-128">Receives the address of a pointer to the [**IWiaItem2**](-wia-iwiaitem2.md) interface of the root item of the hierarchical tree that represents the selected WIA 2.0 device.</span></span> <span data-ttu-id="3d8a8-129">Si aucun appareil n’est trouvé, la **valeur null** est reçue.</span><span class="sxs-lookup"><span data-stu-id="3d8a8-129">If no device is found, it receives **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d8a8-130">Valeur renvoyée</span><span class="sxs-lookup"><span data-stu-id="3d8a8-130">Return value</span></span>

<span data-ttu-id="3d8a8-131">Type : **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="3d8a8-131">Type: **HRESULT**</span></span>

<span data-ttu-id="3d8a8-132">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="3d8a8-132">This method can return one of these values.</span></span>



| <span data-ttu-id="3d8a8-133">Code de retour</span><span class="sxs-lookup"><span data-stu-id="3d8a8-133">Return code</span></span>                                                                                                  | <span data-ttu-id="3d8a8-134">Description</span><span class="sxs-lookup"><span data-stu-id="3d8a8-134">Description</span></span>                                                                                            |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3d8a8-135"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="3d8a8-135"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="3d8a8-136">L’appareil a été sélectionné avec succès.</span><span class="sxs-lookup"><span data-stu-id="3d8a8-136">Device was successfully selected.</span></span> <br/>                                                          |
| <dl> <span data-ttu-id="3d8a8-137"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="3d8a8-137"><dt>**S\_FALSE**</dt></span></span> </dl>                      | <span data-ttu-id="3d8a8-138">L’utilisateur a annulé la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="3d8a8-138">User canceled the dialog box.</span></span> <br/>                                                              |
| <dl> <span data-ttu-id="3d8a8-139"><dt>**WIA \_ - \_ aucun \_ appareil \_ disponible**</dt></span><span class="sxs-lookup"><span data-stu-id="3d8a8-139"><dt>**WIA\_S\_NO\_DEVICE\_AVAILABLE**</dt></span></span> </dl> | <span data-ttu-id="3d8a8-140">Aucun périphérique matériel WIA 2,0 ne correspond aux spécifications indiquées dans le paramètre *lDeviceType* .</span><span class="sxs-lookup"><span data-stu-id="3d8a8-140">No WIA 2.0 hardware devices match the specifications given in the *lDeviceType* parameter.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="3d8a8-141">Notes </span><span class="sxs-lookup"><span data-stu-id="3d8a8-141">Remarks</span></span>

<span data-ttu-id="3d8a8-142">Cette méthode crée et affiche la boîte de dialogue **Sélectionner un appareil** afin que l’utilisateur puisse sélectionner un appareil WIA 2,0 pour l’acquisition d’images.</span><span class="sxs-lookup"><span data-stu-id="3d8a8-142">This method creates and displays the **Select Device** dialog box so the user can select a WIA 2.0 device for image acquisition.</span></span> <span data-ttu-id="3d8a8-143">Si un appareil est sélectionné avec succès, la méthode **IWiaDevMgr2 :: SelectDeviceDlg** crée une arborescence hiérarchique d’objets [**IWiaItem2**](-wia-iwiaitem2.md) pour l’appareil.</span><span class="sxs-lookup"><span data-stu-id="3d8a8-143">If a device is successfully selected, the **IWiaDevMgr2::SelectDeviceDlg** method creates a hierarchical tree of [**IWiaItem2**](-wia-iwiaitem2.md) objects for the device.</span></span> <span data-ttu-id="3d8a8-144">Elle stocke un pointeur vers l’interface **IWiaItem2** de l’élément racine dans le paramètre *ppItemRoot*.</span><span class="sxs-lookup"><span data-stu-id="3d8a8-144">It stores a pointer to the **IWiaItem2** interface of the root item in the parameter *ppItemRoot*.</span></span>

<span data-ttu-id="3d8a8-145">L’application peut limiter les appareils affichés à l’utilisateur à des types particuliers en spécifiant les types d’appareils via le paramètre *lDeviceType* .</span><span class="sxs-lookup"><span data-stu-id="3d8a8-145">The application can restrict the devices displayed to the user to particular types by specifying the device types through the *lDeviceType* parameter.</span></span> <span data-ttu-id="3d8a8-146">Si un seul périphérique répond à la spécification, **IWiaDevMgr2 :: SelectDeviceDlg** n’affiche pas la boîte de dialogue **Sélectionner un périphérique** .</span><span class="sxs-lookup"><span data-stu-id="3d8a8-146">If only one device meets the specification, **IWiaDevMgr2::SelectDeviceDlg** does not display the **Select Device** dialog box.</span></span> <span data-ttu-id="3d8a8-147">Au lieu de cela, il crée l’arborescence [**IWiaItem2**](-wia-iwiaitem2.md) pour l’appareil et stocke un pointeur vers l’interface **IWiaItem2** de l’élément racine dans le paramètre *ppItemRoot*.</span><span class="sxs-lookup"><span data-stu-id="3d8a8-147">Instead it creates the [**IWiaItem2**](-wia-iwiaitem2.md) tree for the device and store a pointer to the **IWiaItem2** interface of the root item in the parameter *ppItemRoot*.</span></span> <span data-ttu-id="3d8a8-148">Vous pouvez remplacer ce comportement et forcer **IWiaDevMgr2 :: SelectDeviceDlg** à afficher la boîte de dialogue en spécifiant \_ WIA \_ Select \_ Device NODEFAULT comme valeur du paramètre *lFlags* .</span><span class="sxs-lookup"><span data-stu-id="3d8a8-148">You can override this behavior and force **IWiaDevMgr2::SelectDeviceDlg** to display the dialog box by specifying WIA\_SELECT\_DEVICE\_NODEFAULT as the value for the *lFlags* parameter.</span></span> <span data-ttu-id="3d8a8-149">Si plus d’un appareil WIA 2,0 correspond à la spécification, tous les appareils correspondants s’affichent dans la boîte de dialogue **Sélectionner un périphérique** afin que l’utilisateur puisse en choisir un.</span><span class="sxs-lookup"><span data-stu-id="3d8a8-149">If more than one WIA 2.0 device matches the specification, all matching devices are displayed in the **Select Device** dialog box so the user may choose one.</span></span>

<span data-ttu-id="3d8a8-150">Les applications doivent appeler la méthode [IUnknown :: Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) sur les pointeurs d’interface qu’elles reçoivent via le paramètre *ppItemRoot* .</span><span class="sxs-lookup"><span data-stu-id="3d8a8-150">Applications must call the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method on the interface pointers they receive through the *ppItemRoot* parameter.</span></span>

> [!Note]  
> <span data-ttu-id="3d8a8-151">Il est recommandé que les applications rendent la sélection de l’appareil et de l’image disponible via un élément de menu nommé **à partir de scanner** dans le menu **fichier** .</span><span class="sxs-lookup"><span data-stu-id="3d8a8-151">It is recommended that applications make device and image selection available through a menu item named **From scanner** on the **File** menu.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3d8a8-152">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3d8a8-152">Requirements</span></span>



| <span data-ttu-id="3d8a8-153">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3d8a8-153">Requirement</span></span> | <span data-ttu-id="3d8a8-154">Valeur</span><span class="sxs-lookup"><span data-stu-id="3d8a8-154">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3d8a8-155">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3d8a8-155">Minimum supported client</span></span><br/> | <span data-ttu-id="3d8a8-156">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3d8a8-156">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3d8a8-157">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="3d8a8-157">Minimum supported server</span></span><br/> | <span data-ttu-id="3d8a8-158">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="3d8a8-158">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3d8a8-159">En-tête</span><span class="sxs-lookup"><span data-stu-id="3d8a8-159">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d8a8-160"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="3d8a8-160"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="3d8a8-161">MIDL</span><span class="sxs-lookup"><span data-stu-id="3d8a8-161">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3d8a8-162"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="3d8a8-162"><dt>Wia.idl</dt></span></span> </dl> |



 

 
