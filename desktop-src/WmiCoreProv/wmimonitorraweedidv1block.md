---
description: Représente les données brutes d’une structure E-EDID (Extended Display Identification Data) améliorée d’une association Video Electronics standard Association (VESA).
ms.assetid: a51b73bb-a5f7-4e01-9c88-780105e9952b
title: WmiMonitorRawEEdidV1Block, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorRawEEdidV1Block
- WmiMonitorRawEEdidV1Block.Active
- WmiMonitorRawEEdidV1Block.InstanceName
- WmiMonitorRawEEdidV1Block.Id
- WmiMonitorRawEEdidV1Block.Type
- WmiMonitorRawEEdidV1Block.Content
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 79566dccceb36281c9b3a94b19fed2ed5679dc8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106518333"
---
# <a name="wmimonitorraweedidv1block-class"></a><span data-ttu-id="7c977-103">WmiMonitorRawEEdidV1Block, classe</span><span class="sxs-lookup"><span data-stu-id="7c977-103">WmiMonitorRawEEdidV1Block class</span></span>

<span data-ttu-id="7c977-104">La classe WMI **WmiMonitorRawEEdidV1Block** représente les données brutes d’une structure E-EDID (Extended Display Identification Data) améliorée d’une association Video Electronics standard Association (VESA).</span><span class="sxs-lookup"><span data-stu-id="7c977-104">The **WmiMonitorRawEEdidV1Block** WMI class represents the raw data from a Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) structure.</span></span> <span data-ttu-id="7c977-105">Cette structure de données de 128 octets contient des informations qui décrivent la configuration optimale pour un affichage.</span><span class="sxs-lookup"><span data-stu-id="7c977-105">This 128-byte data structure contains information that describes the optimal configuration for a display.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c977-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="7c977-106">Syntax</span></span>

``` syntax
class WmiMonitorRawEEdidV1Block : MSMonitorClass
{
  boolean Active;
  string  InstanceName;
  uint8   Id;
  uint8   Type;
  uint8   Content[];
};
```

## <a name="members"></a><span data-ttu-id="7c977-107">Membres</span><span class="sxs-lookup"><span data-stu-id="7c977-107">Members</span></span>

<span data-ttu-id="7c977-108">La classe **WmiMonitorRawEEdidV1Block** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="7c977-108">The **WmiMonitorRawEEdidV1Block** class has these types of members:</span></span>

-   [<span data-ttu-id="7c977-109">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7c977-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7c977-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="7c977-110">Properties</span></span>

<span data-ttu-id="7c977-111">La classe **WmiMonitorRawEEdidV1Block** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="7c977-111">The **WmiMonitorRawEEdidV1Block** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7c977-112">**Actif**</span><span class="sxs-lookup"><span data-stu-id="7c977-112">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c977-113">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="7c977-113">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="7c977-114">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7c977-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c977-115">Indique le moniteur actif.</span><span class="sxs-lookup"><span data-stu-id="7c977-115">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="7c977-116">**Contenu**</span><span class="sxs-lookup"><span data-stu-id="7c977-116">**Content**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c977-117">Type de données : tableau **UInt8**</span><span class="sxs-lookup"><span data-stu-id="7c977-117">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="7c977-118">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7c977-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c977-119">Tableau de 128 octets qui contient le contenu du bloc brut.</span><span class="sxs-lookup"><span data-stu-id="7c977-119">128 byte array that contains the raw block content.</span></span>

</dd> <dt>

<span data-ttu-id="7c977-120">**Id**</span><span class="sxs-lookup"><span data-stu-id="7c977-120">**Id**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c977-121">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="7c977-121">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="7c977-122">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7c977-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c977-123">Identité du bloc de données.</span><span class="sxs-lookup"><span data-stu-id="7c977-123">Identity of the data block.</span></span>

</dd> <dt>

<span data-ttu-id="7c977-124">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="7c977-124">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c977-125">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="7c977-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7c977-126">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7c977-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7c977-127">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="7c977-127">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="7c977-128">Nom de l’instance d’analyse spécifique.</span><span class="sxs-lookup"><span data-stu-id="7c977-128">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="7c977-129">**Type**</span><span class="sxs-lookup"><span data-stu-id="7c977-129">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7c977-130">Type de données : **UInt8**</span><span class="sxs-lookup"><span data-stu-id="7c977-130">Data type: **uint8**</span></span>
</dt> <dt>

<span data-ttu-id="7c977-131">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="7c977-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7c977-132">Type de bloc de données.</span><span class="sxs-lookup"><span data-stu-id="7c977-132">Type of data block.</span></span> <span data-ttu-id="7c977-133">Le tableau suivant répertorie les valeurs possibles qui peuvent être retournées.</span><span class="sxs-lookup"><span data-stu-id="7c977-133">The following table lists possible values that can be returned.</span></span>



| <span data-ttu-id="7c977-134">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c977-134">Value</span></span>                                                                                 | <span data-ttu-id="7c977-135">Signification</span><span class="sxs-lookup"><span data-stu-id="7c977-135">Meaning</span></span>                    |
|---------------------------------------------------------------------------------------|----------------------------|
| <dl> <span data-ttu-id="7c977-136"><dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="7c977-136"><dt>0 (0x0)</dt></span></span> </dl>    | <span data-ttu-id="7c977-137">Non initialisé(e)</span><span class="sxs-lookup"><span data-stu-id="7c977-137">Uninitialized</span></span><br/>   |
| <dl> <span data-ttu-id="7c977-138"><dt>1 (0x1)</dt></span><span class="sxs-lookup"><span data-stu-id="7c977-138"><dt>1 (0x1)</dt></span></span> </dl>    | <span data-ttu-id="7c977-139">Bloc de base EDID</span><span class="sxs-lookup"><span data-stu-id="7c977-139">EDID base block</span></span><br/> |
| <dl> <span data-ttu-id="7c977-140"><dt>2 (0X2)</dt></span><span class="sxs-lookup"><span data-stu-id="7c977-140"><dt>2 (0x2)</dt></span></span> </dl>    | <span data-ttu-id="7c977-141">Carte de blocs EDID</span><span class="sxs-lookup"><span data-stu-id="7c977-141">EDID block map</span></span><br/>  |
| <dl> <span data-ttu-id="7c977-142"><dt>255 (0xFF)</dt></span><span class="sxs-lookup"><span data-stu-id="7c977-142"><dt>255 (0xFF)</dt></span></span> </dl> | <span data-ttu-id="7c977-143">Autres</span><span class="sxs-lookup"><span data-stu-id="7c977-143">Other</span></span><br/>           |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7c977-144">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="7c977-144">Requirements</span></span>



| <span data-ttu-id="7c977-145">Condition requise</span><span class="sxs-lookup"><span data-stu-id="7c977-145">Requirement</span></span> | <span data-ttu-id="7c977-146">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c977-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7c977-147">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c977-147">Minimum supported client</span></span><br/> | <span data-ttu-id="7c977-148">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7c977-148">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="7c977-149">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="7c977-149">Minimum supported server</span></span><br/> | <span data-ttu-id="7c977-150">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7c977-150">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="7c977-151">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="7c977-151">Namespace</span></span><br/>                | <span data-ttu-id="7c977-152">\\WMI racine</span><span class="sxs-lookup"><span data-stu-id="7c977-152">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="7c977-153">MOF</span><span class="sxs-lookup"><span data-stu-id="7c977-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7c977-154"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7c977-154"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="7c977-155">DLL</span><span class="sxs-lookup"><span data-stu-id="7c977-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7c977-156"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7c977-156"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c977-157">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="7c977-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c977-158">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="7c977-158">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> <dt>

[<span data-ttu-id="7c977-159">**WmiGetMonitorRawEEdidV1Block**</span><span class="sxs-lookup"><span data-stu-id="7c977-159">**WmiGetMonitorRawEEdidV1Block**</span></span>](wmigetmonitorraweedidv1block-wmimonitordescriptormethods.md)
</dt> </dl>

 

 




