---
description: Appareils mobiles Windows prend en charge les propriétés de données de la section suivante.
ms.assetid: 8760d963-fc07-4b54-aa24-5725f4b95ed2
title: Propriétés de l’attribut section (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Section
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 383e2e50aa5d2a922ad50609e316b3dc9905cc38
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528988"
---
# <a name="section-attribute-properties"></a><span data-ttu-id="9fa55-103">Propriétés de l’attribut de section</span><span class="sxs-lookup"><span data-stu-id="9fa55-103">Section Attribute Properties</span></span>

<span data-ttu-id="9fa55-104">Appareils mobiles Windows prend en charge les propriétés de données de la section suivante.</span><span class="sxs-lookup"><span data-stu-id="9fa55-104">Windows Portable Devices supports the following section data properties.</span></span>



| <span data-ttu-id="9fa55-105">Propriété</span><span class="sxs-lookup"><span data-stu-id="9fa55-105">Property</span></span>                                             | <span data-ttu-id="9fa55-106">VarType</span><span class="sxs-lookup"><span data-stu-id="9fa55-106">VarType</span></span>         | <span data-ttu-id="9fa55-107">Description</span><span class="sxs-lookup"><span data-stu-id="9fa55-107">Description</span></span>                                                                                                                                                                                                                                                                                                                                 |
|------------------------------------------------------|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fa55-108">**longueur des données de la \_ section wpd \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9fa55-108">**WPD\_SECTION\_DATA\_LENGTH**</span></span>                       | <span data-ttu-id="9fa55-109">**\_UI8 VT**</span><span class="sxs-lookup"><span data-stu-id="9fa55-109">**VT\_UI8**</span></span>     | <span data-ttu-id="9fa55-110">Spécifie la longueur de l’objet référencé.</span><span class="sxs-lookup"><span data-stu-id="9fa55-110">Specifies the length of the referenced object.</span></span>                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="9fa55-111">**décalage des données de la \_ section wpd \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9fa55-111">**WPD\_SECTION\_DATA\_OFFSET**</span></span>                       | <span data-ttu-id="9fa55-112">**\_UI8 VT**</span><span class="sxs-lookup"><span data-stu-id="9fa55-112">**VT\_UI8**</span></span>     | <span data-ttu-id="9fa55-113">Spécifie l’offset de base zéro des données pour l’objet référencé.</span><span class="sxs-lookup"><span data-stu-id="9fa55-113">Specifies the zero-based offset of the data for the referenced object.</span></span>                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="9fa55-114">**\_ressource d' \_ objet de référence des données \_ \_ de la section wpd \_**</span><span class="sxs-lookup"><span data-stu-id="9fa55-114">**WPD\_SECTION\_DATA\_REFERENCED\_OBJECT\_RESOURCE**</span></span> | <span data-ttu-id="9fa55-115">**VT \_ inconnu**</span><span class="sxs-lookup"><span data-stu-id="9fa55-115">**VT\_UNKNOWN**</span></span> | <span data-ttu-id="9fa55-116">[**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) contenant une valeur unique qui spécifie la clé d’une ressource donnée. Cette ressource est l’objet référencé par la \_ section offset de données de la section wpd \_ et la \_ longueur des données de la \_ section wpd \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="9fa55-116">An [**IPortableDeviceKeyCollection**](iportabledevicekeycollection.md) containing a single value that specifies the key for a given resource.This resource is the object referenced by WPD\_SECTION\_DATA\_OFFSET and WPD\_SECTION\_DATA\_LENGTH.</span></span><br/> <span data-ttu-id="9fa55-117">Si cette propriété n’existe pas, \_ la \_ valeur par défaut de la ressource wpd est supposée.</span><span class="sxs-lookup"><span data-stu-id="9fa55-117">If this property doesn't exist, WPD\_RESOURCE\_DEFAULT is assumed.</span></span><br/> |
| <span data-ttu-id="9fa55-118">**unités de données de la \_ section wpd \_ \_**</span><span class="sxs-lookup"><span data-stu-id="9fa55-118">**WPD\_SECTION\_DATA\_UNITS**</span></span>                        | <span data-ttu-id="9fa55-119">**VT \_ UI4**</span><span class="sxs-lookup"><span data-stu-id="9fa55-119">**VT\_UI4**</span></span>     | <span data-ttu-id="9fa55-120">Spécifie les unités utilisées pour ce décalage, par exemple, les octets, les millisecondes, etc. Les valeurs possibles de cette propriété sont définies dans l’énumération des valeurs d’unités de données de la **\_ section \_ \_ \_ wpd** dans le fichier PortableDevice. h.</span><span class="sxs-lookup"><span data-stu-id="9fa55-120">Specifies the units used for this offset, for example, bytes, milliseconds, and so on.The possible values for this property are defined in the **WPD\_SECTION\_DATA\_UNITS\_VALUES** enumeration in the file PortableDevice.h.</span></span><br/> <span data-ttu-id="9fa55-121">Si aucune unité n’est spécifiée, les octets sont supposés.</span><span class="sxs-lookup"><span data-stu-id="9fa55-121">If no units are specified, bytes are assumed.</span></span><br/>                                          |



 

## <a name="requirements"></a><span data-ttu-id="9fa55-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="9fa55-122">Requirements</span></span>



| <span data-ttu-id="9fa55-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="9fa55-123">Requirement</span></span> | <span data-ttu-id="9fa55-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="9fa55-124">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="9fa55-125">En-tête</span><span class="sxs-lookup"><span data-stu-id="9fa55-125">Header</span></span><br/> | <dl> <span data-ttu-id="9fa55-126"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="9fa55-126"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9fa55-127">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="9fa55-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9fa55-128">**Propriétés et attributs WPD**</span><span class="sxs-lookup"><span data-stu-id="9fa55-128">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




