---
title: Activation des styles visuels
description: Cette rubrique explique comment configurer votre application pour vous assurer que les contrôles communs s’affichent dans le style visuel préféré de l’utilisateur.
ms.assetid: eb6c2469-25b9-43c4-a6ca-391a7b2859b3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a4673d0a47f42f557e09f4afe46131cd48bad1b0
ms.sourcegitcommit: 967ba3a2a618e6088cb607164a2a924530278645
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113102168"
---
# <a name="enabling-visual-styles"></a>Activation des styles visuels

Cette rubrique explique comment configurer votre application pour vous assurer que les contrôles communs s’affichent dans le style visuel préféré de l’utilisateur.

Cette rubrique comprend les sections suivantes.

-   [Utilisation de manifestes ou de directives pour s’assurer que les styles visuels peuvent être appliqués aux applications](#using-manifests-or-directives-to-ensure-that-visual-styles-can-be-applied-to-applications)
-   [Utilisation de ComCtl32.dll version 6 dans une application qui utilise uniquement des extensions standard](#using-comctl32dll-version-6-in-an-application-that-uses-only-standard-extensions)
-   [À l’aide de ComCtl32 version 6 dans le panneau de configuration ou d’une DLL exécutée par RunDll32.exe](#using-comctl32-version-6-in-control-panel-or-a-dll-that-is-run-by-rundll32exe)
-   [Ajout de la prise en charge de style visuel à une extension, à un plug-in, à un composant logiciel enfichable MMC ou à une DLL introduite dans un processus](#adding-visual-style-support-to-an-extension-plug-in-mmc-snap-in-or-a-dll-that-is-brought-into-a-process)
-   [Désactivation des styles visuels](#turning-off-visual-styles)
-   [Utilisation de styles visuels avec du contenu HTML](#using-visual-styles-with-html-content)
-   [Quand les styles visuels ne sont pas appliqués](#when-visual-styles-are-not-applied)
-   [Rendre votre application compatible avec les versions antérieures de Windows](#making-your-application-compatible-with-earlier-versions-of-windows)
-   [Rubriques connexes](#related-topics)

## <a name="using-manifests-or-directives-to-ensure-that-visual-styles-can-be-applied-to-applications"></a>Utilisation de manifestes ou de directives pour s’assurer que les styles visuels peuvent être appliqués aux applications

Pour permettre à votre application d’utiliser des styles visuels, vous devez utiliser ComCtl32.dll version 6 ou ultérieure. Étant donné que la version 6 n’est pas redistribuable, elle est disponible uniquement lorsque votre application s’exécute sur une version de Windows qui la contient. Windows est fourni avec les versions 5 et 6. ComCtl32.dll version 6 contient à la fois les contrôles utilisateur et les contrôles communs. Par défaut, les applications utilisent les contrôles utilisateur définis dans User32.dll et les contrôles communs définis dans ComCtl32.dll version 5. Pour obtenir la liste des versions de DLL et leurs plateformes de distribution, consultez la page [versions de contrôle courantes](common-control-versions.md).

Si vous souhaitez que votre application utilise des styles visuels, vous devez ajouter un manifeste d’application ou une directive de compilateur qui indique que ComCtl32.dll version 6 doit être utilisée si elle est disponible.

Un manifeste d’application permet à une application de spécifier les versions d’un assembly dont elle a besoin. Dans Microsoft Win32, un assembly est un ensemble de dll et une liste d’objets pouvant être mis en version qui sont contenus dans ces dll.

Les manifestes sont écrits en XML. Le nom du fichier manifeste de l’application est le nom de votre exécutable suivi de l’extension de nom de fichier. manifest ; par exemple, MyApp.exe. manifest. L’exemple de manifeste suivant montre que la première section décrit le manifeste lui-même. Le tableau suivant présente les attributs définis par l’élément **assemblyIdentity** dans la section Description du manifeste.



| Attribut             | Description                                                                                                                 |
|-----------------------|-----------------------------------------------------------------------------------------------------------------------------|
| version               | Version du manifeste. La version doit se présenter sous la forme major. minor. revision. Build (autrement dit, n. n. n. n, où n <= 65535). |
| processorArchitecture | Processeur pour lequel votre application est développée.                                                                          |
| name                  | Comprend le nom de la société, le nom du produit et le nom de l’application.                                                                   |
| type                  | Type de votre application, tel que Win32.                                                                                    |



 

L’exemple de manifeste fournit également une description de votre application et spécifie des dépendances d’application. Le tableau suivant présente les attributs définis par l’élément **assemblyIdentity** dans la section Dependency.



| Attribut             | Description                                      |
|-----------------------|--------------------------------------------------|
| type                  | Type du composant de dépendance, tel que Win32. |
| name                  | Nom du composant.                           |
| version               | Numéro de version du composant.                        |
| processorArchitecture | Processeur pour lequel le composant est conçu.    |
| publicKeyToken        | Jeton de clé utilisé avec ce composant.              |
| langage              | Langue du composant.                       |



 

Voici un exemple de fichier manifeste.

> [!IMPORTANT]
> Définissez l’entrée **ProcessorArchitecture** sur **« x86 »** si votre application cible la plateforme Windows 32 bits, ou sur **« amd64 »** si votre application cible la plateforme Windows 64 bits. Vous pouvez également spécifier **« \* »**, ce qui garantit que toutes les plateformes sont ciblées, comme illustré dans les exemples suivants.

 


```C++
<?xml version="1.0" encoding="UTF-8" standalone="yes"?>
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
<assemblyIdentity
    version="1.0.0.0"
    processorArchitecture="*"
    name="CompanyName.ProductName.YourApplication"
    type="win32"
/>
<description>Your application description here.</description>
<dependency>
    <dependentAssembly>
        <assemblyIdentity
            type="win32"
            name="Microsoft.Windows.Common-Controls"
            version="6.0.0.0"
            processorArchitecture="*"
            publicKeyToken="6595b64144ccf1df"
            language="*"
        />
    </dependentAssembly>
</dependency>
</assembly>
```



Si vous utilisez Microsoft Visual C++ 2005 ou une version ultérieure, vous pouvez ajouter la directive de compilateur suivante à votre code source au lieu de créer manuellement un manifeste. Pour une meilleure lisibilité, la directive est divisée en plusieurs lignes ici.


```C++
#pragma comment(linker,"\"/manifestdependency:type='win32' \
name='Microsoft.Windows.Common-Controls' version='6.0.0.0' \
processorArchitecture='*' publicKeyToken='6595b64144ccf1df' language='*'\"")
```



Les rubriques suivantes décrivent les étapes à suivre pour appliquer des styles visuels à différents types d’applications. Notez que le format du manifeste est le même dans chaque cas.

## <a name="using-comctl32dll-version-6-in-an-application-that-uses-only-standard-extensions"></a>Utilisation de ComCtl32.dll version 6 dans une application qui utilise uniquement des extensions standard

Voici quelques exemples d’applications qui n’utilisent pas d’extensions tierces.

-   Calculatrice
-   FreeCell (dans Windows Vista et Windows 7)
-   Démineur (dans Windows Vista et Windows 7)
-   Bloc-notes
-   Solitaire (dans Windows Vista et Windows 7)

**Pour créer un manifeste et permettre à votre application d’utiliser des styles visuels.**

1.  Liez à ComCtl32. lib et appelez [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols).
2.  Ajoutez un fichier appelé YourApp.exe. manifest à votre arborescence source qui a le format de manifeste XML.
    ```C++
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        version="1.0.0.0"
        processorArchitecture="*"
        name="CompanyName.ProductName.YourApplication"
        type="win32"
    />
    <description>Your application description here.</description>
    <dependency>
        <dependentAssembly>
            <assemblyIdentity
                type="win32"
                name="Microsoft.Windows.Common-Controls"
                version="6.0.0.0"
                processorArchitecture="*"
                publicKeyToken="6595b64144ccf1df"
                language="*"
            />
        </dependentAssembly>
    </dependency>
    </assembly>
    ```

    

3.  Ajoutez le manifeste au fichier de ressources de votre application comme suit :
    ```C++
    CREATEPROCESS_MANIFEST_RESOURCE_ID RT_MANIFEST "YourApp.exe.manifest"
    ```

    

    > [!Note]  
    > Lorsque vous ajoutez l’entrée précédente à la ressource, vous devez la mettre en forme sur une seule ligne. Vous pouvez également placer le fichier manifeste XML dans le même répertoire que le fichier exécutable de votre application. Le système d’exploitation chargera d’abord le manifeste à partir du système de fichiers, puis vérifiera la section de la ressource du fichier exécutable. La version du système de fichiers est prioritaire.

     

Lorsque vous générez votre application, le manifeste est ajouté en tant que ressource binaire.

## <a name="using-comctl32-version-6-in-control-panel-or-a-dll-that-is-run-by-rundll32exe"></a>À l’aide de ComCtl32 version 6 dans le panneau de configuration ou d’une DLL exécutée par RunDll32.exe

**Pour créer un manifeste et permettre à votre application d’utiliser des styles visuels.**

1.  Liez à ComCtl32. lib et appelez [**InitCommonControls**](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols).
2.  Ajoutez un fichier appelé YourApp.cpl. manifest à votre arborescence source qui a le format de manifeste XML.
    ```C++
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        version="1.0.0.0"
        processorArchitecture="*"
        name="CompanyName.ProductName.YourApplication"
        type="win32"
    />
    <description>Your application description here.</description>
    <dependency>
        <dependentAssembly>
            <assemblyIdentity
                type="win32"
                name="Microsoft.Windows.Common-Controls"
                version="6.0.0.0"
                processorArchitecture="*"
                publicKeyToken="6595b64144ccf1df"
                language="*"
            />
        </dependentAssembly>
    </dependency>
    </assembly>
    ```

    

3.  Ajoutez le manifeste au fichier de ressources de votre application en tant qu’ID de ressource 123.

> [!Note]  
> Lorsque vous créez une application du panneau de configuration, placez-la dans la catégorie appropriée. Le panneau de configuration prend désormais en charge la catégorisation des applications du panneau de configuration. Cela signifie qu’il est possible d’affecter des identificateurs aux applications du panneau de configuration et de les séparer en zones de tâches telles que l’ajout ou la suppression de programmes, l’apparence et les thèmes, ou la date, l’heure, la langue et les options régionales.

 

## <a name="adding-visual-style-support-to-an-extension-plug-in-mmc-snap-in-or-a-dll-that-is-brought-into-a-process"></a>Ajout de la prise en charge de style visuel à une extension, à un plug-in, à un composant logiciel enfichable MMC ou à une DLL introduite dans un processus

La prise en charge des styles visuels peut être ajoutée à une extension, à un plug-in, à un composant logiciel enfichable MMC ou à une DLL introduite dans un processus. Par exemple, utilisez les étapes suivantes pour ajouter la prise en charge des styles visuels pour un composant logiciel enfichable MMC (Microsoft Management Console).

1.  Compilez votre composant logiciel enfichable avec l’indicateur compatible-DISOLATION \_ \_ ou insérez l’instruction suivante avant l' \# instruction include « Windows. h ».

    ```C++
    #define ISOLATION_AWARE_ENABLED 1
    ```

    

    Pour plus d’informations sur la prise en charge de l’ISOLATION \_ \_ , consultez [isolation des composants](/windows/desktop/SbsCs/isolating-components).

2.  Incluez le fichier d’en-tête de contrôle commun dans votre source de composant logiciel enfichable.
    ```C++
    #include <commctrl.h>
    ```

    

3.  Ajoutez un fichier nommé VotreApplication. manifest à votre arborescence source qui utilise le format de manifeste XML.
    ```C++
    <?xml version="1.0" encoding="UTF-8" standalone="yes"?>
    <assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
    <assemblyIdentity
        version="1.0.0.0"
        processorArchitecture="*"
        name="CompanyName.ProductName.YourApplication"
        type="win32"
    />
    <description>Your application description here.</description>
    <dependency>
        <dependentAssembly>
            <assemblyIdentity
                type="win32"
                name="Microsoft.Windows.Common-Controls"
                version="6.0.0.0"
                processorArchitecture="*"
                publicKeyToken="6595b64144ccf1df"
                language="*"
            />
        </dependentAssembly>
    </dependency>
    </assembly>
    ```

    

4.  Ajoutez le manifeste au fichier de ressources de votre composant logiciel enfichable. Pour plus d’informations sur l’ajout d’un manifeste à un fichier de ressources, consultez [utilisation de ComCtl32 version 6 dans une application qui utilise des extensions, des plug-ins ou une dll introduite dans un processus](/previous-versions//ms649781(v=vs.85)) .

## <a name="turning-off-visual-styles"></a>Désactivation des styles visuels

Vous pouvez désactiver les styles visuels pour un contrôle ou pour tous les contrôles d’une fenêtre en appelant la fonction [**SetWindowTheme**](/windows/desktop/api/Uxtheme/nf-uxtheme-setwindowtheme) comme suit :


```C++
SetWindowTheme(hwnd, L" ", L" ");
```



Dans l’exemple précédent, *HWND* est le handle de la fenêtre dans laquelle désactiver les styles visuels. Après l’appel, le contrôle s’affiche sans styles visuels.

## <a name="using-visual-styles-with-html-content"></a>Utilisation de styles visuels avec du contenu HTML

Les styles visuels ne sont pas appliqués aux pages HTML qui modifient les propriétés de feuilles de style en cascade (CSS) telles que l’arrière-plan ou la bordure. Ils affichent l’attribut CSS spécifié. Lorsqu’ils sont spécifiés dans le cadre du contenu, la plupart des propriétés CSS s’appliquent aux éléments auxquels des styles visuels sont appliqués.

Par défaut, les styles visuels sont appliqués aux contrôles HTML intrinsèques sur les pages affichées dans Microsoft Internet Explorer 6 et versions ultérieures. Pour désactiver les styles visuels pour une page HTML, ajoutez une balise META au <head> un peu plus loin dans cet article, aborde l’actualisation de chaque type de source de données. Cette technique s’applique également au contenu empaqueté en tant qu’applications HTML (HTA). Pour désactiver les styles visuels, la balise META doit être la suivante :


```
<META HTTP-EQUIV="MSThemeCompatible" CONTENT="no">
```



> [!Note]  
> Si le paramètre de navigateur et le paramètre de balise ne correspondent pas, la page n’applique pas les styles visuels. Par exemple, si la balise META est définie sur « no » et que le navigateur est configuré pour activer les styles visuels, les styles visuels ne sont pas appliqués à la page. Toutefois, si le navigateur ou la balise META a la valeur « Yes » et que l’autre élément n’est pas spécifié, les styles visuels sont appliqués.

 

Les styles visuels peuvent modifier la disposition de votre contenu. En outre, si vous définissez certains attributs sur des contrôles HTML intrinsèques, tels que la largeur d’un bouton, vous pouvez constater que l’étiquette sur le bouton est illisible dans certains styles visuels.

Vous devez tester minutieusement votre contenu à l’aide de styles visuels pour déterminer si l’application de styles visuels a un effet néfaste sur votre contenu et votre disposition.

## <a name="when-visual-styles-are-not-applied"></a>Quand les styles visuels ne sont pas appliqués

Pour éviter d’appliquer des styles visuels à une fenêtre de niveau supérieur, attribuez à la fenêtre une région non null (**SetWindowRgn**). Le système suppose qu’une fenêtre avec une région non NULL est une fenêtre spécialisée qui n’utilise pas de styles visuels. Une fenêtre enfant associée à une fenêtre de niveau supérieur de styles non visuels peut toujours appliquer des styles visuels même si la fenêtre parente ne le fait pas.

Si vous souhaitez désactiver l’utilisation de styles visuels pour toutes les fenêtres de votre application, appelez [**SetThemeAppProperties**](/windows/desktop/api/Uxtheme/nf-uxtheme-setthemeappproperties) et ne transmettez pas l' \_ indicateur STAP allow non \_ client. Si une application n’appelle pas **SetThemeAppProperties**, les valeurs d’indicateur supposées sont STAP autoriser le non- \_ \_ client \| STAP \_ autoriser les \_ contrôles \| STAP \_ autoriser le \_ contenu WEBCONTENT. Les valeurs supposées provoquent l’application d’un style visuel à la zone non cliente, aux contrôles et au contenu Web.

## <a name="making-your-application-compatible-with-earlier-versions-of-windows"></a>Rendre votre application compatible avec les versions antérieures de Windows

Une grande partie de l’architecture de style visuel est conçue pour faciliter la livraison de votre produit sur les versions antérieures de Windows qui ne prennent pas en charge la modification de l’apparence des contrôles. Lors de l’expédition d’une application pour plusieurs systèmes d’exploitation, tenez compte des éléments suivants :

-   Dans les versions de Windows antérieures à Windows 8, les styles visuels sont désactivés lorsque le contraste élevé est activé. Pour prendre en charge le contraste élevé, une application héritée qui prend en charge les styles visuels doit fournir un chemin de code distinct pour dessiner correctement les éléments d’interface utilisateur en contraste élevé. Dans Windows 8, le contraste élevé fait partie des styles visuels. Toutefois, une application Windows 8 (qui comprend le GUID de Windows 8 dans la section compatibilité de son manifeste d’application) doit toujours fournir un chemin d’accès de code distinct pour restituer correctement avec un contraste élevé sur Windows 7.
-   Si vous utilisez les fonctionnalités de ComCtl32.dll version 6, telles que l’affichage en mosaïque ou le contrôle de lien, vous devez gérer le cas où ces contrôles ne sont pas disponibles sur l’ordinateur de l’utilisateur. ComCtl32.dll version 6 n’est pas redistribuable.
-   Testez votre application pour vous assurer que vous ne vous fiez pas aux fonctionnalités de ComCtl32.dll version 6 sans vérifier d’abord la version actuelle.
-   Ne pas lier à UxTheme. lib.
-   Écrire le code de gestion des erreurs pour les instances lorsque les styles visuels ne fonctionnent pas comme prévu.
-   L’installation du manifeste de votre application dans les versions antérieures n’affectera pas le rendu des contrôles.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Styles visuels](themes-overview.md)
</dt> </dl>

 

 
