---
description: Décrit les liens physiques et les jonctions.
ms.assetid: f9e40a86-a4a6-4524-8045-312da72dc655
title: Liens physiques et jonctions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b8d1444db977dd95419e4cb004d2b3cb811da9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106545092"
---
# <a name="hard-links-and-junctions"></a>Liens physiques et jonctions

Il existe trois types de liens de fichiers pris en charge dans le système de fichiers NTFS : les liens physiques, les jonctions et les liens symboliques. Cette rubrique est une vue d’ensemble des liens physiques et des jonctions. Pour plus d’informations sur les liens symboliques, consultez [création de liens symboliques](creating-symbolic-links.md).

## <a name="hard-links"></a>Liens physiques

Un *lien physique* est la représentation de système de fichiers d’un fichier par lequel plusieurs chemins d’accès font référence à un seul fichier dans le même volume. Pour créer un lien physique, utilisez la fonction [**CreateHardLink**](/windows/desktop/api/WinBase/nf-winbase-createhardlinka) . Toutes les modifications apportées à ce fichier sont instantanément visibles par les applications qui y accèdent via les liens physiques qui y font référence. Toutefois, la taille de l’entrée de répertoire et les informations d’attribut sont mises à jour uniquement pour le lien par le biais duquel la modification a été apportée. Notez que les attributs du fichier sont reflétés dans chaque lien physique vers ce fichier, et les modifications apportées aux attributs de ce fichier sont propagées à tous les liens physiques. Par exemple, si vous réinitialisez l’attribut READONLY sur un lien physique pour supprimer ce lien physique particulier, et qu’il y a plusieurs liens physiques vers le fichier réel, vous devrez réinitialiser le bit READONLY sur le fichier à partir de l’un des autres liens physiques pour ramener le fichier et tous les autres liens physiques à l’État READONLY.

Par exemple, dans un système où C : et D : sont des lecteurs locaux et Z : est un lecteur réseau mappé à \\ \\ Fred \\ share, les références suivantes sont autorisées en tant que lien physique :

-   C : \\ dira \\ethel.txt lié à c : \\ DIRB \\ DIRC \\lucy.txt
-   D : \\ dir1 \\tinker.txt à d : \\ dir2 \\ DirX \\bell.txt
-   C : \\ DirY \\ Bob. bak lié à c : \\ dir2 \\mina.txt

Les éléments suivants ne sont pas :

-   C : \\ dira lié à c : \\ DIRB
-   C : \\ dira \\ethel.txt lié à D : \\ DIRB \\lucy.txt
-   C : \\ dira \\ethel.txt lié à Z : \\ DIRB \\lucy.txt

Pour supprimer un lien physique, utilisez la fonction [**DeleteFile**](/windows/desktop/api/FileAPI/nf-fileapi-deletefilea) . Vous pouvez supprimer des liens physiques dans n’importe quel ordre, quel que soit l’ordre dans lequel ils sont créés.

## <a name="junctions"></a>Jonctions

Une *jonction* (également appelée *lien conditionnel*) diffère d’un lien physique dans la mesure où les objets de stockage qu’elle référencent sont des répertoires distincts et une jonction peut lier des répertoires situés sur des volumes locaux différents sur le même ordinateur. Dans le cas contraire, les jonctions fonctionnent de la même façon que les liens physiques. Les jonctions sont implémentées par le biais de [points d’analyse](reparse-points.md).

En supposant les mêmes conditions dans la section des liens physiques, les références suivantes sont autorisées en tant que jonctions :

-   C : \\ dira lié à c : \\ DIRB \\ DIRC
-   C : \\ DirX lié à D : \\ DirY

Les éléments suivants ne sont pas :

-   C : \\ dira \\one.txt lié à c : \\ DIRB \\two.txt
-   C : \\ dir1 lié à Z : \\ dir2

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Création de liens symboliques](creating-symbolic-links.md)
</dt> </dl>

 

 



