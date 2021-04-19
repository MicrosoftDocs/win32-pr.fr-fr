---
description: L’action RemoveEnvironmentStrings modifie les valeurs des variables d’environnement.
ms.assetid: 024a734a-2e40-45b6-9dec-73def89a417f
title: Action RemoveEnvironmentStrings
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c958f2095d2b8562bbd7518ef691634186a9128
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106538226"
---
# <a name="removeenvironmentstrings-action"></a><span data-ttu-id="6dfb7-103">Action RemoveEnvironmentStrings</span><span class="sxs-lookup"><span data-stu-id="6dfb7-103">RemoveEnvironmentStrings Action</span></span>

<span data-ttu-id="6dfb7-104">L’action RemoveEnvironmentStrings modifie les valeurs des variables d’environnement.</span><span class="sxs-lookup"><span data-stu-id="6dfb7-104">The RemoveEnvironmentStrings action modifies the values of environment variables.</span></span>

<span data-ttu-id="6dfb7-105">Notez que les variables d’environnement ne changent pas pour l’installation en cours lors de l’exécution de l’action [WriteEnvironmentStrings](writeenvironmentstrings-action.md) ou RemoveEnvironmentStrings.</span><span class="sxs-lookup"><span data-stu-id="6dfb7-105">Note that environment variables do not change for the installation in progress when either the [WriteEnvironmentStrings action](writeenvironmentstrings-action.md) or RemoveEnvironmentStrings action are run.</span></span> <span data-ttu-id="6dfb7-106">Sur Windows 2000, ces informations sont stockées dans le registre et un message est envoyé pour notifier le système de modifications une fois l’installation terminée.</span><span class="sxs-lookup"><span data-stu-id="6dfb7-106">On Windows 2000, this information is stored in the registry and a message is sent to notify the system of changes when the installation completes.</span></span> <span data-ttu-id="6dfb7-107">Un nouveau processus, ou un autre processus qui vérifie ces messages, utilisera les nouvelles variables d’environnement.</span><span class="sxs-lookup"><span data-stu-id="6dfb7-107">A new process, or another process that checks for these messages, will use the new environment variables.</span></span>

<span data-ttu-id="6dfb7-108">Le programme d’installation exécute l' [action WriteEnvironmentStrings](writeenvironmentstrings-action.md) uniquement lors de l’installation ou de la réinstallation d’un composant, et exécute l’action RemoveEnvironmentStrings uniquement pendant la suppression d’un composant.</span><span class="sxs-lookup"><span data-stu-id="6dfb7-108">The installer runs the [WriteEnvironmentStrings action](writeenvironmentstrings-action.md) only during the installation or reinstallation of a component, and runs the RemoveEnvironmentStrings action only during the removal of a component.</span></span>

<span data-ttu-id="6dfb7-109">Les valeurs sont écrites ou supprimées en fonction de la sélection d’actions et de modificateurs principaux.</span><span class="sxs-lookup"><span data-stu-id="6dfb7-109">Values are written or removed based on the selection of primary actions and modifiers.</span></span> <span data-ttu-id="6dfb7-110">Celles-ci sont décrites dans la section messages ActionData suivants.</span><span class="sxs-lookup"><span data-stu-id="6dfb7-110">These are described in the following ActionData Messages section.</span></span> <span data-ttu-id="6dfb7-111">Notez que, selon l’action spécifiée, WriteEnvironmentStrings peut supprimer des variables et RemoveEnvironmentStrings peut les ajouter en fonction de la création de la [table d’environnement](environment-table.md).</span><span class="sxs-lookup"><span data-stu-id="6dfb7-111">Note that depending upon the action specified, WriteEnvironmentStrings may remove variables, and RemoveEnvironmentStrings may add them based on the authoring of the [Environment table](environment-table.md).</span></span>

## <a name="sequence-restrictions"></a><span data-ttu-id="6dfb7-112">Restrictions de séquence</span><span class="sxs-lookup"><span data-stu-id="6dfb7-112">Sequence Restrictions</span></span>

<span data-ttu-id="6dfb7-113">L' [action InstallValidate](installvalidate-action.md) doit être exécutée avant l’action RemoveEnvironmentStrings.</span><span class="sxs-lookup"><span data-stu-id="6dfb7-113">The [InstallValidate action](installvalidate-action.md) must be executed before the RemoveEnvironmentStrings action.</span></span> <span data-ttu-id="6dfb7-114">Étant donné que les actions WriteEnvironmentStrings et RemoveEnvironmentStrings ne sont jamais appliquées au cours de l’installation ou de la suppression d’un composant, leur séquence relative n’est pas restreinte.</span><span class="sxs-lookup"><span data-stu-id="6dfb7-114">Because the WriteEnvironmentStrings action and RemoveEnvironmentStrings action are never both applied during the installation or removal of a component, their relative sequence is not restricted.</span></span>

## <a name="actiondata-messages"></a><span data-ttu-id="6dfb7-115">Messages ActionData</span><span class="sxs-lookup"><span data-stu-id="6dfb7-115">ActionData Messages</span></span>



| <span data-ttu-id="6dfb7-116">Champ</span><span class="sxs-lookup"><span data-stu-id="6dfb7-116">Field</span></span> | <span data-ttu-id="6dfb7-117">Description des données d’action</span><span class="sxs-lookup"><span data-stu-id="6dfb7-117">Description of action data</span></span>                                                                                                                                                                                                |
|-------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6dfb7-118">\[1\]</span><span class="sxs-lookup"><span data-stu-id="6dfb7-118">\[1\]</span></span> | <span data-ttu-id="6dfb7-119">Nom de la variable d’environnement à modifier.</span><span class="sxs-lookup"><span data-stu-id="6dfb7-119">Name of the environment variable to modify.</span></span>                                                                                                                                                                               |
| <span data-ttu-id="6dfb7-120">\[2\]</span><span class="sxs-lookup"><span data-stu-id="6dfb7-120">\[2\]</span></span> | <span data-ttu-id="6dfb7-121">Valeur de la variable d’environnement.</span><span class="sxs-lookup"><span data-stu-id="6dfb7-121">The environment variable value.</span></span>                                                                                                                                                                                           |
| <span data-ttu-id="6dfb7-122">\[3\]</span><span class="sxs-lookup"><span data-stu-id="6dfb7-122">\[3\]</span></span> | <span data-ttu-id="6dfb7-123">Il s’agit d’un champ d’indicateurs binaires qui spécifient l’action à exécuter.</span><span class="sxs-lookup"><span data-stu-id="6dfb7-123">This is a field of bit flags that specify the action to be performed.</span></span> <span data-ttu-id="6dfb7-124">N’incluez qu’un seul bit pour une action principale.</span><span class="sxs-lookup"><span data-stu-id="6dfb7-124">Include only one bit for a primary action.</span></span> <span data-ttu-id="6dfb7-125">Il peut y avoir plusieurs bits de modificateur inclus dans ce champ.</span><span class="sxs-lookup"><span data-stu-id="6dfb7-125">There may be more than one modifier bit included in this field.</span></span> <span data-ttu-id="6dfb7-126">Consultez les descriptions des indicateurs de bits suivantes.</span><span class="sxs-lookup"><span data-stu-id="6dfb7-126">See the following bit flag descriptions.</span></span> |



 



| <span data-ttu-id="6dfb7-127">Valeur en bits</span><span class="sxs-lookup"><span data-stu-id="6dfb7-127">Bit value</span></span> | <span data-ttu-id="6dfb7-128">Description des actions principales</span><span class="sxs-lookup"><span data-stu-id="6dfb7-128">Description of primary actions</span></span>                                                                                                                                                                                      |
|-----------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6dfb7-129">0x1</span><span class="sxs-lookup"><span data-stu-id="6dfb7-129">0x1</span></span>       | <span data-ttu-id="6dfb7-130">Prêts ?</span><span class="sxs-lookup"><span data-stu-id="6dfb7-130">Set.</span></span> <span data-ttu-id="6dfb7-131">Définit la valeur de la variable d’environnement dans tous les cas.</span><span class="sxs-lookup"><span data-stu-id="6dfb7-131">Sets the value of the environment variable in all cases.</span></span><br/> <span data-ttu-id="6dfb7-132">Si ce bit est combiné avec un bit de modificateur d’ajout ou de préfixe, l’action ajoute la valeur à toute valeur existante dans la variable.</span><span class="sxs-lookup"><span data-stu-id="6dfb7-132">If this bit is combined with an Append or Prefix modifier bit, the action adds the value to any existing value in the variable.</span></span><br/> |
| <span data-ttu-id="6dfb7-133">0x2</span><span class="sxs-lookup"><span data-stu-id="6dfb7-133">0x2</span></span>       | <span data-ttu-id="6dfb7-134">Prêts ?</span><span class="sxs-lookup"><span data-stu-id="6dfb7-134">Set.</span></span> <span data-ttu-id="6dfb7-135">Définit la valeur si la variable est absente.</span><span class="sxs-lookup"><span data-stu-id="6dfb7-135">Sets the value if the variable is absent.</span></span><br/> <span data-ttu-id="6dfb7-136">Si ce bit est combiné avec un bit de modificateur d’ajout ou de préfixe, l’action ajoute la valeur à toute valeur existante dans la variable.</span><span class="sxs-lookup"><span data-stu-id="6dfb7-136">If this bit is combined with an Append or Prefix modifier bit, the action adds the value to any existing value in the variable.</span></span><br/>                |
| <span data-ttu-id="6dfb7-137">0x4</span><span class="sxs-lookup"><span data-stu-id="6dfb7-137">0x4</span></span>       | <span data-ttu-id="6dfb7-138">Supprimer.</span><span class="sxs-lookup"><span data-stu-id="6dfb7-138">Remove.</span></span> <span data-ttu-id="6dfb7-139">Supprime la valeur de la variable.</span><span class="sxs-lookup"><span data-stu-id="6dfb7-139">Removes the value from the variable.</span></span><br/> <span data-ttu-id="6dfb7-140">Si ce bit est combiné avec un bit de modificateur d’ajout ou de préfixe, la valeur est supprimée de la chaîne existante, si la valeur existe.</span><span class="sxs-lookup"><span data-stu-id="6dfb7-140">If this bit is combined with an Append or Prefix modifier bit, the value is removed from the existing string, if the value exists.</span></span><br/>               |



 



| <span data-ttu-id="6dfb7-141">Valeur en bits</span><span class="sxs-lookup"><span data-stu-id="6dfb7-141">Bit value</span></span>  | <span data-ttu-id="6dfb7-142">Description du modificateur</span><span class="sxs-lookup"><span data-stu-id="6dfb7-142">Description of modifier</span></span>                                                                                                                                                              |
|------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6dfb7-143">0x20000000</span><span class="sxs-lookup"><span data-stu-id="6dfb7-143">0x20000000</span></span> | <span data-ttu-id="6dfb7-144">Si ce bit est défini, les actions sont appliquées aux variables d’environnement de l’ordinateur.</span><span class="sxs-lookup"><span data-stu-id="6dfb7-144">If this bit is set, actions are applied to the machine environment variables.</span></span><br/> <span data-ttu-id="6dfb7-145">Si ce bit n’est pas défini, des actions sont appliquées aux variables d’environnement de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="6dfb7-145">If this bit is not set, actions are applied to the user's environment variables.</span></span><br/> |
| <span data-ttu-id="6dfb7-146">0x40000000</span><span class="sxs-lookup"><span data-stu-id="6dfb7-146">0x40000000</span></span> | <span data-ttu-id="6dfb7-147">Ajouter :</span><span class="sxs-lookup"><span data-stu-id="6dfb7-147">Append.</span></span> <span data-ttu-id="6dfb7-148">Ce bit est facultatif.</span><span class="sxs-lookup"><span data-stu-id="6dfb7-148">This bit is optional.</span></span> <span data-ttu-id="6dfb7-149">Ne définissez pas à la fois les modificateurs Append et prefix.</span><span class="sxs-lookup"><span data-stu-id="6dfb7-149">Do not set both the Append and Prefix modifiers.</span></span><br/>                                                                                            |
| <span data-ttu-id="6dfb7-150">0x80000000</span><span class="sxs-lookup"><span data-stu-id="6dfb7-150">0x80000000</span></span> | <span data-ttu-id="6dfb7-151">Céder.</span><span class="sxs-lookup"><span data-stu-id="6dfb7-151">Prefix.</span></span> <span data-ttu-id="6dfb7-152">Ce bit est facultatif.</span><span class="sxs-lookup"><span data-stu-id="6dfb7-152">This bit is optional.</span></span> <span data-ttu-id="6dfb7-153">Ne définissez pas à la fois les modificateurs Append et prefix.</span><span class="sxs-lookup"><span data-stu-id="6dfb7-153">Do not set both the Append and Prefix modifiers.</span></span><br/>                                                                                            |



 

 

 




