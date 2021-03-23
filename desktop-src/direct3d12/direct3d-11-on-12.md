---
title: Direct3D 11 sur 12
description: D3D11On12 est un mécanisme qui permet aux développeurs d’utiliser des interfaces et des objets D3D11 pour piloter l’API D3D12.
ms.assetid: 8412D8BB-B6DD-471E-AAB2-A81121FB0FFA
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62816ea0d7d7969cd56e0a9f525b2c412c8da182
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104548499"
---
# <a name="direct3d-11-on-12"></a>Direct3D 11 sur 12

D3D11On12 est un mécanisme qui permet aux développeurs d’utiliser des interfaces et des objets D3D11 pour piloter l’API D3D12. D3D11on12 permet aux composants écrits à l’aide de D3D11 (par exemple, du texte et de l’interface utilisateur D2D) de fonctionner conjointement avec des composants écrits ciblant l’API D3D12. D3D11on12 permet également le portage incrémentiel d’une application de D3D11 vers D3D12, en permettant aux parties de l’application de continuer à cibler les D3D11 pour plus de simplicité, tandis que d’autres ciblent D3D12 pour les performances, tout en ayant toujours un rendu complet et correct. D3D11On12 simplifie l’utilisation de techniques d’interopérabilité pour partager des ressources et synchroniser le travail entre les deux API.

-   [Initialisation de D3D11On12](#initializing-d3d11on12)
-   [Exemple d’utilisation](#example-usage)
-   [Contexte](#background)
-   [Nettoyage](#cleaning-up)
-   [Limitations](#limitations)
-   [API](#apis)
-   [Rubriques connexes](#related-topics)

## <a name="initializing-d3d11on12"></a>Initialisation de D3D11On12

Pour commencer à utiliser D3D11On12, la première étape consiste à créer un appareil D3D12 et une file d’attente de commandes. Ces objets sont fournis comme entrée à la méthode d’initialisation [**D3D11On12CreateDevice**](/windows/desktop/api/d3d11on12/nf-d3d11on12-d3d11on12createdevice). Vous pouvez considérer cette méthode comme la création d’un appareil D3D11 avec le type de pilote en mode D3D \_ \_ \_ 11ON12, où le pilote d3d11 est responsable de la création d’objets et de l’envoi de listes de commandes à l’API D3D12.

Une fois que vous disposez d’un appareil D3D11 et d’un contexte immédiat, vous pouvez `QueryInterface` désactiver l’appareil pour l’interface [**ID3D11On12Device**](/windows/desktop/api/d3d11on12/nn-d3d11on12-id3d11on12device) . Il s’agit de l’interface principale utilisée pour l’interopérabilité entre D3D11 et D3D12. Afin que le contexte de périphérique D3D11 et les listes de commandes D3D12 fonctionnent sur les mêmes ressources, il est nécessaire de créer des « ressources encapsulées » à l’aide de l’API [**CreateWrappedResource**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-createwrappedresource) . Cette méthode « promeut » une ressource D3D12 pour être compréhensible dans D3D11. Une ressource encapsulée commence à l’état « acquis », une propriété qui est manipulée par les méthodes [**AcquireWrappedResources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-acquirewrappedresources) et [**ReleaseWrappedResources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-releasewrappedresources) .

## <a name="example-usage"></a>Exemple d’utilisation

L’utilisation classique de D3D11On12 serait d’utiliser D2D pour afficher du texte ou des images sur une mémoire tampon d’arrière-plan D3D12. Pour obtenir un exemple de code, consultez l’exemple D3D11On12. Voici un plan approximatif des étapes à suivre pour effectuer cette opération :

-   Créez un appareil D3D12 ([**D3D12CreateDevice**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice)) et une chaîne d’échange D3D12 ([**CreateSwapChain**](/windows/desktop/api/dxgi/nf-dxgi-idxgifactory-createswapchain) avec un [**ID3D12CommandQueue**](/windows/desktop/api/d3d12/nn-d3d12-id3d12commandqueue) comme entrée).
-   Créez un appareil D3D11On12 à l’aide de l’appareil D3D12 et de la même file d’attente de commandes en entrée.
-   Récupérez les mémoires tampons d’arrière-plan de la chaîne de permutation et créez des ressources encapsulées D3D11 pour chacune d’elles. L’état d’entrée utilisé doit être la dernière façon dont D3D12 l’a utilisé (par exemple, \_ la cible de rendu) et l’état de sortie doit être la manière dont D3D12 l’utilise une fois d3d11 terminée (par exemple, présent).
-   Initialisez D2D et fournissez les ressources D3D11 encapsulées à D2D pour préparer le rendu.

Ensuite, sur chaque trame, procédez comme suit :

-   Effectuez le rendu dans la mémoire tampon d’arrière-plan actuelle de la chaîne d’échange à l’aide d’une liste de commandes D3D12 et exécutez-la.
-   Acquérir la ressource encapsulée de la mémoire tampon d’arrière-plan ([**AcquireWrappedResources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-acquirewrappedresources)) actuelle.
-   Émettez des commandes de rendu D2D.
-   Libérer la ressource encapsulée ([**ReleaseWrappedResources**](/windows/desktop/api/d3d11on12/nf-d3d11on12-id3d11on12device-releasewrappedresources)).
-   Videz le contexte immédiat D3D11.
-   Présent ([**IDXGISwapChain1 ::P resent1**](/windows/desktop/api/dxgi1_2/nf-dxgi1_2-idxgiswapchain1-present1)).

## <a name="background"></a>Arrière-plan

D3D11On12 fonctionne systématiquement. Chaque appel d’API D3D11 passe par la validation d’exécution classique et passe au pilote. Au niveau de la couche du pilote, le pilote 11on12 spécial enregistre les opérations de rendu des États et des problèmes dans les listes de commandes D3D12. Ces listes de commandes sont envoyées si nécessaire (par exemple, une requête `GetData` ou une ressource `Map` peut nécessiter le vidage des commandes) ou comme demandé par Flush. La création d’un objet D3D11 entraîne généralement la création de l’objet D3D12 correspondant. Certaines opérations de rendu de fonction fixe dans D3D11 telles que `GenerateMips` ou ne `DrawAuto` sont pas prises en charge dans D3D12, de sorte que D3D11On12 les émule à l’aide de nuanceurs et de ressources supplémentaires.

Pour l’interopérabilité, il est important de comprendre comment D3D11On12 interagit avec les objets D3D12 que l’application a créés et fournis. Pour garantir que le travail s’effectue dans le bon ordre, le contexte immédiat D3D11 doit être vidé avant que du travail D3D12 supplémentaire puisse être soumis à cette file d’attente. Il est également important de s’assurer que la file d’attente donnée à D3D11On12 doit être drainable à tout moment. Cela signifie que toutes les attentes sur la file d’attente doivent être satisfaites, même si le thread de rendu D3D11 est bloqué indéfiniment. Faites attention à ne pas dépendre du moment où D3D11On12 insère ou attend, car cela peut changer dans les versions ultérieures. En outre, D3D11On12 suit et manipule les États des ressources de manière autonome. La seule façon d’assurer la cohérence des transitions d’état consiste à utiliser les API Acquire/Release pour manipuler le suivi d’État afin qu’il corresponde aux besoins de l’application.

## <a name="cleaning-up"></a>Nettoyage

Pour libérer une ressource encapsulée D3D11On12, deux éléments doivent se produire dans cet ordre :

-   Toutes les références à la ressource, y compris toutes les vues de la ressource, doivent être libérées.
-   Le traitement de la destruction différée doit avoir lieu. La façon la plus simple de vous assurer que cela se produit consiste à appeler l’API de contexte immédiat `Flush` .

Une fois ces deux étapes terminées, toutes les références prises par la ressource encapsulée doivent être libérées et la ressource D3D12 appartient exclusivement au composant D3D12. Sachez que D3D12 a toujours besoin d’attendre la fin du GPU avant de libérer complètement une ressource. Veillez donc à conserver une référence sur la ressource avant d’effectuer les deux étapes ci-dessus, sauf si vous avez déjà confirmé que le GPU n’utilise plus la ressource.

Toutes les autres ressources ou objets créés par D3D11On12 seront nettoyés au moment opportun, lorsque le GPU aura fini de les utiliser, en utilisant le mécanisme de destruction différée D3D11's. Toutefois, si vous tentez de libérer l’appareil D3D11On12 alors que le GPU est toujours en cours d’exécution, la destruction peut se bloquer jusqu’à ce que le GPU se termine.

## <a name="limitations"></a>Limites

La couche D3D11On12 implémente un très grand sous-ensemble de l’API D3D11, mais il existe des lacunes connues (en plus des bogues dans l’implémentation qui peuvent provoquer un rendu incorrect).

À partir de Windows 10, version 1809 (10,0 ; Build 17763), à condition que D3D11On12 s’exécute sur un pilote qui prend en charge le modèle de nuanceur 6,0 ou ultérieur, il peut exécuter des nuanceurs qui utilisent des interfaces. Dans les versions antérieures de Windows, la fonctionnalité d’interfaces de nuanceur n’est pas implémentée dans D3D11On12 et la tentative d’utilisation de la fonctionnalité provoquera des erreurs et des messages de débogage.

À partir de Windows 10, version 1803 (10,0 ; Build 17134), les chaînes de permutation sont prises en charge sur les appareils D3D11On12. Dans les versions antérieures de Windows, elles ne le sont pas.

D3D11On12 n’a pas été optimisé pour les performances. Il y aura probablement une surcharge de processeur modérée par rapport à un pilote D3D11 standard, une surcharge de GPU minimale et une surcharge de mémoire importante est connue. Par conséquent, il n’est pas recommandé d’utiliser D3D11On12 pour les scènes 3D complexes, et c’est plutôt recommandé pour les scènes simples ou le rendu 2D.

## <a name="apis"></a>API

Les API qui composent la couche 11on12 sont décrites dans [référence 11on12](direct3d-11on12-reference.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[D2D à l’aide d’une procédure pas à pas D3D11on12](d2d-using-d3d11on12.md)
</dt> <dt>

[Comprendre Direct3D 12](directx-12-getting-started.md)
</dt> <dt>

[Utilisation de Direct3D 11, Direct3D 10 et Direct2D](direct3d-12-interop.md)
</dt> </dl>

 

 