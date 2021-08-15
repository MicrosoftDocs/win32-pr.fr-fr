---
description: Cette rubrique répertorie les constructeurs de la classe font. Pour obtenir une liste complète des classes, consultez font Class.
ms.assetid: a0169751-50f6-41d9-bd59-3c85aec1bb78
title: Fonts, constructeurs de police
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: ff876120655adcf58318a471ed66ddfa4502d625305d9fda37f01c966e19e0cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118977899"
---
# <a name="fontfont-constructors"></a>Fonts, constructeurs de police

Cette rubrique répertorie les constructeurs de la classe [**font**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-font) . Pour obtenir une liste complète des classes, consultez **font Class**.

### <a name="overload-list"></a>Liste de surcharge



| Constructeur                                                                                                                   | Description                                                                                                                                                                                                                                                                                                  |
|:------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Police (HDC, HFONT)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconsthfont))                                                                | Crée un objet [**font :: font**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconsthfont)) indirectement à partir d’une police logique GDI à l’aide d’un handle vers une structure GDI **LOGFONT** .<br/>                                                                                                                                   |
| [**Font (HDC, LOGFONTA \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconstlogfonta))                                            | Crée un objet [**font :: font**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconstlogfonta)) directement à partir d’une police logique GDI. La police logique GDI est une structure **LOGFONTA** , qui est la version à caractères codés sur un octet d’une police logique. Ce constructeur est fourni à des fins de compatibilité avec GDI.<br/> |
| [**Font (HDC, LOGFONTW \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconstlogfontw))                                            | Crée un objet [**font :: font**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc_inconstlogfontw)) directement à partir d’une police logique GDI. La police logique GDI est une structure **LOGFONTW** , qui est la version à caractères larges d’une police logique. Ce constructeur est fourni à des fins de compatibilité avec GDI.<br/>     |
| [**Police (FontFamily \* , Real, int, Unit)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inconstfontfamily_inreal_inint_inunit))                                | Crée un objet [**font :: font**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inconstfontfamily_inreal_inint_inunit)) basé sur un objet [**FontFamily**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) , une taille, un style de police et une unité de mesure.<br/>                                                                               |
| [**Police (WCHAR \* , Real, int, Unit, FontCollection \* )**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inconstwchar_inreal_inint_inunit_inconstfontcollection)) | Crée un objet [**font :: font**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inconstwchar_inreal_inint_inunit_inconstfontcollection)) basé sur une famille de polices, une taille, un style de police, une unité de mesure et un objet [**FontCollection**](/windows/win32/api/gdiplusheaders/nl-gdiplusheaders-fontcollection) .<br/>                                     |
| [**Police (HDC)**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc))                                                                            | Crée un objet [**font :: font**](/windows/win32/api/gdiplusheaders/nf-gdiplusheaders-font-font(inhdc)) en fonction de l’objet de police GDI qui est actuellement sélectionné dans un contexte de périphérique spécifié. Ce constructeur est fourni à des fins de compatibilité avec GDI. <br/>                                                                           |



 

 
