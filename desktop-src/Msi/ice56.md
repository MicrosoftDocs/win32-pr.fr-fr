---
description: ICE56 vérifie que la structure de répertoires du fichier .msi possède un répertoire racine unique, que la racine est la propriété TARGETDIR et que la valeur de la propriété SourceDir se trouve dans la colonne DefaultDir de la table Directory.
ms.assetid: 6fbb51ff-64fc-40b7-852f-490c93e592c0
title: ICE56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70c1feb3e3dbab84a58809496b28a60d3a2436c3041d3a2d58f0ac8f2b5e47a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119528219"
---
# <a name="ice56"></a>ICE56

ICE56 vérifie que la structure de répertoires du fichier .msi possède un répertoire racine unique, que la racine est la propriété [**targetDir**](targetdir.md) et que la valeur de la propriété [**SourceDir**](sourcedir.md) se trouve dans la colonne DefaultDir de la [table Directory](directory-table.md).

Si un fichier de .msi a plusieurs racines ou spécifie une racine autre que [**targetDir**](targetdir.md), une [installation administrative](administrative-installation.md) ne crée pas d’image administrative correcte.

Notez que les répertoires vides ne sont pas vérifiés par ICE56. La structure de répertoires est validée avec plusieurs répertoires racine si les répertoires supplémentaires sont vides.

## <a name="result"></a>Résultat

ICE56 publie une erreur si la .msi n’a pas de racine unique, [**targetDir**](targetdir.md)ou si [**SourceDir**](sourcedir.md) n’est pas spécifié dans la colonne DefaultDir de la [table de répertoires](directory-table.md).

## <a name="example"></a>Exemples

ICE56 signale les erreurs suivantes pour l’exemple indiqué.

``` syntax
Directory 'TARGETDIR' has a bad DefaultDir value. 
Directory 'Root2' is an invalid root Directory.
```

[Table de répertoire](directory-table.md)



| Répertoire | Répertoire \_ parent | DefaultDir |
|-----------|-------------------|------------|
| TARGETDIR |                   | Temp       |
| ROOT2     | ROOT2             | SourceDir  |



 

Pour corriger la première erreur, la racine [**targetDir**](targetdir.md) doit avoir une valeur DefaultDir de [**SourceDir**](sourcedir.md). SOURCEDIR est également accepté. Il peut être possible de faire de **targetDir** le parent de la deuxième racine et d’utiliser la valeur'. 'dans la colonne DefaultDir. Pour plus d’informations, consultez la [table Directory](directory-table.md) .

Pour corriger la deuxième erreur, la structure de répertoire ne doit avoir qu’une seule racine appelée [**targetDir**](targetdir.md).

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Référence ICE](ice-reference.md)
</dt> </dl>

 

 



