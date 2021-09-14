---
description: ICE60 valide la table de fichiers d’une base de données Windows Installer.
ms.assetid: 95d9b8b4-0b65-451a-8629-f0b276d6e35d
title: ICE60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e26c6f296fd514f582a699a5f839a7e145169e3e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021523"
---
# <a name="ice60"></a>ICE60

ICE60 vérifie que les fichiers de la [table de fichiers](file-table.md) remplissent les conditions suivantes :

-   Si le fichier n’est pas une police et a une version, il doit avoir une langue.
-   ICE60 vérifie qu’aucun fichier avec version n’est répertorié dans la [table MsiFileHash](msifilehash-table.md).

Si vous ne corrigez pas un avertissement signalé par ICE60, il est généralement possible de réinstaller un fichier en cas de réparation d’un produit. Cela est dû au fait que le fichier à installer dans la réparation et le fichier existant sur le disque ont la même version (il s’agit du même fichier) mais des langues différentes. La table file indique la langue comme étant null, mais le fichier lui-même a une valeur Language dans la ressource. En fonction des [règles](file-versioning-rules.md)de contrôle de version des fichiers, le programme d’installation privilégie le fichier à installer, de sorte qu’il est recopié inutilement.

## <a name="result"></a>Résultats

ICE60 publie un avertissement ou une erreur si un fichier de la [table de fichiers](file-table.md) qui n’est pas une police et a une version n’a pas de langue.

ICE60 publie l’erreur suivante si la version d’un fichier figurant dans la table MsiFileHash est gérée.

``` syntax
ERROR: "The file [1] is Versioned. It cannot be hashed"
```

## <a name="example"></a>Exemple

ICE60 signale l’erreur et l’avertissement suivants pour l’exemple indiqué. (Le fichier B est une police ; les autres fichiers ne le sont pas.)

``` syntax
WARNING: The file FileE is not a Font, and its version is not a companion file reference. It should have a language specified in the Language column.
```

Filea a une version et une langue ; par conséquent, aucun avertissement ou erreur n’est généré.

FileB a une version, mais pas de langue. Toutefois, aucun avertissement ou erreur n’est généré, car il s’agit d’une police.

FileC est une référence complémentaire, il n’est donc pas nécessaire de disposer d’un langage. Aucun avertissement ou erreur n’est généré.

Le dépôt n’a pas de version, il n’est donc pas nécessaire de disposer d’une langue. Aucun avertissement ou erreur n’est généré.

La version de fichier est sans langue. Par conséquent, un avertissement est généré.

Pour résoudre cet avertissement, ajoutez une langue à fichier.

Chaque fois que cela est possible, les fichiers doivent avoir des valeurs de langue stockées dans la ressource de version. Si un fichier est indépendant de la langue, utilisez l' [ID](column-data-types.md) de langue 0.

[Table de fichiers](file-table.md) (fileB est une police ; les autres fichiers ne sont pas.)



| Fichier  | Version | Langage |
|-------|---------|----------|
| Filea | 1.0     | 1033     |
| FileB | 1.0     |          |
| FileC | Filea   |          |
| Classer |         |          |
| Fichier | 1.0     |          |



 

[Tableau des polices](font-table.md)



| Fichier  | FontTitle  |
|-------|------------|
| FileB | Titre de la police |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



