---
description: 'En savoir plus sur : exemples d’outils VShadow'
ms.assetid: 6a69b75b-ee4a-4613-ba05-d2deb42759b7
title: Exemples d’outils VShadow
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86ec0a753f2865be98cfed76cd192a73cfc785b3fcdc487f7685c9f4ae7d52e8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119056347"
---
# <a name="vshadow-tool-examples"></a>Exemples d’outils VShadow

Les exemples suivants montrent comment utiliser l’outil VShadow pour effectuer les tâches les plus courantes :

-   [Accès aux propriétés des clichés instantanés à partir d’un script CMD](#accessing-shadow-copy-properties-from-a-cmd-script)
-   [Accès aux clichés instantanés non persistants](#accessing-nonpersistent-shadow-copies)
-   [Copie d’un fichier à partir d’un cliché instantané](#copying-a-file-from-a-shadow-copy)
-   [Énumération de tous les fichiers sur un appareil de clichés instantanés](#enumerating-all-files-on-a-shadow-copy-device)
-   [Importation d’un cliché instantané transportable](#importing-a-transportable-shadow-copy)
-   [Ajout d’enregistreurs ou de composants](#including-writers-or-components)
-   [Exclusion d’enregistreurs ou de composants](#excluding-writers-or-components)
-   [Interruption des jeux de clichés instantanés à l’aide de la méthode BreakSnapshotSetEx](#breaking-shadow-copy-sets-using-the-breaksnapshotsetex-method)

Pour obtenir la liste complète des options de ligne de commande et leur utilisation, consultez [outil VShadow et exemple](vshadow-tool-and-sample.md).

## <a name="accessing-shadow-copy-properties-from-a-cmd-script"></a>Accès aux propriétés des clichés instantanés à partir d’un script CMD

Si vous utilisez l’indicateur **-script** facultatif lors de la création de clichés instantanés, VShadow crée un fichier de script cmd contenant les variables d’environnement associées aux clichés instantanés nouvellement créés, comme suit :

-   L’ID du jeu de clichés instantanés, qui est stocké dans la variable d’environnement% VSHADOW \_ Set \_ ID%
-   Les ID de cliché instantané, qui sont stockés dans des variables au format% VSHADOW \_ ID \_ *nnn*%, où *nnn* représente l’index du volume source dans la ligne de commande VSHADOW
-   Les noms des appareils de clichés instantanés, qui sont stockés dans des variables au format% VSHADOW de l' \_ appareil \_ *nnn*%, où *nnn* est l’index du volume source dans la ligne de commande VSHADOW

Vous pouvez utiliser le fichier CMD généré pour effectuer des opérations de gestion limitées sur les clichés instantanés.

> [!Note]  
> L’événement du writer [**BackupComplete**](/windows/win32/api/VsBackup/nf-vsbackup-ivssbackupcomponents-backupcomplete) est envoyé après l’exécution du script **-Exec** . VSS appelle la méthode **IVssBackupComponents :: BackupComplete** pour signaler aux rédacteurs que la sauvegarde est terminée, et les enregistreurs peuvent potentiellement tronquer les journaux à ce stade. Par conséquent, il est important de vérifier que l’ombre/sauvegarde est effectivement terminée. En cas d’échec de la sauvegarde, vous pouvez annuler le processus de création en retournant un code de sortie différent de zéro dans le script/la commande exécuté (e). (consultez la documentation de la commande exit dans la [Windows référence de ligne de commande](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc754340(v=ws.11)).) Si la commande personnalisée retourne avec un code de sortie différent de zéro, la création de clichés instantanés est annulée et **IVssBackupComponents :: BackupComplete** n’est pas appelé.

 

L’exemple suivant montre comment créer un cliché instantané persistant à partir de la ligne de commande et utiliser le script CMD pour l’exposer.

1.  **vshadow-p-NW-script = SETVAR1. cmd c :**
2.  **appeler SETVAR1. cmd**
3.  **C : \\>vshadow-El =% vshadow \_ ID \_ 1%, c : \\ Directory1**

## <a name="accessing-nonpersistent-shadow-copies"></a>Accès aux clichés instantanés non persistants

Les clichés instantanés non persistants sont automatiquement supprimés lorsque le programme qui les crée (dans ce cas, VShadow) se termine. Pour accéder au contenu de ces clichés instantanés, VShadow vous permet d’exécuter un script après la création des clichés instantanés, mais avant la fermeture du programme VShadow.

L’exemple suivant montre comment utiliser l’option de ligne de commande-exec pour exécuter un script appelé « Enum. cmd » :

**vshadow-NW-exec = Enum. cmd c :**

Dans le script exécuté, vous pouvez également exécuter le script SETVAR généré dans cette commande personnalisée. Cela permet au script d’accéder directement au contenu des clichés instantanés. N’oubliez pas que l’appareil instantané peut être récupéré à partir de la \_ variable d’environnement VSHADOW Device \_ nnn.

Voici un exemple de script Enum. cmd :

``` syntax
call SETVAR1.cmd
for /R %VSHADOW_DEVICE_1%\ %%i in (*.*) do @echo %%i
```

Voici la ligne de commande permettant d’exécuter le script Enum. cmd :

**vshadow-NW-exec = c : \\ enum. cmd-script = setvar1. cmd c :**

## <a name="copying-a-file-from-a-shadow-copy"></a>Copie d’un fichier à partir d’un cliché instantané

L’exemple suivant montre comment copier un fichier à partir d’un cliché instantané.

1.  **Répertoire > c : \\somefile.txt**
2.  **vshadow-p-NW-script = SETVAR1. cmd c :**
3.  **appeler SETVAR1. cmd**
4.  **copier% VSHADOW \_ appareil \_ 1% \\somefile.txt c : \\ somefile \_bak.txt**

## <a name="enumerating-all-files-on-a-shadow-copy-device"></a>Énumération de tous les fichiers sur un appareil de clichés instantanés

L’exemple suivant montre comment énumérer tous les fichiers sur un appareil de clichés instantanés à partir d’un fichier de commandes.

1.  **Répertoire > c : \\somefile.txt**
2.  **vshadow-p-NW-script = SETVAR1. cmd c :**
3.  **appeler SETVAR1. cmd**
4.  **pour l’appareil/R% VSHADOW \_ \_ 1% \\ %% i dans ( \* ) do @echo %% i**

## <a name="importing-a-transportable-shadow-copy"></a>Importation d’un cliché instantané transportable

Pour créer un cliché instantané transportable sur un ordinateur et l’importer sur un autre ordinateur, vous devez disposer de deux ordinateurs connectés (via une configuration SAN) à un groupe de stockage qui prend en charge les clichés instantanés de matériel VSS. Un fournisseur de matériel VSS doit être installé sur chaque ordinateur.

L’exemple suivant montre comment créer et importer le cliché instantané.

1.  Créez le jeu de clichés instantanés sur l’ordinateur A (serveur de production) en tapant la commande suivante après l’invite de commandes :

    **vshadow-p-t =bc1.xml**

    Cela n’expose pas les appareils de clichés instantanés sur l’ordinateur A.

2.  Copiez le document des composants de sauvegarde (bc1.xml) de l’ordinateur A vers l’ordinateur B.
3.  Importez le jeu d’ombres sur l’ordinateur B en tapant la commande suivante :

    **vshadow-i =bc1.xml**

Vous pouvez éventuellement exposer ces clichés instantanés en tant que lettres de lecteur ou dossiers montés. En outre, vous pouvez potentiellement rompre le jeu d’ombres pour que les nouveaux volumes de clichés instantanés soient accessibles en lecture-écriture.

Pour automatiser le processus de gestion des jeux de clichés instantanés, vous pouvez utiliser l’option de ligne de commande **-script** pour générer le script cmd contenant les ID de cliché instantané. Ensuite, vous pouvez copier le script généré avec les composants de sauvegarde sur l’autre ordinateur.

L’exemple suivant montre comment créer, exposer et rompre les clichés instantanés transportables à l’aide de scripts CMD.

1.  Créez le jeu de clichés instantanés sur l’ordinateur A (serveur de production) à partir de la ligne de commande comme suit :

    **vshadow-p-t =bc1.xml-script = SC1. cmd**

    Spécifiez l’option **-script** pour générer le script contenant les définitions de variables d’environnement appropriées. Notez que cela n’exposera aucun appareil de clichés instantanés sur l’ordinateur A.

2.  Copiez le document des composants de sauvegarde (bc1.xml) et le script généré (SC1. cmd) de l’ordinateur A vers l’ordinateur B.
3.  Importez le jeu d’ombres sur l’ordinateur B en tapant la commande suivante :

    **vshadow-i =bc1.xml**

    Cela entraînera l’exposition des appareils créés sur l’ordinateur B.

4.  Exécutez le script généré pour définir les variables d’environnement pour le jeu de clichés instantanés en tapant le nom de fichier à l’invite de commandes, comme dans l’exemple suivant :

    **SC1. cmd**

    Cela permet de définir les variables d’environnement appropriées comme décrit dans accéder aux propriétés des clichés instantanés à partir d’un script CMD.

5.  Exposez les clichés instantanés sur l’ordinateur B en tapant les commandes suivantes :
    1.  **rmdir/s c : \\ point de montage \_**
    2.  **mkdir c : \\ point de montage \_**
    3.  **vshadow – El =% VSHADOW \_ ID \_ 1%, c : \\ point de montage \_**

    Les appareils de clichés instantanés créés sont alors exposés sur l’ordinateur B.
6.  Rompez le jeu de clichés instantanés pour rendre les volumes accessibles en écriture en tapant la commande suivante :**C : \\>vshadow – BW =% vshadow \_ Set \_ ID%**

Notez que les clichés instantanés transportables non persistants peuvent également être importés, mais ils sont automatiquement supprimés lorsque le processus **vshadow** **-i** s’arrête. Pour importer les clichés instantanés avant leur suppression, vous devez utiliser l’option de ligne de commande **-Exec** comme décrit dans accéder aux clichés instantanés non persistants.

## <a name="including-writers-or-components"></a>Ajout d’enregistreurs ou de composants

Par défaut, tous les enregistreurs participent à la création de clichés instantanés. Pour déterminer les rédacteurs et les composants qui seront inclus dans un jeu de clichés instantanés, utilisez l’option de ligne de commande **-WM** ou **-wm2** comme décrit dans la section Affichage de l' [État et des métadonnées](vshadow-tool-and-sample.md)de l’enregistreur.

Pour vérifier que tous les composants d’un enregistreur sont inclus, utilisez l’indicateur **-Wi** facultatif dans l’un des formats suivants :

-   **vshadow** **-Wi** *WriterName*
-   **vshadow** **-Wi** **"**_chaîne de nom de l’enregistreur_*_"_*
-   **vshadow** **-Wi** **{**_WriterID_*_}_*
-   **vshadow** **-Wi** **{**_InstanceID_*_}_*

Pour vérifier que des composants spécifiques sont inclus, utilisez l’indicateur **-Wi** facultatif dans l’un des formats suivants :

-   **vshadow** **-Wi** *WriterName ***: \\**_LogicalPath_* _\\_ * _ComponentName_
-   **vshadow** **-Wi** **"**_chaîne de nom de l’enregistreur_*_" : \\_*_LogicalPath_ *_\\_* _ComponentName_
-   **vshadow** **-Wi** **{**_WriterID_*_} : \\_*_LogicalPath_ *_\\_* _ComponentName_
-   **vshadow** **-Wi** **{**_InstanceID_*_} : \\_*_LogicalPath_ *_\\_* _ComponentName_

Les exemples suivants montrent comment utiliser l’indicateur facultatif **-Wi** .

-   Spécification de *WriterName*: \\ *LogicalPath* \\ *ComponentName*:

    **vshadow-Wi = "Registry writer : \\ Registry"**

-   Spécification de {*WriterID*} :

    **vshadow-Wi = {BE000CBE-11FE-4426-9C58-531AA6355FC4}**

-   Spécification de plusieurs rédacteurs ou composants :

    **vshadow-Wi = "Registry writer : \\ Registry"-Wi = "com+ RegDB Writer"**

## <a name="excluding-writers-or-components"></a>Exclusion d’enregistreurs ou de composants

Pour exclure tous les enregistreurs, utilisez l’indicateur **-NW** facultatif lors de la création du cliché instantané.

Pour exclure tous les composants d’un enregistreur, utilisez l’indicateur **-WX** facultatif dans l’un des formats suivants :

-   **vshadow** **-WX** *WriterName*
-   **vshadow** **-WX** **"**_chaîne de nom de l’enregistreur_*_"_*
-   **vshadow** **-WX** **{**_WriterID_*_}_*
-   **vshadow** **-WX** **{**_InstanceID_*_}_*

Pour exclure des composants spécifiques, utilisez l’indicateur **-WX** facultatif dans l’un des formats suivants :

-   **vshadow** **-WX** *WriterName ***: \\**_LogicalPath_* _\\_ * _ComponentName_
-   **vshadow** **-WX** **"**_chaîne de nom de l’enregistreur_*_" : \\_*_LogicalPath_ *_\\_* _ComponentName_
-   **vshadow** **-WX** **{**_WriterID_*_} : \\_*_LogicalPath_ *_\\_* _ComponentName_
-   **vshadow** **-WX** **{**_InstanceID_*_} : \\_*_LogicalPath_ *_\\_* _ComponentName_

Les exemples suivants montrent comment utiliser l’indicateur facultatif **-WX** .

-   Spécification de *WriterName*: \\ *LogicalPath* \\ *ComponentName*:

    **vshadow-WX = "Registry writer : \\ Registry"**

-   Spécification de {*WriterID*} :

    **vshadow-WX = {BE000CBE-11FE-4426-9C58-531AA6355FC4}**

-   Spécification de plusieurs rédacteurs ou composants :

    **vshadow-WX = "Registry writer : \\ Registry"-WX = "com+ RegDB Writer"**

## <a name="breaking-shadow-copy-sets-using-the-breaksnapshotsetex-method"></a>Interruption des jeux de clichés instantanés à l’aide de la méthode BreakSnapshotSetEx

Les exemples suivants montrent comment utiliser l’option de ligne de commande **-Bex** .

-   Spécifiez que le numéro d’unité logique de cliché instantané sera masqué de l’hôte :

    **vshadow** **-Bex** **-Mask**

-   Spécifiez que le numéro d’unité logique de cliché instantané sera exposé à l’hôte en tant que volume en lecture/écriture :

    **vshadow** **-Bex** **-RW**

-   En spécifiant que le numéro d’unité logique de cliché instantané sera exposé à l’hôte en tant que volume en lecture/écriture, et qu’aucune des signatures de disque sur les numéros d’unités logiques de cliché instantané ne sera restaurée à celle des numéros d’unités logiques d’origine :

    **vshadow** **-Bex** **-Revert**

 

 
