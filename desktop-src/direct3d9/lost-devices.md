---
description: Un appareil Direct3D peut être dans un état opérationnel ou perdu.
ms.assetid: dc4326ba-2ebc-4bca-8fba-02d8db739b8f
title: Appareils perdus (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a808cb113f5c2fd35a741e0efc7c6b8af9e127df
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104317709"
---
# <a name="lost-devices-direct3d-9"></a>Appareils perdus (Direct3D 9)

Un appareil Direct3D peut être dans un état opérationnel ou perdu. L’état opérationnel est l’état normal de l’appareil dans lequel l’appareil s’exécute et affiche tout le rendu comme prévu. L’appareil effectue une transition vers l’état perdu lorsqu’un événement, tel que la perte du focus clavier dans une application en plein écran, rend le rendu impossible. L’état perdu est caractérisé par l’échec silencieux de toutes les opérations de rendu, ce qui signifie que les méthodes de rendu peuvent retourner des codes de réussite même si les opérations de rendu échouent. Dans ce cas, le code d’erreur D3DERR \_ DEVICELOST est retourné par [**IDirect3DDevice9 ::P renvoyé**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present).

Par défaut, le jeu complet de scénarios pouvant entraîner la perte d’un appareil n’est pas spécifié. Parmi les exemples classiques, citons la perte de focus, par exemple quand l’utilisateur appuie sur ALT + TAB ou lorsqu’une boîte de dialogue système est initialisée. Les appareils peuvent également être perdus en raison d’un événement de gestion de l’alimentation ou lorsqu’une autre application suppose une opération en plein écran. En outre, tout échec de [**IDirect3DDevice9 :: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) met l’appareil dans un état perdu.

Toutes les méthodes dérivées de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) sont assurées de fonctionner après la perte d’un appareil. Après la perte de l’appareil, chaque fonction a généralement les trois options suivantes :

-   Échec avec D3DERR \_ DEVICELOST-cela signifie que l’application doit reconnaître que l’appareil a été perdu, afin que l’application identifie qu’un événement ne se produit pas comme prévu.
-   Échec en mode silencieux, en renvoyant \_ un ou plusieurs codes de retour : si une fonction échoue en mode silencieux, l’application ne peut généralement pas faire la distinction entre le résultat de « succès » et une « défaillance silencieuse ».
-   La fonction retourne un code de retour.



|                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Différences entre Direct3D 9 et Direct3D 9Ex :<br/> Un appareil Direct3D 9 retourne D3DERR \_ DEVICELOST. Une fois qu’elle a été retournée à partir de [**IDirect3DDevice9 ::P renvoyé**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present), le comportement d’émulation ne fonctionne plus et tous les appels futurs échouent jusqu’à ce que l’appareil soit réinitialisé avec succès.<br/> Un appareil Direct3D 9Ex ne retourne jamais D3DERR \_ DEVICELOST, mais peut renvoyer de nouveaux messages d’État (voir [modifications de comportement](dx9lh.md)de l’appareil).<br/> |



 

## <a name="responding-to-a-lost-device"></a>Réponse à un appareil perdu

Un appareil perdu doit recréer les ressources (y compris les ressources mémoire vidéo) après sa réinitialisation. Si un appareil est perdu, l’application interroge l’appareil pour voir s’il peut être restauré à l’état opérationnel. Si ce n’est pas le cas, l’application attend que l’appareil puisse être restauré.

Si l’appareil peut être restauré, l’application prépare l’appareil en détruisant toutes les ressources de la mémoire vidéo et toutes les chaînes de permutation. L’application appelle ensuite la méthode [**IDirect3DDevice9 :: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) . La réinitialisation est la seule méthode qui a un effet lorsqu’un appareil est perdu, et est la seule méthode par laquelle une application peut remplacer l’appareil par un état opérationnel perdu. La réinitialisation échouera sauf si l’application libère toutes les ressources qui sont allouées dans D3DPOOL \_ par défaut, y compris celles créées par les méthodes [**IDirect3DDevice9 :: CreateRenderTarget**](/windows/desktop/api) et [**IDirect3DDevice9 :: CreateDepthStencilSurface**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createdepthstencilsurface) .

Pour l’essentiel, les appels haute fréquence de Direct3D ne retournent aucune information indiquant si l’appareil a été perdu. L’application peut continuer à appeler des méthodes de rendu, telles que [**IDirect3DDevice9 ::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive), sans recevoir de notification d’un appareil perdu. En interne, ces opérations sont ignorées jusqu’à ce que l’appareil soit réinitialisé à l’état opérationnel.

L’application peut déterminer la marche à suivre pour trouver un appareil perdu en interrogeant la valeur de retour de la méthode [**IDirect3DDevice9 :: TestCooperativeLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-testcooperativelevel) .

## <a name="locking-operations"></a>Opérations de verrouillage

En interne, Direct3D effectue suffisamment de travail pour s’assurer qu’une opération de verrouillage va être effectuée après la perte d’un appareil. Toutefois, il n’est pas garanti que les données de la ressource de mémoire vidéo seront exactes au cours de l’opération de verrouillage. Il est garanti qu’aucun code d’erreur ne sera renvoyé. Cela permet d’écrire des applications sans se préoccuper de la perte d’appareil pendant une opération de verrouillage.

## <a name="resources"></a>Ressources

Les ressources peuvent consommer de la mémoire vidéo. Étant donné qu’un appareil perdu est déconnecté de la mémoire vidéo appartenant à la carte, il n’est pas possible de garantir l’allocation de mémoire vidéo lorsque l’appareil est perdu. Par conséquent, toutes les méthodes de création de ressources sont implémentées pour aboutir en retournant D3D \_ OK, mais elles allouent en fait uniquement de la mémoire système factice. Étant donné que toutes les ressources de mémoire vidéo doivent être détruites avant le redimensionnement de l’appareil, il n’y a aucun problème de dépassement de la mémoire vidéo. Ces surfaces factices permettent d’afficher les opérations de verrouillage et de copie pour fonctionner normalement jusqu’à ce que l’application appelle [**IDirect3DDevice9 ::P renvoyée**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present) et découvre que l’appareil a été perdu.

Toute la mémoire vidéo doit être libérée pour qu’un appareil puisse être réinitialisé à un état opérationnel. Cela signifie que l’application doit libérer toutes les chaînes de permutation créées avec [**IDirect3DDevice9 :: CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) et toutes les ressources placées dans la \_ classe de mémoire par défaut D3DPOOL. L’application n’a pas besoin de libérer des ressources dans les \_ classes de mémoire D3DPOOL gérées ou D3DPOOL \_ SYSTEMMEM. Les autres données d’État sont automatiquement détruites par la transition vers un état opérationnel.

Vous êtes encouragé à développer des applications avec un seul chemin de code pour répondre à la perte de l’appareil. Ce chemin de code est susceptible d’être similaire, s’il n’est pas identique, au chemin de code utilisé pour initialiser l’appareil au démarrage.

## <a name="retrieved-data"></a>Données récupérées

Direct3D permet aux applications de valider les États de texture et de rendu par rapport au rendu de passe unique par le matériel à l’aide de [**IDirect3DDevice9 :: ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice). Cette méthode, qui est généralement appelée pendant l’initialisation de l’application, retourne D3DERR \_ DEVICELOST si l’appareil a été perdu.

Direct3D permet également aux applications de copier des images générées ou écrites précédemment à partir de ressources de mémoire vidéo vers des ressources de mémoire système non volatiles. Étant donné que les images sources de ces transferts peuvent être perdues à tout moment, Direct3D autorise l’échec de ces opérations de copie lorsque l’appareil est perdu.

En ce qui concerne les requêtes asynchrones, [**IDirect3DQuery9 :: GetData**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dquery9-getdata) retourne D3DERR \_ DEVICELOST si l’indicateur Flush est spécifié, afin d’indiquer à l’application que **IDirect3DQuery9 :: GetData** ne retourne jamais la valeur S \_ .

L’opération de copie, [**IDirect3DDevice9 :: GetFrontBufferData**](/windows/desktop/api), peut échouer avec D3DERR \_ DEVICELOST, car il n’y a aucune surface primaire lorsque l’appareil est perdu. [**IDirect3DDevice9 :: CreateAdditionalSwapChain**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createadditionalswapchain) peut également échouer avec D3DERR \_ DEVICELOST, car une mémoire tampon d’arrière-plan ne peut pas être créée lorsque l’appareil est perdu. Notez que ces cas sont la seule instance de D3DERR \_ DEVICELOST en dehors des méthodes [**IDirect3DDevice9 ::P**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present)Reverse, [**IDirect3DDevice9 :: TestCooperativeLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-testcooperativelevel)et [**IDirect3DDevice9 :: Reset**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-reset) .

## <a name="programmable-shaders"></a>Nuanceurs programmables

Dans Direct3D 9, les nuanceurs de vertex et les nuanceurs de pixels n’ont pas besoin d’être recréés après la réinitialisation. Ils seront mémorisés. Dans les versions précédentes de DirectX, un appareil perdu nécessitait la recréation des nuanceurs.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Périphériques Direct3D](direct3d-devices.md)
</dt> </dl>

 

 
