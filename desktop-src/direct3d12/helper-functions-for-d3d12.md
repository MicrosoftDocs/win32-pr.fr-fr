---
title: Fonctions d’assistance pour D3D12
description: Ces fonctions d’assistance sont particulièrement utiles pour gérer les sous-ressources et sont déclarées dans d3dx12. h.
ms.assetid: E40B20D9-C700-4142-BBF3-7A5086E34712
keywords:
- Fonctions d’assistance
- d3dx12. h
ms.localizationpriority: low
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6cacaaf5ad2a8204cc35b8a89f7c3c00e756116
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106522625"
---
# <a name="helper-functions-for-d3d12"></a>Fonctions d’assistance pour D3D12

Ces fonctions d’assistance sont particulièrement utiles pour gérer les sous-ressources et sont déclarées dans **d3dx12. h**.

## <a name="in-this-section"></a>Contenu de cette section



| Rubrique                                                                                             | Description                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CommandListCast**](cd3dx12-shader-bytecode.md)<br/>                                     | Ce modèle de fonction convertit un pointeur constant en une liste de commandes en pointeur const vers un ID3D12CommandList.<br/>                                                                                                                               |
| [**D3D12CalcSubresource**](d3d12calcsubresource.md)<br/>                                   | Calcule un index de sous-ressource pour une texture. <br/>                                                                                                                                                                                                  |
| [**D3D12DecomposeSubresource**](d3d12decomposesubresource.md)<br/>                         | Affiche la tranche MIP, le segment de tableau et la tranche de plan correspondant à l’index de sous-ressource spécifié. <br/>                                                                                                                                        |
| [**D3D12GetFormatPlaneCount**](d3d12getformatplanecount.md)<br/>                           | Obtient le nombre de plans pour le format DXGI spécifié pour la carte virtuelle spécifiée (un **ID3D12Device**). <br/>                                                                                                                               |
| [**D3D12IsLayoutOpaque**](d3d12islayoutopaque.md)<br/>                                     | Indique si la disposition est opaque.<br/>                                                                                                                                                                                                         |
| [**D3DX12GetBaseSubobjectType**](d3dx12getbasesubobjecttype.md)<br/>                       | Retourne le type de sous-objet qui correspond à la classe de base du type de sous-objet passé.<br/>                                                                                                                                                  |
| [**D3DX12ParsePipelineStateStream**](d3dx12parsepipelinestream.md)<br/>                    | Analyse une description du flux d’État du pipeline, en appelant un rappel défini par l’utilisateur pour chaque instance de sous-objet analysée.<br/>                                                                                                                                 |
| [**D3DX12SerializeVersionedRootSignature**](d3dx12serializeversionedrootsignature.md)<br/> | Permet d’activer les fonctionnalités de signature racine 1,1 lorsqu’elles sont disponibles et ne nécessite pas la gestion de deux chemins de code pour générer des signatures racines. Cette méthode d’assistance reconstruit une signature racine version 1,0 quand la version 1,1 n’est pas prise en charge.<br/> |
| [**GetRequiredIntermediateSize**](getrequiredintermediatesize.md)<br/>                     | Retourne la taille requise d’une mémoire tampon à utiliser pour le téléchargement de données. <br/>                                                                                                                                                                              |
| [**Memcpysubresource**](memcpysubresource.md)<br/>                                         | Copie une sous-ressource ligne par ligne. <br/>                                                                                                                                                                                                               |
| [**Updatesubresources**](updatesubresources1.md)<br/>                                      | Met à jour les sous-ressources, tous les tableaux de sous-ressources doivent être remplis, en général en appelant [**ID3D12Device :: GetCopyableFootprints**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-getcopyablefootprints). <br/>                                                                  |
| [**Updatesubresources (allocation du tas)**](updatesubresources2.md)<br/>                    | Met à jour les sous-ressources avec une implémentation d’allocation de tas. <br/>                                                                                                                                                                                    |
| [**Updatesubresources (allocation de la pile)**](updatesubresources3.md)<br/>                   | Met à jour les sous-ressources avec une implémentation d’allocation de pile. <br/>                                                                                                                                                                                   |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence de Direct3D 12](direct3d-12-reference.md)
</dt> <dt>

[Structures et fonctions d’assistance pour D3D12](helper-structures-and-functions-for-d3d12.md)
</dt> </dl>

 

 





