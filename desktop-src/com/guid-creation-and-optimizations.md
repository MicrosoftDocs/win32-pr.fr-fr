---
title: Création et optimisations de GUID
description: Création et optimisations de GUID
ms.assetid: 698322f2-db89-4553-90c6-4278e96716dc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 82dc1b0cc52312768759daca35824f8e7e515629131ac2c301a17d7ae99d6455
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119731429"
---
# <a name="guid-creation-and-optimizations"></a>Création et optimisations de GUID

Comme un CLSID, comme un identificateur d’interface (IID), est un GUID, aucune autre classe, quelle que soit la personne qui l’écrit, a un CLSID en double. Les implémenteurs de serveur obtiennent généralement des CLSID par le biais de la fonction [**CoCreateGuid**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateguid) . Cette fonction est assurée pour produire des CLSID uniques, de sorte que les responsables de l’implémentation de serveur dans le monde entier peuvent développer et déployer leurs logiciels indépendamment sans crainte de collision accidentelle avec les logiciels écrits par d’autres.

L’utilisation de CLSID uniques évite le risque de collisions de noms entre les classes, car les CLSID ne sont en aucun cas connectés aux noms utilisés dans l’implémentation sous-jacente. Par exemple, deux fournisseurs différents peuvent écrire des classes appelées « StackClass », mais chacun a un CLSID unique et n’a donc pas pu être confondu.

COM doit fréquemment mapper les GUID (IID et CLSID) à un ensemble arbitrairement important d’autres valeurs. En tant que développeur d’applications, vous pouvez accélérer ces recherches et améliorer ainsi les performances du système en générant les GUID de votre application sous la forme d’un bloc de valeurs consécutives.

La méthode la plus efficace pour générer un bloc de GUID consécutifs consiste à exécuter l’utilitaire uuidgen à l’aide des commutateurs-n et-x, qui génèrent un bloc d’UUID, chacun d’entre eux dont la première valeur DWORD est incrémentée d’une unité.

Par exemple, si vous tapez

**uuidgen-n5-x**

l’utilitaire uuidgen génère un bloc d’UUID similaire à ce qui suit :

``` syntax
12340001-4980-1920-6788-123456789012
12340002-4980-1920-6788-123456789012
12340003-4980-1920-6788-123456789012
12340004-4980-1920-6788-123456789012
12340005-4980-1920-6788-123456789012
 
```

L’une des méthodes permettant de générer et de suivre des GUID pour un projet entier commence par la génération d’un bloc de plusieurs UUID, par exemple, 500. Par exemple, si vous tapez

**uuidgen-N500-x > guids.txt**

l’utilitaire génère 500 UUID consécutifs et les écrit dans le fichier texte spécifié. Vous pouvez ensuite vérifier ce fichier dans votre arborescence source, en fournissant un référentiel unique pour tous les GUID à utiliser dans un projet. À mesure que les utilisateurs ont besoin de GUID pour leurs parties du projet, ils peuvent extraire le fichier, prendre en compte de nombreux GUID dont ils ont besoin, les marquer comme pris et laisser une note sur l’emplacement du code ou « spec » qu’ils utilisent.

Outre l’amélioration des performances du système, la génération de blocs de GUID consécutifs de cette façon présente les avantages suivants :

-   Un fichier central contenant tous les GUID d’une application facilite le suivi des GUID qui sont destinés aux personnes qui les utilisent.
-   Un bloc de GUID consécutifs associés à une application particulière permet aux développeurs et aux testeurs de reconnaître les GUID internes lors du débogage et facilite leur recherche dans le registre système, car ils sont stockés de manière séquentielle.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Responsabilités du serveur COM](com-server-responsibilities.md)
</dt> </dl>

 

 




