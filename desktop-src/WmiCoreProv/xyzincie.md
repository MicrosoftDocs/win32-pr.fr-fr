---
description: Contient les coordonnées de l’affichage dans l’espace de couleurs CIE (International Commission on illumination) XYZ.
ms.assetid: e44e8a5f-005d-4d58-84e3-135d4e396086
title: XYZinCIE, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- XYZinCIE
- XYZinCIE.X
- XYZinCIE.Y
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: ba7f781a83f3e6ba5aa4683003386a0478d65088
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521352"
---
# <a name="xyzincie-class"></a><span data-ttu-id="f4ad2-103">XYZinCIE, classe</span><span class="sxs-lookup"><span data-stu-id="f4ad2-103">XYZinCIE class</span></span>

<span data-ttu-id="f4ad2-104">La classe WMI **XYZinCIE** contient les coordonnées de l’affichage dans l’espace de couleurs Cie (International Commission on illumination) XYZ.</span><span class="sxs-lookup"><span data-stu-id="f4ad2-104">The **XYZinCIE** WMI class contains the coordinates of the display in the International Commission on Illumination (CIE) XYZ color space.</span></span>

## <a name="syntax"></a><span data-ttu-id="f4ad2-105">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="f4ad2-105">Syntax</span></span>

``` syntax
class XYZinCIE : WmiMonitorColorCharacteristics
{
  uint16 X;
  uint16 Y;
};
```

## <a name="members"></a><span data-ttu-id="f4ad2-106">Membres</span><span class="sxs-lookup"><span data-stu-id="f4ad2-106">Members</span></span>

<span data-ttu-id="f4ad2-107">La classe **XYZinCIE** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="f4ad2-107">The **XYZinCIE** class has these types of members:</span></span>

-   [<span data-ttu-id="f4ad2-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f4ad2-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f4ad2-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="f4ad2-109">Properties</span></span>

<span data-ttu-id="f4ad2-110">La classe **XYZinCIE** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="f4ad2-110">The **XYZinCIE** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f4ad2-111">**X**</span><span class="sxs-lookup"><span data-stu-id="f4ad2-111">**X**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4ad2-112">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f4ad2-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f4ad2-113">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f4ad2-113">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4ad2-114">Coordonnée X.</span><span class="sxs-lookup"><span data-stu-id="f4ad2-114">X-coordinate.</span></span>

</dd> <dt>

<span data-ttu-id="f4ad2-115">**O**</span><span class="sxs-lookup"><span data-stu-id="f4ad2-115">**Y**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f4ad2-116">Type de données : **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f4ad2-116">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f4ad2-117">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="f4ad2-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f4ad2-118">Coordonnée Y.</span><span class="sxs-lookup"><span data-stu-id="f4ad2-118">Y-coordinate.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f4ad2-119">Notes</span><span class="sxs-lookup"><span data-stu-id="f4ad2-119">Remarks</span></span>

<span data-ttu-id="f4ad2-120">La classe [**WmiMonitorColorCharacteristics**](wmimonitorcolorcharacteristics.md) contient des instances incorporées de la classe **XYZinCIE** pour décrire les caractéristiques de couleur d’une analyse.</span><span class="sxs-lookup"><span data-stu-id="f4ad2-120">The [**WmiMonitorColorCharacteristics**](wmimonitorcolorcharacteristics.md) class contains embedded instances of the **XYZinCIE** class to describe the color characteristics of a monitor.</span></span>

<span data-ttu-id="f4ad2-121">Pour calculer la coordonnée z, en fonction des valeurs x et y, utilisez la relation \| \| (x, y, z) \| \| = 1.</span><span class="sxs-lookup"><span data-stu-id="f4ad2-121">To calculate the z-coordinate, based on the x and y values, use the relation \|\|(x,y,z)\|\| = 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4ad2-122">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="f4ad2-122">Requirements</span></span>



| <span data-ttu-id="f4ad2-123">Condition requise</span><span class="sxs-lookup"><span data-stu-id="f4ad2-123">Requirement</span></span> | <span data-ttu-id="f4ad2-124">Valeur</span><span class="sxs-lookup"><span data-stu-id="f4ad2-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f4ad2-125">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f4ad2-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f4ad2-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f4ad2-126">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="f4ad2-127">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="f4ad2-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f4ad2-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f4ad2-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="f4ad2-129">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="f4ad2-129">Namespace</span></span><br/>                | <span data-ttu-id="f4ad2-130">\\WMI racine</span><span class="sxs-lookup"><span data-stu-id="f4ad2-130">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="f4ad2-131">MOF</span><span class="sxs-lookup"><span data-stu-id="f4ad2-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f4ad2-132"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f4ad2-132"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="f4ad2-133">DLL</span><span class="sxs-lookup"><span data-stu-id="f4ad2-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f4ad2-134"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f4ad2-134"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4ad2-135">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="f4ad2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4ad2-136">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="f4ad2-136">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




