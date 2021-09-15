---
description: Cette rubrique explique comment les applications peuvent exposer les informations nécessaires pour activer certains scénarios.
ms.assetid: F88AA3E6-6F7B-442d-935A-7D2CB4958E6B
title: Inscription de l’application
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0b9647809f46c2147ab6ed464f0e8de1d7ef0df
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127313169"
---
# <a name="application-registration"></a>Inscription de l’application

Cette rubrique explique comment les applications peuvent exposer les informations nécessaires pour activer certains scénarios. Cela comprend les informations nécessaires pour localiser l’application, les verbes pris en charge par l’application et les types de fichiers qu’une application peut gérer.

Cette rubrique est organisée comme suit :

-   [Recherche d’un exécutable d’application](#finding-an-application-executable)
-   [Inscription des applications](#registering-applications)
    -   [Utilisation de la sous-clé Paths de l’application](#using-the-app-paths-subkey)
    -   [Utilisation de la sous-clé applications](#using-the-applications-subkey)
-   [Inscription de verbes et d’autres informations d’association de fichiers](#registering-verbs-and-other-file-association-information)
-   [Inscription d’un type perçu](#registering-a-perceived-type)
-   [Rubriques connexes](#related-topics)

> [!Note]  
> Les applications peuvent également être inscrites dans les applications configurer les paramètres d’accès aux programmes et les paramètres par défaut de l’ordinateur (SPAD) et définir les applications du panneau de configuration des programmes par défaut (SYDP). Pour plus d’informations sur SPAD et l’inscription des applications SYDP, consultez [instructions pour les associations de fichiers et les programmes par défaut](appguide-fa-defpro.md), et [définir les paramètres par défaut de l’accès aux programmes et des ordinateurs (SPAD)](cpl-setprogramaccess.md).

 

## <a name="finding-an-application-executable"></a>Recherche d’un exécutable d’application

Lorsque la fonction [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa) est appelée avec le nom d’un fichier exécutable dans son paramètre *lpFile* , il y a plusieurs emplacements où la fonction recherche le fichier. Nous vous recommandons d’inscrire votre application dans la sous-clé de Registre **App Paths** . Cela permet d’éviter que des applications modifient la variable d’environnement du chemin d’accès système.

Le fichier est recherché dans les emplacements suivants :

-   Le répertoire de travail actuel
-   répertoire **Windows** uniquement (aucun sous-répertoire n’est recherché).
-   répertoire **Windows \\ System32** .
-   Répertoires figurant dans la variable d’environnement PATH.
-   recommandé : **HKEY \_ LOCAL \_ MACHINE** \\ **SOFTWARE** \\ **Microsoft** \\ **Windows** les \\  \\ **chemins d’accès** de l’application CurrentVersion

## <a name="registering-applications"></a>Inscription des applications

Les sous-clés de registre des **applications** et des **chemins d’application** sont utilisées pour enregistrer et contrôler le comportement du système pour le compte des applications. La sous-clé **paths** de l’application est l’emplacement par défaut.

### <a name="using-the-app-paths-subkey"></a>Utilisation de la sous-clé Paths de l’application

dans Windows 7 et versions ultérieures, nous vous recommandons vivement d’installer les applications par utilisateur plutôt qu’par ordinateur. une application installée pour par utilisateur peut être inscrite sous **HKEY \_ CURRENT \_ user** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **App paths**. une application installée pour tous les utilisateurs de l’ordinateur peut être inscrite sous **HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **App paths**.

Les entrées trouvées sous les **chemins d’accès aux applications** sont principalement utilisées pour les opérations suivantes :

-   Pour mapper le nom du fichier exécutable d’une application au chemin d’accès complet de ce fichier.
-   Pour prédéfinir les informations de la variable d’environnement PATH pour chaque application, par processus.

Si le nom d’une sous-clé de **chemins d’accès d’application** correspond au nom de fichier, l’interpréteur de commandes effectue deux actions :

-   L’entrée (par défaut) est utilisée en tant que chemin d’accès qualifié complet du fichier.
-   L’entrée de chemin d’accès de cette sous-clé est précédée de la variable d’environnement PATH de ce processus. Si ce n’est pas nécessaire, la valeur du chemin d’accès peut être omise.

Les problèmes potentiels à prendre en compte sont les suivants :

-   L’interpréteur de commandes limite la longueur d’une ligne de commande à un chemin d’accès maximal de \_ \* 2 caractères. Si de nombreux fichiers sont répertoriés comme entrées de registre ou si leurs chemins d’accès sont longs, les noms de fichiers plus loin dans la liste peuvent être perdus lorsque la ligne de commande est tronquée.
-   Certaines applications n’acceptent pas plusieurs noms de fichiers dans une ligne de commande.
-   Certaines applications qui acceptent plusieurs noms de fichiers ne reconnaissent pas le format dans lequel l’interpréteur de commandes les fournit. L’interpréteur de commandes fournit la liste de paramètres sous la forme d’une chaîne entre guillemets, mais certaines applications peuvent nécessiter des chaînes sans guillemets.
-   Tous les éléments qui peuvent être déplacés ne font pas partie du système de fichiers. par exemple, imprimantes. Comme ces éléments n’ont pas de chemin d’accès Win32 standard, il n’est pas possible de fournir une valeur *lpParameters* significative à [**ShellExecuteEx**](/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa).

L’utilisation de l’entrée DropTarget permet d’éviter ces problèmes potentiels en fournissant un accès à tous les formats de presse-papiers, y compris [CFSTR \_ SHELLIDLIST](clipboard.md) (pour les listes de fichiers longues) et [CFSTR \_ FILECONTENTS](clipboard.md) (pour les objets non-système de fichiers).

**Pour inscrire et contrôler le comportement de vos applications avec la sous-clé chemins d’accès de l’application**:

1.  Ajoutez une sous-clé portant le même nom que votre fichier exécutable à la sous-clé **chemins d’accès** de l’application, comme indiqué dans l’entrée de Registre suivante.

    ```
    HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
       SOFTWARE
          Microsoft
             Windows
                CurrentVersion
                   App Paths
                      file.exe
                         (Default)
                         DontUseDesktopChangeRouter
                         DropTarget
                         Path
                         UseUrl
    ```

2.  Consultez le tableau suivant pour plus d’informations sur les entrées de la sous-clé **paths** de l’application. 

    
| Entrée de Registre | Détails | 
|----------------|---------|
| (Par défaut) | Est le chemin d’accès complet à l’application. Le nom d’application fourni dans l’entrée (valeur par défaut) peut être indiqué avec ou sans son extension de .exe. Si nécessaire, la fonction <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> ajoute l’extension lors de la recherche de la sous-clé <strong>chemins d’accès</strong> de l’application. L’entrée est du type de <strong>REG_SZ</strong> . | 
| DontUseDesktopChangeRouter | est obligatoire pour les applications du débogueur afin d’éviter les blocages de boîtes de dialogue de fichier lors du débogage du processus Windows Explorer. Toutefois, la définition de l’entrée DontUseDesktopChangeRouter produit une gestion légèrement moins efficace des notifications de modification. L’entrée est du type de <strong>REG_DWORD</strong> et la valeur est 0x1. | 
| DropTarget | Identificateur de classe (CLSID). L’entrée DropTarget contient le CLSID d’un objet (généralement un serveur local plutôt qu’un serveur in-process) qui implémente <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget</strong></a>. Par défaut, lorsque la cible de déplacement est un fichier exécutable et qu’aucune valeur DropTarget n’est fournie, l’interpréteur de commandes convertit la liste des fichiers déplacés en un paramètre de ligne de commande et le transmet à <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> via <em>lpParameters</em>. | 
| Chemin d’accès | Fournit une chaîne (sous la forme d’une liste de répertoires séparés par des points-virgules) à ajouter à la variable d’environnement PATH quand une application est lancée en appelant <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a>. Il s’agit du chemin d’accès complet au .exe. Elle est de <strong>REG_SZ</strong>. dans <strong>Windows 7 et versions ultérieures</strong>, le type peut être <strong>REG_EXPAND_SZ</strong>, et est généralement <strong>REG_EXPAND_SZ</strong> % ProgramFiles%.    <blockquote>    [!Note]<br />    En plus des entrées (par défaut), path et DropTarget reconnues par l’interpréteur de commandes, une application peut également ajouter des valeurs personnalisées à la sous-clé <strong>chemins d’accès</strong> de l’application de son fichier exécutable. Nous encourageons les développeurs d’applications à utiliser la sous-clé <strong>paths</strong> de l’application pour fournir un chemin d’accès spécifique à l’application au lieu d’apporter des ajouts au chemin d’accès du système global.    </blockquote><br /> | 
| SupportedProtocols | Crée une chaîne qui contient les schémas de protocole d’URL pour une clé donnée. Peut contenir plusieurs valeurs de Registre pour indiquer les schémas pris en charge. Cette chaîne suit le format <strong>scheme1 : scheme2</strong>. Si cette liste n’est pas vide, le <strong>fichier :</strong> sera ajouté à la chaîne. Ce protocole est pris en charge implicitement quand <em>SupportedProtocols</em> est défini. <br /> | 
| UseUrl | Indique que votre application peut accepter une URL (au lieu d’un nom de fichier) sur la ligne de commande. Les applications qui peuvent ouvrir des documents directement à partir d’Internet, comme les navigateurs Web et les lecteurs multimédias, doivent définir cette entrée. <br /> Lorsque la fonction <a href="/windows/desktop/api/Shellapi/nf-shellapi-shellexecuteexa"><strong>ShellExecuteEx</strong></a> démarre une application et que la valeur UseUrl = 1 n’est pas définie, <strong>ShellExecuteEx</strong> télécharge le document dans un fichier local et appelle le gestionnaire sur la copie locale.<br /> Par exemple, si cette entrée est définie pour l’application et qu’un utilisateur clique avec le bouton droit sur un fichier stocké sur un serveur Web, le verbe Open est rendu disponible. Si ce n’est pas le cas, l’utilisateur doit télécharger le fichier et ouvrir la copie locale. <br /> L’entrée UseUrl est de type <strong>REG_DWORD</strong> , et la valeur est 0x1.<br /> dans Windows Vista et les versions antérieures, cette entrée indique que l’URL doit être transmise à l’application avec un nom de fichier local, lorsqu’elle est appelée via ShellExecuteEx. dans Windows 7, il indique que l’application peut comprendre toute url http ou https qui lui est transmise, sans avoir à fournir également le nom du fichier cache. Cette clé de Registre est associée à la clé <em>SupportedProtocols</em> .<br /> | 


    

     

### <a name="using-the-applications-subkey"></a>Utilisation de la sous-clé applications

Grâce à l’inclusion d’entrées de Registre sous la sous-clé de l’application **\_ \_ racine HKEY classes** \\  \\ *ApplicationName.exe* , les applications peuvent fournir les informations spécifiques à l’application, comme indiqué dans le tableau suivant.



| Entrée de Registre                   | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| verbe de Shell \\                      | Fournit la méthode Verb pour appeler l’application à partir de OpenWith. Sans définition de verbe spécifiée ici, le système suppose que l’application prend en charge [**CreateProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa)et transmet le nom de fichier sur la ligne de commande. cette fonctionnalité s’applique à toutes les méthodes de verbe, notamment DropTarget, ExecuteCommand et échange dynamique de données (DDE).                                                                                                                                                                                                                                                                                                                            |
| DefaultIcon                      | Permet à une application de fournir une icône spécifique pour représenter l’application au lieu de la première icône stockée dans le fichier de .exe.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| FriendlyAppName                  | Fournit un moyen d’obtenir un nom localisable à afficher pour une application au lieu de simplement les informations de version qui apparaissent, qui peuvent ne pas être localisables. La requête d’association [**ASSOCSTR**](/windows/desktop/api/Shlwapi/ne-shlwapi-assocstr) lit cette valeur d’entrée de Registre et revient à utiliser le nom de FileDescription dans les informations de version. Si ce nom est manquant, la requête d’association prend par défaut le nom d’affichage du fichier. Les applications doivent utiliser **ASSOCSTR \_ FRIENDLYAPPNAME** pour récupérer ces informations afin d’obtenir le comportement approprié.                                                                                                                                                                        |
| SupportedTypes                   | Répertorie les types de fichiers pris en charge par l’application. Cela permet à l’application d’être listée dans le menu cascade de la boîte de dialogue **Ouvrir avec** .                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| NoOpenWith                       | Indique qu’aucune application n’est spécifiée pour l’ouverture de ce type de fichier. Sachez que si une sous-clé OpenWithProgIDs a été définie pour une application par type de fichier et que la sous-clé ProgID elle-même n’a pas d’entrée NoOpenWith, celle-ci apparaît dans la liste des applications recommandées ou disponibles, même si elle a spécifié l’entrée NoOpenWith. Pour plus d’informations, consultez [Comment inclure une application dans la boîte de dialogue Ouvrir avec](how-to-include-an-application-on-the-open-with-dialog-box.md) et [Comment exclure une application de la boîte de dialogue Ouvrir avec](how-to-exclude-an-application-from-the-open-with-dialog-box-for-unassociated-file-types.md).<br/> |
| IsHostApp                        | Indique que le processus est un processus hôte, par exemple Rundll32.exe ou Dllhost.exe, et qu’il ne doit pas être pris en compte pour l’épinglage du menu **Démarrer** ou pour l’inclusion dans la liste la plus fréquemment utilisée (MFU). Lorsqu’il est lancé avec un raccourci qui contient une liste d’arguments non null ou un [ID de modèle d’utilisateur d’application explicite (AppUserModelIDs)](appids.md), le processus peut être épinglé (comme ce raccourci). Ces raccourcis sont des candidats à inclure dans la liste des MFU.                                                                                                                                                                                                                                                  |
| NoStartPage                      | Indique que l’exécutable et les raccourcis de l’application doivent être exclus du menu **Démarrer** et de l’épinglage ou de l’inclusion dans la liste des applications les plus fréquemment exécutées. Cette entrée est généralement utilisée pour exclure les outils système, les programmes d’installation et les programmes de désinstallation, ainsi que les fichiers Lisez-moi.                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| UseExecutableForTaskbarGroupIcon | Fait en sorte que la barre des tâches utilise l’icône par défaut de cet exécutable s’il n’y a aucun raccourci regroupement pour cette application, et au lieu de l’icône de la fenêtre qui a été rencontrée pour la première fois.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| TaskbarGroupIcon                 | Spécifie l’icône utilisée pour remplacer l’icône de la barre des tâches. L’icône de la fenêtre est normalement utilisée pour la barre des tâches. La définition de l’entrée TaskbarGroupIcon fait en sorte que le système utilise l’icône à la place de l' .exe pour l’application.                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |



 

### <a name="examples"></a>Exemples

Voici quelques exemples d’inscriptions d’applications par le biais des applications **\_ \_ racines HKEY classes** \\  \\ *ApplicationName.exe* sous-clé. Toutes les valeurs d’entrée de Registre sont de type de Registre **\_ SZ** , à l’exception de **DefaultIcon** , qui est de type reg de type **\_ \_ SZ** .

```
HKEY_CLASSES_ROOT
   Applications
      wordpad.exe
         FriendlyAppName = @%SystemRoot%\System32\shell32.dll,-22069
```

```
HKEY_CLASSES_ROOT
   Applications
      wmplayer.exe
         SupportedTypes
            .3gp2
```

```
HKEY_CLASSES_ROOT
   Applications
      wmplayer.exe
         DefaultIcon
            (Default) = %SystemRoot%\system32\wmploc.dll,-730
```

```
HKEY_CLASSES_ROOT
   Applications
      WScript.exe
         NoOpenWith
```

```
HKEY_CLASSES_ROOT
   Applications
      photoviewer.dll
         shell
            open
               DropTarget
                  Clsid = {FFE2A43C-56B9-4bf5-9A79-CC6D4285608A}
```

```
HKEY_CLASSES_ROOT
   Applications
      mspaint.exe
         SupportedTypes
            .bmp
            .dib
            .rle
            .jpg
            .jpeg
            .jpe
            .jfif
            .gif
            .emf
            .wmf
            .tif
            .tiff
            .png
            .ico
```

## <a name="registering-verbs-and-other-file-association-information"></a>Inscription de verbes et d’autres informations d’association de fichiers

Les sous-clés inscrites sous les SystemFileAssociations **\_ \_ racines de la classe HKEY** \\  permettent à l’interpréteur de commandes de définir le comportement par défaut des attributs pour les types de fichiers et d’activer les associations de fichiers partagés. Lorsque les utilisateurs modifient l’application par défaut pour un type de fichier, le ProgID de la nouvelle application par défaut a la priorité dans la fourniture de verbes et d’autres informations d’association. Cette priorité est due à la première entrée dans le tableau d’association. Si le programme par défaut est modifié, les informations sous le ProgID précédent ne sont plus disponibles.

Pour traiter de manière proactive avec les conséquences d’une modification apportée aux programmes par défaut, vous pouvez utiliser les **\_ classes HKEY \_ root** \\ **SystemFileAssociations** pour enregistrer les verbes et d’autres informations d’association. En raison de leur emplacement après le ProgID dans le tableau d’association, ces inscriptions ont une priorité plus faible. Ces SystemFileAssociationsregistrations sont stables même lorsque les utilisateurs modifient les programmes par défaut et fournissent un emplacement pour enregistrer les verbes secondaires qui seront toujours disponibles pour un type de fichier particulier. Pour obtenir un exemple de Registre, consultez [inscription d’un type perçu](#registering-a-perceived-type) plus loin dans cette rubrique.

L’exemple de Registre suivant montre ce qui se produit lorsque l’utilisateur exécute l’élément **programmes par défaut** dans le panneau de configuration pour modifier la valeur par défaut de .mp3 fichiers en App2ProgID. Après avoir modifié la valeur par défaut, Verb1 n’est plus disponible et Verb2 devient la valeur par défaut.

```
HKEY_CLASSES_ROOT
   .mp3
      (Default) = App1ProgID
```

```
HKEY_CLASSES_ROOT
   App1ProgID
      shell
         Verb1
```

```
HKEY_CLASSES_ROOT
   App2ProgID
      shell
         Verb2
```

## <a name="registering-a-perceived-type"></a>Inscription d’un type perçu

Les valeurs de Registre pour les types perçus sont définies en tant que sous-clés de la sous-clé de Registre **HKEY \_ classes \_ racine** \\ **SystemFileAssociations** . Par exemple, le **texte** du type perçu est inscrit comme suit :

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      text
         shell
            edit
               command
                  (Default) = "%SystemRoot%\system32\NOTEPAD.EXE" "%1"
            open
               command
                  (Default) = "%SystemRoot%\system32\NOTEPAD.EXE" "%1"
```

Le type perçu d’un type de fichier est indiqué par l’inclusion d’une valeur PerceivedType dans la sous-clé du type de fichier. La valeur PerceivedType est définie sur le nom du type perçu inscrit sous la sous-clé de Registre **\_ \_ racine** SystemFileAssociations de la classe HKEY \\  , comme indiqué dans l’exemple précédent du Registre. Pour déclarer des fichiers. cpp comme étant du type « text », par exemple, ajoutez l’entrée de Registre suivante :

```
HKEY_CLASSES_ROOT
   .cpp
      PerceivedType = text
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Types de fichiers](fa-file-types.md)
</dt> <dt>

[Fonctionnement des associations de fichiers](fa-how-work.md)
</dt> <dt>

[Affichage du contenu par type de fichier ou par type](prophand-content-view.md)
</dt> <dt>

[Vérificateur de type de fichier](file-type-verifier.md)
</dt> <dt>

[Gestionnaires de types de fichiers](fa-file-extensions.md)
</dt> <dt>

[Identificateurs programmatiques](fa-progids.md)
</dt> <dt>

[Types perçus](fa-perceivedtypes.md)
</dt> <dt>

[Tableaux d’association](fa-associationarray.md)
</dt> </dl>

