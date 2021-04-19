---
description: Représente les paramètres d’entrée de la vidéo numérique.
ms.assetid: aa459612-db79-477b-891f-28c9d0b1b497
title: WmiMonitorDigitalVideoInputParams, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorDigitalVideoInputParams
- WmiMonitorDigitalVideoInputParams.Active
- WmiMonitorDigitalVideoInputParams.InstanceName
- WmiMonitorDigitalVideoInputParams.IsDFP1xCompatible
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: a08e38a38bb5f5e8d539fabdf69c429c42f4b1f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521097"
---
# <a name="wmimonitordigitalvideoinputparams-class"></a><span data-ttu-id="80b4a-103">WmiMonitorDigitalVideoInputParams, classe</span><span class="sxs-lookup"><span data-stu-id="80b4a-103">WmiMonitorDigitalVideoInputParams class</span></span>

<span data-ttu-id="80b4a-104">**WmiMonitorDigitalVideoInputParams** représente les paramètres d’entrée de la vidéo numérique.</span><span class="sxs-lookup"><span data-stu-id="80b4a-104">The **WmiMonitorDigitalVideoInputParams** represents input parameters for digital video.</span></span> <span data-ttu-id="80b4a-105">Les données de cette classe correspondent aux données de la définition d’entrée vidéo de la norme E-EDID (Extended Display Identification Data) améliorée de l’Association Video Electronics standard Association (VESA).</span><span class="sxs-lookup"><span data-stu-id="80b4a-105">The data in this class corresponds to data in the Video Input Definition of Video Electronics Standard Association (VESA) Enhanced Extended Display Identification Data (E-EDID) standard.</span></span> <span data-ttu-id="80b4a-106">Une instance de cette classe est disponible uniquement lorsque la valeur de la propriété **VideoInputType** de la classe [**WmiMonitorBasicDisplayParams**](wmimonitorbasicdisplayparams.md) est « Digital ».</span><span class="sxs-lookup"><span data-stu-id="80b4a-106">An instance of this class is available only when the value of the **VideoInputType** property of the [**WmiMonitorBasicDisplayParams**](wmimonitorbasicdisplayparams.md) class is "Digital".</span></span>

## <a name="syntax"></a><span data-ttu-id="80b4a-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="80b4a-107">Syntax</span></span>

``` syntax
class WmiMonitorDigitalVideoInputParams : MSMonitorClass
{
  boolean Active;
  string  InstanceName;
  boolean IsDFP1xCompatible;
};
```

## <a name="members"></a><span data-ttu-id="80b4a-108">Membres</span><span class="sxs-lookup"><span data-stu-id="80b4a-108">Members</span></span>

<span data-ttu-id="80b4a-109">La classe **WmiMonitorDigitalVideoInputParams** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="80b4a-109">The **WmiMonitorDigitalVideoInputParams** class has these types of members:</span></span>

-   [<span data-ttu-id="80b4a-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="80b4a-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="80b4a-111">Propriétés</span><span class="sxs-lookup"><span data-stu-id="80b4a-111">Properties</span></span>

<span data-ttu-id="80b4a-112">La classe **WmiMonitorDigitalVideoInputParams** possède les propriétés suivantes.</span><span class="sxs-lookup"><span data-stu-id="80b4a-112">The **WmiMonitorDigitalVideoInputParams** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="80b4a-113">**Actif**</span><span class="sxs-lookup"><span data-stu-id="80b4a-113">**Active**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80b4a-114">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="80b4a-114">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="80b4a-115">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80b4a-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80b4a-116">Indique le moniteur actif.</span><span class="sxs-lookup"><span data-stu-id="80b4a-116">Indicates the active monitor.</span></span>

</dd> <dt>

<span data-ttu-id="80b4a-117">**InstanceName**</span><span class="sxs-lookup"><span data-stu-id="80b4a-117">**InstanceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80b4a-118">Type de données : **chaîne**</span><span class="sxs-lookup"><span data-stu-id="80b4a-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="80b4a-119">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80b4a-119">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="80b4a-120">Qualificateurs : **clé**</span><span class="sxs-lookup"><span data-stu-id="80b4a-120">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="80b4a-121">Nom de l’instance d’analyse spécifique.</span><span class="sxs-lookup"><span data-stu-id="80b4a-121">Name of the specific monitor instance.</span></span>

</dd> <dt>

<span data-ttu-id="80b4a-122">**IsDFP1xCompatible**</span><span class="sxs-lookup"><span data-stu-id="80b4a-122">**IsDFP1xCompatible**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="80b4a-123">Type de données : **booléen**</span><span class="sxs-lookup"><span data-stu-id="80b4a-123">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="80b4a-124">Type d'accès : Lecture seule</span><span class="sxs-lookup"><span data-stu-id="80b4a-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="80b4a-125">VESA DFP 1. x ou compatible.</span><span class="sxs-lookup"><span data-stu-id="80b4a-125">VESA DFP 1.x or compatible.</span></span> <span data-ttu-id="80b4a-126">Si cette valeur est définie, l’interface est signalée comme étant compatible avec le panneau plat numérique (DFP) 1. x transition réduite de signal différentiel (TMDS) CRGB, 1 pixel/horloge, jusqu’à 8 bits/bit DE poids le plus significatif (MSB) aligné, DE haut actif.</span><span class="sxs-lookup"><span data-stu-id="80b4a-126">If set, interface is signal compatible with VESA Digital Flat Panel (DFP) 1.x Transition Minimized Differential Signaling (TMDS) CRGB, 1 pixel/clock, up to 8 bits/color most significant bit (MSB) aligned, DE active high.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="80b4a-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="80b4a-127">Requirements</span></span>



| <span data-ttu-id="80b4a-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="80b4a-128">Requirement</span></span> | <span data-ttu-id="80b4a-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="80b4a-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="80b4a-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80b4a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="80b4a-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="80b4a-131">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="80b4a-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="80b4a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="80b4a-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="80b4a-133">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="80b4a-134">Espace de noms</span><span class="sxs-lookup"><span data-stu-id="80b4a-134">Namespace</span></span><br/>                | <span data-ttu-id="80b4a-135">\\WMI racine</span><span class="sxs-lookup"><span data-stu-id="80b4a-135">Root\\wmi</span></span><br/>                                                                   |
| <span data-ttu-id="80b4a-136">MOF</span><span class="sxs-lookup"><span data-stu-id="80b4a-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="80b4a-137"><dt>WmiCore. mof</dt></span><span class="sxs-lookup"><span data-stu-id="80b4a-137"><dt>WmiCore.mof</dt></span></span> </dl> |
| <span data-ttu-id="80b4a-138">DLL</span><span class="sxs-lookup"><span data-stu-id="80b4a-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80b4a-139"><dt>WmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80b4a-139"><dt>WmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80b4a-140">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="80b4a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80b4a-141">**MSMonitorClass**</span><span class="sxs-lookup"><span data-stu-id="80b4a-141">**MSMonitorClass**</span></span>](msmonitorclass.md)
</dt> </dl>

 

 




