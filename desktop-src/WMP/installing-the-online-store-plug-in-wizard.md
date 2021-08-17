---
title: Installation de l’Assistant de plug-in de boutique en ligne
description: Installation de l’Assistant de plug-in de boutique en ligne
ms.assetid: 75f7c279-4800-4146-8198-1dc76472237d
keywords:
- Lecteur Windows Media des magasins en ligne, plug-ins
- magasins en ligne, plug-ins
- types 1 magasins en ligne, plug-ins
- Lecteur Windows Media magasins en ligne, assistant de plug-in
- magasins en ligne, Assistant de plug-in
- tapez 1 magasins en ligne, Assistant de plug-in
- Lecteur Windows Media magasins en ligne, assistant installation du plug-in
- magasins en ligne, Assistant Installation du plug-in
- type 1 magasins en ligne, Assistant Installation du plug-in
- plug-ins, Lecteur Windows Media magasins en ligne
- plug-ins, magasins en ligne
- plug-ins, type 1 magasins en ligne
- plug-ins, installation de l’Assistant de plug-in
- plug-ins, Assistant de plug-in
- Lecteur Windows Media les plug-ins, tapez 1 magasins en ligne
- plug-ins Lecteur Windows Media, magasins en ligne
- plug-ins Lecteur Windows Media, Lecteur Windows Media les magasins en ligne
- plug-ins de Lecteur Windows Media, installation de l’assistant de plug-in
- plug-ins Lecteur Windows Media, assistant de plug-in
- Assistant Installation du plug-in
- Assistant de plug-in
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1088d915715be44de092604d626bc24792f6d263a9765a1076ce1afa3f67ef4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119135542"
---
# <a name="installing-the-online-store-plug-in-wizard"></a>Installation de l’Assistant de plug-in de boutique en ligne

Pour configurer votre environnement de développement afin de créer des plug-ins de magasin en ligne de type 1, vous devez installer les éléments suivants :

-   Microsoft Visual Studio 2005 ou version ultérieure
-   Lecteur Windows Media 11 ou version ultérieure
-   Windows sdk, qui comprend le kit de développement logiciel (sdk) Lecteur Windows Media
-   Assistant de plug-in de magasin en ligne

## <a name="installing-the-wizard"></a>Installation de l’Assistant

Procédez comme suit pour installer l’Assistant de plug-in du magasin en ligne dans Visual Studio.

1.  localisez le dossier dans lequel vous avez installé le SDK Windows. Développez le dossier pour afficher ses sous-dossiers, puis accédez à exemples d' \\ \\ \\ assistants multimédia WMP \\ .
2.  Recherchez les trois fichiers suivants :
    -   wmpservices. vsz
    -   wmpservices. vsdir
    -   wmpservices. ico
3.  à l’aide d’un éditeur de texte tel que Bloc-notes, modifiez le fichier wmpservices. vsz.

    Recherchez la ligne suivante :

    ```
    Wizard=VsWizard.<VsWizardEngine version goes here>
    ```

    

    modifiez `<VsWizardEngine version goes here>` l’une des valeurs suivantes, en fonction de la version de Visual Studio que vous avez installée.

    

    | Valeur              | Version de Visual Studio |
    |--------------------|-----------------------|
    | VsWizardEngine. 8.0 | Visual Studio 2005    |
    | VsWizardEngine. 9.0 | Visual Studio 2008    |

    

     

    Recherchez la ligne suivante :

    ```
    Param="ABSOLUTE_PATH = <path to wmpservices directory goes here>"
    ```

    

    Accédez au `<path to wmpservices directory goes here>` chemin d’accès où se trouvent les fichiers de l’Assistant.

    supposons, par exemple, que vous avez Visual Studio 2008 et que vos fichiers d’assistant se trouvent ici : C : \\ Program files \\ Microsoft sdk \\ Windows \\ v 7.0 \\ exemples \\ Multimedia \\ WMP \\ assistants \\ services. Votre fichier wmpservices. vsz ressemble alors à ceci :

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

 

 




