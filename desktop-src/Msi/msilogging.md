---
description: La propriété MsiLogging définit le mode de journalisation par défaut pour le package Windows Installer.
ms.assetid: f5ae389e-bc27-465d-886b-4f4f41d49118
title: Propriété MsiLogging
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97e53df57723157f7184a904e512aac9035a9f53
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526654"
---
# <a name="msilogging-property"></a><span data-ttu-id="67698-103">Propriété MsiLogging</span><span class="sxs-lookup"><span data-stu-id="67698-103">MsiLogging property</span></span>

<span data-ttu-id="67698-104">La propriété **MsiLogging** définit le mode de journalisation par défaut pour le package Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="67698-104">The **MsiLogging** property sets the default logging mode for the Windows Installer package.</span></span> <span data-ttu-id="67698-105">Si cette propriété facultative est présente dans la [table de propriétés](property-table.md), le programme d’installation génère un fichier journal nommé MSI \* . Sign.</span><span class="sxs-lookup"><span data-stu-id="67698-105">If this optional property is present in the [Property table](property-table.md), the installer generates a log file named MSI\*.LOG.</span></span> <span data-ttu-id="67698-106">Le chemin d’accès complet au fichier journal est donné par la valeur de la propriété [**MsiLogFileLocation**](msilogfilelocation.md) .</span><span class="sxs-lookup"><span data-stu-id="67698-106">The full path to the log file is given by the value of the [**MsiLogFileLocation**](msilogfilelocation.md) property.</span></span>

## <a name="value"></a><span data-ttu-id="67698-107">Valeur</span><span class="sxs-lookup"><span data-stu-id="67698-107">Value</span></span>

<span data-ttu-id="67698-108">La valeur de cette propriété doit être une chaîne des caractères suivants qui spécifient le mode de journalisation par défaut.</span><span class="sxs-lookup"><span data-stu-id="67698-108">The value of this property should be a string of the following characters that specify the default logging mode.</span></span>



| <span data-ttu-id="67698-109">Valeur</span><span class="sxs-lookup"><span data-stu-id="67698-109">Value</span></span>                                                                        | <span data-ttu-id="67698-110">Signification</span><span class="sxs-lookup"><span data-stu-id="67698-110">Meaning</span></span>                                                                        |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="67698-111"><dt>Cliqu</dt></span><span class="sxs-lookup"><span data-stu-id="67698-111"><dt>I</dt></span></span> </dl> | <span data-ttu-id="67698-112">Messages d’État.</span><span class="sxs-lookup"><span data-stu-id="67698-112">Status messages.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="67698-113"><dt>w</dt></span><span class="sxs-lookup"><span data-stu-id="67698-113"><dt>w</dt></span></span> </dl> | <span data-ttu-id="67698-114">Avertissements non irrécupérables.</span><span class="sxs-lookup"><span data-stu-id="67698-114">Nonfatal warnings.</span></span><br/>                                                  |
| <dl> <span data-ttu-id="67698-115"><dt>Envoyer</dt></span><span class="sxs-lookup"><span data-stu-id="67698-115"><dt>e</dt></span></span> </dl> | <span data-ttu-id="67698-116">Tous les messages d’erreur.</span><span class="sxs-lookup"><span data-stu-id="67698-116">All error messages.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="67698-117"><dt>un</dt></span><span class="sxs-lookup"><span data-stu-id="67698-117"><dt>a</dt></span></span> </dl> | <span data-ttu-id="67698-118">Démarrage des actions.</span><span class="sxs-lookup"><span data-stu-id="67698-118">Start up of actions.</span></span><br/>                                                |
| <dl> <span data-ttu-id="67698-119"><dt>r</dt></span><span class="sxs-lookup"><span data-stu-id="67698-119"><dt>r</dt></span></span> </dl> | <span data-ttu-id="67698-120">Enregistrements spécifiques aux actions.</span><span class="sxs-lookup"><span data-stu-id="67698-120">Action-specific records.</span></span><br/>                                            |
| <dl> <span data-ttu-id="67698-121"><dt>u</dt></span><span class="sxs-lookup"><span data-stu-id="67698-121"><dt>u</dt></span></span> </dl> | <span data-ttu-id="67698-122">Demandes de l’utilisateur.</span><span class="sxs-lookup"><span data-stu-id="67698-122">User requests.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="67698-123"><dt>c</dt></span><span class="sxs-lookup"><span data-stu-id="67698-123"><dt>c</dt></span></span> </dl> | <span data-ttu-id="67698-124">Paramètres initiaux de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="67698-124">Initial UI parameters.</span></span><br/>                                              |
| <dl> <span data-ttu-id="67698-125"><dt>m</dt></span><span class="sxs-lookup"><span data-stu-id="67698-125"><dt>m</dt></span></span> </dl> | <span data-ttu-id="67698-126">Informations de sortie insuffisantes ou irrécupérables.</span><span class="sxs-lookup"><span data-stu-id="67698-126">Out-of-memory or fatal exit information.</span></span><br/>                            |
| <dl> <span data-ttu-id="67698-127"><dt>o</dt></span><span class="sxs-lookup"><span data-stu-id="67698-127"><dt>o</dt></span></span> </dl> | <span data-ttu-id="67698-128">Messages d’espace disque insuffisants.</span><span class="sxs-lookup"><span data-stu-id="67698-128">Out-of-disk-space messages.</span></span><br/>                                         |
| <dl> <span data-ttu-id="67698-129"><dt>p</dt></span><span class="sxs-lookup"><span data-stu-id="67698-129"><dt>p</dt></span></span> </dl> | <span data-ttu-id="67698-130">Propriétés du terminal.</span><span class="sxs-lookup"><span data-stu-id="67698-130">Terminal properties.</span></span><br/>                                                |
| <dl> <span data-ttu-id="67698-131"><dt>v</dt></span><span class="sxs-lookup"><span data-stu-id="67698-131"><dt>v</dt></span></span> </dl> | <span data-ttu-id="67698-132">Sortie détaillée.</span><span class="sxs-lookup"><span data-stu-id="67698-132">Verbose output.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="67698-133"><dt>x</dt></span><span class="sxs-lookup"><span data-stu-id="67698-133"><dt>x</dt></span></span> </dl> | <span data-ttu-id="67698-134">Informations supplémentaires sur le débogage.</span><span class="sxs-lookup"><span data-stu-id="67698-134">Extra debugging information.</span></span> <span data-ttu-id="67698-135">Disponible uniquement sur Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="67698-135">Only available on Windows Server 2003.</span></span><br/> |
| <dl> <span data-ttu-id="67698-136"><dt>!</dt></span><span class="sxs-lookup"><span data-stu-id="67698-136"><dt>!</dt></span></span> </dl> | <span data-ttu-id="67698-137">Videz chaque ligne dans le journal.</span><span class="sxs-lookup"><span data-stu-id="67698-137">Flush each line to the log.</span></span><br/>                                         |



 

## <a name="remarks"></a><span data-ttu-id="67698-138">Notes</span><span class="sxs-lookup"><span data-stu-id="67698-138">Remarks</span></span>

<span data-ttu-id="67698-139">Cette propriété est disponible à partir de Windows Installer 4,0.</span><span class="sxs-lookup"><span data-stu-id="67698-139">This property is available starting with Windows Installer 4.0.</span></span>

<span data-ttu-id="67698-140">Vous ne pouvez pas utiliser les valeurs « + » et « \* » de l’option/l dans la valeur de la propriété **MsiLogging** .</span><span class="sxs-lookup"><span data-stu-id="67698-140">You cannot use the "+" and "\*" values of the /L option in the value of the **MsiLogging** property.</span></span>

<span data-ttu-id="67698-141">Le mode de journalisation peut être défini à l’aide d’une stratégie, d’une option de ligne de commande ou par programme.</span><span class="sxs-lookup"><span data-stu-id="67698-141">The logging mode can be set using policy, a command-line option, or programmatically.</span></span> <span data-ttu-id="67698-142">Cela remplace le mode de journalisation par défaut.</span><span class="sxs-lookup"><span data-stu-id="67698-142">This overrides the default logging mode.</span></span> <span data-ttu-id="67698-143">Pour plus d’informations sur toutes les méthodes qui sont disponibles pour définir le mode de journalisation, consultez [journalisation normale](normal-logging.md) dans la section [journalisation Windows Installer](windows-installer-logging.md) .</span><span class="sxs-lookup"><span data-stu-id="67698-143">For more information about all the methods that are available for setting the logging mode, see [Normal Logging](normal-logging.md) in the [Windows Installer Logging](windows-installer-logging.md) section.</span></span>

<span data-ttu-id="67698-144">Si la propriété **MsiLogging** est présente dans la [table de propriétés](property-table.md), le mode de journalisation par défaut du package peut être modifié en modifiant la valeur de cette propriété à l’aide d’une [transformation de base de données](database-transforms.md).</span><span class="sxs-lookup"><span data-stu-id="67698-144">If the **MsiLogging** property is present in the [Property table](property-table.md), the default logging mode of the package can be modified by changing the value of this property using a [database transform](database-transforms.md).</span></span> <span data-ttu-id="67698-145">Le mode de journalisation par défaut ne peut pas être modifié à l’aide d’un [package correctif](patch-packages.md) (un fichier. msp).</span><span class="sxs-lookup"><span data-stu-id="67698-145">The default logging mode cannot be changed using a [Patch Package](patch-packages.md) (a .msp file.)</span></span>

<span data-ttu-id="67698-146">Si la propriété **MsiLogging** a été définie dans la [table de propriétés](property-table.md), le mode de journalisation par défaut pour tous les utilisateurs de l’ordinateur peut être spécifié en définissant la stratégie [DisableLoggingFromPackage](disableloggingfrompackage.md) et la stratégie de [journalisation](logging.md) .</span><span class="sxs-lookup"><span data-stu-id="67698-146">If the **MsiLogging** property has been set in the [Property table](property-table.md), the default logging mode for all users of the computer can be specified by setting both the [DisableLoggingFromPackage](disableloggingfrompackage.md) policy and [Logging](logging.md) policy.</span></span> <span data-ttu-id="67698-147">La définition de la stratégie DisableLoggingFromPackage et de la stratégie de journalisation remplace la propriété **MsiLogging** pour tous les packages.</span><span class="sxs-lookup"><span data-stu-id="67698-147">Setting both the DisableLoggingFromPackage policy and Logging policy will override the **MsiLogging** property for all packages.</span></span>

## <a name="requirements"></a><span data-ttu-id="67698-148">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="67698-148">Requirements</span></span>



| <span data-ttu-id="67698-149">Condition requise</span><span class="sxs-lookup"><span data-stu-id="67698-149">Requirement</span></span> | <span data-ttu-id="67698-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="67698-150">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="67698-151">Version</span><span class="sxs-lookup"><span data-stu-id="67698-151">Version</span></span><br/> | <span data-ttu-id="67698-152">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="67698-152">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="67698-153">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="67698-153">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="67698-154">Windows Installer 4,5 sur Windows Server 2003 ou Windows XP.</span><span class="sxs-lookup"><span data-stu-id="67698-154">Windows Installer 4.5 on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="67698-155">Pour plus d’informations sur le Service Pack Windows minimal requis par une version de Windows Installer, consultez la [Configuration requise pour la Windows Installer Run-Time](windows-installer-portal.md) .</span><span class="sxs-lookup"><span data-stu-id="67698-155">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="67698-156">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="67698-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67698-157">Propriétés</span><span class="sxs-lookup"><span data-stu-id="67698-157">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="67698-158">Non pris en charge dans Windows Installer 3,1 et versions antérieures</span><span class="sxs-lookup"><span data-stu-id="67698-158">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




