---
description: Le compilateur MOF accepte une valeur à virgule flottante spécifiée pour une propriété à virgule flottante. La valeur est arrondie vers le haut ou vers le haut et stockée sous la forme d’un nombre à virgule flottante. Cette situation peut entraîner des résultats inattendus.
ms.assetid: 5cf7d8e1-c29d-4b9f-8557-e656c5e83370
ms.tgt_platform: multiple
title: Compilation de code MOF avec des valeurs Floating-Point
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 734639e1038b8e9739fead694740dbf5ab5f9cc7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127520233"
---
# <a name="compiling-mof-code-with-floating-point-values"></a>Compilation de code MOF avec des valeurs Floating-Point

Le compilateur MOF accepte une valeur à virgule flottante spécifiée pour une propriété à virgule flottante. La valeur est arrondie vers le haut ou vers le haut et stockée sous la forme d’un nombre à virgule flottante. Cette situation peut entraîner des résultats inattendus.

L’exemple de code MOF suivant définit une classe appelée **ABC** dans un espace de noms appelé « test ». Ce code MOF est compilé sans erreurs, mais vous ne pouvez pas interroger la valeur à virgule flottante définie pour la propriété **exampleUint16** dans l’instance créée par ce code.

``` syntax
#pragma namespace ("\\\\.\\Root")

instance of __Namespace
{
    Name = "Test";
};

#pragma namespace ("\\\\.\\Root\\test")

Class abc
{
        [KEY] String testID ;
        Uint16 exampleUint16;
        Real64 exampleReal64;
};

Instance of abc
{ 
        TestID ="exampleID";
        exampleUint16 = 1000.4;
};
```

Si vous exécutez la requête suivante, vous recevez un code d’erreur qui indique une requête non valide.


```sql
SELECT * FROM abc WHERE exampleUint16 = 1000.4
```



Toutefois, la requête suivante recherche l’instance indiquée.


```sql
SELECT * FROM abc WHERE exampleUint16 = 1000
```



## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Compilation des fichiers MOF](compiling-mof-files.md)
</dt> <dt>

[**mofcomp**](mofcomp.md)
</dt> <dt>

[Commandes de préprocesseur](preprocessor-commands.md)
</dt> </dl>

 

 



