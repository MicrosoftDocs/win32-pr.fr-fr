---
title: Structure XML du fichier de définition d’apparence
description: Structure XML du fichier de définition d’apparence
ms.assetid: 93325b94-667a-42a6-92f8-78288d36da81
keywords:
- création d’apparences, de fichiers de définition d’apparence
- apparences de Lecteur Windows Media, fichiers de définition d’apparence
- apparences, fichiers de définition d’apparence
- fichiers pour les apparences, définition d’apparence
- fichiers de définition d’apparence, structure XML
- Structure XML pour les fichiers de définition d’apparence
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbc3506ab03d3af7445e75983299577c713412fbeb0899d39c7098c55be2450a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118995249"
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

 

 




