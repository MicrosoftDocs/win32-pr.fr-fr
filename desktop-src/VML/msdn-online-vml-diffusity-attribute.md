---
title: Attribut de diffusion VML
description: Attribut de diffusion VML
ms.assetid: 1d131540-9166-47fc-bb0d-fada38f6a3de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b311c70e1cf49ece7f0072d70b07e886d11f0fe9122fc5d248a32f4321ba19b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754734"
---
# <a name="vml-diffusity-attribute"></a>Attribut de diffusion VML

cette rubrique décrit VML, une fonctionnalité déconseillée à partir de Windows Internet Explorer 9. Les pages Web et les applications qui reposent sur VML doivent être migrées vers SVG ou d’autres normes largement prises en charge.

> [!Note]  
> Depuis le 2011 décembre, cette rubrique a été archivée. Par conséquent, il n’est plus activement conservé. Pour plus d’informations, consultez [contenu archivé](/previous-versions/windows/internet-explorer/ie-developer/). pour obtenir des informations, des recommandations et des conseils relatifs à la version actuelle de Windows internet explorer, consultez le [centre de développement internet explorer](https://msdn.microsoft.com/ie/).

 

Définit la quantité de diffusion de la lumière réfléchie à partir d’une forme extrudée. En lecture/écriture. **VgNumber**.

**S’applique à**

[Extrusion](msdn-online-vml-extrusion-element.md)

**Syntaxe de balise**

<o : diffusion d' *élément* = " *expression* " >

**Syntaxe du script**

*Element* . diffusion = "*expression*"

*expression* = *élément*. diffusion

**Remarques**

Cette valeur définit le rapport entre l’incident et la lumière réfléchie. Les valeurs normales sont comprises entre 0 et 1. La valeur par défaut est 0.

Si les valeurs supérieures à 1 sont spécifiées, des effets inhabituels peuvent se produire.

*Microsoft Office Attribut extensions*

 

 