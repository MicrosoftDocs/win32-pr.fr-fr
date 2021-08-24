---
description: La gestion de texture est le processus qui consiste à déterminer les textures nécessaires au rendu à un moment donné et à s’assurer que ces textures sont chargées dans la mémoire vidéo.
ms.assetid: ea6d64ee-f570-49eb-b5fd-67fcde3f8ddc
title: Gestion automatique de la texture (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43c65168947acb05c8437836ba0b27765a9b03d3ba97fd223f50eb9a99ab8c50
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119751399"
---
# <a name="automatic-texture-management-direct3d-9"></a>Gestion automatique de la texture (Direct3D 9)

La gestion de texture est le processus qui consiste à déterminer les textures nécessaires au rendu à un moment donné et à s’assurer que ces textures sont chargées dans la mémoire vidéo. Comme pour n’importe quel algorithme, les schémas de gestion de texture varient en fonction de la complexité, mais toute approche de la gestion de texture implique les tâches clés suivantes.

-   Suivi de la quantité de mémoire de texture disponible.
-   Calcul des textures nécessaires pour le rendu, et qui ne le sont pas.
-   Détermination des ressources de texture existantes qui peuvent être rechargées avec une autre image de texture, et quelles surfaces doivent être détruites et remplacées par de nouvelles ressources de texture.

Direct3D implémente la gestion des textures prise en charge par le système pour s’assurer que les textures sont chargées pour des performances optimales. Les ressources de texture que Direct3D gère sont appelées textures gérées.

Le gestionnaire de texture effectue le suivi des textures avec un horodatage qui identifie le moment où la texture a été utilisée pour la dernière fois. Il utilise ensuite un algorithme utilisé le moins récemment pour déterminer les textures à supprimer. Les priorités de texture sont utilisées comme séparateurs de liaison lorsque deux textures sont destinées à être supprimées de la mémoire. Si deux textures ont la même valeur de priorité, la texture utilisée le moins récemment est supprimée. Toutefois, si deux textures ont le même horodatage, la texture qui a une priorité inférieure est supprimée en premier.

Vous demandez une gestion automatique de la texture pour les surfaces de texture lorsque vous les créez. Pour récupérer une texture managée dans une application C++, créez une ressource de texture en appelant [**IDirect3DDevice9 :: CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) et en spécifiant le D3DPOOL \_ géré pour le paramètre de pool. Vous n’êtes pas autorisé à spécifier l’endroit où vous souhaitez créer la texture. Vous ne pouvez pas utiliser les \_ indicateurs D3DPOOL par défaut ou D3DPOOL \_ SYSTEMMEM lors de la création d’une texture managée. Après avoir créé la texture managée, vous pouvez appeler la méthode [**IDirect3DDevice9 :: SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) pour lui affecter une étape dans la texture de texture de l’appareil de rendu.

Vous pouvez affecter une priorité aux textures gérées en appelant la méthode [**IDirect3DResource9 :: SetPriority**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dresource9-setpriority) pour la surface de texture.

Direct3D télécharge automatiquement les textures dans la mémoire vidéo en fonction des besoins. Le système peut mettre en cache des textures gérées dans la mémoire vidéo locale ou non locale, en fonction de la disponibilité de la mémoire vidéo non locale ou d’autres facteurs. L’emplacement du cache de vos Textures gérées n’est pas communiqué à votre application, et ces informations ne sont pas requises pour utiliser la gestion automatique de la texture. Si votre application utilise plus de textures que la mémoire vidéo ne peut en contenir, Direct3D supprime les textures plus anciennes de la mémoire vidéo pour libérer de l’espace pour les nouvelles textures. Si vous réutilisez une texture supprimée, le système utilise la surface d’origine de la texture de mémoire système pour recharger la texture dans le cache de la mémoire vidéo. Même si le rechargement de la texture est nécessaire, elle réduit également les performances de l’application.

Vous pouvez modifier dynamiquement la copie mémoire système d’origine de la texture en mettant à jour ou en verrouillant la ressource de texture. Lorsque le système détecte une surface incorrecte, après qu’une mise à jour est terminée ou lorsque la surface est déverrouillée, le gestionnaire de texture met automatiquement à jour la copie de la mémoire vidéo de la texture. Le gain de performance entraîné est semblable au rechargement d’une texture supprimée.

Lorsque vous entrez un nouveau niveau dans un jeu, votre application peut avoir besoin de vider toutes les textures gérées de la mémoire vidéo (en appelant [**IDirect3DDevice9 :: EvictManagedResources**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-evictmanagedresources)).

Pour plus d’informations sur la gestion des ressources, consultez [gestion des ressources (Direct3D 9)](managing-resources.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Textures Direct3D](direct3d-textures.md)
</dt> </dl>

 

 
