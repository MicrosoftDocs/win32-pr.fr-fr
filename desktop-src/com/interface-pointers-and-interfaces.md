---
title: Pointeurs d’interface et interfaces
description: Pointeurs d’interface et interfaces
ms.assetid: 8a8671fe-f0b2-4698-8c98-89753fffce0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: abeb6040c2e55168fee1aa2c73db0056de557d0ddafaed6499e7da048dfc56de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119854369"
---
# <a name="interface-pointers-and-interfaces"></a>Pointeurs d’interface et interfaces

Une instance d’une implémentation d’interface est en fait un pointeur vers un tableau de pointeurs vers des méthodes, autrement dit une table de fonctions qui fait référence à une implémentation de toutes les méthodes spécifiées dans l’interface. Les objets avec plusieurs interfaces peuvent fournir des pointeurs vers plusieurs tables de fonctions. Tout code qui a un pointeur via lequel il peut accéder au tableau peut appeler les méthodes dans cette interface.

Parler précisément de cette indirection multiple est peu pratique. par conséquent, le pointeur vers la table de fonctions d’interface qu’un autre objet doit avoir pour appeler ses méthodes est appelé simplement un *pointeur d’interface*. Vous pouvez créer manuellement des tables de fonctions dans une application C ou presque automatiquement à l’aide de Visual C++ (ou d’autres langages orientés objet qui prennent en charge COM).

Avec la prise en charge de compilateur appropriée (qui est inhérente à C et C++), un client peut appeler une méthode d’interface par son nom, et non pas sa position dans le tableau. Étant donné qu’une interface est un type, le compilateur, en fonction des noms de méthodes, peut vérifier les types de paramètres et les valeurs de retour de chaque appel de méthode d’interface. En revanche, si un client utilise un schéma d’appel basé sur la position, cette vérification de type n’est pas disponible, même en C ou C++.

Chaque interface est un contrat immuable d’un groupe fonctionnel de méthodes. Vous référencez une interface au moment de l’exécution avec un identificateur d’interface global unique (IID). Cet IID, qui est une instance spécifique d’un identificateur global unique (GUID) pris en charge par COM, permet à un client de demander précisément à un objet s’il prend en charge la sémantique de l’interface, sans surcharge inutile, et sans la confusion qui peut se produire dans un système en présence de plusieurs versions de la même interface avec le même nom.

Pour résumer, il est important de comprendre ce qu’est une interface COM et n’est pas :

-   Une interface COM n’est pas la même chose qu’une classe C++. La définition virtuelle pure ne comporte aucune implémentation. Si vous êtes un programmeur C++, vous pouvez définir l’implémentation d’une interface en tant que classe, mais cela se trouve sous l’en-tête des détails d’implémentation, que COM ne spécifie pas. Une instance d’un objet qui implémente une interface doit être créée pour que l’interface existe réellement. En outre, différentes classes d’objets peuvent implémenter une interface de manière différente, mais elles peuvent être utilisées de manière interchangeable sous forme binaire, à condition que le comportement soit conforme à la définition de l’interface.
-   Une interface COM n’est pas un objet. Il s’agit simplement d’un groupe de fonctions associé et est la norme binaire par laquelle les clients et les objets communiquent. Tant qu’il peut fournir des pointeurs vers des méthodes d’interface, l’objet peut être implémenté dans n’importe quel langage avec une représentation d’état interne.
-   Les interfaces COM sont fortement typées. Chaque interface a son propre identificateur d’interface (GUID), ce qui élimine le risque de duplication qui peut se produire avec n’importe quel autre schéma d’attribution de noms.
-   Les interfaces COM sont immuables. Vous ne pouvez pas définir une nouvelle version d’une ancienne interface et lui attribuer le même identificateur. L’ajout ou la suppression de méthodes d’une interface ou la modification d’une sémantique crée une nouvelle interface, et non une nouvelle version d’une ancienne interface. Par conséquent, une nouvelle interface ne peut pas entrer en conflit avec une ancienne interface. Toutefois, les objets peuvent prendre en charge plusieurs interfaces simultanément et peuvent exposer des interfaces qui sont des révisions consécutives d’une interface, avec des identificateurs différents. Ainsi, chaque interface est un contrat distinct, et les objets du système ne doivent pas se préoccuper de savoir si la version de l’interface qu’elle appelle est celle qu’elle attend. L’ID d’interface (IID) définit le contrat d’interface de manière explicite et unique.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Objets et interfaces COM](com-objects-and-interfaces.md)
</dt> </dl>

 

 




