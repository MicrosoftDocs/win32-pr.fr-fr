---
description: 'Cette section contient des informations sur les interfaces de nuanceur suivantes :'
ms.assetid: d8770b45-a05c-4dd8-9fa7-08fb4330d734
title: Interfaces de nuanceur (graphiques Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 838a65d263533d0b2225515664e21c2d93114495
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483400"
---
# <a name="shader-interfaces-direct3d-10-graphics"></a>Interfaces de nuanceur (graphiques Direct3D 10)

Cette section contient des informations sur les interfaces de nuanceur suivantes :

Chacune de ces interfaces de nuanceur gère un nuanceur compilé. L’interface est créée lors de la compilation d’un nuanceur et est ensuite transmise à différentes API qui doivent accéder à un nuanceur compilé ; par exemple, lors de la liaison d’un nuanceur à une phase de pipeline ou de l’obtention d’une signature de nuanceur.



| Interfaces Pipeline-Stage                                      | Description                                                                                                                                 |
|----------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [**Interface ID3D10GeometryShader**](/windows/win32/api/d3d10/nn-d3d10-id3d10geometryshader) | Un nuanceur Geometry implémente un traitement par primitive dans l' [étape Geometry-Shader](d3d10-graphics-programming-guide-pipeline-stages.md). |
| [**Interface ID3D10PixelShader**](/windows/win32/api/d3d10/nn-d3d10-id3d10pixelshader)       | Un nuanceur de pixels implémente le traitement par pixel dans l' [étape nuanceur de pixels](d3d10-graphics-programming-guide-pipeline-stages.md).           |
| [**Interface ID3D10VertexShader**](/windows/win32/api/d3d10/nn-d3d10-id3d10vertexshader)     | Un nuanceur de sommets implémente le traitement par vertex dans l' [étape de nuanceur de sommets](d3d10-graphics-programming-guide-pipeline-stages.md).        |



 

Les interfaces de nuanceur-réflexion permettent à une application d’inspecter le contenu d’un nuanceur au moment de la conception ou de l’auteur. La réflexion du nuanceur n’est pas utile pour définir des variables au moment de l’exécution, car il s’agit d’un miroir des données du nuanceur et ne prend donc pas en charge les méthodes de définition des données.



| Interfaces Shader-Reflection                                                                   | Description                                                                        |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| [**Interface ID3D10ShaderReflection**](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflection)                             | Interface COM pour lire des informations à partir d’un nuanceur compilé au moment de l’édition.     |
| [**Interface ID3D10ShaderReflectionConstantBuffer**](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflectionconstantbuffer) | Une interface d’assistance pour obtenir une interface de mémoire tampon de nuanceur-réflexion.      |
| [**Interface ID3D10ShaderReflectionType**](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflectiontype)                     | Interface d’assistance pour l’obtention d’une interface de type nuanceur-réflexion.                 |
| [**Interface ID3D10ShaderReflectionVariable**](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflectionvariable)             | Interface d’assistance pour l’obtention d’une interface de nuanceur-réflexion-variable.             |
| [**Interface ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)                         | Interface de nuanceur-réflexion permettant de lire des informations à partir d’un affichage des ressources de nuanceur. |



 

Les API de réflexion de nuanceur implémentent une interface de réflexion de nuanceur COM ([**ID3D10ShaderReflection interface**](/windows/desktop/api/D3D10Shader/nn-d3d10shader-id3d10shaderreflection)) et plusieurs interfaces d’assistance non com (le reste des interfaces). L' **interface ID3D10ShaderReflection** est créée lors de la création d’un objet de réflexion de nuanceur. Il suit les règles COM standard ; la création de l’interface augmente le nombre de références et l’interface doit être libérée lorsqu’elle n’est plus nécessaire. Les interfaces de nuanceur-réflexion restantes sont des interfaces d’assistance qui n’héritent pas de IUnknown. Cela signifie qu’ils ne modifient aucun nombre de références lors de leur création, et qu’ils n’ont pas besoin d’être détruits lorsque vous en avez terminé avec eux.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence du nuanceur](d3d10-graphics-reference-d3d10-shader.md)
</dt> </dl>

 

 
