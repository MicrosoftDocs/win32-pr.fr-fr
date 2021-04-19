---
description: L’objet SafeWia est un &\# 0034 ; Safe pour les scripts&\# 0034 ; point d’entrée pour toutes les fonctionnalités de script WIA (Windows Image Acquisition).
ms.assetid: 6b10bb8e-8500-4f2c-ae18-5db78ef75f74
title: Objet SafeWia
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SafeWia
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: 1f227180b7420f5c70ef64d7d1d3feb0f13ae164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514442"
---
# <a name="safewia-object"></a><span data-ttu-id="c09c0-103">Objet SafeWia</span><span class="sxs-lookup"><span data-stu-id="c09c0-103">SafeWia object</span></span>

<span data-ttu-id="c09c0-104">L’objet **SafeWia** est un point d’entrée « sécurisé pour le script » pour toutes les fonctionnalités de script WIA (Windows Image Acquisition).</span><span class="sxs-lookup"><span data-stu-id="c09c0-104">The **SafeWia** object is a "safe for scripting" entry point for all Windows Image Acquisition (WIA) scripting functionality.</span></span> <span data-ttu-id="c09c0-105">Toute application qui utilise le modèle de script WIA doit créer un objet **SafeWia** ou [**WIA**](-wia-wia.md) .</span><span class="sxs-lookup"><span data-stu-id="c09c0-105">Any application that uses the WIA scripting model must create a **SafeWia** or [**Wia**](-wia-wia.md) object.</span></span> <span data-ttu-id="c09c0-106">Utilisez cet objet pour énumérer et créer des appareils et recevoir des notifications d’événements matériels.</span><span class="sxs-lookup"><span data-stu-id="c09c0-106">Use that object to enumerate and create devices and to receive notification of hardware events.</span></span>

## <a name="members"></a><span data-ttu-id="c09c0-107">Membres</span><span class="sxs-lookup"><span data-stu-id="c09c0-107">Members</span></span>

<span data-ttu-id="c09c0-108">L’objet **SafeWia** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="c09c0-108">The **SafeWia** object has these types of members:</span></span>

-   [<span data-ttu-id="c09c0-109">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c09c0-109">Methods</span></span>](#methods)
-   [<span data-ttu-id="c09c0-110">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c09c0-110">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c09c0-111">Méthodes</span><span class="sxs-lookup"><span data-stu-id="c09c0-111">Methods</span></span>

<span data-ttu-id="c09c0-112">L’objet **SafeWia** a ces méthodes.</span><span class="sxs-lookup"><span data-stu-id="c09c0-112">The **SafeWia** object has these methods.</span></span>



| <span data-ttu-id="c09c0-113">Méthode</span><span class="sxs-lookup"><span data-stu-id="c09c0-113">Method</span></span>                             | <span data-ttu-id="c09c0-114">Description</span><span class="sxs-lookup"><span data-stu-id="c09c0-114">Description</span></span>                                                                                                                                                                                                                |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c09c0-115">**Créés**</span><span class="sxs-lookup"><span data-stu-id="c09c0-115">**Create**</span></span>](-wia-iwia-create.md) | <span data-ttu-id="c09c0-116">La méthode [**Create**](-wia-iwia-create.md) de l’objet [**WIA**](-wia-wia.md) établit une connexion à l’appareil WIA spécifié et retourne un objet [**Item**](-wia-item.md) qui représente l’appareil.</span><span class="sxs-lookup"><span data-stu-id="c09c0-116">The [**Create**](-wia-iwia-create.md) method of the [**Wia**](-wia-wia.md) object makes a connection to the specified WIA device, and returns an [**Item**](-wia-item.md) object that represents the device.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c09c0-117">Propriétés</span><span class="sxs-lookup"><span data-stu-id="c09c0-117">Properties</span></span>

<span data-ttu-id="c09c0-118">L’objet **SafeWia** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="c09c0-118">The **SafeWia** object has these properties.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="c09c0-119">Propriété</span><span class="sxs-lookup"><span data-stu-id="c09c0-119">Property</span></span></th>
<th style="text-align: left;"><span data-ttu-id="c09c0-120">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="c09c0-120">Access type</span></span></th>
<th style="text-align: left;"><span data-ttu-id="c09c0-121">Description</span><span class="sxs-lookup"><span data-stu-id="c09c0-121">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="c09c0-122"><a href="-wia-iwia-devices.md"><strong>Appareils</strong></a></span><span class="sxs-lookup"><span data-stu-id="c09c0-122"><a href="-wia-iwia-devices.md"><strong>Devices</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="c09c0-123">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="c09c0-123">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="c09c0-124">Collection d’objets <a href="-wia-deviceinfo.md"><strong>DeviceInfo</strong></a> qui représentent tous les périphériques installés sur l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="c09c0-124">Collection of <a href="-wia-deviceinfo.md"><strong>DeviceInfo</strong></a> objects that represents all of the devices installed on the computer.</span></span> <span data-ttu-id="c09c0-125">Lecture seule.</span><span class="sxs-lookup"><span data-stu-id="c09c0-125">Read-only.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="c09c0-126">Cette collection est de base 0.</span><span class="sxs-lookup"><span data-stu-id="c09c0-126">This collection is 0-based.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="c09c0-127">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c09c0-127">Requirements</span></span>



| <span data-ttu-id="c09c0-128">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c09c0-128">Requirement</span></span> | <span data-ttu-id="c09c0-129">Valeur</span><span class="sxs-lookup"><span data-stu-id="c09c0-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c09c0-130">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c09c0-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c09c0-131">Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c09c0-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="c09c0-132">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="c09c0-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c09c0-133">Applications de bureau Windows Server 2003 \[ uniquement\]</span><span class="sxs-lookup"><span data-stu-id="c09c0-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="c09c0-134">DLL</span><span class="sxs-lookup"><span data-stu-id="c09c0-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c09c0-135"><dt>Wiascr.dll (version 4,90 ou ultérieure)</dt></span><span class="sxs-lookup"><span data-stu-id="c09c0-135"><dt>Wiascr.dll (version 4.90 or later)</dt></span></span> </dl> |
| <span data-ttu-id="c09c0-136">IID</span><span class="sxs-lookup"><span data-stu-id="c09c0-136">IID</span></span><br/>                      | <span data-ttu-id="c09c0-137">CLSID \_ SafeWia</span><span class="sxs-lookup"><span data-stu-id="c09c0-137">CLSID\_SafeWia</span></span><br/>                                                                                     |



## <a name="see-also"></a><span data-ttu-id="c09c0-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="c09c0-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c09c0-139">**WIA**</span><span class="sxs-lookup"><span data-stu-id="c09c0-139">**Wia**</span></span>](-wia-wia.md)
</dt> </dl>

 

 




