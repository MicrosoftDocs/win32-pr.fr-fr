---
description: quand une application convertit des chaînes ASCII ou d’une page de codes Windows (ANSI) en unicode, elle doit convertir les séquences d’échappement caractère par caractère en unicode.
ms.assetid: 4be0fd47-0903-44d3-a323-0adc6e9c0cc9
title: Utilisation de séquences d’échappement et de caractères de contrôle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ea89997a8f94a9fdd573b2c8360dbdd5342d38ca8bd2e7a133aa29943c07e9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118389918"
---
# <a name="using-escape-sequences-and-control-characters"></a>Utilisation de séquences d’échappement et de caractères de contrôle

quand une application convertit des chaînes ASCII ou d’une [page de codes Windows (ANSI)](code-pages.md) en unicode, elle doit convertir les séquences d’échappement caractère par caractère en unicode. Lorsqu’un fichier texte ASCII ou d’un autre fichier texte 8 bits est converti en Unicode, il est possible qu’il soit reconverti par la suite. La conversion de séquences d’échappement en Unicode caractère par caractère, au lieu de les combiner comme un caractère Unicode unique, permet d’effectuer la conversion inverse sans avoir besoin de reconnaître et d’analyser les séquences d’échappement comme telles. Par exemple, ESC + A doit devenir 0x001B (ESC), 0x0041 (A), au lieu de 0x411B.

Les premières valeurs de code 32 16 bits en Unicode sont destinées aux caractères de contrôle 32. Cette spécification prend en charge l’utilisation existante de caractères de contrôle à des fins de mise en forme. Les applications Unicode peuvent traiter ces caractères de contrôle exactement de la même façon qu’ils traitent leurs équivalents ASCII.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de caractères spéciaux en Unicode](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



