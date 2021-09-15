---
description: 'L’affectation d’une valeur différente de zéro à la méthode IDirect3DDevice9 :: CreateVertexBuffer, qui doit être un code valide pour la Commission, indique que le contenu de la mémoire tampon doit être caractérisé par un code de la Commission.'
ms.assetid: 7cab559f-3e9d-46bd-b00f-439e0922aeeb
title: Mémoires tampons de vertex du prix final (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a86201c3ddc1cab6d492539caccc61c1430b3a2c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127516832"
---
# <a name="fvf-vertex-buffers-direct3d-9"></a>Mémoires tampons de vertex du prix final (Direct3D 9)

L’affectation d’une valeur différente de zéro à la méthode [**IDirect3DDevice9 :: CreateVertexBuffer**](/windows/desktop/api) , qui doit être un code valide pour la Commission, indique que le contenu de la mémoire tampon doit être caractérisé par un code de la Commission. Une mémoire tampon de vertex créée avec un code de la Commission des prix finals est appelée « mémoire tampon de vertex ». Certaines méthodes ou utilisations de [**IDirect3DDevice9**](/windows/desktop/api) requièrent des tampons de vertex de la Commission, tandis que d’autres nécessitent des tampons de vertex non-Commission. Les tampons de vertex de la Commission de la Commission sont requis comme argument de mémoire tampon de vertex de destination pour [**IDirect3DDevice9 ::P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices).

Les mémoires tampons de vertex du prix final peuvent être liées à un flux de données source pour n’importe quel numéro de flux.

La présence du composant D3DFVF \_ XYZRHW sur les mémoires tampons de vertex de la Commission des prix finalistes indique que les vertex de cette mémoire tampon ont été traités. Les mémoires tampons de vertex utilisées pour [**IDirect3DDevice9 ::P rocessvertices**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-processvertices) les tampons de vertex de destination doivent être postérieures au traitement. Les mémoires tampons de vertex utilisées pour les entrées de nuanceur de fonction fixe peuvent être prétraitées ou postprocessed. Si la mémoire tampon de vertex est après traitement, le nuanceur est effectivement contourné et les données sont transmises directement au module de découpage et d’installation primitif.

Les mémoires tampons de vertex de la Commission des prix finalistes peuvent être utilisées avec des nuanceurs vertex. En outre, les flux vertex peuvent représenter les mêmes formats de vertex que ceux qui ne le sont pas. Ils n’ont pas besoin d’être utilisés pour entrer des données à partir de mémoires tampons de vertex distinctes. La flexibilité supplémentaire des nouveaux flux de vertex permet aux applications qui doivent conserver leurs données de se séparer pour mieux travailler, mais cela n’est pas obligatoire. Si l’application peut conserver les données entrelacées à l’avance, il s’agit d’une amélioration des performances. Si l’application entrelace uniquement les données avant chaque appel de rendu, elle doit activer l’API ou le matériel pour effectuer cette opération avec plusieurs flux.

Les aspects les plus importants avec les performances des vertex sont l’utilisation d’un vertex de 32 octets et la gestion d’un bon classement du cache.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Mémoires tampons de vertex](vertex-buffers.md)
</dt> </dl>

 

 
