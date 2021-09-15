---
description: Le matériel actuel n’implémente pas nécessairement toutes les fonctionnalités que l’interface Direct3D active. Votre application doit tester le matériel de l’utilisateur et ajuster ses stratégies de rendu en conséquence.
ms.assetid: 7b5f586c-616c-4351-b6b9-5c0179db5d8b
title: Considérations matérielles relatives à la texturation (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21f1ba8bea85cc3657478767aac7c7ffc2abebbd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403362"
---
# <a name="hardware-considerations-for-texturing-direct3d-9"></a>Considérations matérielles relatives à la texturation (Direct3D 9)

Le matériel actuel n’implémente pas nécessairement toutes les fonctionnalités que l’interface Direct3D active. Votre application doit tester le matériel de l’utilisateur et ajuster ses stratégies de rendu en conséquence.

De nombreuses cartes d’accélération 3D ne prennent pas en charge les valeurs itérées diffuses comme arguments pour les unités de fusion. Toutefois, votre application peut introduire des données de couleur itérées lorsqu’elle effectue une fusion de texture.

Un matériel 3D peut ne pas avoir une étape de fusion associée à la première texture. Sur ces adaptateurs, votre application doit effectuer une fusion au cours des deuxième et troisième étapes de texture dans le jeu de textures actuelles.

En raison de limitations dans la plupart des configurations matérielles actuelles, peu d’adaptateurs d’affichage peuvent effectuer une interpolation mipmap trilinéaire via l’interface de fusion de plusieurs textures proposée par [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9). Votre application peut utiliser la fusion de texture multipasse pour obtenir les mêmes effets, ou se dégrader en \_ mode de filtre mipmap de point D3DTEXF, qui est largement pris en charge.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Textures Direct3D](direct3d-textures.md)
</dt> </dl>

 

 
