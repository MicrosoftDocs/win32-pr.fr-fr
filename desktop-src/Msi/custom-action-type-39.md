---
description: Les développeurs de packages de Windows Installer peuvent choisir d’utiliser un type d’action personnalisé 39 quand les actions standard sont insuffisantes pour exécuter l’installation.
ms.assetid: edf96cc6-ef32-4660-b4ee-50c130626e15
title: Type d’action personnalisé 39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e49667fbad6e71aa8b2197b00ae9dd49f7dfff0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866090"
---
# <a name="custom-action-type-39"></a><span data-ttu-id="17331-103">Type d’action personnalisé 39</span><span class="sxs-lookup"><span data-stu-id="17331-103">Custom Action Type 39</span></span>

<span data-ttu-id="17331-104">Le type d’action personnalisé 39 est utilisé avec les installations simultanées.</span><span class="sxs-lookup"><span data-stu-id="17331-104">The Custom Action Type 39 is used with concurrent installations.</span></span> <span data-ttu-id="17331-105">Les installations simultanées ne sont pas recommandées pour l’installation d’applications destinées à être communiquées au public.</span><span class="sxs-lookup"><span data-stu-id="17331-105">Concurrent installations are not recommended for the installation of applications intended for release to the public.</span></span> <span data-ttu-id="17331-106">Pour plus d’informations sur les installations simultanées, consultez [installations simultanées](concurrent-installations.md).</span><span class="sxs-lookup"><span data-stu-id="17331-106">For information about concurrent installations please see [Concurrent Installations](concurrent-installations.md).</span></span>

<span data-ttu-id="17331-107">Tapez 39 action personnalisée pour installer une application publiée ou déjà installée.</span><span class="sxs-lookup"><span data-stu-id="17331-107">Type 39 custom action installs an application that is advertised or already installed.</span></span> <span data-ttu-id="17331-108">Ce type d’action personnalisé peut être utilisé pour réinstaller ou supprimer un produit qui a été installé en tant qu’installation simultanée par le package d’installation du produit actuel.</span><span class="sxs-lookup"><span data-stu-id="17331-108">This custom action type may be used to reinstall or remove a product that has been installed as a concurrent installation by the current product's installation package.</span></span> <span data-ttu-id="17331-109">L’action personnalisée de type 39 ne peut pas être utilisée pour réinstaller ou supprimer un produit précédemment installé par d’autres moyens.</span><span class="sxs-lookup"><span data-stu-id="17331-109">The Type 39 custom action cannot be used to reinstall or remove any product previously installed by any other means.</span></span> <span data-ttu-id="17331-110">Par exemple, si le produit secondaire est installé à l’aide d’un type 39, de type 23 ou de l’action personnalisée de type 7 lors de l’installation du produit principal, une action personnalisée de type 39 peut être utilisée pour supprimer le produit secondaire lors de la désinstallation du produit principal.</span><span class="sxs-lookup"><span data-stu-id="17331-110">For example, if the secondary product is installed using a Type 39, Type 23, or Type 7 custom action during the installation of the primary product, a Type 39 custom action may be used to remove the secondary product when the primary product is uninstalled.</span></span>

## <a name="source"></a><span data-ttu-id="17331-111">Source</span><span class="sxs-lookup"><span data-stu-id="17331-111">Source</span></span>

<span data-ttu-id="17331-112">Le champ source de la [table CustomAction](customaction-table.md) contient le code de produit de l’application.</span><span class="sxs-lookup"><span data-stu-id="17331-112">The Source field of the [CustomAction table](customaction-table.md) contains the product code for the application.</span></span>

## <a name="numeric-type"></a><span data-ttu-id="17331-113">Type numérique</span><span class="sxs-lookup"><span data-stu-id="17331-113">Numeric Type</span></span>



| <span data-ttu-id="17331-114">Nom de type</span><span class="sxs-lookup"><span data-stu-id="17331-114">Type name</span></span>                                                     | <span data-ttu-id="17331-115">Valeur</span><span class="sxs-lookup"><span data-stu-id="17331-115">Value</span></span> |
|---------------------------------------------------------------|-------|
| <span data-ttu-id="17331-116">msidbCustomActionTypeInstall + msidbCustomActionTypeDirectory</span><span class="sxs-lookup"><span data-stu-id="17331-116">msidbCustomActionTypeInstall + msidbCustomActionTypeDirectory</span></span> | <span data-ttu-id="17331-117">39</span><span class="sxs-lookup"><span data-stu-id="17331-117">39</span></span>    |



 

## <a name="target"></a><span data-ttu-id="17331-118">Cible</span><span class="sxs-lookup"><span data-stu-id="17331-118">Target</span></span>

<span data-ttu-id="17331-119">Le champ cible de la [table CustomAction](customaction-table.md) contient les paramètres de propriété qui doivent être passés à l’installation simultanée.</span><span class="sxs-lookup"><span data-stu-id="17331-119">The Target field of the [CustomAction table](customaction-table.md) contains property settings that are to be passed to the concurrent installation.</span></span> <span data-ttu-id="17331-120">Ces paramètres de propriété peuvent spécifier des fonctionnalités.</span><span class="sxs-lookup"><span data-stu-id="17331-120">These property settings can specify features.</span></span>

## <a name="return-processing-options"></a><span data-ttu-id="17331-121">Options de traitement des retours</span><span class="sxs-lookup"><span data-stu-id="17331-121">Return Processing Options</span></span>

<span data-ttu-id="17331-122">Le type d’action personnalisé 39 échoue si l’application n’est pas publiée ou installée.</span><span class="sxs-lookup"><span data-stu-id="17331-122">The custom action type 39 fails if the application is not advertised or installed.</span></span> <span data-ttu-id="17331-123">Pour éviter ce problème, vous devez définir **msidbCustomActionTypeContinueflag**.</span><span class="sxs-lookup"><span data-stu-id="17331-123">To avoid this failure, you must set the **msidbCustomActionTypeContinueflag**.</span></span>

<span data-ttu-id="17331-124">Une installation simultanée ne peut pas s’exécuter de façon asynchrone.</span><span class="sxs-lookup"><span data-stu-id="17331-124">A concurrent install cannot run asynchronously.</span></span>

<span data-ttu-id="17331-125">Consultez [options de traitement des retours d’actions personnalisées](custom-action-return-processing-options.md).</span><span class="sxs-lookup"><span data-stu-id="17331-125">See [Custom Action Return Processing Options](custom-action-return-processing-options.md).</span></span>

## <a name="execution-scheduling-options"></a><span data-ttu-id="17331-126">Options de planification de l’exécution</span><span class="sxs-lookup"><span data-stu-id="17331-126">Execution Scheduling Options</span></span>

<span data-ttu-id="17331-127">Des indicateurs d’options sont disponibles pour contrôler l’exécution multiple potentielle des actions personnalisées.</span><span class="sxs-lookup"><span data-stu-id="17331-127">Options flags are available to control the potential multiple execution of custom actions.</span></span> <span data-ttu-id="17331-128">Consultez [options de planification de l’exécution des actions personnalisées](custom-action-execution-scheduling-options.md).</span><span class="sxs-lookup"><span data-stu-id="17331-128">See [Custom Action Execution Scheduling Options](custom-action-execution-scheduling-options.md).</span></span>

## <a name="in-script-execution-options"></a><span data-ttu-id="17331-129">In-Script les options d’exécution</span><span class="sxs-lookup"><span data-stu-id="17331-129">In-Script Execution Options</span></span>

<span data-ttu-id="17331-130">L’action personnalisée n’utilise pas cette option.</span><span class="sxs-lookup"><span data-stu-id="17331-130">The custom action does not use this option.</span></span>

## <a name="return-values"></a><span data-ttu-id="17331-131">Valeurs de retour</span><span class="sxs-lookup"><span data-stu-id="17331-131">Return Values</span></span>

<span data-ttu-id="17331-132">L’état de retour de la sortie de l’utilisateur, de l’échec, de l’interruption ou de la réussite d’une installation simultanée est traité de la même façon que toute autre action.</span><span class="sxs-lookup"><span data-stu-id="17331-132">The return status of user exit, failure, suspend, or success from a concurrent installation is processed in the same way as any other action.</span></span> <span data-ttu-id="17331-133">Notez toutefois que Windows Installer traduit les valeurs de retour de toutes les actions quand il écrit la valeur de retour dans le fichier journal.</span><span class="sxs-lookup"><span data-stu-id="17331-133">Note however that Windows Installer translates the return values from all actions when it writes the return value into the log file.</span></span> <span data-ttu-id="17331-134">Par exemple, si la valeur de retour de l’action apparaît comme 1 dans le fichier journal, cela signifie que l’action a retourné une erreur de \_ réussite.</span><span class="sxs-lookup"><span data-stu-id="17331-134">For example, if the action return value appears as 1 in the log file, this means that the action returned ERROR\_SUCCESS.</span></span> <span data-ttu-id="17331-135">Pour plus d’informations, consultez [journalisation des valeurs de retour d’action](logging-of-action-return-values.md).</span><span class="sxs-lookup"><span data-stu-id="17331-135">For more information, see [Logging of Action Return Values](logging-of-action-return-values.md).</span></span>

<span data-ttu-id="17331-136">Notez que, si une installation simultanée a une **msidbCustomActionTypeContinue** définie, un retour de l’erreur d’installation de USEREXIT, une erreur d’installation de \_ \_ \_ \_ redémarrage, une erreur d' \_ installation de \_ redémarrage \_ maintenant ou une erreur de \_ redémarrage de la réussite \_ \_ requise est traitée comme une erreur de \_ réussite.</span><span class="sxs-lookup"><span data-stu-id="17331-136">Note that if a concurrent installation has **msidbCustomActionTypeContinue** set, then a return of ERROR\_INSTALL\_USEREXIT, ERROR\_INSTALL\_REBOOT, ERROR\_INSTALL\_REBOOT\_NOW, or ERROR\_SUCCESS\_REBOOT\_REQUIRED is treated as ERROR\_SUCCESS.</span></span> <span data-ttu-id="17331-137">Cela signifie que si vous définissez **msidbCustomActionTypeContinue** et que votre installation simultanée requiert un redémarrage, la nécessité du redémarrage sera ignorée.</span><span class="sxs-lookup"><span data-stu-id="17331-137">This means that if you set **msidbCustomActionTypeContinue** and your concurrent installation requires a restart, the requirement for the restart will be ignored.</span></span> <span data-ttu-id="17331-138">En outre, le code d’erreur de l’action personnalisée d’installation simultanée est ignoré.</span><span class="sxs-lookup"><span data-stu-id="17331-138">Additionally, the error code from the concurrent installation custom action will be ignored.</span></span>

<span data-ttu-id="17331-139">Si **msidbCustomActionTypeContinue** n’est pas défini, les codes de retour suivants plus la réussite de l’erreur \_ sont traités comme des succès et ont les significations suivantes.</span><span class="sxs-lookup"><span data-stu-id="17331-139">If **msidbCustomActionTypeContinue** is not set, the following return codes plus ERROR\_SUCCESS are treated as success and have the following meanings.</span></span> <span data-ttu-id="17331-140">Les autres codes de retour sont traités comme des échecs.</span><span class="sxs-lookup"><span data-stu-id="17331-140">Other return codes are treated as failure.</span></span>



| <span data-ttu-id="17331-141">Message</span><span class="sxs-lookup"><span data-stu-id="17331-141">Message</span></span>                          | <span data-ttu-id="17331-142">Signification</span><span class="sxs-lookup"><span data-stu-id="17331-142">Meaning</span></span>                                                                                              |
|----------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17331-143">ERREUR d' \_ installation de \_ redémarrage</span><span class="sxs-lookup"><span data-stu-id="17331-143">ERROR\_INSTALL\_REBOOT</span></span>           | <span data-ttu-id="17331-144">L’indicateur de redémarrage sera configuré pour redémarrer à la fin de l’installation.</span><span class="sxs-lookup"><span data-stu-id="17331-144">The restart flag will be set to restart at end of the installation.</span></span>                                  |
| <span data-ttu-id="17331-145">ERREUR d' \_ installation de \_ redémarrage \_ maintenant</span><span class="sxs-lookup"><span data-stu-id="17331-145">ERROR\_INSTALL\_REBOOT\_NOW</span></span>      | <span data-ttu-id="17331-146">Un redémarrage est nécessaire avant de terminer l’installation.</span><span class="sxs-lookup"><span data-stu-id="17331-146">A restart is required before completing the installation.</span></span> <span data-ttu-id="17331-147">Le redémarrage sera traité immédiatement.</span><span class="sxs-lookup"><span data-stu-id="17331-147">The restart will be processed immediately.</span></span> |
| <span data-ttu-id="17331-148">ERREUR \_ de \_ redémarrage de la réussite \_ obligatoire</span><span class="sxs-lookup"><span data-stu-id="17331-148">ERROR\_SUCCESS\_REBOOT\_REQUIRED</span></span> | <span data-ttu-id="17331-149">Un redémarrage était nécessaire, mais a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="17331-149">A restart was required, but was suppressed.</span></span>                                                          |



 

## <a name="remarks"></a><span data-ttu-id="17331-150">Notes</span><span class="sxs-lookup"><span data-stu-id="17331-150">Remarks</span></span>

<span data-ttu-id="17331-151">Une expression conditionnelle est requise pour activer l’installation simultanée au niveau de l’installation ou de la suppression du composant ou de la fonctionnalité associé.</span><span class="sxs-lookup"><span data-stu-id="17331-151">A conditional expression is required to enable the concurrent installation at either installation or removal of the associated component or feature.</span></span>

## <a name="related-topics"></a><span data-ttu-id="17331-152">Rubriques connexes</span><span class="sxs-lookup"><span data-stu-id="17331-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17331-153">Installations simultanées</span><span class="sxs-lookup"><span data-stu-id="17331-153">Concurrent Installations</span></span>](concurrent-installations.md)
</dt> <dt>

[<span data-ttu-id="17331-154">Référence des actions personnalisées</span><span class="sxs-lookup"><span data-stu-id="17331-154">Custom Action Reference</span></span>](custom-action-reference.md)
</dt> <dt>

[<span data-ttu-id="17331-155">À propos des actions personnalisées</span><span class="sxs-lookup"><span data-stu-id="17331-155">About Custom Actions</span></span>](about-custom-actions.md)
</dt> <dt>

[<span data-ttu-id="17331-156">Utilisation d’actions personnalisées</span><span class="sxs-lookup"><span data-stu-id="17331-156">Using Custom Actions</span></span>](using-custom-actions.md)
</dt> </dl>

 

 



