---
title: Interfaces principales (Direct3D 12 Graphics)
description: Les interfaces suivantes sont déclarées dans d3d12. h.
ms.assetid: A9BD5910-8FF2-4540-BB8E-E8EA5C10528C
ms.localizationpriority: low
ms.topic: article
ms.date: 04/19/2019
ms.custom: 19H1
ms.openlocfilehash: f204484b3565564f72e815bd21cf8e449ee55e4c
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884294"
---
# <a name="core-interfaces"></a>Interfaces de base

Les interfaces suivantes sont déclarées dans d3d12. h.

## <a name="in-this-section"></a>Contenu de cette section

| Rubrique | Description |
|-|-|
| [**ID3D12CommandAllocator**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandallocator) | Représente les allocations de stockage pour les commandes de l’unité de traitement graphique (GPU). |
| [**ID3D12CommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist) | Interface à partir de laquelle [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) hérite de. Il représente un ensemble ordonné de commandes que le GPU exécute, tout en autorisant l’extension à prendre en charge d’autres listes de commandes que celles pour les graphiques (telles que Compute et Copy). |
| [**ID3D12CommandQueue**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandqueue) | Fournit des méthodes pour envoyer des listes de commandes, synchroniser l’exécution d’une liste de commandes, instrumenter la file d’attente de commandes et mettre à jour les mappages de vignettes de ressources. |
| [**ID3D12CommandSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandsignature) | Un objet de signature de commande permet aux applications de spécifier un dessin indirect, y compris le format de la mémoire tampon, le type de commande et les liaisons de ressources à utiliser. |
| [**ID3D12DescriptorHeap**](/windows/win32/api/d3d12/nn-d3d12-id3d12descriptorheap) | Un tas de descripteur est une collection d’allocations contiguës de descripteurs, une allocation pour chaque descripteur. Les tas de descripteurs contiennent de nombreux types d’objets qui ne font pas partie d’un objet d’État du pipeline (PSO), tels que les vues des ressources de nuanceur (SRVs), les vues d’accès non ordonnées (UAVs), les vues de mémoire tampon constante (CBVs) et les échantillonneurs. |
| [**ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device) | Représente un adaptateur virtuel ; Il permet de créer des allocateurs de commandes, des listes de commandes, des files d’attente de commandes, des délimiteurs, des ressources, des objets d’état de pipeline, des tas, des signatures racines, des échantillonneurs et de nombreuses vues de ressources. |
| [**ID3D12Device1**](/windows/win32/api/d3d12/nn-d3d12-id3d12device1) | Représente un adaptateur virtuel et s’étend sur la plage des méthodes fournies par [**ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device). |
| [**ID3D12Device2**](/windows/win32/api/d3d12/nn-d3d12-id3d12device2) | Représente un adaptateur virtuel. Cette interface étend [**ID3D12Device1**](/windows/win32/api/d3d12/nn-d3d12-id3d12device1) pour créer des objets d’état de pipeline à partir des descriptions de flux d’état de pipeline. |
| [**ID3D12Device3**](/windows/win32/api/d3d12/nn-d3d12-id3d12device3) | Représente un adaptateur virtuel. Cette interface étend [**ID3D12Device2**](/windows/win32/api/d3d12/nn-d3d12-id3d12device2) pour prendre en charge la création de tas de diagnostics à usage spécial dans la mémoire système qui persistent même en cas de défaillance du GPU ou de l’appareil. |
| [**ID3D12Device4**](/windows/win32/api/d3d12/nn-d3d12-id3d12device4) | Représente un adaptateur virtuel. Cette interface étend [ID3D12Device3](/windows/win32/api/d3d12/nn-d3d12-id3d12device3). |
| [**ID3D12Device5**](/windows/win32/api/d3d12/nn-d3d12-id3d12device5) | Représente un adaptateur virtuel. Cette interface étend [ID3D12Device4](/windows/win32/api/d3d12/nn-d3d12-id3d12device4). |
| [**ID3D12Device6**](/windows/win32/api/d3d12/nn-d3d12-id3d12device6) | Représente un adaptateur virtuel. Cette interface étend [ID3D12Device5](/windows/win32/api/d3d12/nn-d3d12-id3d12device5). |
| [**ID3D12Device7**](/windows/win32/api/d3d12/nn-d3d12-id3d12device7) | Représente un adaptateur virtuel. Cette interface étend [ID3D12Device6](/windows/win32/api/d3d12/nn-d3d12-id3d12device6). |
| [**ID3D12Device8**](/windows/win32/api/d3d12/nn-d3d12-id3d12device8) | Représente un adaptateur virtuel. Cette interface étend [ID3D12Device7](/windows/win32/api/d3d12/nn-d3d12-id3d12device7). |
| [**ID3D12Device9**](/windows/win32/api/d3d12/nn-d3d12-id3d12device9) | Représente un adaptateur virtuel. Cette interface étend [ID3D12Device8](/windows/win32/api/d3d12/nn-d3d12-id3d12device8) pour ajouter des méthodes pour gérer les caches de nuanceur. |
| [**ID3D12DeviceChild**](/windows/win32/api/d3d12/nn-d3d12-id3d12devicechild) | Interface à partir de laquelle d’autres interfaces principales héritent, notamment [**ID3D12PipelineLibrary**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinelibrary), [**ID3D12CommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12commandlist), [**ID3D12Pageable**](/windows/win32/api/d3d12/nn-d3d12-id3d12pageable)et [**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature). Il fournit une méthode pour revenir à l’objet appareil sur lequel il a été créé. |
| [**ID3D12DeviceRemovedExtendedData**](/windows/win32/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddata) | Fournit l’accès au moment de l’exécution aux données de données étendues supprimées (ordinateur) de l’appareil. |
| [**ID3D12DeviceRemovedExtendedDataSettings**](/windows/win32/api/d3d12/nn-d3d12-id3d12deviceremovedextendeddatasettings) | Cette interface contrôle les paramètres de données étendus (ordinateur) supprimés de l’appareil. |
| [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence) | Représente une clôture, un objet utilisé pour la synchronisation de l’UC et un ou plusieurs GPU.  |
| [**ID3D12Fence1**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence1) | Représente une clôture. Cette interface étend [**ID3D12Fence**](/windows/win32/api/d3d12/nn-d3d12-id3d12fence)et prend en charge la récupération des indicateurs utilisés pour créer la limite d’origine.  |
| [**ID3D12GraphicsCommandList**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist) | Encapsule une liste de commandes graphiques pour le rendu. Comprend des API pour l’instrumentation de l’exécution de la liste de commandes, ainsi que pour la définition et l’effacement de l’état du pipeline. |
| [**ID3D12GraphicsCommandList1**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist1) | Encapsule une liste de commandes graphiques pour le rendu, en étendant le inteface pour prendre en charge les positions programmables, les copies atomiques pour l’implémentation des techniques de verrouillage tardif et les tests de limites de profondeur facultatifs. |
| [**ID3D12GraphicsCommandList2**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist2) | Encapsule une liste de commandes graphiques pour le rendu, en étendant l’interface pour prendre en charge l’écriture de valeurs immédiates directement dans une mémoire tampon. |
| [**ID3D12GraphicsCommandList3**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist3) | Encapsule une liste de commandes graphiques pour le rendu. |
| [**ID3D12GraphicsCommandList4**](/windows/win32/api/d3d12/nn-d3d12-id3d12graphicscommandlist4) | Encapsule une liste de commandes graphiques pour le rendu, en étendant l’interface pour prendre en charge le suivi de rayon et les passes de rendu. |
| [**ID3D12Heap**](/windows/win32/api/d3d12/nn-d3d12-id3d12heap) | Un segment de mémoire est une abstraction de l’allocation de mémoire contiguë, utilisée pour gérer la mémoire physique. Ce segment de mémoire peut être utilisé avec les objets [**ID3D12Resource**](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) pour prendre en charge les ressources placées ou les ressources réservées. |
| [**ID3D12LifetimeOwner**](/windows/win32/api/d3d12/nn-d3d12-id3d12lifetimeowner) | Représente un rappel défini par l’application utilisé pour être averti des modifications de durée de vie d’un objet. |
| [**ID3D12LifetimeTracker**](/windows/win32/api/d3d12/nn-d3d12-id3d12lifetimetracker) | Représente les fonctionnalités de contrôle de la durée de vie d’un objet suivi de durée de vie. |
| [**ID3D12MetaCommand**](/windows/win32/api/d3d12/nn-d3d12-id3d12metacommand) | Représente une commande meta. Une commande Meta est un objet Direct3D 12 qui représente un algorithme accéléré par des fournisseurs de matériel indépendants (IHV). Il s’agit d’une référence opaque à un générateur de commandes implémenté par le pilote. |
| [**ID3D12Object**](/windows/win32/api/d3d12/nn-d3d12-id3d12object) | Interface à partir de laquelle [**ID3D12Device**](/windows/win32/api/d3d12/nn-d3d12-id3d12device) et [**ID3D12DeviceChild**](/windows/win32/api/d3d12/nn-d3d12-id3d12devicechild) héritent de. Il fournit des méthodes pour associer des données privées et annoter des noms d’objets. |
| [**ID3D12Pageable**](/windows/win32/api/d3d12/nn-d3d12-id3d12pageable) | Interface à partir de laquelle de nombreuses autres interfaces principales héritent. Elle indique que le type d’objet encapsule une certaine quantité de mémoire accessible par le GPU ; mais n’indique pas fortement si l’application peut manipuler la résidence de l’objet.  |
| [**ID3D12PipelineLibrary**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinelibrary) | Gère une bibliothèque de pipelines, en particulier le chargement et la récupération de objets PSO individuels. |
| [**ID3D12PipelineLibrary1**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinelibrary1) | Gère une bibliothèque de pipelines. Cette interface étend [**ID3D12PipelineLibrary**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinelibrary) pour charger les objets PSO à partir d’une description de flux d’État du pipeline. |
| [**ID3D12PipelineState**](/windows/win32/api/d3d12/nn-d3d12-id3d12pipelinestate) | Représente l’état de tous les nuanceurs actuellement définis, ainsi que certains objets d’état de fonction fixes. |
| [**ID3D12QueryHeap**](/windows/win32/api/d3d12/nn-d3d12-id3d12queryheap) | Gère un segment de mémoire de requête. Un segment de mémoire de requête contient un tableau de requêtes, référencé par des index. |
| [**ID3D12Resource**](/windows/win32/api/d3d12/nn-d3d12-id3d12resource) | Encapsule une capacité généralisée du processeur et du GPU à lire et à écrire dans la mémoire physique, ou les tas. Il contient des abstractions pour l’organisation et la manipulation de tableaux de données simples, ainsi que des données multidimensionnelles optimisées pour l’échantillonnage de nuanceur. |
| [**ID3D12RootSignature**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignature) | La signature racine définit les ressources qui sont liées au pipeline Graphics. Une signature racine est configurée par les listes de commandes App et Links pour les ressources requises par les nuanceurs. Actuellement, il existe un graphique et une signature racine de calcul par application. |
| [**ID3D12RootSignatureDeserializer**](/windows/win32/api/d3d12/nn-d3d12-id3d12rootsignaturedeserializer) | Contient une méthode pour retourner la structure de données [**D3D12-root-signature-DESC**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_signature_desc) désérialisée d’une signature racine sérialisée version 1,0.  |
| [**ID3D12SDKConfiguration**](/windows/win32/api/d3d12/nn-d3d12-id3d12sdkconfiguration) | Fournit des méthodes de configuration du kit de développement logiciel. |
| [**ID3D12ShaderCacheSession**](/windows/win32/api/d3d12/nn-d3d12-id3d12shadercachesession) | Représente une session de cache du nuanceur. |
| [**ID3D12StateObject**](/windows/win32/api/d3d12/nn-d3d12-id3d12stateobject) | Représente une quantité variable d’état de configuration, y compris les nuanceurs, qu’une application gère en tant qu’unité unique et qui est donnée à un pilote de manière atomique à traiter, telle que la compilation ou l’optimisation.  |
| [**ID3D12StateObjectProperties**](/windows/win32/api/d3d12/nn-d3d12-id3d12stateobjectproperties) | Fournit des méthodes pour obtenir et définir les propriétés d’un [**ID3D12StateObject**](/windows/win32/api/d3d12/nn-d3d12-id3d12stateobject).  |
| [**ID3D12Tools**](/windows/win32/api/d3d12/nn-d3d12-id3d12tools) | Cette interface permet de configurer le runtime pour les outils tels que PIX. Il n’est pas prévu ou pris en charge pour un autre scénario. |
| [**ID3D12VersionedRootSignatureDeserializer**](/windows/win32/api/d3d12/nn-d3d12-id3d12versionedrootsignaturedeserializer) | Contient des méthodes pour retourner la structure de données [**D3D12-root-signature-DESC1**](/windows/win32/api/d3d12/ns-d3d12-d3d12_root_signature_desc1) désérialisée, de n’importe quelle version d’une signature racine sérialisée.  |

## <a name="related-topics"></a>Rubriques connexes

* [Référence de base](direct3d-12-core-reference.md)
* [Informations de référence sur Direct3D 12](direct3d-12-reference.md)
* [Hiérarchie des interfaces](interface-hierarchy.md)
