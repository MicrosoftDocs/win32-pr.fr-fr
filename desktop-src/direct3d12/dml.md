---
title: Direct Machine Learning (DirectML)
description: Direct Machine Learning (DirectML) est une API de bas niveau pour Machine Learning. Elle possède une interface de programmation connue (native C++, nano-COM) et des flux de travail du style de DirectX 12.
ms.custom: Windows 10 May 2019 Update
ms.localizationpriority: high
ms.topic: article
ms.date: 04/19/2019
ms.openlocfilehash: 25bbd169a1ad0467ed56135c31c8c2a0b70b57a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74104039"
---
# <a name="direct-machine-learning-directml"></a>Direct Machine Learning (DirectML)

Direct Machine Learning (DirectML) est une API de bas niveau pour Machine Learning. Elle possède une interface de programmation connue (native C++, nano-COM) et des flux de travail du style de DirectX 12. Vous pouvez intégrer l’apprentissage machine par le biais d’inférences de charges de travail dans votre jeu, votre moteur, votre intergiciel (middleware), votre serveur principal ou toute autre application. DirectML est prise en charge par tout le matériel compatible avec DirectX 12.

DirectML est introduit dans Windows 10, version 1903 et dans la version correspondante du SDK Windows.

## <a name="in-this-section"></a>Contenu de cette section

| Rubrique | Description |
|-|-|
| [Introduction à DirectML](dml-intro.md) | Direct Machine Learning (DirectML) est une API de bas niveau pour Machine Learning (ML). |
| [Liaison dans DirectML](dml-binding.md) | Dans DirectML, la *liaison* fait référence à l’attachement des ressources au pipeline que le GPU doit utiliser pendant l’initialisation et l’exécution de vos opérateurs machine learning. Ces ressources peuvent être des dizaines d’entrée et de sortie, par exemple, ainsi que toutes les ressources temporaires ou persistantes dont l’opérateur a besoin. |
| [Barrières UAV et barrières de l’état des ressources dans DirectML](dml-barriers.md) | Décrit les avantages de l’exactitude des barrières et comment vous pouvez les utiliser dans DirectML. |
| [Utilisation de Strides pour exprimer le remplissage et la disposition de la mémoire](dml-strides.md) | Les dizaines de DirectML sont décrits par des propriétés connues sous le nom de *tailles* et de *Strides* du tenseur. |
| [Durée de vie et synchronisation des ressources](dml-resource-lifetime.md) | Afin d’éviter un comportement indéfini, votre application DirectML doit gérer correctement les durées de vie des objets et la synchronisation entre l’UC et le GPU. |
| [Utilisation de la couche de débogage DirectML](dml-debug-layer.md) | La couche de débogage DirectML est un composant facultatif de développement qui vous permet de déboguer votre code DirectML. |
| [Gestion des erreurs et suppression d’appareil](dml-errors.md) | Cette rubrique explique comment déboguer la suppression de l’appareil DirectML et d’autres conditions d’erreur. |
| [Fonctions d’assistance DirectML](dml-helper-functions.md) | Listes de code des fonctions d’assistance DirectML essentielles. |
| [Exemples d’applications DirectML](dml-min-app.md) | Liens vers des exemples d’applications DirectML, y compris un exemple d’application DirectML minimale. |

## <a name="related-topics"></a>Rubriques connexes

* [Guide de programmation Direct3D 12](directx-12-programming-guide.md)
