---
title: à propos des Types de données .NET Framework
description: à propos des Types de données .NET Framework
ms.assetid: 8683888b-889f-4ab2-8eab-dbb79735f13f
keywords:
- Lecteur Windows Media, .NET Framework
- Lecteur Windows Media modèle objet, .NET Framework
- modèle objet, .NET Framework
- Lecteur Windows Media Mobile, .NET Framework
- Lecteur Windows Media contrôle ActiveX, .NET Framework
- Lecteur Windows Media contrôle de ActiveX Mobile, .NET Framework
- contrôle ActiveX, .NET Framework
- .NET Framework, types de données
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36854d971b0fc220f8f77b754b08b486ff93d339935bedcf33edca39fb701e4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004517"
---
# <a name="about-net-framework-data-types"></a>à propos des Types de données .NET Framework

cette section contient les informations dont vous avez besoin pour traduire la référence du modèle objet orienté script en types de données de base Microsoft .NET Framework. la référence de script Lecteur Windows Media a presque toutes les informations dont vous avez besoin pour utiliser le contrôle Lecteur Windows Media dans un programme basé sur .NET Framework. dans la plupart des cas, la syntaxe sera similaire à celle des autres langages de script tels que Microsoft JScript.

la référence Lecteur Windows Media fournit le type de données JScript et, si nécessaire, la conversion C++. Par exemple, un **nombre** peut être retourné par une méthode. JScript traite tous les nombres de la même manière, mais d’autres langues distinguent les différents types de nombres (entier, virgule flottante, etc.). La référence fournit la conversion C++ pour les types de données numériques, car les nombres peuvent être traités différemment par C++. Par exemple, C++ utilise le type de données **int** pour les opérations arithmétiques sur les entiers et **float** pour la virgule flottante.

le .NET Framework utilise un système de types de données de base légèrement différent. Le tableau suivant présente les différences entre les types de données courants que vous êtes susceptible d’utiliser. pour plus d’informations sur les types de données de base .NET Framework et la conversion vers d’autres systèmes de type de données, consultez le Guide du développeur .NET Framework présentation des types de données de base de l’espace de noms System.

ce tableau indique le nom de la classe .NET Framework et le type de données C#. Les types de données pour d’autres langages sont définis pour chaque langue dans leurs références de langue respectives.



| Type de données de script | Type de données C++     | .NET Framework, classe (type de données C#) |
|------------------|-------------------|---------------------------------------|
| **Nombre**       | **int**           | **Int32** (**entier**)                   |
| **Nombre**       | **long**          | **Int32** (**entier**)                   |
| **Nombre**       | **double**        | **Double** (**double**)               |
| **Nombre**       | **float**         | **Single** (**float**)                |
| **Chaîne**       | **BSTR**          | **Chaîne** (**String**)               |
| **Booléen**      | **VARIANT \_ booléen** | **Boolean** (**booléen**)                |
| **Object**       | **Object**        | **Object** (**objet**)               |



 

si vous utilisez Visual Studio, vous pouvez utiliser la technologie Microsoft IntelliSense pour déterminer le type de données attendu pour une fonction spécifique.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[**incorporation du contrôle Lecteur Windows Media dans une Solution .NET Framework**](using-the-windows-media-player-control-in-a--net-framework-solution.md)
</dt> <dt>

[**Référence du modèle objet pour l’écriture de scripts**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




