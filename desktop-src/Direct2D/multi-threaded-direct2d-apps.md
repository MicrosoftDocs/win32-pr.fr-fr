---
title: Applications Direct2D multithread
description: Décrit les meilleures pratiques pour créer des applications Direct2D multithread.
ms.assetid: FDD770D4-817F-44D9-86C4-15DD04D214AE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6be979b867edd6d36583959c4a595dbd507ca94f
ms.sourcegitcommit: c3243ec4ada05b7faf9d563853cb667ecef825e8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 11/03/2020
ms.locfileid: "103734789"
---
# <a name="multithreaded-direct2d-apps"></a>Applications Direct2D multithread

Si vous développez des applications [Direct2D](./direct2d-portal.md) , vous devrez peut-être accéder aux ressources Direct2D à partir de plusieurs threads. Dans d’autres cas, vous pouvez utiliser le multithreading pour obtenir de meilleures performances ou une meilleure réactivité (comme l’utilisation d’un thread pour l’affichage à l’écran et d’un thread distinct pour le rendu hors connexion).

Cette rubrique décrit les meilleures pratiques pour le développement d’applications [Direct2D](./direct2d-portal.md) multithread avec peu ou pas de rendu [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) . Les défaillances logicielles causées par des problèmes d’accès concurrentiel peuvent être difficiles à détecter et il est utile de planifier votre stratégie de multithreading et de suivre les meilleures pratiques décrites ici.

> [!Note]  
> Si vous accédez à deux ressources [Direct2D](./direct2d-portal.md) créées à partir de deux fabriques Direct2D à thread unique différentes, elles ne provoquent pas de conflits d’accès tant que les périphériques [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) sous-jacents et les contextes de périphérique sont également distincts. Lorsque l’on parle de « l’accès aux ressources Direct2D » dans cet article, cela signifie vraiment « l’accès aux ressources Direct2D créées à partir du même appareil Direct2D », sauf indication contraire.

## <a name="developing-thread-safe-apps-that-call-only-direct2d-apis"></a>Développement d’applications Thread-Safe qui appellent uniquement des API Direct2D

Vous pouvez créer une instance de fabrique [Direct2D](./direct2d-portal.md) multithread. Vous pouvez utiliser et partager une fabrique multithread et toutes ses ressources à partir de plusieurs threads, mais les accès à ces ressources (via les appels Direct2D) sont sérialisés par Direct2D, de sorte qu’aucun conflit d’accès ne se produit. Si votre application appelle uniquement des API Direct2D, cette protection est automatiquement effectuée par Direct2D à un niveau granulaire avec une surcharge minimale. Code permettant de créer une fabrique multithread ici.

```cpp
ID2D1Factory* m_D2DFactory;

// Create a Direct2D factory.
HRESULT hr = D2D1CreateFactory(
    D2D1_FACTORY_TYPE_MULTI_THREADED,
    &m_D2DFactory
);
```

L’image ici montre comment [Direct2D](./direct2d-portal.md) sérialise deux threads qui effectuent des appels à l’aide de l’API Direct2D uniquement.

![diagramme de deux threads sérialisés.](images/multi-thread.png)

## <a name="developing-thread-safe-direct2d-apps-with-minimal-direct3d-or-dxgi-calls"></a>Développement d’applications Thread-Safe Direct2D avec des appels Direct3D ou DXGI minimes

Il est fréquent qu’une application [Direct2D](./direct2d-portal.md) effectue également des appels [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) ou DXGI. Par exemple, un thread d’affichage est dessiné dans Direct2D, puis est présent à l’aide d’une [**chaîne de permutation dxgi**](/windows/desktop/api/dxgi/nn-dxgi-idxgiswapchain).

Dans ce cas, garantir la sécurité des threads est plus complexe : certains appels [Direct2D](./direct2d-portal.md) accèdent indirectement aux ressources [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) sous-jacentes, qui peuvent être accessibles simultanément par un autre thread qui appelle Direct3D ou DXGI. Étant donné que ces appels Direct3D ou DXGI n’ont pas conscience de la Direct2d et du contrôle, vous devez créer une fabrique Direct2D multithread, mais vous devez effectuer des responsable Mor ajoutera pour éviter les conflits d’accès.

Le diagramme ci-dessous montre un conflit d’accès aux ressources [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) en raison du thread T0 qui accède indirectement à une ressource via un appel [Direct2D](./direct2d-portal.md) et T2 qui accède à la même ressource directement via un appel Direct3D ou DXGI.

> [!Note]  
> La protection des threads fournie par [Direct2D](./direct2d-portal.md) (le verrou bleu dans cette image) n’est pas utile dans ce cas.

 

![diagramme de protection des threads.](images/multi-thread2.png)

Pour éviter les conflits d’accès aux ressources ici, nous vous recommandons d’acquérir explicitement le verrou utilisé par [Direct2D](./direct2d-portal.md) pour la synchronisation d’accès interne, et d’appliquer ce verrou quand un thread doit effectuer des appels [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) ou dxgi susceptibles de provoquer un conflit d’accès comme indiqué ici. En particulier, vous devez être particulièrement vigilant avec le code qui utilise des exceptions ou un système précoce en fonction des codes de retour HRESULT. Pour cette raison, nous vous recommandons d’utiliser un modèle RAII (Resource Acquisition Is Initialization) pour appeler les méthodes [**Enter**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-enter) et [**Leave**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-leave) .

> [!Note]  
> Il est important de coupler les appels aux méthodes [**Enter**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-enter) et [**Leave**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-leave) , sinon votre application peut se bloquer.

 

Le code ci-dessous montre un exemple de verrouillage, puis déverrouillage autour des appels [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) ou DXGI.


```C++
void MyApp::DrawFromThread2()
{
    // We are accessing Direct3D resources directly without Direct2D's knowledge, so we
    // must manually acquire and apply the Direct2D factory lock.
    ID2D1Multithread* m_D2DMultithread;
    m_D2DFactory->QueryInterface(IID_PPV_ARGS(&m_D2DMultithread));
    m_D2DMultithread->Enter();
    
    // Now it is safe to make Direct3D/DXGI calls, such as IDXGISwapChain::Present
    MakeDirect3DCalls();

    // It is absolutely critical that the factory lock be released upon
    // exiting this function, or else any consequent Direct2D calls will be blocked.
    m_D2DMultithread->Leave();
}
```



> [!Note]  
> Certains appels [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) ou dxgi (notamment [**IDXGISwapChain ::P**](/windows/desktop/api/dxgi/nf-dxgi-idxgiswapchain-present)renouvely) peuvent acquérir des verrous et/ou déclencher des rappels dans le code de la fonction ou de la méthode appelante. Vous devez être conscient de cela et vous assurer que ce comportement ne provoque pas de blocages. Pour plus d’informations, consultez la rubrique [vue d’ensemble de dxgi](/windows/desktop/direct3ddxgi/d3d10-graphics-programming-guide-dxgi) .

 

![diagramme de verrouillage de threads Direct2D et Direct3D.](images/multi-thread3.png)

Lorsque vous utilisez les méthodes [**Enter**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-enter) et [**Leave**](/windows/win32/api/d2d1_1/nf-d2d1_1-id2d1multithread-leave) , les appels sont protégés par le [Direct2D](./direct2d-portal.md) automatique et le verrou explicite, de sorte que l’application n’atteint pas le conflit d’accès.

Il existe d’autres approches pour contourner ce problème. Toutefois, nous vous recommandons de protéger explicitement les appels [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) ou dxgi avec le verrou [Direct2D](./direct2d-portal.md) , car il offre généralement de meilleures performances, car il protège la concurrence à un niveau nettement plus fin et avec une surcharge inférieure sous Direct2D cover.

## <a name="ensuring-atomicity-of-stateful-operations"></a>Garantir l’atomicité des opérations avec état

Bien que les fonctionnalités de sécurité des threads de [DirectX](/previous-versions//ee663301(v=vs.85)) permettent de garantir que deux appels d’API individuels ne sont pas effectués simultanément, vous devez également vous assurer que les threads qui effectuent des appels d’API avec état n’interfèrent pas entre eux. Voici un exemple.

1.  Il y a deux lignes de texte que vous souhaitez afficher à la fois sur l’écran (par thread 0) et hors écran (par thread 1) : \# la ligne 1 est « un est plus élevé » et la ligne \# 2 est « à B », qui seront dessinées à l’aide d’un pinceau noir Uni.
2.  Le thread 1 dessine la première ligne de texte.
3.  Le thread 0 réagit à une entrée utilisateur, met à jour les deux lignes de texte en « B est plus petit » et « supérieur à », puis modifie la couleur du pinceau en rouge plein pour son propre dessin.
4.  Le thread 1 continue à dessiner la deuxième ligne de texte, qui est maintenant « à un », avec le pinceau de couleur rouge ;
5.  Enfin, nous obtenons deux lignes de texte sur la cible de dessin hors écran : « A est plus grand » en noir et « que A » en rouge.

![diagramme des threads d’écran activés et désactivés.](images/multi-thread4.png)

Dans la ligne supérieure, le thread 0 est dessiné avec les chaînes de texte actuelles et le pinceau noir actuel. Thread 1 se termine uniquement par le dessin hors écran sur la moitié supérieure.

Dans la ligne du milieu, le thread 0 répond à l’interaction de l’utilisateur, met à jour les chaînes de texte et le pinceau, puis actualise l’écran. À ce stade, thread 1 est bloqué. Dans la ligne inférieure, le rendu final hors écran après le thread 1 reprend le dessin de la moitié inférieure avec un pinceau modifié et une chaîne de texte modifiée.

Pour résoudre ce problème, nous vous recommandons d’avoir un contexte distinct pour chaque thread, de sorte que :

-   Vous devez créer une copie du contexte de périphérique afin que les ressources mutables (c’est-à-dire les ressources qui peuvent varier au cours de l’affichage ou de l’impression, telles que le contenu texte ou le pinceau de couleur unie dans l’exemple) ne changent pas lors du rendu. Dans cet exemple, vous devez conserver une copie de ces deux lignes de texte et du pinceau de couleur avant de dessiner. En procédant ainsi, vous garantissez que chaque thread dispose d’un contenu complet et cohérent à dessiner et à présenter.
-   Vous devez partager des ressources à poids élevé (telles que des bitmaps et des graphiques d’effets complexes) qui sont initialisées une seule fois, puis jamais modifiées sur les threads pour améliorer les performances.
-   Vous pouvez partager des ressources légères (telles que des pinceaux de couleur unie et des formats de texte) qui sont initialisés une seule fois et qui ne sont jamais modifiés à travers les threads.

## <a name="summary"></a>Résumé

Lorsque vous développez des applications [Direct2D](./direct2d-portal.md) multithread, vous devez créer une fabrique Direct2D multithread, puis dériver toutes les ressources Direct2D de cette fabrique. Si un thread effectue des appels [Direct3D](/windows/desktop/direct3d11/atoc-dx-graphics-direct3d-11) ou dxgi, vous devez également l’acquérir explicitement, puis appliquer le verrou Direct2D pour assurer la protection de ces appels Direct3D ou DXGI. En outre, vous devez garantir l’intégrité du contexte en utilisant une copie de ressources mutables pour chaque thread.
