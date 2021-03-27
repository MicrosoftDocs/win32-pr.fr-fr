---
description: La racine d’une extension d’espace de noms est normalement affichée par l’Explorateur Windows comme un dossier dans les vues d’arborescence et de dossier.
title: Spécification de l’emplacement d’une extension d’espace de noms
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 2c1fdd5d-b359-4d5c-a20e-0622f3a1cb1d
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 7617c7361c5f2ae76331c5f1b59eb845f6806395
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866161"
---
# <a name="specifying-a-namespace-extensions-location"></a>Spécification de l’emplacement d’une extension d’espace de noms

La racine d’une extension d’espace de noms est normalement affichée par l’Explorateur Windows comme un dossier dans les vues d’arborescence et de dossier. Pour que l’Explorateur Windows affiche les fichiers et les sous-dossiers de votre extension, vous devez spécifier l’emplacement du dossier racine dans la hiérarchie d’espace de noms de l’interpréteur de commandes. Cet emplacement est désigné sous le terme de *point de jonction*.

-   [Utilisation de dossiers virtuels comme points de jonction](#using-virtual-folders-as-junction-points)
-   [Utilisation des dossiers du système de fichiers en tant que points de jonction](#using-file-system-folders-as-junction-points)
-   [Ouverture d’une vue d’une extension d’espace de noms](#opening-a-view-of-a-namespace-extension)

## <a name="using-virtual-folders-as-junction-points"></a>Utilisation de dossiers virtuels comme points de jonction

La façon la plus simple de définir le point de jonction d’une extension consiste à faire du dossier racine un sous-dossier d’un dossier virtuel système. Ce type de point de jonction est désigné sous le terme de *point de jonction virtuel*. Les dossiers **Bureau** et **poste de travail** sont les emplacements typiques des points de jonction virtuels, mais vous pouvez également définir un point de jonction virtuel sur un ordinateur distant ou sous les dossiers favoris **réseau**, **Internet Explorer** et **panneau de configuration** .

Pour définir un point de jonction virtuel, créez une sous-clé de la clé qui représente le dossier virtuel approprié et nommez-la avec la chaîne de l’identificateur de classe (CLSID) de l’extension. Le CLSID inscrit s’affiche comme suit.

```
HKEY_LOCAL_MACHINE or HKEY_CURRENT_USER
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  Virtual Folder Name
                     NameSpace
                        {Extension CLSID}
                           (Default) = Junction Point Name
```

Le *nom du dossier virtuel* est l’une des sous-clés du tableau suivant.



| Emplacement          | Nom du dossier virtuel                        |
|-------------------|--------------------------------------------|
| Control panel     | **ControlPanel**                           |
| Bureau           | **Bureau**                                |
| Réseau entier    | **NetworkNeighborhood** \\ **EntireNetwork** |
| Poste de travail       | **MyComputer**                             |
| Favoris réseau | **NetworkNeighborhood**                    |
| Ordinateur distant   | **Ordinateur_distant**                         |
| Fichiers utilisateurs       | **UsersFiles**                             |



 

Les extensions distantes doivent être initialisées avec [**IRemoteComputer**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iremotecomputer).

## <a name="using-file-system-folders-as-junction-points"></a>Utilisation des dossiers du système de fichiers en tant que points de jonction

Il existe deux façons de définir des dossiers de système de fichiers en tant que points de jonction. L’approche la plus simple consiste à créer un dossier à l’emplacement approprié et à ajouter un point au nom du dossier, suivi du format de chaîne du CLSID de votre extension. Seul le nom du dossier sera visible dans l’Explorateur Windows. L’exemple suivant crée un point de jonction avec un nom d’affichage de mondossier.


```
MyFolder.{Extension CLSID}
```



Vous pouvez également définir un dossier nommé de façon conventionnelle comme point de jonction en :

-   Définition du dossier en lecture seule.
-   Création du dossier dans un dossier système en appelant [**PathMakeSystemFolder**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera).
-   Placer un fichier Desktop.ini masqué dans le dossier qui comprend le CLSID de l’extension.

Desktop.ini est un fichier texte standard qui peut être ajouté à n’importe quel dossier pour personnaliser certains aspects du comportement du dossier. Pour une présentation générale de l’utilisation de ce fichier, consultez [Comment personnaliser des dossiers avec Desktop.ini](how-to-customize-folders-with-desktop-ini.md). Pour définir un dossier comme point de jonction, le \[ . \] La section ShellClassInfo de Desktop.ini doit contenir le CLSID de l’extension, comme suit :


```
[.ShellClassInfo]
CLSID={Extension CLSID}
```



## <a name="opening-a-view-of-a-namespace-extension"></a>Ouverture d’une vue d’une extension d’espace de noms

Quand un utilisateur accède à un point de jonction, l’Explorateur Windows crée automatiquement une vue du dossier racine. Vous pouvez également créer une vue en lançant explicitement Explorer.exe avec le CLSID de l’extension comme argument. Vous pouvez, par exemple, utiliser cette approche pour lancer une vue d’une extension à partir d’un menu contextuel ou d’un raccourci. Par exemple, pour lancer une vue de MyExtension qui comprend une arborescence, vous pouvez utiliser la chaîne de commande suivante.


```
%SystemRoot%\Explorer.exe /e,::{MyExtension CLSID}
```



Une autre chaîne de commande peut être utilisée pour lancer une vue d’un objet dans l’extension. Cette fonctionnalité est utile, par exemple, pour une extension qui utilise un affichage des dossiers pour permettre aux utilisateurs d’afficher le contenu de l’un des nombreux fichiers compressés.


```
%SystemRoot%\Explorer.exe /e,::{MyExtension CLSID},objectname
```



Le paramètre *ObjectName* est le nom de l’objet qui doit être affiché. L’Explorateur Windows convertit le nom en PIDL correspondant et transmet le PIDL à la méthode [**IPersistFolder :: Initialize**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipersistfolder-initialize) de l’objet du nouveau dossier.

> [!Note]  
> La chaîne CLSID doit être précédée d’une paire de signes deux-points ( ::) Sinon, la commande échoue. L’indicateur barre oblique e (/e) utilisé dans les deux exemples de lignes de commande indiqué ci-dessus demande à l’Explorateur Windows d’afficher une arborescence. L’indicateur doit être séparé des deux signes deux-points par une virgule. Si vous ne souhaitez pas une arborescence, omettez l’indicateur/e et la virgule.

 

 

 



