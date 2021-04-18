---
description: Personnalisation de l’apparence et du comportement d’un dossier individuel avec Desktop.ini.
ms.assetid: 0361b7da-bfb3-4880-b982-85d2fe419805
title: Comment personnaliser des dossiers avec Desktop.ini
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eaac3e6a96257e63b5e4210da0aa6e6e1db77eaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104560697"
---
# <a name="how-to-customize-folders-with-desktopini"></a>Comment personnaliser des dossiers avec Desktop.ini

Les dossiers du système de fichiers sont généralement affichés avec une icône standard et un ensemble de propriétés, qui spécifient, par exemple, si le dossier est partagé. Vous pouvez personnaliser l’apparence et le comportement d’un dossier individuel en créant un fichier Desktop.ini pour ce dossier.

## <a name="instructions"></a>Instructions

### <a name="using-desktopini-files"></a>Utilisation de fichiers Desktop.ini

Les dossiers s’affichent normalement avec l’icône de dossier standard. Le fichier Desktop.ini est couramment utilisé pour assigner une icône ou une image miniature personnalisée à un dossier. Vous pouvez également utiliser Desktop.ini pour créer une *info-bulle* qui affiche des informations sur le dossier et contrôle certains aspects du comportement du dossier, par exemple la spécification de noms localisés pour le ou les éléments du dossier.

**Utilisez la procédure suivante pour personnaliser le style d’un dossier avec Desktop.ini :**

1.  Utilisez [**PathMakeSystemFolder**](/windows/desktop/api/Shlwapi/nf-shlwapi-pathmakesystemfoldera) pour transformer le dossier en dossier système. Cela définit le bit en lecture seule sur le dossier pour indiquer que le comportement spécial réservé à Desktop.ini doit être activé. Vous pouvez également créer un dossier système à partir de la ligne de commande à l’aide d' **Attrib + s** *NomDossier*.
2.  Créez un fichier de Desktop.ini pour le dossier. Vous devez le marquer comme étant *masqué* et *système* pour vous assurer qu’il est masqué pour les utilisateurs normaux.
3.  Assurez-vous que le fichier de Desktop.ini que vous créez est au format Unicode. Cela est nécessaire pour stocker les chaînes localisées qui peuvent être affichées aux utilisateurs.

### <a name="creating-a-desktopini-file"></a>Création d’un fichier de Desktop.ini

Le fichier Desktop.ini est un fichier texte qui vous permet de spécifier le mode d’affichage d’un dossier de système de fichiers. \[. \]La section ShellClassInfo vous permet de personnaliser l’affichage du dossier en affectant des valeurs à plusieurs entrées :

|                   |                                                                                                                                                                                                                                                                                                                                                                                |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Entrée**         | **Valeur**                                                                                                                                                                                                                                                                                                                                                                      |
| **ConfirmFileOp** | Affectez la valeur 0 à cette entrée pour éviter l’avertissement « vous supprimez un dossier système » lors de la suppression ou du déplacement du dossier.                                                                                                                                                                                                                                                                  |
| **Nopartage**     | Non pris en charge sous Windows Vista ou version ultérieure. Définissez cette entrée sur 1 pour empêcher le partage du dossier.                                                                                                                                                                                                                                                                       |
| **IconFile**      | Si vous souhaitez spécifier une icône personnalisée pour le dossier, définissez cette entrée sur le nom de fichier de l’icône. L’extension de nom de fichier. ico est préférable, mais il est également possible de spécifier des fichiers. bmp ou. exe et. dll qui contiennent des icônes. Si vous utilisez un chemin d’accès relatif, l’icône est disponible pour les personnes qui consultent le dossier sur le réseau. Vous devez également définir l’entrée **IndexIcône** . |
| **IndexIcône**     | Définissez cette entrée pour spécifier l’index d’une icône personnalisée. Si le fichier affecté à **IconFile** ne contient qu’une seule icône, définissez **IndexIcône** sur 0.                                                                                                                                                                                                                               |
| **InfoTip**       | Définissez cette entrée sur une chaîne de texte informatif. Elle s’affiche sous la forme d’une info-bulle lorsque le curseur pointe sur le dossier. Si l’utilisateur clique sur le dossier, le texte d’information s’affiche dans le bloc d’informations du dossier, sous les informations standard.                                                                                                                      |



 

Les illustrations suivantes sont du dossier Music avec un fichier de Desktop.ini personnalisé. Le dossier maintenant :

-   A une icône personnalisée.
-   N’affiche pas d’avertissement « vous supprimez un dossier système » si le dossier est déplacé ou supprimé.
-   Ne peut pas être partagé.
-   Affiche du texte informatif lorsque le curseur pointe sur le dossier.

Les options des dossiers dans les illustrations suivantes sont définies pour afficher les fichiers masqués afin que Desktop.ini soit visible. Le dossier se présente comme suit :

![capture d’écran du dossier avec icône personnalisée](images/webview4.jpg)

Quand le curseur pointe sur le dossier, l’info-bulle s’affiche.

![capture d’écran d’un dossier avec une info-bulle](images/webview6.jpg)

L’icône personnalisée remplace l’icône de dossier partout où le nom du dossier s’affiche.

![capture d’écran de l’icône personnalisée qui remplace l’icône de dossier](images/webview5.jpg)

Le fichier desktop.ini suivant a été utilisé pour personnaliser le dossier musique, comme indiqué dans les illustrations précédentes.


```
[.ShellClassInfo]
ConfirmFileOp=0
NoSharing=1
IconFile=Folder.ico
IconIndex=0
InfoTip=Some sensible information.
```



 

 



