---
description: ICE90 publie un avertissement s’il détecte que le répertoire d’un raccourci a été spécifié en tant que propriété publique.
ms.assetid: 47565d9b-c3c2-4a5c-8f91-2b3912a63b47
title: ICE90
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7b4063d06aa5a0a8688e2a411040d4b64f58f75
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021461"
---
# <a name="ice90"></a>ICE90

ICE90 publie un avertissement s’il détecte que le répertoire d’un raccourci a été spécifié en tant que propriété publique. Les noms des [propriétés publiques](public-properties.md) sont écrits en lettres majuscules. Un raccourci spécifié par une propriété publique peut ne pas fonctionner si la valeur de la propriété [**ALLUSERS**](allusers.md) change.

Cette action personnalisée ICE valide la table de raccourcis et utilise la table de répertoires. Si la table de répertoires n’est pas présente, elle retourne sans valider la table de raccourcis et ne publie aucune erreur ou avertissement.

## <a name="result"></a>Résultats

ICE90 publie l’avertissement suivant.



| Erreur ICE90                                                                                                                                                                                                                    | Description                                                     |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| Le raccourci' \[ 1 \] 'a un répertoire qui est une propriété publique (tout en majuscules) et se trouve sous le répertoire du profil utilisateur. Cela entraîne un problème si la valeur de la propriété [**ALLUSERS**](allusers.md) change dans la séquence d’interface utilisateur. | Le répertoire d’un raccourci a été spécifié en tant que propriété publique. |



 

## <a name="example"></a>Exemple

ICE90 signale l’avertissement suivant pour l’exemple :

``` syntax
The shortcut 'Shortcut1' has a directory that is a public property (ALL CAPS) 
and is under user profile directory. This results in a problem if the value 
of the ALLUSERS property changes in the UI sequence.
```

Dans cet exemple, MYDIR se trouve sous un profil Users. ICE90 publie un avertissement, car l’emplacement du répertoire cible est spécifié par une propriété publique, MYDIR. Un utilisateur peut modifier la propriété MYDIR ou [**ALLUSERS**](allusers.md) . Si **ALLUSERS** est défini pour le [contexte d’installation](installation-context.md)par ordinateur et que MYDIR se trouve sous un profil utilisateurs, le fichier de raccourci dans MYDIR est copié sous le profil « tous les utilisateurs », et non un profil utilisateur particulier. Si **ALLUSERS** est défini pour le contexte d’installation par utilisateur, le fichier de raccourci dans MYDIR est copié dans le profil d’un utilisateur particulier et n’est pas disponible pour les autres utilisateurs.

[Table de raccourcis](shortcut-table.md) (partielle)



| Raccourci  | Répertoire\_ |
|-----------|-------------|
| Shortcut1 | MYDIR       |



 

[Table de répertoires](directory-table.md) (partielle)



| Répertoire | Répertoire \_ parent |
|-----------|-------------------|
| MYDIR     | ProgramMenuFolder |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



