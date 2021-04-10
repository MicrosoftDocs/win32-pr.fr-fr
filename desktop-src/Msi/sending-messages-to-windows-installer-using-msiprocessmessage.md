---
description: Les messages envoyés à l’aide de MsiProcessMessage sont les mêmes que ceux reçus par la \_ fonction de rappel du gestionnaire INSTALLUI si MsiSetExternalUI a été appelé.
ms.assetid: ca73bd0a-6f4e-453c-9e38-14cfd602d42c
title: Envoyer des messages à Windows Installer à l’aide de MsiProcessMessage
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bcd8c8a704c1f4dd24763f7f47ff0d8898a95c0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103953073"
---
# <a name="sending-messages-to-windows-installer-using-msiprocessmessage"></a><span data-ttu-id="a3c22-103">Envoi de messages à Windows Installer à l’aide de MsiProcessMessage</span><span class="sxs-lookup"><span data-stu-id="a3c22-103">Sending Messages to Windows Installer Using MsiProcessMessage</span></span>

<span data-ttu-id="a3c22-104">Les messages envoyés à l’aide de [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) sont les mêmes que ceux reçus par la fonction de rappel du [**\_ Gestionnaire INSTALLUI**](/windows/desktop/api/Msi/nc-msi-installui_handlera) si [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) a été appelé.</span><span class="sxs-lookup"><span data-stu-id="a3c22-104">The messages sent using [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) are the same messages that are received by the [**INSTALLUI\_HANDLER**](/windows/desktop/api/Msi/nc-msi-installui_handlera) callback function if [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) was called.</span></span> <span data-ttu-id="a3c22-105">Dans le cas contraire, Windows Installer gère les messages.</span><span class="sxs-lookup"><span data-stu-id="a3c22-105">Otherwise, Windows Installer handles the messages.</span></span> <span data-ttu-id="a3c22-106">Pour plus d’informations, consultez [analyse des messages de Windows Installer](parsing-windows-installer-messages.md).</span><span class="sxs-lookup"><span data-stu-id="a3c22-106">For details, see [Parsing Windows Installer Messages](parsing-windows-installer-messages.md).</span></span>

<span data-ttu-id="a3c22-107">Par exemple, pour envoyer un \_ message d’erreur INSTALLMESSAGE avec l' \_ icône Mo ICONWARNING et les \_ boutons MB ABORTRETRYCANCEL :</span><span class="sxs-lookup"><span data-stu-id="a3c22-107">For example, to send an INSTALLMESSAGE\_ERROR message with the MB\_ICONWARNING icon and the MB\_ABORTRETRYCANCEL buttons:</span></span>


```C++
PMSIHANDLE hInstall;
PMSIHANDLE hRec;
MsiProcessMessage(hInstall, INSTALLMESSAGE(INSTALLMESSAGE_ERROR|MB_ABORTRETRYIGNORE|MB_ICONWARNING), hRec);
```



<span data-ttu-id="a3c22-108">Où *hInstall* est le descripteur de l’installation, fourni à une action personnalisée ou au descripteur *hProduct* à partir de [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta) ou [**MsiOpenPackage**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea), et *hRec* est l’enregistrement contenant les informations d’erreur à mettre en forme.</span><span class="sxs-lookup"><span data-stu-id="a3c22-108">Where *hInstall* is the handle to the installation, provided to a custom action or the *hProduct* handle from [**MsiOpenProduct**](/windows/desktop/api/Msi/nf-msi-msiopenproducta) or [**MsiOpenPackage**](/windows/desktop/api/Msi/nf-msi-msiopenpackagea), and *hRec* is the record containing the error information to format.</span></span> <span data-ttu-id="a3c22-109">Pour plus d’informations sur la façon dont la mise en forme est effectuée, consultez [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda).</span><span class="sxs-lookup"><span data-stu-id="a3c22-109">For information on how formatting is performed, see [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda).</span></span>

<span data-ttu-id="a3c22-110">Par défaut, si une \_ erreur INSTALLMESSAGE ou un \_ message INSTALLMESSAGE FATALEXIT est envoyé sans spécifier le type de bouton ou les types d’icône, MB \_ OK, aucune icône et Mo \_ DEFBUTTON1 sont utilisés.</span><span class="sxs-lookup"><span data-stu-id="a3c22-110">By default, if an INSTALLMESSAGE\_ERROR or INSTALLMESSAGE\_FATALEXIT message is sent without specifying button type or icon types, MB\_OK, no icon, and MB\_DEFBUTTON1 are used.</span></span>

<span data-ttu-id="a3c22-111">Windows Installer n’étiquette pas le bouton **abandonner** avec la chaîne « Abort » lors de l’affichage d’une MessageBox avec la \_ spécification du bouton ABORTRETRYIGNORE Mo, il étiquette plutôt le bouton avec la chaîne « Cancel ».</span><span class="sxs-lookup"><span data-stu-id="a3c22-111">Windows Installer does not label the **ABORT** button with the "Abort" string when displaying a MessageBox with the MB\_ABORTRETRYIGNORE button specification, instead it labels the button with the "Cancel" string.</span></span> <span data-ttu-id="a3c22-112">Tous les messages d’erreur s’abstiennent d’utiliser le mot « Abort » et utilisent plutôt le mot « Cancel ».</span><span class="sxs-lookup"><span data-stu-id="a3c22-112">All error messages refrain from using the word "Abort" and instead use the word "Cancel".</span></span>

<span data-ttu-id="a3c22-113">Le paramètre *hRecord* de la fonction [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) dépend du type de message envoyé au [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage).</span><span class="sxs-lookup"><span data-stu-id="a3c22-113">The *hRecord* parameter of the [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) function depends upon the message type sent to the [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage).</span></span> <span data-ttu-id="a3c22-114">La liste suivante détaille les spécifications de l’enregistrement par rapport au type de message :</span><span class="sxs-lookup"><span data-stu-id="a3c22-114">The following list details the requirements of the record in relation to the message type:</span></span>

<span data-ttu-id="a3c22-115">INSTALLMESSAGE \_ FATALEXIT</span><span class="sxs-lookup"><span data-stu-id="a3c22-115">INSTALLMESSAGE\_FATALEXIT</span></span>

 

<span data-ttu-id="a3c22-116">\_informations INSTALLMESSAGE</span><span class="sxs-lookup"><span data-stu-id="a3c22-116">INSTALLMESSAGE\_INFO</span></span>

 

<span data-ttu-id="a3c22-117">INSTALLMESSAGE \_ OUTOFDISKSPACE</span><span class="sxs-lookup"><span data-stu-id="a3c22-117">INSTALLMESSAGE\_OUTOFDISKSPACE</span></span>



| <span data-ttu-id="a3c22-118">Champ</span><span class="sxs-lookup"><span data-stu-id="a3c22-118">Field</span></span>         | <span data-ttu-id="a3c22-119">Description</span><span class="sxs-lookup"><span data-stu-id="a3c22-119">Description</span></span>                                                                                                                                                                                                        |
|---------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3c22-120">0</span><span class="sxs-lookup"><span data-stu-id="a3c22-120">0</span></span>             | <span data-ttu-id="a3c22-121">Modèle pour la mise en forme de la chaîne résultante.</span><span class="sxs-lookup"><span data-stu-id="a3c22-121">Template for the formatting of the resultant string.</span></span> <span data-ttu-id="a3c22-122">Pour plus d’informations, consultez [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) .</span><span class="sxs-lookup"><span data-stu-id="a3c22-122">See [**MsiFormatRecord**](/windows/desktop/api/Msiquery/nf-msiquery-msiformatrecorda) for more information.</span></span> <span data-ttu-id="a3c22-123">Les champs de l’enregistrement sont référencés à l’aide \[ \] de 1 pour le champ 1, \[ 2 pour le \] champ 2, etc.</span><span class="sxs-lookup"><span data-stu-id="a3c22-123">The fields of the record are referenced using \[1\] for field 1, \[2\] for field 2, etc.</span></span> |
| <span data-ttu-id="a3c22-124">1 à *n*</span><span class="sxs-lookup"><span data-stu-id="a3c22-124">1 through *n*</span></span> | <span data-ttu-id="a3c22-125">Tous les champs suivants sont directement liés aux champs référencés par le modèle dans le champ 0.</span><span class="sxs-lookup"><span data-stu-id="a3c22-125">All subsequent fields are directly related to the fields referenced by the template in field 0.</span></span>                                                                                                                    |



 

<span data-ttu-id="a3c22-126">Si le champ 0 a la valeur null, la chaîne reçue par le gestionnaire d’interface utilisateur est mise en forme comme suit : 1 : \[ données du champ 1 \] 2 : les \[ données du champ 2 \] signifient que, pour chaque champ de l’enregistrement, la chaîne contient le numéro de champ suivi des données stockées dans le champ.</span><span class="sxs-lookup"><span data-stu-id="a3c22-126">If field 0 is null, the string received by the UI handler is formatted as: 1: \[data from field 1\] 2: \[data from field 2\] meaning that for each field of the record, the string contains the field number followed by the data stored in the field.</span></span>

<span data-ttu-id="a3c22-127">Les messages d’information de [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) sont journalisés lorsque [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga), l' [option de ligne de commande](command-line-options.md)« /l » ou la [stratégie de journalisation](logging.md) spécifient « I » ou INSTALLLOGMODE \_ info.</span><span class="sxs-lookup"><span data-stu-id="a3c22-127">Information messages from [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) are logged when [**MsiEnableLog**](/windows/desktop/api/Msi/nf-msi-msienableloga), the '/l' [command line option](command-line-options.md), or the [logging policy](logging.md) specify 'I' or INSTALLLOGMODE\_INFO.</span></span>

<span data-ttu-id="a3c22-128">\_erreur INSTALLMESSAGE</span><span class="sxs-lookup"><span data-stu-id="a3c22-128">INSTALLMESSAGE\_ERROR</span></span>

 

<span data-ttu-id="a3c22-129">\_Avertissement INSTALLMESSAGE</span><span class="sxs-lookup"><span data-stu-id="a3c22-129">INSTALLMESSAGE\_WARNING</span></span>

 

<span data-ttu-id="a3c22-130">\_utilisateur INSTALLMESSAGE</span><span class="sxs-lookup"><span data-stu-id="a3c22-130">INSTALLMESSAGE\_USER</span></span>

<span data-ttu-id="a3c22-131">Pour utiliser un message de la table d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="a3c22-131">To use a message from the Error table.</span></span>



| <span data-ttu-id="a3c22-132">Champ</span><span class="sxs-lookup"><span data-stu-id="a3c22-132">Field</span></span>         | <span data-ttu-id="a3c22-133">Description</span><span class="sxs-lookup"><span data-stu-id="a3c22-133">Description</span></span>                                           |
|---------------|-------------------------------------------------------|
| <span data-ttu-id="a3c22-134">0</span><span class="sxs-lookup"><span data-stu-id="a3c22-134">0</span></span>             | <span data-ttu-id="a3c22-135">Doit avoir la valeur null.</span><span class="sxs-lookup"><span data-stu-id="a3c22-135">Must be null.</span></span>                                         |
| <span data-ttu-id="a3c22-136">1</span><span class="sxs-lookup"><span data-stu-id="a3c22-136">1</span></span>             | <span data-ttu-id="a3c22-137">Numéro de message dans la [table d’erreurs](error-table.md).</span><span class="sxs-lookup"><span data-stu-id="a3c22-137">Message number in the [Error table](error-table.md).</span></span> |
| <span data-ttu-id="a3c22-138">2 à *n*</span><span class="sxs-lookup"><span data-stu-id="a3c22-138">2 through *n*</span></span> | <span data-ttu-id="a3c22-139">Lié au message spécifié dans la table d’erreurs.</span><span class="sxs-lookup"><span data-stu-id="a3c22-139">Related to the specified message in the Error table.</span></span>  |



 

<span data-ttu-id="a3c22-140">Par exemple,</span><span class="sxs-lookup"><span data-stu-id="a3c22-140">For example.</span></span>



| <span data-ttu-id="a3c22-141">Champ</span><span class="sxs-lookup"><span data-stu-id="a3c22-141">Field</span></span> | <span data-ttu-id="a3c22-142">Type</span><span class="sxs-lookup"><span data-stu-id="a3c22-142">Type</span></span>   | <span data-ttu-id="a3c22-143">Données</span><span class="sxs-lookup"><span data-stu-id="a3c22-143">Data</span></span>       |
|-------|--------|------------|
| <span data-ttu-id="a3c22-144">0</span><span class="sxs-lookup"><span data-stu-id="a3c22-144">0</span></span>     | <span data-ttu-id="a3c22-145">string</span><span class="sxs-lookup"><span data-stu-id="a3c22-145">string</span></span> | <span data-ttu-id="a3c22-146">null</span><span class="sxs-lookup"><span data-stu-id="a3c22-146">null</span></span>       |
| <span data-ttu-id="a3c22-147">1</span><span class="sxs-lookup"><span data-stu-id="a3c22-147">1</span></span>     | <span data-ttu-id="a3c22-148">int</span><span class="sxs-lookup"><span data-stu-id="a3c22-148">int</span></span>    | <span data-ttu-id="a3c22-149">1304</span><span class="sxs-lookup"><span data-stu-id="a3c22-149">1304</span></span>       |
| <span data-ttu-id="a3c22-150">2</span><span class="sxs-lookup"><span data-stu-id="a3c22-150">2</span></span>     | <span data-ttu-id="a3c22-151">string</span><span class="sxs-lookup"><span data-stu-id="a3c22-151">string</span></span> | <span data-ttu-id="a3c22-152">Myfile.txt</span><span class="sxs-lookup"><span data-stu-id="a3c22-152">Myfile.txt</span></span> |



 

<span data-ttu-id="a3c22-153">Le message obtenu à partir du gestionnaire d’interface utilisateur est le suivant :</span><span class="sxs-lookup"><span data-stu-id="a3c22-153">The resulting message received from the UI handler is:</span></span>

<span data-ttu-id="a3c22-154">Erreur 1304.</span><span class="sxs-lookup"><span data-stu-id="a3c22-154">Error 1304.</span></span> <span data-ttu-id="a3c22-155">Erreur lors de l’écriture dans le fichier : Myfile.txt.</span><span class="sxs-lookup"><span data-stu-id="a3c22-155">Error writing to file: Myfile.txt.</span></span> <span data-ttu-id="a3c22-156">Vérifiez que vous avez accès à ce répertoire.</span><span class="sxs-lookup"><span data-stu-id="a3c22-156">Verify that you have access to that directory.</span></span>

<span data-ttu-id="a3c22-157">Si le champ 0 n’est pas null, le message de la table d’erreurs est substitué.</span><span class="sxs-lookup"><span data-stu-id="a3c22-157">If field 0 is not null, the message from the error table is overridden.</span></span> <span data-ttu-id="a3c22-158">Au lieu de cela, le modèle de champ 0 détermine le format du message.</span><span class="sxs-lookup"><span data-stu-id="a3c22-158">Instead, the field 0 template determines the format of the message.</span></span>

<span data-ttu-id="a3c22-159">Le message peut également spécifier les boutons, y compris le bouton par défaut, et l’icône à utiliser avec le message comme indiqué ci-dessus.</span><span class="sxs-lookup"><span data-stu-id="a3c22-159">The message may also specify the buttons, including the default button, and the icon for use with the message as mentioned above.</span></span> <span data-ttu-id="a3c22-160">Les types de bouton et d’icône sont répertoriés dans le [**\_ Gestionnaire INSTALLUI**](/windows/desktop/api/Msi/nc-msi-installui_handlera).</span><span class="sxs-lookup"><span data-stu-id="a3c22-160">The button and icon types are listed in [**INSTALLUI\_HANDLER**](/windows/desktop/api/Msi/nc-msi-installui_handlera).</span></span>

<span data-ttu-id="a3c22-161">INSTALLMESSAGE \_ COMMONDATA</span><span class="sxs-lookup"><span data-stu-id="a3c22-161">INSTALLMESSAGE\_COMMONDATA</span></span>

<span data-ttu-id="a3c22-162">Ce message est envoyé pour activer ou désactiver le bouton **Annuler** dans une boîte de dialogue de progression.</span><span class="sxs-lookup"><span data-stu-id="a3c22-162">This message is sent to enable or disable the **Cancel** button in a progress dialog box.</span></span>



| <span data-ttu-id="a3c22-163">Champ</span><span class="sxs-lookup"><span data-stu-id="a3c22-163">Field</span></span> | <span data-ttu-id="a3c22-164">Description</span><span class="sxs-lookup"><span data-stu-id="a3c22-164">Description</span></span>                                                                                                                                  |
|-------|----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3c22-165">0</span><span class="sxs-lookup"><span data-stu-id="a3c22-165">0</span></span>     | <span data-ttu-id="a3c22-166">Inutilisé.</span><span class="sxs-lookup"><span data-stu-id="a3c22-166">Unused.</span></span>                                                                                                                                      |
| <span data-ttu-id="a3c22-167">1</span><span class="sxs-lookup"><span data-stu-id="a3c22-167">1</span></span>     | <span data-ttu-id="a3c22-168">2 fait référence au bouton **Annuler** .</span><span class="sxs-lookup"><span data-stu-id="a3c22-168">2 refers to the **Cancel** button.</span></span>                                                                                                           |
| <span data-ttu-id="a3c22-169">2</span><span class="sxs-lookup"><span data-stu-id="a3c22-169">2</span></span>     | <span data-ttu-id="a3c22-170">La valeur 1 indique que le bouton **Annuler** doit être visible.</span><span class="sxs-lookup"><span data-stu-id="a3c22-170">A value of 1 indicates the **Cancel** button should be visible.</span></span> <span data-ttu-id="a3c22-171">La valeur 0 indique que le bouton **Annuler** doit être invisible.</span><span class="sxs-lookup"><span data-stu-id="a3c22-171">A value of 0 indicates the **Cancel** button should be invisible.</span></span><br/> |



 

<span data-ttu-id="a3c22-172">Par exemple, pour désactiver ou masquer le bouton **Annuler** , l’enregistrement s’affiche comme suit.</span><span class="sxs-lookup"><span data-stu-id="a3c22-172">For example, to disable or hide the **Cancel** button, the record would appear as follows.</span></span>



| <span data-ttu-id="a3c22-173">Champ</span><span class="sxs-lookup"><span data-stu-id="a3c22-173">Field</span></span> | <span data-ttu-id="a3c22-174">Type</span><span class="sxs-lookup"><span data-stu-id="a3c22-174">Type</span></span>   | <span data-ttu-id="a3c22-175">Données</span><span class="sxs-lookup"><span data-stu-id="a3c22-175">Data</span></span> |
|-------|--------|------|
| <span data-ttu-id="a3c22-176">0</span><span class="sxs-lookup"><span data-stu-id="a3c22-176">0</span></span>     | <span data-ttu-id="a3c22-177">string</span><span class="sxs-lookup"><span data-stu-id="a3c22-177">string</span></span> | <span data-ttu-id="a3c22-178">null</span><span class="sxs-lookup"><span data-stu-id="a3c22-178">null</span></span> |
| <span data-ttu-id="a3c22-179">1</span><span class="sxs-lookup"><span data-stu-id="a3c22-179">1</span></span>     | <span data-ttu-id="a3c22-180">int</span><span class="sxs-lookup"><span data-stu-id="a3c22-180">int</span></span>    | <span data-ttu-id="a3c22-181">2</span><span class="sxs-lookup"><span data-stu-id="a3c22-181">2</span></span>    |
| <span data-ttu-id="a3c22-182">2</span><span class="sxs-lookup"><span data-stu-id="a3c22-182">2</span></span>     | <span data-ttu-id="a3c22-183">int</span><span class="sxs-lookup"><span data-stu-id="a3c22-183">int</span></span>    | <span data-ttu-id="a3c22-184">0</span><span class="sxs-lookup"><span data-stu-id="a3c22-184">0</span></span>    |



 

<span data-ttu-id="a3c22-185">INSTALLMESSAGE \_ ACTIONSTART</span><span class="sxs-lookup"><span data-stu-id="a3c22-185">INSTALLMESSAGE\_ACTIONSTART</span></span>

 

<span data-ttu-id="a3c22-186">INSTALLMESSAGE \_ ACTIONDATA</span><span class="sxs-lookup"><span data-stu-id="a3c22-186">INSTALLMESSAGE\_ACTIONDATA</span></span>

<span data-ttu-id="a3c22-187">L' \_ enregistrement INSTALLMESSAGE ACTIONSTART détermine le format de l’enregistrement ActionData.</span><span class="sxs-lookup"><span data-stu-id="a3c22-187">The INSTALLMESSAGE\_ACTIONSTART record determines the format of the ActionData record.</span></span>



| <span data-ttu-id="a3c22-188">Champ</span><span class="sxs-lookup"><span data-stu-id="a3c22-188">Field</span></span> | <span data-ttu-id="a3c22-189">Description</span><span class="sxs-lookup"><span data-stu-id="a3c22-189">Description</span></span>                                                                                                   |
|-------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3c22-190">0</span><span class="sxs-lookup"><span data-stu-id="a3c22-190">0</span></span>     | <span data-ttu-id="a3c22-191">null</span><span class="sxs-lookup"><span data-stu-id="a3c22-191">null</span></span>                                                                                                          |
| <span data-ttu-id="a3c22-192">1</span><span class="sxs-lookup"><span data-stu-id="a3c22-192">1</span></span>     | <span data-ttu-id="a3c22-193">Nom de l’action.</span><span class="sxs-lookup"><span data-stu-id="a3c22-193">Action name.</span></span> <span data-ttu-id="a3c22-194">Le nom de ce champ doit être non null.</span><span class="sxs-lookup"><span data-stu-id="a3c22-194">The name in this field must be non-null.</span></span>                                                         |
| <span data-ttu-id="a3c22-195">2</span><span class="sxs-lookup"><span data-stu-id="a3c22-195">2</span></span>     | <span data-ttu-id="a3c22-196">Description de l’action.</span><span class="sxs-lookup"><span data-stu-id="a3c22-196">Action description.</span></span>                                                                                           |
| <span data-ttu-id="a3c22-197">3</span><span class="sxs-lookup"><span data-stu-id="a3c22-197">3</span></span>     | <span data-ttu-id="a3c22-198">Modèle d’action.</span><span class="sxs-lookup"><span data-stu-id="a3c22-198">Action template.</span></span> <span data-ttu-id="a3c22-199">Cette valeur est utilisée pour le ActionData dont le message est mis en forme en fonction de ce modèle.</span><span class="sxs-lookup"><span data-stu-id="a3c22-199">This is used for the ActionData whose message is being formatted according to this template.</span></span> |



 

<span data-ttu-id="a3c22-200">Ne faites pas référence au champ 0 dans le message de modèle d’action.</span><span class="sxs-lookup"><span data-stu-id="a3c22-200">Do not reference field 0 in the Action template message.</span></span>

<span data-ttu-id="a3c22-201">L' \_ enregistrement INSTALLMESSAGE ACTIONDATA est mis en forme comme suit.</span><span class="sxs-lookup"><span data-stu-id="a3c22-201">The INSTALLMESSAGE\_ACTIONDATA record is formatted as follows.</span></span>



| <span data-ttu-id="a3c22-202">Champ</span><span class="sxs-lookup"><span data-stu-id="a3c22-202">Field</span></span>         | <span data-ttu-id="a3c22-203">Description</span><span class="sxs-lookup"><span data-stu-id="a3c22-203">Description</span></span>                                                                                                                                        |
|---------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3c22-204">0</span><span class="sxs-lookup"><span data-stu-id="a3c22-204">0</span></span>             | <span data-ttu-id="a3c22-205">null</span><span class="sxs-lookup"><span data-stu-id="a3c22-205">null</span></span>                                                                                                                                               |
| <span data-ttu-id="a3c22-206">1 à *n*</span><span class="sxs-lookup"><span data-stu-id="a3c22-206">1 through *n*</span></span> | <span data-ttu-id="a3c22-207">Dépend du champ 3 du \_ message ou du modèle INSTALLMESSAGE ACTIONSTART correspondant spécifié dans la [table ActionText](actiontext-table.md).</span><span class="sxs-lookup"><span data-stu-id="a3c22-207">Dependent upon field 3 of the corresponding INSTALLMESSAGE\_ACTIONSTART message or template specified in [ActionText table](actiontext-table.md).</span></span> |



 

<span data-ttu-id="a3c22-208">Par exemple, l' \_ enregistrement INSTALLMESSAGE ACTIONSTART.</span><span class="sxs-lookup"><span data-stu-id="a3c22-208">For example, the INSTALLMESSAGE\_ACTIONSTART record.</span></span>



| <span data-ttu-id="a3c22-209">Champ</span><span class="sxs-lookup"><span data-stu-id="a3c22-209">Field</span></span> | <span data-ttu-id="a3c22-210">Type</span><span class="sxs-lookup"><span data-stu-id="a3c22-210">Type</span></span>   | <span data-ttu-id="a3c22-211">Données</span><span class="sxs-lookup"><span data-stu-id="a3c22-211">Data</span></span>                                                            |
|-------|--------|-----------------------------------------------------------------|
| <span data-ttu-id="a3c22-212">0</span><span class="sxs-lookup"><span data-stu-id="a3c22-212">0</span></span>     | <span data-ttu-id="a3c22-213">string</span><span class="sxs-lookup"><span data-stu-id="a3c22-213">string</span></span> | <span data-ttu-id="a3c22-214">null</span><span class="sxs-lookup"><span data-stu-id="a3c22-214">null</span></span>                                                            |
| <span data-ttu-id="a3c22-215">1</span><span class="sxs-lookup"><span data-stu-id="a3c22-215">1</span></span>     | <span data-ttu-id="a3c22-216">string</span><span class="sxs-lookup"><span data-stu-id="a3c22-216">string</span></span> | <span data-ttu-id="a3c22-217">MyAction</span><span class="sxs-lookup"><span data-stu-id="a3c22-217">MyAction</span></span>                                                        |
| <span data-ttu-id="a3c22-218">2</span><span class="sxs-lookup"><span data-stu-id="a3c22-218">2</span></span>     | <span data-ttu-id="a3c22-219">string</span><span class="sxs-lookup"><span data-stu-id="a3c22-219">string</span></span> | <span data-ttu-id="a3c22-220">Il s’agit de la description de « MyAction »</span><span class="sxs-lookup"><span data-stu-id="a3c22-220">This is the description of "MyAction"</span></span>                           |
| <span data-ttu-id="a3c22-221">3</span><span class="sxs-lookup"><span data-stu-id="a3c22-221">3</span></span>     | <span data-ttu-id="a3c22-222">string</span><span class="sxs-lookup"><span data-stu-id="a3c22-222">string</span></span> | <span data-ttu-id="a3c22-223">Modèle MyAction : les données champ1 sont \[ 1 \] .</span><span class="sxs-lookup"><span data-stu-id="a3c22-223">MyAction template: field1 data is \[1\].</span></span> <span data-ttu-id="a3c22-224">les données du champ 2 sont \[ 2 \] .</span><span class="sxs-lookup"><span data-stu-id="a3c22-224">field 2 data is \[2\].</span></span> |



 

<span data-ttu-id="a3c22-225">Le modèle pour INSTALLMESSAGE \_ ACTIONSTART (Field 3) fait référence aux champs 1 et 2, l' \_ enregistrement INSTALLMESSAGE ACTIONDATA doit avoir 2 champs contenant les données justifiées.</span><span class="sxs-lookup"><span data-stu-id="a3c22-225">The template for INSTALLMESSAGE\_ACTIONSTART (field 3) references fields 1 and 2, the INSTALLMESSAGE\_ACTIONDATA record should have 2 fields containing the warranted data.</span></span> <span data-ttu-id="a3c22-226">Les champs peuvent être des champs de type chaîne ou entier.</span><span class="sxs-lookup"><span data-stu-id="a3c22-226">The fields could be either string or integer fields.</span></span>

<span data-ttu-id="a3c22-227">\_Enregistrement INSTALLMESSAGE ACTIONDATA.</span><span class="sxs-lookup"><span data-stu-id="a3c22-227">INSTALLMESSAGE\_ACTIONDATA record.</span></span>



| <span data-ttu-id="a3c22-228">Champ</span><span class="sxs-lookup"><span data-stu-id="a3c22-228">Field</span></span> | <span data-ttu-id="a3c22-229">Type</span><span class="sxs-lookup"><span data-stu-id="a3c22-229">Type</span></span>   | <span data-ttu-id="a3c22-230">Données</span><span class="sxs-lookup"><span data-stu-id="a3c22-230">Data</span></span>                    |
|-------|--------|-------------------------|
| <span data-ttu-id="a3c22-231">0</span><span class="sxs-lookup"><span data-stu-id="a3c22-231">0</span></span>     | <span data-ttu-id="a3c22-232">string</span><span class="sxs-lookup"><span data-stu-id="a3c22-232">string</span></span> | <span data-ttu-id="a3c22-233">null</span><span class="sxs-lookup"><span data-stu-id="a3c22-233">null</span></span>                    |
| <span data-ttu-id="a3c22-234">1</span><span class="sxs-lookup"><span data-stu-id="a3c22-234">1</span></span>     | <span data-ttu-id="a3c22-235">int</span><span class="sxs-lookup"><span data-stu-id="a3c22-235">int</span></span>    | <span data-ttu-id="a3c22-236">2</span><span class="sxs-lookup"><span data-stu-id="a3c22-236">2</span></span>                       |
| <span data-ttu-id="a3c22-237">2</span><span class="sxs-lookup"><span data-stu-id="a3c22-237">2</span></span>     | <span data-ttu-id="a3c22-238">string</span><span class="sxs-lookup"><span data-stu-id="a3c22-238">string</span></span> | <span data-ttu-id="a3c22-239">ActionData pour MyAction</span><span class="sxs-lookup"><span data-stu-id="a3c22-239">ActionData for MyAction</span></span> |



 

<span data-ttu-id="a3c22-240">INSTALLMESSAGE \_ FILESINUSE</span><span class="sxs-lookup"><span data-stu-id="a3c22-240">INSTALLMESSAGE\_FILESINUSE</span></span>

<span data-ttu-id="a3c22-241">L’enregistrement FILESINUSE est un enregistrement de longueur variable.</span><span class="sxs-lookup"><span data-stu-id="a3c22-241">The FILESINUSE record is a variable length record.</span></span>



| <span data-ttu-id="a3c22-242">Champ</span><span class="sxs-lookup"><span data-stu-id="a3c22-242">Field</span></span> | <span data-ttu-id="a3c22-243">Description</span><span class="sxs-lookup"><span data-stu-id="a3c22-243">Description</span></span>                                                                                                                                                                                                                                                                                                                                                     |
|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3c22-244">0</span><span class="sxs-lookup"><span data-stu-id="a3c22-244">0</span></span>     | <span data-ttu-id="a3c22-245">Ce champ peut avoir la valeur null.</span><span class="sxs-lookup"><span data-stu-id="a3c22-245">This field can be null.</span></span> <span data-ttu-id="a3c22-246">Pour une installation à l’aide d’une interface utilisateur de base, ce champ peut spécifier un texte statique à afficher dans le [contrôle ListBox](listbox-control.md) de la [boîte de dialogue FilesInUse](filesinuse-dialog.md).</span><span class="sxs-lookup"><span data-stu-id="a3c22-246">For an installation using a basic UI, this field may specify static text for display in the [ListBox control](listbox-control.md) of the [FilesInUse dialog](filesinuse-dialog.md).</span></span> <span data-ttu-id="a3c22-247">Pour une installation à l’aide d’une interface utilisateur complète, ce champ n’a aucun effet, car le texte est spécifié par la création de la boîte de dialogue FilesInUse personnalisée.</span><span class="sxs-lookup"><span data-stu-id="a3c22-247">For an installation using a full UI, this field has no effect because the text is specified by the authoring of the custom FilesInUse dialog box.</span></span> |
| <span data-ttu-id="a3c22-248">1</span><span class="sxs-lookup"><span data-stu-id="a3c22-248">1</span></span>     | <span data-ttu-id="a3c22-249">Nom du fichier en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="a3c22-249">Name of the file in use.</span></span>                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="a3c22-250">2</span><span class="sxs-lookup"><span data-stu-id="a3c22-250">2</span></span>     | <span data-ttu-id="a3c22-251">Ce champ identifie le processus contenant le fichier en cours d’utilisation. **Windows Installer version 4,0 :** L’ID de processus (PID) du processus, ou le titre de la fenêtre pour le processus.</span><span class="sxs-lookup"><span data-stu-id="a3c22-251">This field identifies the process holding the file in use.**Windows Installer version 4.0:** The process id (PID) of the process, or the title of the window for the process.</span></span><br/> <span data-ttu-id="a3c22-252">**Windows Installer la version 3,1 et les versions antérieures :** Ce champ doit correspondre à l’ID de processus (PID) du processus.</span><span class="sxs-lookup"><span data-stu-id="a3c22-252">**Windows Installer version 3.1 and earlier:** This field must be the process id (PID) of the process.</span></span><br/>                                                      |



 

<span data-ttu-id="a3c22-253">Par exemple, pour envoyer un message FilesInUse indiquant que deux fichiers sont en cours d’utilisation, red.exe et blue.exe, l’enregistrement contient quatre champs plus le champ 0.</span><span class="sxs-lookup"><span data-stu-id="a3c22-253">For example, to send a FilesInUse message showing two files in use, red.exe and blue.exe, the record has four fields plus the 0 field.</span></span> <span data-ttu-id="a3c22-254">Le format de l’enregistrement est comme indiqué dans le tableau suivant.</span><span class="sxs-lookup"><span data-stu-id="a3c22-254">The format of the record would be as shown in the following table.</span></span> <span data-ttu-id="a3c22-255">Cet exemple requiert Windows Installer version 4,0.</span><span class="sxs-lookup"><span data-stu-id="a3c22-255">This example requires Windows Installer version 4.0.</span></span>

<span data-ttu-id="a3c22-256">**Windows Installer la version 3,1 et les versions antérieures :** Dans l’exemple suivant, les champs 2 et 4 doivent contenir les PID des processus contenant red.exe et blue.exe en cours d’utilisation.</span><span class="sxs-lookup"><span data-stu-id="a3c22-256">**Windows Installer version 3.1 and earlier:** Fields 2 and 4 in the following example must contain the PIDs of the processes holding red.exe and blue.exe in use.</span></span>



| <span data-ttu-id="a3c22-257">Champ</span><span class="sxs-lookup"><span data-stu-id="a3c22-257">Field</span></span> | <span data-ttu-id="a3c22-258">Description</span><span class="sxs-lookup"><span data-stu-id="a3c22-258">Description</span></span>       |
|-------|-------------------|
| <span data-ttu-id="a3c22-259">0</span><span class="sxs-lookup"><span data-stu-id="a3c22-259">0</span></span>     | <span data-ttu-id="a3c22-260">null</span><span class="sxs-lookup"><span data-stu-id="a3c22-260">null</span></span>              |
| <span data-ttu-id="a3c22-261">1</span><span class="sxs-lookup"><span data-stu-id="a3c22-261">1</span></span>     | <span data-ttu-id="a3c22-262">Red.exe</span><span class="sxs-lookup"><span data-stu-id="a3c22-262">Red.exe</span></span>           |
| <span data-ttu-id="a3c22-263">2</span><span class="sxs-lookup"><span data-stu-id="a3c22-263">2</span></span>     | <span data-ttu-id="a3c22-264">Titre de la fenêtre rouge</span><span class="sxs-lookup"><span data-stu-id="a3c22-264">Red Window Title</span></span>  |
| <span data-ttu-id="a3c22-265">3</span><span class="sxs-lookup"><span data-stu-id="a3c22-265">3</span></span>     | <span data-ttu-id="a3c22-266">Blue.exe</span><span class="sxs-lookup"><span data-stu-id="a3c22-266">Blue.exe</span></span>          |
| <span data-ttu-id="a3c22-267">4</span><span class="sxs-lookup"><span data-stu-id="a3c22-267">4</span></span>     | <span data-ttu-id="a3c22-268">Titre de fenêtre bleue</span><span class="sxs-lookup"><span data-stu-id="a3c22-268">Blue Window Title</span></span> |



 

> [!Note]  
> <span data-ttu-id="a3c22-269">Sur Windows Installer version 4,0, si le PID passé à partir du service n’a pas de titre de fenêtre, tel qu’une application de barre d’état système, le fichier ne s’affiche pas et le journal détaillé contient les messages suivants.</span><span class="sxs-lookup"><span data-stu-id="a3c22-269">On Windows Installer version 4.0, if the PID passed from the service does not have a window title, such as a system tray application, the file is not be displayed and the verbose log contains the following messages.</span></span>

 

``` syntax
File In Use: -<FileName>- Window could not be found. Process ID: <PID>
No window with title could be found for FilesInUse
```

<span data-ttu-id="a3c22-270">INSTALLMESSAGE \_ RESOLVESOURCE</span><span class="sxs-lookup"><span data-stu-id="a3c22-270">INSTALLMESSAGE\_RESOLVESOURCE</span></span>

<span data-ttu-id="a3c22-271">L' \_ enregistrement INSTALLMESSAGE RESOLVESOURCE contient sept champs.</span><span class="sxs-lookup"><span data-stu-id="a3c22-271">The INSTALLMESSAGE\_RESOLVESOURCE record has seven fields.</span></span> <span data-ttu-id="a3c22-272">Pour \_ que INSTALLMESSAGE RESOLVESOURCE fonctionne correctement, un gestionnaire d’interface utilisateur externe peut ne pas gérer le \_ message INSTALLMESSAGE RESOLVESOURCE.</span><span class="sxs-lookup"><span data-stu-id="a3c22-272">For INSTALLMESSAGE\_RESOLVESOURCE to work correctly, an external UI handler may not handle the INSTALLMESSAGE\_RESOLVESOURCE message.</span></span> <span data-ttu-id="a3c22-273">Windows Installer devez gérer le \_ message INSTALLMESSAGE RESOLVESOURCE.</span><span class="sxs-lookup"><span data-stu-id="a3c22-273">Windows Installer must handle the INSTALLMESSAGE\_RESOLVESOURCE message.</span></span> <span data-ttu-id="a3c22-274">Autrement dit, le gestionnaire d’interface utilisateur externe retourne 0 pour indiquer « aucune action effectuée » lors du filtrage du \_ message INSTALLMESSAGE RESOLVESOURCE.</span><span class="sxs-lookup"><span data-stu-id="a3c22-274">That is, the external UI handler returns 0 to indicate "no action taken" when filtering the INSTALLMESSAGE\_RESOLVESOURCE message.</span></span> <span data-ttu-id="a3c22-275">La meilleure pratique consiste à éviter d’envoyer un message RESOLVESOURCE.</span><span class="sxs-lookup"><span data-stu-id="a3c22-275">The best practice is to avoid sending a RESOLVESOURCE message.</span></span>



| <span data-ttu-id="a3c22-276">Champ</span><span class="sxs-lookup"><span data-stu-id="a3c22-276">Field</span></span> | <span data-ttu-id="a3c22-277">Description</span><span class="sxs-lookup"><span data-stu-id="a3c22-277">Description</span></span>                                                                                                                                                        |
|-------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a3c22-278">0</span><span class="sxs-lookup"><span data-stu-id="a3c22-278">0</span></span>     | <span data-ttu-id="a3c22-279">null</span><span class="sxs-lookup"><span data-stu-id="a3c22-279">null</span></span>                                                                                                                                                               |
| <span data-ttu-id="a3c22-280">1</span><span class="sxs-lookup"><span data-stu-id="a3c22-280">1</span></span>     | <span data-ttu-id="a3c22-281">null</span><span class="sxs-lookup"><span data-stu-id="a3c22-281">null</span></span>                                                                                                                                                               |
| <span data-ttu-id="a3c22-282">2</span><span class="sxs-lookup"><span data-stu-id="a3c22-282">2</span></span>     | <span data-ttu-id="a3c22-283">Nom du package.</span><span class="sxs-lookup"><span data-stu-id="a3c22-283">Package name.</span></span>                                                                                                                                                      |
| <span data-ttu-id="a3c22-284">3</span><span class="sxs-lookup"><span data-stu-id="a3c22-284">3</span></span>     | <span data-ttu-id="a3c22-285">Code du produit.</span><span class="sxs-lookup"><span data-stu-id="a3c22-285">Product code.</span></span>                                                                                                                                                      |
| <span data-ttu-id="a3c22-286">4</span><span class="sxs-lookup"><span data-stu-id="a3c22-286">4</span></span>     | <span data-ttu-id="a3c22-287">Chemin d’accès relatif, s’il est connu, peut avoir la valeur null.</span><span class="sxs-lookup"><span data-stu-id="a3c22-287">Relative path if known, can be null.</span></span>                                                                                                                               |
| <span data-ttu-id="a3c22-288">5</span><span class="sxs-lookup"><span data-stu-id="a3c22-288">5</span></span>     | <span data-ttu-id="a3c22-289">0</span><span class="sxs-lookup"><span data-stu-id="a3c22-289">0</span></span>                                                                                                                                                                  |
| <span data-ttu-id="a3c22-290">6</span><span class="sxs-lookup"><span data-stu-id="a3c22-290">6</span></span>     | <span data-ttu-id="a3c22-291">Indique s’il faut valider le code du package.</span><span class="sxs-lookup"><span data-stu-id="a3c22-291">Whether to validate the package code.</span></span> <span data-ttu-id="a3c22-292">La valeur « 1 » indique que le code du package doit être validé.</span><span class="sxs-lookup"><span data-stu-id="a3c22-292">A value of '1' indicates the package code should be validated.</span></span> <span data-ttu-id="a3c22-293">La valeur « 0 » indique que le package ne doit pas être validé.</span><span class="sxs-lookup"><span data-stu-id="a3c22-293">A value of '0' indicates the package should not be validated.</span></span> |
| <span data-ttu-id="a3c22-294">7</span><span class="sxs-lookup"><span data-stu-id="a3c22-294">7</span></span>     | <span data-ttu-id="a3c22-295">Disque requis à partir de la table de supports.</span><span class="sxs-lookup"><span data-stu-id="a3c22-295">Required disk from media table.</span></span> <span data-ttu-id="a3c22-296">La valeur « 0 » indique que tous les disques sont acceptables.</span><span class="sxs-lookup"><span data-stu-id="a3c22-296">A value of '0' indicates that any disk is acceptable.</span></span>                                                                              |



 

 

 




