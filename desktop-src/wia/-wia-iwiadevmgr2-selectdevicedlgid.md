---
description: Affiche une boîte de dialogue qui permet à l’utilisateur de sélectionner un périphérique matériel pour l’acquisition d’images.
ms.assetid: 6baca959-0f97-4a39-88d0-ed34b813c80a
title: 'IWiaDevMgr2 :: SelectDeviceDlgID, méthode (WIA. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWiaDevMgr2.SelectDeviceDlgID
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: bad749eb48e72b362070ea4951d4e9eac380e737
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517549"
---
# <a name="iwiadevmgr2selectdevicedlgid-method"></a><span data-ttu-id="46c60-103">IWiaDevMgr2 :: SelectDeviceDlgID, méthode</span><span class="sxs-lookup"><span data-stu-id="46c60-103">IWiaDevMgr2::SelectDeviceDlgID method</span></span>

<span data-ttu-id="46c60-104">Affiche une boîte de dialogue qui permet à l’utilisateur de sélectionner un périphérique matériel pour l’acquisition d’images.</span><span class="sxs-lookup"><span data-stu-id="46c60-104">Displays a dialog box that enables the user to select a hardware device for image acquisition.</span></span>

## <a name="syntax"></a><span data-ttu-id="46c60-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="46c60-105">Syntax</span></span>


```C++
HRESULT SelectDeviceDlgID(
  [in]          HWND hwndParent,
  [in]          LONG lDeviceType,
  [in]          LONG lFlags,
  [out, retval] BSTR *pbstrDeviceID
);
```



## <a name="parameters"></a><span data-ttu-id="46c60-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="46c60-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46c60-107">*hwndParent* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="46c60-107">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46c60-108">Type : **HWND**</span><span class="sxs-lookup"><span data-stu-id="46c60-108">Type: **HWND**</span></span>

<span data-ttu-id="46c60-109">Spécifie la fenêtre parente de la boîte de dialogue **Sélectionner un périphérique** .</span><span class="sxs-lookup"><span data-stu-id="46c60-109">Specifies the parent window of the **Select Device** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="46c60-110">*lDeviceType* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="46c60-110">*lDeviceType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46c60-111">Type : **long**</span><span class="sxs-lookup"><span data-stu-id="46c60-111">Type: **LONG**</span></span>

<span data-ttu-id="46c60-112">Spécifie le type d’appareil WIA 2,0 à utiliser.</span><span class="sxs-lookup"><span data-stu-id="46c60-112">Specifies which type of WIA 2.0 device to use.</span></span> <span data-ttu-id="46c60-113">Pour obtenir la liste des valeurs possibles, consultez [spécificateurs de type d’appareil WIA](-wia-wia-device-type-specifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="46c60-113">See [WIA Device Type Specifiers](-wia-wia-device-type-specifiers.md) for a list of possible values.</span></span>

</dd> <dt>

<span data-ttu-id="46c60-114">*lFlags* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="46c60-114">*lFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46c60-115">Type : **long**</span><span class="sxs-lookup"><span data-stu-id="46c60-115">Type: **LONG**</span></span>

<span data-ttu-id="46c60-116">Spécifie le comportement de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="46c60-116">Specifies the behavior of the dialog box.</span></span> <span data-ttu-id="46c60-117">La valeur peut être l’une des suivantes.</span><span class="sxs-lookup"><span data-stu-id="46c60-117">The value can be one of the following.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="46c60-118"><span id="0"></span>**entre**</span><span class="sxs-lookup"><span data-stu-id="46c60-118"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="46c60-119">Utiliser le comportement par défaut.</span><span class="sxs-lookup"><span data-stu-id="46c60-119">Use the default behavior.</span></span>

</dd> <dt>

<span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>

<span data-ttu-id="46c60-120"><span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>**WIA- \_ Sélectionner un \_ appareil \_ par défaut**</span><span class="sxs-lookup"><span data-stu-id="46c60-120"><span id="WIA_SELECT_DEVICE_NODEFAULT"></span><span id="wia_select_device_nodefault"></span>**WIA\_SELECT\_DEVICE\_NODEFAULT**</span></span>


</dt> <dd>

<span data-ttu-id="46c60-121">Affiche la boîte de dialogue même s’il n’y a qu’un seul appareil correspondant.</span><span class="sxs-lookup"><span data-stu-id="46c60-121">Display the dialog box even though there is only one matching device.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="46c60-122">*pbstrDeviceID* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="46c60-122">*pbstrDeviceID* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="46c60-123">Type : \**BSTR \** _</span><span class="sxs-lookup"><span data-stu-id="46c60-123">Type: \**BSTR\** _</span></span>

<span data-ttu-id="46c60-124">Pointeur vers une chaîne qui reçoit la chaîne d’identificateur de l’appareil.</span><span class="sxs-lookup"><span data-stu-id="46c60-124">Pointer to a string that receives the identifier string of the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46c60-125">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="46c60-125">Return value</span></span>

<span data-ttu-id="46c60-126">Type : _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="46c60-126">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="46c60-127">Cette méthode peut retourner l’une de ces valeurs.</span><span class="sxs-lookup"><span data-stu-id="46c60-127">This method can return one of these values.</span></span>



| <span data-ttu-id="46c60-128">Code de retour</span><span class="sxs-lookup"><span data-stu-id="46c60-128">Return code</span></span>                                                                                                  | <span data-ttu-id="46c60-129">Description</span><span class="sxs-lookup"><span data-stu-id="46c60-129">Description</span></span>                                                                                            |
|--------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="46c60-130"><dt>**\_OK**</dt></span><span class="sxs-lookup"><span data-stu-id="46c60-130"><dt>**S\_OK**</dt></span></span> </dl>                         | <span data-ttu-id="46c60-131">L’appareil a été sélectionné avec succès.</span><span class="sxs-lookup"><span data-stu-id="46c60-131">Device was successfully selected.</span></span> <br/>                                                          |
| <dl> <span data-ttu-id="46c60-132"><dt>**S \_ false**</dt></span><span class="sxs-lookup"><span data-stu-id="46c60-132"><dt>**S\_FALSE**</dt></span></span> </dl>                      | <span data-ttu-id="46c60-133">L’utilisateur a annulé la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="46c60-133">User canceled the dialog box.</span></span> <br/>                                                              |
| <dl> <span data-ttu-id="46c60-134"><dt>**WIA \_ - \_ aucun \_ appareil \_ disponible**</dt></span><span class="sxs-lookup"><span data-stu-id="46c60-134"><dt>**WIA\_S\_NO\_DEVICE\_AVAILABLE**</dt></span></span> </dl> | <span data-ttu-id="46c60-135">Aucun périphérique matériel WIA 2,0 ne correspond aux spécifications indiquées dans le paramètre *lDeviceType* .</span><span class="sxs-lookup"><span data-stu-id="46c60-135">No WIA 2.0 hardware devices match the specifications given in the *lDeviceType* parameter.</span></span> <br/> |



 

## <a name="remarks"></a><span data-ttu-id="46c60-136">Notes</span><span class="sxs-lookup"><span data-stu-id="46c60-136">Remarks</span></span>

<span data-ttu-id="46c60-137">Cette méthode crée et affiche la boîte de dialogue **Sélectionner un appareil** afin que l’utilisateur puisse sélectionner un appareil WIA 2,0 pour l’acquisition d’images.</span><span class="sxs-lookup"><span data-stu-id="46c60-137">This method creates and displays the **Select Device** dialog box so the user can select a WIA 2.0 device for image acquisition.</span></span> <span data-ttu-id="46c60-138">Si un appareil est sélectionné avec succès, la méthode **IWiaDevMgr2 :: SelectDeviceDlgID** passe sa chaîne d’identificateur à l’application par le biais de son paramètre *pbstrDeviceID* .</span><span class="sxs-lookup"><span data-stu-id="46c60-138">If a device is successfully selected, the **IWiaDevMgr2::SelectDeviceDlgID** method passes its identifier string to the application through its *pbstrDeviceID* parameter.</span></span>

<span data-ttu-id="46c60-139">L’application peut limiter les appareils affichés à l’utilisateur à des types particuliers en spécifiant les types d’appareils via le paramètre *lDeviceType* .</span><span class="sxs-lookup"><span data-stu-id="46c60-139">The application can restrict the devices displayed to the user to particular types by specifying the device types through the *lDeviceType* parameter.</span></span> <span data-ttu-id="46c60-140">Si un seul périphérique répond à la spécification, **IWiaDevMgr2 :: SelectDeviceDlgID** n’affiche pas la boîte de dialogue **Sélectionner un périphérique** .</span><span class="sxs-lookup"><span data-stu-id="46c60-140">If only one device meets the specification, **IWiaDevMgr2::SelectDeviceDlgID** does not display the **Select Device** dialog box.</span></span> <span data-ttu-id="46c60-141">Au lieu de cela, il transmet la chaîne d’identificateur de l’appareil à l’application sans afficher la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="46c60-141">Instead it passes the device's identifier string to the application without displaying the dialog box.</span></span> <span data-ttu-id="46c60-142">Vous pouvez remplacer ce comportement et forcer **IWiaDevMgr2 :: SelectDeviceDlgID** à afficher la boîte de dialogue en passant WIA \_ Select \_ Device \_ NODEFAULT comme valeur du paramètre *lFlags* .</span><span class="sxs-lookup"><span data-stu-id="46c60-142">You can override this behavior and force **IWiaDevMgr2::SelectDeviceDlgID** to display the dialog box by passing WIA\_SELECT\_DEVICE\_NODEFAULT as the value for the *lFlags* parameter.</span></span> <span data-ttu-id="46c60-143">Si plus d’un appareil WIA 2,0 correspond à la spécification, tous les appareils correspondants sont affichés dans la boîte de dialogue SelectDevice pour que l’utilisateur puisse en choisir un.</span><span class="sxs-lookup"><span data-stu-id="46c60-143">If more than one WIA 2.0 device matches the specification, all matching devices are displayed in the SelectDevice dialog box so the user may choose one.</span></span>

> [!Note]  
> <span data-ttu-id="46c60-144">Il est recommandé que les applications rendent la sélection de l’appareil et de l’image disponible via un élément de menu nommé **à partir de scanner** dans le menu **fichier** .</span><span class="sxs-lookup"><span data-stu-id="46c60-144">It is recommended that applications make device and image selection available through a menu item named **From scanner** on the **File** menu.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="46c60-145">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="46c60-145">Requirements</span></span>



| <span data-ttu-id="46c60-146">Condition requise</span><span class="sxs-lookup"><span data-stu-id="46c60-146">Requirement</span></span> | <span data-ttu-id="46c60-147">Valeur</span><span class="sxs-lookup"><span data-stu-id="46c60-147">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="46c60-148">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="46c60-148">Minimum supported client</span></span><br/> | <span data-ttu-id="46c60-149">Applications de \[ Bureau Windows Vista uniquement\]</span><span class="sxs-lookup"><span data-stu-id="46c60-149">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="46c60-150">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="46c60-150">Minimum supported server</span></span><br/> | <span data-ttu-id="46c60-151">Applications de bureau Windows Server 2008 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="46c60-151">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="46c60-152">En-tête</span><span class="sxs-lookup"><span data-stu-id="46c60-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="46c60-153"><dt>WIA. h</dt></span><span class="sxs-lookup"><span data-stu-id="46c60-153"><dt>Wia.h</dt></span></span> </dl>   |
| <span data-ttu-id="46c60-154">MIDL</span><span class="sxs-lookup"><span data-stu-id="46c60-154">IDL</span></span><br/>                      | <dl> <span data-ttu-id="46c60-155"><dt>WIA. idl</dt></span><span class="sxs-lookup"><span data-stu-id="46c60-155"><dt>Wia.idl</dt></span></span> </dl> |



 

 




