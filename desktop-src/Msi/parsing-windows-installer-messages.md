---
description: Un gestionnaire d’interface utilisateur externe peut traiter la liste des messages du programme d’installation spécifiée par le paramètre dwMessagedFilter de la fonction MsiSetExternalUI.
ms.assetid: c4405803-9abd-40f4-9090-c075e7dcf293
title: Analyse des messages de Windows Installer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65cf96c85499b44accd0e01548ca184a030775d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104202198"
---
# <a name="parsing-windows-installer-messages"></a><span data-ttu-id="cb042-103">Analyse des messages de Windows Installer</span><span class="sxs-lookup"><span data-stu-id="cb042-103">Parsing Windows Installer Messages</span></span>

<span data-ttu-id="cb042-104">Un gestionnaire d’interface utilisateur externe peut traiter la liste des messages du programme d’installation spécifiée par le paramètre *dwMessagedFilter* de la fonction [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) .</span><span class="sxs-lookup"><span data-stu-id="cb042-104">An external UI handler can process the list of installer messages specified by the *dwMessagedFilter* parameter of the [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) function.</span></span> <span data-ttu-id="cb042-105">Certains de ces messages contiennent des chaînes qui peuvent être utilisées directement, et d’autres messages peuvent avoir besoin d’être analysés et traités par le gestionnaire d’interface utilisateur externe pour être utiles.</span><span class="sxs-lookup"><span data-stu-id="cb042-105">Some of these messages contain strings that can be used directly, and other messages may need to be parsed and processed by the external UI handler to be useful.</span></span> <span data-ttu-id="cb042-106">Il se peut que votre gestionnaire d’interface utilisateur externe doive uniquement analyser les messages Windows Installer sans effectuer aucune opération qui affecte l’installation.</span><span class="sxs-lookup"><span data-stu-id="cb042-106">Your external UI handler may only need to monitor Windows Installer messages without performing any operation that affects the installation.</span></span>

<span data-ttu-id="cb042-107">Les messages de Windows Installer suivants contiennent des chaînes qui peuvent être affichées par une boîte de dialogue et ne nécessitent aucun traitement supplémentaire.</span><span class="sxs-lookup"><span data-stu-id="cb042-107">The following Windows Installer messages contain strings that can be displayed by a dialog box and need no additional processing.</span></span> <span data-ttu-id="cb042-108">Ces messages contiennent une liste de boutons et d’icônes qui doivent être affichés par une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="cb042-108">These messages contain a list of buttons and icons that are to be displayed by a dialog box.</span></span> <span data-ttu-id="cb042-109">Vous pouvez utiliser les valeurs **Mo \_ ICONMASK**, **MB \_ DEFMASK** et **MB \_ TYPEMASK** pour spécifier les icônes et les boutons.</span><span class="sxs-lookup"><span data-stu-id="cb042-109">You can use the **MB\_ICONMASK**, **MB\_DEFMASK**, and **MB\_TYPEMASK** values to specify icons and buttons.</span></span>

<dl> <dt>

<span data-ttu-id="cb042-110"><span id="INSTALLMESSAGE_FATALEXIT"></span><span id="installmessage_fatalexit"></span>**INSTALLMESSAGE \_ FATALEXIT**</span><span class="sxs-lookup"><span data-stu-id="cb042-110"><span id="INSTALLMESSAGE_FATALEXIT"></span><span id="installmessage_fatalexit"></span>**INSTALLMESSAGE\_FATALEXIT**</span></span>
</dt> <dd>

<span data-ttu-id="cb042-111">Un arrêt prématuré de l’installation s’est produit.</span><span class="sxs-lookup"><span data-stu-id="cb042-111">Premature termination of installation has occurred.</span></span>

</dd> <dt>

<span data-ttu-id="cb042-112"><span id="INSTALLMESSAGE_ERROR"></span><span id="installmessage_error"></span>**\_erreur INSTALLMESSAGE**</span><span class="sxs-lookup"><span data-stu-id="cb042-112"><span id="INSTALLMESSAGE_ERROR"></span><span id="installmessage_error"></span>**INSTALLMESSAGE\_ERROR**</span></span>
</dt> <dd>

<span data-ttu-id="cb042-113">Message d’erreur mis en forme.</span><span class="sxs-lookup"><span data-stu-id="cb042-113">Formatted error message.</span></span>

</dd> <dt>

<span data-ttu-id="cb042-114"><span id="INSTALLMESSAGE_WARNING"></span><span id="installmessage_warning"></span>**\_Avertissement INSTALLMESSAGE**</span><span class="sxs-lookup"><span data-stu-id="cb042-114"><span id="INSTALLMESSAGE_WARNING"></span><span id="installmessage_warning"></span>**INSTALLMESSAGE\_WARNING**</span></span>
</dt> <dd>

<span data-ttu-id="cb042-115">Message d’avertissement mis en forme.</span><span class="sxs-lookup"><span data-stu-id="cb042-115">Formatted warning message.</span></span>

</dd> <dt>

<span data-ttu-id="cb042-116"><span id="INSTALLMESSAGE_INFO"></span><span id="installmessage_info"></span>**\_informations INSTALLMESSAGE**</span><span class="sxs-lookup"><span data-stu-id="cb042-116"><span id="INSTALLMESSAGE_INFO"></span><span id="installmessage_info"></span>**INSTALLMESSAGE\_INFO**</span></span>
</dt> <dd>

<span data-ttu-id="cb042-117">Message du journal mis en forme.</span><span class="sxs-lookup"><span data-stu-id="cb042-117">Formatted log message.</span></span>

</dd> <dt>

<span data-ttu-id="cb042-118"><span id="INSTALLMESSAGE_USER"></span><span id="installmessage_user"></span>**\_utilisateur INSTALLMESSAGE**</span><span class="sxs-lookup"><span data-stu-id="cb042-118"><span id="INSTALLMESSAGE_USER"></span><span id="installmessage_user"></span>**INSTALLMESSAGE\_USER**</span></span>
</dt> <dd>

<span data-ttu-id="cb042-119">Message utilisateur mis en forme.</span><span class="sxs-lookup"><span data-stu-id="cb042-119">Formatted user message.</span></span>

</dd> <dt>

<span data-ttu-id="cb042-120"><span id="INSTALLMESSAGE_OUTOFDISKSPACE"></span><span id="installmessage_outofdiskspace"></span>**INSTALLMESSAGE \_ OUTOFDISKSPACE**</span><span class="sxs-lookup"><span data-stu-id="cb042-120"><span id="INSTALLMESSAGE_OUTOFDISKSPACE"></span><span id="installmessage_outofdiskspace"></span>**INSTALLMESSAGE\_OUTOFDISKSPACE**</span></span>
</dt> <dd>

<span data-ttu-id="cb042-121">Message mis en forme indiquant une condition d’espace disque insuffisant</span><span class="sxs-lookup"><span data-stu-id="cb042-121">Formatted message indicating an out of disk space condition</span></span>

</dd> </dl>

<span data-ttu-id="cb042-122">Le gestionnaire de l’utilisateur externe peut utiliser les messages de Windows Installer suivants pour surveiller une séquence de l’interface utilisateur Windows Installer.</span><span class="sxs-lookup"><span data-stu-id="cb042-122">The external user handler can use the following Windows Installer messages to monitor a sequence of the Windows Installer UI.</span></span> <span data-ttu-id="cb042-123">Le programme d’installation envoie ces messages au début d’une séquence d’interface utilisateur Windows Installer, chaque fois que chaque boîte de dialogue est affichée et à la fin de la séquence d’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cb042-123">The installer sends these messages at the start of a Windows Installer UI sequence, as each dialog box is displayed, and at the end of the UI sequence.</span></span> <span data-ttu-id="cb042-124">Aucun traitement n’est nécessaire pour utiliser ces messages.</span><span class="sxs-lookup"><span data-stu-id="cb042-124">No processing is required to use these messages.</span></span>

<dl> <dt>

<span data-ttu-id="cb042-125"><span id="INSTALLMESSAGE_TERMINATE"></span><span id="installmessage_terminate"></span>INSTALLMESSAGE \_ Terminate</span><span class="sxs-lookup"><span data-stu-id="cb042-125"><span id="INSTALLMESSAGE_TERMINATE"></span><span id="installmessage_terminate"></span>INSTALLMESSAGE\_TERMINATE</span></span>
</dt> <dd>

<span data-ttu-id="cb042-126">Ce message indique la fin de la séquence de l’interface utilisateur.</span><span class="sxs-lookup"><span data-stu-id="cb042-126">This message indicates the end of the UI sequence.</span></span> <span data-ttu-id="cb042-127">La chaîne est une chaîne NULL.</span><span class="sxs-lookup"><span data-stu-id="cb042-127">The string is a null string.</span></span>

</dd> <dt>

<span data-ttu-id="cb042-128"><span id="INSTALLMESSAGE_INITIALIZE"></span><span id="installmessage_initialize"></span>initialisation de INSTALLMESSAGE \_</span><span class="sxs-lookup"><span data-stu-id="cb042-128"><span id="INSTALLMESSAGE_INITIALIZE"></span><span id="installmessage_initialize"></span>INSTALLMESSAGE\_INITIALIZE</span></span>
</dt> <dd>

<span data-ttu-id="cb042-129">Ce message indique que la séquence d’interface utilisateur a démarré.</span><span class="sxs-lookup"><span data-stu-id="cb042-129">This message indicates that the UI sequence has started.</span></span> <span data-ttu-id="cb042-130">La chaîne est une chaîne NULL.</span><span class="sxs-lookup"><span data-stu-id="cb042-130">The string is a null string.</span></span>

</dd> <dt>

<span data-ttu-id="cb042-131"><span id="INSTALLMESSAGE_SHOWDIALOG"></span><span id="installmessage_showdialog"></span>INSTALLMESSAGE, \_ SHOWDIALOG</span><span class="sxs-lookup"><span data-stu-id="cb042-131"><span id="INSTALLMESSAGE_SHOWDIALOG"></span><span id="installmessage_showdialog"></span>INSTALLMESSAGE\_SHOWDIALOG</span></span>
</dt> <dd>

<span data-ttu-id="cb042-132">La chaîne contient le nom de la boîte de dialogue active.</span><span class="sxs-lookup"><span data-stu-id="cb042-132">The string contains the name of the current dialog box.</span></span>

</dd> </dl>

<span data-ttu-id="cb042-133">Les messages de Windows Installer suivants requièrent un traitement supplémentaire par le gestionnaire de l’interface utilisateur externe.</span><span class="sxs-lookup"><span data-stu-id="cb042-133">The following Windows Installer messages require additional processing by the external UI handler.</span></span>

<dl> <dt>

<span data-ttu-id="cb042-134"><span id="INSTALLMESSAGE_RESOLVESOURCE"></span><span id="installmessage_resolvesource"></span>**INSTALLMESSAGE \_ RESOLVESOURCE**</span><span class="sxs-lookup"><span data-stu-id="cb042-134"><span id="INSTALLMESSAGE_RESOLVESOURCE"></span><span id="installmessage_resolvesource"></span>**INSTALLMESSAGE\_RESOLVESOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="cb042-135">Le gestionnaire d’interface utilisateur externe doit retourner 0 et autoriser Windows Installer à gérer le message.</span><span class="sxs-lookup"><span data-stu-id="cb042-135">The external user interface handler must return 0 and allow Windows Installer to handle the message.</span></span> <span data-ttu-id="cb042-136">Le gestionnaire d’interface utilisateur externe peut surveiller ce message, mais il ne doit effectuer aucune action qui affecte l’installation.</span><span class="sxs-lookup"><span data-stu-id="cb042-136">The external user interface handler can monitor for this message, but it should not perform any action that affects the installation .</span></span>

</dd> <dt>

<span data-ttu-id="cb042-137"><span id="INSTALLMESSAGE_FILESINUSE"></span><span id="installmessage_filesinuse"></span>**INSTALLMESSAGE \_ FILESINUSE**</span><span class="sxs-lookup"><span data-stu-id="cb042-137"><span id="INSTALLMESSAGE_FILESINUSE"></span><span id="installmessage_filesinuse"></span>**INSTALLMESSAGE\_FILESINUSE**</span></span>
</dt> <dd>

<span data-ttu-id="cb042-138">L’interface utilisateur externe doit afficher une [boîte de dialogue FilesInUse](filesinuse-dialog.md) en réponse à ce message.</span><span class="sxs-lookup"><span data-stu-id="cb042-138">The external UI should display a [FilesInUse dialog](filesinuse-dialog.md) in response to this message.</span></span>

</dd> <dt>

<span data-ttu-id="cb042-139"><span id="INSTALLMESSAGE_RMFILESINUSE"></span><span id="installmessage_rmfilesinuse"></span>**INSTALLMESSAGE \_ RMFILESINUSE**</span><span class="sxs-lookup"><span data-stu-id="cb042-139"><span id="INSTALLMESSAGE_RMFILESINUSE"></span><span id="installmessage_rmfilesinuse"></span>**INSTALLMESSAGE\_RMFILESINUSE**</span></span>
</dt> <dd>

<span data-ttu-id="cb042-140">L’interface utilisateur externe doit afficher une [boîte de dialogue MsiRMFilesInUse](msirmfilesinuse-dialog.md) en réponse à ce message.</span><span class="sxs-lookup"><span data-stu-id="cb042-140">The external UI should display a [MsiRMFilesInUse dialog](msirmfilesinuse-dialog.md) in response to this message.</span></span> <span data-ttu-id="cb042-141">Disponible à partir de Windows Installer version 4,0.</span><span class="sxs-lookup"><span data-stu-id="cb042-141">Available beginning with Windows Installer version 4.0.</span></span> <span data-ttu-id="cb042-142">Pour plus d’informations sur ce message, consultez [utilisation du gestionnaire de redémarrage avec une interface utilisateur externe](using-restart-manager-with-an-external-ui-.md).</span><span class="sxs-lookup"><span data-stu-id="cb042-142">For more information about this message see [Using Restart Manager with an External UI](using-restart-manager-with-an-external-ui-.md).</span></span>

</dd> <dt>

<span data-ttu-id="cb042-143"><span id="INSTALLMESSAGE_ACTIONSTART"></span><span id="installmessage_actionstart"></span>**INSTALLMESSAGE \_ ACTIONSTART**</span><span class="sxs-lookup"><span data-stu-id="cb042-143"><span id="INSTALLMESSAGE_ACTIONSTART"></span><span id="installmessage_actionstart"></span>**INSTALLMESSAGE\_ACTIONSTART**</span></span>
</dt> <dd>

<span data-ttu-id="cb042-144">Ce message contient des informations sur l’action en cours.</span><span class="sxs-lookup"><span data-stu-id="cb042-144">This message gives information about the current action.</span></span> <span data-ttu-id="cb042-145">Le format est action \[ 1 \] : \[ 2 \] .</span><span class="sxs-lookup"><span data-stu-id="cb042-145">The format is Action \[1\]: \[2\].</span></span> <span data-ttu-id="cb042-146">\[3 \] , où un signe deux-points est utilisé pour séparer le champ 1 et le champ 2 et un point est utilisé pour séparer les champs 2 et 3.</span><span class="sxs-lookup"><span data-stu-id="cb042-146">\[3\], where a colon is used to separate Field 1 and Field 2 and a period is used to separate Field 2 and Field 3.</span></span> <span data-ttu-id="cb042-147">Le champ \[ 1 \] contient l’heure à laquelle l’action a été démarrée à l’aide du format de propriété [**Time**](time.md) .</span><span class="sxs-lookup"><span data-stu-id="cb042-147">Field \[1\] contains the time the action was started using the [**Time**](time.md) property format.</span></span> <span data-ttu-id="cb042-148">Le champ \[ 2 \] contient le nom de l’action à partir de la table de séquences.</span><span class="sxs-lookup"><span data-stu-id="cb042-148">Field \[2\] contains the action's name from the sequence table.</span></span> <span data-ttu-id="cb042-149">Le champ \[ 3 \] donne la description de l’action à partir de la [table ActionText](actiontext-table.md) ou de la fonction [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) .</span><span class="sxs-lookup"><span data-stu-id="cb042-149">Field \[3\] gives the action's description from the [ActionText table](actiontext-table.md) or from the [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) function.</span></span>

</dd> <dt>

<span data-ttu-id="cb042-150"><span id="INSTALLMESSAGE_ACTIONDATA"></span><span id="installmessage_actiondata"></span>**INSTALLMESSAGE \_ ACTIONDATA**</span><span class="sxs-lookup"><span data-stu-id="cb042-150"><span id="INSTALLMESSAGE_ACTIONDATA"></span><span id="installmessage_actiondata"></span>**INSTALLMESSAGE\_ACTIONDATA**</span></span>
</dt> <dd>

<span data-ttu-id="cb042-151">Le format de cette chaîne est spécifié par la valeur de [modèle](template.md) fournie dans la [table ActionText](actiontext-table.md) ou par la fonction [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) .</span><span class="sxs-lookup"><span data-stu-id="cb042-151">The format of this string is specified by the [Template](template.md) value provided in the [ActionText table](actiontext-table.md) or by the [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) function.</span></span> <span data-ttu-id="cb042-152">Une fois le message **INSTALLMESSAGE \_ ACTIONSTART** , il peut y avoir un nombre illimité de messages **INSTALLMESSAGE \_ ACTIONDATA** .</span><span class="sxs-lookup"><span data-stu-id="cb042-152">There can be an unlimited number of **INSTALLMESSAGE\_ACTIONDATA** messages after the **INSTALLMESSAGE\_ACTIONSTART** message.</span></span>

</dd> <dt>

<span data-ttu-id="cb042-153"><span id="INSTALLMESSAGE_COMMONDATA"></span><span id="installmessage_commondata"></span>**INSTALLMESSAGE \_ COMMONDATA**</span><span class="sxs-lookup"><span data-stu-id="cb042-153"><span id="INSTALLMESSAGE_COMMONDATA"></span><span id="installmessage_commondata"></span>**INSTALLMESSAGE\_COMMONDATA**</span></span>
</dt> <dd>

<span data-ttu-id="cb042-154">Ce message comporte trois sous-types : Language, Caption et CancelShow.</span><span class="sxs-lookup"><span data-stu-id="cb042-154">This message has three subtypes: Language, Caption, and CancelShow.</span></span> <span data-ttu-id="cb042-155">La chaîne peut avoir trois champs séparés par un nombre suivi d’un signe deux-points.</span><span class="sxs-lookup"><span data-stu-id="cb042-155">The string can have three fields delimited by a number followed by a colon.</span></span> <span data-ttu-id="cb042-156">Tous les champs ne sont pas requis.</span><span class="sxs-lookup"><span data-stu-id="cb042-156">Not all fields are required.</span></span> <span data-ttu-id="cb042-157">Le message peut être une chaîne NULL ou vide ("").</span><span class="sxs-lookup"><span data-stu-id="cb042-157">The message can be a NULL or empty ("") string.</span></span>

<dl> <dt>

<span data-ttu-id="cb042-158"><span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Sous</span><span class="sxs-lookup"><span data-stu-id="cb042-158"><span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Language</span></span>
</dt> <dd>

<span data-ttu-id="cb042-159">Le champ 1 contient la valeur 0 pour indiquer que cette chaîne contient des informations de langue.</span><span class="sxs-lookup"><span data-stu-id="cb042-159">Field 1 contains the value 0 to indicate this string contains language information.</span></span> <span data-ttu-id="cb042-160">Le champ 2 contient une valeur de [langage](language.md) qui est un identificateur de langue numérique (LANGID). Le champ 3 est une valeur qui représente une page de codes ANSI.</span><span class="sxs-lookup"><span data-stu-id="cb042-160">Field 2 contains a [Language](language.md) value that is a numeric language identifier (LANGID.) Field 3 is a value that represents an ANSI code page.</span></span>

</dd> <dt>

<span data-ttu-id="cb042-161"><span id="Caption"></span><span id="caption"></span><span id="CAPTION"></span>-</span><span class="sxs-lookup"><span data-stu-id="cb042-161"><span id="Caption"></span><span id="caption"></span><span id="CAPTION"></span>Caption</span></span>
</dt> <dd>

<span data-ttu-id="cb042-162">Le champ 1 contient la valeur 1 pour indiquer que cette chaîne contient le texte d’une légende ou d’un titre.</span><span class="sxs-lookup"><span data-stu-id="cb042-162">Field 1 contains the value 1 to indicate this string contains the text of a caption or title.</span></span> <span data-ttu-id="cb042-163">Le champ 2 contient du texte qu’un gestionnaire d’interface utilisateur externe peut utiliser comme légende de titre pour une boîte de dialogue.</span><span class="sxs-lookup"><span data-stu-id="cb042-163">Field 2 contains text that an external UI handler can use as a caption of title for a dialog box.</span></span> <span data-ttu-id="cb042-164">Le champ 3 a la valeur NULL ou est une chaîne vide ("").</span><span class="sxs-lookup"><span data-stu-id="cb042-164">Field 3 is NULL or an empty ("") string.</span></span> <span data-ttu-id="cb042-165">Le champ 3 peut être absent d’un message de légende.</span><span class="sxs-lookup"><span data-stu-id="cb042-165">Field 3 can be absent from a the Caption message.</span></span>

</dd> <dt>

<span data-ttu-id="cb042-166"><span id="CancelShow"></span><span id="cancelshow"></span><span id="CANCELSHOW"></span>CancelShow</span><span class="sxs-lookup"><span data-stu-id="cb042-166"><span id="CancelShow"></span><span id="cancelshow"></span><span id="CANCELSHOW"></span>CancelShow</span></span>
</dt> <dd>

<span data-ttu-id="cb042-167">Le champ 1 contient la valeur 2 pour indiquer que cette chaîne contient des informations indiquant s’il faut afficher le bouton Annuler.</span><span class="sxs-lookup"><span data-stu-id="cb042-167">Field 1 contains the value 2 to indicate this string contains information about whether to display the cancel button.</span></span> <span data-ttu-id="cb042-168">Si le bouton Annuler doit être masqué, le champ 2 contient la valeur 0.</span><span class="sxs-lookup"><span data-stu-id="cb042-168">If the cancel button should be hidden, Field 2 contains the value 0.</span></span> <span data-ttu-id="cb042-169">Si le bouton Annuler doit être visible, le champ 2 contient la valeur 1.</span><span class="sxs-lookup"><span data-stu-id="cb042-169">If the cancel button should be visible, Field 2 contains the value 1.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="cb042-170"><span id="INSTALLMESSAGE_PROGRESS"></span><span id="installmessage_progress"></span>progression de INSTALLMESSAGE \_</span><span class="sxs-lookup"><span data-stu-id="cb042-170"><span id="INSTALLMESSAGE_PROGRESS"></span><span id="installmessage_progress"></span>INSTALLMESSAGE\_PROGRESS</span></span>
</dt> <dd>

<span data-ttu-id="cb042-171">Ce message comporte quatre sous-types : Reset, ActionInfo, ProgressReport et ProgressAddition.</span><span class="sxs-lookup"><span data-stu-id="cb042-171">This message has four subtypes: Reset, ActionInfo, ProgressReport, and ProgressAddition.</span></span> <span data-ttu-id="cb042-172">Le gestionnaire externe ne doit agir sur aucun de ces messages tant que le premier message de progression de la réinitialisation n’a pas été reçu.</span><span class="sxs-lookup"><span data-stu-id="cb042-172">The external handler should not act upon any of these messages until the first a Reset progress message is received.</span></span> <span data-ttu-id="cb042-173">Cela fournit une estimation du nombre total de graduations pour la barre de progression.</span><span class="sxs-lookup"><span data-stu-id="cb042-173">This provides an estimate of the total number of ticks for the progress bar.</span></span>

<dl> <dt>

<span data-ttu-id="cb042-174"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>Initialisation</span><span class="sxs-lookup"><span data-stu-id="cb042-174"><span id="Reset"></span><span id="reset"></span><span id="RESET"></span>Reset</span></span>
</dt> <dd>

<span data-ttu-id="cb042-175">Le champ 1 contient la valeur 0 pour indiquer une réinitialisation de la barre de progression.</span><span class="sxs-lookup"><span data-stu-id="cb042-175">Field 1 contains the value 0 to indicate a reset of the progress bar.</span></span> <span data-ttu-id="cb042-176">Le champ 2 contient le nombre total de graduations dans la barre de progression.</span><span class="sxs-lookup"><span data-stu-id="cb042-176">Field 2 contains the total number of ticks in the progress bar.</span></span> <span data-ttu-id="cb042-177">Le champ 3 contient la valeur 0 pour le mouvement de la barre de progression vers l’avant.</span><span class="sxs-lookup"><span data-stu-id="cb042-177">Field 3 contains the value 0 for forward progress bar motion.</span></span> <span data-ttu-id="cb042-178">Le champ 3 contient la valeur 1 pour le mouvement de la barre de progression arrière.</span><span class="sxs-lookup"><span data-stu-id="cb042-178">Field 3 contains the value 1 for backward progress bar motion.</span></span> <span data-ttu-id="cb042-179">La valeur 0 dans le champ 4 signifie que l’installation est en cours et que le temps restant peut être calculé.</span><span class="sxs-lookup"><span data-stu-id="cb042-179">The value 0 in Field 4 means the installation is in progress and the time remaining may be calculated.</span></span> <span data-ttu-id="cb042-180">La valeur 1 dans le champ 4 signifie que le script est en cours d’exécution et qu’un « Veuillez patienter... » le message peut être affiché.</span><span class="sxs-lookup"><span data-stu-id="cb042-180">The value 1 in Field 4 means script is being run and a "Please wait ..." message can be displayed.</span></span> <span data-ttu-id="cb042-181">L’estimation du nombre total de graduations est une approximation et peut être inexacte.</span><span class="sxs-lookup"><span data-stu-id="cb042-181">The estimate of the total number of ticks is an approximation and may be inaccurate.</span></span>

</dd> <dt>

<span data-ttu-id="cb042-182"><span id="ActionInfo"></span><span id="actioninfo"></span><span id="ACTIONINFO"></span>ActionInfo</span><span class="sxs-lookup"><span data-stu-id="cb042-182"><span id="ActionInfo"></span><span id="actioninfo"></span><span id="ACTIONINFO"></span>ActionInfo</span></span>
</dt> <dd>

<span data-ttu-id="cb042-183">Le champ 1 contient la valeur 1 pour indiquer que cette chaîne contient des informations sur l’action.</span><span class="sxs-lookup"><span data-stu-id="cb042-183">Field 1 contains the value 1 to indicate this string contains action information.</span></span> <span data-ttu-id="cb042-184">Le champ 2 contient le nombre de graduations que la barre de progression déplace pour chaque message ActionData envoyé par l’action actuelle.</span><span class="sxs-lookup"><span data-stu-id="cb042-184">Field 2 contains the number of ticks the progress bar moves for each ActionData message sent by the current action.</span></span> <span data-ttu-id="cb042-185">Si le champ 3 contient la valeur 0, ignorez le champ 2.</span><span class="sxs-lookup"><span data-stu-id="cb042-185">If Field 3 contains the value 0, ignore Field 2.</span></span> <span data-ttu-id="cb042-186">Si le champ 3 contient la valeur 1, incrémentez la barre de progression du nombre de graduations dans le champ 2 pour chaque message ActionData envoyé par l’action actuelle.</span><span class="sxs-lookup"><span data-stu-id="cb042-186">If Field 3 contains the value 1, increment the progress bar by the number of ticks in Field 2 for each ActionData message sent by the current action.</span></span> <span data-ttu-id="cb042-187">Le champ 4 n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="cb042-187">Field 4 is unused.</span></span>

</dd> <dt>

<span data-ttu-id="cb042-188"><span id="ProgressReport"></span><span id="progressreport"></span><span id="PROGRESSREPORT"></span>ProgressReport</span><span class="sxs-lookup"><span data-stu-id="cb042-188"><span id="ProgressReport"></span><span id="progressreport"></span><span id="PROGRESSREPORT"></span>ProgressReport</span></span>
</dt> <dd>

<span data-ttu-id="cb042-189">Le champ 1 contient la valeur 2 pour indiquer que cette chaîne contient des informations de progression.</span><span class="sxs-lookup"><span data-stu-id="cb042-189">Field 1 contains the value 2 to indicate this string contains progress information.</span></span> <span data-ttu-id="cb042-190">Le champ 2 contient le nombre de graduations que la barre de progression a déplacées.</span><span class="sxs-lookup"><span data-stu-id="cb042-190">Field 2 contains the number of ticks the progress bar has moved.</span></span> <span data-ttu-id="cb042-191">Le champ 3 n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="cb042-191">Field 3 is unused.</span></span> <span data-ttu-id="cb042-192">Le champ 4 n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="cb042-192">Field 4 is unused.</span></span>

</dd> <dt>

<span data-ttu-id="cb042-193"><span id="ProgressAddition"></span><span id="progressaddition"></span><span id="PROGRESSADDITION"></span>ProgressAddition</span><span class="sxs-lookup"><span data-stu-id="cb042-193"><span id="ProgressAddition"></span><span id="progressaddition"></span><span id="PROGRESSADDITION"></span>ProgressAddition</span></span>
</dt> <dd>

<span data-ttu-id="cb042-194">Le champ 1 contient la valeur 3 pour indiquer qu’une action peut ajouter graduation la barre de progression.</span><span class="sxs-lookup"><span data-stu-id="cb042-194">Field 1 contains the value 3 to indicate that an action can add ticks the progress bar.</span></span> <span data-ttu-id="cb042-195">Le champ 2 contient le nombre de graduations à ajouter au nombre total de cycles de progression attendu.</span><span class="sxs-lookup"><span data-stu-id="cb042-195">Field 2 contains the number of ticks to add to total expected count of progress ticks.</span></span> <span data-ttu-id="cb042-196">Le champ 3 n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="cb042-196">Field 3 is unused.</span></span> <span data-ttu-id="cb042-197">Le champ 4 n’est pas utilisé.</span><span class="sxs-lookup"><span data-stu-id="cb042-197">Field 4 is unused.</span></span>

</dd> </dl> </dd> </dl>

 

 



