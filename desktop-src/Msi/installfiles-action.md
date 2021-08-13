---
description: L’action InstallFiles copie les fichiers spécifiés dans la table de fichiers du répertoire source vers le répertoire de destination.
ms.assetid: 187ad82f-13f5-4ea3-913c-2ae7561a6ee6
title: Action InstallFiles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8df2a62deb253314e84e72cd84e88052f1175db7451807c3f266542e29c10c7d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118629930"
---
# <a name="installfiles-action"></a>Action InstallFiles

L’action InstallFiles copie les fichiers spécifiés dans la table de fichiers du répertoire source vers le répertoire de destination.

## <a name="sequence-restrictions"></a>Restrictions de séquence

L’action InstallFiles doit venir après l’action [InstallValidate](installvalidate-action.md) et avant toute action dépendante d’un fichier.

## <a name="actiondata-messages"></a>Messages ActionData



| Champ | Description des données d’action                      |
|-------|-------------------------------------------------|
| \[1\] | Identificateur du fichier installé.                   |
| \[6\] | Taille du fichier installé en octets.                |
| \[9\] | Identificateur du répertoire contenant le fichier installé. |



 

## <a name="remarks"></a>Remarques

L’action InstallFiles opère sur les fichiers spécifiés dans la [table de fichiers](file-table.md). Chaque fichier est installé en fonction de l’état d’installation du composant associé du fichier dans la [table des composants](component-table.md). Seuls les fichiers dont les composants sont résolus à l’état **msiInstallStatelocal** peuvent être copiés.

L’action InstallFiles implémente les colonnes suivantes de la table de fichiers.

-   La colonne FileName spécifie le nom du fichier cible.
-   La colonne version spécifie la version du fichier.
-   La colonne attributs spécifie les bits d’indicateur d’attribut de fichier et d’installation.
-   La colonne file spécifie le jeton de fichier unique.
-   La colonne FileSize spécifie la taille du fichier non compressé en octets.
-   La colonne Language spécifie l’identificateur de langue du fichier.
-   La colonne Sequence spécifie le numéro de séquence sur le support.

L’action InstallFiles implémente les colonnes suivantes de la table des composants.

-   La \_ colonne Directory spécifie une référence à un élément de [table de répertoire](directory-table.md) .
-   La colonne composant spécifie un nom unique pour l’élément de composant.

Le fichier spécifié est copié uniquement si l’une des conditions suivantes est vraie :

-   Le fichier n’est pas installé actuellement sur l’ordinateur local.
-   Le fichier se trouve sur l’ordinateur local, mais son numéro de version est inférieur à celui du fichier figurant dans la [table de fichiers](file-table.md).
-   Le fichier se trouve sur l’ordinateur local, mais il n’y a aucun numéro de version associé.

Le répertoire source de chaque fichier à copier est déterminé par le sourceMode, qui à son tour dépend de la valeur dans la colonne Cabinet de la table multimédia. Pour une présentation complète du mode Source, consultez la [table Media](media-table.md).

Si le répertoire source d’un fichier à copier réside sur un support amovible, tel qu’une disquette ou un CD-ROM, l’action InstallFiles vérifie que le média source approprié est inséré avant de tenter de copier le fichier. InstallFiles recherche des médias du même type amovible avec un nom de [*volume*](v-gly.md) qui correspond à la valeur spécifiée dans la colonne VolumeLabel de la table multimédia. Si un volume monté correspondant est trouvé, le processus de copie de fichiers se poursuit. Si aucune correspondance n’est trouvée, une boîte de dialogue demande à l’utilisateur d’insérer le média approprié. Dans ce cas, la boîte de dialogue utilise le nom du support trouvé dans la colonne DiskPrompt de la table Media dans le cadre de l’invite.

ATTENTION : l’action InstallFiles peut supprimer un fichier d’origine sans le remplacer. Cela se produit lorsque l’action InstallFiles rencontre une erreur lors du remplacement d’un fichier plus ancien et que l’utilisateur choisit d’ignorer l’erreur. Le comportement par défaut du programme d’installation consiste à supprimer un ancien fichier avant de vous assurer que le nouveau fichier est correctement copié.

Pour connaître les règles de contrôle de version des fichiers utilisées par le programme d’installation, consultez règles de contrôle de [version de fichier](file-versioning-rules.md).

 

 



