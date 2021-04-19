---
description: La propriété VerifyDiskSpace est une propriété en lecture seule.
ms.assetid: 62f11f71-00b0-4e04-8c45-d6d670238886
title: Session. VerifyDiskSpace, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.VerifyDiskSpace
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: a73f2b6f846cb918d5eb10689388a174950c0edc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106531117"
---
# <a name="sessionverifydiskspace-property"></a><span data-ttu-id="09bb3-103">Session. VerifyDiskSpace, propriété</span><span class="sxs-lookup"><span data-stu-id="09bb3-103">Session.VerifyDiskSpace property</span></span>

<span data-ttu-id="09bb3-104">La propriété **VerifyDiskSpace** est une propriété en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="09bb3-104">The **VerifyDiskSpace** property is a read-only property.</span></span> <span data-ttu-id="09bb3-105">Elle retourne true si l’espace disque disponible est suffisant et false si le disque est plein.</span><span class="sxs-lookup"><span data-stu-id="09bb3-105">It returns true if enough disk space exists and false if the disk is full.</span></span> <span data-ttu-id="09bb3-106">Étant donné que cette propriété utilise les informations collectées par les actions d’évaluation, **VerifyDiskSpace** doit être appelé uniquement après l’action [CostInitialize](costinitialize-action.md), l’action [FileCost](filecost-action.md)et l' [action CostFinalize](costfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="09bb3-106">Because this property uses information gathered by the costing actions, **VerifyDiskSpace** should only be called after the [CostInitialize action](costinitialize-action.md), [FileCost action](filecost-action.md), and [CostFinalize action](costfinalize-action.md).</span></span>

<span data-ttu-id="09bb3-107">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="09bb3-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="09bb3-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="09bb3-108">Syntax</span></span>


```JScript
propVal = Session.VerifyDiskSpace
```



## <a name="property-value"></a><span data-ttu-id="09bb3-109">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="09bb3-109">Property value</span></span>

## <a name="requirements"></a><span data-ttu-id="09bb3-110">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="09bb3-110">Requirements</span></span>



| <span data-ttu-id="09bb3-111">Condition requise</span><span class="sxs-lookup"><span data-stu-id="09bb3-111">Requirement</span></span> | <span data-ttu-id="09bb3-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="09bb3-112">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09bb3-113">Version</span><span class="sxs-lookup"><span data-stu-id="09bb3-113">Version</span></span><br/> | <span data-ttu-id="09bb3-114">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="09bb3-114">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="09bb3-115">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="09bb3-115">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="09bb3-116">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="09bb3-116">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="09bb3-117">DLL</span><span class="sxs-lookup"><span data-stu-id="09bb3-117">DLL</span></span><br/>     | <dl> <span data-ttu-id="09bb3-118"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09bb3-118"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="09bb3-119">IID</span><span class="sxs-lookup"><span data-stu-id="09bb3-119">IID</span></span><br/>     | <span data-ttu-id="09bb3-120">IID \_ ISession est défini en tant que 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="09bb3-120">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




