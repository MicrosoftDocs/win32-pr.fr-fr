---
description: Créez des liens symboliques qui utilisent un chemin d’accès absolu ou relatif à l’aide de la fonction CreateSymbolicLink.
ms.assetid: 3821478d-87bb-4e47-8263-d977cf665503
title: Création de liens symboliques
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c978532ffc11e44615d4de0ea902152438ecc7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320109"
---
# <a name="creating-symbolic-links"></a>Création de liens symboliques

La fonction [**CreateSymbolicLink**](/windows/desktop/api/WinBase/nf-winbase-createsymboliclinka) vous permet de créer des liens symboliques à l’aide d’un chemin d’accès absolu ou relatif.

Les liens symboliques peuvent être des liens absolus ou relatifs. Les liens absolus sont des liens qui spécifient chaque partie du nom de chemin d’accès ; les liens relatifs sont déterminés par rapport à l’emplacement relatif : les spécificateurs de lien se trouvent dans un chemin d’accès spécifié. Les liens relatifs sont spécifiés à l’aide des conventions suivantes :

-   Point (. et..) les conventions, par exemple, « .. \\ » résout le chemin d’accès relatif au répertoire parent.
-   Les noms sans barres obliques ( \) par exemple, « tmp » résout le chemin d’accès relatif au répertoire actif.
-   La racine relative, par exemple « \\ Windows \\ system32 », est résolue en «*lecteur actuel*: \\ Windows \\ system32 ». Répertoire
-   Répertoire de travail actuel-relatif : par exemple, si le répertoire de travail actuel est « C : \\ Windows \\ system32 », « C:File.txt » est résolu en « c : \\ Windows \\ system32 \\File.txt ».

    **Remarque**  Si vous spécifiez un lien relatif au répertoire de travail actif, il est créé en tant que lien absolu, en raison de la façon dont le répertoire de travail actuel est traité en fonction de l’utilisateur et du thread.

Un lien symbolique peut également contenir des points de jonction et des dossiers montés dans le cadre du nom du chemin d’accès.

Les liens symboliques peuvent pointer directement vers un fichier ou un répertoire distant à l’aide du chemin d’accès UNC.

Les liens symboliques relatifs sont limités à un seul volume.

## <a name="example-of-an-absolute-symbolic-link"></a>Exemple de lien symbolique absolu

Dans cet exemple, le chemin d’accès d’origine contient un composant, '*x*', qui est un lien symbolique absolu. Lorsque'*x*'est rencontré, le fragment du chemin d’accès d’origine jusqu’à'*x*', y compris, est complètement remplacé par le chemin d’accès désigné par'*x*'. Le reste du chemin d’accès après «*x*» est ajouté à ce nouveau chemin d’accès. Cela devient alors le chemin d’accès modifié.

X : « C : \\ alpha \\ beta \\ absLink \\ gamma \\ file »

Lien : « absLink » est mappé à « \\ \\ machineB \\ share »

Chemin modifié : « \\ \\ machineB \\ share \\ gamma \\ file »

## <a name="example-of-a-relative-symbolic-links"></a>Exemple de liens symboliques relatifs

Dans cet exemple, le chemin d’accès d’origine contient un composant «*x*», qui est un lien symbolique relatif. Lorsque'*x*'est rencontré, '*x*'est complètement remplacé par le nouveau fragment pointé par'*x*'. Le reste du chemin d’accès après «*x*» est ajouté au nouveau chemin d’accès. Tous les points (..) de ce nouveau chemin remplacent les composants qui apparaissent avant les points (..). Chaque ensemble de points remplace le composant précédent. Si le nombre de points (..) dépasse le nombre de composants, une erreur est retournée. Dans le cas contraire, lorsque tous les composants de remplacement sont terminés, le chemin d’accès final modifié est conservé.

X : C : \\ \\ \\ fichier gamma de liaison bêta \\ alpha \\

Lien : « Link » est mappé à «.. \\ .. \\ thêta

Chemin modifié : «C : \\ alpha \\ beta \\ ... \\ . \\ \\fichier gamma thêta \\ "

Chemin final : « C : \\ Theta \\ gamma \\ file »

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Liens symboliques](symbolic-links.md)
</dt> <dt>

[Liens physiques et jonctions](hard-links-and-junctions.md)
</dt> <dt>

[Nommage des fichiers, chemins d’accès et espaces de noms](naming-a-file.md)
</dt> </dl>

 

 



