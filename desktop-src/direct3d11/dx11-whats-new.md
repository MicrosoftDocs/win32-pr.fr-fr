---
title: nouveautés du kit de développement logiciel (SDK) Windows 7/Direct3D 11 d’août 2009
description: cette version de Windows 7/Direct3D 11 est fournie avec le kit de développement logiciel (SDK) DirectX et contient de nouvelles fonctionnalités, outils et documentation.
ms.assetid: c2dc3726-70a0-49ff-bbad-8ef774bc4868
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83c51f350065134893ed2303d8854eb9d24fc7f58e8ab762f71da019d89d45b2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119608909"
---
# <a name="whats-new-in-the-august-2009-windows-7direct3d-11-sdk"></a>nouveautés du kit de développement logiciel (SDK) Windows 7/Direct3D 11 d’août 2009

cette version de Windows 7/Direct3D 11 est fournie avec le kit de développement logiciel (SDK) DirectX et contient de nouvelles fonctionnalités, outils et documentation.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Élément</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="Direct2D"></span><span id="direct2d"></span><span id="DIRECT2D"></span>Direct2D<br/></td>
<td>Direct2D est une API graphique à accélération matérielle, en mode immédiat, en 2D, qui offre des performances élevées et un rendu de haute qualité pour la géométrie 2D, les bitmaps et le texte. L’API Direct2D est conçue pour interagir correctement avec Direct3D et GDI. Ce kit de développement logiciel (SDK) permet aux développeurs d’évaluer l’API et d’écrire des applications simples, avec certaines des fonctionnalités les plus avancées possibles sur les ordinateurs configurés correctement. <br/> <a href="/windows/win32/direct2d/direct2d-portal">La documentation</a> et les <a href="/previous-versions//dd372354(v=vs.85)">exemples</a> de Direct2D sont actuellement disponibles sur MSDN.<br/></td>
</tr>
<tr class="even">
<td><span id="DirectWrite"></span><span id="directwrite"></span><span id="DIRECTWRITE"></span>DirectWrite<br/></td>
<td>DirectWrite prend en charge le rendu de texte de haute qualité, les polices de contour indépendantes de la résolution, la prise en charge complète du texte Unicode et de la disposition, et bien plus encore :<br/>
<ul>
<li>Système de disposition de texte indépendant du périphérique qui améliore la lisibilité du texte dans les documents et dans l’interface utilisateur.<br/></li>
<li>Rendu de texte ClearType de haute qualité, sous-pixel, qui peut utiliser l’interface GDI Direct3D, Direct2D ou la technologie de rendu propre à l’application.<br/></li>
<li>Prise en charge du texte à plusieurs formats. <br/></li>
<li>Prise en charge des fonctionnalités typographiques avancées des polices OpenType.<br/></li>
<li>Prise en charge de la disposition et du rendu du texte dans toutes les langues prises en charge par Windows.<br/></li>
</ul>
Ce kit de développement logiciel (SDK) permet aux développeurs d’évaluer l’API et d’écrire des applications de base à des fins de démonstration uniquement.<br/> <a href="/windows/win32/directwrite/direct-write-portal">la Documentation</a> et les <a href="/windows/win32/directwrite/samples">exemples</a> de DirectWrite sont actuellement disponibles sur MSDN.<br/></td>
</tr>
<tr class="odd">
<td><span id="DXGI_1.1"></span><span id="dxgi_1.1"></span>DXGI 1,1<br/></td>
<td><a href="/windows/desktop/direct3ddxgi/dx-graphics-dxgi-overviews">DXGI 1,1</a> s’appuie sur DXGI 1,0 et sera disponible à la fois sur Windows Vista et Windows 7. DXGI 1,1 ajoute plusieurs nouvelles fonctionnalités :<br/>
<ul>
<li>Prise en charge des surfaces partagées synchronisées. Cela permet un partage des surfaces de lecture et d’écriture efficace entre plusieurs périphériques D3D (entre D3D10 et D3D11).<br/></li>
<li>Prise en charge du format BGRA. Cela permet à GDI de s’afficher sur la même surface DXGI ciblée par un appareil Direct2D, Direct3D 10,1 ou Direct3D 11. <br/></li>
<li>Latence de trame maximale. À l’aide de <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgidevice1-setmaximumframelatency"><strong>IDXGIDevice1 :: SetMaximumFrameLatency</strong></a> et <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgidevice1-getmaximumframelatency"><strong>IDXGIDevice1 :: GetMaximumFrameLatency</strong></a>, les titres peuvent contrôler le nombre de frames qui sont autorisés à être stockés dans une file d’attente avant leur envoi. La latence est souvent utilisée pour contrôler la façon dont l’UC choisit de répondre aux entrées d’utilisateur et aux trames qui se trouvent dans la file d’attente de rendu.<br/></li>
<li>Énumération des adaptateurs. À l’aide de <a href="/windows/desktop/api/dxgi/nf-dxgi-idxgifactory1-enumadapters1"><strong>IDXGIFactory1 :: EnumAdapters1</strong></a>, Titles peut énumérer des adaptateurs locaux sans moniteurs ou sorties attachés, ainsi que des adaptateurs avec des sorties attachées.<br/></li>
</ul></td>
</tr>
<tr class="even">
<td><span id="Updated_Samples"></span><span id="updated_samples"></span><span id="UPDATED_SAMPLES"></span>Exemples mis à jour<br/></td>
<td>Cette version comporte plusieurs exemples nouveaux et mis à jour.<br/>
<ul>
<li>Le nouveau <a href="https://msdn.microsoft.com/library/Ee416556(v=VS.85).aspx">AdaptiveTessellationCS40</a> est une illustration de techniques de traitement de nuanceur de calcul avancées qui peuvent être exécutées sur un GPU D3D10 ou d3d11.</li>
<li>L' <a href="https://msdn.microsoft.com/library/Ee416569(v=VS.85).aspx">exemple HDRToneMappingCS11</a> a été développé pour implémenter des effets de flou et de floraison (en plus du mappage de tons) à l’aide du nuanceur de calcul, ainsi que des implémentations de nuanceur de pixels pour la comparaison.</li>
<li>L' <a href="https://msdn.microsoft.com/library/Ee416570(v=VS.85).aspx">exemple MultithreadedRendering11</a> a été considérablement mis à jour, avec des ressources artistiques plus complexes et un traitement par thread plus intensif.</li>
<li>L' <a href="https://msdn.microsoft.com/library/Ee416576(v=VS.85).aspx">exemple SubD11</a> a été mis à jour avec un nouveau modèle facial, et l’exemple tire parti de la fonctionnalité de calcul contiguïté de l’exportateur de contenu Samples.</li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Fonctionnalités introduites dans les versions précédentes](d3d11-features-introduced-previous-releases.md)
</dt> </dl>

