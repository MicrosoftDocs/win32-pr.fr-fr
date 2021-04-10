---
title: À propos des types de données .NET Framework
description: À propos des types de données .NET Framework
ms.assetid: 8683888b-889f-4ab2-8eab-dbb79735f13f
keywords:
- Lecteur Windows Media,. NET Framework
- Windows Media Player Object Model, .NET Framework
- modèle objet, .NET Framework
- Windows Media Player Mobile, .NET Framework
- Contrôle ActiveX du lecteur Windows Media, .NET Framework
- Contrôle ActiveX mobile du lecteur Windows Media, .NET Framework
- Contrôle ActiveX, .NET Framework
- .NET Framework, types de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c8774f4ee4521628a05bf766c50c8c7609c1107
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029710"
---
# <a name="about-net-framework-data-types"></a>À propos des types de données .NET Framework

Cette section contient les informations dont vous avez besoin pour traduire la référence du modèle objet orienté script en types de données de base Microsoft .NET Framework. La référence du script du lecteur Windows Media a presque toutes les informations dont vous avez besoin pour utiliser le contrôle du lecteur Windows Media dans un programme .NET Framework. dans la plupart des cas, la syntaxe sera similaire à celle des autres langages de script tels que Microsoft JScript.

La référence du lecteur Windows Media fournit le type de données JScript et, si nécessaire, la conversion C++. Par exemple, un **nombre** peut être retourné par une méthode. JScript traite tous les nombres de la même manière, mais d’autres langages distinguent les différents types de nombres (entier, virgule flottante, etc.). La référence fournit la conversion C++ pour les types de données numériques, car les nombres peuvent être traités différemment par C++. Par exemple, C++ utilise le type de données **int** pour les opérations arithmétiques sur les entiers et **float** pour la virgule flottante.

Le .NET Framework utilise un système de types de données de base légèrement différent. Le tableau suivant présente les différences entre les types de données courants que vous êtes susceptible d’utiliser. Pour plus d’informations sur les types de données de base .NET Framework et la conversion vers d’autres systèmes de type de données, consultez le Guide du développeur .NET Framework présentation des types de données de base de l’espace de noms System.

Ce tableau indique le nom de la classe .NET Framework et le type de données C#. Les types de données pour d’autres langages sont définis pour chaque langue dans leurs références de langue respectives.



| Type de données de script | Type de données C++     | .NET Framework, classe (type de données C#) |
|------------------|-------------------|---------------------------------------|
| **Nombre**       | **int**           | **Int32** (**entier**)                   |
| **Nombre**       | **long**          | **Int32** (**entier**)                   |
| **Nombre**       | **double**        | **Double** (**double**)               |
| **Nombre**       | **float**         | **Single** (**float**)                |
| **Chaîne**       | **BSTR**          | **Chaîne** (**String**)               |
| **Booléen**      | **VARIANT \_ booléen** | **Boolean** (**booléen**)                |
| **Object**       | **Object**        | **Object** (**objet**)               |



 

Si vous utilisez Visual Studio, vous pouvez utiliser la technologie Microsoft IntelliSense pour déterminer le type de données attendu pour une fonction spécifique.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**Intégration du contrôle du lecteur Windows Media dans une solution .NET Framework**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> <dt>

[**Référence du modèle objet pour l’écriture de scripts**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




