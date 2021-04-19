---
description: La propriété AVAILABLEFREEREG spécifie, en kilo-octets, l’espace libre total disponible dans le registre après l’appel de l’action AllocateRegistrySpace. La valeur maximale de la propriété AVAILABLEFREEREG est de 2 millions kilo-octets. Cette propriété est définie uniquement sur Windows 2000.
ms.assetid: 95afc397-2f28-4ab9-8d95-d071c2f1f498
title: Propriété AVAILABLEFREEREG
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 517073748195c47ee27b68adbe70d6c69f3f585b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541652"
---
# <a name="availablefreereg-property"></a><span data-ttu-id="2e911-103">Propriété AVAILABLEFREEREG</span><span class="sxs-lookup"><span data-stu-id="2e911-103">AVAILABLEFREEREG property</span></span>

<span data-ttu-id="2e911-104">La propriété **AVAILABLEFREEREG** spécifie, en kilo-octets, l’espace libre total disponible dans le registre après l’appel de l' [action AllocateRegistrySpace](allocateregistryspace-action.md).</span><span class="sxs-lookup"><span data-stu-id="2e911-104">The **AVAILABLEFREEREG** property specifies in kilobytes the total free space available in the registry after calling the [AllocateRegistrySpace action](allocateregistryspace-action.md).</span></span>

<span data-ttu-id="2e911-105">La valeur maximale de la propriété **AVAILABLEFREEREG** est de 2 millions kilo-octets.</span><span class="sxs-lookup"><span data-stu-id="2e911-105">The maximum value of the **AVAILABLEFREEREG** property is 2000000 kilobytes.</span></span>

<span data-ttu-id="2e911-106">Cette propriété est définie uniquement sur Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="2e911-106">This property is set only on Windows 2000.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e911-107">Notes</span><span class="sxs-lookup"><span data-stu-id="2e911-107">Remarks</span></span>

<span data-ttu-id="2e911-108">La propriété **AVAILABLEFREEREG** doit être définie sur une valeur suffisamment grande pour garantir un espace suffisant dans le registre pour toutes les informations d’inscription ajoutées par l’installation.</span><span class="sxs-lookup"><span data-stu-id="2e911-108">The **AVAILABLEFREEREG** property must be set to a value large enough to ensure sufficient space in the registry for all registration information added by the installation.</span></span> <span data-ttu-id="2e911-109">La valeur minimale requise pour garantir un espace suffisant dépend de l’emplacement de l' [action AllocateRegistrySpace](allocateregistryspace-action.md) dans la séquence d’action, car le programme d’installation augmente automatiquement l’espace en fonction des besoins lors de l’enregistrement des informations dans les tables [Registry](registry-table.md), [Class](class-table.md), [Selfreg](selfreg-table.md), [extension](extension-table.md), [MIME](mime-table.md)et [verb](verb-table.md) .</span><span class="sxs-lookup"><span data-stu-id="2e911-109">The minimum value required to ensure sufficient space depends on where the [AllocateRegistrySpace action](allocateregistryspace-action.md) is located in the action sequence because the installer automatically increases the space as needed when registering information in the [Registry](registry-table.md), [Class](class-table.md), [SelfReg](selfreg-table.md), [Extension](extension-table.md), [MIME](mime-table.md), and [Verb](verb-table.md) tables.</span></span> <span data-ttu-id="2e911-110">Le programme d’installation n’augmente pas l’espace total du Registre à la quantité spécifiée par **AVAILABLEFREEREG** jusqu’à atteindre AllocateRegistrySpace dans la séquence d’action.</span><span class="sxs-lookup"><span data-stu-id="2e911-110">The installer does not increase the total registry space to the amount specified by **AVAILABLEFREEREG** until reaching AllocateRegistrySpace in the action sequence.</span></span>

<span data-ttu-id="2e911-111">Si AllocateRegistrySpace est l’une des premières actions de la séquence d’action, **AVAILABLEFREEREG** doit être défini sur l’espace total requis par les informations d’inscription dans la table du Registre, la table de classes, la table Typelib, la table Selfreg, la table d’extension, la table MIME, la table de verbes, l’inscription des [actions personnalisées](custom-actions.md) , l’inscription automatique et toutes les autres informations de Registre écrites</span><span class="sxs-lookup"><span data-stu-id="2e911-111">If AllocateRegistrySpace is one of the first actions in the action sequence, **AVAILABLEFREEREG** should be set to the total space required by the registration information in the Registry table, Class table, TypeLib table, SelfReg table, Extension table, MIME table, Verb table, [custom actions](custom-actions.md) registration, self registration, and any other registry information written during the installation.</span></span> <span data-ttu-id="2e911-112">La valeur de **AVAILABLEFREEREG** est la quantité totale d’informations ajoutées par l’installation et garantit un espace suffisant dans tous les cas.</span><span class="sxs-lookup"><span data-stu-id="2e911-112">The value of **AVAILABLEFREEREG** is the total amount of information added by the installation and ensures sufficient space in all cases.</span></span> <span data-ttu-id="2e911-113">C’est également le cas le plus courant.</span><span class="sxs-lookup"><span data-stu-id="2e911-113">This is also the most common case.</span></span>

<span data-ttu-id="2e911-114">Si l’action AllocateRegistrySpace peut être créée dans la séquence d’action après toutes les [actions standard](standard-actions.md) qui écrivent des données d’inscription, telles que [WriteRegistryValues](writeregistryvalues-action.md) et [RegisterClassInfo](registerclassinfo-action.md), la valeur de **AVAILABLEFREEREG** doit uniquement être définie sur l’espace nécessaire pour enregistrer des actions personnalisées, inscrire des bibliothèques de types et toute autre information non encore inscrite dans les tables.</span><span class="sxs-lookup"><span data-stu-id="2e911-114">If the AllocateRegistrySpace action can be authored into the action sequence after all [standard actions](standard-actions.md) that write registration data, such as [WriteRegistryValues](writeregistryvalues-action.md) and [RegisterClassInfo](registerclassinfo-action.md), the value of **AVAILABLEFREEREG** needs only be set to the space needed to register custom actions, register type libraries, and any other information not yet registered through the tables.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e911-115">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="2e911-115">Requirements</span></span>



| <span data-ttu-id="2e911-116">Condition requise</span><span class="sxs-lookup"><span data-stu-id="2e911-116">Requirement</span></span> | <span data-ttu-id="2e911-117">Valeur</span><span class="sxs-lookup"><span data-stu-id="2e911-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e911-118">Version</span><span class="sxs-lookup"><span data-stu-id="2e911-118">Version</span></span><br/> | <span data-ttu-id="2e911-119">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="2e911-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="2e911-120">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="2e911-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="2e911-121">Windows Installer sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2e911-121">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="2e911-122">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="2e911-122">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2e911-123">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="2e911-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e911-124">Propriétés</span><span class="sxs-lookup"><span data-stu-id="2e911-124">Properties</span></span>](properties.md)
</dt> </dl>

 

 




