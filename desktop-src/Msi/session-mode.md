---
description: Il s’agit de la propriété mode de l’objet session. Cette propriété est une valeur représentant l’indicateur de mode désigné pour la session d’installation en cours. La plupart des indicateurs de mode sont en lecture seule en externe, mais quelques indicateurs spécifiés peuvent également être définis.
ms.assetid: 9aca413d-d653-4ec1-a39b-af956f6c95e7
title: Session. mode (propriété)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.Mode
api_type:
- COM
api_location: ''
ms.openlocfilehash: f081859db789601f2c41bf95d65c377fba8d51f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526461"
---
# <a name="sessionmode-property"></a><span data-ttu-id="c0b76-105">Session. mode (propriété)</span><span class="sxs-lookup"><span data-stu-id="c0b76-105">Session.Mode property</span></span>

<span data-ttu-id="c0b76-106">Il s’agit de la propriété **mode** de l’objet [**session**](session-object.md) .</span><span class="sxs-lookup"><span data-stu-id="c0b76-106">This is the **Mode** property of the [**Session**](session-object.md) object.</span></span> <span data-ttu-id="c0b76-107">Cette propriété est une valeur représentant l’indicateur de mode désigné pour la session d’installation en cours.</span><span class="sxs-lookup"><span data-stu-id="c0b76-107">This property is a value representing the designated mode flag for the current install session.</span></span> <span data-ttu-id="c0b76-108">La plupart des indicateurs de mode sont en lecture seule en externe, mais quelques indicateurs spécifiés peuvent également être définis.</span><span class="sxs-lookup"><span data-stu-id="c0b76-108">Most of the mode flags are read-only externally, but a few specified flags may be set as well.</span></span>

<span data-ttu-id="c0b76-109">La fonction [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) retourne une valeur booléenne true ou false, indiquant si la propriété spécifique passée dans la fonction est actuellement définie (true) ou non définie (false).</span><span class="sxs-lookup"><span data-stu-id="c0b76-109">The [**MsiGetMode**](/windows/desktop/api/Msiquery/nf-msiquery-msigetmode) function returns a Boolean TRUE or FALSE, indicating whether the specific property passed into the function is currently set (TRUE) or not set (FALSE).</span></span>

<span data-ttu-id="c0b76-110">Notez que toutes les valeurs de mode d’exécution de *Flag* ne sont pas disponibles lors de l’appel de la propriété **mode** à partir d’une action personnalisée différée.</span><span class="sxs-lookup"><span data-stu-id="c0b76-110">Note that not all the run mode values of *flag* are available when calling the **Mode** property from a deferred custom action.</span></span> <span data-ttu-id="c0b76-111">Pour plus d’informations, consultez [obtention d’informations de contexte pour les actions personnalisées d’exécution différée](obtaining-context-information-for-deferred-execution-custom-actions.md).</span><span class="sxs-lookup"><span data-stu-id="c0b76-111">For more information, see [Obtaining Context Information for Deferred Execution Custom Actions](obtaining-context-information-for-deferred-execution-custom-actions.md).</span></span>

<span data-ttu-id="c0b76-112">Cette propriété est en lecture seule.</span><span class="sxs-lookup"><span data-stu-id="c0b76-112">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0b76-113">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="c0b76-113">Syntax</span></span>


```JScript
propVal = Session.Mode
```



## <a name="property-value"></a><span data-ttu-id="c0b76-114">Valeur de la propriété</span><span class="sxs-lookup"><span data-stu-id="c0b76-114">Property value</span></span>

<span data-ttu-id="c0b76-115">Valeur entière requise pour l’indicateur.</span><span class="sxs-lookup"><span data-stu-id="c0b76-115">Required integer value for the flag.</span></span> <span data-ttu-id="c0b76-116">Doit prendre l'une des valeurs suivantes :</span><span class="sxs-lookup"><span data-stu-id="c0b76-116">Must be one of the following:</span></span>



| <span data-ttu-id="c0b76-117">Nom de l’indicateur</span><span class="sxs-lookup"><span data-stu-id="c0b76-117">Flag name</span></span>                                                                                                                                                                                                                                                                                                | <span data-ttu-id="c0b76-118">Signification</span><span class="sxs-lookup"><span data-stu-id="c0b76-118">Meaning</span></span>                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| <span id="msiRunModeAdmin"></span><span id="msirunmodeadmin"></span><span id="MSIRUNMODEADMIN"></span><dl> <span data-ttu-id="c0b76-119"><dt>**msiRunModeAdmin**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="c0b76-119"><dt>**msiRunModeAdmin**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="c0b76-120">Installation en mode administrateur, sinon installation du produit.</span><span class="sxs-lookup"><span data-stu-id="c0b76-120">Administrative mode install, else product install.</span></span><br/>                                  |
| <span id="msiRunModeAdvertise"></span><span id="msirunmodeadvertise"></span><span id="MSIRUNMODEADVERTISE"></span><dl> <span data-ttu-id="c0b76-121"><dt>**msiRunModeAdvertise**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="c0b76-121"><dt>**msiRunModeAdvertise**</dt> <dt>1</dt></span></span> </dl>                              | <span data-ttu-id="c0b76-122">Mode de publication de l’installation.</span><span class="sxs-lookup"><span data-stu-id="c0b76-122">Advertise mode of install.</span></span><br/>                                                          |
| <span id="msiRunModeMaintenance"></span><span id="msirunmodemaintenance"></span><span id="MSIRUNMODEMAINTENANCE"></span><dl> <span data-ttu-id="c0b76-123"><dt>**msiRunModeMaintenance**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="c0b76-123"><dt>**msiRunModeMaintenance**</dt> <dt>2</dt></span></span> </dl>                      | <span data-ttu-id="c0b76-124">Base de données du mode de maintenance chargée.</span><span class="sxs-lookup"><span data-stu-id="c0b76-124">Maintenance mode database loaded.</span></span><br/>                                                   |
| <span id="msiRunModeRollbackEnabled"></span><span id="msirunmoderollbackenabled"></span><span id="MSIRUNMODEROLLBACKENABLED"></span><dl> <span data-ttu-id="c0b76-125"><dt>**msiRunModeRollbackEnabled**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="c0b76-125"><dt>**msiRunModeRollbackEnabled**</dt> <dt>3</dt></span></span> </dl>      | <span data-ttu-id="c0b76-126">La restauration est activée.</span><span class="sxs-lookup"><span data-stu-id="c0b76-126">Rollback is enabled.</span></span><br/>                                                                |
| <span id="msiRunModeLogEnabled"></span><span id="msirunmodelogenabled"></span><span id="MSIRUNMODELOGENABLED"></span><dl> <span data-ttu-id="c0b76-127"><dt>**msiRunModeLogEnabled**</dt> <dt>4</dt></span><span class="sxs-lookup"><span data-stu-id="c0b76-127"><dt>**msiRunModeLogEnabled**</dt> <dt>4</dt></span></span> </dl>                          | <span data-ttu-id="c0b76-128">Le fichier journal est actif.</span><span class="sxs-lookup"><span data-stu-id="c0b76-128">Log file is active.</span></span><br/>                                                                 |
| <span id="msiRunModeOperations"></span><span id="msirunmodeoperations"></span><span id="MSIRUNMODEOPERATIONS"></span><dl> <span data-ttu-id="c0b76-129"><dt>**msiRunModeOperations**</dt> <dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="c0b76-129"><dt>**msiRunModeOperations**</dt> <dt>5</dt></span></span> </dl>                          | <span data-ttu-id="c0b76-130">Exécution ou mise en attente des opérations.</span><span class="sxs-lookup"><span data-stu-id="c0b76-130">Executing or spooling operations.</span></span><br/>                                                   |
| <span id="msiRunModeRebootAtEnd"></span><span id="msirunmoderebootatend"></span><span id="MSIRUNMODEREBOOTATEND"></span><dl> <span data-ttu-id="c0b76-131"><dt>**msiRunModeRebootAtEnd**</dt> <dt>6</dt></span><span class="sxs-lookup"><span data-stu-id="c0b76-131"><dt>**msiRunModeRebootAtEnd**</dt> <dt>6</dt></span></span> </dl>                      | <span data-ttu-id="c0b76-132">Un redémarrage est nécessaire (définissable).</span><span class="sxs-lookup"><span data-stu-id="c0b76-132">Reboot is needed (settable).</span></span><br/>                                                        |
| <span id="msiRunModeRebootNow"></span><span id="msirunmoderebootnow"></span><span id="MSIRUNMODEREBOOTNOW"></span><dl> <span data-ttu-id="c0b76-133"><dt>**msiRunModeRebootNow**</dt> <dt>7</dt></span><span class="sxs-lookup"><span data-stu-id="c0b76-133"><dt>**msiRunModeRebootNow**</dt> <dt>7</dt></span></span> </dl>                              | <span data-ttu-id="c0b76-134">Le redémarrage est nécessaire pour continuer l’installation (définissable).</span><span class="sxs-lookup"><span data-stu-id="c0b76-134">Reboot is needed to continue installation (settable).</span></span><br/>                               |
| <span id="msiRunModeCabinet"></span><span id="msirunmodecabinet"></span><span id="MSIRUNMODECABINET"></span><dl> <span data-ttu-id="c0b76-135"><dt>**msiRunModeCabinet**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="c0b76-135"><dt>**msiRunModeCabinet**</dt> <dt>8</dt></span></span> </dl>                                      | <span data-ttu-id="c0b76-136">Installation de fichiers à partir d’armoires et de fichiers à l’aide de la table multimédia.</span><span class="sxs-lookup"><span data-stu-id="c0b76-136">Installing files from cabinets and files using Media table.</span></span><br/>                         |
| <span id="msiRunModeSourceShortNames"></span><span id="msirunmodesourceshortnames"></span><span id="MSIRUNMODESOURCESHORTNAMES"></span><dl> <span data-ttu-id="c0b76-137"><dt>**msiRunModeSourceShortNames**</dt> <dt>9</dt></span><span class="sxs-lookup"><span data-stu-id="c0b76-137"><dt>**msiRunModeSourceShortNames**</dt> <dt>9</dt></span></span> </dl>  | <span data-ttu-id="c0b76-138">Les fichiers sources utilisent uniquement des noms de fichiers courts.</span><span class="sxs-lookup"><span data-stu-id="c0b76-138">Source files use only short file names.</span></span><br/>                                             |
| <span id="msiRunModeTargetShortNames"></span><span id="msirunmodetargetshortnames"></span><span id="MSIRUNMODETARGETSHORTNAMES"></span><dl> <span data-ttu-id="c0b76-139"><dt>**msiRunModeTargetShortNames**</dt> <dt>10</dt></span><span class="sxs-lookup"><span data-stu-id="c0b76-139"><dt>**msiRunModeTargetShortNames**</dt> <dt>10</dt></span></span> </dl> | <span data-ttu-id="c0b76-140">Les fichiers cibles doivent utiliser uniquement des noms de fichiers courts.</span><span class="sxs-lookup"><span data-stu-id="c0b76-140">Target files are to use only short file names.</span></span><br/>                                      |
| <span id="msiRunModeWindows9x"></span><span id="msirunmodewindows9x"></span><span id="MSIRUNMODEWINDOWS9X"></span><dl> <span data-ttu-id="c0b76-141"><dt>**msiRunModeWindows9x**</dt> <dt>12</dt></span><span class="sxs-lookup"><span data-stu-id="c0b76-141"><dt>**msiRunModeWindows9x**</dt> <dt>12</dt></span></span> </dl>                             | <span data-ttu-id="c0b76-142">Le système d’exploitation est Windows 98/95.</span><span class="sxs-lookup"><span data-stu-id="c0b76-142">Operating system is Windows 98/95.</span></span><br/>                                                  |
| <span id="msiRunModeZawEnabled"></span><span id="msirunmodezawenabled"></span><span id="MSIRUNMODEZAWENABLED"></span><dl> <span data-ttu-id="c0b76-143"><dt>**msiRunModeZawEnabled**</dt> <dt>13</dt></span><span class="sxs-lookup"><span data-stu-id="c0b76-143"><dt>**msiRunModeZawEnabled**</dt> <dt>13</dt></span></span> </dl>                         | <span data-ttu-id="c0b76-144">Le système d’exploitation prend en charge la publicité de produits.</span><span class="sxs-lookup"><span data-stu-id="c0b76-144">Operating system supports advertising of products.</span></span><br/>                                  |
| <span id="msiRunModeScheduled"></span><span id="msirunmodescheduled"></span><span id="MSIRUNMODESCHEDULED"></span><dl> <span data-ttu-id="c0b76-145"><dt>**msiRunModeScheduled**</dt> <dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="c0b76-145"><dt>**msiRunModeScheduled**</dt> <dt>16</dt></span></span> </dl>                             | <span data-ttu-id="c0b76-146">[Action personnalisée](custom-actions.md) différée appelée à partir de l’exécution du script d’installation.</span><span class="sxs-lookup"><span data-stu-id="c0b76-146">Deferred [custom action](custom-actions.md) called from install script execution.</span></span><br/>  |
| <span id="msiRunModeRollback"></span><span id="msirunmoderollback"></span><span id="MSIRUNMODEROLLBACK"></span><dl> <span data-ttu-id="c0b76-147"><dt>**msiRunModeRollback**</dt> <dt>17</dt></span><span class="sxs-lookup"><span data-stu-id="c0b76-147"><dt>**msiRunModeRollback**</dt> <dt>17</dt></span></span> </dl>                                 | <span data-ttu-id="c0b76-148">[Action personnalisée](custom-actions.md) différée appelée à partir du script d’exécution de restauration.</span><span class="sxs-lookup"><span data-stu-id="c0b76-148">Deferred [custom action](custom-actions.md) called from rollback execution script.</span></span><br/> |
| <span id="msiRunModeCommit"></span><span id="msirunmodecommit"></span><span id="MSIRUNMODECOMMIT"></span><dl> <span data-ttu-id="c0b76-149"><dt>**msiRunModeCommit**</dt> <dt>18</dt></span><span class="sxs-lookup"><span data-stu-id="c0b76-149"><dt>**msiRunModeCommit**</dt> <dt>18</dt></span></span> </dl>                                         | <span data-ttu-id="c0b76-150">[Action personnalisée](custom-actions.md) différée appelée à partir du script d’exécution de validation.</span><span class="sxs-lookup"><span data-stu-id="c0b76-150">Deferred [custom action](custom-actions.md) called from commit execution script.</span></span><br/>   |



 

## <a name="requirements"></a><span data-ttu-id="c0b76-151">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="c0b76-151">Requirements</span></span>



| <span data-ttu-id="c0b76-152">Condition requise</span><span class="sxs-lookup"><span data-stu-id="c0b76-152">Requirement</span></span> | <span data-ttu-id="c0b76-153">Valeur</span><span class="sxs-lookup"><span data-stu-id="c0b76-153">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0b76-154">Version</span><span class="sxs-lookup"><span data-stu-id="c0b76-154">Version</span></span><br/> | <span data-ttu-id="c0b76-155">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c0b76-155">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="c0b76-156">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="c0b76-156">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="c0b76-157">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="c0b76-157">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |



 

 




