---
description: Un objet de gestionnaire d’extensions d’interpréteur de commandes doit être inscrit pour que l’interpréteur de commandes puisse l’utiliser. Cette rubrique est une discussion générale sur l’enregistrement d’un gestionnaire d’extensions de Shell.
ms.assetid: e4b98c18-746b-4909-8821-f25de9d15373
title: Inscription des gestionnaires d’extensions de Shell
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec883f6e843bdfbf663108c0acda123d786262916f4a347d9433e7fd5f77baca
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111209"
---
# <a name="registering-shell-extension-handlers"></a>Inscription des gestionnaires d’extensions de Shell

Un objet de gestionnaire d’extensions d’interpréteur de commandes doit être inscrit pour que l’interpréteur de commandes puisse l’utiliser. Cette rubrique est une discussion générale sur l’enregistrement d’un gestionnaire d’extensions de Shell.

Chaque fois que vous créez ou modifiez un gestionnaire d’extensions de Shell, il est important d’informer le système que vous avez apporté une modification. Pour ce faire, appelez [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify), en spécifiant l’événement **\_ ASSOCCHANGED SHCNE** . Si vous n’appelez pas **SHChangeNotify**, la modification peut ne pas être reconnue tant que le système n’est pas redémarré.

certains facteurs supplémentaires s’appliquent à Windows systèmes 2000. pour plus d’informations, consultez la section [inscrire des gestionnaires d’extensions de Shell sur Windows systèmes 2000](#registering-shell-extension-handlers) .

comme pour tous les objets COM (component Object Model), vous devez créer un GUID pour le gestionnaire à l’aide d’un outil tel que Guidgen.exe, fourni avec le kit de développement logiciel (SDK) Windows. Créez une sous-clé sous le CLSID **\_ \_ racine des classes HKEY** \\  dont le nom est le format de chaîne de ce GUID. Étant donné que les gestionnaires d’extensions de Shell sont des serveurs in-process, vous devez également créer une sous-clé **InprocServer32** sous la sous-clé de GUID avec la valeur (par défaut) définie sur le chemin d’accès de la dll du gestionnaire. Utilisez le modèle de thread cloisonné. En voici un exemple :

```
HKEY_CLASSES_ROOT
   CLSID
      {00021500-0000-0000-C000-000000000046}
         InprocServer32
            (Default) = %windir%\System32\Example.dll
            ThreadingModel = Apartment
```

Chaque fois que l’interpréteur de commandes prend une mesure qui peut impliquer un gestionnaire d’extensions de Shell, il vérifie la sous-clé de registre appropriée. Sous-clé sous laquelle un gestionnaire d’extensions est inscrit contrôle quand il sera appelé. Par exemple, il est courant d’avoir un gestionnaire de menu contextuel appelé lorsque l’interpréteur de commandes affiche un menu contextuel pour un membre d’un [type de fichier](fa-file-types.md). Dans ce cas, le gestionnaire doit être inscrit sous la sous-clé **ProgID** du type de fichier.

Cette rubrique traite des sujets suivants :

-   [Noms de gestionnaires](#handler-names)
-   [Objets Shell prédéfinis](#predefined-shell-objects)
-   [Exemple d’inscription d’un gestionnaire d’extensions](#example-of-an-extension-handler-registration)
    -   [Inscription des gestionnaires d’extensions de Shell](#registering-shell-extension-handlers)
-   [Rubriques connexes](#related-topics)

## <a name="handler-names"></a>Noms de gestionnaires

Pour activer un gestionnaire d’extensions de Shell, créez une sous-clé avec le nom de la sous-clé du gestionnaire (voir ci-dessous) sous la sous-clé **shellex** du **ProgID** (pour les types de fichiers) ou du nom du type d’objet Shell (pour les [ \_ \_ objets Shell prédéfinis](handlers.md)).

Par exemple, si vous souhaitez inscrire un gestionnaire d’extension de menu contextuel pour MyProgram. 1, commencez par créer la sous-clé suivante :

```
HKEY_CLASSES_ROOT
   MyProgram.1
      ShellEx
         ContextMenuHandlers
```

Pour les gestionnaires suivants, créez une sous-clé sous la sous-clé « nom de la sous-clé du gestionnaire » nommée comme version de chaîne de l’identificateur de classe (CLSID) de l’extension de Shell. Plusieurs extensions peuvent être inscrites sous le nom de la sous-clé du gestionnaire en créant plusieurs sous-clés.



| Handler                 | Interface          | Nom de la sous-clé du gestionnaire       |
|-------------------------|--------------------|---------------------------|
| Gestionnaire de fournisseur de colonne | IColumnProvider    | **ColumnHandlers**        |
| Gestionnaire de menu contextuel   | IContextMenu       | **ContextMenuHandlers**   |
| Gestionnaire CopyHook        | ICopyHook          | **CopyHookHandlers**      |
| Gestionnaire de glisser-déplacer   | IContextMenu       | **DragDropHandlers**      |
| Gestionnaire de feuille de propriétés  | IShellPropSheetExt | **PropertySheetHandlers** |



 

Pour les gestionnaires suivants, la valeur par défaut de la clé « nom de la sous-clé du gestionnaire » est la version de chaîne du CLSID de l’extension de Shell. Une seule extension peut être inscrite pour ces gestionnaires.



| Handler                 | Interface            | Nom de la sous-clé du gestionnaire                        |
|-------------------------|----------------------|--------------------------------------------|
| Gestionnaire de données            | IDataObject          | **DataHandler**                            |
| Supprimer le gestionnaire            | IDropTarget          | **DropHandler**                            |
| Gestionnaire d’icône            | IExtractIconA/W      | **IconHandler**                            |
| Gestionnaire d’images miniatures | IThumbnailProvider   | **{E357FCCD-A995-4576-B01F-234630154E96}** |
| Gestionnaire d'info-bulle         | IQueryInfo           | **{00021500-0000-0000-C000-000000000046}** |
| Lien de Shell (ANSI)       | IShellLinkA          | **{000214EE-0000-0000-C000-000000000046}** |
| Lien de Shell (UNICODE)    | IShellLinkW          | **{000214F9-0000-0000-C000-000000000046}** |
| Stockage structuré      | IStorage             | **{0000000B-0000-0000-C000-000000000046}** |
| Métadonnées                | IPropertySetStorage  | **PropertyHandler**                        |
| Épingler au menu Démarrer       | IStartMenuPinnedList | **{a2a9545d-a0c2-42b4-9708-a0b2badd77c8}** |
| Épingler à la barre des tâches          |                      | **{90AA3A4E-1CBA-4233-B8BB-535773D48449}** |



 

Les sous-clés spécifiées pour ajouter **Épingler au menu Démarrer** et **Épingler à la barre des tâches** dans le menu contextuel d’un élément ne sont nécessaires que pour les types de fichiers qui incluent l’entrée [IsShortCut](./links.md) .

## <a name="predefined-shell-objects"></a>Objets Shell prédéfinis

L’interpréteur de commandes définit des objets supplémentaires sous la **\_ \_ racine HKEY classes** qui peuvent être étendus de la même façon que les types de fichiers. Par exemple, pour ajouter un gestionnaire de feuille de propriétés pour tous les fichiers, vous pouvez vous inscrire sous la sous-clé **PropertySheetHandlers** .

```
HKEY_CLASSES_ROOT
   *
      shellex
         PropertySheetHandlers
```

Le tableau suivant indique les différentes sous-clés de la **\_ \_ racine de la classe HKEY** sous lesquelles les gestionnaires d’extension peuvent être inscrits. Notez que de nombreux gestionnaires d’extension ne peuvent pas être enregistrés sous toutes les sous-clés répertoriées. Pour plus d’informations, consultez la documentation du gestionnaire spécifique.



| Sous-clé                    | Description                                                          | Gestionnaires possibles                                |
|---------------------------|----------------------------------------------------------------------|--------------------------------------------------|
| **\***                    | Tous les fichiers                                                            | Menu contextuel, feuille de propriétés, verbes (voir ci-dessous) |
| **AllFileSystemObjects**  | Tous les fichiers et dossiers de fichiers                                           | Menu contextuel, feuille de propriétés, verbes             |
| **Folder**                | Tous les dossiers                                                          | Menu contextuel, feuille de propriétés, verbes             |
| **Directory**             | Dossiers de fichiers                                                         | Menu contextuel, feuille de propriétés, verbes             |
| **\\Arrière-plan du répertoire** | Arrière-plan du dossier de fichiers                                               | Menu contextuel uniquement                               |
| **DesktopBackground**     | arrière-plan du bureau (Windows 7 et versions ultérieures)                            | Menu contextuel, verbes                             |
| **Lecteur**                 | Tous les lecteurs dans MyComputer, tels que « C : \\ »                             | Menu contextuel, feuille de propriétés, verbes             |
| **Réseau**               | Tout le réseau (sous Favoris réseau)                             | Menu contextuel, feuille de propriétés, verbes             |
| **Type de réseau \\\\\#**     | Tous les objets de type \# (voir ci-dessous)                                   | Menu contextuel, feuille de propriétés, verbes             |
| **NetShare**              | Tous les partages réseau                                                   | Menu contextuel, feuille de propriétés, verbes             |
| **Serveur netserver**             | Tous les serveurs réseau                                                  | Menu contextuel, feuille de propriétés, verbes             |
| *\_nom du fournisseur réseau \_* | Tous les objets fournis par le fournisseur réseau «*\_ \_ nom du fournisseur réseau*» | Menu contextuel, feuille de propriétés, verbes             |
| **Imprimantes**              | Toutes les imprimantes                                                         | Menu contextuel, feuille de propriétés                    |
| **AudioCD**               | CD audio dans le lecteur CD                                                 | Verbes uniquement                                       |
| **DVD**                   | lecteur de DVD (Windows 2000)                                             | Menu contextuel, feuille de propriétés, verbes             |



 

### <a name="notes"></a>Remarques

-   Le menu contextuel de l’arrière-plan du dossier de fichiers est accessible en cliquant avec le bouton droit dans un dossier de fichiers, mais pas sur le contenu du dossier.
-   Les « verbes » sont des commandes spéciales **inscrites sous le \_ \_** verbe de Shell de la \\ *sous-clé* de l' \\ **interpréteur** de commandes \\ .
-   Pour le type de **réseau** \\  \\ **\#** , « \# » est un code de type de fournisseur réseau au format décimal. Le code du type de fournisseur réseau est le mot de poids fort d’un type de réseau. La liste des types de réseau est fournie dans le fichier d’en-tête Winnetwk. h ( \_ valeurs net WNNC \_ \* ). Par exemple, WNNC \_ NET \_ Shiva est 0x00330000. par conséquent, la sous-clé de type correspondante serait de type **HKEY \_ classes \_ racine** de \\  \\ **type** \\ **51**.
-   «*\_ \_ nom du fournisseur réseau*» est un nom de fournisseur réseau spécifié par [**WNetGetProviderName**](/windows/win32/api/winnetwk/nf-winnetwk-wnetgetprovidernamea), avec les espaces convertis en traits de soulignement. par exemple, si le fournisseur réseau de réseau microsoft est installé, son nom de fournisseur est « microsoft Windows network » et le *\_ \_ nom du fournisseur réseau* correspondant est **Microsoft \_ Windows \_ réseau**.

## <a name="example-of-an-extension-handler-registration"></a>Exemple d’inscription d’un gestionnaire d’extensions

Pour activer un gestionnaire spécifique, créez une sous-clé sous la sous-clé de type de gestionnaire d’extension avec le nom du gestionnaire. L’interpréteur de commandes n’utilise pas le nom du gestionnaire, mais il doit être différent de tous les autres noms sous cette sous-clé de type. Définissez la valeur par défaut de la sous-clé Name sur la forme de chaîne du GUID du gestionnaire.

L’exemple suivant illustre les entrées de Registre qui activent les gestionnaires d’extensions de menu contextuel et de feuille de propriétés, à l’aide d’un exemple de type de fichier. MYP.

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   CLSID
      {00000000-1111-2222-3333-444444444444}
         InProcServer32
            (Default) = C:\MyDir\MyCommand.dll
            ThreadingModel = Apartment
      {11111111-2222-3333-4444-555555555555}
         InProcServer32
            (Default) = C:\MyDir\MyPropSheet.dll
            ThreadingModel = Apartment
   MyProgram.1
      (Default) = MyProgram Application
      Shellex
         ContextMenuHandler
            MyCommand
               (Default) = {00000000-1111-2222-3333-444444444444}
         PropertySheetHandlers
            MyPropSheet
               (Default) = {11111111-2222-3333-4444-555555555555}
```

### <a name="registering-shell-extension-handlers"></a>Inscription des gestionnaires d’extensions de Shell

la procédure d’inscription décrite dans cette section doit être suivie pour tous les systèmes de Windows. Toutefois, avec les systèmes ultérieurs, une étape supplémentaire peut être nécessaire. étant donné que ces versions ultérieures de Windows sont conçues pour être utilisées dans un environnement géré, l’accès au registre peut être limité administrativement, ce qui nécessite une approche quelque peu différente de celle décrite dans la section précédente.

> [!Note]  
> Les programmes d’installation ne doivent généralement pas écrire directement dans le registre. au lieu de cela, le programme d’installation doit être effectué avec Windows Installer packages. Ces outils garantissent que les logiciels s’exécutent correctement et fournissent un accès à des fonctionnalités telles que l’inscription de classe par utilisateur.

 

Les gestionnaires d’extensions de Shell s’exécutent dans le processus de Shell. Étant donné qu’il s’agit d’un processus système, l’administrateur d’un système peut limiter les gestionnaires d’extension d’environnement à ceux d’une liste approuvée en définissant la valeur EnforceShellExtensionSecurity de la clé de l' **Explorateur** sur 1 comme indiqué ici :

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Policies
                  Explorer
                     EnforceShellExtensionSecurity = 1
```

Pour placer un gestionnaire d’extensions de Shell dans la liste approuvée, créez une valeur **reg \_ SZ** dont le nom correspond à la chaîne du GUID du gestionnaire sous la sous-clé **approuvée** .

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Shell Extensions
                  Approved
```

Par exemple, l’exemple suivant ajoute les gestionnaires *myCommand* et *MyPropSheet* à la liste approuvée.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Shell Extensions
                  Approved
                     {00000000-1111-2222-3333-444444444444} = MyCommand
                     {11111111-2222-3333-4444-555555555555} = MyPropSheet
```

L’interpréteur de commandes n’utilise pas la valeur qui est assignée au GUID, mais il doit être configuré pour faciliter l’inspection du Registre.

Votre application de configuration peut ajouter des valeurs à la sous-clé **approuvée** uniquement si la personne qui installe l’application dispose de privilèges suffisants. Si la tentative d’ajout d’un gestionnaire d’extensions échoue, vous devez informer l’utilisateur que des privilèges d’administrateur sont nécessaires pour installer complètement l’application. Si le gestionnaire est essentiel pour l’application, vous devez faire échouer le programme d’installation et demander à l’utilisateur de contacter un administrateur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Initialisation des gestionnaires d’extensions de Shell](int-shell-exts.md)
</dt> </dl>

 

 
