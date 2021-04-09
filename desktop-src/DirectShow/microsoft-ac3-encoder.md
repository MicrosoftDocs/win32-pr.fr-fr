---
description: Le filtre d’encodeur AC-3 microsoft Encode le son stéréo PCM sur un flux de données numérique Dolby Digital.
ms.assetid: 59d46ee2-d45f-4492-938d-39c55a7368e1
title: Encodeur AC-3 Microsoft (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 160b020e07bb3ba4e4dc5636b58dd0e66f581a6f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109179"
---
# <a name="microsoft-ac-3-encoder"></a>Encodeur AC-3 Microsoft

Le filtre d’encodeur AC-3 microsoft Encode le son stéréo PCM sur un flux de données numérique Dolby Digital.

> [!Note]  
> L’implémentation Microsoft de la technologie Dolby Digital est limitée aux termes du programme de gestion de licences Dolby Digital à utiliser par les applications Microsoft.

 

> [!Note]  
> Ce filtre n’est pas pris en charge sur les plateformes IA-64.

 



Informations de filtre

Interfaces de filtre

[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/>

Types de média de broche d’entrée

**MediaType \_ Audio**, **MEDIASUBTYPE \_ PCM**<br/> Le type d’entrée doit être stéréo de 48 kHz, 16 bits par échantillon.<br/>

Interfaces pin d’entrée

[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

Types de média de broche de sortie

**MediaType \_ Audio**, **MEDIASUBTYPE \_ Dolby \_ AC3**<br/> **MediaType \_ Stream**, **MEDIASUBTYPE \_ Dolby \_ AC3**<br/>

Interfaces de broche de sortie

[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

CLSID du filtre

**CLSID \_ CMSAC3Enc** (déclaré dans wmcodecdsp. h)

Exécutable

msac3enc.dll

[Mérite](merit.md)

**MÉRITE \_ n' \_ \_ utilise pas**

[Catégorie de filtre](filter-categories.md)

**CLSID \_ LegacyAmFilterCategory**



 

## <a name="remarks"></a>Notes

Ce filtre n’est pas disponible pour une utilisation par des applications tierces.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista Édition familiale Premium, Windows Vista Édition intégrale, Windows 7 Édition familiale Premium, Windows 7 professionnel, Windows 7 entreprise, applications de bureau Windows 7 édition intégrale \[ uniquement\]<br/> |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                                                                                     |
| En-tête<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl>                                                                                       |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Filtres DirectShow](directshow-filters.md)
</dt> </dl>

 

 




