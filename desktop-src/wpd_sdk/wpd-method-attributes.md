---
description: 'Pour Windows 7, Windows Mobile Devices prend en charge les attributs suivants pour les méthodes d’un service d’appareil. Ces attributs sont retournés par la méthode IPortableDeviceServiceCapabilities :: GetMethodAttributes.'
ms.assetid: b920e037-7737-4a18-b4f1-5c59e0a857dd
title: Attributs de méthode (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Method
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: fe638bcd0d87af7b16bfb4f202f21cea97908fcd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525435"
---
# <a name="method-attributes"></a><span data-ttu-id="7491a-104">Attributs de méthode</span><span class="sxs-lookup"><span data-stu-id="7491a-104">Method Attributes</span></span>

<span data-ttu-id="7491a-105">Pour Windows 7, Windows Mobile Devices prend en charge les attributs suivants pour les méthodes d’un service d’appareil.</span><span class="sxs-lookup"><span data-stu-id="7491a-105">For Windows 7, Windows Portable Devices supports the following attributes for methods of a device service.</span></span> <span data-ttu-id="7491a-106">Ces attributs sont retournés par la méthode [**IPortableDeviceServiceCapabilities :: GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) .</span><span class="sxs-lookup"><span data-stu-id="7491a-106">These attributes are returned by the [**IPortableDeviceServiceCapabilities::GetMethodAttributes**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicecapabilities-getmethodattributes) method.</span></span>




| <span data-ttu-id="7491a-107">Attribut</span><span class="sxs-lookup"><span data-stu-id="7491a-107">Attribute</span></span>                                      | <span data-ttu-id="7491a-108">VarType</span><span class="sxs-lookup"><span data-stu-id="7491a-108">VarType</span></span>         | <span data-ttu-id="7491a-109">Description</span><span class="sxs-lookup"><span data-stu-id="7491a-109">Description</span></span>                                                                                                               |
|------------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7491a-110">**\_ \_ accès aux attributs de la méthode wpd \_**</span><span class="sxs-lookup"><span data-stu-id="7491a-110">**WPD\_METHOD\_ATTRIBUTE\_ACCESS**</span></span>             | <span data-ttu-id="7491a-111">**\_CLSID VT**</span><span class="sxs-lookup"><span data-stu-id="7491a-111">**VT\_CLSID**</span></span>   | <span data-ttu-id="7491a-112">Accès à la méthode requis.</span><span class="sxs-lookup"><span data-stu-id="7491a-112">The required method access.</span></span>                                                                                               |
| <span data-ttu-id="7491a-113">**\_ \_ \_ format associé à l’attribut de méthode wpd \_**</span><span class="sxs-lookup"><span data-stu-id="7491a-113">**WPD\_METHOD\_ATTRIBUTE\_ASSOCIATED\_FORMAT**</span></span> | <span data-ttu-id="7491a-114">**\_CLSID VT**</span><span class="sxs-lookup"><span data-stu-id="7491a-114">**VT\_CLSID**</span></span>   | <span data-ttu-id="7491a-115">Format associé à la méthode, ou **GUID \_ null** s’il n’existe aucun format associé.</span><span class="sxs-lookup"><span data-stu-id="7491a-115">The format associated with the method, or **GUID\_NULL** if there is no associated format.</span></span>                                |
| <span data-ttu-id="7491a-116">**nom de l' \_ attribut de méthode wpd \_ \_**</span><span class="sxs-lookup"><span data-stu-id="7491a-116">**WPD\_METHOD\_ATTRIBUTE\_NAME**</span></span>               | <span data-ttu-id="7491a-117">**\_LPWStr VT**</span><span class="sxs-lookup"><span data-stu-id="7491a-117">**VT\_LPWSTR**</span></span>  | <span data-ttu-id="7491a-118">Chaîne qui spécifie le nom convivial du script de la méthode.</span><span class="sxs-lookup"><span data-stu-id="7491a-118">A string that specifies the script-friendly name of the method.</span></span> <span data-ttu-id="7491a-119">Les caractères valides sont alphanumériques \[ a-zA-z0-9 \] et' \_ '.</span><span class="sxs-lookup"><span data-stu-id="7491a-119">Valid characters are alphanumeric \[a-zA-Z0-9\] and '\_'.</span></span> |
| <span data-ttu-id="7491a-120">**\_paramètres d' \_ attribut de méthode wpd \_**</span><span class="sxs-lookup"><span data-stu-id="7491a-120">**WPD\_METHOD\_ATTRIBUTE\_PARAMETERS**</span></span>         | <span data-ttu-id="7491a-121">**VT \_ inconnu**</span><span class="sxs-lookup"><span data-stu-id="7491a-121">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="7491a-122">Interface [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) qui contient les paramètres de la méthode.</span><span class="sxs-lookup"><span data-stu-id="7491a-122">An [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) interface that contains the method parameters.</span></span>    |



 

## <a name="requirements"></a><span data-ttu-id="7491a-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7491a-123">Requirements</span></span>



| <span data-ttu-id="7491a-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7491a-124">Requirement</span></span> | <span data-ttu-id="7491a-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="7491a-125">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="7491a-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="7491a-126">Header</span></span><br/> | <dl> <span data-ttu-id="7491a-127"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="7491a-127"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7491a-128">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7491a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7491a-129">**Propriétés et attributs**</span><span class="sxs-lookup"><span data-stu-id="7491a-129">**Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




