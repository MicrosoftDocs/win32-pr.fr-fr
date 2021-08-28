---
title: Interface ID3DX11DataLoader (D3DX11core. h)
description: 'remarque : la bibliothèque de l’utilitaire d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store. Objet chargeant des données utilisé par l’interface ID3DX11ThreadPump pour le chargement des données de façon asynchrone.'
ms.assetid: 878929ea-0228-4650-9ca0-f83d60d9f915
keywords:
- Interface ID3DX11DataLoader Direct3D 11
- Interface ID3DX11DataLoader Direct3D 11, Description
topic_type:
- apiref
api_name:
- ID3DX11DataLoader
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91d589c6393642829eed6d803f8b8ac306c41b9fe88f0f16f69e30abf55311b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120096269"
---
# <a name="id3dx11dataloader-interface"></a>Interface ID3DX11DataLoader

> [!Note]  
> la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store.

 

Objet chargeant des données utilisé par l' [**interface ID3DX11ThreadPump**](id3dx11threadpump.md) pour le chargement des données de façon asynchrone.

## <a name="members"></a>Membres

L’interface **ID3DX11DataLoader** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ID3DX11DataLoader** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DX11DataLoader** possède ces méthodes.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Méthode</th>
<th style="text-align: left;">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="id3dx11dataloader-decompress.md"><strong>Décompresser</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store.
</blockquote>
<br/> Décompresse les données encodées.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="id3dx11dataloader-destroy.md"><strong>Suppression</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store.
</blockquote>
<br/> Détruit le chargeur après l’achèvement d’un élément de travail.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="id3dx11dataloader-load.md"><strong>Load</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store.
</blockquote>
<br/> Charge des données à partir d’un disque.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Remarques

Cet objet peut être hérité et ses membres redéfinis. Cela vous permettrait de personnaliser l’API pour le chargement et la décompression de vos propres formats de fichiers personnalisés.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | applications de \[ bureau Windows 7 uniquement\]<br/>                                              |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 R2, \[ applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>D3DX11core. h</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>D3DX11. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Interfaces D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

