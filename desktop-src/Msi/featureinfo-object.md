---
description: L’objet FeatureInfo contient des informations sur la fonctionnalité ciblée et est créée à partir de l’objet session à l’aide de la méthode FeatureInfo.
ms.assetid: c9c96799-22c7-4e74-947b-3b8d31ebc1f1
title: Objet FeatureInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FeatureInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1db1bab5b1e55f027bb01eb9eff22484a4e39170
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535231"
---
# <a name="featureinfo-object"></a><span data-ttu-id="5276f-103">Objet FeatureInfo</span><span class="sxs-lookup"><span data-stu-id="5276f-103">FeatureInfo object</span></span>

<span data-ttu-id="5276f-104">L’objet **FeatureInfo** contient des informations sur la fonctionnalité ciblée et est créée à partir de l’objet [**session**](session-object.md) à l’aide de la méthode [**FeatureInfo**](session-featureinfo.md) .</span><span class="sxs-lookup"><span data-stu-id="5276f-104">The **FeatureInfo** object contains information regarding the targeted feature and is created from the [**Session**](session-object.md) object using the [**FeatureInfo**](session-featureinfo.md) Method.</span></span>

## <a name="members"></a><span data-ttu-id="5276f-105">Membres</span><span class="sxs-lookup"><span data-stu-id="5276f-105">Members</span></span>

<span data-ttu-id="5276f-106">L’objet **FeatureInfo** possède les types de membres suivants :</span><span class="sxs-lookup"><span data-stu-id="5276f-106">The **FeatureInfo** object has these types of members:</span></span>

-   [<span data-ttu-id="5276f-107">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5276f-107">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5276f-108">Propriétés</span><span class="sxs-lookup"><span data-stu-id="5276f-108">Properties</span></span>

<span data-ttu-id="5276f-109">L’objet **FeatureInfo** a ces propriétés.</span><span class="sxs-lookup"><span data-stu-id="5276f-109">The **FeatureInfo** object has these properties.</span></span>



| <span data-ttu-id="5276f-110">Propriété</span><span class="sxs-lookup"><span data-stu-id="5276f-110">Property</span></span>                                                  | <span data-ttu-id="5276f-111">Type d’accès</span><span class="sxs-lookup"><span data-stu-id="5276f-111">Access type</span></span>           | <span data-ttu-id="5276f-112">Description</span><span class="sxs-lookup"><span data-stu-id="5276f-112">Description</span></span>                                                                                 |
|:----------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5276f-113">**Attributs**</span><span class="sxs-lookup"><span data-stu-id="5276f-113">**Attributes**</span></span>](featureinfo-attributes.md)<br/>   | <span data-ttu-id="5276f-114">Lecture/écriture</span><span class="sxs-lookup"><span data-stu-id="5276f-114">Read/write</span></span><br/> | <span data-ttu-id="5276f-115">Retourne la valeur de la fonctionnalité dans la colonne attributs du tableau des fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="5276f-115">Returns the value for the feature in the Attributes column of the Feature table.</span></span><br/> |
| [<span data-ttu-id="5276f-116">**Description**</span><span class="sxs-lookup"><span data-stu-id="5276f-116">**Description**</span></span>](featureinfo-description.md)<br/> |                       | <span data-ttu-id="5276f-117">Retourne la description de la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="5276f-117">Returns the description of the feature.</span></span><br/>                                          |
| [<span data-ttu-id="5276f-118">**Intitulé**</span><span class="sxs-lookup"><span data-stu-id="5276f-118">**Title**</span></span>](featureinfo-title.md)<br/>             | <span data-ttu-id="5276f-119">Lecture seule</span><span class="sxs-lookup"><span data-stu-id="5276f-119">Read-only</span></span><br/>  | <span data-ttu-id="5276f-120">Retourne le titre de la fonctionnalité.</span><span class="sxs-lookup"><span data-stu-id="5276f-120">Returns the title of the feature.</span></span><br/>                                                |



 

## <a name="requirements"></a><span data-ttu-id="5276f-121">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="5276f-121">Requirements</span></span>



| <span data-ttu-id="5276f-122">Condition requise</span><span class="sxs-lookup"><span data-stu-id="5276f-122">Requirement</span></span> | <span data-ttu-id="5276f-123">Valeur</span><span class="sxs-lookup"><span data-stu-id="5276f-123">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5276f-124">Version</span><span class="sxs-lookup"><span data-stu-id="5276f-124">Version</span></span><br/> | <span data-ttu-id="5276f-125">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="5276f-125">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="5276f-126">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="5276f-126">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="5276f-127">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="5276f-127">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="5276f-128">DLL</span><span class="sxs-lookup"><span data-stu-id="5276f-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="5276f-129"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5276f-129"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="5276f-130">IID</span><span class="sxs-lookup"><span data-stu-id="5276f-130">IID</span></span><br/>     | <span data-ttu-id="5276f-131">IID \_ IFeatureInfo est défini en tant que 000C109F-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="5276f-131">IID\_IFeatureInfo is defined as 000C109F-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                         |



## <a name="see-also"></a><span data-ttu-id="5276f-132">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="5276f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5276f-133">Exemples de scripts Windows Installer</span><span class="sxs-lookup"><span data-stu-id="5276f-133">Windows Installer Scripting Examples</span></span>](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




