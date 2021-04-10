---
description: Les développeurs de packages de Windows Installer peuvent choisir d’utiliser une action personnalisée type 23 quand les actions standard sont insuffisantes pour exécuter l’installation.
ms.assetid: 8219f157-585d-4733-8e10-c05813b398ba
title: Type d’action personnalisé 23
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 05576c44ab634dc117501a89e6b86594f5483458
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103869253"
---
# <a name="custom-action-type-23"></a><span data-ttu-id="7c80c-103">Type d’action personnalisé 23</span><span class="sxs-lookup"><span data-stu-id="7c80c-103">Custom Action Type 23</span></span>

<span data-ttu-id="7c80c-104">Le type d’action personnalisé 23 est utilisé avec les installations simultanées.</span><span class="sxs-lookup"><span data-stu-id="7c80c-104">The Custom Action Type 23 is used with concurrent installations.</span></span> <span data-ttu-id="7c80c-105">Les installations simultanées ne sont pas recommandées pour l’installation d’applications destinées à être communiquées au public.</span><span class="sxs-lookup"><span data-stu-id="7c80c-105">Concurrent installations are not recommended for the installation of applications intended for release to the public.</span></span> <span data-ttu-id="7c80c-106">Pour plus d’informations sur les installations simultanées, consultez [installations simultanées](concurrent-installations.md).</span><span class="sxs-lookup"><span data-stu-id="7c80c-106">For information about concurrent installations please see [Concurrent Installations](concurrent-installations.md).</span></span>

<span data-ttu-id="7c80c-107">Cette action personnalisée installe un autre package d’installation qui se trouve dans l’arborescence source de l’application.</span><span class="sxs-lookup"><span data-stu-id="7c80c-107">This custom action installs another installer package that resides in the application's source tree.</span></span>

## <a name="source"></a><span data-ttu-id="7c80c-108">Source</span><span class="sxs-lookup"><span data-stu-id="7c80c-108">Source</span></span>

<span data-ttu-id="7c80c-109">L’emplacement du package d’installation simultané est spécifié par rapport à la racine de l’emplacement source indiqué dans le champ source de la [table CustomAction](customaction-table.md).</span><span class="sxs-lookup"><span data-stu-id="7c80c-109">The location of the concurrent installation package is specified relative to the root of the source location shown in the Source field of the [CustomAction table](customaction-table.md).</span></span>

## <a name="numeric-type"></a><span data-ttu-id="7c80c-110">Type numérique</span><span class="sxs-lookup"><span data-stu-id="7c80c-110">Numeric Type</span></span>



| <span data-ttu-id="7c80c-111">Nom de type</span><span class="sxs-lookup"><span data-stu-id="7c80c-111">Type name</span></span>                                                      | <span data-ttu-id="7c80c-112">Valeur</span><span class="sxs-lookup"><span data-stu-id="7c80c-112">Value</span></span> |
|----------------------------------------------------------------|-------|
| <span data-ttu-id="7c80c-113">msidbCustomActionTypeInstall + msidbCustomActionTypeSourceFile</span><span class="sxs-lookup"><span data-stu-id="7c80c-113">msidbCustomActionTypeInstall + msidbCustomActionTypeSourceFile</span></span> | <span data-ttu-id="7c80c-114">23</span><span class="sxs-lookup"><span data-stu-id="7c80c-114">23</span></span>    |



 

## <a name="target"></a><span data-ttu-id="7c80c-115">Cible</span><span class="sxs-lookup"><span data-stu-id="7c80c-115">Target</span></span>

<span data-ttu-id="7c80c-116">Le champ cible de la [table CustomAction](customaction-table.md) contient les paramètres de propriété qui doivent être passés à l’installation simultanée.</span><span class="sxs-lookup"><span data-stu-id="7c80c-116">The Target field of the [CustomAction table](customaction-table.md) contains property settings that are to be passed to the concurrent installation.</span></span> <span data-ttu-id="7c80c-117">Ces paramètres de propriété peuvent spécifier des fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="7c80c-117">These property settings can specify features.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="7c80c-118">Options de traitement des retours</span><span class="sxs-lookup"><span data-stu-id="7c80c-118">Return Processing Options</span></span>

<span data-ttu-id="7c80c-119">La session d’installation simultanée s’exécute en tant que thread distinct dans le processus en cours.</span><span class="sxs-lookup"><span data-stu-id="7c80c-119">The concurrent installation session runs as a separate thread in the current process.</span></span> <span data-ttu-id="7c80c-120">Une installation simultanée ne peut pas s’exécuter de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="7c80c-120">A concurrent installation cannot run asynchronously.</span></span>

<span data-ttu-id="7c80c-121">Pour plus d’informations, consultez [options de traitement des retours d’actions personnalisées](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="7c80c-121">For more information, see [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="7c80c-122">Options de planification de l’exécution</span><span class="sxs-lookup"><span data-stu-id="7c80c-122">Execution Scheduling Options</span></span>

<span data-ttu-id="7c80c-123">Des indicateurs d’options sont disponibles pour contrôler l’exécution multiple potentielle des actions personnalisées.</span><span class="sxs-lookup"><span data-stu-id="7c80c-123">Options flags are available to control the potential multiple execution of custom actions.</span></span> <span data-ttu-id="7c80c-124">Pour plus d’informations, consultez [options de planification de l’exécution des actions personnalisées](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="7c80c-124">For more information, see [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="7c80c-125">In-Script les options d’exécution</span><span class="sxs-lookup"><span data-stu-id="7c80c-125">In-Script Execution Options</span></span>

<span data-ttu-id="7c80c-126">Non utilisé.</span><span class="sxs-lookup"><span data-stu-id="7c80c-126">Not used.</span></span>

## <a name="return-values"></a><span data-ttu-id="7c80c-127">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="7c80c-127">Return Values</span></span>

<span data-ttu-id="7c80c-128">L’état de retour de la sortie de l’utilisateur, de l’échec, de l’interruption ou de la réussite d’une installation simultanée est traité de la même façon que toute autre action.</span><span class="sxs-lookup"><span data-stu-id="7c80c-128">The return status of user exit, failure, suspend, or success from a concurrent installation is processed in the same way as any other action.</span></span> <span data-ttu-id="7c80c-129">Notez toutefois que Windows Installer traduit les valeurs de retour de toutes les actions quand il écrit la valeur de retour dans le fichier journal.</span><span class="sxs-lookup"><span data-stu-id="7c80c-129">Note however, that Windows Installer translates the return values from all actions when it writes the return value into the log file.</span></span> <span data-ttu-id="7c80c-130">Par exemple, si la valeur de retour de l’action apparaît comme 1 dans le fichier journal, cela signifie que l’action a retourné une erreur de \_ réussite.</span><span class="sxs-lookup"><span data-stu-id="7c80c-130">For example, if the action return value appears as 1 in the log file, this means that the action returned ERROR\_SUCCESS.</span></span> <span data-ttu-id="7c80c-131">Pour plus d’informations, consultez [journalisation des valeurs de retour d’action](logging-of-action-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="7c80c-131">For more information, see [Logging of Action Return Values](logging-of-action-return-values.md).</span></span>

<span data-ttu-id="7c80c-132">Notez que, si une installation simultanée a une **msidbCustomActionTypeContinue** définie, un retour de l’erreur d’installation de USEREXIT, une erreur d’installation de \_ \_ \_ \_ redémarrage, une erreur d' \_ installation de \_ redémarrage \_ maintenant ou une erreur de \_ redémarrage de la réussite \_ \_ requise est traitée comme une erreur de \_ réussite.</span><span class="sxs-lookup"><span data-stu-id="7c80c-132">Note that if a concurrent installation has **msidbCustomActionTypeContinue** set, then a return of ERROR\_INSTALL\_USEREXIT, ERROR\_INSTALL\_REBOOT, ERROR\_INSTALL\_REBOOT\_NOW, or ERROR\_SUCCESS\_REBOOT\_REQUIRED is treated as ERROR\_SUCCESS.</span></span> <span data-ttu-id="7c80c-133">Cela signifie que si vous définissez **msidbCustomActionTypeContinue** et que votre installation simultanée requiert un redémarrage, la nécessité du redémarrage sera ignorée.</span><span class="sxs-lookup"><span data-stu-id="7c80c-133">This means that if you set **msidbCustomActionTypeContinue** and your concurrent installation requires a restart, the requirement for the restart will be ignored.</span></span> <span data-ttu-id="7c80c-134">En outre, le code d’erreur de l’action personnalisée d’installation simultanée est ignoré.</span><span class="sxs-lookup"><span data-stu-id="7c80c-134">Additionally, the error code from the concurrent installation custom action will be ignored.</span></span>

<span data-ttu-id="7c80c-135">Si **msidbCustomActionTypeContinue** n’est pas défini, les codes de retour suivants plus la réussite de l’erreur \_ sont traités comme des succès et ont les significations suivantes.</span><span class="sxs-lookup"><span data-stu-id="7c80c-135">If **msidbCustomActionTypeContinue** is not set, the following return codes plus ERROR\_SUCCESS are treated as success and have the following meanings.</span></span> <span data-ttu-id="7c80c-136">Les autres codes de retour sont traités comme des échecs.</span><span class="sxs-lookup"><span data-stu-id="7c80c-136">Other return codes are treated as failure.</span></span>



| <span data-ttu-id="7c80c-137">Message</span><span class="sxs-lookup"><span data-stu-id="7c80c-137">Message</span></span>                          | <span data-ttu-id="7c80c-138">Signification</span><span class="sxs-lookup"><span data-stu-id="7c80c-138">Meaning</span></span>                                                                                              |
|----------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7c80c-139">ERREUR d' \_ installation de \_ redémarrage</span><span class="sxs-lookup"><span data-stu-id="7c80c-139">ERROR\_INSTALL\_REBOOT</span></span>           | <span data-ttu-id="7c80c-140">L’indicateur de redémarrage sera configuré pour redémarrer à la fin de l’installation.</span><span class="sxs-lookup"><span data-stu-id="7c80c-140">The restart flag will be set to restart at end of the installation.</span></span>                                  |
| <span data-ttu-id="7c80c-141">ERREUR d' \_ installation de \_ redémarrage \_ maintenant</span><span class="sxs-lookup"><span data-stu-id="7c80c-141">ERROR\_INSTALL\_REBOOT\_NOW</span></span>      | <span data-ttu-id="7c80c-142">Un redémarrage est nécessaire avant de terminer l’installation.</span><span class="sxs-lookup"><span data-stu-id="7c80c-142">A restart is required before completing the installation.</span></span> <span data-ttu-id="7c80c-143">Le redémarrage sera traité immédiatement.</span><span class="sxs-lookup"><span data-stu-id="7c80c-143">The restart will be processed immediately.</span></span> |
| <span data-ttu-id="7c80c-144">ERREUR \_ de \_ redémarrage de la réussite \_ obligatoire</span><span class="sxs-lookup"><span data-stu-id="7c80c-144">ERROR\_SUCCESS\_REBOOT\_REQUIRED</span></span> | <span data-ttu-id="7c80c-145">Un redémarrage était nécessaire, mais a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="7c80c-145">A restart was required, but was suppressed.</span></span>                                                          |



 

## <a name="remarks"></a><span data-ttu-id="7c80c-146">Notes</span><span class="sxs-lookup"><span data-stu-id="7c80c-146">Remarks</span></span>

<span data-ttu-id="7c80c-147">Une expression conditionnelle est requise pour activer l’installation simultanée au niveau de l’installation ou de la suppression du composant ou de la fonctionnalité associé.</span><span class="sxs-lookup"><span data-stu-id="7c80c-147">A conditional expression is required to enable the concurrent installation at either installation or removal of the associated component or feature.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7c80c-148">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="7c80c-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c80c-149">Installations simultanées</span><span class="sxs-lookup"><span data-stu-id="7c80c-149">Concurrent Installations</span></span>](concurrent-installations.md)
</dt> <dt>

[<span data-ttu-id="7c80c-150">Référence des actions personnalisées</span><span class="sxs-lookup"><span data-stu-id="7c80c-150">Custom Action Reference</span></span>](custom-action-reference.md)
</dt> <dt>

[<span data-ttu-id="7c80c-151">À propos des actions personnalisées</span><span class="sxs-lookup"><span data-stu-id="7c80c-151">About Custom Actions</span></span>](about-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="7c80c-152">Utilisation d’actions personnalisées</span><span class="sxs-lookup"><span data-stu-id="7c80c-152">Using Custom Actions</span></span>](using-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="7c80c-153">Valeurs de retour de l’action personnalisée</span><span class="sxs-lookup"><span data-stu-id="7c80c-153">Custom Action Return Values</span></span>](custom-action-return-values.md)
</dt> </dl>

 

 



