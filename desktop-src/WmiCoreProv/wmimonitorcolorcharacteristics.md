---
description: Représente les caractéristiques de couleur CIE (International Commission on illumination) d’un moniteur d’ordinateur.
ms.assetid: 476aefae-11c0-46be-a2bb-83fbafd70421
title: WmiMonitorColorCharacteristics, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorColorCharacteristics
- WmiMonitorColorCharacteristics.Active
- WmiMonitorColorCharacteristics.Blue
- WmiMonitorColorCharacteristics.DefaultWhite
- WmiMonitorColorCharacteristics.Green
- WmiMonitorColorCharacteristics.InstanceName
- WmiMonitorColorCharacteristics.Red
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 9fbb7d56e56519576d257b077311a144e923d6bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319578"
---
# <a name="wmimonitorcolorcharacteristics-class"></a><span data-ttu-id="43191-103">WmiMonitorColorCharacteristics, classe</span><span class="sxs-lookup"><span data-stu-id="43191-103">WmiMonitorColorCharacteristics class</span></span>

<span data-ttu-id="43191-104">La classe **WmiMonitorColorCharacteristics** représente les caractéristiques de couleur Cie (International Commission on illumination) d’un moniteur d’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="43191-104">The **WmiMonitorColorCharacteristics** class represents the International Commission on Illumination (CIE) color characteristics of a computer monitor.</span></span> <span data-ttu-id="43191-105">Les données correspondent aux données dans le bloc des caractéristiques de couleur de la structure E-EDID (Extended Display Identification Data) améliorée de l’Association Video Electronics standard Association (VESA).</span><span class="sxs-lookup"><span data-stu-id="43191-105">The data corresponds to data in the Color Characteristics block of the Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="43191-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="43191-106">Syntax</span></span>

``` syntax
class WmiMonitorColorCharacteristics : MSMonitorClass
{
  boolean  Active;
  XYZinCIE Blue;
  XYZinCIE DefaultWhite;
  XYZinCIE Green;
  string   InstanceName;
  XYZinCIE Red;
};
```

## <a name="members"></a><span data-ttu-id="43191-107">Membres</span><span class="sxs-lookup"><span data-stu-id="43191-107">Members</span></span>

<span data-ttu-id="43191-108">La classe **WmiMonitorColorCharacteristics** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="43191-108">The **WmiMonitorColorCharacteristics** class has these types of members:</span></span>

-   [<span data-ttu-id="43191-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="43191-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="43191-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="43191-110">Properties</span></span>

<span data-ttu-id="43191-111">La classe **WmiMonitorColorCharacteristics** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="43191-111">The **WmiMonitorColorCharacteristics** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="43191-112">**Actif**</span><span class="sxs-lookup"><span data-stu-id="43191-112">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43191-113">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="43191-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="43191-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="43191-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43191-115">Indique le moniteur actif.</span><span class="sxs-lookup"><span data-stu-id="43191-115">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="43191-116">**Bleu**</span><span class="sxs-lookup"><span data-stu-id="43191-116">**Blue**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43191-117">Type de données : **[ **XYZinCIE**](xyzincie.md)**</span><span class="sxs-lookup"><span data-stu-id="43191-117">Data type: **[**XYZinCIE**](xyzincie.md)**</span></span>
</dt> <dt>

<span data-ttu-id="43191-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="43191-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43191-119">Coordonnées CIE pour le bleu, représentées par une instance de la classe [**XYZinCIE**](xyzincie.md) .</span><span class="sxs-lookup"><span data-stu-id="43191-119">CIE coordinates for blue, represented by an instance of the [**XYZinCIE**](xyzincie.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="43191-120">**DefaultWhite**</span><span class="sxs-lookup"><span data-stu-id="43191-120">**DefaultWhite**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43191-121">Type de données : **[ **XYZinCIE**](xyzincie.md)**</span><span class="sxs-lookup"><span data-stu-id="43191-121">Data type: **[**XYZinCIE**](xyzincie.md)**</span></span>
</dt> <dt>

<span data-ttu-id="43191-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="43191-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43191-123">Coordonnées CIE blanches par défaut.</span><span class="sxs-lookup"><span data-stu-id="43191-123">Default white CIE coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="43191-124">**Vert**</span><span class="sxs-lookup"><span data-stu-id="43191-124">**Green**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43191-125">Type de données : **[ **XYZinCIE**](xyzincie.md)**</span><span class="sxs-lookup"><span data-stu-id="43191-125">Data type: **[**XYZinCIE**](xyzincie.md)**</span></span>
</dt> <dt>

<span data-ttu-id="43191-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="43191-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43191-127">Coordonnées CIE pour le vert, représentées par une instance de la classe [**XYZinCIE**](xyzincie.md) .</span><span class="sxs-lookup"><span data-stu-id="43191-127">CIE coordinates for green, represented by an instance of the [**XYZinCIE**](xyzincie.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="43191-128">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="43191-128">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43191-129">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="43191-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="43191-130">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="43191-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="43191-131">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="43191-131">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="43191-132">Nom de l’instance d’analyse spécifique.</span><span class="sxs-lookup"><span data-stu-id="43191-132">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="43191-133">**Rouge**</span><span class="sxs-lookup"><span data-stu-id="43191-133">**Red**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43191-134">Type de données : **[ **XYZinCIE**](xyzincie.md)**</span><span class="sxs-lookup"><span data-stu-id="43191-134">Data type: **[**XYZinCIE**](xyzincie.md)**</span></span>
</dt> <dt>

<span data-ttu-id="43191-135">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="43191-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43191-136">Coordonnées CIE pour le rouge, représentées par une instance de la classe [**XYZinCIE**](xyzincie.md) .</span><span class="sxs-lookup"><span data-stu-id="43191-136">CIE coordinates for red, represented by an instance of the [**XYZinCIE**](xyzincie.md) class.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="43191-137">Notes</span><span class="sxs-lookup"><span data-stu-id="43191-137">Remarks</span></span>

<span data-ttu-id="43191-138">Les valeurs de la chromatique et du point blanc sont exprimées sous forme de nombres fractionnaires à l’aide d’un format d’encodage.</span><span class="sxs-lookup"><span data-stu-id="43191-138">The chromaticity and white point values are expressed as fractional numbers using an encoding format.</span></span> <span data-ttu-id="43191-139">Ce format est précis à l’emplacement du millième, ce qui correspond à une longueur de 10 bits.</span><span class="sxs-lookup"><span data-stu-id="43191-139">This format is accurate to the thousandth place, which is 10 bits in length.</span></span> <span data-ttu-id="43191-140">Le bit le plus significatif (MSB) représente 2 ^-1 et le bit le moins significatif (LSB) représente respectivement 2 ^-10 coefficients.</span><span class="sxs-lookup"><span data-stu-id="43191-140">The most significant bit (MSB) represents 2^-1 and the least significant bit (LSB) represents 2^-10 coefficients, respectively.</span></span> <span data-ttu-id="43191-141">La précision des valeurs stockées dans la structure E-EDID v1. x doit être précise à +/-0,005 de la valeur réelle.</span><span class="sxs-lookup"><span data-stu-id="43191-141">Precision of the stored values in the E-EDID v1.x structure should be accurate to +/- 0.005 of the actual value.</span></span>

## <a name="requirements"></a><span data-ttu-id="43191-142">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="43191-142">Requirements</span></span>



| <span data-ttu-id="43191-143">Condition requise</span><span class="sxs-lookup"><span data-stu-id="43191-143">Requirement</span></span> | <span data-ttu-id="43191-144">Valeur</span><span class="sxs-lookup"><span data-stu-id="43191-144">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="43191-145">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="43191-145">Minimum supported client</span></span><br/> | <span data-ttu-id="43191-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="43191-146">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="43191-147">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="43191-147">Minimum supported server</span></span><br/> | <span data-ttu-id="43191-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="43191-148">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="43191-149">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="43191-149">Namespace</span></span><br/>                | <span data-ttu-id="43191-150">\\WMI racine</span><span class="sxs-lookup"><span data-stu-id="43191-150">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="43191-151">MOF</span><span class="sxs-lookup"><span data-stu-id="43191-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="43191-152"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="43191-152"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="43191-153">DLL</span><span class="sxs-lookup"><span data-stu-id="43191-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43191-154"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="43191-154"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43191-155">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="43191-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43191-156">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="43191-156">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




