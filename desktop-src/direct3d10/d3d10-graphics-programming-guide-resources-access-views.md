---
description: Dans Direct3D 10, les ressources de texture sont accessibles à l’aide d’une vue, qui est un mécanisme d’interprétation matérielle d’une ressource en mémoire.
ms.assetid: ccfe6273-0dcf-4b42-9d74-665a0b4cd14a
title: Affichages de texture (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83dd83b1a3896637ce73505de00027ea9dfadac4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126922807"
---
# <a name="texture-views-direct3d-10"></a>Affichages de texture (Direct3D 10)

Dans Direct3D 10, les ressources de texture sont accessibles à l’aide d’une vue, qui est un mécanisme d’interprétation matérielle d’une ressource en mémoire. Une vue permet à une étape de pipeline particulière d’accéder uniquement aux sous- [ressources](d3d10-graphics-programming-guide-resources-types.md) dont elle a besoin, dans la représentation souhaitée par l’application.

Une vue prend en charge la notion de ressource sans type. Une ressource sans type est une ressource créée avec une taille spécifique, mais pas un type de données spécifique. Les données sont interprétées dynamiquement lorsqu’elles sont liées au pipeline.

L’illustration suivante montre un exemple de liaison d’un tableau de texture 2D avec 6 textures en tant que ressource de nuanceur en créant une vue de ressource de nuanceur pour celle-ci. La ressource est ensuite traitée comme un tableau de textures. (Remarque : une sous-ressource ne peut pas être liée à la fois en entrée et en sortie au pipeline simultanément.)

![illustration d’un tableau de textures avec six textures](images/d3d10-cube-texture-faces.png)

Lors de l’utilisation d’un tableau de texture 2D en tant que cible de rendu, la ressource peut être affichée sous la forme d’un tableau de textures 2D (6 dans cet exemple) avec des niveaux de mipmap (3 dans cet exemple).

Créez un objet de vue pour une cible de rendu en appelant CreateRenderTargetView. Appelez ensuite OMSetRenderTargets pour définir la vue de la cible de rendu sur le pipeline. Affichez les cibles de rendu en appelant Draw et en utilisant le RenderTargetArrayIndex pour indexer dans la texture appropriée dans le tableau. Vous pouvez utiliser une sous-ressource (un niveau de mipmap, une combinaison d’index de tableau) pour effectuer une liaison à n’importe quel tableau de sous-ressources. Vous pouvez donc effectuer une liaison avec le deuxième niveau de mipmap et mettre à jour ce niveau de mipmap particulier uniquement si vous le souhaitez, comme dans l’illustration suivante.

![illustration de la liaison uniquement au deuxième niveau de mipmap d’un tableau de texture](images/d3d10-cube-texture-faces-subresource.png)



Différences entre Direct3D 9 et Direct3D 10 :

- Dans Direct3D 10, vous ne liez plus une ressource directement au pipeline, vous créez une vue d’une ressource, puis vous définissez la vue sur le pipeline. Cela permet la validation et le mappage dans le runtime et le pilote pour se produire lors de la création de la vue, réduisant ainsi la vérification du type au moment de la liaison.



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Ressources (Direct3D 10)](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 




