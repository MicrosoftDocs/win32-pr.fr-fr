---
description: Filtre de convertisseur de flux de fichier
ms.assetid: e26462bb-e67f-4522-bec2-88378c4ff442
title: Filtre de convertisseur de flux de fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a64c8d8a0c87dab3aa811c8246be24ded8ee04dc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104522316"
---
# <a name="file-stream-renderer-filter"></a>Filtre de convertisseur de flux de fichier

Le filtre de convertisseur de flux de fichier restitue les noms de fichiers qui sont analysés par le filtre de l' [Analyseur de fichiers multiples](multi-file-parser-filter.md) . Pour plus d’informations, consultez la documentation de ce filtre.

L’utilisation de ce filtre est déconseillée. Pour afficher plusieurs fichiers dans le même graphique de filtre, l’application doit simplement appeler **RenderFile** ou **AddSourceFilter** plusieurs fois.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Interfaces de filtre</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></td>
</tr>
<tr class="even">
<td>Types de média de broche d’entrée</td>
<td><ul>
<li>Type majeur : MEDIATYPE_File</li>
<li>Sous-type : GUID_NULL</li>
<li>Type de format : MEDIATYPE_File</li>
</ul></td>
</tr>
<tr class="odd">
<td>Interfaces pin d’entrée</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Types de média de broche de sortie</td>
<td>Aucun</td>
</tr>
<tr class="odd">
<td>Interfaces de broche de sortie</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-istreambuilder"><strong>IStreamBuilder</strong></a></td>
</tr>
<tr class="even">
<td>CLSID du filtre</td>
<td>CLSID_FileRend</td>
</tr>
<tr class="odd">
<td>Exécutable</td>
<td>Quartz.dll</td>
</tr>
<tr class="even">
<td><a href="merit.md">Mérite</a></td>
<td>MERIT_UNLIKELY</td>
</tr>
<tr class="odd">
<td><a href="filter-categories.md">Catégorie de filtre</a></td>
<td>CLSID_LegacyAmFilterCategory</td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Notes

Le CLSID du filtre n’est pas défini dans UUID. h. Utilisez cette macro dans votre propre fichier d’en-tête :


```C++
// {D51BD5A5-7548-11cf-A520-0080C77EF58A}
DEFINE_GUID(CLSID_FileRend,
0xd51bd5A5, 0x7548, 0x11cf, 0xa5, 0x20, 0x0, 0x80, 0xc7, 0x7e, 0xf5, 0x8a);
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Filtres DirectShow](directshow-filters.md)
</dt> </dl>

 

 



