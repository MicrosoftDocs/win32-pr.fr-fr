---
description: Filtre de convertisseur de flux de fichier
ms.assetid: e26462bb-e67f-4522-bec2-88378c4ff442
title: Filtre de convertisseur de flux de fichier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d438d77b4f402cefed2e80f2c32d061d1652710f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127224436"
---
# <a name="file-stream-renderer-filter"></a>Filtre de convertisseur de flux de fichier

Le filtre de convertisseur de flux de fichier restitue les noms de fichiers qui sont analysés par le filtre de l' [Analyseur de fichiers multiples](multi-file-parser-filter.md) . Pour plus d’informations, consultez la documentation de ce filtre.

L’utilisation de ce filtre est déconseillée. Pour afficher plusieurs fichiers dans le même graphique de filtre, l’application doit simplement appeler **RenderFile** ou **AddSourceFilter** plusieurs fois.




| Étiquette | Valeur |
|--------|-------|
| Interfaces de filtre | <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a> | 
| Types de média de broche d’entrée | <ul><li>Type majeur : MEDIATYPE_File</li><li>Sous-type : GUID_NULL</li><li>Type de format : MEDIATYPE_File</li></ul> | 
| Interfaces pin d’entrée | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a> | 
| Types de média de broche de sortie | None | 
| Interfaces de broche de sortie | <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPIN</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-istreambuilder"><strong>IStreamBuilder</strong></a> | 
| CLSID du filtre | CLSID_FileRend | 
| Exécutable | Quartz.dll | 
| <a href="merit.md">Mérite</a> | MERIT_UNLIKELY | 
| <a href="filter-categories.md">Catégorie de filtre</a> | CLSID_LegacyAmFilterCategory | 




 

## <a name="remarks"></a>Notes

Le CLSID du filtre n’est pas défini dans UUID. h. Utilisez cette macro dans votre propre fichier d’en-tête :


```C++
// {D51BD5A5-7548-11cf-A520-0080C77EF58A}
DEFINE_GUID(CLSID_FileRend,
0xd51bd5A5, 0x7548, 0x11cf, 0xa5, 0x20, 0x0, 0x80, 0xc7, 0x7e, 0xf5, 0x8a);
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[DirectShow Filtres](directshow-filters.md)
</dt> </dl>

 

 



