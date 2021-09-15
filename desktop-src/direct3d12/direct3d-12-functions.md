---
title: Fonctions de base (Direct3D 12 Graphics)
description: Les fonctions suivantes sont déclarées dans d3d12. h.
ms.assetid: C0F9A52C-483D-40B2-9E1F-CB92ADDC2856
ms.localizationpriority: low
ms.topic: article
ms.date: 11/27/2018
ms.openlocfilehash: e38145bc4aef4c07ba00de4185fc97ad449f4f2c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127404338"
---
# <a name="core-functions"></a>Fonctions de base

Les fonctions suivantes sont déclarées dans d3d12. h.

## <a name="in-this-section"></a>Contenu de cette section

| Rubrique | Description |
|-|-|
| [**D3D12CreateDevice**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createdevice) | Crée un appareil qui représente la carte graphique. |
| [**D3D12CreateRootSignatureDeserializer**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createrootsignaturedeserializer) | Désérialise une signature racine pour vous permettre de déterminer la définition de la disposition ([**D3D12 racine de la \_ \_ signature \_ desc**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_root_signature_desc)). |
| [**D3D12CreateVersionedRootSignatureDeserializer**](/windows/desktop/api/d3d12/nf-d3d12-d3d12createversionedrootsignaturedeserializer) | Génère une interface qui peut retourner la structure de données désérialisée, via [**GetUnconvertedRootSignatureDesc**](/windows/desktop/api/d3d12/nf-d3d12-id3d12versionedrootsignaturedeserializer-getunconvertedrootsignaturedesc). |
| [**D3D12EnableExperimentalFeatures**](/windows/desktop/api/d3d12/nf-d3d12-d3d12enableexperimentalfeatures) | Active une liste de fonctionnalités expérimentales. |
| [**D3D12GetDebugInterface**](/windows/desktop/api/d3d12/nf-d3d12-d3d12getdebuginterface) | Obtient une interface de débogage. |
| [**D3D12GetInterface**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializeversionedrootsignature) | sélectionne une version du kit de développement logiciel (SDK) au moment de l’exécution lorsque le système est en Mode développeur Windows. |
| [**D3D12SerializeRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializerootsignature) | Sérialise une signature racine version 1,0 qui peut être passée à [**ID3D12Device :: CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature). |
| [**D3D12SerializeVersionedRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-d3d12serializeversionedrootsignature) | Sérialise une signature racine de n’importe quelle version qui peut être passée à [**ID3D12Device :: CreateRootSignature**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-createrootsignature). |

## <a name="related-topics"></a>Rubriques connexes

* [Référence de base](direct3d-12-core-reference.md)
* [Informations de référence sur Direct3D 12](direct3d-12-reference.md)
