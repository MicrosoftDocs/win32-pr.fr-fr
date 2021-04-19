---
description: Cette section décrit le format des enregistrements pour chacun des jetons d’enregistrement. Les informations sont réparties dans les sections suivantes.
ms.assetid: 4fdd8339-f660-4389-878a-e7ab067d8508
title: Enregistrements de jeton
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ae7e1dcdd36d538ed44205fa51b8e2094d1ff14
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/06/2021
ms.locfileid: "106514511"
---
# <a name="token-records"></a>Enregistrements de jeton

Cette section décrit le format des enregistrements pour chacun des jetons d’enregistrement. Les informations sont réparties dans les sections suivantes.

-   [nom du jeton \_](/windows)
-   [chaîne de jeton \_](/windows)
-   [entier de jeton \_](/windows)
-   [GUID du jeton \_](/windows)
-   [\_liste des entiers de jeton \_](/windows)
-   [\_liste flottante de jeton \_](/windows)

## <a name="token_name"></a>nom du jeton \_

Enregistrement de longueur variable. Le jeton est suivi d’une valeur de nombre qui spécifie le nombre d’octets qui suivent dans le champ nom. Un nom ASCII de longueur nombre termine l’enregistrement.



| Champ | Type       | Taille (en octets) | Contenu                       |
|-------|------------|--------------|--------------------------------|
| token | WORD       | 2            | nom du jeton \_                    |
| count | DWORD      | 4            | Longueur du champ de nom, en octets |
| name  | Tableau d’octets | count        | Nom ASCII                     |



 

## <a name="token_string"></a>chaîne de jeton \_

Enregistrement de longueur variable. Le jeton est suivi d’une valeur de nombre qui spécifie le nombre d’octets qui suivent dans le champ de chaîne. Une chaîne ASCII de nombre de longueurs continue l’enregistrement, qui est terminé par un jeton de fin. Le choix du terminateur est déterminé par des problèmes de syntaxe abordés ailleurs.



| Champ      | Type       | Taille (en octets) | Contenu                         |
|------------|------------|--------------|----------------------------------|
| token      | WORD       | 2            | chaîne de jeton \_                    |
| count      | DWORD      | 4            | Longueur du champ de chaîne en octets  |
| Chaîne     | Tableau d’octets | count        | Chaîne ASCII                     |
| terminateur | DWORD      | 4            | \_point-virgule ou \_ virgule de jeton |



 

## <a name="token_integer"></a>entier de jeton \_

Enregistrement de longueur fixe. Le jeton est suivi de la valeur entière requise.



| Champ | Type  | Taille (en octets) | Contenu       |
|-------|-------|--------------|----------------|
| token | WORD  | 2            | entier de jeton \_ |
| Ajoutée | DWORD | 4            | Entier unique |



 

## <a name="token_guid"></a>GUID du jeton \_

Enregistrement de longueur fixe. Le jeton est suivi des quatre champs de données tels qu’ils sont définis par la norme de l’ETCD OSF.



| Champ | Type       | Taille (en octets) | Contenu          |
|-------|------------|--------------|-------------------|
| token | WORD       | 2            | GUID du jeton \_       |
| Data1 | DWORD      | 4            | Champ de données UUID 1 |
| Data2 | WORD       | 2            | Champ de données UUID 2 |
| Data3 | WORD       | 2            | Champ de données UUID 3 |
| Data4 | Tableau d’octets | 8            | Champ de données UUID 4 |



 

## <a name="token_integer_list"></a>\_liste des entiers de jeton \_

Enregistrement de longueur variable. Le jeton est suivi d’une valeur de nombre qui spécifie le nombre d’entiers figurant dans le champ de liste. Pour des performances optimales, les listes d’entiers consécutives doivent être composées en une seule liste.



| Champ | Type  | Taille (en octets) | Contenu                         |
|-------|-------|--------------|----------------------------------|
| token | WORD  | 2            | \_liste des entiers de jeton \_             |
| count | DWORD | 4            | Nombre d’entiers dans le champ de liste |
| list  | DWORD | nombre de 4 x    | Liste d’entiers                     |



 

## <a name="token_float_list"></a>\_liste flottante de jeton \_

Enregistrement de longueur variable. Le jeton est suivi d’une valeur de nombre qui spécifie le nombre de valeurs float ou double qui suivent dans le champ de liste. La taille de la valeur à virgule flottante (float ou double) est déterminée par la valeur de float SizeSpecified dans l’en-tête de fichier. Pour des performances optimales, les listes de valeurs float de jeton consécutives \_ \_ doivent être composées en une seule liste.



| Champ | Type               | Taille (en octets)   | Contenu                                  |
|-------|--------------------|----------------|-------------------------------------------|
| token | WORD               | 2              | \_liste flottante de jeton \_                        |
| count | DWORD              | 4              | Nombre de valeurs float ou double dans le champ de liste |
| list  | float/double Array | nombre de 4 ou 8 x | Liste flottante ou double                      |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Encodage Binaire](binary-encoding.md)
</dt> </dl>

 

 
