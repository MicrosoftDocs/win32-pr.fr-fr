---
description: La propriété FeatureValidStates de l’objet session retourne un entier représentant des indicateurs binaires avec chaque bit approprié représentant un état d’installation valide pour la fonctionnalité spécifiée.
ms.assetid: 8a1f6911-b0a6-4fac-ba77-df4f1b7d15e2
title: Session. FeatureValidStates, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.FeatureValidStates
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: b76080bb7854c75cbfbb06697de9fc7d7a1af0c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106521651"
---
# <a name="sessionfeaturevalidstates-property"></a><span data-ttu-id="8317d-103">Session. FeatureValidStates, propriété</span><span class="sxs-lookup"><span data-stu-id="8317d-103">Session.FeatureValidStates property</span></span>

<span data-ttu-id="8317d-104">La propriété **FeatureValidStates** de l’objet [**session**](session-object.md) retourne un entier représentant des indicateurs binaires avec chaque bit approprié représentant un état d’installation valide pour la fonctionnalité spécifiée.</span><span class="sxs-lookup"><span data-stu-id="8317d-104">The **FeatureValidStates** property of the [**Session**](session-object.md) object returns an integer representing bit flags with each relevant bit representing a valid installation state for the specified feature.</span></span>

<span data-ttu-id="8317d-105">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="8317d-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8317d-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="8317d-106">Syntax</span></span>


```JScript
propVal = Session.FeatureValidStates
```



## <a name="property-value"></a><span data-ttu-id="8317d-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="8317d-107">Property value</span></span>

<span data-ttu-id="8317d-108">Nom de chaîne requis de l’élément de fonctionnalité dont les États d’installation valides doivent être récupérés.</span><span class="sxs-lookup"><span data-stu-id="8317d-108">Required string name of the feature item whose valid installation states are to be retrieved.</span></span>

## <a name="remarks"></a><span data-ttu-id="8317d-109">Notes</span><span class="sxs-lookup"><span data-stu-id="8317d-109">Remarks</span></span>

<span data-ttu-id="8317d-110">La valeur de retour est composée d’indicateurs binaires, comme suit.</span><span class="sxs-lookup"><span data-stu-id="8317d-110">The return value is composed of bit flags as follows.</span></span> <span data-ttu-id="8317d-111">Bit 0 : s’il est défini, local est un état valide.</span><span class="sxs-lookup"><span data-stu-id="8317d-111">Bit 0: if set, Local is a valid state.</span></span> <span data-ttu-id="8317d-112">Bit 1 : s’il est défini, la source est un état valide.</span><span class="sxs-lookup"><span data-stu-id="8317d-112">Bit 1: if set, Source is a valid state.</span></span>

<span data-ttu-id="8317d-113">La propriété **FeatureValidStates** ne fonctionne que si le programme d’installation a appelé les actions [CostInitialize](costinitialize-action.md) et [CostFinalize](costfinalize-action.md) .</span><span class="sxs-lookup"><span data-stu-id="8317d-113">The **FeatureValidStates** property only succeeds after the installer has called the [CostInitialize](costinitialize-action.md) and [CostFinalize](costfinalize-action.md) actions.</span></span>

<span data-ttu-id="8317d-114">**FeatureValidStates** détermine la validité de l’État en interrogeant tous les composants liés à la fonctionnalité spécifiée sans tenir compte de l’état d’installation actuel d’un composant.</span><span class="sxs-lookup"><span data-stu-id="8317d-114">**FeatureValidStates** determines state validity by querying all components that are linked to the specified feature without taking into account the current installed state of any component.</span></span>

<span data-ttu-id="8317d-115">Les États valides possibles pour une fonctionnalité sont déterminés comme suit :</span><span class="sxs-lookup"><span data-stu-id="8317d-115">The possible valid states for a feature are determined as follows:</span></span>

-   <span data-ttu-id="8317d-116">Si la fonctionnalité ne contient pas de composants, les deux versions \_ \_ de la source de l’élément InstallState locale et de la source InstallState sont valides pour la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="8317d-116">If the feature does not contain components, both INSTALLSTATE\_LOCAL and INSTALLSTATE\_SOURCE are valid states for the feature.</span></span>
-   <span data-ttu-id="8317d-117">Si au moins un composant de la fonctionnalité a un attribut msidbComponentAttributesLocalOnly ou msidbComponentAttributesOptional, INSTALLSTATE \_ local est un état valide pour la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="8317d-117">If at least one component of the feature has an attribute of msidbComponentAttributesLocalOnly or msidbComponentAttributesOptional, INSTALLSTATE\_LOCAL is a valid state for the feature.</span></span>
-   <span data-ttu-id="8317d-118">Si au moins un composant de la fonctionnalité a un attribut msidbComponentAttributesSourceOnly ou msidbComponentAttributesOptional, INSTALLSTATE \_ source est un état valide pour la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="8317d-118">If at least one component of the feature has an attribute of msidbComponentAttributesSourceOnly or msidbComponentAttributesOptional, INSTALLSTATE\_SOURCE is a valid state for the feature.</span></span>
-   <span data-ttu-id="8317d-119">Si un fichier d’un composant appartenant à la fonctionnalité est corrigé ou provient d’une source compressée, \_ la source INSTALLSTATE n’est pas incluse dans un état valide pour la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="8317d-119">If a file of a component belonging to the feature is patched or from a compressed source, then INSTALLSTATE\_SOURCE is not included as a valid state for the feature.</span></span>
-   <span data-ttu-id="8317d-120">INSTALLSTATE \_ advertise n’est pas un état valide si la fonctionnalité interdit la publication (msidbFeatureAttributesDisallowAdvertise) ou si la fonctionnalité requiert la prise en charge de la plateforme pour la publication (msidbFeatureAttributesNoUnsupportedAdvertise) et que la plateforme ne la prend pas en charge.</span><span class="sxs-lookup"><span data-stu-id="8317d-120">INSTALLSTATE\_ADVERTISE is not a valid state if the feature disallows advertisement (msidbFeatureAttributesDisallowAdvertise) or the feature requires platform support for advertisement (msidbFeatureAttributesNoUnsupportedAdvertise) and the platform does not support it.</span></span>
-   <span data-ttu-id="8317d-121">INSTALLSTATE \_ absent est un état valide pour la fonctionnalité si ses attributs n’incluent pas msidbFeatureAttributesUIDisallowAbsent.</span><span class="sxs-lookup"><span data-stu-id="8317d-121">INSTALLSTATE\_ABSENT is a valid state for the feature if its attributes do not include msidbFeatureAttributesUIDisallowAbsent.</span></span>
-   <span data-ttu-id="8317d-122">Les États valides pour les fonctionnalités enfants marquées pour suivre la fonctionnalité parente (msidbFeatureAttributesFollowParent) sont basés sur l’action de la fonctionnalité parente ou sur l’état installé.</span><span class="sxs-lookup"><span data-stu-id="8317d-122">Valid states for child features marked to follow the parent feature (msidbFeatureAttributesFollowParent) are based upon the parent feature's action or installed state.</span></span>

<span data-ttu-id="8317d-123">Si la propriété échoue, vous pouvez obtenir des informations d’erreur étendues à l’aide de la méthode [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="8317d-123">If the property fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="8317d-124">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="8317d-124">Requirements</span></span>



| <span data-ttu-id="8317d-125">Condition requise</span><span class="sxs-lookup"><span data-stu-id="8317d-125">Requirement</span></span> | <span data-ttu-id="8317d-126">Valeur</span><span class="sxs-lookup"><span data-stu-id="8317d-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8317d-127">Version</span><span class="sxs-lookup"><span data-stu-id="8317d-127">Version</span></span><br/> | <span data-ttu-id="8317d-128">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="8317d-128">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="8317d-129">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8317d-129">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="8317d-130">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="8317d-130">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="8317d-131">DLL</span><span class="sxs-lookup"><span data-stu-id="8317d-131">DLL</span></span><br/>     | <dl> <span data-ttu-id="8317d-132"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8317d-132"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="8317d-133">IID</span><span class="sxs-lookup"><span data-stu-id="8317d-133">IID</span></span><br/>     | <span data-ttu-id="8317d-134">IID \_ ISession est défini en tant que 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="8317d-134">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




