---
title: Conversion en JavaScript à partir de JScript
description: Conversion en JavaScript à partir de JScript
ms.assetid: 11d31c8c-868d-4220-9298-6d24a209dc47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71b18972f407cf008626245798b3f7740d98058e
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 02/20/2020
ms.locfileid: "104381609"
---
# <a name="translating-to-javascript-from-jscript"></a>Conversion en JavaScript à partir de JScript

JScript est en grande partie compatible avec JavaScript. Toutefois, JScript comprend certains objets qui ne sont actuellement pas pris en charge par JavaScript, tels que ActiveXObject, Enumerator, Error, global et VBArray.

JScript version 5,0 prend en charge la gestion des exceptions via **try**... instructions **catch** . JavaScript ne fournit pas actuellement de mécanisme de gestion des erreurs.

Lors de l’utilisation de JScript ou JavaScript, il existe quelques différences subtiles entre les implémentations de modèle objet prises en charge par différents navigateurs Web. Pour écrire un script qui s’exécute à la fois sur Internet Explorer et Netscape Navigator, limitez les fonctionnalités utilisées par vos scripts à celles spécifiées dans la norme World Wide Web Consortium (W3C) [pour HTML version 3,2](https://www.w3.org/tr/rec-html32.html).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Conversion en JavaScript](translating-to-javascript.md)
</dt> </dl>

 

 




