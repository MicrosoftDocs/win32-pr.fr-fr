---
description: Le \_ type d’énumération Options de suppression d’objet décrit les \_ options prises en charge par un appareil lors de la suppression d’un objet.
ms.assetid: d0e46e77-d333-498f-b2f5-26be1461a116
title: Énumération DELETE_OBJECT_OPTIONS (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DELETE_OBJECT_OPTIONS
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 3a1fb8ce9a443c7cc93019804094dca84a635c40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543197"
---
# <a name="delete_object_options-enumeration"></a><span data-ttu-id="d4329-103">SUPPRIMER \_ l' \_ énumération des options d’objet</span><span class="sxs-lookup"><span data-stu-id="d4329-103">DELETE\_OBJECT\_OPTIONS enumeration</span></span>

<span data-ttu-id="d4329-104">Le type d’énumération **\_ \_ options de suppression d’objet** décrit les options prises en charge par un appareil lors de la suppression d’un objet.</span><span class="sxs-lookup"><span data-stu-id="d4329-104">The **DELETE\_OBJECT\_OPTIONS** enumeration type describes options that are supported by a device when deleting an object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4329-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d4329-105">Syntax</span></span>


```C++
typedef enum DELETE_OBJECT_OPTIONS { 
  PORTABLE_DEVICE_DELETE_NO_RECURSION    = 0,
  PORTABLE_DEVICE_DELETE_WITH_RECURSION  = 1
} ;
```



## <a name="constants"></a><span data-ttu-id="d4329-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="d4329-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d4329-107"><span id="PORTABLE_DEVICE_DELETE_NO_RECURSION"></span><span id="portable_device_delete_no_recursion"></span>**suppression de l' \_ appareil mobile \_ \_ sans \_ récurrence**</span><span class="sxs-lookup"><span data-stu-id="d4329-107"><span id="PORTABLE_DEVICE_DELETE_NO_RECURSION"></span><span id="portable_device_delete_no_recursion"></span>**PORTABLE\_DEVICE\_DELETE\_NO\_RECURSION**</span></span>
</dt> <dd>

<span data-ttu-id="d4329-108">Supprimer l’objet uniquement et échouer s’il a des enfants.</span><span class="sxs-lookup"><span data-stu-id="d4329-108">Delete the object only and fail if it has children.</span></span>

</dd> <dt>

<span data-ttu-id="d4329-109"><span id="PORTABLE_DEVICE_DELETE_WITH_RECURSION"></span><span id="portable_device_delete_with_recursion"></span>**\_Suppression de l’appareil portable \_ \_ avec \_ récurrence**</span><span class="sxs-lookup"><span data-stu-id="d4329-109"><span id="PORTABLE_DEVICE_DELETE_WITH_RECURSION"></span><span id="portable_device_delete_with_recursion"></span>**PORTABLE\_DEVICE\_DELETE\_WITH\_RECURSION**</span></span>
</dt> <dd>

<span data-ttu-id="d4329-110">Supprimez l’objet et tous ses enfants.</span><span class="sxs-lookup"><span data-stu-id="d4329-110">Delete the object and all its children.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d4329-111">Notes</span><span class="sxs-lookup"><span data-stu-id="d4329-111">Remarks</span></span>

<span data-ttu-id="d4329-112">L’application peut récupérer les options de suppression que l’appareil prend en charge en appelant [**IPortableDeviceCapabilities :: GetCommandOptions**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getcommandoptions) pour la commande de **Suppression d' \_ \_ \_ \_ \_ objets de commande wpd** .</span><span class="sxs-lookup"><span data-stu-id="d4329-112">The application can retrieve the deletion options that the device supports by calling [**IPortableDeviceCapabilities::GetCommandOptions**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecapabilities-getcommandoptions) for the **WPD\_COMMAND\_OBJECT\_MANAGEMENT\_DELETE\_OBJECTS** command.</span></span> <span data-ttu-id="d4329-113">Il doit examiner la valeur de l’option **\_ \_ \_ \_ \_ \_ prise en charge de la gestion récursive des objets d’option wpd** retournée par cette méthode dans un objet [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md) .</span><span class="sxs-lookup"><span data-stu-id="d4329-113">It should examine the **WPD\_OPTION\_OBJECT\_MANAGEMENT\_RECURSIVE\_DELETE\_SUPPORTED** option value that this method returns in an [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md) object.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4329-114">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d4329-114">Requirements</span></span>



| <span data-ttu-id="d4329-115">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d4329-115">Requirement</span></span> | <span data-ttu-id="d4329-116">Valeur</span><span class="sxs-lookup"><span data-stu-id="d4329-116">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4329-117">En-tête</span><span class="sxs-lookup"><span data-stu-id="d4329-117">Header</span></span><br/> | <dl> <span data-ttu-id="d4329-118"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="d4329-118"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d4329-119">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d4329-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4329-120">**Structures et types énumération**</span><span class="sxs-lookup"><span data-stu-id="d4329-120">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




