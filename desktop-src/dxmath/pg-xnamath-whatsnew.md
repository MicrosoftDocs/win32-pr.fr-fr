---
description: La bibliothèque DirectXMath est basée sur la bibliothèque XNA Math C++ SIMD version 2. x. Ici, nous décrivons comment DirectXMath diffère de XNA Math et comment les versions de DirectXMath diffèrent.
ms.assetid: 105800d3-a191-c78f-316a-bf2daf7b27a6
title: Nouveautés (DirectXMath)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eb9fa8c7ee0600ce0b0fa5eade3a3e111e5edbe4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106527789"
---
# <a name="whats-new-directxmath"></a>Nouveautés (DirectXMath)

La bibliothèque DirectXMath est basée sur la [bibliothèque XNA Math C++ SIMD version 2,04](https://walbourn.github.io/). Ici, nous décrivons comment DirectXMath diffère de XNA Math et comment les versions de DirectXMath diffèrent.

-   [Historique Rlease](#release-history)
-   [DirectXMath les différences par rapport à XNA Math](#directxmath-differences-from-xna-math)
-   [Rubriques connexes](#related-topics)

## <a name="release-history"></a>Historique des mises en production

<table>
 <tr>
  <td>Kit de développement logiciel de mise à jour Windows 10 2020</td><td>DirectXMath 3,14</td>
 </tr>
 <tr>
  <td>SDK de mise à jour de Windows 10 octobre 2018</td><td>DirectXMath 3,13</td>
 </tr>
 <tr>
  <td>Kit de mise à jour de Windows 10 avril 2018<br />SDK de la mise à jour des créateurs Windows 10 automne</td><td>DirectXMath 3,11</td>
 </tr>
 <tr>
  <td>SDK Windows 10 Creators Update</td><td>DirectXMath 3,10</td>
 </tr>
 <tr>
  <td>SDK Windows 10 anniversaire</td><td>DirectXMath 3,09</td>
 </tr>
 <tr>
  <td>SDK Windows 10 (2015 novembre)</td><td>DirectXMath 3,08</td>
 </tr>
 <tr>
  <td>SDK Windows pour Windows 8.1 (Spring 2015)</td><td>DirectXMath 3,07</td>
 </tr>
 <tr>
  <td>Kit de développement logiciel (SDK) Windows pour Windows 8.1</td><td>DirectXMath 3,06</td>
 </tr>
 <tr>
  <td>SDK Windows pour Windows 8</td><td>DirectXMath 3,03</td>
 </tr>
</table>

Pour plus d’informations, consultez [versions DirectXMath](https://github.com/Microsoft/DirectXMath/releases) .

## <a name="directxmath-differences-from-xna-math"></a>DirectXMath les différences par rapport à XNA Math

Voici comment la bibliothèque DirectXMath diffère principalement de la bibliothèque XNA Math :

-   DirectXMath est uniquement en C++ (espaces de noms, surcharges, nouveaux modèles, etc.).
-   Requiert la prise en charge de la bibliothèque standard C++ 11 (c’est-à-dire, stdint. h, etc.).
-   Prise en charge des intrinsèques ARM-néon pour la plateforme Windows RT.
-   Nouvelles fonctionnalités de couleur (conversions d’espace colorimétrique, constantes de couleur .NET).
-   Délimitation des types de volumes (version de qui était précédemment dans l’en-tête XNACollision dans l’exemple de collision du kit de développement logiciel (SDK) DirectX).
-   Aucune version Xbox 360 n’est disponible. La Xbox 360 XDK continue à expédier XNAMath v2. x ; suppression des types de données et des variantes de fonction spécifiques à Xbox 360.
-   [**XMVectorPermute**](/windows/win32/api/directxmath/nf-directxmath-xmvectorpermute) retravaillé pour améliorer l’optimisation des intrinsèques SSE et ARM-néon.
-   Le type [**XMMATRIX**](/windows/win32/api/directxmath/ns-directxmath-xmmatrix) est entièrement opaque. Pour accéder à des éléments individuels de **XMMATRIX**, utilisez d’autres types tels que [**XMFLOAT4X4**](/windows/win32/api/directxmath/ns-directxmath-xmfloat4x4).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Guide de programmation DirectXMath](ovw-xnamath-progguide.md)
</dt> <dt>

[Versions de DirectXMath](https://github.com/Microsoft/DirectXMath/releases)
</dt> </dl>

 

 
