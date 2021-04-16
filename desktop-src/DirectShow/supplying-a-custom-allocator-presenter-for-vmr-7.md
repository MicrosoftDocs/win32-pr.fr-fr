---
description: Fourniture d’un Allocator-Presenter personnalisé pour VMR-7
ms.assetid: 19b43c9b-2578-418f-b03b-af7c7a3a46e4
title: Fourniture d’un Allocator-Presenter personnalisé pour VMR-7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e79f191401f990214b2551f9210fab4dfe4d43b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104564241"
---
# <a name="supplying-a-custom-allocator-presenter-for-vmr-7"></a>Fourniture d’un Allocator-Presenter personnalisé pour VMR-7

L’Allocator-Presenter est chargé d’allouer des surfaces DirectDraw et de présenter les images vidéo pour le rendu. Dans la grande majorité des scénarios, les fonctionnalités de l’allocateur par défaut-Presenter sont plus que suffisantes pour les besoins d’une application. Toutefois, en branchant un Allocator-Presenter personnalisé, une application peut obtenir un accès direct aux bits vidéo et contrôler complètement le processus de rendu. Le compromis pour cette puissance accrue est que l’application doit gérer la complexité supplémentaire de la gestion de la surface de DirectDraw.

![utilisation d’un allocateur personnalisé-présentateur](images/custom-ap.png)

La figure précédente montre les interfaces de communication utilisées par VMR et l’Allocator-presenter. Un Allocator-Presenter personnalisé qui remplace toutes les fonctionnalités d’allocation et de présentation par défaut doit implémenter les interfaces [**IVMRImagePresenter**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter) et [**IVMRSurfaceAllocator**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocator) , et éventuellement [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol).

Pour remplacer l’Allocator-Presenter par défaut, une application appelle la méthode [**IVMRSurfaceAllocatorNotify :: AdviseSurfaceAllocator**](/windows/desktop/api/Strmif/nf-strmif-ivmrsurfaceallocatornotify-advisesurfaceallocator) et passe un pointeur vers le nouvel Allocator-presenter. En réponse à cet appel, VMR appellera la méthode [**IVMRSurfaceAllocator :: AdviseNotify**](/windows/desktop/api/Strmif/nf-strmif-ivmrsurfaceallocator-advisenotify) de l’Allocator-Presenter pour fournir le pointeur à l’interface [**IVMRSurfaceAllocatorNotify**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocatornotify) de VMR. L’Allocator-Presenter utilise ce pointeur d’interface lors du passage des événements à VMR avec la méthode [**IVMRSurfaceAllocatorNotify :: NotifyEvent**](/windows/desktop/api/Strmif/nf-strmif-ivmrsurfaceallocatornotify-notifyevent) .

En guise de solution alternative, une application peut utiliser à la fois son propre allocateur-présentateur et l’allocateur par défaut-présentateur. Dans ce scénario, l’allocateur personnalisé-Presenter gère uniquement les appels où des fonctionnalités personnalisées sont nécessaires et passe le reste des appels de VMR à l’Allocator par défaut-presenter. Dans de nombreux cas, il est seulement nécessaire de remplacer l’interface [**IVMRImagePresenter**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter) .

![utilisation de deux aslocateurs-présentateurs](images/custom-ap2.png)

Pour utiliser à la fois un Allocator personnalisé-présentateur et l’Allocator-présentateur par défaut, une application appelle d’abord [**IVMRSurfaceAllocatorNotify :: AdviseSurfaceAllocator**](/windows/desktop/api/Strmif/nf-strmif-ivmrsurfaceallocatornotify-advisesurfaceallocator) pour fournir un pointeur vers le nouvel Allocator-présentateur. Cela entraîne la destruction de l’Allocator-Presenter par défaut. l’application doit donc créer une autre instance de celle-ci en appelant **QueryInterface** sur VMR et en demandant l’interface [**IVMRSurfaceAllocator**](/windows/desktop/api/Strmif/nn-strmif-ivmrsurfaceallocator) . Comme indiqué dans l’illustration précédente, l’allocateur-présentateur personnalisé remplace les méthodes de l’interface [**IVMRImagePresenter**](/windows/desktop/api/Strmif/nn-strmif-ivmrimagepresenter) et passe simplement tous les appels à l’interface **IVMRSurfaceAllocator** par le biais de l’implémentation par défaut. La figure montre également l’interface [**IVMRWindowlessControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrwindowlesscontrol) comme étant implémentée sur l’Allocator-presenter.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fourniture d’un Allocator-Presenter personnalisé pour VMR-9](supplying-a-custom-allocator-presenter-for-vmr-9.md)
</dt> <dt>

[Mode de lecture non rendu VMR (Allocator personnalisé-présentateur)](vmr-renderless-playback-mode--custom-allocator-presenters.md)
</dt> </dl>

 

 



