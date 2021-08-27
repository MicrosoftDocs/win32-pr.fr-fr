---
description: paramètres régionaux \_ ILANGUAGE
ms.assetid: 8f80a941-8ba6-4a0d-92fa-77230fe0a9d1
title: LOCALE_ILANGUAGE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3159fe26ce1af7291c5990a07297e7513144b5187b55c00086bf46e452ef188c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120106649"
---
# <a name="locale_ilanguage"></a>paramètres régionaux \_ ILANGUAGE

[Identificateur de langue](language-identifiers.md) avec une valeur hexadécimale. Par exemple, l’anglais (États-Unis) a la valeur 0409, qui indique 0x0409 hexadécimal, et est équivalent à 1033 décimal. Le nombre maximal de caractères autorisés pour cette chaîne est de cinq, y compris un caractère null de fin.

**Windows Vista et versions ultérieures :** L’utilisation de cette constante peut entraîner le renvoi d’un identificateur de paramètres régionaux non valides par [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) . Votre application doit utiliser la constante [locale \_ sName](locale-sname.md) lors de l’appel de cette fonction.

 

 



