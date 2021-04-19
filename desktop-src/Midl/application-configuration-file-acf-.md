---
title: Fichier de configuration de l’application (ACF)
description: Il peut y avoir des aspects de votre application distribuée qui affectent un composant, mais qui n’ont rien à faire avec un autre.
ms.assetid: 017d93fd-1701-4713-a786-752a7695b5a6
keywords:
- MIDL DE ACF
- Microsoft Interface Definition Language MIDL, décrit, fichier de configuration de l’application
- fichier de configuration de l’application MIDL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f9066e5641d6b71e68ba670984765661f1b9f6c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "106510222"
---
# <a name="application-configuration-file-acf"></a>Fichier de configuration de l’application (ACF)

Il peut y avoir des aspects de votre application distribuée qui affectent un composant, mais qui n’ont rien à faire avec un autre. Par exemple, un objet peut contenir une structure de données complexe de grande taille et passer le contenu de cette structure de données à un autre objet. La disposition exacte de cette structure de données peut ne pas avoir de sens pour l’application réceptrice. En outre, la structure peut contenir des types de données que le compilateur MIDL ne reconnaît pas et ne peut pas générer de code de marshaling et de démarshaling.

Les applications clientes peuvent partager la même interface, mais elles s’exécutent sur des plateformes différentes ; ils peuvent avoir besoin de leur propre ensemble de routines de marshaling. Enfin, les clients individuels n’ont pas forcément besoin du même ensemble de fonctions. Il est inefficace de générer du code stub pour les fonctions qui ne seront jamais implémentées dans une application cliente particulière.

En définissant ces aspects locaux de votre interface dans un fichier de configuration d’application (ACF), vous pouvez séparer les différences entre les interfaces client de leur représentation réseau, ce qui permet au serveur d’envoyer et de recevoir des données dans un format cohérent, et de rendre votre code stub plus compact et efficace.

La structure et la syntaxe d’une définition d’interface ACF sont identiques à la définition IDL :

``` syntax
[ interface-attribute-list] interface interface-name {. . .}
```

Par défaut, le nom de l’interface ACF doit correspondre à son nom dans la définition IDL. Toutefois, lorsque vous utilisez l’option/ [**ACF**](-acf.md) du compilateur MIDL pour spécifier explicitement un nom de fichier ACF, il n’est pas nécessaire que les noms d’interface correspondent. Cette fonctionnalité permet à plusieurs interfaces de partager une seule spécification ACF.

 

 




