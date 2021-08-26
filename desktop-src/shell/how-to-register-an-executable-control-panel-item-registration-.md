---
description: Pour les éléments du panneau de configuration qui sont implémentés en tant que fichiers .exe, aucune exportation ou gestion de messages spéciale n’est requise. Tout fichier de .exe peut être enregistré en tant qu’objet de commande pour s’afficher avec un point d’entrée dans le dossier du panneau de configuration.
title: Comment inscrire des éléments du panneau de configuration exécutables
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b81e52e18bd2cd1c48d5d260b08844784a5286dd2cd4d9d5ec782a86f624fc42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120009429"
---
# <a name="how-to-register-executable-control-panel-items"></a>Comment inscrire des éléments du panneau de configuration exécutables

Pour les éléments du panneau de configuration qui sont implémentés en tant que fichiers .exe, aucune exportation ou gestion de messages spéciale n’est requise. Tout fichier de .exe peut être enregistré en tant qu’objet de commande pour s’afficher avec un point d’entrée dans le dossier du panneau de configuration.

Un exemple est utilisé ici pour illustrer les exigences d’inscription. l’exemple montre comment inscrire un élément du panneau de configuration appelé **My Paramètres** en tant qu’objet de commande afin qu’il apparaisse dans la fenêtre du panneau de configuration. la fenêtre **mes Paramètres** s’affiche également lorsque la commande `MyApp.exe /settings` est exécutée.

## <a name="instructions"></a>Instructions

### <a name="step-1"></a>Étape 1 :

Générez un GUID pour l’élément du panneau de configuration. Le GUID identifie de façon unique l’élément du panneau de configuration. Dans cet exemple, `{0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}` est le GUID de l’élément du panneau de configuration.

### <a name="step-2"></a>Étape 2 :

En utilisant le GUID comme nom, ajoutez une sous-clé au registre comme suit.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  ControlPanel
                     NameSpace
                        {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
                           (Default) = My Settings
```

Les données de l’entrée par défaut sont simplement le \_ nom de la reg SZ de l’élément du panneau de configuration. L’entrée par défaut peut être utile pour identifier l’entrée GUID, mais elle est facultative.

### <a name="step-3"></a>Étape 3 :

En utilisant le GUID comme nom, ajoutez une sous-clé et ses entrées au registre comme suit.

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         (Default) = My Settings
         LocalizedString = @%ProgramFiles%\MyCorp\MyApp.exe,-9
         InfoTip = @%ProgramFiles%\MyCorp\MyApp.exe,-5
         System.ApplicationName = MyCorporation.MySettings
         System.ControlPanel.Category = 1,8
         System.Software.TasksFileUrl = %ProgramFiles%\MyCorp\MyApp\MyTaskLinks.xml
```

-   **Par défaut**. PRIX \_ SZ Nom complet de l’élément du panneau de configuration.
-   **LocalizedString**. Facultatif. REG \_ SZ ou reg \_ expand \_ sz. Nom du module et ID de la table de chaînes du nom localisé de l’élément du panneau de configuration. le format est un signe « at » (@) suivi du nom de l' .exe ou .dll qui contient la table de chaînes interface utilisateur multilingue (MUI). Les variables d’environnement peuvent être utilisées comme substituts pour une partie du chemin d’accès. Le chemin d’accès et le nom de fichier sont suivis d’une virgule (,) et d’un trait d’Union (-), suivi de l’ID dans la table de chaînes.

    Si le module n’a pas de table de chaînes, cette entrée peut simplement être la chaîne de nom complet. Si vous utilisez uniquement la chaîne de nom complet plutôt qu’une table de chaînes, le nom ne s’ajuste pas à la langue d’affichage actuelle.

-   **Info-bulle**. REG \_ SZ ou reg \_ expand \_ sz. Description de l’élément du panneau de configuration. Ces informations sont affichées dans une info-bulle qui s’affiche lorsque la souris pointe sur l’icône de l’élément. La syntaxe est la même que celle utilisée pour LocalizedString, y compris la possibilité de fournir simplement une chaîne plutôt qu’une référence de table de chaînes.
-   **System. ApplicationName**. PRIX \_ SZ Nom canonique de l'élément. La commande de formulaire `control.exe /name System.ApplicationName` ouvre l’élément, par exemple `control.exe /name MyCorporation.MySettings` . Pour plus d’informations sur l’utilisation de Control.exe, consultez [exécution des éléments du panneau de configuration](executing-control-panel-items.md) .
-   **System. ControlPanel. Category**. PRIX \_ SZ Valeur qui déclare les catégories du panneau de configuration où l’élément apparaît. Plusieurs catégories sont séparées par des virgules. dans le cas de l’exemple ci-dessus, l’entrée indique que l’élément **My Paramètres** doit apparaître dans les catégories **apparence et personnalisation** et **programmes** . Consultez [assignation de catégories du panneau de configuration](assigning-control-panel-categories.md) pour connaître les valeurs de catégorie possibles.
-   **System. Software. TasksFileUrl**. REG \_ SZ ou reg \_ expand \_ sz. Chemin d’accès du fichier XML qui définit les [liens de tâche](creating-searchable-task-links.md). Il peut s’agir d’un chemin d’accès direct à un fichier, comme indiqué dans l’exemple, ou d’une ressource incorporée spécifiée comme nom de module et ID de ressource, par exemple « % ProgramFiles% \\ champ MyCorp \\ MyApp \\MyApp.exe,-31 ».

### <a name="step-4"></a>Étape 4 :

Sous la même sous-clé GUID, ajoutez la sous-clé suivante au registre pour fournir le chemin d’accès du fichier qui contient l’icône et l’ID de ressource de l’image dans ce fichier.

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         DefaultIcon
            (Default) = %ProgramFiles%\MyCorp\MyApp.exe,-2
```

Notez que, bien que la syntaxe soit similaire aux entrées LocalizedString et info-bulle présentées précédemment, aucun caractère « @ » n’est utilisé comme préfixe dans l' \_ entrée reg SZ ou reg \_ expand \_ SZ qui spécifie le chemin d’accès.

### <a name="step-5"></a>Étape 5 :

Ajoutez les informations suivantes au registre pour fournir la commande appelée par le système lorsque l’utilisateur ouvre le panneau de configuration.

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         Shell
            Open
               Command
                  (Default) = [REG_EXPAND_SZ] %ProgramFiles%\MyCorp\MyApp.exe /Settings
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Inscription des éléments du panneau de configuration](registering-control-panel-items.md)
</dt> <dt>

[Comment inscrire les éléments du panneau de configuration de la DLL](how-to-register-dll-control-panel-item-registration-.md)
</dt> </dl>

 

 



