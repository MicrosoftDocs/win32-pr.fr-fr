---
description: La bibliothèque DirectXMath est basée sur la bibliothèque XNA Math C++ SIMD version 2. x. Ici, nous décrivons comment DirectXMath diffère de XNA Math et comment les versions de DirectXMath diffèrent.
ms.assetid: 105800d3-a191-c78f-316a-bf2daf7b27a6
title: Nouveautés (DirectXMath)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e94d4ba2433501fb5389b82dab4f5c3de4b8ed80904ed4629729537bbf264a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118984709"
---
# <a name="whats-new-directxmath"></a>Nouveautés (DirectXMath)

La bibliothèque DirectXMath est basée sur la [bibliothèque XNA Math C++ SIMD version 2,04](https://walbourn.github.io/xna-math-version-2-04/). Ici, nous décrivons comment DirectXMath diffère de XNA Math et comment les versions de DirectXMath diffèrent.

-   [Historique Rlease](#release-history)
-   [DirectXMath les différences par rapport à XNA Math](#directxmath-differences-from-xna-math)
-   [Rubriques connexes](#related-topics)

## <a name="release-history"></a>Historique des mises en production

<table>
 <tr>
  <td>Windows 10 SDK (20348), version 2104</td><td>DirectXMath 3,16</td>
 </td>
 <tr>
  <td>Windows 10 SDK de mise à jour mai 2020</td><td>DirectXMath 3,14</td>
 </tr>
 <tr>
  <td>SDK Mise à jour d’octobre 2018 de Windows 10</td><td>DirectXMath 3,13</td>
 </tr>
 <tr>
  <td>Windows 10 SDK de mise à jour d’avril 2018<br />Windows 10 Fall Creators Update SDK</td><td>DirectXMath 3,11</td>
 </tr>
 <tr>
  <td>Windows 10 Creators Update SDK</td><td>DirectXMath 3,10</td>
 </tr>
 <tr>
  <td>Windows 10 SDK anniversaire</td><td>DirectXMath 3,09</td>
 </tr>
 <tr>
  <td>Windows 10 SDK (2015 novembre)</td><td>DirectXMath 3,08</td>
 </tr>
 <tr>
  <td>Windows kit de développement logiciel (SDK) pour Windows 8.1 (Spring 2015)</td><td>DirectXMath 3,07</td>
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
-   prise en charge des intrinsèques ARM-néon pour la plateforme Windows RT.
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

 

 
