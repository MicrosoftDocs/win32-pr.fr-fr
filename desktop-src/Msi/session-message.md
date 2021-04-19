---
description: La méthode message de l’objet session effectue toutes les opérations de journalisation activées et diffère l’exécution à l’objet gestionnaire d’interface utilisateur associé au moteur. La journalisation peut être activée de manière sélective pour les différents types de messages. Consultez la méthode EnableLog.
ms.assetid: 09053700-a641-4970-bf55-d7c81f345257
title: Session. message, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Session.Message
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: e20cfebe0a3359a99770cbd242501649bf93f86e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537893"
---
# <a name="sessionmessage-method"></a><span data-ttu-id="e1036-105">Session. message, méthode</span><span class="sxs-lookup"><span data-stu-id="e1036-105">Session.Message method</span></span>

<span data-ttu-id="e1036-106">La méthode **message** de l’objet [**session**](session-object.md) effectue toutes les opérations de journalisation activées et diffère l’exécution à l’objet gestionnaire d’interface utilisateur associé au moteur.</span><span class="sxs-lookup"><span data-stu-id="e1036-106">The **Message** method of the [**Session**](session-object.md) object performs any enabled logging operations and defers execution to the UI handler object associated with the engine.</span></span> <span data-ttu-id="e1036-107">La journalisation peut être activée de manière sélective pour les différents types de messages.</span><span class="sxs-lookup"><span data-stu-id="e1036-107">Logging may be selectively enabled for the various message types.</span></span> <span data-ttu-id="e1036-108">Consultez la méthode [**EnableLog**](installer-enablelog.md) .</span><span class="sxs-lookup"><span data-stu-id="e1036-108">See the [**EnableLog**](installer-enablelog.md) method.</span></span>

<span data-ttu-id="e1036-109">Si le champ d’enregistrement 0 contient une chaîne de mise en forme, il est utilisé pour mettre en forme les données dans les autres champs.</span><span class="sxs-lookup"><span data-stu-id="e1036-109">If record field 0 contains a formatting string, it is used to format the data in the other fields.</span></span> <span data-ttu-id="e1036-110">Sinon, si le message est une erreur, un avertissement ou un message utilisateur, une tentative est faite pour trouver un modèle de message dans la table d’erreurs pour la base de données actuelle à l’aide du numéro d’erreur trouvé dans le champ 1 de l’enregistrement pour les types de messages et les valeurs de retour.</span><span class="sxs-lookup"><span data-stu-id="e1036-110">Else if the message is an error, warning, or user message, an attempt is made to find a message template in the Error table for the current database using the error number found in field 1 of the record for message types and return values.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1036-111">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="e1036-111">Syntax</span></span>


```JScript
Session.Message(
  kind,
  record
)
```



## <a name="parameters"></a><span data-ttu-id="e1036-112">Paramètres</span><span class="sxs-lookup"><span data-stu-id="e1036-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e1036-113">*espèces*</span><span class="sxs-lookup"><span data-stu-id="e1036-113">*kind*</span></span> 
</dt> <dd>

<span data-ttu-id="e1036-114">Le paramètre *Kind* doit avoir l’une des valeurs suivantes.</span><span class="sxs-lookup"><span data-stu-id="e1036-114">The *kind* parameter is required to be one of the following values.</span></span> <span data-ttu-id="e1036-115">Pour afficher une boîte de message avec des boutons et des icônes de type push, calculez la valeur de *genre* en ajoutant les styles de zone de message standard utilisés par [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) et [**MessageBoxEx**](/windows/win32/api/winuser/nf-winuser-messageboxexa) à **msiMessageTypeError**, **msiMessageTypeWarning** ou **msiMessageTypeUser**.</span><span class="sxs-lookup"><span data-stu-id="e1036-115">To display a message box with push buttons and icons, calculate the value of *kind* by adding the standard message box styles used by [**MessageBox**](/windows/win32/api/winuser/nf-winuser-messagebox) and [**MessageBoxEx**](/windows/win32/api/winuser/nf-winuser-messageboxexa) to **msiMessageTypeError**, **msiMessageTypeWarning**, or **msiMessageTypeUser**.</span></span> <span data-ttu-id="e1036-116">Pour plus d’informations, consultez la section Notes ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="e1036-116">For more information see the Remarks section below.</span></span>



| <span data-ttu-id="e1036-117">Constante</span><span class="sxs-lookup"><span data-stu-id="e1036-117">Constant</span></span>                                                                                                                                                                                                                                                                                                                 | <span data-ttu-id="e1036-118">Signification</span><span class="sxs-lookup"><span data-stu-id="e1036-118">Meaning</span></span>                                                                                                                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiMessageTypeFatalExit"></span><span id="msimessagetypefatalexit"></span><span id="MSIMESSAGETYPEFATALEXIT"></span><dl> <span data-ttu-id="e1036-119"><dt>**msiMessageTypeFatalExit**</dt> <dt>&H00000000</dt></span><span class="sxs-lookup"><span data-stu-id="e1036-119"><dt>**msiMessageTypeFatalExit**</dt> <dt>&H00000000</dt></span></span> </dl>                     | <span data-ttu-id="e1036-120">Arrêt prématuré, risque de manquer de mémoire.</span><span class="sxs-lookup"><span data-stu-id="e1036-120">Premature termination, possibly fatal out of memory.</span></span><br/>                                                                              |
| <span id="msiMessageTypeError"></span><span id="msimessagetypeerror"></span><span id="MSIMESSAGETYPEERROR"></span><dl> <span data-ttu-id="e1036-121"><dt>**msiMessageTypeError**</dt> <dt>&H01000000</dt></span><span class="sxs-lookup"><span data-stu-id="e1036-121"><dt>**msiMessageTypeError**</dt> <dt>&H01000000</dt></span></span> </dl>                                     | <span data-ttu-id="e1036-122">Message d’erreur mis en forme, \[ 1 \] est le numéro de message dans la [table d’erreurs](error-table.md).</span><span class="sxs-lookup"><span data-stu-id="e1036-122">Formatted error message, \[1\] is message number in [Error table](error-table.md).</span></span><br/>                                               |
| <span id="msiMessageTypeWarning"></span><span id="msimessagetypewarning"></span><span id="MSIMESSAGETYPEWARNING"></span><dl> <span data-ttu-id="e1036-123"><dt>**msiMessageTypeWarning**</dt> <dt>&H02000000</dt></span><span class="sxs-lookup"><span data-stu-id="e1036-123"><dt>**msiMessageTypeWarning**</dt> <dt>&H02000000</dt></span></span> </dl>                             | <span data-ttu-id="e1036-124">Message d’avertissement mis en forme, \[ 1 \] est le numéro de message dans la [table d’erreurs](error-table.md).</span><span class="sxs-lookup"><span data-stu-id="e1036-124">Formatted warning message, \[1\] is message number in [Error table](error-table.md).</span></span><br/>                                             |
| <span id="msiMessageTypeUser_"></span><span id="msimessagetypeuser_"></span><span id="MSIMESSAGETYPEUSER_"></span><dl> <span data-ttu-id="e1036-125"><dt> **msiMessageTypeUser**</dt> <dt>&H03000000</dt></span><span class="sxs-lookup"><span data-stu-id="e1036-125"><dt>**msiMessageTypeUser** </dt> <dt>&H03000000</dt></span></span> </dl>                                     | <span data-ttu-id="e1036-126">Message de demande utilisateur, \[ 1 \] est le numéro de message dans la [table d’erreurs](error-table.md).</span><span class="sxs-lookup"><span data-stu-id="e1036-126">User request message, \[1\] is message number in [Error table](error-table.md).</span></span><br/>                                                  |
| <span id="msiMessageTypeInfo"></span><span id="msimessagetypeinfo"></span><span id="MSIMESSAGETYPEINFO"></span><dl> <span data-ttu-id="e1036-127"><dt>**msiMessageTypeInfo**</dt> <dt>&H04000000</dt></span><span class="sxs-lookup"><span data-stu-id="e1036-127"><dt>**msiMessageTypeInfo**</dt> <dt>&H04000000</dt></span></span> </dl>                                         | <span data-ttu-id="e1036-128">Message d’information pour le journal, à ne pas afficher.</span><span class="sxs-lookup"><span data-stu-id="e1036-128">Informative message for log, not to be displayed.</span></span><br/>                                                                                 |
| <span id="msiMessageTypeFilesInUse"></span><span id="msimessagetypefilesinuse"></span><span id="MSIMESSAGETYPEFILESINUSE"></span><dl> <span data-ttu-id="e1036-129"><dt>**msiMessageTypeFilesInUse**</dt> <dt>&H05000000</dt></span><span class="sxs-lookup"><span data-stu-id="e1036-129"><dt>**msiMessageTypeFilesInUse**</dt> <dt>&H05000000</dt></span></span> </dl>                 | <span data-ttu-id="e1036-130">Liste des fichiers en cours d’utilisation qui doivent être remplacés.</span><span class="sxs-lookup"><span data-stu-id="e1036-130">List of files in use that need to be replaced.</span></span><br/>                                                                                    |
| <span id="msiMessageTypeResolveSource"></span><span id="msimessagetyperesolvesource"></span><span id="MSIMESSAGETYPERESOLVESOURCE"></span><dl> <span data-ttu-id="e1036-131"><dt>**msiMessageTypeResolveSource**</dt> <dt>&H06000000</dt></span><span class="sxs-lookup"><span data-stu-id="e1036-131"><dt>**msiMessageTypeResolveSource**</dt> <dt>&H06000000</dt></span></span> </dl>     | <span data-ttu-id="e1036-132">Demandez à déterminer un emplacement source valide.</span><span class="sxs-lookup"><span data-stu-id="e1036-132">Request to determine a valid source location.</span></span><br/>                                                                                     |
| <span id="msiMessageTypeOutOfDiskSpace"></span><span id="msimessagetypeoutofdiskspace"></span><span id="MSIMESSAGETYPEOUTOFDISKSPACE"></span><dl> <span data-ttu-id="e1036-133"><dt>**msiMessageTypeOutOfDiskSpace**</dt> <dt>&H07000000</dt></span><span class="sxs-lookup"><span data-stu-id="e1036-133"><dt>**msiMessageTypeOutOfDiskSpace**</dt> <dt>&H07000000</dt></span></span> </dl> | <span data-ttu-id="e1036-134">Message d’espace disque insuffisant.</span><span class="sxs-lookup"><span data-stu-id="e1036-134">Insufficient disk space message.</span></span><br/>                                                                                                  |
| <span id="msiMessageTypeActionStart"></span><span id="msimessagetypeactionstart"></span><span id="MSIMESSAGETYPEACTIONSTART"></span><dl> <span data-ttu-id="e1036-135"><dt>**msiMessageTypeActionStart**</dt> <dt>&H08000000</dt></span><span class="sxs-lookup"><span data-stu-id="e1036-135"><dt>**msiMessageTypeActionStart**</dt> <dt>&H08000000</dt></span></span> </dl>             | <span data-ttu-id="e1036-136">Début de l’action, \[ 1 \] nom d’action, \[ 2 \] Description, \[ 3 \] modèle pour les messages ACTIONDATA.</span><span class="sxs-lookup"><span data-stu-id="e1036-136">Start of action, \[1\] action name, \[2\] description, \[3\] template for ACTIONDATA messages.</span></span><br/>                                    |
| <span id="msiMessageTypeActionData"></span><span id="msimessagetypeactiondata"></span><span id="MSIMESSAGETYPEACTIONDATA"></span><dl> <span data-ttu-id="e1036-137"><dt>**msiMessageTypeActionData**</dt> <dt>&H09000000</dt></span><span class="sxs-lookup"><span data-stu-id="e1036-137"><dt>**msiMessageTypeActionData**</dt> <dt>&H09000000</dt></span></span> </dl>                 | <span data-ttu-id="e1036-138">Données d’action.</span><span class="sxs-lookup"><span data-stu-id="e1036-138">Action data.</span></span> <span data-ttu-id="e1036-139">Les champs d’enregistrement correspondent au modèle de message ACTIONSTART.</span><span class="sxs-lookup"><span data-stu-id="e1036-139">Record fields correspond to the template of ACTIONSTART message.</span></span><br/>                                                     |
| <span id="msiMessageTypeProgress"></span><span id="msimessagetypeprogress"></span><span id="MSIMESSAGETYPEPROGRESS"></span><dl> <span data-ttu-id="e1036-140"><dt>**msiMessageTypeProgress**</dt> <dt>&H0A000000</dt></span><span class="sxs-lookup"><span data-stu-id="e1036-140"><dt>**msiMessageTypeProgress**</dt> <dt>&H0A000000</dt></span></span> </dl>                         | <span data-ttu-id="e1036-141">Informations sur la barre de progression.</span><span class="sxs-lookup"><span data-stu-id="e1036-141">Progress bar information.</span></span> <span data-ttu-id="e1036-142">Consultez la description des champs d’enregistrement ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="e1036-142">See the description of record fields below.</span></span><br/>                                                             |
| <span id="msiMessageTypeCommonData_"></span><span id="msimessagetypecommondata_"></span><span id="MSIMESSAGETYPECOMMONDATA_"></span><dl> <span data-ttu-id="e1036-143"><dt> **msiMessageTypeCommonData**</dt> <dt>&H0B000000</dt></span><span class="sxs-lookup"><span data-stu-id="e1036-143"><dt>**msiMessageTypeCommonData** </dt> <dt>&H0B000000</dt></span></span> </dl>             | <span data-ttu-id="e1036-144">Pour activer le bouton Annuler défini \[ \] entre 1 et 2 \[ \] à 1.</span><span class="sxs-lookup"><span data-stu-id="e1036-144">To enable the Cancel button set \[1\] to 2 and \[2\] to 1.</span></span> <br/> <span data-ttu-id="e1036-145">Pour désactiver le bouton Annuler défini \[ \] entre 1 et 2 et \[ 2 \] à 0</span><span class="sxs-lookup"><span data-stu-id="e1036-145">To disable the Cancel button set \[1\] to 2 and \[2\] to 0</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="e1036-146">*enregistrement*</span><span class="sxs-lookup"><span data-stu-id="e1036-146">*record*</span></span> 
</dt> <dd>

<span data-ttu-id="e1036-147">Objet [**Record**](record-object.md) requis contenant un champ spécifique au message.</span><span class="sxs-lookup"><span data-stu-id="e1036-147">Required [**Record**](record-object.md) object containing a message-specific field.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e1036-148">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="e1036-148">Return value</span></span>



| <span data-ttu-id="e1036-149">Constante</span><span class="sxs-lookup"><span data-stu-id="e1036-149">Constant</span></span>                                                                                              | <span data-ttu-id="e1036-150">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1036-150">Value</span></span>         |
|-------------------------------------------------------------------------------------------------------|---------------|
| <dl> <span data-ttu-id="e1036-151"><dt>**msiMessageStatusError**</dt></span><span class="sxs-lookup"><span data-stu-id="e1036-151"><dt>**msiMessageStatusError**</dt></span></span> </dl>  | <span data-ttu-id="e1036-152">-1</span><span class="sxs-lookup"><span data-stu-id="e1036-152">-1</span></span><br/> |
| <dl> <span data-ttu-id="e1036-153"><dt>**msiMessageStatusNone**</dt></span><span class="sxs-lookup"><span data-stu-id="e1036-153"><dt>**msiMessageStatusNone**</dt></span></span> </dl>   | <span data-ttu-id="e1036-154">0</span><span class="sxs-lookup"><span data-stu-id="e1036-154">0</span></span><br/>  |
| <dl> <span data-ttu-id="e1036-155"><dt>**msiMessageStatusOk**</dt></span><span class="sxs-lookup"><span data-stu-id="e1036-155"><dt>**msiMessageStatusOk**</dt></span></span> </dl>     | <span data-ttu-id="e1036-156">1</span><span class="sxs-lookup"><span data-stu-id="e1036-156">1</span></span><br/>  |
| <dl> <span data-ttu-id="e1036-157"><dt>**msiMessageStatusCancel**</dt></span><span class="sxs-lookup"><span data-stu-id="e1036-157"><dt>**msiMessageStatusCancel**</dt></span></span> </dl> | <span data-ttu-id="e1036-158">2</span><span class="sxs-lookup"><span data-stu-id="e1036-158">2</span></span><br/>  |
| <dl> <span data-ttu-id="e1036-159"><dt>**msiMessageStatusAbort**</dt></span><span class="sxs-lookup"><span data-stu-id="e1036-159"><dt>**msiMessageStatusAbort**</dt></span></span> </dl>  | <span data-ttu-id="e1036-160">3</span><span class="sxs-lookup"><span data-stu-id="e1036-160">3</span></span><br/>  |
| <dl> <span data-ttu-id="e1036-161"><dt>**msiMessageStatusRetry**</dt></span><span class="sxs-lookup"><span data-stu-id="e1036-161"><dt>**msiMessageStatusRetry**</dt></span></span> </dl>  | <span data-ttu-id="e1036-162">4</span><span class="sxs-lookup"><span data-stu-id="e1036-162">4</span></span><br/>  |
| <dl> <span data-ttu-id="e1036-163"><dt>**msiMessageStatusIgnore**</dt></span><span class="sxs-lookup"><span data-stu-id="e1036-163"><dt>**msiMessageStatusIgnore**</dt></span></span> </dl> | <span data-ttu-id="e1036-164">5</span><span class="sxs-lookup"><span data-stu-id="e1036-164">5</span></span><br/>  |
| <dl> <span data-ttu-id="e1036-165"><dt>**msiMessageStatusYes**</dt></span><span class="sxs-lookup"><span data-stu-id="e1036-165"><dt>**msiMessageStatusYes**</dt></span></span> </dl>    | <span data-ttu-id="e1036-166">6</span><span class="sxs-lookup"><span data-stu-id="e1036-166">6</span></span><br/>  |
| <dl> <span data-ttu-id="e1036-167"><dt>**msiMessageStatusNo**</dt></span><span class="sxs-lookup"><span data-stu-id="e1036-167"><dt>**msiMessageStatusNo**</dt></span></span> </dl>     | <span data-ttu-id="e1036-168">7</span><span class="sxs-lookup"><span data-stu-id="e1036-168">7</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="e1036-169">Notes</span><span class="sxs-lookup"><span data-stu-id="e1036-169">Remarks</span></span>

<span data-ttu-id="e1036-170">**Champs d’enregistrement de message**</span><span class="sxs-lookup"><span data-stu-id="e1036-170">**Message Record Fields**</span></span>

<span data-ttu-id="e1036-171">La rubrique suivante décrit les définitions de champs d’enregistrement lorsque msiMessageTypeProgress est transmis comme type de message.</span><span class="sxs-lookup"><span data-stu-id="e1036-171">The following describes the record field definitions when msiMessageTypeProgress is passed as the message type.</span></span>

<span data-ttu-id="e1036-172">Le champ 1 spécifie le type de message de progression.</span><span class="sxs-lookup"><span data-stu-id="e1036-172">Field 1 specifies the type of the progress message.</span></span> <span data-ttu-id="e1036-173">La signification des autres champs dépend de la valeur de ce champ.</span><span class="sxs-lookup"><span data-stu-id="e1036-173">The meaning of the other fields depend upon the value in this field.</span></span> <span data-ttu-id="e1036-174">Les valeurs possibles qui peuvent être définies dans le champ 1 sont les suivantes.</span><span class="sxs-lookup"><span data-stu-id="e1036-174">The possible values that can be set into Field 1 are as follows.</span></span>



| <span data-ttu-id="e1036-175">Nom du message</span><span class="sxs-lookup"><span data-stu-id="e1036-175">Message name</span></span>     | <span data-ttu-id="e1036-176">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1036-176">Value</span></span> | <span data-ttu-id="e1036-177">Description du champ 1</span><span class="sxs-lookup"><span data-stu-id="e1036-177">Field 1 description</span></span>                                                                                                 |
|------------------|-------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1036-178">MasterReset</span><span class="sxs-lookup"><span data-stu-id="e1036-178">MasterReset</span></span>      | <span data-ttu-id="e1036-179">0</span><span class="sxs-lookup"><span data-stu-id="e1036-179">0</span></span>     | <span data-ttu-id="e1036-180">Réinitialise la barre de progression et définit le nombre total de graduations attendu dans la barre.</span><span class="sxs-lookup"><span data-stu-id="e1036-180">Resets progress bar and sets the expected total number of ticks in the bar.</span></span>                                         |
| <span data-ttu-id="e1036-181">ActionInfo</span><span class="sxs-lookup"><span data-stu-id="e1036-181">ActionInfo</span></span>       | <span data-ttu-id="e1036-182">1</span><span class="sxs-lookup"><span data-stu-id="e1036-182">1</span></span>     | <span data-ttu-id="e1036-183">Fournit des informations relatives aux messages de progression qui doivent être envoyés par l’action en cours.</span><span class="sxs-lookup"><span data-stu-id="e1036-183">Provides information related to progress messages to be sent by the current action.</span></span>                                 |
| <span data-ttu-id="e1036-184">ProgressReport</span><span class="sxs-lookup"><span data-stu-id="e1036-184">ProgressReport</span></span>   | <span data-ttu-id="e1036-185">2</span><span class="sxs-lookup"><span data-stu-id="e1036-185">2</span></span>     | <span data-ttu-id="e1036-186">Incrémente la barre de progression.</span><span class="sxs-lookup"><span data-stu-id="e1036-186">Increments the progress bar.</span></span>                                                                                        |
| <span data-ttu-id="e1036-187">ProgressAddition</span><span class="sxs-lookup"><span data-stu-id="e1036-187">ProgressAddition</span></span> | <span data-ttu-id="e1036-188">3</span><span class="sxs-lookup"><span data-stu-id="e1036-188">3</span></span>     | <span data-ttu-id="e1036-189">Permet à une action (telle que CustomAction) d’ajouter des graduations au nombre total attendu de la progression de la barre de progression.</span><span class="sxs-lookup"><span data-stu-id="e1036-189">Enables an action (such as CustomAction) to add ticks to the expected total number of progress of the progress bar.</span></span> |



 

<span data-ttu-id="e1036-190">La signification du champ 2 dépend de la valeur du champ 1 comme suit.</span><span class="sxs-lookup"><span data-stu-id="e1036-190">The meaning of Field 2 depends upon the value in Field 1 as follows.</span></span>



| <span data-ttu-id="e1036-191">Valeur champ 1</span><span class="sxs-lookup"><span data-stu-id="e1036-191">Field 1 value</span></span> | <span data-ttu-id="e1036-192">Description du champ 2</span><span class="sxs-lookup"><span data-stu-id="e1036-192">Field 2 description</span></span>                                                                                        |
|---------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1036-193">0</span><span class="sxs-lookup"><span data-stu-id="e1036-193">0</span></span>             | <span data-ttu-id="e1036-194">Nombre total de graduations attendu dans la barre de progression.</span><span class="sxs-lookup"><span data-stu-id="e1036-194">Expected total number of ticks in the progress bar.</span></span>                                                        |
| <span data-ttu-id="e1036-195">1</span><span class="sxs-lookup"><span data-stu-id="e1036-195">1</span></span>             | <span data-ttu-id="e1036-196">Nombre de graduations que la barre de progression déplace pour chaque message ActionData.</span><span class="sxs-lookup"><span data-stu-id="e1036-196">Number of ticks the progress bar moves for each ActionData message.</span></span> <span data-ttu-id="e1036-197">Ce champ est ignoré si le champ 3 est égal à 0.</span><span class="sxs-lookup"><span data-stu-id="e1036-197">This field is ignored if Field 3 is 0.</span></span> |
| <span data-ttu-id="e1036-198">2</span><span class="sxs-lookup"><span data-stu-id="e1036-198">2</span></span>             | <span data-ttu-id="e1036-199">Nombre de graduations de la barre de progression.</span><span class="sxs-lookup"><span data-stu-id="e1036-199">Number of ticks the progress bar has moved.</span></span>                                                                |
| <span data-ttu-id="e1036-200">3</span><span class="sxs-lookup"><span data-stu-id="e1036-200">3</span></span>             | <span data-ttu-id="e1036-201">Nombre de graduations à ajouter à la progression attendue totale.</span><span class="sxs-lookup"><span data-stu-id="e1036-201">Number of ticks to add to total expected progress.</span></span>                                                         |



 

<span data-ttu-id="e1036-202">La signification du champ 3 dépend de la valeur du champ 1 comme suit.</span><span class="sxs-lookup"><span data-stu-id="e1036-202">The meaning of Field 3 depends upon the value in Field 1 as follows.</span></span>



| <span data-ttu-id="e1036-203">Valeur champ 1</span><span class="sxs-lookup"><span data-stu-id="e1036-203">Field 1 value</span></span> | <span data-ttu-id="e1036-204">Valeur champ 3</span><span class="sxs-lookup"><span data-stu-id="e1036-204">Field 3 value</span></span> | <span data-ttu-id="e1036-205">Description du champ 3</span><span class="sxs-lookup"><span data-stu-id="e1036-205">Field 3 description</span></span>                                                                                             |
|---------------|---------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1036-206">0</span><span class="sxs-lookup"><span data-stu-id="e1036-206">0</span></span>             | <span data-ttu-id="e1036-207">0</span><span class="sxs-lookup"><span data-stu-id="e1036-207">0</span></span>             | <span data-ttu-id="e1036-208">Barre de progression vers l’avant (de gauche à droite)</span><span class="sxs-lookup"><span data-stu-id="e1036-208">Forward progress bar (left to right)</span></span>                                                                            |
|               | <span data-ttu-id="e1036-209">1</span><span class="sxs-lookup"><span data-stu-id="e1036-209">1</span></span>             | <span data-ttu-id="e1036-210">Barre de progression vers l’arrière (de droite à gauche)</span><span class="sxs-lookup"><span data-stu-id="e1036-210">Backward progress bar (right to left)</span></span>                                                                           |
| <span data-ttu-id="e1036-211">1</span><span class="sxs-lookup"><span data-stu-id="e1036-211">1</span></span>             | <span data-ttu-id="e1036-212">0</span><span class="sxs-lookup"><span data-stu-id="e1036-212">0</span></span>             | <span data-ttu-id="e1036-213">L’action en cours enverra des messages ProgressReport explicites.</span><span class="sxs-lookup"><span data-stu-id="e1036-213">The current action will send explicit ProgressReport messages.</span></span>                                                  |
|               | <span data-ttu-id="e1036-214">1</span><span class="sxs-lookup"><span data-stu-id="e1036-214">1</span></span>             | <span data-ttu-id="e1036-215">Incrémente la barre de progression du nombre de graduations spécifié dans le champ 2 chaque fois qu’un message ActionData est envoyé.</span><span class="sxs-lookup"><span data-stu-id="e1036-215">Increment the progress bar by the number of ticks specified in Field 2 each time an ActionData message is sent.</span></span> |
| <span data-ttu-id="e1036-216">2</span><span class="sxs-lookup"><span data-stu-id="e1036-216">2</span></span>             | <span data-ttu-id="e1036-217">Inutilisé</span><span class="sxs-lookup"><span data-stu-id="e1036-217">Unused</span></span>        |                                                                                                                 |
| <span data-ttu-id="e1036-218">3</span><span class="sxs-lookup"><span data-stu-id="e1036-218">3</span></span>             | <span data-ttu-id="e1036-219">Inutilisé</span><span class="sxs-lookup"><span data-stu-id="e1036-219">Unused</span></span>        |                                                                                                                 |



 

<span data-ttu-id="e1036-220">La signification du champ 4 dépend de la valeur du champ 1 comme suit.</span><span class="sxs-lookup"><span data-stu-id="e1036-220">The meaning of Field 4 depends upon the value in Field 1 as follows.</span></span>



| <span data-ttu-id="e1036-221">Valeur champ 1</span><span class="sxs-lookup"><span data-stu-id="e1036-221">Field 1 value</span></span> | <span data-ttu-id="e1036-222">Valeur champ 4</span><span class="sxs-lookup"><span data-stu-id="e1036-222">Field 4 value</span></span> | <span data-ttu-id="e1036-223">Description du champ 4</span><span class="sxs-lookup"><span data-stu-id="e1036-223">Field 4 description</span></span>                                                                                                                                 |
|---------------|---------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1036-224">0</span><span class="sxs-lookup"><span data-stu-id="e1036-224">0</span></span>             | <span data-ttu-id="e1036-225">0</span><span class="sxs-lookup"><span data-stu-id="e1036-225">0</span></span>             | <span data-ttu-id="e1036-226">L’exécution est en cours.</span><span class="sxs-lookup"><span data-stu-id="e1036-226">Execution is in progress.</span></span> <span data-ttu-id="e1036-227">Dans ce cas, l’interface utilisateur peut calculer et afficher le temps restant.</span><span class="sxs-lookup"><span data-stu-id="e1036-227">In this case, the UI could calculate and display the time remaining.</span></span>                                                      |
|               | <span data-ttu-id="e1036-228">1</span><span class="sxs-lookup"><span data-stu-id="e1036-228">1</span></span>             | <span data-ttu-id="e1036-229">Création du script d’exécution.</span><span class="sxs-lookup"><span data-stu-id="e1036-229">Creating the execution script.</span></span> <span data-ttu-id="e1036-230">Dans ce cas, l’interface utilisateur peut afficher un message pour patienter pendant que le programme d’installation a terminé la préparation de l’installation.</span><span class="sxs-lookup"><span data-stu-id="e1036-230">In this case, the UI could display a message to please wait while the installer finishes preparing the installation.</span></span> |
| <span data-ttu-id="e1036-231">1</span><span class="sxs-lookup"><span data-stu-id="e1036-231">1</span></span>             | <span data-ttu-id="e1036-232">Inutilisé</span><span class="sxs-lookup"><span data-stu-id="e1036-232">Unused</span></span>        |                                                                                                                                                     |
| <span data-ttu-id="e1036-233">2</span><span class="sxs-lookup"><span data-stu-id="e1036-233">2</span></span>             | <span data-ttu-id="e1036-234">Inutilisé</span><span class="sxs-lookup"><span data-stu-id="e1036-234">Unused</span></span>        |                                                                                                                                                     |
| <span data-ttu-id="e1036-235">3</span><span class="sxs-lookup"><span data-stu-id="e1036-235">3</span></span>             | <span data-ttu-id="e1036-236">Inutilisé</span><span class="sxs-lookup"><span data-stu-id="e1036-236">Unused</span></span>        |                                                                                                                                                     |



 

<span data-ttu-id="e1036-237">**Affichage des boîtes de message**</span><span class="sxs-lookup"><span data-stu-id="e1036-237">**Displaying Message Boxes**</span></span>

<span data-ttu-id="e1036-238">Pour afficher une boîte de message avec des boutons et des icônes de type push, calculez la valeur de *genre* en ajoutant les styles de zone de message standard utilisés par **MessageBox** et **MessageBoxEx** à **msiMessageTypeError**, **msiMessageTypeWarning** ou **msiTypeUser**.</span><span class="sxs-lookup"><span data-stu-id="e1036-238">To display a message box with push buttons and icons, calculate the value of *kind* by adding the standard message box styles used by **MessageBox** and **MessageBoxEx** to **msiMessageTypeError**, **msiMessageTypeWarning**, or **msiTypeUser**.</span></span> <span data-ttu-id="e1036-239">Les options de bouton de commande disponibles pour VBScript sont vbOKOnly (Mo \_ OK), vbOKCancel (MB \_ OKCANCEL), VBABORTRETRYIGNORE (Mo \_ ABORTRETRYIGNORE), vbYesNoCancel (Mo \_ YESNOCANCEL), vbYesNo (Mo \_ YesNo) et vbRetryCancel (Mo \_ RETRYCANCEL).</span><span class="sxs-lookup"><span data-stu-id="e1036-239">The available push button options for VBScript are vbOKOnly (MB\_OK), vbOKCancel (MB\_OKCANCEL), vbAbortRetryIgnore (MB\_ABORTRETRYIGNORE), vbYesNoCancel (MB\_YESNOCANCEL), vbYesNo (MB\_YESNO), and vbRetryCancel (MB\_RETRYCANCEL).</span></span> <span data-ttu-id="e1036-240">Les options d’icône disponibles pour VBScript sont vbCritical (Mo \_ ICONERROR), vbQuestion (MB \_ ICONQUESTION), VBEXCLAMATION (Mo \_ ICONWARNING) et vbInformation (Mo \_ ICONINFORMATION).</span><span class="sxs-lookup"><span data-stu-id="e1036-240">The available icon options for VBScript are vbCritical (MB\_ICONERROR), vbQuestion (MB\_ICONQUESTION), vbExclamation (MB\_ICONWARNING), and vbInformation (MB\_ICONINFORMATION).</span></span>

<span data-ttu-id="e1036-241">Par exemple, l’appel suivant envoie un message **msiMessageTypeError** avec l’icône vbExclamation et les boutons vbYesNo.</span><span class="sxs-lookup"><span data-stu-id="e1036-241">For example, the following call sends a **msiMessageTypeError** message with the vbExclamation icon and vbYesNo buttons.</span></span>


```VB
Session.Message &H01000034, record
```



<span data-ttu-id="e1036-242">Si une action personnalisée appelle la méthode de **message** , l’action personnalisée doit être en mesure de gérer une annulation par l’utilisateur et de retourner **msiDoActionStatusUserExit**.</span><span class="sxs-lookup"><span data-stu-id="e1036-242">If a custom action calls the **Message** method, the custom action should be capable of handling a cancellation by the user and should return **msiDoActionStatusUserExit**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1036-243">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="e1036-243">Requirements</span></span>



| <span data-ttu-id="e1036-244">Condition requise</span><span class="sxs-lookup"><span data-stu-id="e1036-244">Requirement</span></span> | <span data-ttu-id="e1036-245">Valeur</span><span class="sxs-lookup"><span data-stu-id="e1036-245">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1036-246">Version</span><span class="sxs-lookup"><span data-stu-id="e1036-246">Version</span></span><br/> | <span data-ttu-id="e1036-247">Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7.</span><span class="sxs-lookup"><span data-stu-id="e1036-247">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="e1036-248">Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="e1036-248">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="e1036-249">Windows Installer sur Windows Server 2003 ou Windows XP</span><span class="sxs-lookup"><span data-stu-id="e1036-249">Windows Installer on Windows Server 2003 or Windows XP</span></span><br/> |
| <span data-ttu-id="e1036-250">DLL</span><span class="sxs-lookup"><span data-stu-id="e1036-250">DLL</span></span><br/>     | <dl> <span data-ttu-id="e1036-251"><dt>Msi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1036-251"><dt>Msi.dll</dt></span></span> </dl>                                                                                                                                                                      |
| <span data-ttu-id="e1036-252">IID</span><span class="sxs-lookup"><span data-stu-id="e1036-252">IID</span></span><br/>     | <span data-ttu-id="e1036-253">IID \_ ISession est défini en tant que 000C109E-0000-0000-C000-000000000046</span><span class="sxs-lookup"><span data-stu-id="e1036-253">IID\_ISession is defined as 000C109E-0000-0000-C000-000000000046</span></span><br/>                                                                                                                                                                             |



 

 
