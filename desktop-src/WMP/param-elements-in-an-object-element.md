---
title: Éléments PARAM dans un élément OBJECT
description: Éléments PARAM dans un élément OBJECT
ms.assetid: f9229d92-3a7e-4ba4-a84c-20e60f2482dc
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
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7da684a39739703038793abb2f4fdd32b924f35cdffc0c0f9d796fb7dbb5532b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054427"
---
# <a name="param-elements-in-an-object-element"></a>Éléments PARAM dans un élément OBJECT

Lecteur Windows Media utilise l’élément PARAM pour définir des conditions de démarrage spécifiques pour le contrôle. L’élément PARAM est incorporé à l’intérieur de l’élément OBJECT.

Par exemple, si vous souhaitez définir si la propriété **AutoStart** a la valeur true, vous devez incorporer l’élément param à l’intérieur de l’élément Object.


```HTML
<OBJECT ID="Player"
  CLASSID="CLSID:6BF52A52-394A-11d3-B153-00C04F79FAA6">
    <PARAM name="autoStart" value="True">
</OBJECT>
```



Vous pouvez avoir autant d’éléments PARAM dans un élément objet que vous le souhaitez. PARAM a deux attributs, Name et value. Les deux attributs doivent être définis.

Les attributs PARAM pris en charge varient légèrement entre les navigateurs et les types MIME. Le tableau suivant répertorie les attributs pris en charge par les navigateurs Internet Explorer et Firefox. Le type MIME préféré pour le navigateur Firefox est application/x-ms-WMP. Toutefois, il existe plusieurs autres types MIME que vous pouvez utiliser pour incorporer le contrôle du lecteur dans une page Web hébergée par le navigateur Firefox. La quatrième colonne du tableau indique les attributs pris en charge lorsque vous utilisez un type MIME autre que application/x-ms-WMP.



| Nom du paramètre                                            | Internet Explorer | Firefox avec type MIME application/x-ms-WMP | Firefox avec tout autre type MIME |
|-------------------------------------------------------|-------------------|---------------------------------------------|----------------------------------|
| [Démarrage automatique](settings-autostart.md)                   | oui               | oui                                         | oui                              |
| [équilibrée](settings-balance.md)                       | oui               | oui                                         | oui                              |
| [baseURL](settings-baseurl.md)                       | oui               | oui                                         | oui                              |
| [captioningID](closedcaption-captioningid.md)        | oui               | oui                                         | oui                              |
| [currentMarker](controls-currentmarker.md)           | oui               | oui                                         | oui                              |
| [currentPosition](controls-currentposition.md)       | oui               | oui                                         | oui                              |
| [defaultFrame](settings-defaultframe.md)             | oui               | non                                          | non                               |
| [enableContextMenu](player-enablecontextmenu.md)     | oui               | oui                                         | oui                              |
| [activé](player-enabled.md)                         | oui               | oui                                         | oui                              |
| [enableErrorDialogs](settings-enableerrordialogs.md) | oui               | oui                                         | non                               |
| **fileName**                                          | non                | oui                                         | oui                              |
| [Large](player-fullscreen.md)                   | oui               | non                                          | non                               |
| [invokeURLs](settings-invokeurls.md)                 | oui               | non                                          | non                               |
| [muette](settings-mute.md)                             | oui               | oui                                         | oui                              |
| [playCount](settings-playcount.md)                   | oui               | oui                                         | non                               |
| [évaluation](settings-rate.md)                             | oui               | oui                                         | oui                              |
| [SAMIFileName](closedcaption-samifilename.md)        | oui               | oui                                         | oui                              |
| [SAMILang](closedcaption-samilang.md)                | oui               | oui                                         | oui                              |
| [SAMIStyle](closedcaption-samistyle.md)              | oui               | oui                                         | oui                              |
| **SOURCES**                                               | non                | oui                                         | oui                              |
| [stretchToFit](player-stretchtofit.md)               | oui               | oui                                         | non                               |
| [URL](player-url.md)                                 | oui               | oui                                         | oui                              |
| [volume](settings-volume.md)                         | oui               | oui                                         | oui                              |
| [windowlessVideo](player-windowlessvideo.md)         | oui               | oui                                         | oui                              |



 

> [!Note]  
> Les éléments **filename** et **src** param sont pris en charge par le plug-in Firefox, mais pas par Internet Explorer. Elles exécutent toutes les deux la même fonction que l’élément **URL** param.

 

Pour plus d’informations sur les valeurs de chaque attribut de nom, consultez [Référence du modèle objet pour l’écriture de scripts](object-model-reference-for-scripting.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**utilisation du contrôle Lecteur Windows Media dans une Page Web**](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




