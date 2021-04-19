---
description: La propriété ComponentCosts de l’objet session retourne un objet RecordList énumérant l’espace disque par lecteur requis pour installer un composant.
ms.assetid: 9b1355f1-cc99-49d9-8187-07fba4804d1f
title: Session. ComponentCosts, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.ComponentCosts
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a6ef4e3bfd441f5de61c0f3d69aea93d6cfd2ed8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528121"
---
# <a name="sessioncomponentcosts-property"></a><span data-ttu-id="0e7ee-103">Session. ComponentCosts, propriété</span><span class="sxs-lookup"><span data-stu-id="0e7ee-103">Session.ComponentCosts property</span></span>

<span data-ttu-id="0e7ee-104">La propriété ComponentCosts de l’objet [**session**](session-object.md) retourne un objet [**RecordList**](recordlist-object.md) énumérant l’espace disque par lecteur requis pour installer un composant.</span><span class="sxs-lookup"><span data-stu-id="0e7ee-104">The ComponentCosts property of the [**Session**](session-object.md) object returns a [**RecordList**](recordlist-object.md) object enumerating the disk space per drive required to install a component.</span></span> <span data-ttu-id="0e7ee-105">Ces informations sont utilisées par l’interface utilisateur pour afficher l’espace disque requis pour tous les lecteurs.</span><span class="sxs-lookup"><span data-stu-id="0e7ee-105">This information is used by the user interface to display the disk space required for all drives.</span></span> <span data-ttu-id="0e7ee-106">Les coûts d’espace disque retournés sont de multiples de 512 octets.</span><span class="sxs-lookup"><span data-stu-id="0e7ee-106">The returned disk space costs are in multiples of 512 bytes.</span></span>

<span data-ttu-id="0e7ee-107">La propriété ComponentCosts doit être utilisée uniquement une fois que le programme d’installation a terminé le [coût des fichiers](file-costing.md) et après l' [action CostFinalize](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="0e7ee-107">The ComponentCosts property should only be used after the installer has completed [file costing](file-costing.md) and after the [CostFinalize action](costfinalize-action.md).</span></span>

<span data-ttu-id="0e7ee-108">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="0e7ee-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e7ee-109">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="0e7ee-109">Syntax</span></span>


```JScript
propVal = Session.ComponentCosts
```



## <a name="property-value"></a><span data-ttu-id="0e7ee-110">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="0e7ee-110">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="0e7ee-111">Notes</span><span class="sxs-lookup"><span data-stu-id="0e7ee-111">Remarks</span></span>

<span data-ttu-id="0e7ee-112">Pour obtenir le coût total, ajoutez les coûts pour tous les composants ainsi que le coût du moteur d’installation (composant = "").</span><span class="sxs-lookup"><span data-stu-id="0e7ee-112">To obtain the total cost, add the costs for all components plus the installer engine cost (Component = "").</span></span>

<span data-ttu-id="0e7ee-113">ComponentCosts retourne un [**objet RecordList**](recordlist-object.md).</span><span class="sxs-lookup"><span data-stu-id="0e7ee-113">ComponentCosts returns a [**RecordList object**](recordlist-object.md).</span></span> <span data-ttu-id="0e7ee-114">Chaque enregistrement de l’objet RecordList retourné contient les champs suivants :</span><span class="sxs-lookup"><span data-stu-id="0e7ee-114">Each record in the returned RecordList object has the following fields:</span></span>



| <span data-ttu-id="0e7ee-115">Champ</span><span class="sxs-lookup"><span data-stu-id="0e7ee-115">Field</span></span> | <span data-ttu-id="0e7ee-116">Description</span><span class="sxs-lookup"><span data-stu-id="0e7ee-116">Description</span></span>                                          |
|-------|------------------------------------------------------|
| <span data-ttu-id="0e7ee-117">1</span><span class="sxs-lookup"><span data-stu-id="0e7ee-117">1</span></span>     | <span data-ttu-id="0e7ee-118">Nom du lecteur/volume</span><span class="sxs-lookup"><span data-stu-id="0e7ee-118">Volume/Drive name</span></span>                                    |
| <span data-ttu-id="0e7ee-119">2</span><span class="sxs-lookup"><span data-stu-id="0e7ee-119">2</span></span>     | <span data-ttu-id="0e7ee-120">Coût de l’espace disque final en multiples de 512 octets.</span><span class="sxs-lookup"><span data-stu-id="0e7ee-120">Final disk space cost in multiples of 512 bytes.</span></span>     |
| <span data-ttu-id="0e7ee-121">3</span><span class="sxs-lookup"><span data-stu-id="0e7ee-121">3</span></span>     | <span data-ttu-id="0e7ee-122">Coût de l’espace disque temporaire en multiples de 512 octets.</span><span class="sxs-lookup"><span data-stu-id="0e7ee-122">Temporary disk space cost in multiples of 512 bytes.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="0e7ee-123">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="0e7ee-123">Requirements</span></span>



| <span data-ttu-id="0e7ee-124">Condition requise</span><span class="sxs-lookup"><span data-stu-id="0e7ee-124">Requirement</span></span> | <span data-ttu-id="0e7ee-125">Valeur</span><span class="sxs-lookup"><span data-stu-id="0e7ee-125">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e7ee-126">Version</span><span class="sxs-lookup"><span data-stu-id="0e7ee-126">Version</span></span><br/> | <span data-ttu-id="0e7ee-127">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0e7ee-127">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="0e7ee-128">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="0e7ee-128">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="0e7ee-129">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="0e7ee-129">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="0e7ee-130">DLL</span><span class="sxs-lookup"><span data-stu-id="0e7ee-130">DLL</span></span><br/>     | <dl> <span data-ttu-id="0e7ee-131"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e7ee-131"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="0e7ee-132">IID</span><span class="sxs-lookup"><span data-stu-id="0e7ee-132">IID</span></span><br/>     | <span data-ttu-id="0e7ee-133">IID \_ ISession est défini en tant que 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="0e7ee-133">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




