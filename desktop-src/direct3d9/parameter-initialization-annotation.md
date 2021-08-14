---
description: Utilisez cette annotation pour définir le contenu d’un fichier externe comme valeur d’initialisation d’un paramètre d’effet.
ms.assetid: 3da1f951-cb8b-49ce-aba2-0badb3178093
title: Annotation d’initialisation de paramètre
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2d66d0cc18782d97a5a56c73ab12cd9222d33827930d60023fccf73cd2a8455
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118798659"
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

 

 



