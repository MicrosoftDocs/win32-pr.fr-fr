---
description: La fonction FindNextPrinterChangeNotification récupère des informations sur la notification de modification la plus récente pour un objet de notification de modification associé à une imprimante ou à un serveur d’impression.
ms.assetid: ea7774ae-361f-41e4-bbc6-3f100028b22a
title: FindNextPrinterChangeNotification, fonction (winspool. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FindNextPrinterChangeNotification
api_type:
- DllExport
api_location:
- Spoolss.dll
ms.openlocfilehash: ef3ece0d4831409d79e2152cf7b6a37d6bbdc8b3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866181"
---
# <a name="findnextprinterchangenotification-function"></a><span data-ttu-id="d5219-103">FindNextPrinterChangeNotification fonction)</span><span class="sxs-lookup"><span data-stu-id="d5219-103">FindNextPrinterChangeNotification function</span></span>

<span data-ttu-id="d5219-104">La fonction **FindNextPrinterChangeNotification** récupère des informations sur la notification de modification la plus récente pour un objet de notification de modification associé à une imprimante ou à un serveur d’impression.</span><span class="sxs-lookup"><span data-stu-id="d5219-104">The **FindNextPrinterChangeNotification** function retrieves information about the most recent change notification for a change notification object associated with a printer or print server.</span></span> <span data-ttu-id="d5219-105">Appelez cette fonction quand une opération d’attente sur l’objet de notification de modification est satisfaite.</span><span class="sxs-lookup"><span data-stu-id="d5219-105">Call this function when a wait operation on the change notification object is satisfied.</span></span>

<span data-ttu-id="d5219-106">La fonction réinitialise également l’objet de notification de modification à l’état non signalé.</span><span class="sxs-lookup"><span data-stu-id="d5219-106">The function also resets the change notification object to the not-signaled state.</span></span> <span data-ttu-id="d5219-107">Vous pouvez ensuite utiliser l’objet dans une autre opération d’attente pour continuer à surveiller l’imprimante ou le serveur d’impression.</span><span class="sxs-lookup"><span data-stu-id="d5219-107">You can then use the object in another wait operation to continue monitoring the printer or print server.</span></span> <span data-ttu-id="d5219-108">Le système d’exploitation affecte à l’objet l’état signalé la prochaine fois qu’un jeu de modifications spécifié se produit sur l’imprimante ou le serveur d’impression.</span><span class="sxs-lookup"><span data-stu-id="d5219-108">The operating system will set the object to the signaled state the next time one of a specified set of changes occurs to the printer or print server.</span></span> <span data-ttu-id="d5219-109">La fonction [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) crée l’objet de notification de modification et spécifie l’ensemble de modifications à surveiller.</span><span class="sxs-lookup"><span data-stu-id="d5219-109">The [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) function creates the change notification object and specifies the set of changes to be monitored.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5219-110">Syntaxe</span><span class="sxs-lookup"><span data-stu-id="d5219-110">Syntax</span></span>


```C++
BOOL FindNextPrinterChangeNotification(
  _In_      HANDLE hChange,
  _Out_opt_ PDWORD pdwChange,
  _In_opt_  LPVOID pPrinterNotifyOptions,
  _Out_opt_ LPVOID *ppPrinterNotifyInfo
);
```



## <a name="parameters"></a><span data-ttu-id="d5219-111">Paramètres</span><span class="sxs-lookup"><span data-stu-id="d5219-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5219-112">*hChange* \[ dans\]</span><span class="sxs-lookup"><span data-stu-id="d5219-112">*hChange* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5219-113">Handle d’un objet de notification de modification associé à une imprimante ou à un serveur d’impression.</span><span class="sxs-lookup"><span data-stu-id="d5219-113">A handle to a change notification object associated with a printer or print server.</span></span> <span data-ttu-id="d5219-114">Vous obtenez ce type de handle en appelant la fonction [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) .</span><span class="sxs-lookup"><span data-stu-id="d5219-114">You obtain such a handle by calling the [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) function.</span></span> <span data-ttu-id="d5219-115">Le système d’exploitation définit cet objet de notification de modification à l’état signalé lorsqu’il détecte l’une des modifications spécifiées dans le filtre de notification de modification de l’objet.</span><span class="sxs-lookup"><span data-stu-id="d5219-115">The operating system sets this change notification object to the signaled state when it detects one of the changes specified in the object's change notification filter.</span></span>

</dd> <dt>

<span data-ttu-id="d5219-116">*pdwChange* \[ out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="d5219-116">*pdwChange* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d5219-117">Pointeur vers une variable dont les bits sont définis pour indiquer les modifications qui se sont produites pour provoquer la notification la plus récente.</span><span class="sxs-lookup"><span data-stu-id="d5219-117">A pointer to a variable whose bits are set to indicate the changes that occurred to cause the most recent notification.</span></span> <span data-ttu-id="d5219-118">Les indicateurs de bits qui peuvent être définis correspondent à ceux spécifiés dans le paramètre *fdwFilter* de l’appel [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) .</span><span class="sxs-lookup"><span data-stu-id="d5219-118">The bit flags that might be set correspond to those specified in the *fdwFilter* parameter of the [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) call.</span></span> <span data-ttu-id="d5219-119">Le système définit un ou plusieurs des indicateurs binaires suivants.</span><span class="sxs-lookup"><span data-stu-id="d5219-119">The system sets one or more of the following bit flags.</span></span>



| <span data-ttu-id="d5219-120">Valeur</span><span class="sxs-lookup"><span data-stu-id="d5219-120">Value</span></span>                                                                                                                                                                                                                                             | <span data-ttu-id="d5219-121">Signification</span><span class="sxs-lookup"><span data-stu-id="d5219-121">Meaning</span></span>                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span id="PRINTER_CHANGE_ADD_FORM"></span><span id="printer_change_add_form"></span><dl> <span data-ttu-id="d5219-122"><dt>**\_Ajouter un \_ \_ formulaire de modification d’imprimante**</dt></span><span class="sxs-lookup"><span data-stu-id="d5219-122"><dt>**PRINTER\_CHANGE\_ADD\_FORM**</dt></span></span> </dl>                                                     | <span data-ttu-id="d5219-123">Un formulaire a été ajouté au serveur.</span><span class="sxs-lookup"><span data-stu-id="d5219-123">A form was added to the server.</span></span><br/>                |
| <span id="PRINTER_CHANGE_ADD_JOB"></span><span id="printer_change_add_job"></span><dl> <span data-ttu-id="d5219-124"><dt>**changement d’imprimante \_ \_ Ajouter un \_ travail**</dt></span><span class="sxs-lookup"><span data-stu-id="d5219-124"><dt>**PRINTER\_CHANGE\_ADD\_JOB**</dt></span></span> </dl>                                                        | <span data-ttu-id="d5219-125">Un travail d’impression a été envoyé à l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="d5219-125">A print job was sent to the printer.</span></span><br/>           |
| <span id="PRINTER_CHANGE_ADD_PORT"></span><span id="printer_change_add_port"></span><dl> <span data-ttu-id="d5219-126"><dt>**changement d’imprimante \_ \_ Ajouter un \_ port**</dt></span><span class="sxs-lookup"><span data-stu-id="d5219-126"><dt>**PRINTER\_CHANGE\_ADD\_PORT**</dt></span></span> </dl>                                                     | <span data-ttu-id="d5219-127">Un port ou une analyse a été ajouté au serveur.</span><span class="sxs-lookup"><span data-stu-id="d5219-127">A port or monitor was added to the server.</span></span><br/>     |
| <span id="PRINTER_CHANGE_ADD_PRINT_PROCESSOR"></span><span id="printer_change_add_print_processor"></span><dl> <span data-ttu-id="d5219-128"><dt>**modification de l’imprimante \_ \_ Ajouter un \_ processeur d’impression \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d5219-128"><dt>**PRINTER\_CHANGE\_ADD\_PRINT\_PROCESSOR**</dt></span></span> </dl>                   | <span data-ttu-id="d5219-129">Un processeur d’impression a été ajouté au serveur.</span><span class="sxs-lookup"><span data-stu-id="d5219-129">A print processor was added to the server.</span></span><br/>     |
| <span id="PRINTER_CHANGE_ADD_PRINTER"></span><span id="printer_change_add_printer"></span><dl> <span data-ttu-id="d5219-130"><dt>**modification de l’imprimante \_ \_ Ajouter l' \_ imprimante**</dt></span><span class="sxs-lookup"><span data-stu-id="d5219-130"><dt>**PRINTER\_CHANGE\_ADD\_PRINTER**</dt></span></span> </dl>                                            | <span data-ttu-id="d5219-131">Une imprimante a été ajoutée au serveur.</span><span class="sxs-lookup"><span data-stu-id="d5219-131">A printer was added to the server.</span></span><br/>             |
| <span id="PRINTER_CHANGE_ADD_PRINTER_DRIVER"></span><span id="printer_change_add_printer_driver"></span><dl> <span data-ttu-id="d5219-132"><dt>**changement d’imprimante \_ \_ Ajouter un \_ pilote d’imprimante \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d5219-132"><dt>**PRINTER\_CHANGE\_ADD\_PRINTER\_DRIVER**</dt></span></span> </dl>                      | <span data-ttu-id="d5219-133">Un pilote d’imprimante a été ajouté au serveur.</span><span class="sxs-lookup"><span data-stu-id="d5219-133">A printer driver was added to the server.</span></span><br/>      |
| <span id="PRINTER_CHANGE_CONFIGURE_PORT"></span><span id="printer_change_configure_port"></span><dl> <span data-ttu-id="d5219-134"><dt>**\_modifier le \_ port de configuration de l’imprimante \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d5219-134"><dt>**PRINTER\_CHANGE\_CONFIGURE\_PORT**</dt></span></span> </dl>                                   | <span data-ttu-id="d5219-135">Un port a été configuré sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="d5219-135">A port was configured on the server.</span></span><br/>           |
| <span id="PRINTER_CHANGE_DELETE_FORM"></span><span id="printer_change_delete_form"></span><dl> <span data-ttu-id="d5219-136"><dt>**\_formulaire de \_ Suppression de modification d’imprimante \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d5219-136"><dt>**PRINTER\_CHANGE\_DELETE\_FORM**</dt></span></span> </dl>                                            | <span data-ttu-id="d5219-137">Un formulaire a été supprimé du serveur.</span><span class="sxs-lookup"><span data-stu-id="d5219-137">A form was deleted from the server.</span></span><br/>            |
| <span id="PRINTER_CHANGE_DELETE_JOB"></span><span id="printer_change_delete_job"></span><dl> <span data-ttu-id="d5219-138"><dt>**\_tâche de \_ Suppression de modification d’imprimante \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d5219-138"><dt>**PRINTER\_CHANGE\_DELETE\_JOB**</dt></span></span> </dl>                                               | <span data-ttu-id="d5219-139">Un travail a été supprimé.</span><span class="sxs-lookup"><span data-stu-id="d5219-139">A job was deleted.</span></span><br/>                             |
| <span id="PRINTER_CHANGE_DELETE_PORT"></span><span id="printer_change_delete_port"></span><dl> <span data-ttu-id="d5219-140"><dt>**\_port de \_ Suppression de modification d’imprimante \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d5219-140"><dt>**PRINTER\_CHANGE\_DELETE\_PORT**</dt></span></span> </dl>                                            | <span data-ttu-id="d5219-141">Un port ou une analyse a été supprimé du serveur.</span><span class="sxs-lookup"><span data-stu-id="d5219-141">A port or monitor was deleted from the server.</span></span><br/> |
| <span id="PRINTER_CHANGE_DELETE_PRINT_PROCESSOR"></span><span id="printer_change_delete_print_processor"></span><dl> <span data-ttu-id="d5219-142"><dt>**changement d’imprimante- \_ \_ supprimer le \_ processeur d’impression \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d5219-142"><dt>**PRINTER\_CHANGE\_DELETE\_PRINT\_PROCESSOR**</dt></span></span> </dl>          | <span data-ttu-id="d5219-143">Un processeur d’impression a été supprimé du serveur.</span><span class="sxs-lookup"><span data-stu-id="d5219-143">A print processor was deleted from the server.</span></span><br/> |
| <span id="PRINTER_CHANGE_DELETE_PRINTER"></span><span id="printer_change_delete_printer"></span><dl> <span data-ttu-id="d5219-144"><dt>**modification de l’imprimante \_ \_ Supprimer l' \_ imprimante**</dt></span><span class="sxs-lookup"><span data-stu-id="d5219-144"><dt>**PRINTER\_CHANGE\_DELETE\_PRINTER**</dt></span></span> </dl>                                   | <span data-ttu-id="d5219-145">Une imprimante a été supprimée.</span><span class="sxs-lookup"><span data-stu-id="d5219-145">A printer was deleted.</span></span><br/>                         |
| <span id="PRINTER_CHANGE_DELETE_PRINTER_DRIVER"></span><span id="printer_change_delete_printer_driver"></span><dl> <span data-ttu-id="d5219-146"><dt>**modification de l’imprimante \_ \_ supprimer le \_ pilote d’imprimante \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d5219-146"><dt>**PRINTER\_CHANGE\_DELETE\_PRINTER\_DRIVER**</dt></span></span> </dl>             | <span data-ttu-id="d5219-147">Un pilote d’imprimante a été supprimé du serveur.</span><span class="sxs-lookup"><span data-stu-id="d5219-147">A printer driver was deleted from the server.</span></span><br/>  |
| <span id="PRINTER_CHANGE_FAILED_CONNECTION_PRINTER"></span><span id="printer_change_failed_connection_printer"></span><dl> <span data-ttu-id="d5219-148"><dt>**\_ \_ imprimante échec de \_ la modification de l’imprimante \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d5219-148"><dt>**PRINTER\_CHANGE\_FAILED\_CONNECTION\_PRINTER**</dt></span></span> </dl> | <span data-ttu-id="d5219-149">Une connexion d’imprimante a échoué.</span><span class="sxs-lookup"><span data-stu-id="d5219-149">A printer connection has failed.</span></span><br/>               |
| <span id="PRINTER_CHANGE_SET_FORM"></span><span id="printer_change_set_form"></span><dl> <span data-ttu-id="d5219-150"><dt>**\_formulaire de modification de l’imprimante \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d5219-150"><dt>**PRINTER\_CHANGE\_SET\_FORM**</dt></span></span> </dl>                                                     | <span data-ttu-id="d5219-151">Un formulaire a été défini sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="d5219-151">A form was set on the server.</span></span><br/>                  |
| <span id="PRINTER_CHANGE_SET_JOB"></span><span id="printer_change_set_job"></span><dl> <span data-ttu-id="d5219-152"><dt>**\_travail d' \_ ensemble de modifications d’imprimante \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d5219-152"><dt>**PRINTER\_CHANGE\_SET\_JOB**</dt></span></span> </dl>                                                        | <span data-ttu-id="d5219-153">Un travail a été défini.</span><span class="sxs-lookup"><span data-stu-id="d5219-153">A job was set.</span></span><br/>                                 |
| <span id="PRINTER_CHANGE_SET_PRINTER"></span><span id="printer_change_set_printer"></span><dl> <span data-ttu-id="d5219-154"><dt>**imprimante de \_ jeu de modifications d’imprimante \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d5219-154"><dt>**PRINTER\_CHANGE\_SET\_PRINTER**</dt></span></span> </dl>                                            | <span data-ttu-id="d5219-155">Une imprimante a été définie.</span><span class="sxs-lookup"><span data-stu-id="d5219-155">A printer was set.</span></span><br/>                             |
| <span id="PRINTER_CHANGE_SET_PRINTER_DRIVER"></span><span id="printer_change_set_printer_driver"></span><dl> <span data-ttu-id="d5219-156"><dt>**\_pilote d' \_ imprimante de jeu de modifications d’imprimante \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d5219-156"><dt>**PRINTER\_CHANGE\_SET\_PRINTER\_DRIVER**</dt></span></span> </dl>                      | <span data-ttu-id="d5219-157">Un pilote d’imprimante a été défini.</span><span class="sxs-lookup"><span data-stu-id="d5219-157">A printer driver was set.</span></span><br/>                      |
| <span id="PRINTER_CHANGE_WRITE_JOB"></span><span id="printer_change_write_job"></span><dl> <span data-ttu-id="d5219-158"><dt>**\_travail d' \_ écriture de modification d’imprimante \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d5219-158"><dt>**PRINTER\_CHANGE\_WRITE\_JOB**</dt></span></span> </dl>                                                  | <span data-ttu-id="d5219-159">Les données du travail ont été écrites.</span><span class="sxs-lookup"><span data-stu-id="d5219-159">Job data was written.</span></span><br/>                          |
| <span id="PRINTER_CHANGE_TIMEOUT"></span><span id="printer_change_timeout"></span><dl> <span data-ttu-id="d5219-160"><dt>**\_délai de modification de l’imprimante \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d5219-160"><dt>**PRINTER\_CHANGE\_TIMEOUT**</dt></span></span> </dl>                                                         | <span data-ttu-id="d5219-161">Le travail a expiré.</span><span class="sxs-lookup"><span data-stu-id="d5219-161">The job timed out.</span></span><br/>                             |
| <span id="PRINTER_CHANGE_SERVER"></span><span id="printer_change_server"></span><dl> <span data-ttu-id="d5219-162"><dt>**\_serveur de changement d’imprimante \_**</dt></span><span class="sxs-lookup"><span data-stu-id="d5219-162"><dt>**PRINTER\_CHANGE\_SERVER**</dt></span></span> </dl>                                                            | <span data-ttu-id="d5219-163">Windows 7 : une modification s’est produite sur le serveur.</span><span class="sxs-lookup"><span data-stu-id="d5219-163">Windows 7: A change occurred on the server.</span></span><br/>    |



 

</dd> <dt>

<span data-ttu-id="d5219-164">*pPrinterNotifyOptions* \[ dans, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="d5219-164">*pPrinterNotifyOptions* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d5219-165">Pointeur vers une structure [**d' \_ \_ options de notification d’imprimante**](printer-notify-options.md) .</span><span class="sxs-lookup"><span data-stu-id="d5219-165">A pointer to a [**PRINTER\_NOTIFY\_OPTIONS**](printer-notify-options.md) structure.</span></span> <span data-ttu-id="d5219-166">Définissez le membre **Flags** de cette structure **sur \_ options Notify d’imprimante \_ \_ Actualiser** pour que la fonction retourne les données actuelles pour tous les champs d’informations d’imprimante analysés.</span><span class="sxs-lookup"><span data-stu-id="d5219-166">Set the **Flags** member of this structure to **PRINTER\_NOTIFY\_OPTIONS\_REFRESH**, to cause the function to return the current data for all monitored printer information fields.</span></span> <span data-ttu-id="d5219-167">La fonction ignore tous les autres membres de la structure.</span><span class="sxs-lookup"><span data-stu-id="d5219-167">The function ignores all other members of the structure.</span></span> <span data-ttu-id="d5219-168">Ce paramètre peut être **NULL**.</span><span class="sxs-lookup"><span data-stu-id="d5219-168">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d5219-169">*ppPrinterNotifyInfo* \[ out, facultatif\]</span><span class="sxs-lookup"><span data-stu-id="d5219-169">*ppPrinterNotifyInfo* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d5219-170">Pointeur vers une variable pointeur qui reçoit un pointeur vers une mémoire tampon en lecture seule allouée par le système.</span><span class="sxs-lookup"><span data-stu-id="d5219-170">A pointer to a pointer variable that receives a pointer to a system-allocated, read-only buffer.</span></span> <span data-ttu-id="d5219-171">Appelez la fonction [**FreePrinterNotifyInfo**](freeprinternotifyinfo.md) pour libérer la mémoire tampon lorsque vous n’en avez plus besoin.</span><span class="sxs-lookup"><span data-stu-id="d5219-171">Call the [**FreePrinterNotifyInfo**](freeprinternotifyinfo.md) function to free the buffer when you are finished with it.</span></span> <span data-ttu-id="d5219-172">Ce paramètre peut avoir la **valeur null** si aucune information n’est requise.</span><span class="sxs-lookup"><span data-stu-id="d5219-172">This parameter can be **NULL** if no information is required.</span></span>

<span data-ttu-id="d5219-173">La mémoire tampon contient une structure d' [**\_ \_ informations de notification d’imprimante**](printer-notify-info.md) , qui contient un tableau de structures de [**\_ \_ \_ données d’informations de notification d’imprimante**](printer-notify-info-data.md) .</span><span class="sxs-lookup"><span data-stu-id="d5219-173">The buffer contains a [**PRINTER\_NOTIFY\_INFO**](printer-notify-info.md) structure, which contains an array of [**PRINTER\_NOTIFY\_INFO\_DATA**](printer-notify-info-data.md) structures.</span></span> <span data-ttu-id="d5219-174">Chaque élément du tableau contient des informations sur l’un des champs spécifiés dans le paramètre *pPrinterNotifyOptions* de l’appel [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) .</span><span class="sxs-lookup"><span data-stu-id="d5219-174">Each element of the array contains information about one of the fields specified in the *pPrinterNotifyOptions* parameter of the [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) call.</span></span> <span data-ttu-id="d5219-175">En règle générale, la fonction fournit uniquement des données pour les champs qui ont été modifiés pour provoquer la notification la plus récente.</span><span class="sxs-lookup"><span data-stu-id="d5219-175">Typically, the function provides data only for the fields that changed to cause the most recent notification.</span></span> <span data-ttu-id="d5219-176">Toutefois, si la structure vers laquelle pointe le paramètre *pPrinterNotifyOptions* spécifie l’actualisation des options de notification d' **imprimante \_ \_ \_**, la fonction fournit des données pour tous les champs surveillés.</span><span class="sxs-lookup"><span data-stu-id="d5219-176">However, if the structure pointed to by the *pPrinterNotifyOptions* parameter specifies **PRINTER\_NOTIFY\_OPTIONS\_REFRESH**, the function provides data for all monitored fields.</span></span>

<span data-ttu-id="d5219-177">Si le bit d' **informations de notification d’imprimante \_ \_ \_ rejeté** est défini dans le membre **Flags** de la structure d' [**informations de \_ notification \_ d’imprimante**](printer-notify-info.md) , un dépassement de capacité ou une erreur se sont produits et des notifications ont peut-être été perdues.</span><span class="sxs-lookup"><span data-stu-id="d5219-177">If the **PRINTER\_NOTIFY\_INFO\_DISCARDED** bit is set in the **Flags** member of the [**PRINTER\_NOTIFY\_INFO**](printer-notify-info.md) structure, an overflow or error occurred, and notifications may have been lost.</span></span> <span data-ttu-id="d5219-178">Dans ce cas, aucune notification supplémentaire n’est envoyée tant que vous n’avez pas effectué un deuxième appel **FindNextPrinterChangeNotification** qui spécifie l' **\_ \_ \_ actualisation des options Notify** de l’imprimante.</span><span class="sxs-lookup"><span data-stu-id="d5219-178">In this case, no additional notifications will be sent until you make a second **FindNextPrinterChangeNotification** call that specifies **PRINTER\_NOTIFY\_OPTIONS\_REFRESH**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5219-179">Valeur retournée</span><span class="sxs-lookup"><span data-stu-id="d5219-179">Return value</span></span>

<span data-ttu-id="d5219-180">Si la fonction est réussie, la valeur de retour est une valeur différente de zéro.</span><span class="sxs-lookup"><span data-stu-id="d5219-180">If the function succeeds, the return value is a nonzero value.</span></span>

<span data-ttu-id="d5219-181">Si la fonction échoue, la valeur de retour est égale à zéro.</span><span class="sxs-lookup"><span data-stu-id="d5219-181">If the function fails, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="d5219-182">Notes</span><span class="sxs-lookup"><span data-stu-id="d5219-182">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="d5219-183">Il s’agit d’une fonction de blocage ou synchrone qui peut ne pas être renvoyée immédiatement.</span><span class="sxs-lookup"><span data-stu-id="d5219-183">This is a blocking or synchronous function and might not return immediately.</span></span> <span data-ttu-id="d5219-184">La vitesse à laquelle cette fonction est retournée dépend des facteurs d’exécution tels que l’état du réseau, la configuration du serveur d’impression et les facteurs d’implémentation des pilotes d’imprimante qui sont difficiles à prédire lors de l’écriture d’une application.</span><span class="sxs-lookup"><span data-stu-id="d5219-184">How quickly this function returns depends on run-time factors such as network status, print server configuration, and printer driver implementation factors that are difficult to predict when writing an application.</span></span> <span data-ttu-id="d5219-185">L’appel de cette fonction à partir d’un thread qui gère l’interaction avec l’interface utilisateur peut faire que l’application semble ne pas répondre.</span><span class="sxs-lookup"><span data-stu-id="d5219-185">Calling this function from a thread that manages interaction with the user interface could make the application appear to be unresponsive.</span></span>

 

<span data-ttu-id="d5219-186">Appelez la fonction **FindNextPrinterChangeNotification** après la satisfaction d’une opération d’attente sur un objet de notification créé par [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) .</span><span class="sxs-lookup"><span data-stu-id="d5219-186">Call the **FindNextPrinterChangeNotification** function after a wait operation on a notification object created by [**FindFirstPrinterChangeNotification**](findfirstprinterchangenotification.md) has been satisfied.</span></span> <span data-ttu-id="d5219-187">L’appel de **FindNextPrinterChangeNotification** vous permet d’obtenir des informations sur la modification qui a respecté l’opération d’attente et réinitialise l’objet de notification afin qu’il puisse être signalé lorsque la modification suivante se produit.</span><span class="sxs-lookup"><span data-stu-id="d5219-187">Calling **FindNextPrinterChangeNotification** lets you obtain information about the change that satisfied the wait operation, and resets the notification object so it can be signaled when the next change occurs.</span></span>

<span data-ttu-id="d5219-188">À une exception près, n’appelez pas la fonction **FindNextPrinterChangeNotification** si l’objet de notification de modification n’est pas dans l’état signalé.</span><span class="sxs-lookup"><span data-stu-id="d5219-188">With one exception, do not call the **FindNextPrinterChangeNotification** function if the change notification object is not in the signaled state.</span></span> <span data-ttu-id="d5219-189">Si une fonction Wait retourne le **\_ délai d'** attente de la valeur, l’objet de modification n’est pas dans l’état signalé.</span><span class="sxs-lookup"><span data-stu-id="d5219-189">If a wait function returns the value **WAIT\_TIMEOUT**, the change object is not in the signaled state.</span></span> <span data-ttu-id="d5219-190">Appelez la fonction **FindNextPrinterChangeNotification** uniquement si la fonction Wait est réussie sans dépassement du délai d’attente. L’exception est quand **FindNextPrinterChangeNotification** est appelé avec le bit d’actualisation des options de notification d’imprimante défini dans le paramètre *pPrinterNotifyOptions* . **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d5219-190">Call the **FindNextPrinterChangeNotification** function only if the wait function succeeds without timing out. The exception is when **FindNextPrinterChangeNotification** is called with the **PRINTER\_NOTIFY\_OPTIONS\_REFRESH** bit set in the *pPrinterNotifyOptions* parameter.</span></span> <span data-ttu-id="d5219-191">Notez que même lorsque cet indicateur est défini, il est toujours possible de définir l’indicateur d’informations de notification d’imprimante dans le paramètre *ppPrinterNotifyInfo* . **\_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="d5219-191">Note that even when this flag is set, it is still possible for the **PRINTER\_NOTIFY\_INFO\_DISCARDED** flag to be set in the *ppPrinterNotifyInfo* parameter.</span></span>

<span data-ttu-id="d5219-192">Pour continuer à surveiller les modifications apportées à l’imprimante ou au serveur d’impression, répétez le cycle de l’appel de l’une des [fonctions d’attente](/windows/desktop/Sync/wait-functions) , puis appelez la fonction **FindNextPrinterChangeNotification** pour examiner la modification et réinitialiser l’objet de notification.</span><span class="sxs-lookup"><span data-stu-id="d5219-192">To continue monitoring the printer or print server for changes, repeat the cycle of calling one of the [wait functions](/windows/desktop/Sync/wait-functions) , and then calling the **FindNextPrinterChangeNotification** function to examine the change and reset the notification object.</span></span>

<span data-ttu-id="d5219-193">**FindNextPrinterChangeNotification** peut combiner plusieurs modifications apportées au même champ d’informations d’imprimante en une seule notification.</span><span class="sxs-lookup"><span data-stu-id="d5219-193">**FindNextPrinterChangeNotification** may combine multiple changes to the same printer information field into a single notification.</span></span> <span data-ttu-id="d5219-194">Dans ce cas, la fonction réduit généralement toutes les modifications apportées au champ en une seule entrée dans le tableau des structures de [**données d’informations de notification d’imprimante \_ \_ \_**](printer-notify-info-data.md) dans *ppPrinterNotifyInfo*; l’entrée unique signale uniquement les informations les plus récentes.</span><span class="sxs-lookup"><span data-stu-id="d5219-194">When this occurs, the function typically collapses all changes for the field into a single entry in the array of [**PRINTER\_NOTIFY\_INFO\_DATA**](printer-notify-info-data.md) structures in *ppPrinterNotifyInfo*; the single entry reports only the most current information.</span></span> <span data-ttu-id="d5219-195">Toutefois, pour certains champs d’informations sur les travaux et les imprimantes, la fonction peut retourner plusieurs entrées de tableau pour le même champ.</span><span class="sxs-lookup"><span data-stu-id="d5219-195">However, for some job and printer information fields, the function can return multiple array entries for the same field.</span></span> <span data-ttu-id="d5219-196">Dans ce cas, la dernière entrée de tableau pour le champ signale les données actuelles, et les entrées précédentes contiennent les données pour les étapes intermédiaires.</span><span class="sxs-lookup"><span data-stu-id="d5219-196">In this case, the last array entry for the field reports the current data, and the earlier entries contain the data for the intermediate stages.</span></span>

<span data-ttu-id="d5219-197">Lorsque vous n’avez plus besoin de l’objet de notification de modification, fermez-le en appelant la fonction [**FindClosePrinterChangeNotification**](findcloseprinterchangenotification.md) .</span><span class="sxs-lookup"><span data-stu-id="d5219-197">When you no longer need the change notification object, close it by calling the [**FindClosePrinterChangeNotification**](findcloseprinterchangenotification.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="d5219-198">Dans Windows XP avec Service Pack 2 (SP2) et versions ultérieures, le pare-feu de connexion Internet (ICF) bloque les ports d’imprimante par défaut, mais une exception pour le partage de fichiers et d’imprimantes peut être activée.</span><span class="sxs-lookup"><span data-stu-id="d5219-198">In Windows XP with Service Pack 2 (SP2) and later, the Internet Connection Firewall (ICF) blocks printer ports by default, but an exception for File and Print Sharing can be enabled.</span></span> <span data-ttu-id="d5219-199">Si un utilisateur établit une connexion d’imprimante avec un autre ordinateur et que l’exception n’est pas activée, l’utilisateur ne reçoit pas de notifications de modification d’imprimante à partir du serveur.</span><span class="sxs-lookup"><span data-stu-id="d5219-199">If a user makes a printer connection to another machine, and the exception is not enabled, then the user will not receive printer change notifications from the server.</span></span> <span data-ttu-id="d5219-200">Un administrateur d’ordinateur devra activer l’exception.</span><span class="sxs-lookup"><span data-stu-id="d5219-200">A machine admin will have to enable exception.</span></span>

 

## <a name="examples"></a><span data-ttu-id="d5219-201">Exemples</span><span class="sxs-lookup"><span data-stu-id="d5219-201">Examples</span></span>

<span data-ttu-id="d5219-202">L’exemple de code suivant illustre la façon dont vous pouvez surveiller l’état de l’imprimante à l’aide de ces fonctions.</span><span class="sxs-lookup"><span data-stu-id="d5219-202">The following code sample illustrates how you might monitor printer status by using these functions.</span></span>


```C++
// Get change notification handle for the printer   
chgObject = FindFirstPrinterChangeNotification( 
                hPrinter, 
                PRINTER_CHANGE_JOB, 
                0, 
                NULL); 

if (chgObject != INVALID_HANDLE_VALUE) {
    while (bKeepMonitoring) {
        // Wait for the change notification 
        WaitForSingleObject(chgObject, INFINITE);

        fcnreturn = FindNextPrinterChangeNotification(
                        chgObject, 
                        pdwChange, 
                        NULL, 
                        NULL);

        if (fcnreturn) {
            // Check value of *pdwChange and 
            //  deal with the indicated change 
        }
        // Insert some mechanism to stop monitoring
        //  such as: 
        //
        // if (something happens) {
        //     bKeepMonitoring = false; 
        // }
        //
    }
    // Close Printer Change Notification handle when finished. 
    FindClosePrinterChangeNotification(chgObject);
} else {
    // Unable to open printer change notification handle 
    dwStatus = GetLastError();
}
```



## <a name="requirements"></a><span data-ttu-id="d5219-203">Configuration requise</span><span class="sxs-lookup"><span data-stu-id="d5219-203">Requirements</span></span>



| <span data-ttu-id="d5219-204">Condition requise</span><span class="sxs-lookup"><span data-stu-id="d5219-204">Requirement</span></span> | <span data-ttu-id="d5219-205">Valeur</span><span class="sxs-lookup"><span data-stu-id="d5219-205">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5219-206">Client minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d5219-206">Minimum supported client</span></span><br/> | <span data-ttu-id="d5219-207">Windows 2000 Professionnel - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d5219-207">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d5219-208">Serveur minimal pris en charge</span><span class="sxs-lookup"><span data-stu-id="d5219-208">Minimum supported server</span></span><br/> | <span data-ttu-id="d5219-209">Windows 2000 Server - \[Applications de bureau uniquement\]</span><span class="sxs-lookup"><span data-stu-id="d5219-209">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d5219-210">En-tête</span><span class="sxs-lookup"><span data-stu-id="d5219-210">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5219-211"><dt>Winspool. h (inclure Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d5219-211"><dt>Winspool.h (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="d5219-212">Bibliothèque</span><span class="sxs-lookup"><span data-stu-id="d5219-212">Library</span></span><br/>                  | <dl> <span data-ttu-id="d5219-213"><dt>Winspool. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d5219-213"><dt>Winspool.lib</dt></span></span> </dl>                   |
| <span data-ttu-id="d5219-214">DLL</span><span class="sxs-lookup"><span data-stu-id="d5219-214">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5219-215"><dt>Spoolss.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5219-215"><dt>Spoolss.dll</dt></span></span> </dl>                    |



## <a name="see-also"></a><span data-ttu-id="d5219-216">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="d5219-216">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5219-217">Impression</span><span class="sxs-lookup"><span data-stu-id="d5219-217">Printing</span></span>](printdocs-printing.md)
</dt> <dt>

[<span data-ttu-id="d5219-218">Fonctions API du spouleur d’impression</span><span class="sxs-lookup"><span data-stu-id="d5219-218">Print Spooler API Functions</span></span>](printing-and-print-spooler-functions.md)
</dt> <dt>

[<span data-ttu-id="d5219-219">**FindClosePrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="d5219-219">**FindClosePrinterChangeNotification**</span></span>](findcloseprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="d5219-220">**FindFirstPrinterChangeNotification**</span><span class="sxs-lookup"><span data-stu-id="d5219-220">**FindFirstPrinterChangeNotification**</span></span>](findfirstprinterchangenotification.md)
</dt> <dt>

[<span data-ttu-id="d5219-221">**\_informations de notification de l’imprimante \_**</span><span class="sxs-lookup"><span data-stu-id="d5219-221">**PRINTER\_NOTIFY\_INFO**</span></span>](printer-notify-info.md)
</dt> <dt>

[<span data-ttu-id="d5219-222">**\_données d' \_ informations de notification d’imprimante \_**</span><span class="sxs-lookup"><span data-stu-id="d5219-222">**PRINTER\_NOTIFY\_INFO\_DATA**</span></span>](printer-notify-info-data.md)
</dt> <dt>

[<span data-ttu-id="d5219-223">**\_options de notification d’imprimante \_**</span><span class="sxs-lookup"><span data-stu-id="d5219-223">**PRINTER\_NOTIFY\_OPTIONS**</span></span>](printer-notify-options.md)
</dt> </dl>

 

