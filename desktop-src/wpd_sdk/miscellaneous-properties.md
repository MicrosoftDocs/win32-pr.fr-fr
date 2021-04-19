---
description: Appareils mobiles Windows prend en charge les propriétés diverses suivantes.
ms.assetid: 0f2a5684-a94f-4a51-8f72-527204e4ebfa
title: Propriétés diverses (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Miscellaneous
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 6bc5f90bb04c2ee0d018d03ee07b6cd7436e6593
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106545400"
---
# <a name="miscellaneous-properties"></a><span data-ttu-id="7d5c1-103">Propriétés diverses</span><span class="sxs-lookup"><span data-stu-id="7d5c1-103">Miscellaneous Properties</span></span>

<span data-ttu-id="7d5c1-104">Appareils mobiles Windows prend en charge les propriétés diverses suivantes.</span><span class="sxs-lookup"><span data-stu-id="7d5c1-104">Windows Portable Devices supports the following miscellaneous properties.</span></span>



| <span data-ttu-id="7d5c1-105">Propriété</span><span class="sxs-lookup"><span data-stu-id="7d5c1-105">Property</span></span>                                       | <span data-ttu-id="7d5c1-106">VarType</span><span class="sxs-lookup"><span data-stu-id="7d5c1-106">VarType</span></span>         | <span data-ttu-id="7d5c1-107">Description</span><span class="sxs-lookup"><span data-stu-id="7d5c1-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d5c1-108">**l' \_ option de l’API WPD \_ utilise un \_ \_ \_ flux de données clair \_**</span><span class="sxs-lookup"><span data-stu-id="7d5c1-108">**WPD\_API\_OPTION\_USE\_CLEAR\_DATA\_STREAM**</span></span> | <span data-ttu-id="7d5c1-109">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="7d5c1-109">**VT\_BOOL**</span></span>    | <span data-ttu-id="7d5c1-110">Valeur booléenne qui spécifie si le flux de données créé pour le transfert de données est clair, c’est-à-dire que la DRM n’est pas impliquée. Les clients peuvent définir cette option en l’ajoutant aux propriétés d’objet passées à [**IPortableDeviceContent :: CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata).</span><span class="sxs-lookup"><span data-stu-id="7d5c1-110">A Boolean value that specifies whether the data stream created for data transfer will be clear, that is, DRM is not involved.Clients can set this option by adding it to the object properties passed to [**IPortableDeviceContent::CreateObjectWithPropertiesAndData**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata).</span></span><br/>                                                                                                                                                   |
| <span data-ttu-id="7d5c1-111">**\_version du service wpd \_**</span><span class="sxs-lookup"><span data-stu-id="7d5c1-111">**WPD\_SERVICE\_VERSION**</span></span>                      | <span data-ttu-id="7d5c1-112">**\_LPWStr VT**</span><span class="sxs-lookup"><span data-stu-id="7d5c1-112">**VT\_LPWSTR**</span></span>  | <span data-ttu-id="7d5c1-113">Chaîne qui spécifie la version d’implémentation d’un service d’appareil donné.</span><span class="sxs-lookup"><span data-stu-id="7d5c1-113">A string that specifies the implementation version of a given device service.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="7d5c1-114">**\_types de contenu de dossier wpd \_ \_ \_ autorisés**</span><span class="sxs-lookup"><span data-stu-id="7d5c1-114">**WPD\_FOLDER\_CONTENT\_TYPES\_ALLOWED**</span></span>       | <span data-ttu-id="7d5c1-115">**VT \_ inconnu**</span><span class="sxs-lookup"><span data-stu-id="7d5c1-115">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="7d5c1-116">Valeur qui spécifie les types d’objets qui peuvent être des enfants directs de ce dossier.</span><span class="sxs-lookup"><span data-stu-id="7d5c1-116">A value that specifies the object types that can be direct children of this folder.</span></span> <span data-ttu-id="7d5c1-117">Les dossiers enfants peuvent avoir des fonctionnalités différentes. Cette propriété est un [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) contenant des \_ valeurs de CLSID VT qui spécifient des types d’objet autorisés.</span><span class="sxs-lookup"><span data-stu-id="7d5c1-117">Child folders can have different capabilities.This property is an [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) holding VT\_CLSID values that specify permitted object types.</span></span><br/> <span data-ttu-id="7d5c1-118">Pour obtenir la liste des types d’objets définis par les appareils mobiles Windows, consultez [Configuration requise pour les objets](requirements-for-objects.md).</span><span class="sxs-lookup"><span data-stu-id="7d5c1-118">For a list of object types defined by Windows Portable Devices, see [Requirements for Objects](requirements-for-objects.md).</span></span><br/>                                         |
| <span data-ttu-id="7d5c1-119">**\_catégorie d' \_ objet \_ fonctionnel wpd**</span><span class="sxs-lookup"><span data-stu-id="7d5c1-119">**WPD\_FUNCTIONAL\_OBJECT\_CATEGORY**</span></span>          | <span data-ttu-id="7d5c1-120">**\_CLSID VT**</span><span class="sxs-lookup"><span data-stu-id="7d5c1-120">**VT\_CLSID**</span></span>   | <span data-ttu-id="7d5c1-121">Valeur qui spécifie la catégorie fonctionnelle de l’objet.</span><span class="sxs-lookup"><span data-stu-id="7d5c1-121">A value that specifies the object's functional category.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span data-ttu-id="7d5c1-122">**\_profils d' \_ informations de rendu wpd \_**</span><span class="sxs-lookup"><span data-stu-id="7d5c1-122">**WPD\_RENDERING\_INFORMATION\_PROFILES**</span></span>      | <span data-ttu-id="7d5c1-123">**VT \_ inconnu**</span><span class="sxs-lookup"><span data-stu-id="7d5c1-123">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="7d5c1-124">Un [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md) qui contient plusieurs interfaces [**IPortableDeviceValues**](iportabledevicevalues.md) , chacune contenant les paramètres de propriété d’un profil que l’objet prend en charge.</span><span class="sxs-lookup"><span data-stu-id="7d5c1-124">An [**IPortableDeviceValuesCollection**](iportabledevicevaluescollection.md) that holds multiple [**IPortableDeviceValues**](iportabledevicevalues.md) interfaces, each of which contains the property settings for a profile that the object supports.</span></span>                                                                                                                                                                                                                                            |
| <span data-ttu-id="7d5c1-125">**\_ \_ \_ \_ \_ nom complet de l’emplacement de l’indicateur d’objet wpd**</span><span class="sxs-lookup"><span data-stu-id="7d5c1-125">**WPD\_OBJECT\_HINT\_LOCATION\_DISPLAY\_NAME**</span></span> | <span data-ttu-id="7d5c1-126">**\_LPWStr VT**</span><span class="sxs-lookup"><span data-stu-id="7d5c1-126">**VT\_LPWSTR**</span></span>  | <span data-ttu-id="7d5c1-127">Si un objet est un emplacement d’indication, cette propriété indique le nom spécifique à l’indicateur à afficher à l’utilisateur au lieu du nom de l’objet. Les pilotes peuvent spécifier des indications d’emplacement pour différents types d’objets.</span><span class="sxs-lookup"><span data-stu-id="7d5c1-127">If an object is a hint location, this property indicates the hint-specific name to display to the user instead of the object name.Drivers can specify location hints for various object types.</span></span> <span data-ttu-id="7d5c1-128">Il s’agit d’emplacements de stockage préférés pour les dossiers qui contiennent un type d’objet particulier.</span><span class="sxs-lookup"><span data-stu-id="7d5c1-128">These are preferred storage locations for folders that hold a particular object type.</span></span> <span data-ttu-id="7d5c1-129">Un équivalent serait le dossier Mes images pour les fichiers image dans Windows.</span><span class="sxs-lookup"><span data-stu-id="7d5c1-129">An equivalent would be the My Pictures folder for image files in Windows.</span></span> <span data-ttu-id="7d5c1-130">Si cette propriété n’existe pas, le nom de l' [ \_ \_ objet wpd](object-properties.md) est généralement utilisé à la place.</span><span class="sxs-lookup"><span data-stu-id="7d5c1-130">If this property does not exist, typically the [WPD\_OBJECT\_NAME](object-properties.md) is used instead.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="7d5c1-131">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7d5c1-131">Requirements</span></span>



| <span data-ttu-id="7d5c1-132">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7d5c1-132">Requirement</span></span> | <span data-ttu-id="7d5c1-133">Valeur</span><span class="sxs-lookup"><span data-stu-id="7d5c1-133">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d5c1-134">En-tête</span><span class="sxs-lookup"><span data-stu-id="7d5c1-134">Header</span></span><br/> | <dl> <span data-ttu-id="7d5c1-135"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d5c1-135"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d5c1-136">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7d5c1-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d5c1-137">**Propriétés et attributs WPD**</span><span class="sxs-lookup"><span data-stu-id="7d5c1-137">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




