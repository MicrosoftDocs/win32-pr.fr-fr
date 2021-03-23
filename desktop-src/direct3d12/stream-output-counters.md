---
title: Compteurs de sortie de flux
description: La sortie de flux est la capacité du GPU à écrire des vertex dans une mémoire tampon. Les compteurs de sortie de flux surveillent la progression.
ms.assetid: 7342DA09-25E9-4154-83BA-B03ADBB8B671
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df4d2f3a823f5f4b5d2d5f365235d7e3f8817207
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "74103557"
---
# <a name="stream-output-counters"></a>Compteurs de sortie de flux

La sortie de flux est la capacité du GPU à écrire des vertex dans une mémoire tampon. Les compteurs de sortie de flux surveillent la progression.

-   [Différences entre les compteurs de flux de Direct3D 11 et Direct3D 12](#differences-in-stream-counters-from-direct3d-11-to-direct3d-12)
-   [BufferFilledSize](#bufferfilledsize)
-   [Rubriques connexes](#related-topics)

## <a name="differences-in-stream-counters-from-direct3d-11-to-direct3d-12"></a>Différences entre les compteurs de flux de Direct3D 11 et Direct3D 12

Dans le cadre du processus de sortie de flux, le GPU doit connaître l’emplacement actuel dans la mémoire tampon dans laquelle il écrit. Dans Direct3D 11, la mémoire pour stocker cet emplacement est allouée par le pilote et le seul moyen pour les applications de manipuler cette valeur est d’utiliser la méthode **SOSetTargets** . Dans Direct3D 12, les applications allouent de la mémoire pour stocker cet emplacement actuel. Il n’existe aucune manière spéciale de manipuler cette valeur, et les applications sont libres de lire/écrire la valeur avec le processeur ou le GPU.

## <a name="bufferfilledsize"></a>BufferFilledSize

L’application est chargée d’allouer le stockage pour une quantité de 32 bits appelée *BufferFilledSize*. Contient le nombre d’octets de données dans la mémoire tampon de sortie de flux. Ce stockage peut être placé dans la même ressource, ou une ressource différente que celle qui contient les données de sortie de flux. Cette valeur est accessible par le GPU dans l’étape de flux de sortie pour déterminer où ajouter les nouvelles données de vertex dans la mémoire tampon. En outre, cette valeur est accessible par le GPU pour déterminer le moment où un dépassement s’est produit.

Reportez-vous à la structure de [**\_ sortie du flux \_ \_ D3D12**](/windows/desktop/api/d3d12/ns-d3d12-d3d12_stream_output_desc).

La couche de débogage validera les éléments suivants dans [**ID3D12GraphicsCommandList :: SOSetTargets**](/windows/desktop/api/d3d12/nf-d3d12-id3d12graphicscommandlist-sosettargets):

-   *BufferFilledSize* se trouve dans la plage impliquée par {*OffsetInBytes*, *sizeInBytes*}, si une ressource non null est spécifiée.
-   *BufferFilledSizeOffsetInBytes* est un multiple de 4.
-   *BufferFilledSizeOffsetInBytes* se trouve dans la plage de la ressource conteneur.
-   La ressource spécifiée est une mémoire tampon.

Le runtime ne valide pas le type de tas associé à la mémoire tampon de sortie de flux, car la sortie de flux est prise en charge dans tous les types de tas.

Les signatures racines doivent spécifier si la sortie de flux sera utilisée, à l’aide des indicateurs de [**\_ \_ signature \_ racine D3D12**](/windows/desktop/api/d3d12/ne-d3d12-d3d12_root_signature_flags) Flags.

\_ \_ L’indicateur de signature racine D3D12 \_ \_ autorise \_ la sortie de flux \_ peut être spécifiée pour les signatures racines créées en HLSL, d’une manière similaire à la façon dont les autres indicateurs sont spécifiés.

[**CreateGraphicsPipelineState**](/windows/desktop/api/d3d12/nf-d3d12-id3d12device-creategraphicspipelinestate) échoue si le nuanceur Geometry contient un flux de sortie, mais que la signature racine n’a pas l’indicateur de \_ signature racine D3D12 allow de la sortie de \_ \_ \_ \_ flux \_ défini.

Lorsqu’une ressource est utilisée en tant que cible de sortie de flux, les ressources utilisées doivent être dans \_ l' \_ \_ État de flux \_ sortant de l’état de ressource D3D12. Cela s’applique à la fois aux données de vertex et au *BufferFilledSize* (qui peuvent être dans les mêmes ressources ou des ressources distinctes).

Il n’existe pas d’API spéciales pour définir des décalages de mémoire tampon de sortie de flux, car les applications peuvent écrire directement sur le *BufferFilledSize* avec le processeur ou le GPU.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Compteurs et requêtes](counters-and-queries.md)
</dt> </dl>

 

 




