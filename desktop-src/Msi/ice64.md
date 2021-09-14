---
description: ICE64 vérifie que les nouveaux répertoires du profil utilisateur sont correctement supprimés dans les scénarios d’itinérance.
ms.assetid: d878bf4a-33c4-4c68-bd74-b7884d6680a5
title: ICE64
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d103498a56bea26415f4f841d5ec78b5dfe370f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021514"
---
# <a name="ice64"></a>ICE64

ICE64 vérifie que les nouveaux répertoires du profil utilisateur sont correctement supprimés dans les scénarios d’itinérance.

Si vous ne corrigez pas un avertissement ou une erreur signalée par ICE64, les problèmes surviennent généralement lors de la désinstallation de l’ordinateur. Lorsqu’un utilisateur itinérant qui a installé l’application se connecte à un ordinateur pour la première fois, tout le profil est copié sur l’ordinateur. Sur la publication (qui a lieu après le téléchargement du profil itinérant), le programme d’installation vérifie que le répertoire existe déjà et, par conséquent, ne le supprime pas lors de la désinstallation. Cela laisse le répertoire sur l’ordinateur de l’utilisateur de façon permanente.

## <a name="result"></a>Résultats

ICE64 publie un avertissement ou une erreur dans une situation d’itinérance si un nouveau répertoire du profil utilisateur à supprimer n’est pas supprimé.

## <a name="example"></a>Exemple

ICE64 signale l’erreur suivante pour l’exemple indiqué.

``` syntax
The directory 'MyOtherFolder' is in the user profile but is not listed in the RemoveFile table.
```

Le dossier « MyOtherFolder » est un dossier de profil personnalisé. Comme il n’est pas listé dans la table RemoveFile, il n’est pas supprimé dans certains scénarios.

Pour corriger cette erreur, créez une ligne pour le dossier dans la table RemoveFile.

[Table de répertoire](directory-table.md)



| Répertoire     | Répertoire \_ parent | DefaultDir  |
|---------------|-------------------|-------------|
| AppDataFolder | TARGETDIR         |             |
| Mondossier      | AppDataFolder     | DataFolder  |
| MyOtherFolder | AppDataFolder     | DataFolder2 |



 

[Table RemoveFile](removefile-table.md)



| FileKey | Composant\_ | FileName | DirProperty | InstallMode |
|---------|-------------|----------|-------------|-------------|
| Clé1    | Composant1  |          | Mondossier    | 2           |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



