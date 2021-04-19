---
description: Filtre de l’analyseur de fichiers multiples
ms.assetid: 8ef06f49-fda4-49e2-9b07-70453a2e897c
title: Filtre de l’analyseur de fichiers multiples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44fc83a56bb12c307b85be875a3a2e7e73b744d9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106515537"
---
# <a name="multi-file-parser-filter"></a>Filtre de l’analyseur de fichiers multiples

Le filtre de l’analyseur de fichiers multiples analyse un format de fichier simple qui permet de spécifier plusieurs noms de fichiers comme s’il s’agissait d’un seul fichier. Ces fichiers ont le format indiqué dans l’exemple suivant :


```C++
;MULTI
https://server/share/video.mpg
https://server/share/captions.smi
```



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
<li>Type majeur : MEDIATYPE_Stream</li>
<li>Sous-type : CLSID_MultFile</li>
<li>Type de format : GUID_NULL</li>
</ul></td>
</tr>
<tr class="odd">
<td>Interfaces pin d’entrée</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>Types de média de broche de sortie</td>
<td><ul>
<li>Type majeur : MEDIATYPE_File</li>
<li>Sous-type : GUID_NULL</li>
<li>Type de format : MEDIATYPE_File</li>
</ul></td>
</tr>
<tr class="odd">
<td>Interfaces de broche de sortie</td>
<td><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></td>
</tr>
<tr class="even">
<td>CLSID du filtre</td>
<td>CLSID_MultFile</td>
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

Le filtre crée une broche de sortie pour chaque fichier figurant dans le fichier source. Le type de sortie est \_ fichier MediaType et le bloc de format pour le type de sortie est une chaîne à caractères larges qui contient le nom de fichier. Chaque code confidentiel se connecte à une instance du filtre de [convertisseur de flux de fichier](file-stream-renderer-filter.md) . Le filtre de convertisseur de flux de fichier crée une broche de sortie, qui expose l’interface [**IStreamBuilder**](/windows/desktop/api/Strmif/nn-strmif-istreambuilder) . La broche de sortie restitue le fichier spécifié. Aucune donnée multimédia ne transite entre l’analyseur de fichiers multiples et le convertisseur de flux de fichier.

Le CLSID du filtre n’est pas défini dans UUID. h. Utilisez cette macro dans votre propre fichier d’en-tête :


```C++
// {D51BD5A3-7548-11cf-A520-0080C77EF58A}
DEFINE_GUID(CLSID_MultFile,
0xd51bd5a3, 0x7548, 0x11cf, 0xa5, 0x20, 0x0, 0x80, 0xc7, 0x7e, 0xf5, 0x8a);
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Filtres DirectShow](directshow-filters.md)
</dt> </dl>

 

 



