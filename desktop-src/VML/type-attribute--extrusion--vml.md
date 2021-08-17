---
title: Attribut type (extrusion) (VML)
description: Attribut type (extrusion) (VML)
ms.assetid: 2c7ad2f1-fb5d-49fb-b490-3efe59ee5177
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a14c3b69aa4156cbd94bb8598caa80ccd92721574daafe074486eb293059cae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057581"
---
# <a name="type-attribute-extrusionvml"></a>Attribut type (extrusion) (VML)

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Définit la façon dont la forme est extrudée. En lecture/écriture. **Chaîne**.

**S’applique à**

[Extrusion](msdn-online-vml-extrusion-element.md)

**Syntaxe de balise**

<o : type d' *élément* = « *expression* » >

**Syntaxe du script**

*Element* . type = "*expression*"

*expression* = *Element*. type

**Remarques**

Ces valeurs comprennent :



| Valeur       | Description                                                                                                                                                            |
|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| parallel    | L’extrusion est rendue afin que le centre de projection soit éloigné à l’infini. autrement dit, les lignes d’extrusion ne convergent pas (contrairement aux projections de perspective). Par défaut. |
| perspective | L’extrusion est rendue au centre de projection, qui est le même que le point de fuite pour les objets non pivotés.                                                       |



 

**Microsoft Office Attribut extensions**

 

 