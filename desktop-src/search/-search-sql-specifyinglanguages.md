---
description: Vous pouvez spécifier la langue utilisée dans les requêtes de recherche.
ms.assetid: 3a7ecf8f-38ae-41d1-be70-e9ab23977a01
title: Spécification des langues
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e50b3f65a41670989d41e235831ec8c008a6d8cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525479"
---
# <a name="specifying-languages"></a>Spécification des langues

Vous pouvez spécifier la langue utilisée dans les requêtes de recherche. Les prédicats FREETEXT et CONTAINs de la clause WHERE prennent en charge la spécification d’une langue. Vous pouvez indiquer le langage de requête en fournissant un identificateur de code de langue numérique (LCID) dans le prédicat CONTAINs ou FREETEXT. Ce LCID spécifie l’analyseur lexical à utiliser pour analyser la chaîne de requête. Il utilise la syntaxe suivante :


```
CONTAINS | FREETEXT
([<column_identifier>,]'<content_search_condition>' [,LCID]) 
```



Pour plus d’informations, consultez la syntaxe des prédicats [Contains](-search-sql-contains.md) et [FREETEXT](-search-sql-freetext.md) .

 

 



