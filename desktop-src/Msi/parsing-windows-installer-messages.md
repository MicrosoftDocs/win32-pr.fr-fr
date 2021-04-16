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
# <a name="parsing-windows-installer-messages"></a>Analyse des messages de Windows Installer

Un gestionnaire d’interface utilisateur externe peut traiter la liste des messages du programme d’installation spécifiée par le paramètre *dwMessagedFilter* de la fonction [**MsiSetExternalUI**](/windows/desktop/api/Msi/nf-msi-msisetexternaluia) . Certains de ces messages contiennent des chaînes qui peuvent être utilisées directement, et d’autres messages peuvent avoir besoin d’être analysés et traités par le gestionnaire d’interface utilisateur externe pour être utiles. Il se peut que votre gestionnaire d’interface utilisateur externe doive uniquement analyser les messages Windows Installer sans effectuer aucune opération qui affecte l’installation.

Les messages de Windows Installer suivants contiennent des chaînes qui peuvent être affichées par une boîte de dialogue et ne nécessitent aucun traitement supplémentaire. Ces messages contiennent une liste de boutons et d’icônes qui doivent être affichés par une boîte de dialogue. Vous pouvez utiliser les valeurs **Mo \_ ICONMASK**, **MB \_ DEFMASK** et **MB \_ TYPEMASK** pour spécifier les icônes et les boutons.

<dl> <dt>

<span id="INSTALLMESSAGE_FATALEXIT"></span><span id="installmessage_fatalexit"></span>**INSTALLMESSAGE \_ FATALEXIT**
</dt> <dd>

Un arrêt prématuré de l’installation s’est produit.

</dd> <dt>

<span id="INSTALLMESSAGE_ERROR"></span><span id="installmessage_error"></span>**\_erreur INSTALLMESSAGE**
</dt> <dd>

Message d’erreur mis en forme.

</dd> <dt>

<span id="INSTALLMESSAGE_WARNING"></span><span id="installmessage_warning"></span>**\_Avertissement INSTALLMESSAGE**
</dt> <dd>

Message d’avertissement mis en forme.

</dd> <dt>

<span id="INSTALLMESSAGE_INFO"></span><span id="installmessage_info"></span>**\_informations INSTALLMESSAGE**
</dt> <dd>

Message du journal mis en forme.

</dd> <dt>

<span id="INSTALLMESSAGE_USER"></span><span id="installmessage_user"></span>**\_utilisateur INSTALLMESSAGE**
</dt> <dd>

Message utilisateur mis en forme.

</dd> <dt>

<span id="INSTALLMESSAGE_OUTOFDISKSPACE"></span><span id="installmessage_outofdiskspace"></span>**INSTALLMESSAGE \_ OUTOFDISKSPACE**
</dt> <dd>

Message mis en forme indiquant une condition d’espace disque insuffisant

</dd> </dl>

Le gestionnaire de l’utilisateur externe peut utiliser les messages de Windows Installer suivants pour surveiller une séquence de l’interface utilisateur Windows Installer. Le programme d’installation envoie ces messages au début d’une séquence d’interface utilisateur Windows Installer, chaque fois que chaque boîte de dialogue est affichée et à la fin de la séquence d’interface utilisateur. Aucun traitement n’est nécessaire pour utiliser ces messages.

<dl> <dt>

<span id="INSTALLMESSAGE_TERMINATE"></span><span id="installmessage_terminate"></span>INSTALLMESSAGE \_ Terminate
</dt> <dd>

Ce message indique la fin de la séquence de l’interface utilisateur. La chaîne est une chaîne NULL.

</dd> <dt>

<span id="INSTALLMESSAGE_INITIALIZE"></span><span id="installmessage_initialize"></span>initialisation de INSTALLMESSAGE \_
</dt> <dd>

Ce message indique que la séquence d’interface utilisateur a démarré. La chaîne est une chaîne NULL.

</dd> <dt>

<span id="INSTALLMESSAGE_SHOWDIALOG"></span><span id="installmessage_showdialog"></span>INSTALLMESSAGE, \_ SHOWDIALOG
</dt> <dd>

La chaîne contient le nom de la boîte de dialogue active.

</dd> </dl>

Les messages de Windows Installer suivants requièrent un traitement supplémentaire par le gestionnaire de l’interface utilisateur externe.

<dl> <dt>

<span id="INSTALLMESSAGE_RESOLVESOURCE"></span><span id="installmessage_resolvesource"></span>**INSTALLMESSAGE \_ RESOLVESOURCE**
</dt> <dd>

Le gestionnaire d’interface utilisateur externe doit retourner 0 et autoriser Windows Installer à gérer le message. Le gestionnaire d’interface utilisateur externe peut surveiller ce message, mais il ne doit effectuer aucune action qui affecte l’installation.

</dd> <dt>

<span id="INSTALLMESSAGE_FILESINUSE"></span><span id="installmessage_filesinuse"></span>**INSTALLMESSAGE \_ FILESINUSE**
</dt> <dd>

L’interface utilisateur externe doit afficher une [boîte de dialogue FilesInUse](filesinuse-dialog.md) en réponse à ce message.

</dd> <dt>

<span id="INSTALLMESSAGE_RMFILESINUSE"></span><span id="installmessage_rmfilesinuse"></span>**INSTALLMESSAGE \_ RMFILESINUSE**
</dt> <dd>

L’interface utilisateur externe doit afficher une [boîte de dialogue MsiRMFilesInUse](msirmfilesinuse-dialog.md) en réponse à ce message. Disponible à partir de Windows Installer version 4,0. Pour plus d’informations sur ce message, consultez [utilisation du gestionnaire de redémarrage avec une interface utilisateur externe](using-restart-manager-with-an-external-ui-.md).

</dd> <dt>

<span id="INSTALLMESSAGE_ACTIONSTART"></span><span id="installmessage_actionstart"></span>**INSTALLMESSAGE \_ ACTIONSTART**
</dt> <dd>

Ce message contient des informations sur l’action en cours. Le format est action \[ 1 \] : \[ 2 \] . \[3 \] , où un signe deux-points est utilisé pour séparer le champ 1 et le champ 2 et un point est utilisé pour séparer les champs 2 et 3. Le champ \[ 1 \] contient l’heure à laquelle l’action a été démarrée à l’aide du format de propriété [**Time**](time.md) . Le champ \[ 2 \] contient le nom de l’action à partir de la table de séquences. Le champ \[ 3 \] donne la description de l’action à partir de la [table ActionText](actiontext-table.md) ou de la fonction [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) .

</dd> <dt>

<span id="INSTALLMESSAGE_ACTIONDATA"></span><span id="installmessage_actiondata"></span>**INSTALLMESSAGE \_ ACTIONDATA**
</dt> <dd>

Le format de cette chaîne est spécifié par la valeur de [modèle](template.md) fournie dans la [table ActionText](actiontext-table.md) ou par la fonction [**MsiProcessMessage**](/windows/desktop/api/Msiquery/nf-msiquery-msiprocessmessage) . Une fois le message **INSTALLMESSAGE \_ ACTIONSTART** , il peut y avoir un nombre illimité de messages **INSTALLMESSAGE \_ ACTIONDATA** .

</dd> <dt>

<span id="INSTALLMESSAGE_COMMONDATA"></span><span id="installmessage_commondata"></span>**INSTALLMESSAGE \_ COMMONDATA**
</dt> <dd>

Ce message comporte trois sous-types : Language, Caption et CancelShow. La chaîne peut avoir trois champs séparés par un nombre suivi d’un signe deux-points. Tous les champs ne sont pas requis. Le message peut être une chaîne NULL ou vide ("").

<dl> <dt>

<span id="Language"></span><span id="language"></span><span id="LANGUAGE"></span>Sous
</dt> <dd>

Le champ 1 contient la valeur 0 pour indiquer que cette chaîne contient des informations de langue. Le champ 2 contient une valeur de [langage](language.md) qui est un identificateur de langue numérique (LANGID). Le champ 3 est une valeur qui représente une page de codes ANSI.

</dd> <dt>

<span id="Caption"></span><span id="caption"></span><span id="CAPTION"></span>-
</dt> <dd>

Le champ 1 contient la valeur 1 pour indiquer que cette chaîne contient le texte d’une légende ou d’un titre. Le champ 2 contient du texte qu’un gestionnaire d’interface utilisateur externe peut utiliser comme légende de titre pour une boîte de dialogue. Le champ 3 a la valeur NULL ou est une chaîne vide (""). Le champ 3 peut être absent d’un message de légende.

</dd> <dt>

<span id="CancelShow"></span><span id="cancelshow"></span><span id="CANCELSHOW"></span>CancelShow
</dt> <dd>

Le champ 1 contient la valeur 2 pour indiquer que cette chaîne contient des informations indiquant s’il faut afficher le bouton Annuler. Si le bouton Annuler doit être masqué, le champ 2 contient la valeur 0. Si le bouton Annuler doit être visible, le champ 2 contient la valeur 1.

</dd> </dl> </dd> <dt>

<span id="INSTALLMESSAGE_PROGRESS"></span><span id="installmessage_progress"></span>progression de INSTALLMESSAGE \_
</dt> <dd>

Ce message comporte quatre sous-types : Reset, ActionInfo, ProgressReport et ProgressAddition. Le gestionnaire externe ne doit agir sur aucun de ces messages tant que le premier message de progression de la réinitialisation n’a pas été reçu. Cela fournit une estimation du nombre total de graduations pour la barre de progression.

<dl> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>Initialisation
</dt> <dd>

Le champ 1 contient la valeur 0 pour indiquer une réinitialisation de la barre de progression. Le champ 2 contient le nombre total de graduations dans la barre de progression. Le champ 3 contient la valeur 0 pour le mouvement de la barre de progression vers l’avant. Le champ 3 contient la valeur 1 pour le mouvement de la barre de progression arrière. La valeur 0 dans le champ 4 signifie que l’installation est en cours et que le temps restant peut être calculé. La valeur 1 dans le champ 4 signifie que le script est en cours d’exécution et qu’un « Veuillez patienter... » le message peut être affiché. L’estimation du nombre total de graduations est une approximation et peut être inexacte.

</dd> <dt>

<span id="ActionInfo"></span><span id="actioninfo"></span><span id="ACTIONINFO"></span>ActionInfo
</dt> <dd>

Le champ 1 contient la valeur 1 pour indiquer que cette chaîne contient des informations sur l’action. Le champ 2 contient le nombre de graduations que la barre de progression déplace pour chaque message ActionData envoyé par l’action actuelle. Si le champ 3 contient la valeur 0, ignorez le champ 2. Si le champ 3 contient la valeur 1, incrémentez la barre de progression du nombre de graduations dans le champ 2 pour chaque message ActionData envoyé par l’action actuelle. Le champ 4 n’est pas utilisé.

</dd> <dt>

<span id="ProgressReport"></span><span id="progressreport"></span><span id="PROGRESSREPORT"></span>ProgressReport
</dt> <dd>

Le champ 1 contient la valeur 2 pour indiquer que cette chaîne contient des informations de progression. Le champ 2 contient le nombre de graduations que la barre de progression a déplacées. Le champ 3 n’est pas utilisé. Le champ 4 n’est pas utilisé.

</dd> <dt>

<span id="ProgressAddition"></span><span id="progressaddition"></span><span id="PROGRESSADDITION"></span>ProgressAddition
</dt> <dd>

Le champ 1 contient la valeur 3 pour indiquer qu’une action peut ajouter graduation la barre de progression. Le champ 2 contient le nombre de graduations à ajouter au nombre total de cycles de progression attendu. Le champ 3 n’est pas utilisé. Le champ 4 n’est pas utilisé.

</dd> </dl> </dd> </dl>

 

 



