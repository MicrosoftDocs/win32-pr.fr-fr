---
description: Un identificateur de langue est une abréviation numérique internationale standard pour la langue d’un pays ou d’une région géographique.
ms.assetid: 076e2a43-256a-4646-a5c8-1d48ab08ce1a
title: Identificateurs de langue
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6245101099b5df5c192af60a977ede88412f95cca8afda9270b7aba6e1c41ad2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120106979"
---
# <a name="language-identifiers"></a>Identificateurs de langue

Un identificateur de langue est une abréviation numérique internationale standard pour la [langue](locales-and-languages.md) d’un pays ou d’une région géographique. Chaque langue possède un identificateur de langue unique (LANGID de type de données), une valeur de 16 bits qui se compose d’un identificateur de langue primaire et d’un identificateur de sous-langue. Pour plus d’informations sur les identificateurs de langue, consultez [constantes et chaînes d’identificateur de langue](language-identifier-constants-and-strings.md).

Un identificateur de langue est construit à l’aide de la macro [**MAKELANGID**](/windows/desktop/api/Winnt/nf-winnt-makelangid) . L’illustration suivante montre le format des bits dans un identificateur de langue.

``` syntax
+-------------------------+-------------------------+
|     SubLanguage ID      |   Primary Language ID   |
+-------------------------+-------------------------+
15                    10  9                         0   bit
```

Les identificateurs de langue prédéfinis sont les suivants :

-   langue \_ par défaut du système lang \_ . Langue par défaut du système d’exploitation.
-   langue \_ par défaut de l’utilisateur lang \_ . La langue de l’utilisateur actuel.

votre application peut récupérer les identificateurs de langue en cours à l’aide des fonctions [interface utilisateur multilingue](multilingual-user-interface.md) .

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Paramètres régionaux et langues](locales-and-languages.md)
</dt> <dt>

[Constantes et chaînes de l’identificateur de langue](language-identifier-constants-and-strings.md)
</dt> <dt>

[Interface utilisateur multilingue](multilingual-user-interface.md)
</dt> <dt>

[**MAKELANGID**](/windows/desktop/api/Winnt/nf-winnt-makelangid)
</dt> </dl>

 

 



