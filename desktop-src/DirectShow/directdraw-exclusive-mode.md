---
description: Mode exclusif DirectDraw
ms.assetid: 3ef4f267-4dc2-421b-ade4-6b1efa364733
title: Mode exclusif DirectDraw
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e5b04bae9c3221a4acee9900c5f19ba4e9b0d54
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106513116"
---
# <a name="directdraw-exclusive-mode"></a>Mode exclusif DirectDraw

> [!Note]  
> Cette rubrique s’applique uniquement à VMR-7. Dans VMR-9, vous activez le mode exclusif en fournissant votre propre allocateur en mode exclusif-présentateur. Cela est relativement simple si vous utilisez la méthode [**IVMRSurfaceAllocatorNotify9 :: AllocateSurfaceHelper**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrsurfaceallocatornotify9-allocatesurfacehelper) . L’exemple VMR9Allocator montre comment implémenter un Allocator-Presenter personnalisé.

 

En mode exclusif DirectDraw, une application prend le contrôle exclusif du matériel graphique. Cela est utile pour les applications telles que les jeux, ou peut-être des applications vidéo plein écran. Normalement, VMR crée les objets DirectDraw et définit le niveau coopératif sur normal. Toutefois, pour exécuter VMR en mode exclusif DirectDraw, l’application elle-même doit créer l’objet DirectDraw et la surface principale, puis appeler **SetCooperativeLevel** pour spécifier le mode exclusif.

VMR possède un Allocator-Presenter spécial qui lui permet de s’exécuter en mode exclusif DirectDraw. Pour configurer VMR afin d’utiliser cet Allocator-presenter :

1.  Créez le graphique de filtre et ajoutez VMR à celui-ci à l’aide de la méthode [**IFilterGraph :: AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) . Pour obtenir un exemple de code, consultez [mode sans fenêtre VMR](vmr-windowless-mode.md).
2.  Créer l’allocateur en mode exclusif-présentateur :
    ```C++
    IVMRImagePresenterExclModeConfig* pExclModeConfig;
    CoCreateInstance(
            CLSID_AllocPresenterDDXclMode,
            NULL,
            CLSCTX_INPROC_SERVER,
            IID_IVMRImagePresenterExclModeConfig,
            (void**)&pExclModeConfig
            );
    ```

    

3.  Configurer le nouvel Allocator-présentateur :
    ```C++
    pExclModeConfig->SetXlcModeDDObjAndPrimarySurface(...);
    ```

    

4.  Branchez le nouvel Allocator-Presenter dans VMR.
5.  Générez le reste du graphique de filtre de la manière habituelle.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Modes de fonctionnement VMR](vmr-modes-of-operation.md)
</dt> </dl>

 

 



