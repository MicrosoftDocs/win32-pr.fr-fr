---
description: Utilisez cette annotation pour définir le contenu d’un fichier externe comme valeur d’initialisation d’un paramètre d’effet.
ms.assetid: 3da1f951-cb8b-49ce-aba2-0badb3178093
title: Annotation d’initialisation de paramètre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c564b5b5e273b320fdc5de6148ef5ba5dd9f1b78
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126918224"
---
# <a name="parameter-initialization-annotation"></a>Annotation d’initialisation de paramètre

Utilisez cette annotation pour définir le contenu d’un fichier externe comme valeur d’initialisation d’un paramètre d’effet. Par exemple :


```
string SasResourceAddress = "Value";
```



où la valeur est une chaîne de texte ASCII qui peut contenir un chemin d’accès absolu ou relatif. Un chemin d’accès relatif est relatif au répertoire qui contient le fichier d’effet.

Voici un exemple :


```
texture2D DetailTexture
<
    string SasResourceAddress = "noise.dds";
>;
```



La valeur par défaut est une chaîne vide.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Informations de référence sur les annotations et sémantiques DirectX standard](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



