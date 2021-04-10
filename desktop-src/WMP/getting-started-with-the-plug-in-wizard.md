---
title: Prise en main à l’aide de l’Assistant de plug-in
description: Prise en main à l’aide de l’Assistant de plug-in
ms.assetid: 77fc1b0c-20f5-434d-9142-f112489a7f08
keywords:
- Plug-ins du lecteur Windows Media, Assistant Installation du plug-in
- plug-ins, installation de l’Assistant de plug-in
- génération de plug-ins, installation de l’Assistant de plug-in
- Assistant de plug-in du lecteur Windows Media, installation
- Assistant Installation du plug-in
- Assistant de plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a4feb9cfa60c120bfc5bb675ea8a8078b95ad14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103940172"
---
# <a name="getting-started-with-the-plug-in-wizard"></a>Prise en main à l’aide de l’Assistant de plug-in

Pour configurer votre environnement de développement pour la création de plug-ins du lecteur Windows Media, vous devez installer les éléments suivants :

-   Microsoft Visual Studio .NET 2003 ou version ultérieure
-   Lecteur Windows Media série 9 ou version ultérieure
-   SDK Windows, qui comprend le kit de développement logiciel (SDK) du lecteur Windows Media
-   Assistant de plug-in du lecteur Windows Media

## <a name="installing-the-wizard"></a>Installation de l’Assistant

Procédez comme suit pour installer l’Assistant de plug-in du lecteur Windows Media.

1.  Localisez le dossier dans lequel vous avez installé le SDK Windows. Développez le dossier pour afficher ses sous-dossiers, puis accédez à exemples d' \\ \\ \\ assistants multimédia WMP \\ wmpwiz.
2.  Recherchez les trois fichiers suivants :
    -   wmpwiz. vsz
    -   wmpwiz. vsdir
    -   wmpwiz. ico
3.  À l’aide d’un éditeur de texte, tel que le bloc-notes, modifiez le fichier wmpwiz. vsz.

    Recherchez la ligne suivante :

    ```
    Wizard=VsWizard.<VsWizardEngine version goes here>
    ```

    

    Modifiez l' `<VsWizardEngine version goes here>` une des valeurs suivantes, en fonction de la version de Visual Studio que vous avez installée.

    

    | Valeur              | Version de Visual Studio   |
    |--------------------|-------------------------|
    | VsWizardEngine. 7.1 | Visual Studio .NET 2003 |
    | VsWizardEngine. 8.0 | Visual Studio 2005      |
    | VsWizardEngine. 9.0 | Visual Studio 2008      |

    

     

    Recherchez la ligne suivante :

    ```
    Param="ABSOLUTE_PATH = <path to wmpwiz directory goes here>"
    ```

    

    Accédez au `<path to wmpwiz directory goes here>` chemin d’accès où se trouvent les fichiers de l’Assistant.

    Supposons, par exemple, que vous disposiez de Visual Studio 2008, et que vos fichiers d’Assistant se trouvent ici : C : \\ Program Files \\ Microsoft SDK \\ Windows \\ v 7.0 \\ Samples \\ Multimedia \\ WMP \\ assistants \\ wmpwiz. Votre fichier wmpwiz. vsz ressemble alors à ceci :

    ```
    VSWIZARD 7.0
    Wizard=VsWizard.VsWizardEngine.9.0

    Param="WIZARD_NAME = Windows Media Player Plug-in Wizard"
    Param="ABSOLUTE_PATH = C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\Multimedia\WMP\wizards\wmpwiz"
    Param="FALLBACK_LCID = 1033"
    ```

    

4.  Localisez le dossier dans lequel vous avez installé Visual Studio. Développez le dossier pour afficher ses sous-dossiers et recherchez un dossier nommé VCProjects.
5.  Copiez les trois fichiers listés à l’étape 2 dans le dossier VCProjects. L’Assistant est maintenant installé.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Génération d’un plug-in](building-a-plug-in.md)
</dt> <dt>

[Utilisation de l’Assistant de plug-in avec Visual Studio](using-the-plug-in-wizard-with-visual-studio.md)
</dt> </dl>

 

 




