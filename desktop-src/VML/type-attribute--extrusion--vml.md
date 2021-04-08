---
title: Attribut type (extrusion) (VML)
description: Attribut type (extrusion) (VML)
ms.assetid: 2c7ad2f1-fb5d-49fb-b490-3efe59ee5177
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14bc91f9348603bc89189debb2255f8fff39e135
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842502"
---
# <a name="type-attribute-extrusionvml"></a>Attribut type (extrusion) (VML)

Cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). Pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows Internet Explorer, consultez le [Centre de développement Internet Explorer](https://msdn.microsoft.com/ie/).

 

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



 

**Attribut extensions Microsoft Office**

 

 