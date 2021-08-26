---
description: 'l’interface IRenderEngine restitue un projet de Services de modification DirectShow (DES) en construisant un graphique de filtre à partir d’une chronologie. DES fournit deux composants qui implémentent cette interface : le moteur de rendu de base crée une sortie non compressée.'
ms.assetid: e2a91b34-ee4d-405e-81bf-29d15ea6342a
title: Interface IRenderEngine (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IRenderEngine
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: a13d51eb41a917dc4790c75a8a1f8a881dbcb8489364722ff8805bdf26fc77f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051309"
---
# <a name="irenderengine-interface"></a>Interface IRenderEngine

> [!Note]  
> \[Déconseillé. Cette API peut être supprimée des futures versions de Windows.\]

 

l' `IRenderEngine` interface restitue un projet de [Services d’édition DirectShow](directshow-editing-services.md) en construisant un graphique de filtre à partir d’une chronologie.

DES fournit deux composants qui implémentent cette interface :

-   Le *moteur de rendu de base* crée une sortie non compressée. Vous pouvez utiliser la sortie pour l’aperçu ou l’acheminer via des filtres de compression et l’écrire dans un fichier.
-   Le *moteur de rendu intelligent* crée une sortie compressée à l’aide de la *recompression intelligente*. Avec la recompression intelligente, un fichier source est recompressé uniquement si son format diffère du format de sortie. Une source avec un format correspondant est écrite directement dans le fichier de sortie. Selon le scénario, la recompression intelligente peut améliorer beaucoup le temps de rendu.

Le moteur de rendu intelligent prend également en charge l’interface [**ISmartRenderEngine**](ismartrenderengine.md) .

Bien qu’une application puisse créer un graphique de filtre et la passer à un moteur de rendu, le scénario classique consiste à ce que le moteur de rendu crée le graphique de filtre. La création du graphique est un processus en deux étapes. Tout d’abord, générez le serveur frontal en appelant la méthode [**IRenderEngine :: ConnectFrontEnd**](irenderengine-connectfrontend.md) . Connectez ensuite les broches de sortie du serveur frontal aux filtres de rendu souhaités :

-   Convertisseurs vidéo et audio pour la version préliminaire, ou
-   Compresseurs, multiplexeurs et Writers de fichiers pour générer la sortie finale.

## <a name="members"></a>Membres

L’interface **IRenderEngine** hérite de l’interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **IRenderEngine** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IRenderEngine** possède ces méthodes.



| Méthode                                                                             | Description                                                                           |
|:-----------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**Valider**](irenderengine-commit.md)                                             | Non implémenté.<br/>                                                           |
| [**ConnectFrontEnd**](irenderengine-connectfrontend.md)                           | Génère la partie frontale du graphique de filtre à partir de la chronologie actuelle.<br/>        |
| [**Annulation**](irenderengine-decommit.md)                                         | Non implémenté.<br/>                                                           |
| [**DoSmartRecompression**](irenderengine-dosmartrecompression.md)                 | Non pris en charge.<br/>                                                             |
| [**GetCaps**](irenderengine-getcaps.md)                                           | Non implémenté.<br/>                                                           |
| [**GetFilterGraph**](irenderengine-getfiltergraph.md)                             | Récupère le graphique de filtre que le moteur de rendu a construit, le cas échéant.<br/> |
| [**GetGroupOutputPin**](irenderengine-getgroupoutputpin.md)                       | Récupère la broche de sortie pour le groupe spécifié.<br/>                          |
| [**GetTimelineObject**](irenderengine-gettimelineobject.md)                       | Récupère la chronologie que le moteur de rendu utilise actuellement.<br/>          |
| [**GetVendorString**](irenderengine-getvendorstring.md)                           | Récupère la chaîne du fournisseur.<br/>                                               |
| [**RenderOutputPins**](irenderengine-renderoutputpins.md)                         | Crée la partie aperçu du graphique de filtre.<br/>                        |
| [**ScrapIt**](irenderengine-scrapit.md)                                           | Ignore le graphique de filtre du moteur de rendu et tous les objets associés.<br/>      |
| [**SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md)         | Définit le niveau de reconnexion dynamique lors du rendu.<br/>                   |
| [**SetFilterGraph**](irenderengine-setfiltergraph.md)                             | Spécifie un graphique de filtre que le moteur de rendu doit utiliser.<br/>                     |
| [**SetInterestRange**](irenderengine-setinterestrange.md)                         | Non pris en charge.<br/>                                                             |
| [**SetInterestRange2**](irenderengine-setinterestrange2.md)                       | Non pris en charge.<br/>                                                             |
| [**SetRenderRange**](irenderengine-setrenderrange.md)                             | Définit la plage de temps à restituer.<br/>                                     |
| [**SetRenderRange2**](irenderengine-setrenderrange2.md)                           | Définit la plage de temps à restituer, sous la forme d’un **double**.<br/>                    |
| [**SetSourceConnectCallback**](irenderengine-setsourceconnectcallback.md)         | Non pris en charge.<br/>                                                             |
| [**SetSourceNameValidation**](irenderengine-setsourcenamevalidation.md)           | Spécifie comment le moteur de rendu valide les noms de fichiers.<br/>                      |
| [**SetTimelineObject**](irenderengine-settimelineobject.md)                       | Définit la chronologie que le moteur de rendu utilise.<br/>                            |
| [**UseInSmartRecompressionGraph**](irenderengine-useinsmartrecompressiongraph.md) | Non pris en charge.<br/>                                                             |



 

## <a name="remarks"></a>Remarques

> [!Note]  
> Le fichier d’en-tête qedit. h n’est pas compatible avec les en-têtes Direct3D ultérieurs à la version 7.

 

> [!Note]  
> pour obtenir Qedit. h, téléchargez la [mise à jour Microsoft Windows SDK pour Windows Vista et .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx). Qedit. h n’est pas disponible dans le Microsoft Windows SDK pour Windows 7 et .NET Framework 3,5 Service Pack 1.

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|-----------------------------------------------------------------------------------------|
| En-tête<br/>  | <dl> <dt>Qedit. h</dt> </dl>      |
| Bibliothèque<br/> | <dl> <dt>Strmiids. lib</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Rendu d’un Project](rendering-a-project.md)
</dt> </dl>

 

 
