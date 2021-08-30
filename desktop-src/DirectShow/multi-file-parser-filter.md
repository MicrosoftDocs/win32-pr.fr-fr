---
description: Filtre de l’analyseur de fichiers multiples
ms.assetid: 8ef06f49-fda4-49e2-9b07-70453a2e897c
title: Filtre de l’analyseur de fichiers multiples
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 444eebb6ff16b7b6d5568b47c939f687bb3207c8
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474625"
---
# <a name="multi-file-parser-filter"></a>Filtre de l’analyseur de fichiers multiples

Le filtre de l’analyseur de fichiers multiples analyse un format de fichier simple qui permet de spécifier plusieurs noms de fichiers comme s’il s’agissait d’un seul fichier. Ces fichiers ont le format indiqué dans l’exemple suivant :


```C++
;MULTI
https://server/share/video.mpg
https://server/share/captions.smi
```



L’utilisation de ce filtre est déconseillée. Pour afficher plusieurs fichiers dans le même graphique de filtre, l’application doit simplement appeler **RenderFile** ou **AddSourceFilter** plusieurs fois.




| | | Filtrer les interfaces | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a> | | Types de média de broche d’entrée | <ul><li>Type majeur : MEDIATYPE_Stream</li><li>Sous-type : CLSID_MultFile</li><li>Type de format : GUID_NULL</li></ul> | | Interfaces pin d’entrée | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | Types de média de broche de sortie | <ul><li>Type majeur : MEDIATYPE_File</li><li>Sous-type : GUID_NULL</li><li>Type de format : MEDIATYPE_File</li></ul> | | Interfaces de broche de sortie | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a> | | CLSID du filtre | CLSID_MultFile | | Fichier exécutable | Quartz.dll | | <a href="merit.md">Mérite</a> | MERIT_UNLIKELY | | <a href="filter-categories.md">Catégorie de filtre</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>Remarques

Le filtre crée une broche de sortie pour chaque fichier figurant dans le fichier source. Le type de sortie est \_ fichier MediaType et le bloc de format pour le type de sortie est une chaîne à caractères larges qui contient le nom de fichier. Chaque code confidentiel se connecte à une instance du filtre de [convertisseur de flux de fichier](file-stream-renderer-filter.md) . Le filtre de convertisseur de flux de fichier crée une broche de sortie, qui expose l’interface [**IStreamBuilder**](/windows/desktop/api/Strmif/nn-strmif-istreambuilder) . La broche de sortie restitue le fichier spécifié. Aucune donnée multimédia ne transite entre l’analyseur de fichiers multiples et le convertisseur de flux de fichier.

Le CLSID du filtre n’est pas défini dans UUID. h. Utilisez cette macro dans votre propre fichier d’en-tête :


```C++
// {D51BD5A3-7548-11cf-A520-0080C77EF58A}
DEFINE_GUID(CLSID_MultFile,
0xd51bd5a3, 0x7548, 0x11cf, 0xa5, 0x20, 0x0, 0x80, 0xc7, 0x7e, 0xf5, 0x8a);
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DirectShow Filtres](directshow-filters.md)
</dt> </dl>

 

 



