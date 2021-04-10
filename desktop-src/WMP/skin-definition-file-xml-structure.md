---
title: Structure XML du fichier de définition d’apparence
description: Structure XML du fichier de définition d’apparence
ms.assetid: 93325b94-667a-42a6-92f8-78288d36da81
keywords:
- création d’apparences, de fichiers de définition d’apparence
- Apparences du lecteur Windows Media, fichiers de définition d’apparence
- apparences, fichiers de définition d’apparence
- fichiers pour les apparences, définition d’apparence
- fichiers de définition d’apparence, structure XML
- Structure XML pour les fichiers de définition d’apparence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8508f1a458930bc2b60d564a45ef08a9f9f5a9d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029476"
---
# <a name="skin-definition-file-xml-structure"></a>Structure XML du fichier de définition d’apparence

Le fichier de définition d’apparence est écrit en XML. L’une des fonctionnalités importantes de XML est qu’elle est entièrement structurée et est similaire à un plan. Le code XML est simplement une série d’éléments tels que **View** et **BUTTONGROUP**. Vous allez commencer par les éléments, puis les définir avec des attributs. Le reste de ce didacticiel vous donne des détails sur les attributs, mais voici le contour des éléments qui seront utilisés :


```C++
<THEME>
    <VIEW>
        <BUTTONGROUP>
            <BUTTONELEMENT/>
            <BUTTONELEMENT/>
        </BUTTONGROUP>
    </VIEW>
<THEME>

```



En gardant à l’esprit la structure simple des éléments, vous pouvez avoir un sens des attributs qui rendent chaque élément unique. Les détails de chaque élément seront traités dans les rubriques restantes de cette section. Pour plus d’informations sur les éléments et les attributs, consultez la référence sur la programmation de l' [apparence](skin-programming-reference.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Création du fichier de définition d’apparence**](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




