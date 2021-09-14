---
title: COM (Component Object Model)
description: COM (Component Object Model)
ms.assetid: f5f66603-466c-496b-be29-89a8ed9361dd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 786a4bef59401877f642273ba7a97756232ac083
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127221721"
---
# <a name="the-component-object-model"></a>COM (Component Object Model)

Le modèle COM (Component Object Model) Microsoft est un système orienté objet et indépendant de la plateforme, qui permet de créer des composants logiciels binaires pouvant interagir. COM est la technologie de base pour OLE (documents composés) de Microsoft, ActiveX (composants Internet), ainsi que d’autres.

Pour comprendre COM (et, par conséquent, toutes les technologies basées sur COM), il est essentiel de comprendre qu’il ne s’agit pas d’un langage orienté objet, mais d’une norme. COM n’indique pas non plus comment une application doit être structurée ; les détails de la langue, de la structure et de l’implémentation sont laissés au développeur de l’application. Au lieu de cela, COM spécifie un modèle objet et des exigences de programmation qui permettent aux objets COM (également appelés composants COM, ou parfois simplement des *objets*) d’interagir avec d’autres objets. Ces objets peuvent se trouver dans un processus unique, dans d’autres processus, et peuvent même se trouver sur des ordinateurs distants. Ils peuvent être écrits dans des langages différents et peuvent être structurés de manière très différente, ce qui explique pourquoi COM est désigné comme une *norme binaire*. norme qui s’applique après qu’un programme a été traduit en code machine binaire.

La seule exigence de langage pour COM est que le code est généré dans un langage qui peut créer des structures de pointeurs et, de manière explicite ou implicite, appeler des fonctions à l’aide de pointeurs. Les langages orientés objet tels que C++ et Smalltalk fournissent des mécanismes de programmation qui simplifient l’implémentation d’objets COM, mais les langages tels que C, Java et VBScript peuvent être utilisés pour créer et utiliser des objets COM.

COM définit la nature essentielle d’un objet COM. En général, un objet logiciel est constitué d’un ensemble de données et des fonctions qui manipulent les données. Un objet COM est un objet dans lequel l’accès aux données d’un objet est réalisé exclusivement par le biais d’un ou plusieurs ensembles de fonctions associées. Ces jeux de fonctions sont appelés des *interfaces* et les fonctions d’une interface sont appelées *méthodes*. En outre, COM requiert que la seule façon d’accéder aux méthodes d’une interface passe par un pointeur vers l’interface.

Outre la spécification de la norme d’objet binaire de base, COM définit certaines interfaces de base qui fournissent des fonctions communes à toutes les technologies COM et fournit un petit nombre de fonctions requises par tous les composants. COM définit également la manière dont les objets fonctionnent ensemble sur un environnement distribué et a ajouté des fonctionnalités de sécurité permettant d’assurer l’intégrité du système et des composants.

Les rubriques suivantes de cette section décrivent les problèmes COM de base liés à la conception d’objets COM :

-   [Objets et interfaces COM](com-objects-and-interfaces.md)
-   [Utilisation et implémentation de IUnknown](using-and-implementing-iunknown.md)
-   [Réutilisation d’objets](reusing-objects.md)
-   [Bibliothèque COM](the-com-library.md)
-   [Gestion de l’allocation de mémoire](managing-memory-allocation.md)

 

 




