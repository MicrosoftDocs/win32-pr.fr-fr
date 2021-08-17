---
description: Lorsque vous créez des scènes 3D, une application peut parfois obtenir des avantages en matière de performances en affichant des objets 2D de manière à ce qu’ils apparaissent comme des objets 3D. Il s’agit de l’idée de base qui sous-tend la technique d’un billboarding.
ms.assetid: 6637a9ce-6731-4f60-8b76-854e86b10bdd
title: Billboarding (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02624a3172df7a36f4d38bb2bc6d613ded26faab8ac6d4f4b37668f0868cd16c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119123406"
---
# <a name="billboarding-direct3d-9"></a>Billboarding (Direct3D 9)

Lorsque vous créez des scènes 3D, une application peut parfois obtenir des avantages en matière de performances en affichant des objets 2D de manière à ce qu’ils apparaissent comme des objets 3D. Il s’agit de l’idée de base qui sous-tend la technique d’un billboarding.

Un tableau blanc dans le sens normal du mot est un signe sur une route. Les applications Microsoft Direct3D peuvent créer et afficher ce type de panneaux en définissant un solide rectangulaire et en lui appliquant une texture. L’affichage des panneaux dans le sens le plus spécialisé des graphiques 3D est une extension de ce. L’objectif est de faire en sorte que les objets 2D apparaissent en 3D. La technique consiste à appliquer une texture qui contient l’image de l’objet à une primitive rectangulaire. La primitive est pivotée afin d’être toujours face à l’utilisateur. Peu importe si l’image de l’objet n’est pas rectangulaire. Les parties du panneau peuvent être rendues transparentes, donc les parties de l’image de tableau que vous ne souhaitez pas voir ne sont pas visibles.

De nombreux jeux utilisent le billboarding pour les sprites animés. Par exemple, lorsque l’utilisateur parcourt un labyrinthe 3D, il peut voir des armes ou des récompenses qui peuvent être récupérées. Il s’agit généralement d’images 2D texturées sur une primitive rectangulaire. Le billboarding est souvent utilisé dans les jeux pour restituer des images d’arbres, d’arbustes et de clouds.

Quand une image est appliquée à un panneau, la primitive rectangulaire doit d’abord être pivotée afin que l’image résultante fasse face à l’utilisateur. Votre application doit ensuite la traduire en position. L’application peut ensuite appliquer une texture à la primitive.

Le billboarding fonctionne mieux pour les objets symétriques, en particulier les objets qui sont symétriques le long de l’axe vertical. Elle requiert également que l’altitude du point de vue n’augmente pas trop. Si l’utilisateur est autorisé à afficher le panneau d’affichage ci-dessus, il devient évident que l’objet est 2D plutôt que 3D.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Exemples alpha](alpha-examples.md)
</dt> </dl>

 

 



