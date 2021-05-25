---
description: Constantes décrivant les types de données de vertex pris en charge par un appareil.
ms.assetid: 751d7b92-b187-40e5-882c-6fdb80e1ff5f
title: D3DDTCAPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97ded570b8f451ea7e99050467f70f945d202bd4
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343233"
---
# <a name="d3ddtcaps"></a>D3DDTCAPS

Constantes décrivant les types de données de vertex pris en charge par un appareil.



| \#définition              | Valeur       | Description                                                                                                                   |
|-----------------------|-------------|-------------------------------------------------------------------------------------------------------------------------------|
| D3DDTCAPS \_ UBYTE4     | 0x00000001L | octet non signé 4D.                                                                                                             |
| D3DDTCAPS \_ UBYTE4N    | 0x00000002L | Octets non signés normalisés et 4D. Chacun des quatre octets est normalisé en divisant à 255,0.                                      |
| D3DDTCAPS \_ SHORT2N    | 0x00000004L | Normald, unsigned short, Expanded to (First Byte/32767.0, second Byte/32767.0, 0, 1).                                     |
| D3DDTCAPS \_ SHORT4N    | 0x00000008L | Normalized, 4D signé Short, développé sur (First Byte/32767.0, second Byte/32767.0, Third Byte/32767.0, quatrième octet/32767.0).  |
| D3DDTCAPS \_ USHORT2N   | 0x00000010L | Normalized, 2J unsigned short, Expanded to (First Byte/65535.0, second Byte/65535.0, 0, 1).                                   |
| D3DDTCAPS \_ USHORT4N   | 0x00000020L | 4D normalisé non signé, développé sur (premier octet/65535.0, deuxième octet/65535.0, troisième octet/65535.0, quatrième octet/65535.0). |
| D3DDTCAPS \_ UDEC3      | 0x00000040L | format 3D non signé 10 10 10 développé sur (valeur, valeur, valeur, 1).                                                             |
| D3DDTCAPS \_ DEC3N      | 0x00000080L | format 3D signé 10 10 10 normalisé et développé en (v \[ 0 \] /511,0, v \[ 1 \] /511,0, v \[ 2 \] /511,0, 1).                           |
| D3DDTCAPS \_ FLOAT16 \_ 2 | 0x00000100L | nombres à virgule flottante 2D 16 bits.                                                                                             |
| D3DDTCAPS \_ FLOAT16 \_ 4 | 0x00000200L | nombres à virgule flottante 4D 16 bits.                                                                                             |



 

Ces constantes sont utilisées par le membre DeclTypes de [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

## <a name="constant-information"></a>Informations constantes



|  Condition requise                        | Valeur           |
|--------------------------|------------|
| En-tête                   | d3d9caps. h |
| Système d’exploitation minimal | Windows 98 |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Constantes Direct3D](dx9-graphics-reference-d3d-constants.md)
</dt> </dl>

 

 



