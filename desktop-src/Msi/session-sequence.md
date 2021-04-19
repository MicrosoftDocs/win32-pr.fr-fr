---
description: La méthode Sequence de l’objet session ouvre une requête sur la table spécifiée, en classant les actions par les nombres de la colonne Sequence.
ms.assetid: cde735b0-0b97-4c4f-adfc-f0321aafb012
title: Session. Sequence, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.Sequence
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 18708b79bdce73b29f46b4d62a15ceb8003d9c9b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525646"
---
# <a name="sessionsequence-method"></a><span data-ttu-id="fe3fe-103">Session. Sequence, méthode</span><span class="sxs-lookup"><span data-stu-id="fe3fe-103">Session.Sequence method</span></span>

<span data-ttu-id="fe3fe-104">La méthode **Sequence** de l’objet [**session**](session-object.md) ouvre une requête sur la table spécifiée, en classant les actions par les nombres de la colonne Sequence.</span><span class="sxs-lookup"><span data-stu-id="fe3fe-104">The **Sequence** method of the [**Session**](session-object.md) object opens a query on the specified table, ordering the actions by the numbers in the Sequence column.</span></span> <span data-ttu-id="fe3fe-105">Pour chaque ligne extraite, la méthode d' [**action**](session-doaction.md) est appelée, à condition que toute expression de condition fournie ne corresponde pas à false.</span><span class="sxs-lookup"><span data-stu-id="fe3fe-105">For each row fetched, the [**DoAction**](session-doaction.md) method is called, provided that any supplied condition expression does not evaluate to False.</span></span> <span data-ttu-id="fe3fe-106">Retourne une énumération msiDoActionStatusEnum, comme décrit dans la méthode d' [**action**](session-doaction.md) .</span><span class="sxs-lookup"><span data-stu-id="fe3fe-106">Returns an enumeration msiDoActionStatusEnum, as described in the [**DoAction**](session-doaction.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe3fe-107">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="fe3fe-107">Syntax</span></span>


```JScript
Session.Sequence(
  table
)
```



## <a name="parameters"></a><span data-ttu-id="fe3fe-108">Paramètres</span><span class="sxs-lookup"><span data-stu-id="fe3fe-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fe3fe-109">*table*</span><span class="sxs-lookup"><span data-stu-id="fe3fe-109">*table*</span></span> 
</dt> <dd>

<span data-ttu-id="fe3fe-110">Nom de chaîne requis de la table à utiliser pour le séquencement.</span><span class="sxs-lookup"><span data-stu-id="fe3fe-110">Required string name of the table to use for sequencing.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fe3fe-111">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="fe3fe-111">Return value</span></span>

<span data-ttu-id="fe3fe-112">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="fe3fe-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe3fe-113">Notes</span><span class="sxs-lookup"><span data-stu-id="fe3fe-113">Remarks</span></span>

<span data-ttu-id="fe3fe-114">Cette méthode est normalement appelée en interne par des actions de niveau supérieur.</span><span class="sxs-lookup"><span data-stu-id="fe3fe-114">This method is normally called internally by top-level actions.</span></span>

<span data-ttu-id="fe3fe-115">Une séquence d’action contenant des actions qui mettent à jour le système, telles que les actions [InstallFiles](installfiles-action.md) et [WriteRegistryValues](writeregistryvalues-action.md) , ne peut pas être exécutée en appelant la méthode **Sequence** .</span><span class="sxs-lookup"><span data-stu-id="fe3fe-115">An action sequence containing actions that update the system, such as the [InstallFiles](installfiles-action.md) and [WriteRegistryValues](writeregistryvalues-action.md) actions, cannot be run by calling the **Sequence** method.</span></span> <span data-ttu-id="fe3fe-116">L’exception à cette règle est si la méthode de **séquence** est appelée à partir d’une action personnalisée qui est planifiée dans la [table InstallExecuteSequence](installexecutesequence-table.md) entre les actions [InstallInitialize](installinitialize-action.md) et [InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="fe3fe-116">The exception to this rule is if the **Sequence** method is called from a custom action that is scheduled in the [InstallExecuteSequence table](installexecutesequence-table.md) between the [InstallInitialize](installinitialize-action.md) and [InstallFinalize actions](installfinalize-action.md).</span></span> <span data-ttu-id="fe3fe-117">Les actions qui ne mettent pas à jour le système, telles que [AppSearch](appsearch-action.md) ou [CostInitialize](costinitialize-action.md), peuvent être appelées.</span><span class="sxs-lookup"><span data-stu-id="fe3fe-117">Actions that do not update the system, such as [AppSearch](appsearch-action.md) or [CostInitialize](costinitialize-action.md), can be called.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe3fe-118">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="fe3fe-118">Requirements</span></span>



| <span data-ttu-id="fe3fe-119">Condition requise</span><span class="sxs-lookup"><span data-stu-id="fe3fe-119">Requirement</span></span> | <span data-ttu-id="fe3fe-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="fe3fe-120">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe3fe-121">Version</span><span class="sxs-lookup"><span data-stu-id="fe3fe-121">Version</span></span><br/> | <span data-ttu-id="fe3fe-122">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="fe3fe-122">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="fe3fe-123">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="fe3fe-123">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="fe3fe-124">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="fe3fe-124">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="fe3fe-125">DLL</span><span class="sxs-lookup"><span data-stu-id="fe3fe-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="fe3fe-126"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fe3fe-126"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="fe3fe-127">IID</span><span class="sxs-lookup"><span data-stu-id="fe3fe-127">IID</span></span><br/>     | <span data-ttu-id="fe3fe-128">IID \_ ISession est défini en tant que 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="fe3fe-128">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




