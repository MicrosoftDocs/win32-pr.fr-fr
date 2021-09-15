---
description: Windows L’Explorateur contrôle la création d’un connecteur de recherche pour un gestionnaire de protocole par le biais d’entrées de clé de registre. par le biais du registre, les implémenteurs et les tiers peuvent permettre aux gestionnaires de protocoles nouveaux et hérités de participer à la recherche de Windows 7.
ms.assetid: 79abdcbc-ba60-43bd-9895-18ee8b6c5829
title: Création d’un connecteur de recherche pour un gestionnaire de protocole
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cec9c7830f61c0dcbf6682e6dfaea0feb30ebfa5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127313257"
---
# <a name="creating-a-search-connector-for-a-protocol-handler"></a>Création d’un connecteur de recherche pour un gestionnaire de protocole

Windows L’Explorateur contrôle la création d’un connecteur de recherche pour un gestionnaire de protocole par le biais d’entrées de clé de registre. par le biais du registre, les implémenteurs et les tiers peuvent permettre aux gestionnaires de protocoles nouveaux et hérités de participer à la recherche de Windows 7.

Cette rubrique est organisée comme suit :

-   [à propos des connecteurs de recherche pour les gestionnaires de protocole dans Windows 7](#about-search-connectors-for-protocol-handlers-in-windows-7)
-   [Activation des gestionnaires de protocole pour participer à la recherche](#enabling-protocol-handlers-to-participate-in-search)
    -   [Désactivation de la création du connecteur de recherche du gestionnaire de protocole](#disabling-protocol-handler-search-connector-creation)
    -   [Personnalisation du nom, de la description ou du FolderType pour un connecteur de recherche de gestionnaire de protocole](#customizing-the-name-description-or-foldertype-for-a-protocol-handler-search-connector)
    -   [Utilisation de la redirection de chaînes de Registre](#using-registry-string-redirection)
    -   [Restauration d’un connecteur de recherche supprimé du gestionnaire de protocole](#restoring-a-deleted-protocol-handler-search-connector)
-   [Ressources supplémentaires](#additional-resources)
-   [Rubriques connexes](#related-topics)

## <a name="about-search-connectors-for-protocol-handlers-in-windows-7"></a>à propos des connecteurs de recherche pour les gestionnaires de protocole dans Windows 7

dans Windows 7, les recherches à partir du menu **démarrer** ou de l’explorateur de Windows incluent uniquement les fichiers situés dans des emplacements indexés, et les éléments de système non-fichier tels que les magasins de données distants ou les éléments de gestionnaire de protocole qui ont un connecteur de recherche. En plus d’inclure les éléments du gestionnaire de protocole dans l’étendue du menu **Démarrer** et les recherches dans le shell, le connecteur de recherche permet au menu **Démarrer** de regrouper les éléments du gestionnaire de protocole dans les résultats du menu **Démarrer** , avec l’avantage qui en résulte que l’utilisateur peut cliquer sur l’en-tête de groupe et afficher les résultats uniquement à partir du gestionnaire de protocole. L’utilisateur peut également accéder au dossier **recherches** , ouvrir le fichier de connecteur de recherche et effectuer une recherche incluant uniquement les éléments du gestionnaire de protocole spécifique associé à ce connecteur de recherche.

lorsqu’un utilisateur démarre pour la première fois une application qui inscrit un gestionnaire de protocole, Windows Explorer génère un fichier de connecteur de recherche (. searchConnector-ms) pour le gestionnaire de protocole dans le dossier **recherches** de l’utilisateur. Les applications avec des gestionnaires de protocole peuvent choisir de désactiver ce comportement ou de personnaliser le nom et la description du connecteur de recherche du gestionnaire de protocole.

> [!Note]  
> L’emplacement du dossier **recherches** de l’utilisateur est% USERPROFILE% \\ recherches ou FOLDERID \_ SavedSearches. Le GUID de FOLDERID \_ SavedSearches est {7d1d3a04-debb-4115-95cf-2f29da2920da}.

 

Windows L’Explorateur contrôle la création d’un connecteur de recherche pour un gestionnaire de protocole via les entrées de clé de Registre décrites dans les sections suivantes :

-   [Activation des gestionnaires de protocole pour participer à la recherche](#enabling-protocol-handlers-to-participate-in-search)
-   [Désactivation de la création du connecteur de recherche du gestionnaire de protocole](#disabling-protocol-handler-search-connector-creation)
-   [Personnalisation du nom, de la description ou du FolderType pour un connecteur de recherche de gestionnaire de protocole](#customizing-the-name-description-or-foldertype-for-a-protocol-handler-search-connector)
-   [Restauration d’un connecteur de recherche supprimé du gestionnaire de protocole](#restoring-a-deleted-protocol-handler-search-connector)

> [!Note]  
> Il n’existe aucun moyen de créer un connecteur de recherche pour un gestionnaire de protocole. Ils doivent être configurés par le biais du Registre.

 

## <a name="enabling-protocol-handlers-to-participate-in-search"></a>Activation des gestionnaires de protocole pour participer à la recherche

Les clés de Registre et leurs valeurs possibles sont décrites dans le tableau suivant. Un gestionnaire de protocole peut remplir une partie ou l’ensemble de ces clés de registre où &lt; &gt; le protocole est remplacé par le nom réel de son protocole, par exemple MAPI, fichier ou CSC.



| Clé de Registre                                                                                                                 | Valeur (s) possible (s)                                                                                                                     | Type       | Commentaires                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Windows Search \\ \\ &lt; Version du protocole &gt; \\ PHSearchConnectors                     | N’existe pas (valeur par défaut). Dans le cas contraire, la valeur est supérieure ou égale à 1.                                                                               | \_valeur DWORD reg | Cette valeur est utilisée pour détecter les modifications apportées aux inscriptions de modèles d’emplacement pour les racines de recherche qui ont déjà été traitées. Si n’existe pas, utilisez 0 comme valeur par défaut. vous pouvez également incrémenter la version pour informer Windows Explorer que le connecteur de recherche doit être régénéré, car une version plus récente du gestionnaire de protocole a été installée. |
| HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Windows Search \\ PHSearchConnectors \\ &lt; protocol &gt; \\ DoNotCreateSearchConnectors | N’existe pas (valeur par défaut). Sinon, la valeur est 1.                                                                                         | \_valeur DWORD reg | S’il n’existe pas, créez un fichier. searchconnector-ms dans le dossier recherches. Si la valeur est 1, marquer comme traité et ne rien faire.                                                                                                                                                                                                                                   |
| HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Windows Search \\ PHSearchConnectors \\ &lt; protocol &gt; \\ Default \\ Description        | Chaîne localisable contenant la description du connecteur de recherche.                                                              | SZ de REG \_    | facultatif. Elle est utilisée dans l’élément Description du fichier. searchconnector-ms.                                                                                                                                                                                                                                                                          |
| HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Windows Search \\ PHSearchConnectors \\ &lt; &gt; \\ nom par défaut du protocole \\               | Chaîne localisée pour nommer le connecteur de recherche. Utilisé comme nom du fichier. searchconnector-ms.                                    | SZ de REG \_    | Chaque emplacement doit avoir un nom unique. En l’absence de cette valeur, le nom complet fourni par l' [interface IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) du gestionnaire de protocole est utilisé.                                                                                                                             |
| HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ Windows Search \\ PHSearchConnectors \\ &lt; protocole &gt; \\ par défaut \\ FolderType         | GUID identifiant le [FOLDERTYPEID](../shell/foldertypeid.md) à appliquer au connecteur de recherche. | SZ de REG \_    | Optionnel. Utilisé dans l’élément folderType du fichier. searchconnector-ms pour indiquer quels modèles doivent être utilisés pour afficher les résultats. Par exemple, la valeur GUID de \_ documents FOLDERTYPEID.                                                                                                                                                            |



 

### <a name="disabling-protocol-handler-search-connector-creation"></a>Désactivation de la création du connecteur de recherche du gestionnaire de protocole

si votre application expose des éléments via un gestionnaire de protocole pour une utilisation dans l’application elle-même et que vous ne souhaitez pas exposer les éléments par le biais de l’interpréteur de commandes (dans le menu **démarrer** et les recherches de l’explorateur de Windows), vous devez désactiver la création d’un connecteur de recherche pour votre gestionnaire de protocole.

Pour désactiver la création du connecteur de recherche, définissez DoNotCreateSearchConnectors sur 0x00000001 (1), comme indiqué dans l’exemple de clé de Registre suivant.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Search
            PHSearchConnectors
               <protocol>
                  DoNotCreateSearchConnectors
```

Si DoNotCreateSearchConnectors a la valeur 1, nous vous recommandons d’exposer la propriété [System. Shell. OmitFromView](/windows/desktop/properties/props-system-shell-omitfromview) sur chaque élément exposé par le gestionnaire de protocole et de définir la valeur de cette propriété sur **true**. Cela empêchera l’affichage des éléments du gestionnaire de protocole sous le groupe **fichiers** du menu **Démarrer** .

si DoNotCreateSearchConnectors est présent et défini à zéro, Windows Explorer crée un connecteur de recherche pour le gestionnaire de protocole et les éléments du gestionnaire de protocole sont retournés dans dans le menu **démarrer** et les recherches Windows Explorer.

### <a name="customizing-the-name-description-or-foldertype-for-a-protocol-handler-search-connector"></a>Personnalisation du nom, de la description ou du FolderType pour un connecteur de recherche de gestionnaire de protocole

Le nom du connecteur de recherche est utilisé non seulement pour identifier le connecteur de recherche dans le dossier **recherches** , mais comme en-tête de groupe pour les résultats dans les recherches dans le menu **Démarrer** . Par conséquent, il est important de fournir un nom descriptif pour le connecteur de recherche. si aucun nom n’est fourni dans la clé de registre, Windows Explorer utilise par défaut le nom fourni par l' [Interface IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) pour la racine de recherche du gestionnaire de protocole et une description vide. Vous pouvez remplacer le nom par défaut par une entrée de clé de registre sans avoir à renommer l’interface IShellFolder. Bien qu’il ne soit pas aussi visible que le nom du connecteur de recherche, vous pouvez également remplacer la description du connecteur de recherche en fournissant votre propre description.

Pour remplacer le nom ou la description par défaut, définissez les entrées comme indiqué dans l’exemple de Registre suivant.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Search
            PHSearchConnectors
               <protocol>
                  Default
                     Name
                     Description
```

En outre, l’entrée FolderType peut être définie sur l’un des GUID [FOLDERTYPEID](../shell/foldertypeid.md) . La valeur doit être le GUID réel et non son nom. par exemple, {94d6ddcc-4a68-4175-a374-bd584a510b78} au lieu de FOLDERTYPEID \_ Musique. le GUID d’un FOLDERTYPEID peut être obtenu dans le fichier d’en-tête Shlguid. h dans le [SDK Windows](https://msdn.microsoft.com/windowsvista/bb980924.aspx).

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Search
            PHSearchConnectors
               <protocol>
                  Default
                     FolderType = {94d6ddcc-4a68-4175-a374-bd584a510b78}
```

### <a name="using-registry-string-redirection"></a>Utilisation de la redirection de chaînes de Registre

Vous pouvez utiliser une [chaîne redirigée](../intl/using-registry-string-redirection.md) pour vous assurer que le nom que vous fournissez pour le connecteur de recherche peut être localisé. Vous pouvez inclure des chaînes localisables pour les clés de Registre Name et description au lieu d’entrer la chaîne réelle dans le registre.

Pour inclure une chaîne localisable pour les valeurs de nom ou de description, définissez la valeur comme indiqué dans l’exemple de clé de Registre suivant.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Search
            PHSearchConnectors
               <protocol>
                  Name = @dllname.dll,-resourceID
```

La chaîne localisable prend le format suivant :

-   @dllname.dll,-resourceID, où :
    -   @dllname.dll est le chemin d’accès à la DLL qui contient la ressource de type chaîne
    -   resourceID est l’ID de ressource entier de la ressource de type chaîne

Le format d’une chaîne indirecte, et une chaîne indirecte ajoutée avec un modificateur de version, est décrit dans la [fonction SHLoadIndirectString](/windows/win32/api/shlwapi/nf-shlwapi-shloadindirectstring).

### <a name="restoring-a-deleted-protocol-handler-search-connector"></a>Restauration d’un connecteur de recherche supprimé du gestionnaire de protocole

Étant donné que les connecteurs de recherche sont des fichiers sur l’ordinateur de l’utilisateur, ils peuvent être supprimés par erreur. Pour restaurer tous les connecteurs de recherche du gestionnaire de protocole supprimés, restaurez les bibliothèques par défaut. pour ce faire, ouvrez Windows Explorer, cliquez avec le bouton droit sur le dossier **bibliothèques** , puis sélectionnez **restaurer les bibliothèques par défaut**.

![capture d’écran montrant l’option de menu restaurer les bibliothèques par défaut](images/libraries.png)

## <a name="additional-resources"></a>Ressources supplémentaires

-   [IShellItem :: GetDisplayName](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname)
-   [SIGDN \_ NORMALDISPLAY](/windows/win32/api/shobjidl_core/ne-shobjidl_core-sigdn)

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Conceptuel**
</dt> <dt>

[Fonctionnement des gestionnaires de protocole](-search-3x-wds-extidx-prot-implementing.md)
</dt> <dt>

[Développement de gestionnaires de protocole](-search-3x-wds-phaddins.md)
</dt> <dt>

[Notification de l’index des modifications](-search-3x-wds-notifyingofchanges.md)
</dt> <dt>

[Ajout d’icônes et de menus contextuels](-search-3x-wds-ph-ui-extensions.md)
</dt> <dt>

[Exemple de code : extensions de Shell pour les gestionnaires de protocole](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[Installation et inscription de gestionnaires de protocole](-search-3x-wds-ph-install-registration.md)
</dt> <dt>

[Débogage de gestionnaires de protocole](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 
