---
description: Une entrée de contrôle d’accès conditionnel (ACE) permet l’évaluation d’une condition d’accès lors de l’exécution d’une vérification d’accès. Le langage SDDL (Security Descriptor Definition Language) fournit la syntaxe permettant de définir des ACE conditionnelles dans un format de chaîne.
ms.assetid: cdc3629d-c4d8-4910-8838-3bdb601f7064
title: Langage de définition du descripteur de sécurité pour les ACE conditionnelles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f65cb6ae0588ae197c84d3b13362721cc3e98b43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527015"
---
# <a name="security-descriptor-definition-language-for-conditional-aces"></a>Langage de définition du descripteur de sécurité pour les ACE conditionnelles

Une [*entrée de contrôle d’accès*](/windows/desktop/SecGloss/a-gly) conditionnel (ACE) permet l’évaluation d’une condition d’accès lors de l’exécution d’une vérification d’accès. Le langage SDDL (Security Descriptor Definition Language) fournit la syntaxe permettant de définir des ACE conditionnelles dans un format de chaîne.

Le SDDL pour une entrée du contrôle d’accès conditionnel est le même que pour n’importe quelle entrée du contrôle d’accès, avec la syntaxe de l’instruction conditionnelle ajoutée à la fin de la chaîne ACE. Pour plus d’informations sur SDDL, consultez [langage de définition du descripteur de sécurité](security-descriptor-definition-language.md).

Le \# signe « » est synonyme de «0 » dans les attributs de ressource. Par exemple, D :AI (XA ; OICI ; FA ;;; WD ; (OctetStringType = = \# 1 \# 2 \# 3 \# \# )) est équivalent à et interprété comme D :ai (XA ; oici ; FA ;;; WD ; (OctetStringType = = \# 01020300)).

-   [Format de chaîne ACE conditionnel](#conditional-ace-string-format)
-   [Expressions conditionnelles](#conditional-expressions)
-   [Attributs](#attributes)
-   [Opérateurs](#operators)
-   [Priorité des opérateurs](#operator-precedence)
-   [Valeurs inconnues](#unknown-values)
-   [Évaluation d’entrée de contrôle d’accès conditionnelle](#conditional-ace-evaluation)
-   [Exemples](#examples)
-   [Rubriques connexes](#related-topics)

## <a name="conditional-ace-string-format"></a>Format de chaîne ACE conditionnel

Chaque entrée du contrôle d’accès dans une chaîne de [*descripteur de sécurité*](/windows/desktop/SecGloss/s-gly) est mise entre parenthèses. Les champs de l’entrée du contrôle d’accès sont dans l’ordre suivant et sont séparés par des points-virgules (;).

*AceType ***;** _AceFlags_* _;_ *_Droits_*_;_ *_ObjectGuid_*_;_ *_InheritObjectGuid_*_;_ *_AccountSid_*_;(_*_ConditionalExpression_*_)_*

Les champs sont décrits dans [chaînes ACE](ace-strings.md), avec les exceptions suivantes.

-   Le champ *AceType* peut être l’une des chaînes suivantes.

    | Chaîne de type ACE | Constante dans SDDL. h                         | Valeur AceType                                   |
    |-----------------|--------------------------------------------|-------------------------------------------------|
    | XA<br/> | \_ \_ accès au rappel SDDL \_ autorisé<br/> | \_type d' \_ entrée du rappel autorisé \_ pour l’accès \_<br/> |
    | VERROUILLAGE<br/> | \_ \_ accès au rappel SDDL \_ refusé<br/>  | \_type d' \_ ACE de rappel de refus d’accès \_ \_<br/>  |

    

     

-   La chaîne ACE comprend une ou plusieurs expressions conditionnelles, placées entre parenthèses à la fin de la chaîne.

## <a name="conditional-expressions"></a>Expressions conditionnelles

Une expression conditionnelle peut inclure l’un des éléments suivants.



| Élément d'expression                                                | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *AttributeName*<br/>                                        | Teste si l’attribut spécifié a une valeur différente de zéro.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| **existe** *AttributeName*<br/>                             | Teste si l’attribut spécifié existe dans le contexte client.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| *Valeur* de l' *opérateur* *AttributeName*<br/>                     | Retourne le résultat de l’opération spécifiée.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| * ConditionalExpression * **\|\|** _ConditionalExpression_<br/> | Teste si l’une des expressions conditionnelles spécifiées a la valeur true.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| *ConditionalExpression* **&&** *ConditionalExpression*<br/> | Teste si les deux expressions conditionnelles spécifiées ont la valeur true.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| **! (**_ConditionalExpression_*_)_*<br/>                     | Inverse d’une expression conditionnelle.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| **Membre \_ de {**_SidArray_*_}_*<br/>                         | Teste si le SID et le tableau d' [**\_ \_ attributs**](/windows/desktop/api/Winnt/ns-winnt-sid_and_attributes) du contexte client contient tous les [identificateurs de sécurité](security-identifiers.md) (SID) de la liste séparée par des virgules spécifiée par *SidArray*.<br/> Pour les ACE Allow, le SID du contexte client doit avoir le jeu d’attributs **\_ \_ Enabled Group** pour être considéré comme une correspondance.<br/> Pour les ACE de refus, un SID de contexte client doit avoir le **groupe de se \_ \_ activé** ou le **\_ groupe \_ de se utilisé pour l’attribut \_ de \_ refus \_ uniquement** défini pour être considéré comme une correspondance.<br/> Le tableau *SidArray* peut contenir soit des chaînes sid (par exemple, « S-1-5-6 »), soit des alias sid (par exemple, « BA »).<br/> |



 

## <a name="attributes"></a>Attributs

Un attribut représente un élément dans le tableau d' [**\_ informations des \_ attributs \_ de sécurité authnt**](/windows/desktop/api/Authz/ns-authz-authz_security_attributes_information) dans le contexte client. Un nom d’attribut peut contenir des caractères alphanumériques et les caractères «  : », « / », « . » et « \_ ».

Une valeur d’attribut peut être de l’un des types suivants.



| Type de valeur         | Description                                                                                                                                                                                         |
|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Integer<br/> | Entier 64 bits en notation décimale ou hexadécimale.<br/>                                                                                                                              |
| String<br/>  | Valeur de chaîne délimitée par des guillemets.<br/>                                                                                                                                                      |
| SID<br/>     | SID (S-1-1-0) ou SID (BA). Doit se trouver sur le RHS du membre \_ de ou de l’appareil \_ membre \_ de.<br/>                                                                                                           |
| BLOB<br/>    | \# suivi de nombres hexadécimaux. Si la longueur des nombres est impaire, le \# est converti en 0 pour le faire même. En outre \# , un autre emplacement dans la valeur est traduit en 0.<br/> |



 

## <a name="operators"></a>Opérateurs

Les opérateurs suivants sont définis pour une utilisation dans les expressions conditionnelles pour tester les valeurs des attributs. Il s’agit d’opérateurs binaires et utilisés dans la forme *valeur* de l' *opérateur* *AttributeName* .



| Opérateur            | Description                                                                                                              |
|---------------------|--------------------------------------------------------------------------------------------------------------------------|
| ==<br/>       | Définition conventionnelle.<br/>                                                                                      |
| !=<br/>       | Définition conventionnelle.<br/>                                                                                      |
| <<br/>     | Définition conventionnelle.<br/>                                                                                      |
| <=<br/>    | Définition conventionnelle.<br/>                                                                                      |
| ><br/>     | Définition conventionnelle.<br/>                                                                                      |
| >=<br/>    | Définition conventionnelle.<br/>                                                                                      |
| Contient<br/> | **True** si la valeur de l’attribut spécifié est un sur-ensemble de la valeur spécifiée ; Sinon, **false**.<br/>  |
| L’un \_ des<br/>  | **True** si la valeur spécifiée est un sur-ensemble de la valeur de l’attribut spécifié ; Sinon, **false**. <br/> |



 

En outre, les opérateurs unaires existent, les membres \_ et les négations ( !) sont définis comme décrit dans le tableau des expressions conditionnelles.

L’opérateur « Contains » doit être précédé et suivi d’un espace blanc, et l’opérateur « ANY \_ of » doit être précédé d’un espace blanc.

## <a name="operator-precedence"></a>Priorité des opérateurs

Les opérateurs sont évalués dans l’ordre de priorité suivant, avec des opérations de priorité égale en cours d’évaluation de gauche à droite.

1.  Exists, membre \_ de
2.  Contains, \_ any
3.  = =, ! =, <, <=, >, >=
4.  !
5.  &&
6.  \|\|

En outre, toute partie d’une expression conditionnelle peut être placée entre parenthèses. Les expressions entre parenthèses sont évaluées en premier.

## <a name="unknown-values"></a>Valeurs inconnues

Les résultats des expressions conditionnelles renvoient parfois la valeur **Unknown**. Par exemple, l’une des opérations relationnelles retourne **Unknown** lorsque l’attribut spécifié n’existe pas.

Le tableau suivant décrit les résultats d’une opération **and** logique entre deux expressions conditionnelles, *ConditionalExpression1* et *ConditionalExpression2*.



| *ConditionalExpression1* | *ConditionalExpression2* | *ConditionalExpression1* **&&** *ConditionalExpression2* |
|--------------------------|--------------------------|----------------------------------------------------------|
| **TRUE**<br/>      | **TRUE**<br/>      | **TRUE**<br/>                                      |
| **TRUE**<br/>      | **FALSE**<br/>     | **FALSE**<br/>                                     |
| **TRUE**<br/>      | **UNKNOWN**<br/>   | **UNKNOWN**<br/>                                   |
| **FALSE**<br/>     | **TRUE**<br/>      | **FALSE**<br/>                                     |
| **FALSE**<br/>     | **FALSE**<br/>     | **FALSE**<br/>                                     |
| **FALSE**<br/>     | **UNKNOWN**<br/>   | **FALSE**<br/>                                     |
| **UNKNOWN**<br/>   | **TRUE**<br/>      | **UNKNOWN**<br/>                                   |
| **UNKNOWN**<br/>   | **FALSE**<br/>     | **FALSE**<br/>                                     |
| **UNKNOWN**<br/>   | **UNKNOWN**<br/>   | **UNKNOWN**<br/>                                   |



 

Le tableau suivant décrit les résultats d’une opération **or** logique entre deux expressions conditionnelles, *ConditionalExpression1* et *ConditionalExpression2*.



| *ConditionalExpression1* | *ConditionalExpression2* | *ConditionalExpression1* **\|\|** *ConditionalExpression2* |
|--------------------------|--------------------------|------------------------------------------------------------|
| **TRUE**<br/>      | **TRUE**<br/>      | **TRUE**<br/>                                        |
| **TRUE**<br/>      | **FALSE**<br/>     | **TRUE**<br/>                                        |
| **TRUE**<br/>      | **UNKNOWN**<br/>   | **TRUE**<br/>                                        |
| **FALSE**<br/>     | **TRUE**<br/>      | **TRUE**<br/>                                        |
| **FALSE**<br/>     | **FALSE**<br/>     | **FALSE**<br/>                                       |
| **FALSE**<br/>     | **UNKNOWN**<br/>   | **UNKNOWN**<br/>                                     |
| **UNKNOWN**<br/>   | **TRUE**<br/>      | **TRUE**<br/>                                        |
| **UNKNOWN**<br/>   | **FALSE**<br/>     | **UNKNOWN**<br/>                                     |
| **UNKNOWN**<br/>   | **UNKNOWN**<br/>   | **UNKNOWN**<br/>                                     |



 

La négation d’une expression conditionnelle avec une valeur **Unknown** est également **inconnue**.

## <a name="conditional-ace-evaluation"></a>Évaluation d’entrée de contrôle d’accès conditionnelle

Le tableau suivant décrit le résultat de la vérification d’accès d’une entrée du contrôle d’accès conditionnel en fonction de l’évaluation finale de l’expression conditionnelle.

| Type d’entrée de contrôle d’accès         | TRUE             | FALSE                 | UNKNOWN               |
|------------------|------------------|-----------------------|-----------------------|
| Autoriser<br/> | Autoriser<br/> | Ignorer l’ACE<br/> | Ignorer l’ACE<br/> |
| Deny<br/>  | Deny<br/>  | Ignorer l’ACE<br/> | Deny<br/>       |



 

## <a name="examples"></a>Exemples

Les exemples suivants montrent comment les stratégies d’accès spécifiées sont représentées par une entrée de contrôle d’accès conditionnel définie à l’aide du langage SDDL.

<dl> <dt>

<span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Renvoi
</dt> <dd>

Autoriser l’exécution à tout le monde si les deux conditions suivantes sont remplies :

-   Titre = PM
-   Division = finance ou division = ventes

</dd> <dt>

<span id="SDDL"></span><span id="sddl"></span>SDDL
</dt> <dd>

D : (XA ;; FX ;;; S-1-1-0 ; ( @User.Title = = "PM"  &&  ( @User.Division = = "finance" \| \| @User.Division = = "Sales")))

</dd> <dt>

 
</dt> <dd>

 

</dd> <dt>

<span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Renvoi
</dt> <dd>

Autorisez l’exécution si l’un des projets de l’utilisateur s’entrecoupent avec les projets de fichier s.

</dd> <dt>

<span id="SDDL"></span><span id="sddl"></span>SDDL
</dt> <dd>

D : (XA ;; FX ;;; S-1-1-0 ; ( @User.Project Tout \_ @Resource.Project ))

</dd> <dt>

 
</dt> <dd>

 

</dd> <dt>

<span id="Policy"></span><span id="policy"></span><span id="POLICY"></span>Renvoi
</dt> <dd>

Autoriser l’accès en lecture si l’utilisateur s’est connecté avec une carte à puce, est un opérateur de sauvegarde et se connecte à partir d’un ordinateur sur lequel BitLocker est activé.

</dd> <dt>

<span id="SDDL"></span><span id="sddl"></span>SDDL
</dt> <dd>

D : (XA ;; FR ;;; S-1-1-0 ; (Membre \_ de {sid (SID de carte à puce \_ ), sid (BO)}  && @Device.Bitlocker ))

</dd> <dt>

 
</dt> <dd>

 

</dd> </dl>

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[\[MS-DTYP \] : langage de description du descripteur de sécurité](/openspecs/windows_protocols/ms-dtyp/4f4251cc-23b6-44b6-93ba-69688422cb06)
</dt> </dl>

