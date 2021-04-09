---
description: La méthode GetItemsFromUI de l’objet Item affiche une boîte de dialogue qui permet à un utilisateur de sélectionner des images et de l’audio à transférer à partir d’un appareil.
ms.assetid: 0ee9a248-20ed-4e1f-a8ce-615c4a6a2bce
title: Item. GetItemsFromUI, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Item.GetItemsFromUI
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 25bb24fd2b4c6b8d3d7f8cc08c23a42257399a14
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113903"
---
# <a name="itemgetitemsfromui-method"></a><span data-ttu-id="8b225-103">Item. GetItemsFromUI, méthode</span><span class="sxs-lookup"><span data-stu-id="8b225-103">Item.GetItemsFromUI method</span></span>

<span data-ttu-id="8b225-104">La méthode **GetItemsFromUI** de l’objet [**Item**](-wia-item.md) affiche une boîte de dialogue qui permet à un utilisateur de sélectionner des images et de l’audio à transférer à partir d’un appareil.</span><span class="sxs-lookup"><span data-stu-id="8b225-104">The **GetItemsFromUI** method of the [**Item**](-wia-item.md) object displays a dialog box that allows a user to select images and audio to transfer from a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b225-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8b225-105">Syntax</span></span>


```JScript
retVal = Item.GetItemsFromUI(
  Flags = 0,
  Intent = 0
)
```



## <a name="parameters"></a><span data-ttu-id="8b225-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="8b225-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b225-107">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="8b225-107">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b225-108">Type : **[ **WiaFlag**](-wia-wiaflag.md)**</span><span class="sxs-lookup"><span data-stu-id="8b225-108">Type: **[**WiaFlag**](-wia-wiaflag.md)**</span></span>

<dt>



 <span data-ttu-id="8b225-109"> (0)</span><span class="sxs-lookup"><span data-stu-id="8b225-109">(0)</span></span>


</dt> <dd>

<span data-ttu-id="8b225-110">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="8b225-110">Default.</span></span> <span data-ttu-id="8b225-111">\[dans \] spécifie le comportement de la boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="8b225-111">\[in\] Specifies dialog box behavior.</span></span> <span data-ttu-id="8b225-112">Les valeurs valides pour ce paramètre sont les mêmes que pour le paramètre *lFlags* de la méthode [**DeviceDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-devicedlg) .</span><span class="sxs-lookup"><span data-stu-id="8b225-112">The valid values for this parameter are the same as for the *lFlags* parameter of the [**DeviceDlg**](/windows/desktop/api/wia_xp/nf-wia_xp-iwiaitem-devicedlg) method.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="8b225-113">*Intention* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="8b225-113">*Intent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b225-114">Type : **WiaIntent**</span><span class="sxs-lookup"><span data-stu-id="8b225-114">Type: **WiaIntent**</span></span>

<dt>



 <span data-ttu-id="8b225-115"> (0)</span><span class="sxs-lookup"><span data-stu-id="8b225-115">(0)</span></span>


</dt> <dd>

<span data-ttu-id="8b225-116">Par défaut.</span><span class="sxs-lookup"><span data-stu-id="8b225-116">Default.</span></span> <span data-ttu-id="8b225-117">\[dans \] spécifie le type de données que l’image doit représenter.</span><span class="sxs-lookup"><span data-stu-id="8b225-117">\[in\] Specifies what type of data the image is intended to represent.</span></span> <span data-ttu-id="8b225-118">Pour obtenir la liste des valeurs d’intention d’image, consultez [**constantes d’intention d’image**](-wia-imageintentconstants.md).</span><span class="sxs-lookup"><span data-stu-id="8b225-118">For a list of image intent values, see [**Image Intent Constants**](-wia-imageintentconstants.md).</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b225-119">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="8b225-119">Return value</span></span>

<span data-ttu-id="8b225-120">Type : **ICollection**</span><span class="sxs-lookup"><span data-stu-id="8b225-120">Type: **ICollection**</span></span>

<span data-ttu-id="8b225-121">Cette méthode retourne une collection d’objets [**Item**](-wia-item.md) qui représentent les éléments sélectionnés par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8b225-121">This method returns a collection of [**Item**](-wia-item.md) objects that represent the items selected by the user.</span></span> <span data-ttu-id="8b225-122">Si aucun élément n’est sélectionné, la collection est vide.</span><span class="sxs-lookup"><span data-stu-id="8b225-122">If no items are selected, the collection is empty.</span></span>

## <a name="remarks"></a><span data-ttu-id="8b225-123">Notes</span><span class="sxs-lookup"><span data-stu-id="8b225-123">Remarks</span></span>

<span data-ttu-id="8b225-124">Pour les applications Microsoft Visual Basic, ajoutez une référence à « Bibliothèque de types Windows Image Acquisition 1,01 ».</span><span class="sxs-lookup"><span data-stu-id="8b225-124">For Microsoft Visual Basic applications, add a reference to "Windows Image Acquisition 1.01 Type Library".</span></span>

<span data-ttu-id="8b225-125">Cette méthode s’applique uniquement aux périphériques (éléments racine).</span><span class="sxs-lookup"><span data-stu-id="8b225-125">This method applies only to devices (root items).</span></span> <span data-ttu-id="8b225-126">La méthode retourne une collection d’objets [**Item**](-wia-item.md) qui représentent les images ou les clips audio sélectionnés par l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="8b225-126">The method returns a collection of [**Item**](-wia-item.md) objects that represent the images or audio clips selected by the user.</span></span>

<span data-ttu-id="8b225-127">Si aucun élément n’est sélectionné par l’utilisateur, la méthode retourne une collection vide.</span><span class="sxs-lookup"><span data-stu-id="8b225-127">If no items are selected by the user, the method returns an empty collection.</span></span>

## <a name="examples"></a><span data-ttu-id="8b225-128">Exemples</span><span class="sxs-lookup"><span data-stu-id="8b225-128">Examples</span></span>

<span data-ttu-id="8b225-129">L’exemple suivant illustre l’utilisation de la méthode **GetItemsFromUI** pour permettre à un utilisateur de sélectionner des images à partir d’une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="8b225-129">The following example demonstrates the use of the **GetItemsFromUI** method to allow a user to select images from a dialog box.</span></span>


```JScript
<SCRIPT LANGUAGE="VBScript">
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim objRootItem
Dim objSelectedItems
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    Set objRootItem = objWia.Create(objDeviceInfo)
    Set objSelectedItems = objRootItem.GetItemsFromUI(0, 0)
    ' Do something with selected items.
Next
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="8b225-130">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8b225-130">Requirements</span></span>



| <span data-ttu-id="8b225-131">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8b225-131">Requirement</span></span> | <span data-ttu-id="8b225-132">Valeur</span><span class="sxs-lookup"><span data-stu-id="8b225-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b225-133">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8b225-133">Minimum supported client</span></span><br/> | <span data-ttu-id="8b225-134">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8b225-134">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="8b225-135">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="8b225-135">Minimum supported server</span></span><br/> | <span data-ttu-id="8b225-136">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="8b225-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="8b225-137">DLL</span><span class="sxs-lookup"><span data-stu-id="8b225-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b225-138"><dt>Wiascr.dll (version 4,90 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="8b225-138"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




