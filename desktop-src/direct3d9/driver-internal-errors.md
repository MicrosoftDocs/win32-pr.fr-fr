---
description: Dans Direct3D 9, Direct3D autorise le pilote à retourner des codes d’erreur tels que E \_ OUTOFMEMORY, D3DERR \_ OUTOFVIDEOMEMORY et D3DERR \_ UNSUPPORTEDCOLORARG afin qu’une application puisse y répondre.
ms.assetid: 483fdb03-e453-4a1b-bd8e-294e9e9a20c2
title: Erreurs internes du pilote (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c81b0ee8ba50edb3c14fbd9a22c9fa9dc93aab8f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109342"
---
# <a name="driver-internal-errors-direct3d-9"></a>Erreurs internes du pilote (Direct3D 9)

Dans Direct3D 9, Direct3D autorise le pilote à retourner des codes d’erreur tels que E \_ OUTOFMEMORY, D3DERR \_ OUTOFVIDEOMEMORY et D3DERR \_ UNSUPPORTEDCOLORARG afin qu’une application puisse y répondre. Toutefois, parfois, les appels d’API qui ont généré ces types de retour sont chargés dans une mémoire tampon de commande et sont traités par lot pour être envoyés au GPU (consultez [contrôle des optimisations du runtime et du pilote](accurately-profiling-direct3d-api-calls.md)). Dans ce cas, les erreurs ne peuvent pas être relayées à l’application lorsque l’action doit être exécutée. le code d’erreur est donc consommé par le runtime et une remarque est faite sur l’objet de l’appareil. Plus tard, quand l’application appelle [**IDirect3DDevice9 ::P renvoyée**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-present), **IDirect3DDevice9 ::P renvoyée** renverra D3DERR \_ DRIVERINTERNALERROR. C’est pour cette raison que la meilleure approche pour une application de recevoir un \_ DRIVERINTERNALERROR D3DERR à partir de **IDirect3DDevice9 ::P renvoyée** consiste à détruire et à recréer l’appareil.

Si vous souhaitez essayer de déboguer davantage, voici quelques suggestions pour tenter de déterminer l’appel d’API qui génère l’erreur :

-   Étant donné que la liste des valeurs de retour possibles n’est pas complète, vous pouvez essayer de trouver l’appel qui échoue en entourant chaque appel d’API comme suit :

    ```
    TRACE ( "Calling DrawPrimitive" );
    d3ddev->DrawPrim(...);
    TRACE ( "done\n" );
    ```

    

    Le flux de débogage de sortie doit ensuite afficher l’appel qui est à l’origine du problème.

-   En outre, à des fins de débogage, essayez d’appeler [**IDirect3DDevice9 :: ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice) immédiatement avant chaque [**IDirect3DDevice9 ::D rawprimitive**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-drawprimitive) pour voir s’il existe un problème supplémentaire avec le pilote de périphérique (opération non prise en charge, combinaison inutilisable de formats de texture, etc.).

    > [!Note]  
    > [**IDirect3DDevice9 :: ValidateDevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-validatedevice) doit être utilisé avec soin et avec modération en raison de la quantité de travail de validation que le pilote doit effectuer pour retourner une réponse.

     

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Conseils de programmation](programming-tips.md)
</dt> </dl>

 

 
