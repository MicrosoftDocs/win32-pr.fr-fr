---
description: Fourniture d’un Allocator-Presenter personnalisé pour VMR-9
ms.assetid: 61bb6b0d-25b5-481b-a241-74c6e421f109
title: Fourniture d’un Allocator-Presenter personnalisé pour VMR-9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f004e119fc1cbfc167c2130852a4f59700706fcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106527247"
---
# <a name="supplying-a-custom-allocator-presenter-for-vmr-9"></a>Fourniture d’un Allocator-Presenter personnalisé pour VMR-9

Pour utiliser un Allocator-présentateur personnalisé avec le filtre de mixage vidéo 9 (VMR-9), procédez comme suit :

1.  Implémentez une classe qui prend en charge les interfaces [**IVMRSurfaceAllocator9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9) et [**IVMRImagePresenter9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrimagepresenter9) .
2.  Appelez **QueryInterface** sur le filtre VMR-9 pour l’interface [**IVMRFilterConfig9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrfilterconfig9) .
3.  Appelez la méthode [**IVMRFilterConfig9 :: SetRenderingMode**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setrenderingmode) et transmettez l’indicateur de **\_ rendu VMR9Mode** .
4.  **QueryInterface** sur le filtre VMR-9 pour l’interface [**IVMRSurfaceAllocatorNotify9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9) .
5.  Appelez la méthode [**IVMRSurfaceAllocatorNotify9 :: AdviseSurfaceAllocator**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-advisesurfaceallocator) et transmettez un pointeur vers la méthode [**IVMRSurfaceAllocator9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocator9) de l’Allocator-presenter.
6.  Appelez la méthode [**IVMRSurfaceAllocator9 :: AdviseNotify**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocator9-advisenotify) de l’Allocator-Presenter et transmettez un pointeur vers l’interface [**IVMRSURFACEALLOCATORNOTIFY9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrsurfaceallocatornotify9) du filtre VMR-9.
7.  Dans votre implémentation de [**IVMRSurfaceAllocator9 :: AdviseNotify**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocator9-advisenotify), appelez [**IVMRSurfaceAllocatorNotify9 :: SetD3DDevice**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-setd3ddevice) Pass dans un pointeur vers l’appareil Direct3D et un handle vers le moniteur dans lequel la vidéo apparaît.
8.  Dans votre implémentation de la méthode [**IVMRSurfaceAllocator9 :: InitializeDevice**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocator9-initializedevice) , créez des surfaces Direct3D qui correspondent aux paramètres fournis dans la méthode **InitializeDevice** . Si vous le souhaitez, vous pouvez utiliser la méthode [**IVMRSurfaceAllocatorNotify9 :: AllocateSurfaceHelper**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper) du filtre VMR-9 pour allouer ces surfaces. Stocke les pointeurs de surface dans un tableau.
    > [!Note]  
    > Si vous souhaitez que VMR-9 dessine les images vidéo sur une surface de texture, ajoutez l’indicateur **VMR9AllocFlag \_ TextureSurface** à la structure [**VMR9AllocationInfo**](/previous-versions/windows/desktop/api/Vmr9/ns-vmr9-vmr9allocationinfo) . Si l’appareil ne prend pas en charge les textures au format vidéo natif, vous devrez peut-être créer une surface de texture distincte, puis copier les images vidéo de la surface vidéo vers la texture.

     

9.  Pendant la diffusion en continu, VMR-9 obtient des surfaces de l’Allocator-Presenter en appelant la méthode [**IVMRSurfaceAllocator9 :: GetSurface**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocator9-getsurface) . VMR-9 spécifie la surface par son index dans le tableau de surface (étape 8).
10. Présentez l’image lorsque VMR-9 appelle la méthode [**IVMRImagePresenter9 ::P resentimage**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrimagepresenter9-presentimage) . Les paramètres incluent un pointeur vers la surface Direct3D qui contient l’image vidéo.
11. Si le périphérique Direct3D est perdu à tout moment, l’allocateur-Presenter doit restaurer l’appareil et recréer les surfaces. Par exemple, l’appareil peut être perdu si le mode d’affichage change ou si l’utilisateur déplace la fenêtre vers un autre moniteur. Si l’appareil Direct3D change, appelez la méthode [**IVMRSurfaceAllocatorNotify9 :: ChangeD3DDevice**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-changed3ddevice) du filtre VMR-9.
12. En cas d’arrêt de la diffusion en continu, VMR-9 appelle la méthode [**IVMRSurfaceAllocator9 :: TerminateDevice**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocator9-terminatedevice) . L’Allocator-Presenter doit libérer toutes ses ressources Direct3D.

Il existe quelques différences entre VMR-7 et VMR-9 dans le mode de gestion des allocateurs personnalisés :

-   La méthode [**AllocateSurfaceHelper**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper) du filtre VMR-9 est disponible pour l’allocateur-Presenter à utiliser lors de l’allocation des surfaces. Cette méthode permet à un allocateur-présentateur personnalisé de transférer des appels à l’Allocator-présentateur par défaut. Pour cette raison, le CLSID de l’allocateur par défaut du filtre VMR-9 n’est pas publié.
-   Contrairement à VMR-7, VMR-9 ne fournit pas d’allocateur de mode exclusif DirectDraw spécial-présentateur. La méthode [**IVMRSurfaceAllocatorNotify9 :: AllocateSurfaceHelper**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper) rend cet objet inutile.
-   Pour la vidéo entrelacée, VMR-9 réintègre toujours la vidéo avant de présenter l’image. L’Allocator-Presenter n’est plus responsable du désentrelacement de l’image avant de l’afficher.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mode de lecture non rendu VMR (Allocator personnalisé-présentateur)](vmr-renderless-playback-mode--custom-allocator-presenters.md)
</dt> </dl>

 

 



