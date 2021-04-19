---
description: La propriété UILevel de l’objet installer est une propriété en lecture-écriture qui indique le type d’interface utilisateur à utiliser lors de l’ouverture et du traitement des packages suivants dans l’espace de processus actuel.
ms.assetid: c89545b5-aeb7-4b05-94b0-d6e2a237152e
title: Installer. UILevel, propriété
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.UILevel
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: de6bda93b5607e00544a69c917a6a238b596c581
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106543947"
---
# <a name="installeruilevel-property"></a><span data-ttu-id="3b31a-103">Installer. UILevel, propriété</span><span class="sxs-lookup"><span data-stu-id="3b31a-103">Installer.UILevel property</span></span>

<span data-ttu-id="3b31a-104">La propriété **UILevel** de l’objet [**installer**](installer-object.md) est une propriété en lecture-écriture qui indique le type d’interface utilisateur à utiliser lors de l’ouverture et du traitement des packages suivants dans l’espace de processus actuel.</span><span class="sxs-lookup"><span data-stu-id="3b31a-104">The **UILevel** property of the [**Installer**](installer-object.md) object is a read-write property that indicates the type of user interface to be used when opening and processing subsequent packages within the current process space.</span></span>

<span data-ttu-id="3b31a-105">Cette propriété est en lecture/écriture.</span><span class="sxs-lookup"><span data-stu-id="3b31a-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b31a-106">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="3b31a-106">Syntax</span></span>


```JScript
propVal = Installer.UILevel
Installer.UILevel = propVal 
```



## <a name="property-value"></a><span data-ttu-id="3b31a-107">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="3b31a-107">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="3b31a-108">Notes</span><span class="sxs-lookup"><span data-stu-id="3b31a-108">Remarks</span></span>



| <span data-ttu-id="3b31a-109">Niveau de l’interface utilisateur</span><span class="sxs-lookup"><span data-stu-id="3b31a-109">User interface level</span></span>   | <span data-ttu-id="3b31a-110">Valeur</span><span class="sxs-lookup"><span data-stu-id="3b31a-110">Value</span></span> | <span data-ttu-id="3b31a-111">Description</span><span class="sxs-lookup"><span data-stu-id="3b31a-111">Description</span></span>                                                                                                                                                                                        |
|------------------------|-------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b31a-112">msiUILevelNoChange</span><span class="sxs-lookup"><span data-stu-id="3b31a-112">msiUILevelNoChange</span></span>     | <span data-ttu-id="3b31a-113">0</span><span class="sxs-lookup"><span data-stu-id="3b31a-113">0</span></span>     | <span data-ttu-id="3b31a-114">Ne modifie pas le niveau de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="3b31a-114">Does not change UI level.</span></span>                                                                                                                                                                          |
| <span data-ttu-id="3b31a-115">msiUILevelDefault</span><span class="sxs-lookup"><span data-stu-id="3b31a-115">msiUILevelDefault</span></span>      | <span data-ttu-id="3b31a-116">1</span><span class="sxs-lookup"><span data-stu-id="3b31a-116">1</span></span>     | <span data-ttu-id="3b31a-117">Utilise le niveau d’interface utilisateur par défaut.</span><span class="sxs-lookup"><span data-stu-id="3b31a-117">Uses default UI level.</span></span>                                                                                                                                                                             |
| <span data-ttu-id="3b31a-118">msiUILevelNone</span><span class="sxs-lookup"><span data-stu-id="3b31a-118">msiUILevelNone</span></span>         | <span data-ttu-id="3b31a-119">2</span><span class="sxs-lookup"><span data-stu-id="3b31a-119">2</span></span>     | <span data-ttu-id="3b31a-120">Installation sans assistance.</span><span class="sxs-lookup"><span data-stu-id="3b31a-120">Silent installation.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="3b31a-121">msiUILevelBasic</span><span class="sxs-lookup"><span data-stu-id="3b31a-121">msiUILevelBasic</span></span>        | <span data-ttu-id="3b31a-122">3</span><span class="sxs-lookup"><span data-stu-id="3b31a-122">3</span></span>     | <span data-ttu-id="3b31a-123">Progression et gestion des erreurs simples.</span><span class="sxs-lookup"><span data-stu-id="3b31a-123">Simple progress and error handling.</span></span>                                                                                                                                                                |
| <span data-ttu-id="3b31a-124">msiUILevelReduced</span><span class="sxs-lookup"><span data-stu-id="3b31a-124">msiUILevelReduced</span></span>      | <span data-ttu-id="3b31a-125">4</span><span class="sxs-lookup"><span data-stu-id="3b31a-125">4</span></span>     | <span data-ttu-id="3b31a-126">L’interface utilisateur créée et les boîtes de dialogue de l’Assistant ont été supprimées.</span><span class="sxs-lookup"><span data-stu-id="3b31a-126">Authored UI and wizard dialog boxes suppressed.</span></span>                                                                                                                                                    |
| <span data-ttu-id="3b31a-127">msiUILevelFull</span><span class="sxs-lookup"><span data-stu-id="3b31a-127">msiUILevelFull</span></span>         | <span data-ttu-id="3b31a-128">5</span><span class="sxs-lookup"><span data-stu-id="3b31a-128">5</span></span>     | <span data-ttu-id="3b31a-129">Interface utilisateur créée avec les assistants, la progression et les erreurs.</span><span class="sxs-lookup"><span data-stu-id="3b31a-129">Authored UI with wizards, progress, and errors.</span></span>                                                                                                                                                    |
| <span data-ttu-id="3b31a-130">msiUILevelHideCancel</span><span class="sxs-lookup"><span data-stu-id="3b31a-130">msiUILevelHideCancel</span></span>   | <span data-ttu-id="3b31a-131">32</span><span class="sxs-lookup"><span data-stu-id="3b31a-131">32</span></span>    | <span data-ttu-id="3b31a-132">En cas de combinaison avec la valeur msiUILevelBasic, le programme d’installation affiche des boîtes de dialogue de progression, mais n’affiche pas de bouton **Annuler** dans la boîte de dialogue pour empêcher les utilisateurs d’annuler l’installation.</span><span class="sxs-lookup"><span data-stu-id="3b31a-132">If combined with the msiUILevelBasic value, the installer shows progress dialog boxes but does not display a **Cancel** button on the dialog box to prevent users from canceling the installation.</span></span> |
| <span data-ttu-id="3b31a-133">msiUILevelProgressOnly</span><span class="sxs-lookup"><span data-stu-id="3b31a-133">msiUILevelProgressOnly</span></span> | <span data-ttu-id="3b31a-134">64</span><span class="sxs-lookup"><span data-stu-id="3b31a-134">64</span></span>    | <span data-ttu-id="3b31a-135">En cas de combinaison avec la valeur msiUILevelBasic, le programme d’installation affiche des boîtes de dialogue de progression, mais n’affiche pas de boîtes de dialogue modales ou de boîtes de dialogue d’erreur.</span><span class="sxs-lookup"><span data-stu-id="3b31a-135">If combined with the msiUILevelBasic value, the installer displays progress dialog boxes but does not display any modal dialog boxes or error dialog boxes.</span></span>                                        |
| <span data-ttu-id="3b31a-136">msiUILevelEndDialog</span><span class="sxs-lookup"><span data-stu-id="3b31a-136">msiUILevelEndDialog</span></span>    | <span data-ttu-id="3b31a-137">128</span><span class="sxs-lookup"><span data-stu-id="3b31a-137">128</span></span>   | <span data-ttu-id="3b31a-138">S’il est associé à une valeur ci-dessus, le programme d’installation affiche une boîte de dialogue modale à la fin d’une installation réussie ou en cas d’erreur.</span><span class="sxs-lookup"><span data-stu-id="3b31a-138">If combined with any above value, the installer displays a modal dialog box at the end of a successful installation or if there has been an error.</span></span> <span data-ttu-id="3b31a-139">Aucune boîte de dialogue ne s’affiche si l’utilisateur annule.</span><span class="sxs-lookup"><span data-stu-id="3b31a-139">No dialog box is displayed if the user cancels.</span></span> |



 

<span data-ttu-id="3b31a-140">Voir aussi [détermination du niveau d’interface utilisateur à partir d’une action personnalisée](determining-ui-level-from-a-custom-action.md).</span><span class="sxs-lookup"><span data-stu-id="3b31a-140">See also, [Determining UI Level from a Custom Action](determining-ui-level-from-a-custom-action.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3b31a-141">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="3b31a-141">Requirements</span></span>



| <span data-ttu-id="3b31a-142">Condition requise</span><span class="sxs-lookup"><span data-stu-id="3b31a-142">Requirement</span></span> | <span data-ttu-id="3b31a-143">Valeur</span><span class="sxs-lookup"><span data-stu-id="3b31a-143">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b31a-144">Version</span><span class="sxs-lookup"><span data-stu-id="3b31a-144">Version</span></span><br/> | <span data-ttu-id="3b31a-145">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="3b31a-145">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="3b31a-146">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="3b31a-146">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="3b31a-147">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="3b31a-147">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="3b31a-148">DLL</span><span class="sxs-lookup"><span data-stu-id="3b31a-148">DLL</span></span><br/>     | <dl> <span data-ttu-id="3b31a-149"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3b31a-149"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="3b31a-150">IID</span><span class="sxs-lookup"><span data-stu-id="3b31a-150">IID</span></span><br/>     | <span data-ttu-id="3b31a-151">IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="3b31a-151">IID\_IInstaller is defined as 000C1090-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                           |



 

 




