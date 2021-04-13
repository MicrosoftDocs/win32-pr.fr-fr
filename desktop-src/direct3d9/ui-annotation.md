---
description: Utilisez cette annotation pour associer un paramètre d’effet à un contrôle d’interface utilisateur dans l’environnement hôte. Cela permet à un utilisateur de contrôler de manière interactive un paramètre d’effet par le biais de l’application hôte.
ms.assetid: 6d0b2450-7d90-4a24-b710-faed26969876
title: Annotation d’IU
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3e873c83a01c5c2214cb49a93e75167e58a3389
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482680"
---
# <a name="ui-annotation"></a>Annotation d’IU

Utilisez cette annotation pour associer un paramètre d’effet à un contrôle d’interface utilisateur dans l’environnement hôte. Cela permet à un utilisateur de contrôler de manière interactive un paramètre d’effet par le biais de l’application hôte.

DXSAS définit un ensemble de contrôles standard en termes de modèle de données et de comportement de base que les auteurs peuvent attendre des applications hôtes. L’annotation de contrôle est utilisée comme suit :


```
string SasUiControl = "ControlType";
```



where


```
ControlType
```



est l’un des éléments suivants :



|             |                                                                                                                                                                                 |                                                                                                    |                                                                                                              |
|-------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| ControlType | Description                                                                                                                                                                     | Type de données interne                                                                                 | Annotations de propriété de contrôle                                                                                 |
| Aucun        | Aucun contrôle ne doit être affiché. Notez qu’un contrôle est visible si [SasUiVisible](#sasuivisible) a la valeur true et que le type de contrôle est un type autre que None.                           | n/a                                                                                                | n/a                                                                                                          |
| Quelconque         | Cela implique qu’aucun contrôle spécial n’est demandé. Le contrôle présenté est le résultat d’un comportement défini par l’application.                                                         | n/a                                                                                                | n/a                                                                                                          |
| ColorPicker | Représente une valeur de couleur sous la forme d’un échantillon de couleur. La valeur est compressée dans les composants XYZ du vecteur associé. Le composant W du vecteur associé est toujours défini sur un. | float *n* , où *n* est compris entre 1 et 4.                                                            | [SasUiEnum](#sasuienum)                                                                                      |
| Sens   | Vecteur de direction.                                                                                                                                                             | float *n* , où *n* est compris entre 2 et 4.                                                            | Aucun                                                                                                         |
| FilePicker  | Boîte de dialogue qui permet à l’utilisateur de parcourir et de sélectionner un fichier.                                                                                                                  | string                                                                                             | Aucun                                                                                                         |
| ListPicker  | Liste de valeurs de chaîne à partir de laquelle l’utilisateur peut sélectionner une entrée. Les valeurs sont générées à partir de l’annotation [SasUiEnum](#sasuienum) .                                         | Tableau de chaînes avec une valeur entière contenant l’index de la valeur de chaîne sélectionnée. | [SasUiEnum](#sasuienum)                                                                                      |
| Numérique     | Ensemble de contrôles d’entrée numériques (tels que des zones de texte).                                                                                                                         | float *m* x *N* où *M* et *N* sont compris entre 1 et 4.                                               | [SasUiMin](#sasuimin), [SasUiMax](#sasuimax), [SasUiStride](#sasuistride)                                    |
| Curseur      | Ensemble de curseurs.                                                                                                                                                               | float *m* x *N* où *M* et *N* sont compris entre 1 et 4                                                | [SasUiMin](#sasuimin), [SasUiMax](#sasuimax), [SasUiSteps](#sasuisteps), [SasUiStepsPower](#sasuistepspower) |
| String      | Zone de texte pour modifier le contenu de la chaîne.                                                                                                                                         | string                                                                                             | Aucun                                                                                                         |



 

Si le type de données interne n’est pas identique au type du paramètre associé, la conversion se produit lorsque les données sont transférées du paramètre de l’application hôte vers le paramètre Effect.

La valeur par défaut est la chaîne « None ».

## <a name="ui-common-properties"></a>Propriétés communes de l’interface utilisateur

### <a name="sasuidescription"></a>SasUiDescription

Utilisez cette annotation pour spécifier une chaîne afin de décrire un outil. Cela peut être utilisé pour les éléments d’interface utilisateur tels que les info-bulles.


```
string SasUiDescription = "descriptive string";
```



Exemple :


```
float3 UpNormal
<
  string SasUiDescription = "The normalized up vector";
>;
```



La valeur par défaut est une chaîne vide.

### <a name="sasuilabel"></a>SasUiLabel

Utilisez cette annotation pour spécifier une chaîne pour étiqueter un contrôle d’interface utilisateur.


```
string SasUiLabel = "some label;
```



Voici un exemple :


```
float3 UpNormal
<
  string SasUiLabel = "Normal that points up.";
>;
```



La valeur par défaut est une chaîne vide.

### <a name="sasuivisible"></a>SasUiVisible

Utilisez cette annotation pour indiquer si le paramètre associé doit être affiché à l’utilisateur.


```
bool SasUiVisible = false;
```



Si la valeur est true, l’application hôte doit afficher un contrôle d’interface utilisateur pour la modification du paramètre d’effet annoté. Si la valeur est false, aucune interface utilisateur n’est affichée dans l’application hôte.

Voici un exemple :


```
float3 UpNormal
<
  string SasUiVisible = false;
>;
```



La valeur par défaut est True.

## <a name="ui-control-properties"></a>Propriétés de contrôle d’IU

Les annotations de propriété de contrôle sont des modificateurs supplémentaires qui permettent de déterminer la façon dont un contrôle particulier fonctionne.

### <a name="sasuienum"></a>SasUiEnum

Cette annotation vous permet de limiter la plage de valeurs d’un contrôle. L’annotation contient une chaîne de valeurs séparées par des virgules.

La valeur par défaut est une chaîne vide.

### <a name="sasuimax"></a>SasUiMax

Cette annotation spécifie la valeur maximale du paramètre associé. Elle ne peut être associée qu’à un paramètre de type numérique. La valeur maximale du paramètre sera calculée comme suit :


```
MaxValue = min(FLT_MAX, PARAMETER_TYPE_MAX);
```



Le \_ type \_ de paramètre Max est la valeur maximale pour le type utilisé par le paramètre associé. Cela signifie que la valeur du paramètre, prenant en compte l’annotation [SasUiMax](#sasuimax) , est calculée comme suit :


```
ParameterValue = min(NewParameterValue, MaxValue);
```



La valeur par défaut est FLT \_ Max comme défini dans Math. h.

### <a name="sasuimin"></a>SasUiMin

Cette annotation spécifie la valeur minimale du paramètre associé. Elle ne peut être associée qu’à un paramètre de type numérique. La valeur minimale du paramètre sera calculée comme suit :


```
MinValue = max(-FLT_MAX, PARAMETER_TYPE_MIN);
```



Le \_ type \_ de paramètre min est la valeur minimale pour le type utilisé par le paramètre associé. Cela signifie que la valeur du paramètre, prenant en compte l’annotation [SasUiMin](#sasuimin) , est calculée comme suit :


```
ParameterValue = max(NewParameterValue, MinValue);
```



La valeur par défaut est-FLT \_ Max, comme défini dans Math. h.

### <a name="sasuisteps"></a>SasUiSteps

Cette annotation spécifie le nombre d’étapes qui peuvent être utilisées lors de l’incrémentation ou de la décrémentation de la valeur de paramètre associée. L’annotation n’est significative que sur un paramètre de type numérique. La valeur zéro indique que l’application hôte choisira un nombre raisonnable d’étapes.

La valeur par défaut est 0.

### <a name="sasuistepspower"></a>SasUiStepsPower

Cette annotation spécifie l’exposant dans la fonction Power, qui a la plage \[ 0.0 f, 1.0 f \] . Les applications hôtes doivent implémenter la méthode suivante lors du calcul des valeurs de paramètre :


```
ParameterValue = ((SasUiMax - SasUiMin) x pow(UI_VALUE, SasUiStepsPower) + SasUiMin
```



La valeur par défaut est 1,0 f.

### <a name="sasuistride"></a>SasUiStride

Cette annotation spécifie l’incrément qui doit être utilisé lors de l’incrémentation ou de la décrémentation de cette valeur. Contrairement à [SasUiSteps](#sasuisteps), [SasUiStride](#sasuistride) est utile avec un contrôle Spinner, par exemple, où les données sont illimitées et l’utilisateur doit plutôt incrémenter la valeur de paramètre par Stride plutôt que par un nombre prédéfini d’étapes. Les applications hôtes doivent incrémenter (ou décrémenter selon le comportement du contrôle) la valeur de SasUiStride, comme suit :


```
ParameterValue = ParameterValue +/- SasUiStride
```



La valeur par défaut est 1,0 f.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Informations de référence sur les annotations et sémantiques DirectX standard](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



