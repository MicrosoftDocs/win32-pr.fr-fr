---
description: Quand une application convertit des chaînes ASCII ou d’une page de codes Windows (ANSI) en Unicode, elle doit convertir les séquences d’échappement caractère par caractère en Unicode.
ms.assetid: 4be0fd47-0903-44d3-a323-0adc6e9c0cc9
title: Utilisation de séquences d’échappement et de caractères de contrôle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4211a487a31d5a79454d7be15159f48cdc3d5beb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106531415"
---
# <a name="using-escape-sequences-and-control-characters"></a>Utilisation de séquences d’échappement et de caractères de contrôle

Quand une application convertit des chaînes ASCII ou d’une [page de codes Windows (ANSI)](code-pages.md) en Unicode, elle doit convertir les séquences d’échappement caractère par caractère en Unicode. Lorsqu’un fichier texte ASCII ou d’un autre fichier texte 8 bits est converti en Unicode, il est possible qu’il soit reconverti par la suite. La conversion de séquences d’échappement en Unicode caractère par caractère, au lieu de les combiner comme un caractère Unicode unique, permet d’effectuer la conversion inverse sans avoir besoin de reconnaître et d’analyser les séquences d’échappement comme telles. Par exemple, ESC + A doit devenir 0x001B (ESC), 0x0041 (A), au lieu de 0x411B.

Les premières valeurs de code 32 16 bits en Unicode sont destinées aux caractères de contrôle 32. Cette spécification prend en charge l’utilisation existante de caractères de contrôle à des fins de mise en forme. Les applications Unicode peuvent traiter ces caractères de contrôle exactement de la même façon qu’ils traitent leurs équivalents ASCII.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation de caractères spéciaux en Unicode](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



