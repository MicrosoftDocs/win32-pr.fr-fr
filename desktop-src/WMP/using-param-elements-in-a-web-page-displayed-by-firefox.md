---
title: Utilisation d’éléments PARAM dans une page Web affichée par Firefox
description: Utilisation d’éléments PARAM dans une page Web affichée par Firefox
ms.assetid: 8403c6f4-f221-4411-b49c-f0c9c22943df
keywords:
- Lecteur Windows Media, éléments PARAM dans l’élément OBJECT
- Lecteur Windows Media modèle objet, éléments PARAM dans l’élément object
- modèle objet, éléments PARAM dans l’élément OBJECT
- Lecteur Windows Media Mobile, éléments PARAM dans l’élément OBJECT
- Lecteur Windows Media ActiveX contrôle, éléments PARAM dans l’élément OBJECT
- Lecteur Windows Media contrôle Mobile ActiveX, éléments PARAM dans l’élément OBJECT
- contrôle ActiveX, éléments PARAM dans l’élément OBJECT
- incorporation, pages Web
- Incorporation de pages Web, éléments PARAM dans l’élément OBJECT
- PARAM, éléments dans l’élément OBJECT
- Lecteur Windows Media, Firefox
- modèle objet Lecteur Windows Media, Firefox
- modèle objet, Firefox
- Lecteur Windows Media Mobile, Firefox
- Lecteur Windows Media ActiveX contrôle, Firefox
- Lecteur Windows Media contrôle de ActiveX Mobile, Firefox
- contrôle ActiveX, Firefox
- Firefox, éléments PARAM dans l’élément OBJECT
- Incorporation de pages Web, Firefox
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b045d111ff3cd0de09f54a8cf7ac25028fa1dc6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127311089"
---
# <a name="using-param-elements-in-a-web-page-displayed-by-firefox"></a>Utilisation d’éléments PARAM dans une page Web affichée par Firefox

Vous pouvez utiliser des éléments PARAM à l’intérieur d’un élément OBJECT pour définir l’état initial du contrôle Player. Par exemple, les éléments PARAM de l’exemple suivant spécifient que le contrôle doit jouer à Seattle. wmv automatiquement.


```HTML
<OBJECT id="Player" type="application/x-ms-wmp" width="300" height="200">
  <PARAM name="url" value="c:\MediaFiles\seattle.wmv" />
  <PARAM name="autostart" value="true" />
</OBJECT>

```



La plupart des éléments PARAM peuvent être interprétés par Internet Explorer et par Firefox. Toutefois, il existe quelques éléments PARAM que le plug-in Firefox ne prend pas en charge. Pour plus d’informations sur les éléments PARAM pris en charge par le plug-in Firefox, consultez [éléments param dans un élément Object](param-elements-in-an-object-element.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**utilisation du contrôle Lecteur Windows Media avec Firefox**](using-the-windows-media-player-control-with-firefox.md)
</dt> </dl>

 

 




