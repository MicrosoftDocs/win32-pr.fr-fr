---
description: Les applications C++ peuvent utiliser le test alpha pour contrôler le moment où les pixels sont écrits dans la surface de cible de rendu.
ms.assetid: 368c3d12-2c8b-43e3-94c3-bccfe6c73e66
title: État des tests alpha (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 020322ee31bc08352dbb2796ea5e7141d03c77c3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514755"
---
# <a name="alpha-testing-state-direct3d-9"></a>État des tests alpha (Direct3D 9)

Les applications C++ peuvent utiliser le test alpha pour contrôler le moment où les pixels sont écrits dans la surface de cible de rendu. En utilisant l’état de rendu [**D3DRS \_ ALPHATESTENABLE**](./d3drenderstatetype.md) , votre application définit l’appareil Direct3D actuel pour qu’il teste chaque pixel en fonction d’une fonction de test alpha. Si le test a abouti, le pixel est écrit sur l’aire de conception. Si ce n’est pas le cas, Direct3D ignore le pixel. Sélectionnez la fonction de test alpha avec l’état de rendu **D3DRS \_ ALPHAFUNC** . Votre application peut définir une valeur alpha de référence pour tous les pixels à comparer à l’aide de l’état de rendu **D3DRS \_ ALPHAREF** .

L’utilisation la plus courante pour le test alpha consiste à améliorer les performances lors de la pixellisation d’objets presque transparents. Si les données de couleur en cours de pixellisation sont plus opaques que la couleur à un pixel donné (D3DPCMPCAPS \_ greaterequal à), le pixel est alors écrit. Dans le cas contraire, le rastériseur ignore complètement le pixel, en enregistrant le traitement requis pour mélanger les deux couleurs. L’exemple de code suivant vérifie si une fonction de comparaison donnée est prise en charge et, si c’est le cas, elle définit les paramètres de fonction de comparaison requis pour améliorer les performances lors du rendu.


```
// This code example assumes that pCaps is a
// D3DCAPS9 structure that was filled with a 
// previous call to IDirect3D9::GetDeviceCaps.

if (pCaps.AlphaCmpCaps & D3DPCMPCAPS_GREATEREQUAL)
{
    dev->SetRenderState(D3DRS_ALPHAREF, (DWORD)0x00000001);
    dev->SetRenderState(D3DRS_ALPHATESTENABLE, TRUE); 
    dev->SetRenderState(D3DRS_ALPHAFUNC, D3DCMP_GREATEREQUAL);
}

// If the comparison is not supported, render anyway. 
// The only drawback is no performance gain.
```



Tous les matériels ne prennent pas en charge toutes les fonctionnalités de test alpha. Vous pouvez vérifier les fonctionnalités de l’appareil en appelant la méthode [**IDirect3D9 :: GetDeviceCaps**](/windows/desktop/api) . Après avoir récupéré les fonctionnalités de l’appareil, vérifiez le membre AlphaCmpCaps de la structure [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) associé pour la fonction de comparaison souhaitée. Si le membre AlphaCmpCaps contient uniquement la \_ fonctionnalité D3DPCMPCAPS Always ou seulement le D3DPCMPCAPS ne \_ fonctionne jamais, le pilote ne prend pas en charge les tests alpha.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[États de rendu](render-states.md)
</dt> </dl>

 

 
