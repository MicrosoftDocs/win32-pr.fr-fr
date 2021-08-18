---
title: Niveau de prise en charge du schéma
description: Cette section décrit en détail le niveau de prise en charge du schéma.
ms.assetid: ca18306e-6d67-406d-9c42-4be159a0b81f
keywords:
- Services Web de niveau de prise en charge de schéma pour Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d6cae112e074d50b90425c1d8952f3b6c06463378d73767346742193b406d2b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026280"
---
# <a name="schema-support-level"></a>Niveau de prise en charge du schéma

Cette section décrit en détail le niveau de prise en charge du schéma.


Le schéma prend directement en charge les éléments suivants :

-   Séquences d’éléments.
-   Dérivation des types d’éléments.
-   Choix simples d’éléments (ceux qui sont mappés à une Union avec balises).
-   Types de base définis par le format binaire XSD/.NET, y compris les plages (min/max).
-   Prise en charge simple de tout élément (aucune restriction sur le type d’élément).
-   Éléments et attributs facultatifs avec des valeurs par défaut.
-   Répétition d’éléments avec des plages (min/max).
-   Éléments nillable.

Le schéma ne prend pas en charge directement les éléments suivants (ce qui implique le comportement « de secours ») :

-   Types de base définis par l’utilisateur.
-   Choix plus compliqués.
-   Rejet des attributs inconnus.
-   Attributs inconnus d’un aller-retour.
-   Prise en charge plus complexe de tout élément.
-   Construction All.
-   Clé/keyref.

Voici une répartition détaillée de la prise en charge des différents composants de schéma. Il est comparé au contrat de données dans WCF, car la similarité des fonctionnalités. La différence est décrite.

En général, pour les comportements de secours :

-   les attributs sont retransmis à WS \_ String ;
-   le contenu de l’élément est stocké dans la \_ \_ mémoire tampon WS XML.
-   complexType sont représentées dans une structure contenant un champ de \_ tampon WS XML \_ .
-   Les types simples sont retransmis à WS \_ String.

Wsutil génère des avertissements pour les composants de schéma qui ne sont pas entièrement pris en charge. L’application devra peut-être effectuer une vérification supplémentaire pour que ces composants soient nécessaires. Les Wsutil d’heures supplémentaires peuvent être améliorées pour gérer certaines des fonctionnalités actuellement prises en charge dans l’exécution, comme la prise en charge de la valeur par défaut. Wsutil peut également être amélioré avec la sérialisation pour prendre en charge d’autres fonctionnalités telles que abstract. Le nombre de composants de schéma non pris en charge peut être réduit dans le temps.

## <a name="the-overall-schema-document"></a>Document de schéma global

Définition globale qui peut affecter les définitions incorporées dans le schéma. Il s’agit d’attributs globaux qui s’appliquent à toutes les définitions du schéma.

<XS : Schema> attributs

-   attributeFromDefault ignoré.
-   blockDefault ignoré.
-   elementFormDefault ignoré. Cela est différent de dataContract, car les éléments non qualifiés sont pris en charge dans le Runtime.
-   finalDefault ignoré. Il n’existe pas de prise en charge du langage C pour le concept final.
-   ID ignoré.
-   targetNamespace pris en charge et mappé à l’espace de noms du service.
-   version ignorée.

<XS : Schema> contents

-   include pris en charge ; Wsutil requiert que toutes les définitions nécessaires soient disponibles en tant que fichiers d’entrée au moment de la compilation.
-   redéfinition ignorée. Wsutil ne prend pas en charge cette.
-   importation prise en charge ; Wsutil requiert que toutes les définitions nécessaires soient disponibles en tant que fichiers d’entrée au moment de la compilation.
-   simpleType pris en charge-voir la section type simple ci-dessous.
-   complexType pris en charge-voir la section’complexType'
-   Groupe ignoré.
-   attributeGroup ignoré.
-   élément pris en charge ; correspond aux définitions d’éléments globaux.
-   attribut pris en charge ; correspond aux définitions d’attributs globaux.
-   Notation ignorée

## <a name="complex-type"></a>Type complexe

Le type complexe, représenté par <XS : complexType>, peut être la restriction d’un type simple ou d’un type complexe, d’une extension de type simple, de tableaux ou de structures. Nous avons remarqué que dans l’extension de types simples, il n’y a pas d’héritage et aucune prise en charge de xsi : type.

<XS : complexType> attributs

-   Résumé générer un avertissement sur les fonctionnalités non prises en charge, aucune modification de la génération de code.
-   bloquer générer un avertissement sur une fonctionnalité non prise en charge, aucune modification de la génération de code.
-   final générer un avertissement sur une fonctionnalité non prise en charge, aucune modification de la génération de code.
-   ID ignoré.
-   Générer un avertissement sur la fonctionnalité non prise en charge, revenir à la structure avec la \_ \_ mémoire tampon WS XML si la valeur est true.
-   nom pris en charge et mappé au nom du type de structure.

<XS : complexType> contenu

Il s’agit de la définition de type pour la structure. la restriction complexContent n’est pas prise en charge.

-   complexContent prend en charge l’extension de contenu complexe. Cartes de l’héritage de la structure.
-   Groupe de secours actuellement à la structure avec le \_ champ de tampon WS XML \_ . Peut être pris en charge en fonction de la particule sous-jacente.
-   choix pris en charge en tant qu’Union. Cela n’est pas pris en charge dans le contrat de données.
-   Sequence pris en charge : correspond aux champs d’une structure
-   attribut pris en charge avec une exception de « interdit ». secours à la structure avec \_ la \_ mémoire tampon XML WS si « interdit ».
-   attributeGroup pris en charge : correspond à la séquence d’attributs
-   anyAttribute ignoré
-   AttributeGroupRef pris en charge : correspond à la séquence d’attributs.
-   GroupRef est actuellement en train de revenir à la structure avec le \_ champ de tampon WS XML \_ . Peut être pris en charge selon le groupe sous-jacent.
-   Tout pris en charge, mappe à une \_ mémoire tampon XML
-   (vide) pris en charge, mappage à la description de struct vide sans struct généré.

<xs:sequence> dans un type complexe : contenu

Wsutil prend entièrement en charge la séquence de minOccurs = 1 et maxOccurs = 1 ; dans le cas contraire, le type complexe est actuellement transmis à la \_ \_ mémoire tampon WS XML. Il peut être pris en charge en tant que tableau de structures.

-   élément pris en charge ; chaque instance est mappée à un champ de la structure.
-   Groupe de secours ; le complexType est de secours à \_ la \_ mémoire tampon XML WS.
-   Tout secours ; le complexType est de secours à \_ la \_ mémoire tampon XML WS.
-   choix pris en charge ; mappage au champ d’Union.
-   séquence de secours ; le complexType est de secours à \_ la \_ mémoire tampon XML WS.
-   tout pris en charge ; mappé à la \_ mémoire tampon XML.
-   (vide) pris en charge ; complexType peut être une structure vide s’il n’y a pas d’attributs.

## <a name="elements"></a>Éléments

<XS : ELEMENT>peut se produire dans trois contextes.

-   Elle peut se produire dans un <XS : Sequence> décrivant un champ d’un struct normal. Dans ce cas, l’attribut maxOccurs doit avoir la 1. Le champ est facultatif si minOccurs a la valeur 0.
-   Elle peut se produire dans un <XS : Sequence> décrivant un champ d’un tableau. Dans ce cas, l’attribut maxOccurs doit être supérieur à 1 ou non lié.
-   Elle peut se produire dans un <XS : Schema> comme une description globale de l’élément.

<XS : ELEMENT> dans un <XS : Sequence> ou <XS : Choice> en tant que champ dans une structure

-   Prise en charge de la référence ; résolu en référence à un élément global.
-   nom pris en charge, mappe au nom du champ.
-   type pris en charge, mappe au type de champ. Pour plus d’informations, consultez « mappage de type ». S’il n’est pas spécifié (et que l’élément ne contient pas de type anonyme), XS : anyType est utilisé par défaut.
-   bloquer générer un avertissement sur une fonctionnalité non prise en charge, aucune modification de la génération de code.
-   par défaut, générer un avertissement sur une fonctionnalité non prise en charge, aucune modification de la génération de code.
-   correction de la génération d’un avertissement sur une fonctionnalité non prise en charge, aucune modification de la génération de code.
-   formulaire ignoré. Notre couche de sérialisation prend en charge les formulaires qualifiés et non qualifiés.
-   ID ignoré.
-   maxOccurs est mappé à un champ de données unique si est égal à 1. elle est mappée à un champ de tableau (élément répétitif) si maxOccurs est supérieur à 1.
-   minOccurs si la valeur est 0, le champ options est défini sur champ \_ facultatif, si la valeur nillable n’est pas définie.
-   nillable le champ est nillable. Pour plus d’informations, consultez [sérialisation](serialization.md) .

<XS : ELEMENT> en tant qu’élément global : attributs

les attributs minOccurs et maxOccurs ne sont pas valides en tant que Description d’élément global. L’application peut utiliser directement la description de l’élément généré dans la couche de sérialisation ou les couches de canal.

-   Résumé générer un avertissement sur les fonctionnalités non prises en charge, aucune modification de la génération de code.
-   bloquer générer un avertissement sur une fonctionnalité non prise en charge, aucune modification de la génération de code.
-   par défaut, générer un avertissement sur une fonctionnalité non prise en charge, aucune modification de la génération de code.
-   final générer un avertissement sur une fonctionnalité non prise en charge, aucune modification de la génération de code.
-   correction de la génération d’un avertissement sur une fonctionnalité non prise en charge, aucune modification de la génération de code.
-   ID ignoré.
-   nom pris en charge : mappez le nom de la description de l’élément global et il s’agit de la base du type anonyme lorsqu’il est spécifié.
-   nillable ignoré-l’application doit appeler avec l’indicateur Right.
-   l’ensemble de la solution de secours à la structure avec la \_ mémoire tampon XML WS est \_ définie. Wsutil ne prend pas en charge substitutionGroup.
-   tapez pris en charge et mappez au type de l’élément.

<XS : ELEMENT> en tant qu’élément global : contenu

-   simpleType pris en charge ; correspond à la définition de type.
-   complexType pris en charge ; correspond à un type complexe.
-   génération unique avertissement sur la fonctionnalité non prise en charge, aucune modification de la génération de code. Wsutil ne prend pas en charge les contraintes d’élément.
-   clé générer un avertissement sur une fonctionnalité non prise en charge, aucune modification de la génération de code. Wsutil ne prend pas en charge les contraintes d’élément.
-   keyref générer un avertissement sur une fonctionnalité non prise en charge, aucune modification de la génération de code. Wsutil ne prend pas en charge les contraintes d’élément.
-   Occult Géré l’élément sans spécification de type est traité comme XS : anyType.

## <a name="simple-types"></a>Types simples

<XS : simpleType> attributs

-   Final générer un avertissement sur une fonctionnalité non prise en charge, aucune modification de la génération de code.
-   ID ignoré
-   Nom pris en charge, mappe au nom de type.

<XS : simpleType> contenu

-   Restriction prise en charge, mappe au type ou à la plage d’énumération. Consultez la section « restrictions XS : simpleType ».
-   Liste générer un avertissement sur les fonctionnalités non prises en charge, de secours à la \_ mémoire tampon XML.
-   L’Union génère un avertissement sur la fonctionnalité non prise en charge, de secours à la \_ mémoire tampon XML.

## <a name="simple-type-restriction"></a>Restriction de type simple

Certaines facettes sont autorisées dans des types intégraux et des chaînes pour permettre la prise en charge de Range et d’enum.

prise en charge de l’énumération

<XS : Enumeration> restriction de type simple pour le type de base de String est traitée comme un type enum. Dans ce cas, l’attribut de base doit être de type chaîne. Dans le cas d’énumération, toutes les autres facettes sont ignorées.

plage sur la prise en charge de type simple

Certaines facettes sont prises en charge dans les types simples. elles prennent en charge efficacement la plage autorisée sur le type. Les éléments suivants sont des restrictions pour les types intégraux et les types float/double. Les types simples avec d’autres facettes sont représentées dans le \_ type de chaîne WS

-   minExclusive pris en charge
-   minInclusive pris en charge
-   maxExclusive pris en charge
-   maxInclusive pris en charge
-   totalDigits générer un avertissement sur les fonctionnalités non prises en charge, aucune modification de la génération de code.
-   fractionDigits générer un avertissement sur une fonctionnalité non prise en charge, aucune modification de la génération de code.
-   longueur générer un avertissement sur une fonctionnalité non prise en charge, aucune modification de la génération de code.
-   minLength générer un avertissement sur la fonctionnalité non prise en charge, aucune modification de la génération de code.
-   maxLength génère un avertissement sur les fonctionnalités non prises en charge, aucune modification de la génération de code.
-   l’énumération génère un avertissement sur les fonctionnalités non prises en charge, aucune modification de la génération de code.
-   whiteSpace générer un avertissement sur une fonctionnalité non prise en charge, aucune modification de la génération de code.
-   modèle générer un avertissement sur les fonctionnalités non prises en charge, aucune modification de la génération de code.
-   Occult Géré.

les fonctions minLength et maxLength sur String ne sont pas prises en charge actuellement, mais cette fonctionnalité est souhaitable pour la prise en charge.

## <a name="inheritance"></a>Héritage

Wsutil prend en charge l’héritage de types complexes, autrement dit, une structure peut hériter d’une autre structure, similaire à l’héritage d’interface en C++. Pour ce faire, <> XS : complexContentExtension. <XS : simpleContentExtension> est pris en charge, mais est généré en tant que structure simple avec le type de base comme premier champ au lieu de l’héritage de type.

## <a name="typeprimitive-mapping"></a>Mappage de type/primitif

Les identificateurs doivent être normalisés lors de la traduction à partir de NCName en XML. Les chaînes sont null ; les types de pointeur sont nillable ; les types intégraux et float/double sont nillable et defaultValue prend la valeur 0.

![Tableau présentant le mappage entre les types XSD et les types de données saphir.](images/schematypemap.png)

 

 




