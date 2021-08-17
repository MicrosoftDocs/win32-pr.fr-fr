---
title: Monikers composites
description: L’une des fonctionnalités les plus utiles des monikers est que vous pouvez concaténer ou composer des monikers ensemble.
ms.assetid: ea2453f3-7a64-4ce0-87c2-de6224ca71df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ad815cdb89dda7f58fe1507d43a07a14d24875309668297e20ec51114dd65d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117737025"
---
# <a name="composite-monikers"></a>Monikers composites

L’une des fonctionnalités les plus utiles des monikers est que vous pouvez concaténer ou composer des monikers ensemble. Un *moniker composite* est un moniker qui est une composition d’autres monikers et peut déterminer la relation entre les parties. Cela vous permet d’assembler le chemin d’accès complet à un objet en fonction de deux monikers ou plus qui sont l’équivalent de chemins d’accès partiels. Vous pouvez composer des monikers de la même classe (tels que deux monikers de fichier) ou de classes différentes (comme un moniker de fichier et un moniker d’élément). Si vous deviez écrire votre propre classe moniker, vous pouvez également composer vos monikers avec des monikers de fichier ou d’élément. L’avantage fondamental d’un composite est qu’il vous donne un morceau de code pour implémenter chaque moniker possible qui est une combinaison de monikers plus simples. Cela réduit considérablement le besoin de classes de moniker personnalisées spécifiques.

Étant donné que les monikers de différentes classes peuvent être composés les uns avec les autres, les monikers offrent la possibilité de joindre plusieurs espaces de noms. Le système de fichiers définit un espace de noms commun pour les objets stockés sous forme de fichiers, car toutes les applications comprennent un nom de chemin d’accès du système de fichiers. De même, un objet conteneur définit également un espace de noms privé pour les objets qu’il contient, car aucun conteneur ne comprend les noms générés par un autre conteneur. Les monikers autorisent la jointure de ces espaces de noms, car les monikers de fichiers et les monikers d’élément peuvent être composés. Un client moniker peut rechercher tous les objets dans l’espace de noms à l’aide d’un mécanisme unique. Le client appelle simplement [**IMoniker :: BindToObject**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-bindtoobject) sur le moniker et le code du moniker gère le reste. Un appel à [**IMoniker :: GetDisplayName**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-getdisplayname) sur un composite crée un nom à l’aide de la concaténation de tous les noms d’affichage des monikers individuels.

En outre, étant donné que vous pouvez écrire votre propre classe moniker, la composition du moniker vous permet d’ajouter des extensions personnalisées à l’espace de noms pour les objets.

Parfois, deux monikers de classes spécifiques peuvent être combinés de manière spéciale. Par exemple, un moniker de fichier représentant un chemin d’accès incomplet et un autre moniker de fichier représentant un chemin d’accès relatif peuvent être combinés pour former un moniker de fichier unique représentant le chemin d’accès complet. Par exemple, les monikers de fichier « c : \\ Work \\ art » peuvent être composés avec le moniker de fichier relatif «». \\ sauvegarde \\myfile.doc « égal à » c : \\ sauvegarde de travail \\ \\myfile.doc». Il s’agit d’un exemple de *composition non générique*.

En revanche, la *composition générique* autorise la connexion de deux monikers, quelle que soit leur classe. Par exemple, vous pouvez composer un moniker d’élément sur un moniker de fichier, bien que ce ne soit pas le cas de l’inverse.

Comme une composition non générique dépend de la classe des monikers impliqués, ses détails sont définis par l’implémentation d’une classe de moniker particulière. Vous pouvez définir de nouveaux types de compositions non génériques si vous écrivez une nouvelle classe moniker. En revanche, les compositions génériques sont définies par OLE. Les monikers créés à la suite d’une composition générique sont appelés monikers composites génériques.

Ces trois classes, les monikers de fichiers, les monikers d’élément et les monikers composites génériques, fonctionnent ensemble et sont les classes de monikers les plus couramment utilisées.

Les clients moniker doivent appeler [**IMoniker :: ComposeWith**](/windows/desktop/api/ObjIdl/nf-objidl-imoniker-composewith) pour créer un composite sur moniker avec un autre. Le moniker sur lequel il est appelé détermine en interne s’il peut effectuer une composition générique ou non générique. Si l’implémentation du moniker détermine qu’une composition générique est utilisable, OLE fournit la fonction [**CreateGenericComposite**](/windows/desktop/api/Objbase/nf-objbase-creategenericcomposite) pour faciliter cette tâche.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Anti-monikers](anti-monikers.md)
</dt> <dt>

[Monikers de classe](class-monikers.md)
</dt> <dt>

[Monikers de fichiers](file-monikers.md)
</dt> <dt>

[Monikers d’élément](item-monikers.md)
</dt> <dt>

[Monikers de pointeur](pointer-monikers.md)
</dt> </dl>

 

 




