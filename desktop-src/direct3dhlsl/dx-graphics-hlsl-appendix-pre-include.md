---
title: " include (directive)"
description: Directive de préprocesseur qui insère le contenu du fichier spécifié dans le programme source à l’emplacement où la directive apparaît.
ms.assetid: 24796d89-5690-469b-950e-df56783aa05a
keywords:
- include, directive HLSL
topic_type:
- apiref
api_name:
- include Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 66df429785a9fb90d2de8c89d23792c1754e2fde8eeb4770912e65a41a622c3a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119855039"
---
# <a name="include-directive"></a>\#include (directive)

Directive de préprocesseur qui insère le contenu du fichier spécifié dans le programme source à l’emplacement où la directive apparaît.


| \#inclure «*nom de fichier*»       |
|------------------------------|
| \#inclure le *nom de fichier* <> |

## <a name="parameters"></a>Paramètres

| Élément | Description |
|------|-------------|
| *extension* | Nom du fichier à inclure, éventuellement précédé d’une spécification de répertoire. Le nom de fichier doit spécifier un fichier existant. |

## <a name="remarks"></a>Remarques

La \# directive include provoque le remplacement de la directive par le contenu entier du fichier spécifié. Le préprocesseur arrête de Rechercher dès qu’il trouve un fichier avec le nom spécifié ; Si vous spécifiez une spécification de chemin d’accès complète et non ambiguë pour le fichier, le préprocesseur recherche uniquement le chemin d’accès spécifié.

> [!NOTE]
> L' [outil Effect-compiler](/windows/desktop/direct3dtools/fxc) est doté d’un gestionnaire d’inclusion intégré utilisant le commutateur/i. Toutefois, lors de l’exécution du compilateur à partir de l’API, vous pouvez fournir un gestionnaire include personnalisé en implémentant l’interface ID3DXInclude.

La différence entre les deux formes de syntaxe est l’ordre dans lequel le préprocesseur recherche les fichiers d’en-tête lorsque le chemin d’accès est spécifié de manière incomplète, comme indiqué dans le tableau suivant.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Forme syntaxique</th>
<th>Modèle de recherche de préprocesseur</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>#inclure le <b>&quot;</b> <em>nom de fichier</em><b>&quot;</b></td>
<td>Recherche le fichier include :
<ol>
<li>dans le même répertoire que le fichier qui contient la directive #include.</li>
<li>dans les répertoires de tous les fichiers qui contiennent une directive #include pour le fichier qui contient la directive #include.</li>
<li>dans les chemins d’accès spécifiés par l’option du compilateur/I, dans l’ordre dans lequel ils sont répertoriés.</li>
<li><p>dans les chemins d’accès spécifiés par la variable d’environnement INCLUDe, dans l’ordre dans lequel ils sont répertoriés.</p>
<blockquote>
[!NOTE]<br />
La variable d’environnement INCLUDe est ignorée dans un environnement de développement. Reportez-vous à la documentation de votre environnement de développement pour plus d’informations sur la façon de définir les chemins d’accès include pour votre projet.
</blockquote>
<p><br/></p></li>
</ol></td>
</tr>
<tr class="even">
<td>#inclure le <b><</b> <em>nom de fichier</em><b>></b></td>
<td>Recherche le fichier include :
<ol>
<li>dans les chemins d’accès spécifiés par l’option du compilateur/I, dans l’ordre dans lequel ils sont répertoriés.</li>
<li><p>dans les chemins d’accès spécifiés par la variable d’environnement INCLUDe, dans l’ordre dans lequel ils sont répertoriés.</p>
<blockquote>
[!NOTE]<br />
La variable d’environnement INCLUDe est ignorée dans un environnement de développement. Reportez-vous à la documentation de votre environnement de développement pour plus d’informations sur la façon de définir les chemins d’accès include pour votre projet.
</blockquote>
<p><br/></p></li>
</ol></td>
</tr>
</tbody>
</table>

## <a name="examples"></a>Exemples

L’exemple suivant fait en sorte que le préprocesseur remplace la \# directive include par le contenu de stdio. h. Étant donné que l’exemple utilise le format Chevron, le préprocesseur recherche le fichier uniquement dans les répertoires listés par l’option de compilateur/I et la variable d’environnement INCLUDe.

```cpp
#include <stdio.h>
```

## <a name="see-also"></a>Voir aussi

- [Directives de préprocesseur (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)

- [Interface ID3D10Include](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))

- [Effect-Tool du compilateur](/windows/desktop/direct3dtools/fxc)