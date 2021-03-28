---
title: Interfaces D3DX (graphiques Direct3D 11)
description: Cette section contient des informations de référence sur les interfaces COM (Component Object Model) fournies par la bibliothèque de l’utilitaire D3DX.
ms.assetid: 0d3be1e6-b558-4586-9440-251a5611d7cd
keywords:
- Interfaces D3DX, Direct3D 11
- interfaces, Direct3D 11 D3DX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da2890c3c55d1bac9eba09c046927e432b1a27f8
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104032179"
---
# <a name="d3dx-interfaces-direct3d-11-graphics"></a>Interfaces D3DX (graphiques Direct3D 11)

Cette section contient des informations de référence sur les interfaces COM (Component Object Model) fournies par la bibliothèque de l’utilitaire D3DX.

> [!Note]  
> La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.

 


## <a name="in-this-section"></a>Contenu de cette section



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Rubrique</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="id3dx11dataloader.md"><strong>ID3DX11DataLoader</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.
</blockquote>
<br/> Objet chargeant des données utilisé par l' <a href="id3dx11threadpump.md"><strong>interface ID3DX11ThreadPump</strong></a> pour le chargement des données de façon asynchrone.<br/></td>
</tr>
<tr class="even">
<td><a href="id3dx11dataprocessor.md"><strong>ID3DX11DataProcessor</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.
</blockquote>
<br/> Objet de traitement de données utilisé par l' <a href="id3dx11threadpump.md"><strong>interface ID3DX11ThreadPump</strong></a> pour le chargement des données de façon asynchrone.<br/></td>
</tr>
<tr class="odd">
<td><a href="id3dx11threadpump.md"><strong>ID3DX11ThreadPump</strong></a><br/></td>
<td><blockquote>
[!Note]<br />
La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.
</blockquote>
<br/> Une pompe de thread exécute des tâches de façon asynchrone. Elle est créée en appelant <a href="d3dx11createthreadpump.md"><strong>D3DX11CreateThreadPump</strong></a>. Il existe plusieurs API qui prennent une pompe de thread facultative comme paramètre, comme <a href="d3dx11createtexturefromfile.md"><strong>D3DX11CreateTextureFromFile</strong></a> et <a href="d3dx11compilefromfile.md"><strong>D3DX11CompileFromFile</strong></a>; Si vous transmettez une interface de pompage de thread dans ces API, les fonctions s’exécutent de façon asynchrone sur un thread séparé. En particulier sur les ordinateurs multiprocesseurs, une pompe de threads peut charger des ressources et traiter des données sans une baisse notable des performances.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence D3DX 11](d3d11-graphics-reference-d3dx11.md)
</dt> </dl>

 

 





