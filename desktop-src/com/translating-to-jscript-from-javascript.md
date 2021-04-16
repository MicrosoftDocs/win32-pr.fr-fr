---
title: Conversion en JScript à partir de JavaScript
description: Conversion en JScript à partir de JavaScript
ms.assetid: 86067a69-a6a1-474f-b8d8-85caf384a311
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45535807a5ef2baf59c2e068007a5a8df8bf4863
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104507818"
---
# <a name="translating-to-jscript-from-javascript"></a>Conversion en JScript à partir de JavaScript

JScript est en grande partie compatible avec JavaScript. Toutefois, JScript version 5,0 comprend certains objets qui ne sont actuellement pas pris en charge par JavaScript, tels que ActiveXObject, Enumerator, Error, global et VBArray.

JScript 5,0 prend en charge la gestion des exceptions via **try**... instructions **catch** . JavaScript ne fournit pas actuellement de mécanisme de gestion des erreurs.

Lors de l’utilisation de JScript ou JavaScript, il existe quelques différences subtiles entre les implémentations de modèle objet prises en charge par différents navigateurs Web. Pour écrire un script qui s’exécute à la fois sur Internet Explorer et Netscape Navigator, limitez les fonctionnalités utilisées par vos scripts à celles spécifiées dans la norme World Wide Web Consortium (W3C) pour HTML version 3,2. Pour plus d’informations sur cette norme, consultez [spécification de référence HTML 3,2](https://www.w3.org/TR/REC-html32.html).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Traduire en JScript](translating-to-jscript.md)
</dt> </dl>

 

 




