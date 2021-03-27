---
title: Warning (directive pragma)
description: Directive pragma qui modifie le comportement des messages d’avertissement du compilateur.
ms.assetid: 69488014-36e3-4c87-8b65-6123b5e87bcb
keywords:
- Warning (directive de pragma) HLSL
topic_type:
- apiref
api_name:
- warning pragma Directive
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7599886b47830b33c69f11c0c341c7775c644dd3
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 10/25/2019
ms.locfileid: "103940446"
---
# <a name="warning-pragma-directive"></a>Warning (directive pragma)

Directive pragma qui modifie le comportement des messages d’avertissement du compilateur.



| \#pragma warning ( *Warning-specifier* : *Warning-Number-List* \[ ; *Warning-specifier* : *Warning-Number-List*... \] ) |
|----------------------------------------------------------------------------------------------------------------------|



 

## <a name="parameters"></a>Paramètres



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Élément</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="warning-specifier"></span><span id="WARNING-SPECIFIER"></span><em>Warning-specifier</em><br/></td>
<td>Comportement à définir pour les avertissements spécifiés. Ce paramètre peut prendre l’une des valeurs indiquées dans le tableau suivant. <br/> 
<table>
<thead>
<tr class="header">
<th>Valeur</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>once</td>
<td>Affiche le message des avertissements avec les nombres spécifiés une seule fois.</td>
</tr>
<tr class="even">
<td>default</td>
<td>Rétablit la valeur par défaut du comportement des avertissements avec les nombres spécifiés. Cela a également pour effet d’activer un avertissement sur qui est désactivé par défaut. L’avertissement est généré à son niveau par défaut.</td>
</tr>
<tr class="odd">
<td>1, 2, 3, 4</td>
<td>Applique le niveau spécifié aux avertissements avec les nombres spécifiés. Cela a également pour effet d’activer un avertissement sur qui est désactivé par défaut.</td>
</tr>
<tr class="even">
<td>disable</td>
<td>N’émettez pas les avertissements avec les nombres spécifiés.</td>
</tr>
<tr class="odd">
<td>erreur</td>
<td>Signalez les avertissements avec les nombres spécifiés en tant qu’erreurs.</td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><p><span id="warning-number-list"></span><span id="WARNING-NUMBER-LIST"></span><em>AVERTISSEMENT : nombre-liste</em></p></td>
<td><p>Liste délimitée par des espaces blancs des numéros des avertissements pour modifier le comportement de.</p></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Notes

Vous pouvez spécifier n’importe quel nombre de changements de comportement d’avertissement distincts dans le même pragma d’avertissement en séparant les modifications par des points-virgules.

Le compilateur ajoute 4000 à tout numéro d’avertissement compris entre 0 et 999. Pour les numéros d’avertissement supérieurs à 4699, (ceux associés à la génération de code), le pragma d’avertissement n’a d’effet que lorsqu’il est placé en dehors des définitions de fonction. Le pragma est ignoré s’il spécifie un nombre supérieur à 4699 et est utilisé à l’intérieur d’une fonction.

Le pragma warning Warning ne prend pas en charge les fonctionnalités **Push** et **pop** du pragma warning inclus dans le compilateur C++.

## <a name="examples"></a>Exemples

L’exemple suivant désactive les avertissements 4507 et 4034, affiche l’avertissement 4385 une fois, et signale l’avertissement 4164 comme une erreur.


```
#pragma warning( disable : 4507 34; once : 4385; error : 164 )
```



L’exemple précédent est fonctionnellement équivalent à ce qui suit :


```
#pragma warning( disable : 4507 34 )
#pragma warning( once : 4385 )
#pragma warning( error : 164 )
```



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Directives de préprocesseur (DirectX HLSL)](dx-graphics-hlsl-appendix-preprocessor.md)
</dt> <dt>

[\#Directive pragma (DirectX HLSL)](dx-graphics-hlsl-appendix-pre-pragma.md)
</dt> </dl>

 

 





