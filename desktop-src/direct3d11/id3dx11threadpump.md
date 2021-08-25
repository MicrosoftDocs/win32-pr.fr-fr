---
title: Interface ID3DX11ThreadPump (D3DX11core. h)
description: Une pompe de thread exécute des tâches de façon asynchrone.
ms.assetid: 1a99f728-149d-4800-a6e4-e3a00cf8cf4f
keywords:
- Interface ID3DX11ThreadPump Direct3D 11
- Interface ID3DX11ThreadPump Direct3D 11, Description
topic_type:
- apiref
api_name:
- ID3DX11ThreadPump
api_location:
- D3DX11.lib
- D3DX11.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b4bcfbc5fcf128f3ef71250180b487c83ce3c0d5430a563dfa3b7069e4235e1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119858039"
---
# <a name="id3dx11threadpump-interface"></a>Interface ID3DX11ThreadPump

> [!Note]  
> la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store.

 

Une pompe de thread exécute des tâches de façon asynchrone. Elle est créée en appelant [**D3DX11CreateThreadPump**](d3dx11createthreadpump.md). Il existe plusieurs API qui prennent une pompe de thread facultative comme paramètre, comme [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) et [**D3DX11CompileFromFile**](d3dx11compilefromfile.md); Si vous transmettez une interface de pompage de thread dans ces API, les fonctions s’exécutent de façon asynchrone sur un thread séparé. En particulier sur les ordinateurs multiprocesseurs, une pompe de threads peut charger des ressources et traiter des données sans une baisse notable des performances.

## <a name="members"></a>Membres

L’interface **ID3DX11ThreadPump** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ID3DX11ThreadPump** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **ID3DX11ThreadPump** possède ces méthodes.



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
<td style="text-align: left;"><a href="id3dx11threadpump-addworkitem.md"><strong>AddWorkItem</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store.
</blockquote>
<br/> Ajoute un élément de travail à la pompe de thread.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="id3dx11threadpump-getqueuestatus.md"><strong>GetQueueStatus</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store.
</blockquote>
<br/> Obtient le nombre d’éléments dans chacune des trois files d’attente à l’intérieur de la pompe de thread.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="id3dx11threadpump-getworkitemcount.md"><strong>GetWorkItemCount</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store.
</blockquote>
<br/> Obtient le nombre d’éléments de travail dans la pompe de thread.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="id3dx11threadpump-processdeviceworkitems.md"><strong>ProcessDeviceWorkItems</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store.
</blockquote>
<br/> Définit les éléments de travail sur l’appareil une fois qu’ils ont terminé le chargement et le traitement.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><a href="id3dx11threadpump-purgeallitems.md"><strong>PurgeAllItems</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store.
</blockquote>
<br/> Efface tous les éléments de travail de la pompe de thread.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><a href="id3dx11threadpump-waitforallitems.md"><strong>WaitForAllItems</strong></a></td>
<td style="text-align: left;"><blockquote>
[!Note]<br />
la bibliothèque d’utilitaires d3dx (d3dx 9, d3dx 10 et d3dx 11) est déconseillée pour Windows 8 et n’est pas prise en charge pour les applications Windows store.
</blockquote>
<br/> Attend la fin de l’exécution de tous les éléments de travail de la pompe de thread.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Remarques

### <a name="using-a-thread-pump"></a>Utilisation d’une pompe de thread

La pompe de thread charge et traite les données à l’aide du processus en trois étapes suivant :

1.  Chargez et décompressez les données avec un [**chargeur de données**](id3dx11dataloader.md). L’objet chargeur de données a trois méthodes que la pompe de thread appellera en interne lors du chargement et de la décompression des données : [**ID3DX11DataLoader :: Load**](id3dx11dataloader-load.md), [**ID3DX11DataLoader ::D eComPress**](id3dx11dataloader-decompress.md)et [**ID3DX11DataLoader ::D estroy**](id3dx11dataloader-destroy.md). La fonctionnalité spécifique de ces trois API diffère selon le type de données chargées et décompressées. L’interface de chargeur de données peut également être héritée et ses API peuvent être modifiées si l’une d’elles est en cours de chargement d’un fichier de données défini dans son propre format personnalisé.
2.  Traitez les données avec un [**processeur de données**](id3dx11dataprocessor.md). L’objet de traitement de données a trois méthodes que la pompe de thread appellera en interne lors du traitement des données : [**ID3DX11DataProcessor ::P tionnaire**](id3dx11dataprocessor-process.md), [**ID3DX11DataProcessor :: CreateDeviceObject**](id3dx11dataprocessor-createdeviceobject.md)et [**ID3DX11DataProcessor ::D estroy**](id3dx11dataprocessor-destroy.md). La façon dont il traite les données est différente selon le type de données. Par exemple, si les données sont une texture stockée en tant que JPEG, [**ID3DX11DataProcessor ::P tionnaire**](id3dx11dataprocessor-process.md) effectue la décompression JPEG pour obtenir les bits d’image RAW de l’image. Si les données sont un nuanceur, [**ID3DX11DataProcessor ::P tionnaire**](id3dx11dataprocessor-process.md) compile le langage HLSL en bytecode. Une fois les données traitées, un objet périphérique sera créé pour ces données (avec [**ID3DX11DataProcessor :: CreateDeviceObject**](id3dx11dataprocessor-createdeviceobject.md)) et l’objet sera ajouté à une file d’attente d’objets périphériques. L’interface du processeur de données peut également être héritée et ses API peuvent être modifiées si l’une d’elles est en cours de traitement d’un fichier de données défini dans son propre format personnalisé.
3.  Liez l’objet appareil à l’appareil. Cette opération est effectuée quand une application appelle [**ID3DX11ThreadPump ::P rocessdeviceworkitems**](id3dx11threadpump-processdeviceworkitems.md), qui lie un nombre spécifié d’objets dans la file d’attente d’objets d’appareil à l’appareil.

La pompe de threads peut être utilisée pour charger des données de deux manières : en appelant une API qui prend une pompe de thread comme paramètre, tel que [**D3DX11CreateTextureFromFile**](d3dx11createtexturefromfile.md) et [**D3DX11CompileFromFile**](d3dx11compilefromfile.md), ou en appelant [**ID3DX11ThreadPump :: AddWorkItem**](id3dx11threadpump-addworkitem.md). Dans le cas des API qui prennent une pompe de thread, le chargeur de données et le processeur de données sont créés en interne. Dans le cas de AddWorkItem, le chargeur de données et le processeur de données doivent être créés au préalable et sont ensuite passés à AddWorkItem. D3DX11 fournit un ensemble d’API permettant de créer des chargeurs de données et des processeurs de données qui disposent de fonctionnalités pour le chargement et le traitement des formats de données courants. Pour les formats de données personnalisés, les interfaces du chargeur de données et du processeur de données doivent être héritées et leurs méthodes doivent être redéfinies.

L’objet thread Pump occupe une quantité importante de ressources. en général, un seul doit être créé par application.

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

 

