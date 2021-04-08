---
title: Éléments PARAM dans un élément OBJECT
description: Éléments PARAM dans un élément OBJECT
ms.assetid: f9229d92-3a7e-4ba4-a84c-20e60f2482dc
keywords:
- Lecteur Windows Media, éléments PARAM dans l’élément OBJECT
- Windows Media Player Object Model, PARAM, éléments dans l’élément OBJECT
- modèle objet, éléments PARAM dans l’élément OBJECT
- Windows Media Player Mobile, éléments PARAM dans l’élément OBJECT
- Windows Media Player ActiveX Control, PARAM, éléments dans l’élément OBJECT
- Windows Media Player Mobile contrôle ActiveX, éléments PARAM dans l’élément OBJECT
- Contrôle ActiveX, éléments PARAM dans l’élément OBJECT
- incorporation, pages Web
- Incorporation de pages Web, éléments PARAM dans l’élément OBJECT
- PARAM, éléments dans l’élément OBJECT
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3f0fc5b9f64fa462386ec037eba34ed4e0659bb1
ms.sourcegitcommit: e22adfb0dd3bb989e59455baedb4d905a877a240
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/21/2019
ms.locfileid: "103840930"
---
# <a name="param-elements-in-an-object-element"></a>Éléments PARAM dans un élément OBJECT

Le lecteur Windows Media utilise l’élément PARAM pour définir des conditions de démarrage spécifiques pour le contrôle. L’élément PARAM est incorporé à l’intérieur de l’élément OBJECT.

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
| [Démarrage automatique](settings-autostart.md)                   | Oui               | Oui                                         | Oui                              |
| [équilibrée](settings-balance.md)                       | Oui               | Oui                                         | Oui                              |
| [baseURL](settings-baseurl.md)                       | Oui               | Oui                                         | Oui                              |
| [captioningID](closedcaption-captioningid.md)        | Oui               | Oui                                         | Oui                              |
| [currentMarker](controls-currentmarker.md)           | Oui               | Oui                                         | Oui                              |
| [currentPosition](controls-currentposition.md)       | Oui               | Oui                                         | Oui                              |
| [defaultFrame](settings-defaultframe.md)             | Oui               | non                                          | non                               |
| [enableContextMenu](player-enablecontextmenu.md)     | Oui               | Oui                                         | Oui                              |
| [activé](player-enabled.md)                         | Oui               | Oui                                         | Oui                              |
| [enableErrorDialogs](settings-enableerrordialogs.md) | Oui               | Oui                                         | non                               |
| **fileName**                                          | non                | Oui                                         | Oui                              |
| [Large](player-fullscreen.md)                   | Oui               | non                                          | non                               |
| [invokeURLs](settings-invokeurls.md)                 | Oui               | non                                          | non                               |
| [muette](settings-mute.md)                             | Oui               | Oui                                         | Oui                              |
| [playCount](settings-playcount.md)                   | Oui               | Oui                                         | non                               |
| [évaluation](settings-rate.md)                             | Oui               | Oui                                         | Oui                              |
| [SAMIFileName](closedcaption-samifilename.md)        | Oui               | Oui                                         | Oui                              |
| [SAMILang](closedcaption-samilang.md)                | Oui               | Oui                                         | Oui                              |
| [SAMIStyle](closedcaption-samistyle.md)              | Oui               | Oui                                         | Oui                              |
| **SOURCES**                                               | non                | Oui                                         | Oui                              |
| [stretchToFit](player-stretchtofit.md)               | Oui               | Oui                                         | non                               |
| [URL](player-url.md)                                 | Oui               | Oui                                         | Oui                              |
| [volume](settings-volume.md)                         | Oui               | Oui                                         | Oui                              |
| [windowlessVideo](player-windowlessvideo.md)         | Oui               | Oui                                         | Oui                              |



 

> [!Note]  
> Les éléments **filename** et **src** param sont pris en charge par le plug-in Firefox, mais pas par Internet Explorer. Elles exécutent toutes les deux la même fonction que l’élément **URL** param.

 

Pour plus d’informations sur les valeurs de chaque attribut de nom, consultez [Référence du modèle objet pour l’écriture de scripts](object-model-reference-for-scripting.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Utilisation du contrôle du lecteur Windows Media dans une page Web**](using-the-windows-media-player-control-in-a-web-page.md)
</dt> </dl>

 

 




