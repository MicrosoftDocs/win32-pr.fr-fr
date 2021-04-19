---
description: VMR avec plusieurs flux (mode de mixage)
ms.assetid: 053edb70-8631-4fe4-a137-2fe54e02ab9e
title: VMR avec plusieurs flux (mode de mixage)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a21a954b0ad78afbceabf0fde493f920961b90dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106543514"
---
# <a name="vmr-with-multiple-streams-mixing-mode"></a>VMR avec plusieurs flux (mode de mixage)

VMR peut afficher plusieurs flux d’entrée. Dans cette configuration, appelée mode de mixage, VMR charge son mélangeur et son compositeur pour effectuer le mixage et la fusion avant le rendu. Le mode de mixage peut être utilisé soit lorsque VMR est en mode fenêtre, soit en mode sans fenêtre.

Le mode de mixage requiert que le pilote Graphics prenne en charge les \_ indicateurs de capacité DDCAPS BLTFOURCC et DDCAPS \_ BLTSTRETCH (respectivement la conversion d’espace colorimétrique et l’étirement blitting). Presque tous les nouveaux pilotes graphiques ont ces fonctionnalités. En outre, le pilote doit prendre en charge la création de cibles de rendu Direct3D pour la profondeur de pixel d’affichage actuelle. Certains appareils ne prennent pas en charge les opérations Direct3D lorsque l’affichage est défini sur 24 bits par pixel. Pour plus d’informations, consultez la documentation du kit SDK DirectX Graphics.

> [!Note]  
> Lorsque VMR mélange plusieurs flux vidéo, le graphique de filtre ne se recherche pas correctement. Si vous avez besoin de Rechercher plusieurs flux vidéo, vous devez créer des graphiques de filtres distincts qui partagent le même objet Allocator-Presenter personnalisé.

 

**Configuration de VMR-7 pour plusieurs flux**

Pour afficher plusieurs flux d’entrée avec VMR-7, procédez comme suit :

1.  Avant de connecter les broches d’entrée de VMR, appelez la méthode [**IVMRFilterConfig :: SetNumberOfStreams**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setnumberofstreams) avec le nombre de flux. Ainsi, VMR charge le mélangeur et le compositeur et crée le nombre spécifié de broches d’entrée.
2.  Appelez [**IVMRFilterConfig :: SetRenderingPrefs**](/windows/desktop/api/Strmif/nf-strmif-ivmrfilterconfig-setrenderingprefs) pour spécifier diverses préférences de rendu.
3.  Connectez les broches aux filtres en amont. Le moyen le plus simple consiste à appeler [**IGraphBuilder :: RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) pour chaque flux d’entrée. Si la broche de sortie sur le filtre amont (généralement un décodeur) et que la broche d’entrée sur VMR ne peut pas s’accorder sur une connexion, une nouvelle instance de VMR avec les paramètres par défaut est créée. Cela génère une nouvelle fenêtre avec « ActiveMovie » dans la barre de titre. Pour éviter ce problème, l’application doit toujours vérifier que l’instance appropriée de VMR est utilisée en appelant une méthode telle que [**IPIN :: ConnectedTo**](/windows/desktop/api/Strmif/nf-strmif-ipin-connectedto). Une autre option consiste à ajouter le filtre source, puis à connecter les codes confidentiels à l’aide de **IGraphBuilder :: Connect**.
4.  Utilisez l’interface [**IVMRMixerControl**](/windows/desktop/api/Strmif/nn-strmif-ivmrmixercontrol) sur VMR pour contrôler les paramètres de chaque flux, tels que la valeur alpha, l’ordre de plan et le rectangle de sortie.
5.  Exécutez le graphique de filtre.

**Configuration de VMR-9 pour plusieurs flux**

Par défaut, VMR-9 crée quatre broches d’entrée. Si vous souhaitez mélanger plus de quatre flux vidéo, appelez [**IVMRFilterConfig9 :: SetNumberOfStreams**](/previous-versions/windows/desktop/api/Vmr9/nf-vmr9-ivmrfilterconfig9-setnumberofstreams) avant de connecter des broches d’entrée. Utilisez l’interface [**IVMRMixerControl9**](/previous-versions/windows/desktop/api/Vmr9/nn-vmr9-ivmrmixercontrol9) pour définir les paramètres de flux, tels que alpha, ordre de plan et position.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation du mode de mixage VMR](using-vmr-mixing-mode.md)
</dt> </dl>

 

 



