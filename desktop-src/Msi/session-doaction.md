---
description: La méthode de script de l’objet session exécute la fonction d’action correspondant au nom fourni.
ms.assetid: 6cff1cf1-1c8f-4c43-a687-e927e8573e55
title: Session. subaction, méthode (photoacquire. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.DoAction
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3084cfd51e7efbcfbfbc3cbcf2c9be21d8373d21
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525293"
---
# <a name="sessiondoaction-method"></a><span data-ttu-id="16791-103">Session. subaction, méthode</span><span class="sxs-lookup"><span data-stu-id="16791-103">Session.DoAction method</span></span>

<span data-ttu-id="16791-104">La **méthode de script de** l’objet [**session**](session-object.md) exécute la fonction d’action correspondant au nom fourni.</span><span class="sxs-lookup"><span data-stu-id="16791-104">The **DoAction** method of the [**Session**](session-object.md) object executes the action function corresponding to the name supplied.</span></span> <span data-ttu-id="16791-105">Si un nom d’action null est fourni, le moteur utilise la valeur majuscule de la [propriété action](action.md) comme action à exécuter.</span><span class="sxs-lookup"><span data-stu-id="16791-105">If a Null action name is supplied, the engine uses the uppercase value of the [ACTION property](action.md) as the action to perform.</span></span> <span data-ttu-id="16791-106">Si aucune valeur de propriété n’est définie, l’action par défaut est effectuée, actuellement définie en tant qu’installation.</span><span class="sxs-lookup"><span data-stu-id="16791-106">If no property value is defined, the default action is performed, currently defined as INSTALL.</span></span> <span data-ttu-id="16791-107">Cette méthode retourne une énumération entière.</span><span class="sxs-lookup"><span data-stu-id="16791-107">This method returns an integer enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="16791-108">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="16791-108">Syntax</span></span>


```JScript
Session.DoAction(
  action
)
```



## <a name="parameters"></a><span data-ttu-id="16791-109">Paramètres</span><span class="sxs-lookup"><span data-stu-id="16791-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16791-110">*action*</span><span class="sxs-lookup"><span data-stu-id="16791-110">*action*</span></span> 
</dt> <dd>

<span data-ttu-id="16791-111">Nom de chaîne obligatoire de l’action à exécuter.</span><span class="sxs-lookup"><span data-stu-id="16791-111">Required string name of the action to execute.</span></span> <span data-ttu-id="16791-112">Respecte la casse.</span><span class="sxs-lookup"><span data-stu-id="16791-112">Case-sensitive.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16791-113">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="16791-113">Return value</span></span>

<span data-ttu-id="16791-114">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="16791-114">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="16791-115">Notes</span><span class="sxs-lookup"><span data-stu-id="16791-115">Remarks</span></span>

<span data-ttu-id="16791-116">Les actions qui mettent à jour le système, telles que les actions [InstallFiles](installfiles-action.md) et [WriteRegistryValues](writeregistryvalues-action.md) , ne peuvent pas être exécutées en appelant la méthode d' **action** .</span><span class="sxs-lookup"><span data-stu-id="16791-116">Actions that update the system, such as the [InstallFiles](installfiles-action.md) and [WriteRegistryValues](writeregistryvalues-action.md) actions, cannot be run by calling the **DoAction** method.</span></span> <span data-ttu-id="16791-117">L’exception à cette règle est si la méthode d' **action** est appelée à partir d’une action personnalisée qui est planifiée dans la [table InstallExecuteSequence](installexecutesequence-table.md) entre les actions [InstallInitialize](installinitialize-action.md) et [InstallFinalize](installfinalize-action.md).</span><span class="sxs-lookup"><span data-stu-id="16791-117">The exception to this rule is if the **DoAction** method is called from a custom action that is scheduled in the [InstallExecuteSequence table](installexecutesequence-table.md) between the [InstallInitialize](installinitialize-action.md) and [InstallFinalize actions](installfinalize-action.md).</span></span> <span data-ttu-id="16791-118">Les actions qui ne mettent pas à jour le système, telles que [AppSearch](appsearch-action.md) ou [CostInitialize](costinitialize-action.md), peuvent être appelées.</span><span class="sxs-lookup"><span data-stu-id="16791-118">Actions that do not update the system, such as [AppSearch](appsearch-action.md) or [CostInitialize](costinitialize-action.md), can be called.</span></span>

## <a name="requirements"></a><span data-ttu-id="16791-119">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="16791-119">Requirements</span></span>



| <span data-ttu-id="16791-120">Condition requise</span><span class="sxs-lookup"><span data-stu-id="16791-120">Requirement</span></span> | <span data-ttu-id="16791-121">Valeur</span><span class="sxs-lookup"><span data-stu-id="16791-121">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="16791-122">Version</span><span class="sxs-lookup"><span data-stu-id="16791-122">Version</span></span><br/> | <span data-ttu-id="16791-123">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="16791-123">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="16791-124">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="16791-124">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="16791-125">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="16791-125">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="16791-126">En-tête</span><span class="sxs-lookup"><span data-stu-id="16791-126">Header</span></span><br/>  | <dl> <span data-ttu-id="16791-127"><dt>Photoacquire. h</dt></span><span class="sxs-lookup"><span data-stu-id="16791-127"><dt>Photoacquire.h</dt></span></span> </dl>                                                                                                                                                               |
| <span data-ttu-id="16791-128">DLL</span><span class="sxs-lookup"><span data-stu-id="16791-128">DLL</span></span><br/>     | <dl> <span data-ttu-id="16791-129"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16791-129"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="16791-130">IID</span><span class="sxs-lookup"><span data-stu-id="16791-130">IID</span></span><br/>     | <span data-ttu-id="16791-131">IID \_ ISession est défini en tant que 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="16791-131">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




