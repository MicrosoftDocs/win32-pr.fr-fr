---
title: Installation de l’Assistant de plug-in de boutique en ligne
description: Installation de l’Assistant de plug-in de boutique en ligne
ms.assetid: 75f7c279-4800-4146-8198-1dc76472237d
keywords:
- Windows Media Player Online stores, plug-ins
- magasins en ligne, plug-ins
- types 1 magasins en ligne, plug-ins
- Windows Media Player Online stores, Assistant plug-in
- magasins en ligne, Assistant de plug-in
- tapez 1 magasins en ligne, Assistant de plug-in
- Windows Media Player Online stores, Assistant Installation du plug-in
- magasins en ligne, Assistant Installation du plug-in
- type 1 magasins en ligne, Assistant Installation du plug-in
- plug-ins, Windows Media Player Online stores
- plug-ins, magasins en ligne
- plug-ins, type 1 magasins en ligne
- plug-ins, installation de l’Assistant de plug-in
- plug-ins, Assistant de plug-in
- Plug-ins du lecteur Windows Media, type 1 magasins en ligne
- Plug-ins du lecteur Windows Media, magasins en ligne
- Plug-ins du lecteur Windows Media, magasins en ligne Windows Media Player
- Plug-ins du lecteur Windows Media, Assistant Installation du plug-in
- Plug-ins du lecteur Windows Media, Assistant plug-in
- Assistant Installation du plug-in
- Assistant de plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13d236c2160c5783f909430e6b49ef2e6361de22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029325"
---
# <a name="installing-the-online-store-plug-in-wizard"></a>Installation de l’Assistant de plug-in de boutique en ligne

Pour configurer votre environnement de développement afin de créer des plug-ins de magasin en ligne de type 1, vous devez installer les éléments suivants :

-   Microsoft Visual Studio 2005 ou version ultérieure
-   Lecteur Windows Media 11 ou version ultérieure
-   SDK Windows, qui comprend le kit de développement logiciel (SDK) du lecteur Windows Media
-   Assistant de plug-in de magasin en ligne

## <a name="installing-the-wizard"></a>Installation de l’Assistant

Utilisez les étapes suivantes pour installer l’Assistant de plug-in du magasin en ligne dans Visual Studio.

1.  Localisez le dossier dans lequel vous avez installé le SDK Windows. Développez le dossier pour afficher ses sous-dossiers, puis accédez à exemples d' \\ \\ \\ assistants multimédia WMP \\ .
2.  Recherchez les trois fichiers suivants :
    -   wmpservices. vsz
    -   wmpservices. vsdir
    -   wmpservices. ico
3.  À l’aide d’un éditeur de texte tel que le bloc-notes, modifiez le fichier wmpservices. vsz.

    Recherchez la ligne suivante :

    ```
    Wizard=VsWizard.<VsWizardEngine version goes here>
    ```

    

    Modifiez l' `<VsWizardEngine version goes here>` une des valeurs suivantes, en fonction de la version de Visual Studio que vous avez installée.

    

    | Valeur              | Version de Visual Studio |
    |--------------------|-----------------------|
    | VsWizardEngine. 8.0 | Visual Studio 2005    |
    | VsWizardEngine. 9.0 | Visual Studio 2008    |

    

     

    Recherchez la ligne suivante :

    ```
    Param="ABSOLUTE_PATH = <path to wmpservices directory goes here>"
    ```

    

    Accédez au `<path to wmpservices directory goes here>` chemin d’accès où se trouvent les fichiers de l’Assistant.

    Par exemple, supposons que vous disposez de Visual Studio 2008 et que vos fichiers d’Assistant se trouvent ici : C : \\ Program Files \\ Microsoft SDK \\ Windows \\ v 7.0 \\ exemples \\ multimédia \\ WMP \\ assistants \\ services. Votre fichier wmpservices. vsz ressemble alors à ceci :

    ```
    VSWIZARD 7.0
    Wizard=VsWizard.VsWizardEngine.9.0

    Param="WIZARD_NAME = wmpservices"
    Param="ABSOLUTE_PATH = C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\Multimedia\WMP\wizards\services"
    Param="FALLBACK_LCID = 1033"
    ```

    

4.  Localisez le dossier dans lequel vous avez installé Visual Studio. Développez le dossier pour afficher ses sous-dossiers et recherchez un dossier nommé VCProjects.
5.  Copiez les trois fichiers listés à l’étape 2 dans le dossier VCProjects. L’Assistant est maintenant installé.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création du plug-in pour un magasin de type 1 en ligne](building-the-plug-in-for-a-type-1-online-store.md)
</dt> </dl>

 

 




