---
title: Vue d’ensemble des descripteurs
description: Les descripteurs sont créés par des appels d’API et identifient les ressources.
ms.assetid: 64721226-5533-4816-865E-9429032FCC86
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17d83b2fbfd5c5df2738c61aea4f1d1115d6c874
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127293607"
---
# <a name="descriptors-overview"></a>Vue d’ensemble des descripteurs

Les descripteurs sont créés par des appels d’API et identifient les ressources.

-   [Données du descripteur](#descriptor-data)
-   [Handles de descripteur](#descriptor-handles)
-   [Descripteurs null](#null-descriptors)
-   [Descripteurs par défaut](#default-descriptors)
-   [Rubriques connexes](#related-topics)

## <a name="descriptor-data"></a>Données du descripteur

Un descripteur est un bloc de données relativement petit, qui décrit entièrement un objet au GPU, dans un format opaque spécifique au GPU. Il existe plusieurs types de descripteurs (RTVs), les vues de &mdash; stencil de profondeur (DSV), les vues de ressources de nuanceur (SRVs), les vues d’accès non ordonnées (UAVs), les vues de mémoire tampon constantes (CBVS) et les échantillonneurs.

La taille des descripteurs varie selon le matériel du GPU. Vous pouvez interroger la taille d’un SRV, d’un UAV ou d’un CBV en appelant [**ID3D12Device :: GetDescriptorHandleIncrementSize**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize). Les descripteurs sont présentés dans cette documentation sous forme d’unités indivisibles ; Voici un exemple.

![SRV, CBV, UAV et échantillonner](images/single-descriptor.png)

Les descripteurs sont créés par des appels d’API et incluent des informations telles que la ressource et les mappages MIP que vous souhaitez que le descripteur contienne.

Le pilote n’effectue pas le suivi ou ne contient pas de références aux descripteurs, c’est à l’application de s’assurer que le type de descripteur correct est utilisé et que les informations sont actuelles. Il y a une petite exception à cela ; le pilote inspecte les liaisons de la cible de rendu pour garantir le bon fonctionnement des chaînes d’échange.

Les descripteurs d’objets n’ont pas besoin d’être libérés ni libérés. Les pilotes n’attachent aucune allocation à la création d’un descripteur. Toutefois, un descripteur peut encoder des références à d’autres allocations pour lesquelles l’application possède la durée de vie. Par exemple, un descripteur pour un SRV doit contenir l’adresse virtuelle de la ressource D3D (par exemple, une texture) à laquelle le SRV fait référence. Il incombe à l’application de s’assurer qu’elle n’utilise pas de descripteur SRV lorsque la ressource D3D sous-jacente dont elle dépend a été détruite ou est en cours de modification (comme étant déclarée comme étant non résident).

Le principal moyen d’utiliser les descripteurs est de les placer dans des tas de descripteurs, qui sont la mémoire de stockage pour les descripteurs.

## <a name="descriptor-handles"></a>Handles de descripteur

Un handle de descripteur est l’adresse unique du descripteur. Elle est similaire à un pointeur, mais est opaque car son implémentation est spécifique au matériel. Le handle est unique dans les tas de descripteurs. par exemple, un tableau de handles peut référencer des descripteurs dans plusieurs tas.

Les handles d’UC sont destinés à une utilisation immédiate, tels que la copie où la source et la destination doivent être identifiées. Immédiatement après l’utilisation (par exemple, un appel à [**ID3D12GraphicsCommandList :: OMSetRenderTargets**](/windows/win32/api/d3d12/nf-d3d12-id3d12graphicscommandlist-omsetrendertargets)), ils peuvent être réutilisés, ou leur tas sous-jacent peut être supprimé.

Les handles GPU ne sont pas destinés à une utilisation immédiate &mdash; ils identifient les emplacements d’une liste de commandes, à utiliser au moment de l’exécution du GPU. Elles doivent être conservées jusqu’à ce que toutes les listes de commandes qui les référencent aient été exécutées entièrement.

Pour créer un handle de descripteur pour le début d’un segment de mémoire, après avoir créé le tas du descripteur lui-même, appelez l’une des méthodes suivantes :

-   [**ID3D12DescriptorHeap::GetCPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getcpudescriptorhandleforheapstart)
-   [**ID3D12DescriptorHeap::GetGPUDescriptorHandleForHeapStart**](/windows/desktop/api/d3d12/nf-d3d12-id3d12descriptorheap-getgpudescriptorhandleforheapstart)

Ces méthodes retournent les structures suivantes :

-   [**\_Handle de \_ descripteur de processeur D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_cpu_descriptor_handle)
-   [**\_Handle du \_ descripteur GPU D3D12 \_**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_gpu_descriptor_handle)

À mesure que la taille des descripteurs varie selon le matériel, pour obtenir l’incrément entre chaque descripteur d’un segment de mémoire, utilisez :

-   [**ID3D12Device::GetDescriptorHandleIncrementSize**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getdescriptorhandleincrementsize)

Il est possible de décaler un emplacement de départ avec un nombre d’incréments, de copier des handles et de passer des handles dans des appels d’API. Il n’est pas possible de déréférencer un handle comme s’il s’agissait d’un pointeur d’UC valide, ni d’analyser les bits dans un handle.

Certaines structures d’assistance ont été ajoutées, avec des membres d’initialisation, pour simplifier légèrement la gestion des handles.

-   [**\_Handle de \_ descripteur de processeur CD3DX12 \_**](cd3dx12-cpu-descriptor-handle.md)
-   [**\_Handle du \_ descripteur GPU CD3DX12 \_**](cd3dx12-gpu-descriptor-handle.md)

## <a name="null-descriptors"></a>Descripteurs null

Lors de la création de descripteurs à l’aide d’appels d’API, les applications passent la valeur NULL pour le pointeur de ressource dans la définition du descripteur afin d’obtenir l’effet d’une liaison Nothing lorsqu’un nuanceur y accède.

Le reste du descripteur doit être rempli autant que possible. Par exemple, dans le cas des vues des ressources de nuanceur (SRVs), le descripteur peut être utilisé pour distinguer le type d’affichage (Texture1D, Texture2D, etc.). Les paramètres numériques du descripteur de vue, tels que le nombre de des mipmaps, doivent tous être définis sur des valeurs qui sont valides pour une ressource.

Dans de nombreux cas, il existe un comportement défini pour accéder à une ressource indépendante, comme SRVs qui retournent des valeurs par défaut. Celles-ci seront respectées lors de l’accès à un descripteur NULL tant que le type d’accès du nuanceur est compatible avec le type de descripteur. Par exemple, si un nuanceur attend un Texture2D SRV et accède à un SRV NULL défini en tant que Texture1D, le comportement n’est pas défini et peut entraîner la réinitialisation de l’appareil.

En résumé, pour créer un descripteur null, transmettez `null` le paramètre de *présource* lors de la création de la vue à l’aide de méthodes telles que [**CreateShaderResourceView**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview). Pour le paramètre de description de vue *pDesc*, définissez une configuration qui fonctionnerait si la ressource n’était pas null (sinon, un incident peut se produire sur un matériel).

Toutefois, les descripteurs racine ne doivent pas avoir la valeur null.

Sur le matériel de niveau 1 (voir les [**niveaux matériels**](./hardware-support.md), tous les descripteurs liés (via les tables de descripteurs) doivent être initialisés en tant que descripteurs réels ou descripteurs null, même s’ils ne sont pas accessibles par le matériel, sinon le comportement n’est pas défini.

Sur le matériel niveau2, cela s’applique aux descripteurs CBV et UAV liés, mais pas aux descripteurs SRV.

Sur le matériel niveau3, il n’y a aucune restriction à cet effet, à condition que les descripteurs non initialisés ne soient jamais accessibles.

## <a name="default-descriptors"></a>Descripteurs par défaut

Pour créer un descripteur par défaut pour une vue particulière, transmettez un paramètre de *présource* valide à la méthode Create View (telle que [**CreateShaderResourceView**](/windows/win32/api/d3d12/nf-d3d12-id3d12device-createshaderresourceview)), mais transmettez **null** pour le paramètre *pDesc* . Par exemple, si la ressource contenait 14 mips, la vue contiendrait 14 mips. Le cas par défaut couvre le mappage le plus évident d’une ressource à une vue. Cela nécessite que la ressource soit allouée avec un nom de format qualifié complet (par exemple, **DXGI_FORMAT_R8G8B8A8_UNORM_SRGB** plutôt que **DXGI_FORMAT_R8G8B8A8_TYPELESS**).

Les descripteurs par défaut ne peuvent pas être utilisés avec une vue de structure d’accélération Raytracing, car le paramètre de *présource* fourni doit avoir la **valeur null**, et l’emplacement doit être passé via une d3d12_raytracing_acceleration_structure_srv de [**D3D12_RAYTRACING_ACCELERATION_STRUCTURE_SRV**]/Windows/Win32/API/d3d12/NS-d3d12-).

## <a name="related-topics"></a>Rubriques connexes

[Descripteurs](descriptors.md)