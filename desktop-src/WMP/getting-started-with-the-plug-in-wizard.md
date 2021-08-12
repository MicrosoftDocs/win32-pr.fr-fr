---
title: Prise en main à l’aide de l’Assistant de plug-in
description: Prise en main à l’aide de l’Assistant de plug-in
ms.assetid: 77fc1b0c-20f5-434d-9142-f112489a7f08
keywords:
- plug-ins de Lecteur Windows Media, installation de l’assistant de plug-in
- plug-ins, installation de l’Assistant de plug-in
- génération de plug-ins, installation de l’Assistant de plug-in
- Lecteur Windows Media Assistant de plug-in, installation
- Assistant Installation du plug-in
- Assistant de plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d2699d0316be93f6387bdc64c6671df868eaa70fb24a4ad3619026524106432
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118576578"
---
# <a name="getting-started-with-the-plug-in-wizard"></a>Prise en main à l’aide de l’Assistant de plug-in

pour configurer votre environnement de développement en vue de créer des plug-ins Lecteur Windows Media, vous devez installer les éléments suivants :

-   Microsoft Visual Studio .net 2003 ou version ultérieure
-   Lecteur Windows Media série 9 ou version ultérieure
-   Windows sdk, qui comprend le kit de développement logiciel (sdk) Lecteur Windows Media
-   Lecteur Windows Media Assistant de plug-in

## <a name="installing-the-wizard"></a>Installation de l’Assistant

procédez comme suit pour installer l’assistant de Plug-in Lecteur Windows Media.

1.  localisez le dossier dans lequel vous avez installé le SDK Windows. Développez le dossier pour afficher ses sous-dossiers, puis accédez à exemples d' \\ \\ \\ assistants multimédia WMP \\ wmpwiz.
2.  Recherchez les trois fichiers suivants :
    -   wmpwiz. vsz
    -   wmpwiz. vsdir
    -   wmpwiz. ico
3.  à l’aide d’un éditeur de texte, tel que Bloc-notes, modifiez le fichier wmpwiz. vsz.

    Recherchez la ligne suivante :

    ```
    Wizard=VsWizard.<VsWizardEngine version goes here>
    ```

    

    modifiez `<VsWizardEngine version goes here>` l’une des valeurs suivantes, en fonction de la version de Visual Studio que vous avez installée.

    

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

    par exemple, supposons que vous avez Visual Studio 2008 et que vos fichiers d’assistant se trouvent ici : C : \\ Program files \\ Microsoft sdk \\ Windows \\ v 7.0 \\ samples \\ Multimedia \\ WMP \\ assistants \\ wmpwiz. Votre fichier wmpwiz. vsz ressemble alors à ceci :

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

 

 




