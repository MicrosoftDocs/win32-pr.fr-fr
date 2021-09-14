---
description: Décrit les types et structures de bibliothèque DirectXMath.
ms.assetid: 58acb05d-e79b-8f42-4cf4-76ae57929739
title: Structures de la bibliothèque DirectXMath
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c6ac040ee932e9da84c186124514d9f763e20e67
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126915084"
---
# <a name="directxmath-library-structures"></a>Structures de la bibliothèque DirectXMath

Décrit les types et structures de bibliothèque DirectXMath.

La bibliothèque DirectXMath fournit un certain nombre de structures et de types définis pour encapsuler les données afin de prendre en charge la facilité d’utilisation, l’optimisation et la portabilité. La liste suivante comprend les structures qui font actuellement partie de la bibliothèque DirectXMath. Ils sont disponibles par le biais de DirectXMath. h.

## <a name="in-this-section"></a>Contenu de cette section

| Rubrique | Description |
|-|-|
| [**XMBYTE2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmbyte2) | Vecteur 2D où chaque composant est un entier signé, 8 bits (1 octet) de longueur. |
| [**XMBYTE4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmbyte4) | Vecteur 4D dans lequel chaque composant est un entier signé de 8 bits (1 octet).  |
| [**XMBYTEN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmbyten2) | Vecteur 2D pour le stockage des valeurs signées et normalisées en tant qu’entiers 8 bits signés (1 octet). |
| [**XMBYTEN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmbyten4) | Vecteur 3D pour le stockage des valeurs signées et normalisées en tant qu’entiers 8 bits signés (1 octet).  |
| [**XMCOLOR**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmcolor) | Vecteur de couleur rouge vert vert à 32 bits (ARGB), où chaque canal de couleurs est spécifié en tant qu’entier 8 bits non signé. |
| [**XMDEC4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmdec4) | Vecteur 4D avec des composants x, y et z représentés sous forme de valeurs entières signées 10 bits et le composant w comme valeur d’entier signé 2 bits.  |
| [**XMDECN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmdecn4) | Vecteur 4D pour stocker des valeurs signées et normalisées comme des composants x, y et z signés 10 bits et un composant w signé 2 bits.  |
| [**XMFLOAT2**](/windows/win32/api/directxmath/ns-directxmath-xmfloat2) | Vecteur 2D constitué de deux valeurs à virgule flottante simple précision. |
| [**XMFLOAT2A**](/previous-versions/windows/desktop/legacy/ee419469(v=vs.85)) | Décrit une structure [**XMFLOAT2**](/windows/win32/api/directxmath/ns-directxmath-xmfloat2) alignée sur une limite de 16 octets. |
| [**XMFLOAT3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3) | Décrit un vecteur 3D constitué de trois valeurs à virgule flottante simple précision. |
| [**XMFLOAT3A**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3a) | Décrit une structure [**XMFLOAT3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3) alignée sur une limite de 16 octets. |
| [**XMFLOAT3PK**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmfloat3pk) | Décrit un vecteur 3D avec des composants X et Y stockés sous la forme d’un nombre à virgule flottante de 11 bits et un composant Z stocké sous la forme d’une valeur à virgule flottante de 10 bits.  |
| [**XMFLOAT3SE**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmfloat3se) | Décrit un vecteur 3D de trois composants à virgule flottante avec 9 bits mantisses, chacun partageant le même exposant 5 bits.  |
| [**XMFLOAT3X3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3x3) | Matrice à virgule flottante 3x3. |
| [**XMFLOAT3X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3x4) | Matrice principale 3x4 Column contenant des composants à virgule flottante 32 bits. |
| [**XMFLOAT3X4A**](/windows/win32/api/directxmath/ns-directxmath-xmfloat3x4a) | Une matrice 3x4-colonne principale contenant des composants à virgule flottante 32 bits alignés sur une limite de 16 octets. |
| [**XMFLOAT4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4) | Décrit un vecteur 4D constitué de quatre valeurs à virgule flottante simple précision.  |
| [**XMFLOAT4A**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4a) | Décrit une structure [**XMFLOAT4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4) alignée sur une limite de 16 octets. |
| [**XMFLOAT4X3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x3) | Matrice à virgule flottante 4x3. |
| [**XMFLOAT4X3A**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x3a) | Décrit une structure [**XMFLOAT4X3**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x3) alignée sur une limite de 16 octets. |
| [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4) | Matrice à virgule flottante 4x4. |
| [**XMFLOAT4X4A**](/previous-versions/windows/desktop/legacy/ee419623(v=vs.85)) | Décrit une structure [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4) alignée sur une limite de 16 octets. |
| [**XMHALF2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmhalf2) | Vecteur 2D constitué de deux valeurs à virgule flottante demi-précision (16 bits).  |
| [**XMHALF4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmhalf4) | Décrit un vecteur 4D constitué de quatre valeurs à virgule flottante demi-précision (16 bits).  |
| [**XMINT2**](/windows/win32/api/directxmath/ns-directxmath-xmint2) | Vecteur 2D où chaque composant est un entier signé. |
| [**XMINT3**](/windows/win32/api/directxmath/ns-directxmath-xmint3) | Vecteur 3D où chaque composant est un entier signé. |
| [**XMINT4**](/windows/win32/api/directxmath/ns-directxmath-xmint4) | Vecteur 4D où chaque composant est un entier signé. |
| [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) | Décrit une matrice 4x4 alignée sur une limite de 16 octets qui mappe à quatre registres vectoriels matériels. |
| [**XMSHORT2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshort2) | Décrit un vecteur 2D constitué de composants entiers signés et normalisés 16 bits.  |
| [**XMSHORT4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshort4) | Vecteur 4D constitué de composants entiers signés 16 bits.  |
| [**XMSHORTN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshortn2) | Vecteur 2D pour stocker des valeurs signées et normalisées en tant qu’entiers 16 bits signés (type `int16_t` ).  |
| [**XMSHORTN4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmshortn4) | Vecteur 4D pour stocker des valeurs signées et normalisées en tant qu’entiers 16 bits signés, (type `int16_t` ).  |
| [**XMU555**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmu555) | Vecteur 4D avec des composants x, y et z, représentés par des valeurs entières non signées de 5 bits, et le composant w comme une valeur entière de 1 bit.  |
| [**XMU565**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmu565) | Vecteur 3D avec des composants x et z représentés sous forme de valeurs entières non signées de 5 bits et le composant y en tant que valeur d’entier non signé 6 bits. |
| [**XMUBYTE2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmubyte2) | Décrit un vecteur 2D où chaque composant est un entier non signé, 8 bits (1 octet) en longueur. |
| [**XMUBYTE4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmubyte4) | Décrit un vecteur 4D où chaque composant est un entier non signé, de 8 bits (1 octet) en longueur.  |
| [**XMUBYTEN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmubyten2) | Vecteur 2D pour stocker des valeurs non signées et normalisées en tant qu’entiers 8 bits signés (1 octet). |
| [**XMUBYTEN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmubyten4) | Vecteur 3D pour stocker des valeurs non signées et normalisées en tant qu’entiers 8 bits signés (1 octet).  |
| [**XMUDEC4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmudec4) | Vecteur 4D avec des composants x, y et z représentés sous forme de valeurs entières non signées 10 bits et le composant w en tant que valeur d’entier non signé 2 bits.  |
| [**XMUDECN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmudecn4) | Vecteur 4D pour stocker des valeurs entières normalisées non signées comme des composants x, y et z non signés 10 bits et un composant w non signé 2 bits.  |
| [**XMUINT2**](/windows/win32/api/directxmath/ns-directxmath-xmuint2) | Vecteur 2D où chaque composant est un entier non signé. |
| [**XMUINT3**](/windows/win32/api/directxmath/ns-directxmath-xmuint3) | Vecteur 3D où chaque composant est un entier non signé. |
| [**XMUINT4**](/windows/win32/api/directxmath/ns-directxmath-xmuint4) | Vecteur 4D où chaque composant est un entier non signé. |
| [**XMUNIBBLE4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmunibble4) | Vecteur 4D avec quatre composants entiers 4 bits non signés.  |
| [**XMUSHORT2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushort2) | Décrit un vecteur 2D constitué de composants entiers non signés 16 bits.  |
| [**XMUSHORT4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushort4) | Vecteur 4D constitué de composants entiers non signés 16 bits.  |
| [**XMUSHORTN2**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushortn2) | Vecteur 2D pour stocker des valeurs non signées et normalisées en tant qu’entiers 16 bits non signés, (type `uint16_t` ).  |
| [**XMUSHORTN4**](/windows/desktop/api/DirectXPackedVector/ns-directxpackedvector-xmushortn4) | Vecteur 4D pour stocker des valeurs non signées et normalisées en tant qu’entiers 16 bits signés (type `uint16_t` ).  |
| [**XMXDEC4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmxdec4) | Vecteur 4D avec des composants x, y et z représentés sous forme de valeurs entières signées 10 bits et le composant w en tant que valeur d’entier non signé 2 bits.  |
| [**XMXDECN4**](/windows/win32/api/directxpackedvector/ns-directxpackedvector-xmxdecn4) | Vecteur 4D pour stocker des valeurs signées et normalisées comme des composants x-, y-et z signés 10 bits, et une valeur non signée et normalisée comme 2 bits non signés w-Component.  |

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Informations de référence sur la programmation DirectXMath](ovw-xnamath-reference.md)
</dt> </dl>
