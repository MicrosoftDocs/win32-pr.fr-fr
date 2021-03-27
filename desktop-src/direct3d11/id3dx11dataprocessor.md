---
title: Interface ID3DX11DataProcessor (D3DX11core. h)
description: 'Remarque : la bibliothèque de l’utilitaire D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store. Objet de traitement de données utilisé par l’interface ID3DX11ThreadPump pour le chargement des données de façon asynchrone.'
ms.assetid: ab893879-416f-4b17-9035-a7f03a62b753
keywords:
- Interface ID3DX11DataProcessor Direct3D 11
- Interface ID3DX11DataProcessor Direct3D 11, Description
topic_type:
- apiref
api_name:
- ID3DX11DataProcessor
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e421a6e840665220311e5a27c0692cd7f347e7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104971859"
---
# <a name="id3dx11dataprocessor-interface"></a>Interface ID3DX11DataProcessor

> [!Note]  
> La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.

 

Objet de traitement de données utilisé par l' [**interface ID3DX11ThreadPump**](id3dx11threadpump.md) pour le chargement des données de façon asynchrone.

## <a name="members"></a>Membres

L’interface **ID3DX11DataProcessor** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ID3DX11DataProcessor** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DX11DataProcessor** possède ces méthodes.



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
<td style="text-align: left;"><a href="id3dx11dataprocessor-createdeviceobject.md"><strong>CreateDeviceObject</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.
</blockquote>
<br/> Crée un objet appareil.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="id3dx11dataprocessor-destroy.md"><strong>Suppression</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.
</blockquote>
<br/> Détruit le processeur après la fin d’un élément de travail.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="id3dx11dataprocessor-process.md"><strong>Processus</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
La bibliothèque d’utilitaires D3DX (D3DX 9, D3DX 10 et D3DX 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications du Windows Store.
</blockquote>
<br/> Traite les données.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Notes

Cet objet peut être hérité et ses membres redéfinis pour le traitement des formats de fichier personnalisés.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>                                              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>D3DX11core. h</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>D3DX11. lib</dt> </dl>   |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Interfaces D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

