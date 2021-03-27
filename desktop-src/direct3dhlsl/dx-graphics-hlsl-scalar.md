---
title: Types scalaires
description: Types scalaires
ms.assetid: bf24d27f-2720-4268-bc74-fc46afedb9aa
keywords:
- Types scalaires HLSL
topic_type:
- apiref
api_name:
- Scalar Types
api_type:
- NA
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/29/2020
ms.openlocfilehash: 7198932c6edb91e6f797b232b6c980976f3696a7
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/10/2021
ms.locfileid: "103761894"
---
# <a name="scalar-types"></a>Types scalaires


Le langage HLSL prend en charge plusieurs types de données scalaires :

-   **bool** -true ou false.
-   entier signé **int** -32 bits.
-   **uint** -entier non signé 32 bits.
-   entier non signé **dword** 32 bits.
-   valeur à virgule flottante **demi** -16 bits. Ce type de données est fourni uniquement pour la compatibilité de langage. Les cibles de nuanceur Direct3D 10 mappent tous les deux types de données aux types de données float. Un type demi-données ne peut pas être utilisé sur une variable globale uniforme (utilisez l’indicateur/GEC si cette fonctionnalité est souhaitée).
-   valeur à virgule flottante 32 bits **float** .
-   valeur à virgule flottante **double** 64 bits. Vous ne pouvez pas utiliser des valeurs à double précision comme entrées et sorties pour un flux. Pour passer des valeurs à double précision entre les nuanceurs, déclarez chaque **double** comme une paire de types de données **uint** . Utilisez ensuite la fonction [**asuint**](asuint.md) pour compresser chaque **double** dans la paire **uint** s et la fonction [**AsDouble**](asdouble.md) pour décompresser la paire de **uint** s dans le **double**.

À compter de Windows 8 HLSL, il prend également en charge les types de données scalaires de précision minimale. Les pilotes graphiques peuvent implémenter des types de données scalaires de précision minimale à l’aide d’une précision supérieure ou égale à la précision de bit spécifiée. Nous vous recommandons de ne pas compter sur le comportement de verrouillage ou d’habillage qui dépend de la précision sous-jacente spécifique. Par exemple, le pilote Graphics peut exécuter une opération arithmétique sur une valeur **min16float** à la précision 32 bits.

-   **min16float** -valeur à virgule flottante 16 bits minimale.
-   **min10float** -valeur à virgule flottante 10 bits minimale.
-   **min16int** -entier signé 16 bits minimal.
-   **min12int** -entier signé 12 bits minimum.
-   **min16uint** -entier non signé 16 bits minimal.

Pour plus d’informations sur les littéraux scalaires, consultez [grammaire](dx-graphics-hlsl-appendix-grammar.md).



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td>Différences entre Direct3D 9 et Direct3D 10 :<br/> Dans Direct3D 10, les types suivants sont des modificateurs du type float.<br/>
<ul>
<li><strong>monoronfler</strong> - Signée IEEE 32 bits-valeur float normalisée dans la plage comprise entre-1 et 1.</li>
<li><strong>unorm float</strong> - Unsigned-bit non signé IEEE 32 dans la plage comprise entre 0 et 1 inclus.</li>
</ul>
Par exemple, voici une déclaration de variable float-normalized-normalized à 4 composants.<br/> <span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<tbody>
<tr class="odd">
<td><pre><code>snorm float4 fourComponentIEEEFloat;</code></pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
</tbody>
</table>



 

## <a name="string-type"></a>Type de chaîne

Le langage HLSL prend également en charge un type **chaîne** , qui est une chaîne ASCII. Il n’y a pas d’opérations ou d’États acceptant des chaînes, mais les effets peuvent interroger des paramètres de chaîne et des annotations.

## <a name="example"></a>Exemple

```c
// top-level variable
float globalShaderVariable; 

// top-level function
void function(
in float4 position: POSITION0 // top-level argument
              )
{
  float localShaderVariable; // local variable
  function2(...)
}

void function2()
{
  ...
}
```

## <a name="see-also"></a>Voir aussi



* [Déclaration de types scalaires](./dx-graphics-hlsl-writing-shaders-9.md#declaring-shader-variables)
* [Types de données (DirectX HLSL)](dx-graphics-hlsl-data-types.md)