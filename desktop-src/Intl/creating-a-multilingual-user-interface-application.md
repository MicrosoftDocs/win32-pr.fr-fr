---
description: Ce didacticiel montre comment prendre une application monolingue et la rendre prête pour le monde. Cette application se présente sous la forme d’une solution complète générée dans Microsoft Visual Studio.
ms.assetid: 6d71aa90-8444-4f30-a2f8-f1a2aab015b0
title: ajout de la prise en charge de interface utilisateur multilingue à une Application
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0f5ca1ddba2574610cde1f375f7fab2b07461008665f2092c9c8e88ae9b51f96
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147692"
---
# <a name="adding-multilingual-user-interface-support-to-an-application"></a>ajout de la prise en charge de interface utilisateur multilingue à une Application

Ce didacticiel montre comment prendre une application monolingue et la rendre prête pour le monde. Cette application se présente sous la forme d’une solution complète générée dans Microsoft Visual Studio.

-   [Vue d'ensemble](#splitting-the-various-language-resource-modules-an-overview)
    -   [L’idée derrière le MUI Hello](#the-idea-behind-hello-mui)
-   [Configuration de la solution Hello MUI](#setting-up-the-hello-mui-solution)
    -   [Configuration requise pour la plateforme](#platform-requirements)
    -   [Composants requis](#prerequisites)
-   [Étape 0 : création de l’interface MUI Hello codée en dur](#step-0-creating-the-hard-coded-hello-mui)
-   [Étape 1 : implémentation du module de ressources de base](#step-1-implementing-the-basic-resource-module)
-   [Étape 2 : génération du module de ressources de base](#step-2-building-the-basic-resource-module)
    -   [Fractionnement des différents modules de ressources linguistiques : vue d’ensemble](#splitting-the-various-language-resource-modules-an-overview)
    -   [Fractionnement des différents modules de ressources linguistiques : création des fichiers](#splitting-the-various-language-resource-modules-creating-the-files)
-   [Étape 3 : création d’un Resource-Savvy « Hello MUI »](#step-3-creating-a-resource-savvy-hello-mui)
-   [Étape 4 : globalisation de « Hello MUI »](#step-4-globalizing-hello-mui)
-   [Étape 5 : personnalisation de « Hello MUI »](#step-5-customizing-hello-mui)
-   [Considérations supplémentaires pour MUI](#additional-considerations-for-mui)
    -   [Prise en charge des applications console](#support-for-console-applications)
    -   [Détermination des langues à prendre en charge au moment de l’exécution](#determination-of-languages-to-support-at-run-time)
    -   [prise en charge des scripts complexes dans les Versions antérieures à Windows Vista](#complex-script-support-in-versions-prior-to-windows-vista)
-   [Résumé](#summary)

## <a name="overview"></a>Vue d’ensemble

à partir de Windows Vista, le système d’exploitation Windows lui-même a été créé dès le départ pour être une plateforme multilingue, avec une prise en charge supplémentaire qui vous permet de créer des applications multilingues qui utilisent le modèle de ressource MUI Windows.

Ce didacticiel illustre cette nouvelle prise en charge des applications multilingues en couvrant les aspects suivants :

-   Utilise la prise en charge améliorée de la plateforme MUI pour activer facilement les applications multilingues.
-   étend les applications multilingues pour qu’elles s’exécutent sur des versions de Windows antérieures à Windows Vista.
-   Aborde les considérations supplémentaires impliquées dans le développement d’applications multilingues spécialisées, telles que les applications de console.

Ces liens permettent d’actualiser rapidement les concepts relatifs à l’internationalisation et à l’interface MUI :

-   [Aperçu rapide de l’internationalisation](understanding-internationalization.md).
-   [Concepts MUI](understanding-mui.md).
-   [Utilisation de l’interface MUI pour développer des applications Win32](using-multilingual-user-interface.md).

### <a name="the-idea-behind-hello-mui"></a>L’idée derrière le MUI Hello

Vous êtes probablement familiarisé avec l’application Hello World classique, qui illustre les concepts de programmation de base. Ce didacticiel adopte une approche similaire pour illustrer l’utilisation du modèle de ressources MUI pour mettre à jour une application monolingue afin de créer une version multilingue appelée Hello MUI.

> [!Note]  
> Les tâches de ce didacticiel sont décrites dans les étapes détaillées en raison de la précision avec laquelle ces activités doivent être exécutées et de la nécessité d’expliquer les détails aux développeurs qui ont peu d’expérience avec ces tâches.

 

## <a name="setting-up-the-hello-mui-solution"></a>Configuration de la solution Hello MUI

Ces étapes décrivent comment préparer la création de la solution de l’interface MUI Hello.

### <a name="platform-requirements"></a>Conditions requises par la plateforme

vous devez compiler les exemples de code de ce didacticiel à l’aide du kit de développement logiciel (SDK) Windows pour Windows 7 et Visual Studio 2008. le kit de développement logiciel (SDK) Windows 7 s’installe sur Windows XP, Windows Vista et Windows 7, et l’exemple de solution peut être créé sur l’une de ces versions de système d’exploitation.

tous les exemples de code de ce didacticiel sont conçus pour être exécutés sur des versions x86 et x64 de Windows XP, Windows Vista et Windows 7. les composants spécifiques qui ne fonctionnent pas sur Windows XP sont dénommés, le cas échéant.

### <a name="prerequisites"></a>Prérequis

1.  installez Visual Studio 2008.

    pour plus d’informations, consultez le [centre de développement Visual Studio](https://msdn.microsoft.com/vstudio/default.aspx).

2.  installez le SDK Windows pour Windows 7.

    vous pouvez l’installer à partir de la page SDK Windows du [centre de développement Windows](https://msdn.microsoft.com/windowsserver/bb980924.aspx). le kit de développement logiciel (SDK) comprend des utilitaires permettant de développer des applications pour les versions de système d’exploitation à partir de Windows XP jusqu’au plus récent.

    > [!Note]  
    > Si vous n’installez pas le package à l’emplacement par défaut, ou si vous n’effectuez pas l’installation sur le lecteur système, qui est généralement le lecteur C, notez le chemin d’installation.

     

3.  configurez les paramètres de ligne de commande Visual Studio.

    1.  ouvrez une fenêtre de commande Visual Studio.
    2.  Tapez **set path**.
    3.  vérifiez que la variable path contient le chemin d’accès du dossier bin du kit de développement logiciel (SDK) Windows 7 :... emplacement des kits de développement logiciel (sdk) Microsoft \\ Windows \\ v 7.0 \\

4.  Installez le package du module complémentaire API de niveau inférieur de Microsoft NLS.
    > [!Note]  
    > dans le cadre de ce didacticiel, ce package est nécessaire uniquement si vous souhaitez personnaliser l’application pour qu’elle s’exécute sur des versions de Windows antérieures à Windows Vista. Consultez [étape 5 : personnalisation de Hello MUI](#step-5-customizing-hello-mui).

     

    1.  Téléchargez et installez le package à partir de son [site de téléchargement](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&amp;DisplayLang=en).
    2.  comme pour la SDK Windows, si vous n’installez pas le package à l’emplacement par défaut, ou si vous n’installez pas sur le lecteur système, qui est généralement le lecteur C, notez le chemin d’installation.
    3.  si votre plateforme de développement est Windows XP ou Windows Server 2003, vérifiez que Nlsdl.dll est installé et inscrit correctement.

        1.  Accédez au dossier « Redist » sous l’emplacement du chemin d’installation.
        2.  Exécutez le nlsdl redistribuable approprié. \*.exe, comme nlsdl.x86.exe. Cette étape installe et inscrit Nlsdl.dll.

    > [!Note]  
    > si vous développez une application qui utilise MUI et qui doit s’exécuter sur Windows versions antérieures à Windows Vista, Nlsdl.dll doit être présent sur la plateforme de Windows de destination. Dans la plupart des cas, cela signifie que l’application doit transporter et installer le programme d’installation redistribuable nlsdl (et pas simplement copier Nlsdl.dll lui-même).

     

## <a name="step-0-creating-the-hard-coded-hello-mui"></a>Étape 0 : création de l’interface MUI Hello codée en dur

Ce didacticiel commence par la version monolingue de l’application Hello MUI. L’application suppose l’utilisation du langage de programmation C++, des chaînes de caractères larges et de la fonction [**MessageBoxW**](/windows/win32/api/winuser/nf-winuser-messagebox) pour la sortie.

Commencez par créer l’application GuiStep \_ 0 initiale, ainsi que la solution HelloMUI, qui contient toutes les applications de ce didacticiel.

1.  dans Visual Studio 2008, créez un nouveau projet. Utilisez les paramètres et valeurs suivants :

    1.  Project type : sous Visual C++ sélectionnez win32, puis sous Visual Studio modèles installés, sélectionnez Project win32.
    2.  Nom : GuiStep \_ 0.
    3.  Emplacement : *ProjectRootDirectory* (les étapes ultérieures font référence à ce répertoire).
    4.  Nom de la solution : HelloMUI.
    5.  Sélectionnez Créer le répertoire pour la solution.
    6.  dans l’assistant Application Win32, sélectionnez le type d’application par défaut : Windows application.

2.  Configurez le modèle de thread de projet :

    1.  Dans le Explorateur de solutions, cliquez avec le bouton droit sur le projet GuiStep \_ 0, puis sélectionnez Propriétés.
    2.  Dans la boîte de dialogue pages de propriétés du projet :

        1.  Dans la liste déroulante en haut à gauche, affectez à configuration la valeur toutes les configurations.
        2.  Sous propriétés de configuration, développez C/C++, sélectionnez génération de code, puis définissez bibliothèque Runtime : débogage multithread (/MTd).

3.  Remplacez le contenu de GuiStep \_ 0. cpp par le code suivant :
    ```C++
    // GuiStep_0.cpp : Defines the entry point for the application.
    //

    #include "stdafx.h"
    #include "GuiStep_0.h"

    int WINAPI WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow)
    {
        UNREFERENCED_PARAMETER(hInstance);
        UNREFERENCED_PARAMETER(hPrevInstance);
        UNREFERENCED_PARAMETER(lpCmdLine);
        UNREFERENCED_PARAMETER(nCmdShow);

        MessageBoxW(NULL,L"Hello MUI",L"HelloMUI!",MB_OK | MB_ICONINFORMATION);
        return 0;
    }
    ```

    

4.  Générez et exécutez l’application.

Le code source simple ci-dessus rend le choix de conception simpliste qui consiste à coder en dur, ou incorporer, toute la sortie que l’utilisateur verra, dans ce cas le texte « Hello MUI ». Ce choix limite l’utilitaire de l’application pour les utilisateurs qui ne reconnaissent pas le mot anglais « Hello ». Étant donné que MUI est un acronyme anglais basé sur la technologie, il est supposé pour ce didacticiel que la chaîne reste « MUI » pour toutes les langues.

## <a name="step-1-implementing-the-basic-resource-module"></a>Étape 1 : implémentation du module de ressources de base

Microsoft Win32 a longtemps exposé la possibilité pour les développeurs d’applications de séparer leurs données de ressources d’interface utilisateur du code source de l’application. Cette séparation est fournie sous la forme du modèle de ressource Win32, dans lequel les chaînes, les bitmaps, les icônes, les messages et les autres éléments normalement affichés pour un utilisateur sont empaquetés dans une section distincte de l’exécutable, séparés du code exécutable.

Pour illustrer cette séparation entre le code exécutable et l’empaquetage des données de ressources, dans cette étape, le didacticiel place la chaîne « Hello » précédemment codée en dur (la ressource « en-US ») dans la section des ressources d’un module DLL du projet HelloModule en \_ \_ US.

Cette DLL Win32 peut également contenir des fonctionnalités exécutables de type bibliothèque (comme n’importe quelle autre DLL). Mais pour vous aider à vous concentrer sur les aspects relatifs aux ressources Win32, nous laissons le code de la DLL runtime extrait dans DllMain. cpp. Les sections suivantes de ce didacticiel utilisent les données de ressource HelloModule créées ici et présentent également le code d’exécution approprié.

Pour construire un module de ressources Win32, commencez par créer une DLL avec une fonction DllMain extraite :

1.  Ajoutez un nouveau projet à la solution HelloMUI :

    1.  Dans le menu fichier, sélectionnez Ajouter, puis nouveau Project.
    2.  type de Project : Win32 Project.
    3.  Nom : HelloModule \_ en \_ US.
    4.  Emplacement : *ProjectRootDirectory* \\ HelloMUI.
    5.  Dans l’Assistant application Win32, sélectionnez type d’application : DLL.

2.  Configurez le modèle de thread de ce projet :

    1.  Dans le Explorateur de solutions, cliquez avec le bouton droit sur le projet HelloModule en \_ \_ -US et sélectionnez Propriétés.
    2.  Dans la boîte de dialogue pages de propriétés du projet :

        1.  Dans la liste déroulante en haut à gauche, affectez à configuration la valeur toutes les configurations.
        2.  Sous propriétés de configuration, développez C/C++, sélectionnez génération de code, puis définissez bibliothèque Runtime : débogage multithread (/MTd).

3.  Examinez DllMain. cpp. (Vous pouvez ajouter le non référencé \_ Les macros de paramètre au code généré, comme nous l’avons vu ici, pour permettre la compilation au niveau d’avertissement 4.)
    ```C++
    // dllmain.cpp : Defines the entry point for the DLL application.
    #include "stdafx.h"

    BOOL APIENTRY DllMain( HMODULE hModule,
                           DWORD  ul_reason_for_call,
                           LPVOID lpReserved
                         )
    {
        UNREFERENCED_PARAMETER(hModule);
        UNREFERENCED_PARAMETER(lpReserved);

        switch (ul_reason_for_call)
        {
        case DLL_PROCESS_ATTACH:
        case DLL_THREAD_ATTACH:
        case DLL_THREAD_DETACH:
        case DLL_PROCESS_DETACH:
            break;
        }
        return TRUE;
    }
    ```

    

4.  Ajoutez un fichier de définition de ressource HelloModule. RC au projet :

    1.  Sous le projet HelloModule \_ \_ en US, cliquez avec le bouton droit sur le dossier fichiers de ressources, sélectionnez Ajouter, puis nouvel élément.
    2.  Dans la boîte de dialogue Ajouter un nouvel élément, choisissez ce qui suit :

        1.  catégories : sous Visual C++ sélectionnez ressource, puis sous « modèles installés Visual Studio », sélectionnez fichier de ressources (. rc).
        2.  Nom : HelloModule.
        3.  Emplacement : acceptez la valeur par défaut.
        4.  Cliquez sur Ajouter.

    3.  Spécifiez que le nouveau fichier HelloModule. RC sera enregistré au format Unicode :

        1.  Dans le Explorateur de solutions, cliquez avec le bouton droit sur HelloModule. RC, puis sélectionnez Afficher le code.
        2.  Si vous voyez un message indiquant que le fichier est déjà ouvert, et vous demande si vous voulez le fermer, cliquez sur Oui.
        3.  Avec le fichier affiché sous forme de texte, définissez le fichier de sélection de menu, puis les options d’enregistrement avancées.
        4.  Sous encodage, spécifiez Unicode-CodePage 1200.
        5.  Cliquez sur OK.
        6.  Enregistrez et fermez HelloModule. rc.

    4.  Ajoutez une table de chaînes contenant la chaîne « Hello » :

        1.  Dans le Affichage des ressources, cliquez avec le bouton droit sur HelloModule. RC, puis sélectionnez Ajouter une ressource.
        2.  Sélectionnez table de chaînes.
        3.  Cliquez sur Nouveau.
        4.  Ajoutez une chaîne à la table de chaînes :

            1.  ID : HELLO \_ MUI \_ Str \_ 0.
            2.  Valeur : 0.
            3.  Légende : Bonjour.

        Si vous affichez HelloModule. RC en tant que texte, vous verrez plusieurs éléments de code source spécifiques aux ressources. L’un des plus intéressants est la section qui décrit la chaîne « Hello » :

        ```C++
        /////////////////////////////////////////////////////////////////////////////
        //
        // String Table
        //

        STRINGTABLE 
        BEGIN
            HELLO_MUI_STR_0         "Hello"
        END
        ```

        

        Cette chaîne « Hello » est la ressource qui doit être localisée (traduite) dans chaque langue que l’application espère prendre en charge. Par exemple, le HelloModule \_ ta \_ dans le projet (que vous allez créer à l’étape suivante) contient sa propre version localisée de HelloModule. RC pour « ta » :

        ```C++
        /////////////////////////////////////////////////////////////////////////////
        //
        // String Table
        //

        STRINGTABLE 
        BEGIN
            HELLO_MUI_STR_0         "வணக்கம்"
        END
        ```

        

    5.  Générez le \_ \_ projet HelloModule en US pour vous assurer qu’il n’y a pas d’erreur.

5.  Créez six projets supplémentaires dans la solution HelloMUI (ou autant que vous le souhaitez) pour créer six autres dll de ressources pour d’autres langues. Utilisez les valeurs de ce tableau :

    | Nom du projet        | Nom du fichier. RC | Identificateur de chaîne          | Valeur de chaîne | Légende de la chaîne |
    |---------------------|------------------|--------------------|--------------|----------------|
    | HelloModule \_ de \_ | HelloModule      | HELLO \_ MUI \_ Str \_ 0 | 0            | Hallo          |
    | HelloModule \_ es \_ es | HelloModule      | HELLO \_ MUI \_ Str \_ 0 | 0            | Hola           |
    | HelloModule \_ fr \_ fr | HelloModule      | HELLO \_ MUI \_ Str \_ 0 | 0            | Bonjour        |
    | HelloModule \_ Hi \_ in | HelloModule      | HELLO \_ MUI \_ Str \_ 0 | 0            | नमस्           |
    | Ru \_ ru HelloModule \_ | HelloModule      | HELLO \_ MUI \_ Str \_ 0 | 0            | Здравствуйте   |
    | HelloModule \_ ta \_ dans | HelloModule      | HELLO \_ MUI \_ Str \_ 0 | 0            | வணக்கம்        |

    

     

Pour plus d’informations sur la syntaxe et la structure des fichiers. RC, consultez [à propos des fichiers de ressources](../menurc/about-resource-files.md).

## <a name="step-2-building-the-basic-resource-module"></a>Étape 2 : génération du module de ressources de base

En utilisant les modèles de ressource précédents, la génération de l’un des sept projets HelloModule entraînerait la création de sept dll distinctes. Chaque DLL contient une section de ressource avec une chaîne unique localisée dans la langue appropriée. Bien qu’il soit approprié pour le modèle de ressource Win32 historique, cette conception ne tire pas parti de MUI.

dans le kit de développement logiciel (SDK) Windows Vista et versions ultérieures, MUI offre la possibilité de fractionner les exécutables dans le code source et les modules de contenu localisables. avec la personnalisation supplémentaire qui est décrite plus loin à l’étape 5, les applications peuvent être activées pour que la prise en charge multilingue s’exécute sur les versions antérieures à Windows Vista.

les mécanismes principaux disponibles pour fractionner les ressources du code exécutable, en commençant par Windows Vista, sont les suivants :

-   À l’aide de rc.exe (compilateur RC) avec des commutateurs spécifiques, ou
-   À l’aide d’un outil de fractionnement de style après génération nommé muirct.exe.

Pour plus d’informations, consultez [utilitaires de ressource](resource-utilities.md) .

Par souci de simplicité, ce didacticiel utilise muirct.exe pour fractionner l’exécutable « Hello MUI ».

### <a name="splitting-the-various-language-resource-modules-an-overview"></a>Fractionnement des différents modules de ressources linguistiques : vue d’ensemble

Un processus en plusieurs parties est impliqué dans le fractionnement des dll en un HelloModule.dll exécutable, ainsi qu’un HelloModule.dll. mui pour chacune des sept langues prises en charge dans ce didacticiel. Cette vue d’ensemble décrit les étapes requises. la section suivante présente un fichier de commandes qui effectue ces étapes.

Tout d’abord, fractionnez le module HelloModule.dll en anglais uniquement à l’aide de la commande :


```C++
mkdir .\en-US
muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0409 -g 0x0407 .\HelloModule_en_us.dll .\HelloModule.dll .\en-US\HelloModule.dll.mui
```



La ligne de commande ci-dessus utilise le fichier de configuration DoReverseMuiLoc. rcconfig. Ce type de fichier de configuration est généralement utilisé par muirct.exe pour fractionner les ressources entre la DLL indépendante de la langue et les fichiers. mui dépendants de la langue. Dans ce cas, le fichier XML DoReverseMuiLoc. rcconfig (répertorié dans la section suivante) indique de nombreux types de ressources, mais ils sont tous classés dans la catégorie de fichier « localizedResources » ou. mui, et il n’y a aucune ressource dans la catégorie indépendante de la langue. Pour plus d’informations sur la préparation d’un fichier de configuration de ressources, consultez [préparation d’un fichier de configuration de ressource](preparing-a-resource-configuration-file.md).

En plus de créer un fichier HelloModule.dll. mui qui contient la chaîne anglaise « Hello », muirct.exe incorpore également une ressource MUI dans le module HelloModule.dll pendant le fractionnement. Afin de charger correctement au moment de l’exécution les ressources appropriées à partir des modules HelloModule.dll. mui spécifiques à une langue, les sommes de contrôle de chaque fichier. mui doivent être fixes pour correspondre aux sommes de contrôle du module de base-Neutral language-Neutral. Cette opération s’effectue à l’aide d’une commande telle que :


```C++
muirct.exe -c HelloModule.dll -e en-US\HelloModule.dll.mui
```



De même, muirct.exe est appelé pour créer un fichier HelloModule.dll. mui pour chacun des autres langages. Toutefois, dans ce cas, la DLL indépendante du langage est ignorée, car seule la première créée est nécessaire. Les commandes qui traitent les ressources espagnoles et françaises se présentent comme suit :


```C++
mkdir .\es-ES
muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0C0A -g 0x0407 .\HelloModule_es_es.dll .\HelloModule_discard.dll .\es-ES\HelloModule.dll.mui
muirct.exe -c HelloModule.dll -e es-ES\HelloModule.dll.mui

mkdir .\fr-FR
muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x040C -g 0x0407 .\HelloModule_fr_fr.dll .\HelloModule_discard.dll .\fr-FR\HelloModule.dll.mui
muirct.exe -c HelloModule.dll -e fr-FR\HelloModule.dll.mui
```



L’un des éléments les plus importants à noter dans les lignes de commande muirct.exe ci-dessus est que l’indicateur-x est utilisé pour spécifier un ID de langue cible. La valeur fournie à muirct.exe est différente pour chaque module HelloModule.dll spécifique à une langue. Cette valeur de langue est centrale et est utilisée par muirct.exe pour marquer de manière appropriée le fichier. mui durant le fractionnement. Une valeur incorrecte génère des échecs de chargement des ressources pour ce fichier. mui particulier au moment de l’exécution. Pour plus d’informations sur le mappage du nom de langage à LCID [, consultez constantes et chaînes](language-identifier-constants-and-strings.md) de l’identificateur de langue.

Chaque fichier. mui Split finit par être placé dans un répertoire correspondant à son nom de langue, immédiatement sous le répertoire dans lequel les HelloModule.dll indépendantes de la langue se trouvent. Pour plus d’informations sur l’emplacement des fichiers. mui, consultez [déploiement d’applications](application-deployment.md).

### <a name="splitting-the-various-language-resource-modules-creating-the-files"></a>Fractionnement des différents modules de ressources linguistiques : création des fichiers

Pour ce didacticiel, vous créez un fichier de commandes contenant les commandes pour fractionner les différentes dll et vous l’appelez manuellement. Notez que dans le cadre du travail de développement réel, vous pouvez réduire le risque d’erreurs de génération en incluant ces commandes en tant qu’événements pré-build ou après génération dans la solution HelloMUI, mais cela n’entre pas dans le cadre de ce didacticiel.

Créez les fichiers pour la version Debug :

1.  Créez un fichier de commandes DoReverseMuiLoc. cmd contenant les commandes suivantes :
    ```C++
    mkdir .\en-US
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0409 -g 0x0407 .\HelloModule_en_us.dll .\HelloModule.dll .\en-US\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e en-US\HelloModule.dll.mui

    mkdir .\de-DE
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0407 -g 0x0407 .\HelloModule_de_de.dll .\HelloModule_discard.dll .\de-DE\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e de-DE\HelloModule.dll.mui

    mkdir .\es-ES
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0C0A -g 0x0407 .\HelloModule_es_es.dll .\HelloModule_discard.dll .\es-ES\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e es-ES\HelloModule.dll.mui

    mkdir .\fr-FR
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x040C -g 0x0407 .\HelloModule_fr_fr.dll .\HelloModule_discard.dll .\fr-FR\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e fr-FR\HelloModule.dll.mui

    mkdir .\hi-IN
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0439 -g 0x0407 .\HelloModule_hi_in.dll .\HelloModule_discard.dll .\hi-IN\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e hi-IN\HelloModule.dll.mui

    mkdir .\ru-RU
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0419 -g 0x0407 .\HelloModule_ru_ru.dll .\HelloModule_discard.dll .\ru-RU\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e ru-RU\HelloModule.dll.mui

    mkdir .\ta-IN
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0449 -g 0x0407 .\HelloModule_ta_in.dll .\HelloModule_discard.dll .\ta-IN\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e ta-IN\HelloModule.dll.mui
    pause
    ```

    

2.  Créez un fichier XML DoReverseMuiLoc. rcconfig contenant les lignes suivantes :
    ```C++
    <?xml version="1.0" encoding="utf-8"?>
        <localization>
            <resources>
                <win32Resources fileType="Application">
                    <neutralResources>
                    </neutralResources>
                    <localizedResources>
                        <resourceType typeNameId="#1"/>
                        <resourceType typeNameId="#10"/>
                        <resourceType typeNameId="#1024"/>
                        <resourceType typeNameId="#11"/>
                        <resourceType typeNameId="#12"/>
                        <resourceType typeNameId="#13"/>
                        <resourceType typeNameId="#14"/>
                        <resourceType typeNameId="#15"/>
                        <resourceType typeNameId="#16"/>
                        <resourceType typeNameId="#17"/>
                        <resourceType typeNameId="#18"/>
                        <resourceType typeNameId="#19"/>
                        <resourceType typeNameId="#2"/>
                        <resourceType typeNameId="#20"/>
                        <resourceType typeNameId="#2110"/>
                        <resourceType typeNameId="#23"/>
                        <resourceType typeNameId="#240"/>
                        <resourceType typeNameId="#3"/>
                        <resourceType typeNameId="#4"/>
                        <resourceType typeNameId="#5"/>
                        <resourceType typeNameId="#6"/>
                        <resourceType typeNameId="#7"/>
                        <resourceType typeNameId="#8"/>
                        <resourceType typeNameId="#9"/>
                        <resourceType typeNameId="HTML"/>
                        <resourceType typeNameId="MOFDATA"/>
                    </localizedResources>
                </win32Resources>
            </resources>
        </localization>
    ```

    

3.  Copiez DoReverseMuiLoc. cmd et DoReverseMuiLoc. rcconfig sur *ProjectRootDirectory* \\ HelloMUI \\ Debug.
4.  ouvrez l’invite de commandes Visual Studio 2008 et accédez au répertoire de débogage.
5.  Exécutez DoReverseMuiLoc. cmd.

Lorsque vous créez une version Release, vous copiez les mêmes fichiers DoReverseMuiLoc. cmd et DoReverseMuiLoc. rcconfig dans le répertoire de mise en version, puis vous exécutez le fichier de commandes.

## <a name="step-3-creating-a-resource-savvy-hello-mui"></a>Étape 3 : création d’un Resource-Savvy « Hello MUI »

En s’appuyant sur le0.exe GuiStep initial codé en dur \_ de l’exemple ci-dessus, vous pouviez étendre la portée de l’application à plusieurs utilisateurs de langage en choisissant d’incorporer le modèle de ressource Win32. Le nouveau code d’exécution présenté dans cette étape comprend la logique de chargement de module ([**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa)) et de récupération de chaîne ([**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa)).

1.  ajoutez un nouveau projet à la solution HelloMUI (en utilisant le fichier de sélection de menu, ajoutez et nouveau Project) avec les paramètres et valeurs suivants :

    1.  type de Project : Win32 Project.
    2.  Nom : GuiStep \_ 1.
    3.  Emplacement : acceptez la valeur par défaut.
    4.  dans l’assistant Application Win32, sélectionnez le type d’application par défaut : Windows application.

2.  définissez ce projet pour qu’il s’exécute à partir de Visual Studio et configurez son modèle de thread :

    1.  Dans le Explorateur de solutions, cliquez avec le bouton droit sur le projet GuiStep \_ 1, puis sélectionnez Définir comme Project de démarrage.
    2.  Cliquez à nouveau avec le bouton droit et sélectionnez Propriétés.
    3.  Dans la boîte de dialogue pages de propriétés du projet :

        1.  Dans la liste déroulante en haut à gauche, affectez à configuration la valeur toutes les configurations.
        2.  Sous propriétés de configuration, développez C/C++, sélectionnez génération de code, puis définissez bibliothèque Runtime : débogage multithread (/MTd).

3.  Remplacez le contenu de GuiStep \_ 1. cpp par le code suivant :
    ```C++
    // GuiStep_1.cpp : Defines the entry point for the application.
    //

    #include "stdafx.h"
    #include "GuiStep_1.h"
    #include "..\HelloModule_en_us\resource.h"

    #define SUFFICIENTLY_LARGE_STRING_BUFFER (MAX_PATH*2)
    #define SUFFICIENTLY_LARGE_ERROR_BUFFER (1024*2)
    #define HELLO_MODULE_CONTRIVED_FILE_PATH  (L"HelloModule.dll")

    int WINAPI WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow)
    {
        UNREFERENCED_PARAMETER(hInstance);
        UNREFERENCED_PARAMETER(hPrevInstance);
        UNREFERENCED_PARAMETER(lpCmdLine);
        UNREFERENCED_PARAMETER(nCmdShow);

        // The following code presents a hypothetical, yet common use pattern of MUI technology
        WCHAR displayBuffer[SUFFICIENTLY_LARGE_ERROR_BUFFER];

        // 1. Basic application obtains access to the proper resource container 
        // for standard Win32 resource loading this is normally a PE module - use LoadLibraryEx
        // LoadLibraryEx is the preferred alternative for resource modules as used below because it
        // provides increased security and performance over that of LoadLibrary
        HMODULE resContainer = LoadLibraryExW(HELLO_MODULE_CONTRIVED_FILE_PATH,NULL,LOAD_LIBRARY_AS_IMAGE_RESOURCE | LOAD_LIBRARY_AS_DATAFILE);
        if(!resContainer)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource container module, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        // 2. Application parses the resource container to find the appropriate item
        WCHAR szHello[SUFFICIENTLY_LARGE_STRING_BUFFER];
        if(LoadStringW(resContainer,HELLO_MUI_STR_0,szHello,SUFFICIENTLY_LARGE_STRING_BUFFER) == 0)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            FreeLibrary(resContainer);
            return 1; // exit
        }

        // 3. Application presents the discovered resource to the user via UI
        swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"%s MUI",szHello);
        MessageBoxW(NULL,displayBuffer,L"HelloMUI",MB_OK | MB_ICONINFORMATION);

        // 4. Application cleans up memory associated with the resource container after this item is no longer needed.
        if(!FreeLibrary(resContainer))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to unload the resource container, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        return 0;
    }
    ```

    

4.  Générez et exécutez l’application. La sortie s’affiche dans la langue actuellement définie en tant que langue d’affichage de l’ordinateur (à condition qu’il s’agit de l’une des sept langues que nous avons générées).

## <a name="step-4-globalizing-hello-mui"></a>Étape 4 : globalisation de « Hello MUI »

Bien que l’exemple précédent soit en mesure d’afficher sa sortie dans différentes langues, il est très petit dans plusieurs domaines. le plus notable est peut-être que l’application n’est disponible que dans un petit sous-ensemble de langues par rapport au système d’exploitation Windows lui-même. si, par exemple, l' \_ application GuiStep 1 de l’étape précédente ont été installées sur une version japonaise de Windows, les échecs d’emplacement de ressource sont probablement possibles.

Pour résoudre ce problème, vous avez deux options principales :

-   Assurez-vous que les ressources d’un langage de secours ultime prédéterminé sont incluses.
-   Permet à l’utilisateur final de configurer ses préférences linguistiques parmi le sous-ensemble de langues spécifiquement pris en charge par l’application.

Parmi ces options, celle qui fournit un langage de secours ultime est très recommandée et est implémentée dans ce didacticiel en passant l’indicateur-g à muirct.exe, comme indiqué ci-dessus. Cet indicateur indique muirct.exe d’effectuer une langue spécifique (de-0x0407) pour le langage de secours ultime associé au module dll indépendant du langage (HelloModule.dll). Au moment de l’exécution, ce paramètre est utilisé en dernier recours pour générer du texte à afficher à l’utilisateur. Dans le cas où un langage de secours ultime est introuvable et qu’aucune ressource appropriée n’est disponible dans le fichier binaire indépendant de la langue, le chargement de la ressource échoue. Par conséquent, vous devez déterminer avec soin les scénarios que votre application peut rencontrer et planifier le langage de secours ultime en conséquence.

L’autre option qui consiste à autoriser les préférences linguistiques configurables et à charger des ressources basées sur cette hiérarchie définie par l’utilisateur peut augmenter la satisfaction des clients. Malheureusement, cela complique également les fonctionnalités nécessaires au sein de l’application.

Cette étape du didacticiel utilise un mécanisme de fichier texte simplifié pour activer la configuration linguistique personnalisée de l’utilisateur. Le fichier texte est analysé au moment de l’exécution par l’application, et la liste des langues analysées et validées est utilisée pour établir une liste de secours personnalisée. une fois la liste de secours personnalisée établie, les api Windows chargent les ressources en fonction de la priorité de langue définie dans cette liste. Le reste du code est similaire à celui trouvé à l’étape précédente.

1.  ajoutez un nouveau projet à la solution HelloMUI (en utilisant le fichier de sélection de menu, ajoutez et nouveau Project) avec les paramètres et valeurs suivants :

    1.  type de Project : Win32 Project.
    2.  Nom : GuiStep \_ 2.
    3.  Emplacement : acceptez la valeur par défaut.
    4.  dans l’assistant Application Win32, sélectionnez le type d’application par défaut : Windows application.

2.  définissez ce projet pour qu’il s’exécute à partir de Visual Studio et configurez son modèle de thread :

    1.  Dans le Explorateur de solutions, cliquez avec le bouton droit sur le projet GuiStep \_ 2 et sélectionnez Définir comme Project de démarrage.
    2.  Cliquez à nouveau avec le bouton droit et sélectionnez Propriétés.
    3.  Dans la boîte de dialogue pages de propriétés du projet :

        1.  Dans la liste déroulante en haut à gauche, affectez à configuration la valeur toutes les configurations.
        2.  Sous propriétés de configuration, développez C/C++, sélectionnez génération de code, puis définissez bibliothèque Runtime : débogage multithread (/MTd).

3.  Remplacez le contenu de GuiStep \_ 2. cpp par le code suivant :
    ```C++
    // GuiStep_2.cpp : Defines the entry point for the application.
    //

    #include "stdafx.h"
    #include "GuiStep_2.h"
    #include <strsafe.h>
    #include "..\HelloModule_en_us\resource.h"

    #define SUFFICIENTLY_LARGE_STRING_BUFFER (MAX_PATH*2)
    #define USER_CONFIGURATION_STRING_BUFFER (((LOCALE_NAME_MAX_LENGTH+1)*5)+1)
    #define SUFFICIENTLY_LARGE_ERROR_BUFFER (1024*2)
    #define HELLO_MODULE_CONTRIVED_FILE_PATH  (L"HelloModule.dll")

    BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize);
    BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize);

    int WINAPI WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow)
    {
        UNREFERENCED_PARAMETER(hInstance);
        UNREFERENCED_PARAMETER(hPrevInstance);
        UNREFERENCED_PARAMETER(lpCmdLine);
        UNREFERENCED_PARAMETER(nCmdShow);

        // The following code presents a hypothetical, yet common use pattern of MUI technology
        WCHAR displayBuffer[SUFFICIENTLY_LARGE_ERROR_BUFFER];

        // 1. Application starts by applying any user defined language preferences
        // (language setting is potentially optional for an application that wishes to strictly use OS system language fallback)
        // 1a. Application looks in pre-defined location for user preferences (registry, file, web, etc.)
        WCHAR userLanguagesString[USER_CONFIGURATION_STRING_BUFFER*2];
        if(!GetMyUserDefinedLanguages(userLanguagesString,USER_CONFIGURATION_STRING_BUFFER*2))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to find the user defined language configuration, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // 1b. Application converts the user defined 'readable' languages to the proper multi-string 'less readable' language name format
        WCHAR userLanguagesMultiString[USER_CONFIGURATION_STRING_BUFFER];
        if(!ConvertMyLangStrToMultiLangStr(userLanguagesString,userLanguagesMultiString,USER_CONFIGURATION_STRING_BUFFER))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to convert the user defined language configuration to multi-string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // 1c. Application now sets the appropriate fallback list
        DWORD langCount = 0;
        // next commented out line of code could be used on Windows 7 and later
        // using SetProcessPreferredUILanguages is recomended for new applications (esp. multi-threaded applications)
    //    if(!SetProcessPreferredUILanguages(MUI_LANGUAGE_NAME,userLanguagesMultiString,&langCount) || langCount == 0)
        // the following line of code is supported on Windows Vista and later
        if(!SetThreadPreferredUILanguages(MUI_LANGUAGE_NAME,userLanguagesMultiString,&langCount) || langCount == 0)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to set the user defined languages, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // NOTES on step #1:
        // an application developer that makes the assumption the fallback list provided by the
        // system / OS is entirely sufficient may or may not be making a good assumption based 
        // mostly on:
        // A. your choice of languages installed with your application
        // B. the languages on the OS at application install time
        // C. the OS users propensity to install/uninstall language packs
        // D. the OS users propensity to change laguage settings

        // 2. Application obtains access to the proper resource container 
        // for standard Win32 resource loading this is normally a PE module - use LoadLibraryEx
        // LoadLibraryEx is the preferred alternative for resource modules as used below because it
        // provides increased security and performance over that of LoadLibrary
        HMODULE resContainer = LoadLibraryExW(HELLO_MODULE_CONTRIVED_FILE_PATH,NULL,LOAD_LIBRARY_AS_IMAGE_RESOURCE | LOAD_LIBRARY_AS_DATAFILE);
        if(!resContainer)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource container module, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        // 3. Application parses the resource container to find the appropriate item
        WCHAR szHello[SUFFICIENTLY_LARGE_STRING_BUFFER];
        if(LoadStringW(resContainer,HELLO_MUI_STR_0,szHello,SUFFICIENTLY_LARGE_STRING_BUFFER) == 0)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            FreeLibrary(resContainer);
            return 1; // exit
        }

        // 4. Application presents the discovered resource to the user via UI
        swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"%s MUI",szHello);
        MessageBoxW(NULL,displayBuffer,L"HelloMUI",MB_OK | MB_ICONINFORMATION);

        // 5. Application cleans up memory associated with the resource container after this item is no longer needed.
        if(!FreeLibrary(resContainer))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to unload the resource container, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        return 0;
    }

    BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize)
    {
        BOOL rtnVal = FALSE;
        // very simple implementation - assumes that first 'langStrSize' characters of the 
        // L".\\langs.txt" file comprises a string of one or more languages
        HANDLE langConfigFileHandle = CreateFileW(L".\\langs.txt", GENERIC_READ, 0, 
            NULL, OPEN_EXISTING, FILE_ATTRIBUTE_NORMAL, NULL);
        if(langConfigFileHandle != INVALID_HANDLE_VALUE)
        {
            // clear out the input variables
            DWORD bytesActuallyRead = 0;
            if(ReadFile(langConfigFileHandle,langStr,langStrSize*sizeof(WCHAR),&bytesActuallyRead,NULL) && bytesActuallyRead > 0)
            {
                rtnVal = TRUE;
                DWORD nullIndex = (bytesActuallyRead/sizeof(WCHAR) < langStrSize) ? bytesActuallyRead/sizeof(WCHAR) : langStrSize;
                langStr[nullIndex] = L'\0';
            }
            CloseHandle(langConfigFileHandle);
        }
        return rtnVal;
    }
    BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize)
    {
        BOOL rtnVal = FALSE;
        size_t strLen = 0;
        rtnVal = SUCCEEDED(StringCchLengthW(langStr,USER_CONFIGURATION_STRING_BUFFER*2,&strLen));
        if(rtnVal && strLen > 0 && langMultiStr && langMultiStrSize > 0)
        {
            WCHAR * langMultiStrPtr = langMultiStr;
            WCHAR * last = langStr + (langStr[0] == 0xFEFF ? 1 : 0);
            WCHAR * context = last;
            WCHAR * next = wcstok_s(last,L",; :",&context);
            while(next && rtnVal)
            {
                // make sure you validate the user input
                if(SUCCEEDED(StringCchLengthW(last,LOCALE_NAME_MAX_LENGTH,&strLen)) && 
                    IsValidLocaleName(next))
                {
                    langMultiStrPtr[0] = L'\0';
                    rtnVal &= SUCCEEDED(StringCchCatW(langMultiStrPtr,(langMultiStrSize - (langMultiStrPtr - langMultiStr)),next));
                    langMultiStrPtr += strLen + 1;
                }
                next = wcstok_s(NULL,L",; :",&context);
                if(next)
                    last = next;
            }
            if(rtnVal && (langMultiStrSize - (langMultiStrPtr - langMultiStr))) // make sure there is a double null term for the multi-string
            {
                langMultiStrPtr[0] = L'\0';
            }
            else // fail and guard anyone whom might use the multi-string
            {
                langMultiStr[0] = L'\0';
                langMultiStr[1] = L'\0';
            }
        }
        return rtnVal;
    }
    ```

    

4.  Créez un fichier texte Unicode langs.txt contenant la ligne suivante :

    ``` syntax
    hi-IN ta-IN ru-RU fr-FR es-ES en-US
    ```

    > [!Note]  
    > Veillez à enregistrer le fichier au format Unicode.

     

    Copiez langs.txt dans le répertoire à partir duquel le programme s’exécutera :

    -   si vous exécutez à partir de Visual Studio, copiez-le dans *ProjectRootDirectory* \\ HelloMUI \\ GuiStep \_ 2.
    -   si vous exécutez à partir de Windows Explorer, copiez-le dans le même répertoire que GuiStep \_2.exe.

5.  Générez et exécutez le projet. Essayez de modifier langs.txt pour que différentes langues s’affichent au début de la liste.

## <a name="step-5-customizing-hello-mui"></a>Étape 5 : personnalisation de « Hello MUI »

un certain nombre de fonctionnalités d’exécution mentionnées jusqu’à présent dans ce didacticiel sont disponibles uniquement sur Windows Vista et versions ultérieures. vous souhaiterez peut-être réutiliser les efforts investis dans la localisation et le fractionnement des ressources en rendant l’application opérationnelle sur les versions de système d’exploitation de bas niveau Windows, comme Windows XP. Ce processus implique l’ajustement de l’exemple précédent dans deux domaines clés :

-   les fonctions de chargement des ressources de préWindows Vista (telles que [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa), [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona), [**LoadBitmap**](/windows/win32/api/winuser/nf-winuser-loadbitmapa), [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage), etc.) ne prennent pas en charge l’interface MUI. Les applications qui sont livrées avec des ressources fractionnées (fichiers LN et. MUI) doivent charger les modules de ressources à l’aide de l’une des deux fonctions suivantes :

    -   si l’application doit être exécutée uniquement sur Windows Vista et versions ultérieures, elle doit charger les modules de ressources avec [**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa).
    -   si l’application doit être exécutée sur des versions antérieures à Windows vista, ainsi que Windows vista ou version ultérieure, elle doit utiliser [**LoadMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya), qui est une fonction de niveau inférieur spécifique fournie dans le kit de développement logiciel (SDK) Windows 7.

-   la prise en charge de l’ordre de gestion linguistique et de la langue de secours dans les versions antérieures Windows vista du système d’exploitation Windows diffère considérablement de celle de Windows vista et versions ultérieures. Pour cette raison, les applications qui autorisent la langue de secours configurée par l’utilisateur doivent ajuster les pratiques de gestion de la langue :

    -   si l’application doit être exécutée uniquement sur Windows Vista et versions ultérieures, la définition de la liste de langues à l’aide de [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) est suffisante.
    -   si l’application doit être exécutée sur toutes les versions de Windows, du code doit être construit pour s’exécuter sur les plateformes de niveau inférieur pour itérer au sein de la liste des langues configurées par l’utilisateur et détecter le module de ressources souhaité. Cela peut être observé dans les sections 1C et 2 du code fourni plus loin dans cette étape.

Créez un projet qui peut utiliser les modules de ressources localisés sur n’importe quelle version de Windows :

1.  ajoutez un nouveau projet à la solution HelloMUI (en utilisant le fichier de sélection de menu, ajoutez et nouveau Project) avec les paramètres et valeurs suivants :

    1.  type de Project : Win32 Project.
    2.  Nom : GuiStep \_ 3.
    3.  Emplacement : acceptez la valeur par défaut.
    4.  dans l’assistant Application Win32, sélectionnez le type d’application par défaut : Windows application.

2.  définissez ce projet pour qu’il s’exécute à partir de Visual Studio et configurez son modèle de thread. En outre, configurez-le pour ajouter les en-têtes et les bibliothèques nécessaires.

    > [!Note]  
    > les chemins d’accès utilisés dans ce didacticiel supposent que le kit de développement logiciel (SDK) Windows 7 et le package des api de niveau inférieur de Microsoft NLS ont été installés dans leurs répertoires par défaut. Si ce n’est pas le cas, modifiez les chemins d’accès de manière appropriée.

     

    1.  Dans le Explorateur de solutions, cliquez avec le bouton droit sur le projet GuiStep \_ 3 et sélectionnez Définir comme Project de démarrage.
    2.  Cliquez à nouveau avec le bouton droit et sélectionnez Propriétés.
    3.  Dans la boîte de dialogue pages de propriétés du projet :

        1.  Dans la liste déroulante en haut à gauche, affectez à configuration la valeur toutes les configurations.
        2.  Sous propriétés de configuration, développez C/C++, sélectionnez génération de code, puis définissez bibliothèque Runtime : débogage multithread (/MTd).
        3.  Sélectionnez général et ajouter aux autres répertoires Include :

            -   « C : \\ API de niveau inférieur de Microsoft nls \\ include ».

        4.  Sélectionnez langage et Set traiter WCHAR \_ t comme type intégré : non (/Zc : WCHAR \_ t-).
        5.  Sélectionnez avancé et définissez Convention d’appel : \_ StdCall (/GZ).
        6.  Sous propriétés de configuration, développez éditeur de liens, sélectionnez entrée, puis ajoutez à des dépendances supplémentaires :

            -   « C : \\ Program Files \\ Microsoft sdk \\ Windows \\ v 7.0 \\ Lib \\ MUILoad. lib ».
            -   « C : \\ API de niveau inférieur Microsoft nls \\ lib \\ x86 \\ nlsdl. lib ».

3.  Remplacez le contenu de GuiStep \_ 3. cpp par le code suivant :
    ```C++
    // GuiStep_3.cpp : Defines the entry point for the application.
    //

    #include "stdafx.h"
    #include "GuiStep_3.h"
    #include <strsafe.h>
    #include <Nlsdl.h>
    #include <MUILoad.h>
    #include "..\HelloModule_en_us\resource.h"

    #define SUFFICIENTLY_LARGE_STRING_BUFFER (MAX_PATH*2)
    #define USER_CONFIGURATION_STRING_BUFFER (((LOCALE_NAME_MAX_LENGTH+1)*5)+1)
    #define SUFFICIENTLY_LARGE_ERROR_BUFFER (1024*2)
    #define HELLO_MODULE_CONTRIVED_FILE_PATH  (L"HelloModule.dll")

    BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize);
    BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize);

    int WINAPI WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow)
    {
        UNREFERENCED_PARAMETER(hInstance);
        UNREFERENCED_PARAMETER(hPrevInstance);
        UNREFERENCED_PARAMETER(lpCmdLine);
        UNREFERENCED_PARAMETER(nCmdShow);

        // The following code presents a hypothetical, yet common use pattern of MUI technology
        WCHAR displayBuffer[SUFFICIENTLY_LARGE_ERROR_BUFFER];

        // 1. Application starts by applying any user defined language preferences
        // (language setting is potentially optional for an application that wishes to strictly use OS system language fallback)
        // 1a. Application looks in pre-defined location for user preferences (registry, file, web, etc.)
        WCHAR userLanguagesString[USER_CONFIGURATION_STRING_BUFFER*2];
        if(!GetMyUserDefinedLanguages(userLanguagesString,USER_CONFIGURATION_STRING_BUFFER*2))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to find the user defined language configuration, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // 1b. Application converts the user defined 'readable' languages to the proper multi-string 'less readable' language name format
        WCHAR userLanguagesMultiString[USER_CONFIGURATION_STRING_BUFFER];
        if(!ConvertMyLangStrToMultiLangStr(userLanguagesString,userLanguagesMultiString,USER_CONFIGURATION_STRING_BUFFER))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to convert the user defined language configuration to multi-string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // 1c. Application now attempts to set the fallback list - this is much different for a down-level 
        // shipping application when compared to a Windows Vista or Windows 7 only shipping application    
        BOOL setSuccess = FALSE;
        DWORD setLangCount = 0;
        HMODULE hDLL = GetModuleHandleW(L"kernel32.dll");
        if( hDLL )
        {
            typedef BOOL (* SET_PREFERRED_UI_LANGUAGES_PROTOTYPE ) ( DWORD, PCWSTR, PULONG );
            SET_PREFERRED_UI_LANGUAGES_PROTOTYPE fp_SetPreferredUILanguages = (SET_PREFERRED_UI_LANGUAGES_PROTOTYPE)NULL;
            fp_SetPreferredUILanguages = (SET_PREFERRED_UI_LANGUAGES_PROTOTYPE) GetProcAddress(hDLL,"SetProcessPreferredUILanguages");
            if( fp_SetPreferredUILanguages )
            {
                // call SetProcessPreferredUILanguages if it is available in Kernel32.dll's export table - Windows 7 and later
                setSuccess = fp_SetPreferredUILanguages(MUI_LANGUAGE_NAME,userLanguagesMultiString,&setLangCount);
            }
            else
            {
                fp_SetPreferredUILanguages = (SET_PREFERRED_UI_LANGUAGES_PROTOTYPE) GetProcAddress(hDLL,"SetThreadPreferredUILanguages");
                // call SetThreadPreferredUILanguages if it is available in Kernel32.dll's export table - Windows Vista and later
                if(fp_SetPreferredUILanguages)
                    setSuccess = fp_SetPreferredUILanguages(MUI_LANGUAGE_NAME,userLanguagesMultiString,&setLangCount);
            }
        }

        // 2. Application obtains access to the proper resource container 
        // for standard Win32 resource loading this is normally a PE module
        // LoadMUILibrary is the preferred alternative for loading of resource modules
        // when the application is potentially run on OS versions prior to Windows Vista
        // LoadMUILibrary is available via Windows SDK releases in Windows Vista and later
        // When available, it is advised to get the most up-to-date Windows SDK (e.g., Windows 7)
        HMODULE resContainer = NULL;
        if(setSuccess) // Windows Vista and later OS scenario
        {
            resContainer = LoadMUILibraryW(HELLO_MODULE_CONTRIVED_FILE_PATH,MUI_LANGUAGE_NAME,0);
        }
        else // this block should only be hit on Windows XP and earlier OS platforms as setSuccess will be TRUE on Windows Vista and later
        {
            // need to provide your own fallback mechanism such as the implementation below
            // in essence the application will iterate through the user configured language list
            WCHAR * next = userLanguagesMultiString;
            while(!resContainer && *next != L'\0')
            {
                // convert the language name to an appropriate LCID
                // DownlevelLocaleNameToLCID is available via standalone download package 
                // and is contained in Nlsdl.h / Nlsdl.lib
                LCID nextLcid = DownlevelLocaleNameToLCID(next,DOWNLEVEL_LOCALE_NAME);
                // then have LoadMUILibrary attempt to probe for the right .mui module
                resContainer = LoadMUILibraryW(HELLO_MODULE_CONTRIVED_FILE_PATH,MUI_LANGUAGE_NAME,(LANGID)nextLcid);
                // increment to the next language name in our list
                size_t nextStrLen = 0;
                if(SUCCEEDED(StringCchLengthW(next,LOCALE_NAME_MAX_LENGTH,&nextStrLen)))
                    next += (nextStrLen + 1);
                else
                    break; // string is invalid - need to exit
            }
            // if the user configured list did not locate a module then try the languages associated with the system
            if(!resContainer)
                resContainer = LoadMUILibraryW(HELLO_MODULE_CONTRIVED_FILE_PATH,MUI_LANGUAGE_NAME,0);
        }
        if(!resContainer)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource container module, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        // 3. Application parses the resource container to find the appropriate item
        WCHAR szHello[SUFFICIENTLY_LARGE_STRING_BUFFER];
        if(LoadStringW(resContainer,HELLO_MUI_STR_0,szHello,SUFFICIENTLY_LARGE_STRING_BUFFER) == 0)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            FreeLibrary(resContainer);
            return 1; // exit
        }

        // 4. Application presents the discovered resource to the user via UI
        swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"%s MUI",szHello);
        MessageBoxW(NULL,displayBuffer,L"HelloMUI",MB_OK | MB_ICONINFORMATION);

        // 5. Application cleans up memory associated with the resource container after this item is no longer needed.
        if(!FreeMUILibrary(resContainer))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to unload the resource container, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        return 0;
    }

    BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize)
    {
        BOOL rtnVal = FALSE;
        // very simple implementation - assumes that first 'langStrSize' characters of the 
        // L".\\langs.txt" file comprises a string of one or more languages
        HANDLE langConfigFileHandle = CreateFileW(L".\\langs.txt", GENERIC_READ, 0, 
            NULL, OPEN_EXISTING, FILE_ATTRIBUTE_NORMAL, NULL);
        if(langConfigFileHandle != INVALID_HANDLE_VALUE)
        {
            // clear out the input variables
            DWORD bytesActuallyRead = 0;
            if(ReadFile(langConfigFileHandle,langStr,langStrSize*sizeof(WCHAR),&bytesActuallyRead,NULL) && bytesActuallyRead > 0)
            {
                rtnVal = TRUE;
                DWORD nullIndex = (bytesActuallyRead/sizeof(WCHAR) < langStrSize) ? bytesActuallyRead/sizeof(WCHAR) : langStrSize;
                langStr[nullIndex] = L'\0';
            }
            CloseHandle(langConfigFileHandle);
        }
        return rtnVal;
    }
    BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize)
    {
        BOOL rtnVal = FALSE;
        size_t strLen = 0;
        rtnVal = SUCCEEDED(StringCchLengthW(langStr,USER_CONFIGURATION_STRING_BUFFER*2,&strLen));
        if(rtnVal && strLen > 0 && langMultiStr && langMultiStrSize > 0)
        {
            WCHAR * langMultiStrPtr = langMultiStr;
            WCHAR * last = langStr + (langStr[0] == 0xFEFF ? 1 : 0);
            WCHAR * context = last;
            WCHAR * next = wcstok_s(last,L",; :",&context);
            while(next && rtnVal)
            {
                // make sure you validate the user input
                if(SUCCEEDED(StringCchLengthW(last,LOCALE_NAME_MAX_LENGTH,&strLen)) 
                    && DownlevelLocaleNameToLCID(next,0) != 0)
                {
                    langMultiStrPtr[0] = L'\0';
                    rtnVal &= SUCCEEDED(StringCchCatW(langMultiStrPtr,(langMultiStrSize - (langMultiStrPtr - langMultiStr)),next));
                    langMultiStrPtr += strLen + 1;
                }
                next = wcstok_s(NULL,L",; :",&context);
                if(next)
                    last = next;
            }
            if(rtnVal && (langMultiStrSize - (langMultiStrPtr - langMultiStr))) // make sure there is a double null term for the multi-string 
            {
                langMultiStrPtr[0] = L'\0';
            }
            else // fail and guard anyone whom might use the multi-string
            {
                langMultiStr[0] = L'\0';
                langMultiStr[1] = L'\0';
            }
        }
        return rtnVal;
    }
    ```

    

4.  Créez ou copiez langs.txt dans le répertoire approprié, comme décrit précédemment à l ['étape 4 : globalisation de « Hello MUI »](#step-4-globalizing-hello-mui).
5.  Générez et exécutez le projet.

> [!Note]  
> si l’application doit s’exécuter sur Windows versions antérieures à Windows Vista, veillez à lire les documents fournis avec le package des [api de niveau inférieur de Microsoft NLS](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&amp;DisplayLang=en) sur la façon de redistribuer les Nlsdl.dll.

 

## <a name="additional-considerations-for-mui"></a>Considérations supplémentaires pour MUI

### <a name="support-for-console-applications"></a>Prise en charge des applications console

Les techniques abordées dans ce didacticiel peuvent également être utilisées dans les applications console. toutefois, contrairement à la plupart des contrôles GUI standard, la fenêtre de commande Windows ne peut pas afficher de caractères pour toutes les langues. Pour cette raison, les applications console multilingues requièrent une attention particulière.

L’appel des API [**SetThreadUILanguage**](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage) ou [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) avec des indicateurs de filtrage spécifiques entraîne la suppression, par les fonctions de chargement des ressources, des sondes de ressources de langue pour des langues spécifiques qui ne sont normalement pas affichées dans une fenêtre de commande. Lorsque ces indicateurs sont définis, les algorithmes de définition de langue autorisent uniquement les langues qui s’affichent correctement dans la fenêtre de commande à se trouver dans la liste de secours.

Pour plus d’informations sur l’utilisation de ces API pour générer une application console multilingue, consultez les sections Notes de [**SetThreadUILanguage**](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage) et [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages).

### <a name="determination-of-languages-to-support-at-run-time"></a>Détermination des langues à prendre en charge au Run-Time

Vous pouvez adopter l’une des suggestions de conception suivantes pour déterminer les langues que votre application doit prendre en charge au moment de l’exécution :

-   **Pendant l’installation, autorisez l’utilisateur final à sélectionner la langue par défaut dans la liste des langues prises en charge.**

-   **Lire une liste de langues à partir d’un fichier de configuration**

    Certains des projets de ce didacticiel contiennent une fonction utilisée pour analyser un fichier de configuration langs.txt, qui contient une liste de langues.

    Étant donné que cette fonction prend une entrée externe, validez les langues fournies comme entrée. Pour plus d’informations sur l’exécution de cette validation, consultez les fonctions [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename) ou [**DownLevelLocaleNameToLCID**](downlevellocalenametolcid.md) .

-   **Interroger le système d’exploitation pour déterminer les langues installées**

    Cette approche permet à l’application d’utiliser la même langue que le système d’exploitation. Bien que cela ne nécessite pas d’invite de l’utilisateur, si vous choisissez cette option, sachez que les langues du système d’exploitation peuvent être ajoutées ou supprimées à tout moment et peuvent changer après l’installation de l’application par l’utilisateur. Sachez également que dans certains cas, le système d’exploitation est installé avec une prise en charge de langue limitée, et l’application offre plus de valeur si elle prend en charge les langues que le système d’exploitation ne prend pas en charge.

    Pour plus d’informations sur la façon de déterminer les langues actuellement installées dans le système d’exploitation, consultez la fonction [**EnumUILanguages**](/windows/desktop/api/Winnls/nf-winnls-enumuilanguagesa) .

### <a name="complex-script-support-in-versions-prior-to-windows-vista"></a>prise en charge des scripts complexes dans les Versions antérieures à Windows Vista

lorsqu’une application qui prend en charge certains scripts complexes s’exécute sur une version de Windows antérieure à Windows Vista, le texte de ce script peut ne pas s’afficher correctement dans les composants de l’interface utilisateur graphique. Par exemple, dans le projet de niveau inférieur de ce didacticiel, les scripts hi-IN et ta peuvent ne pas s’afficher dans la boîte de message en raison de problèmes liés au traitement de scripts complexes et au manque de polices associées. En règle générale, les problèmes de cette nature se présentent sous forme de carrés dans le composant GUI.

Pour plus d’informations sur l’activation du traitement de script complexe [, consultez prise en charge des scripts et des polices dans Windows](https://msdn.microsoft.com/goglobal/bb688099.aspx).

## <a name="summary"></a>Résumé

Ce didacticiel a globalisé une application monolingue et a démontré les meilleures pratiques suivantes.

-   Concevez l’application pour tirer parti du modèle de ressource Win32.
-   Utilisez le fractionnement MUI des ressources en fichiers binaires satellites (fichiers. MUI).
-   Assurez-vous que le processus de localisation met à jour les ressources dans les fichiers. mui afin qu’elles soient adaptées à la langue cible.
-   Assurez-vous que l’empaquetage et le déploiement de l’application, des fichiers. mui associés et du contenu de configuration sont effectués correctement pour permettre aux API de chargement des ressources de rechercher le contenu localisé.
-   Fournissez à l’utilisateur final un mécanisme pour ajuster la configuration de la langue de l’application.
-   Ajustez le code d’exécution pour tirer parti de la configuration du langage, afin de rendre l’application plus réactive aux besoins de l’utilisateur final.

 

 
