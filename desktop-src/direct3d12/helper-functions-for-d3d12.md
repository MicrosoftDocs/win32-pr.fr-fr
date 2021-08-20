---
title: Fonctions d’assistance pour Direct3D 12
description: Ces fonctions d’assistance permettent notamment de gérer des sous-ressources et sont déclarées dans `d3dx12.h` .
ms.assetid: E40B20D9-C700-4142-BBF3-7A5086E34712
keywords:
- Fonctions d’assistance
- d3dx12. h
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce9434bf916d7cb92116cdf4f7f6d86363b2eb51
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/13/2021
ms.locfileid: "121813185"
---
# <a name="helper-functions-for-direct3d-12"></a>Fonctions d’assistance pour Direct3D 12

Ces fonctions d’assistance permettent notamment de gérer des sous-ressources et sont déclarées dans `d3dx12.h` .

`d3dx12.h` est disponible séparément des en-têtes Direct3D 12. Vous pouvez télécharger `d3dx12.h` à partir de [la bibliothèque d’assistance D3D12](https://github.com/microsoft/DirectX-Headers/blob/main/include/directx/d3dx12.h).

## <a name="in-this-section"></a>Contenu de cette section

| Rubrique | Description |
|-|-|
| [**CommandListCast**](commandlistcast.md) | Ce modèle de fonction convertit un pointeur constant en une liste de commandes en pointeur const vers un ID3D12CommandList. |
| [**D3D12CalcSubresource**](d3d12calcsubresource.md) | Calcule un index de sous-ressource pour une texture. |
| [**D3D12DecomposeSubresource**](d3d12decomposesubresource.md) | Affiche la tranche MIP, le segment de tableau et la tranche de plan correspondant à l’index de sous-ressource spécifié. |
| [**D3D12GetFormatPlaneCount**](d3d12getformatplanecount.md) | Obtient le nombre de plans pour le format DXGI spécifié pour la carte virtuelle spécifiée (un **ID3D12Device**). |
| [**D3D12IsLayoutOpaque**](d3d12islayoutopaque.md) | Indique si la disposition est opaque. |
| [**D3DX12GetBaseSubobjectType**](d3dx12getbasesubobjecttype.md) | Retourne le type de sous-objet qui correspond à la classe de base du type de sous-objet passé. |
| [**D3DX12ParsePipelineStateStream**](d3dx12parsepipelinestream.md) | Analyse une description du flux d’État du pipeline, en appelant un rappel défini par l’utilisateur pour chaque instance de sous-objet analysée. |
| [**D3DX12SerializeVersionedRootSignature**](d3dx12serializeversionedrootsignature.md) | Permet d’activer les fonctionnalités de signature racine 1,1 lorsqu’elles sont disponibles et ne nécessite pas la gestion de deux chemins de code pour générer des signatures racines. Cette méthode d’assistance reconstruit une signature racine version 1,0 quand la version 1,1 n’est pas prise en charge. |
| [**GetRequiredIntermediateSize**](getrequiredintermediatesize.md) | Retourne la taille requise d’une mémoire tampon à utiliser pour le téléchargement de données. |
| [**Memcpysubresource**](memcpysubresource.md) | Copie une sous-ressource ligne par ligne. |
| [**Updatesubresources**](updatesubresources1.md) | Met à jour les sous-ressources, tous les tableaux de sous-ressources doivent être remplis, en général en appelant [**ID3D12Device :: GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints). |
| [**Updatesubresources (allocation du tas)**](updatesubresources2.md) | Met à jour les sous-ressources avec une implémentation d’allocation de tas. |
| [**Updatesubresources (allocation de la pile)**](updatesubresources3.md) | Met à jour les sous-ressources avec une implémentation d’allocation de pile. |

## <a name="related-topics"></a>Rubriques connexes

* [Référence de Direct3D 12](direct3d-12-reference.md)
* [Structures et fonctions d’assistance pour D3D12](helper-structures-and-functions-for-d3d12.md)
