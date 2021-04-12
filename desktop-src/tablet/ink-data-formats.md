---
description: 'Il existe un certain nombre de formats dans lesquels les données d’encre peuvent être stockées, notamment :'
ms.assetid: b08fba71-46cb-4419-9da5-a33a5b9a5ec0
title: Formats de données manuscrites
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7ccd0ab298e183867a9c4f8018727f22e51e7bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318105"
---
# <a name="ink-data-formats"></a>Formats de données manuscrites

Il existe un certain nombre de formats dans lesquels les données d’encre peuvent être stockées, notamment :

-   ISF (Ink Serialized Format)
-   HTML
-   RTF (Rich Text Format)
-   Format binaire
-   Formats basés sur des Extensible Markup Language (XML)

Différents formats s’appliquent dans différentes circonstances. Pour interagir avec le presse-papiers avec succès, les applications doivent être en mesure de reconnaître et de générer autant de formats que possible.

Les formats les plus importants et les plus simples qui peuvent être utilisés pour stocker l’encre sont le format ISF (Ink Serialized Format). ISF offre une représentation compacte, mais complète, d’un seul objet [**Ink**](inkdisp-class.md) .

Le format HTML est tout aussi important. Les données manuscrites peuvent être représentées en HTML de telle façon qu’elles peuvent être affichées en tant qu’image par les applications qui ne reconnaissent pas l’encre. En outre, la fidélité totale de l’encre est maintenue. Pour ces raisons, et parce qu’il s’agit d’un format couramment compris qui permet la représentation de nombreux types de contenu différents, Microsoft recommande le format HTML pour le partage de l’encre.

Il est également possible de stocker de l’encre dans d’autres formats. En utilisant le format RTF, vous pouvez coller l’encre dans des applications qui ne reconnaissent pas l’encre, telles que Microsoft Word 2002. Pour ce faire, incorporez des objets OLE qui contiennent de l’encre dans le RTF. D’autres formats, tels que des formats binaires ou XML, peuvent être utilisés.

Les formats que vous choisissez pour une application particulière pour copier, coller ou sérialiser de l’encre doivent reposer sur les besoins et ressources spécifiques des applications. Au minimum, une application doit être en mesure de copier et coller des applications ISF, ce qui permet le plus bas niveau d’interopérabilité de l’encre. ISF et la possibilité de copier et coller des éléments ISF sont intégrés à la plateforme Tablet PC. Toutefois, de nombreuses applications doivent représenter du contenu plus complexe, par exemple une sélection contenant plusieurs objets Ink ou du texte mis en forme. Dans ce cas, une application peut copier et coller du code HTML. Cela offre une flexibilité maximale. Le format HTML est largement compréhensible et facile à générer. Enfin, les applications qui produisent déjà du RTF ou ont un besoin important de communiquer avec des applications plus anciennes doivent également produire un format RTF.

> [!Note]  
> Tout au long de la discussion sur l’interopérabilité de l’encre, bitmap, ISF et GIF sont des formats d’image. L’objet d’encre de texte (tInk) et l’objet d’encrage d’esquisse (sInk) sont des objets OLE. Binary, HTML, XML et RTF sont des formats de document dans lesquels les images sont consommées.

 

La plateforme Tablet PC fournit des API pour vous aider à générer et interpréter ces formats. Il existe de nombreuses options qui, ensemble, doivent correspondre aux besoins d’interopérabilité et de persistance de toute application. Pour plus d’informations sur les formats d’encre, consultez [formats de persistance](persistence-formats.md).

 

 



