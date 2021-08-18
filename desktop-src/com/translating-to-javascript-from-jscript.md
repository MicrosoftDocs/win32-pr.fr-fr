---
title: Conversion en JavaScript à partir de JScript
description: Conversion en JavaScript à partir de JScript
ms.assetid: 11d31c8c-868d-4220-9298-6d24a209dc47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49c4adb5827952cc9bab0dac268997b5b73a52ecd1403e5431cdb3939b08c7e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129581"
---
# <a name="translating-to-javascript-from-jscript"></a>Conversion en JavaScript à partir de JScript

JScript est en grande partie compatible avec JavaScript. toutefois, JScript comprend certains objets qui ne sont actuellement pas pris en charge par JavaScript, tels que ActiveXObject, Enumerator, Error, Global et VBArray.

la version 5,0 de JScript prend en charge la gestion des exceptions via **try**... instructions **catch** . JavaScript ne fournit pas actuellement de mécanisme de gestion des erreurs.

lors de l’utilisation de JScript ou de JavaScript, il existe quelques différences subtiles entre les implémentations de modèle objet prises en charge par différents navigateurs Web. Pour écrire un script qui s’exécute à la fois sur Internet Explorer et Netscape Navigator, limitez les fonctionnalités utilisées par vos scripts à celles spécifiées dans la norme World Wide Web Consortium (W3C) [pour HTML version 3,2](https://www.w3.org/tr/rec-html32.html).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Conversion en JavaScript](translating-to-javascript.md)
</dt> </dl>

 

 




