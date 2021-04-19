---
description: La méthode GetPropById de l’objet DeviceInfo utilise l’ID d’une propriété d’appareil pour retourner sa valeur.
ms.assetid: 9c68e6af-446c-4750-89e6-70862b23b296
title: Méthode DeviceInfo. GetPropById
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DeviceInfo.GetPropById
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: adbc8b6a29f97066c8dc5b2e45b7ddc5834f2b60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527904"
---
# <a name="deviceinfogetpropbyid-method"></a><span data-ttu-id="e2085-103">Méthode DeviceInfo. GetPropById</span><span class="sxs-lookup"><span data-stu-id="e2085-103">DeviceInfo.GetPropById method</span></span>

<span data-ttu-id="e2085-104">La méthode **GetPropById** de l’objet [**DEVICEINFO**](-wia-deviceinfo.md) utilise l’ID d’une propriété d’appareil pour retourner sa valeur.</span><span class="sxs-lookup"><span data-stu-id="e2085-104">The **GetPropById** method of the [**DeviceInfo**](-wia-deviceinfo.md) object uses a device property's ID to return its value.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2085-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e2085-105">Syntax</span></span>


```JScript
retVal = DeviceInfo.GetPropById(
  Id
)
```



## <a name="parameters"></a><span data-ttu-id="e2085-106">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e2085-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2085-107">*ID* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="e2085-107">*Id* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2085-108">Type : **[WiaDeviceInfoPropertyId](-wia-wiadeviceinfopropertyid.md)**</span><span class="sxs-lookup"><span data-stu-id="e2085-108">Type: **[WiaDeviceInfoPropertyId](-wia-wiadeviceinfopropertyid.md)**</span></span>

<span data-ttu-id="e2085-109">Spécifie l’ID de la propriété.</span><span class="sxs-lookup"><span data-stu-id="e2085-109">Specifies the ID of the property.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2085-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e2085-110">Return value</span></span>

<span data-ttu-id="e2085-111">Type : **variante**</span><span class="sxs-lookup"><span data-stu-id="e2085-111">Type: **VARIANT**</span></span>

<span data-ttu-id="e2085-112">Cette méthode retourne la valeur de la propriété spécifiée par *ID*.</span><span class="sxs-lookup"><span data-stu-id="e2085-112">This method returns the value of the property specified by *Id*.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2085-113">Notes</span><span class="sxs-lookup"><span data-stu-id="e2085-113">Remarks</span></span>

<span data-ttu-id="e2085-114">Utilisez cette méthode pour rechercher la valeur d’une propriété d’appareil à partir de son ID.</span><span class="sxs-lookup"><span data-stu-id="e2085-114">Use this method to find the value of a device property from its ID.</span></span> <span data-ttu-id="e2085-115">Pour obtenir la liste des ID de propriété, consultez [définitions de constante de propriété WIA](-wia-wia-property-constant-definitions.md).</span><span class="sxs-lookup"><span data-stu-id="e2085-115">For a list of property IDs, see [WIA Property Constant Definitions](-wia-wia-property-constant-definitions.md).</span></span> <span data-ttu-id="e2085-116">Pour plus d’informations sur les propriétés WIA (Windows Image Acquisition) elles-mêmes, consultez [constantes de propriété WIA](-wia-wia-property-constants.md).</span><span class="sxs-lookup"><span data-stu-id="e2085-116">For information about Windows Image Acquisition (WIA) properties themselves, see [WIA Property Constants](-wia-wia-property-constants.md).</span></span>

<span data-ttu-id="e2085-117">Pour les applications Microsoft Visual Basic, ajoutez une référence à « Bibliothèque de types Windows Image Acquisition 1,01 ».</span><span class="sxs-lookup"><span data-stu-id="e2085-117">For Microsoft Visual Basic applications, add a reference to "Windows Image Acquisition 1.01 Type Library".</span></span> <span data-ttu-id="e2085-118">Les constantes suivantes définies dans ce fichier sont valides pour cette méthode :</span><span class="sxs-lookup"><span data-stu-id="e2085-118">This following constants defined in that file are valid for this method:</span></span>

``` syntax
const DeviceID = 2
const Manufacturer = 3
const Description = 4
const Type = 5
const Port = 6
const Name = 7
const Server = 8
const RemoteDevID = 9
const UIClassID = 10
```

## <a name="examples"></a><span data-ttu-id="e2085-119">Exemples</span><span class="sxs-lookup"><span data-stu-id="e2085-119">Examples</span></span>

<span data-ttu-id="e2085-120">L’exemple suivant illustre l’utilisation de la méthode **GetPropById** pour récupérer une valeur de propriété.</span><span class="sxs-lookup"><span data-stu-id="e2085-120">The following example demonstrates the use of the **GetPropById** method to retrieve a property value.</span></span>


```JScript
<SCRIPT LANGUAGE="VBScript">
const WIA_DIP_DEV_TYPE = 5
Dim objWia
Dim objDeviceInfoCollection
Dim objDeviceInfo
Dim PropValue
 
Set objWIA = CreateObject("Wia.Script")
 
Set objDeviceInfoCollection = objWia.Devices
 
For Each objDeviceInfo In objDeviceInfoCollection
    PropValue = objDeviceInfo.GetPropById(WIA_DIP_DEV_TYPE)
Next
</SCRIPT>
```



## <a name="requirements"></a><span data-ttu-id="e2085-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e2085-121">Requirements</span></span>



| <span data-ttu-id="e2085-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e2085-122">Requirement</span></span> | <span data-ttu-id="e2085-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="e2085-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2085-124">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e2085-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e2085-125">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e2085-125">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="e2085-126">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="e2085-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e2085-127">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="e2085-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="e2085-128">DLL</span><span class="sxs-lookup"><span data-stu-id="e2085-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e2085-129"><dt>Wiascr.dll (version 4,90 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="e2085-129"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |



 

 




