---
description: La méthode SetInstallLevel de l’objet session définit le niveau d’installation de l’installation actuelle sur une valeur spécifiée et recalcule les États SELECT et installed pour toutes les fonctionnalités de la table Feature.
ms.assetid: d47f8025-d484-42c7-9808-5ee590a4d200
title: Session. SetInstallLevel, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.SetInstallLevel
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: abb5ff5f7a528ff654787e9b2ee3d935abee57d6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106540076"
---
# <a name="sessionsetinstalllevel-method"></a><span data-ttu-id="d1cab-103">Session. SetInstallLevel, méthode</span><span class="sxs-lookup"><span data-stu-id="d1cab-103">Session.SetInstallLevel method</span></span>

<span data-ttu-id="d1cab-104">La méthode **SetInstallLevel** de l’objet [**session**](session-object.md) définit le niveau d’installation de l’installation actuelle sur une valeur spécifiée et recalcule les États SELECT et installed pour toutes les fonctionnalités de la table Feature.</span><span class="sxs-lookup"><span data-stu-id="d1cab-104">The **SetInstallLevel** method of the [**Session**](session-object.md) object sets the install level for the current installation to a specified value and recalculates the Select and Installed states for all features in the Feature table.</span></span> <span data-ttu-id="d1cab-105">Il définit également l’état d’action de chaque composant dans la [table des composants](component-table.md) en fonction du nouveau niveau.</span><span class="sxs-lookup"><span data-stu-id="d1cab-105">It also sets the Action state of each component in the [Component table](component-table.md) based on the new level.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1cab-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d1cab-106">Syntax</span></span>


```JScript
Session.SetInstallLevel(
  installLevel
)
```



## <a name="parameters"></a><span data-ttu-id="d1cab-107">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d1cab-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d1cab-108">*installLevel*</span><span class="sxs-lookup"><span data-stu-id="d1cab-108">*installLevel*</span></span> 
</dt> <dd>

<span data-ttu-id="d1cab-109">Nouveau niveau d’installation demandé requis.</span><span class="sxs-lookup"><span data-stu-id="d1cab-109">Required requested new install level.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d1cab-110">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d1cab-110">Return value</span></span>

<span data-ttu-id="d1cab-111">Cette méthode ne retourne pas de valeur.</span><span class="sxs-lookup"><span data-stu-id="d1cab-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d1cab-112">Notes</span><span class="sxs-lookup"><span data-stu-id="d1cab-112">Remarks</span></span>

<span data-ttu-id="d1cab-113">L' [action CostInitialize](costinitialize-action.md) doit être exécutée avant d’appeler **SetInstallLevel**.</span><span class="sxs-lookup"><span data-stu-id="d1cab-113">The [CostInitialize action](costinitialize-action.md) must be executed prior to calling **SetInstallLevel**.</span></span>

<span data-ttu-id="d1cab-114">Si 0 est passé pour le paramètre *installLevel* , le niveau d’installation actuel n’est pas modifié, mais toutes les fonctionnalités sont toujours mises à jour en fonction du niveau d’installation actuel.</span><span class="sxs-lookup"><span data-stu-id="d1cab-114">If 0 is passed for the *installLevel* parameter, the current install level is not changed, but all features are still updated based on the current install level.</span></span> <span data-ttu-id="d1cab-115">Par exemple, cette fonctionnalité peut être utilisée par le module Handler pour réinitialiser toutes les sélections à leur état initial par défaut à tout moment dans le processus de sélection de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="d1cab-115">For example, this functionality could be used by the Handler module to reset all selections back to their initial default states at any point in the UI selection process.</span></span>

<span data-ttu-id="d1cab-116">Si la méthode échoue, vous pouvez obtenir des informations d’erreur étendues à l’aide de la méthode [**LastErrorRecord**](installer-lasterrorrecord.md) .</span><span class="sxs-lookup"><span data-stu-id="d1cab-116">If the method fails, you can obtain extended error information by using the [**LastErrorRecord**](installer-lasterrorrecord.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1cab-117">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d1cab-117">Requirements</span></span>



| <span data-ttu-id="d1cab-118">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d1cab-118">Requirement</span></span> | <span data-ttu-id="d1cab-119">Valeur</span><span class="sxs-lookup"><span data-stu-id="d1cab-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1cab-120">Version</span><span class="sxs-lookup"><span data-stu-id="d1cab-120">Version</span></span><br/> | <span data-ttu-id="d1cab-121">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="d1cab-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d1cab-122">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="d1cab-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d1cab-123">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="d1cab-123">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="d1cab-124">DLL</span><span class="sxs-lookup"><span data-stu-id="d1cab-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="d1cab-125"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d1cab-125"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="d1cab-126">IID</span><span class="sxs-lookup"><span data-stu-id="d1cab-126">IID</span></span><br/>     | <span data-ttu-id="d1cab-127">IID \_ ISession est défini en tant que 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="d1cab-127">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 




