---
description: Le compilateur format MOF (MOF) prend en charge deux styles de commentaires à l’aide de deux styles différents de délimiteurs de commentaire.
ms.assetid: 5ab71b45-7ed1-44c4-8710-6b833b0afb80
ms.tgt_platform: multiple
title: Création d’un commentaire
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 870833f1dbb86f53c7114c4e376af2b4882906ffe1b8cc10f5876bd2c80492e3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120097339"
---
# <a name="creating-a-comment"></a>Création d’un commentaire

Le compilateur format MOF (MOF) prend en charge deux styles de commentaires à l’aide de deux styles différents de délimiteurs de commentaire.

Le tableau suivant répertorie les délimiteurs utilisés pour les commentaires et l’effet que les délimiteurs ont dans le code.



| Délimiteur   | Marques                                                                                         |
|-------------|-----------------------------------------------------------------------------------------------|
| //          | Début d’un commentaire qui se termine à la fin de la ligne.                                    |
| /\* les \*/ | Début et fin d’un commentaire qui peut s’étendre sur plusieurs lignes ou s’étendre uniquement sur une partie d’une ligne. |



 

Comme dans les langages de programmation C et C++, vous devez utiliser le délimiteur//avec des commentaires sur une seule ligne, mais vous pouvez utiliser les \* \* délimiteurs/et/avec des commentaires sur une ou plusieurs lignes.

L’exemple de code suivant décrit les deux styles de délimiteur.

``` syntax
int32 MyProp = 2; // This is a comment until the line ends.
int32 /* This is a comment. */ MyProp = 2;
```

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Conception de classes format MOF (MOF)](designing-managed-object-format--mof--classes.md)
</dt> </dl>

 

 



