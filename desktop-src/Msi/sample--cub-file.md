---
description: 'Cet exemple illustre la disposition d’un fichier. CUB contenant deux CIEM. Le programme d’installation exécute les actions personnalisées dans la séquence : ICE01 et ICE08.'
ms.assetid: 609cd16a-4421-4082-855d-229f5ba7117b
title: Exemple de fichier. CUB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e937b779e2a620ffc17cf936e37f74867f3dfdd4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127021259"
---
# <a name="sample-cub-file"></a>Exemple de fichier. CUB

Cet exemple illustre la disposition d’un fichier. CUB contenant deux [CIEM](internal-consistency-evaluators-ices.md). Le programme d’installation exécute les actions personnalisées dans la séquence : ICE01 et ICE08.

L’action personnalisée ICE01 est un [type d’action personnalisé 1](custom-action-type-1.md). Il s’agit d’un point d’entrée d’une DLL stockée en tant que flux dans le fichier. CUB. Ce flux est listé dans la ice.dll table binaire.

L’action personnalisée ICE08 est un [type d’action personnalisé 6](custom-action-type-6.md). Il s’agit d’un point d’entrée d’une fonction dans VBScript qui est stockée sous forme de flux dans le fichier. CUB. Ce flux est listé dans la table binaire comme ice.vbs.

[Table binaire](binary-table.md)



| Nom    | Données                               |
|---------|------------------------------------|
| ice.vbs | Données binaires non mises en forme de ice.vbs |
| ice.dll | Données binaires non mises en forme de ice.dll |



 

[Table CustomAction](customaction-table.md)



| Action | Type | Source  | Cible |
|--------|------|---------|--------|
| ICE01  | 1    | ice.dll | ICE01  |
| ICE08  | 6    | ice.vbs | ICE02  |



 

\_Table ICESequence



| Action | Condition | Séquence |
|--------|-----------|----------|
| ICE01  |           | 10       |
| ICE08  |           | 20       |



 

\_Table spéciale

ICE01 et ICE08 ne nécessitent pas l’inclusion de tables de traitement spéciales. Quand le fichier. CUB contient des tables spéciales, elles doivent également être incluses dans le \_ tableau de validation.

[\_Tableau de validation](-validation-table.md)



| Table de charge de travail         | Colonne    | Nullable | MinValue | MaxValue | Keytable | KeyColumn | Category                         | Définissez | Description |
|---------------|-----------|----------|----------|----------|----------|-----------|----------------------------------|-----|-------------|
| Binary        | Nom      | N        |          |          |          |           | [Identificateur](identifier.md)     |     |             |
| Binary        | Données      | N        |          |          |          |           | [Binaire](binary.md)             |     |             |
| CustomAction  | Action    | N        |          |          |          |           | [Identificateur](identifier.md)     |     |             |
| CustomAction  | Type      | N        |          |          |          |           | [Integer](integer.md)           |     |             |
| CustomAction  | Source    | O        |          |          |          |           | [CustomSource](customsource.md) |     |             |
| CustomAction  | Cible    | O        |          |          |          |           | [Correct](formatted.md)       |     |             |
| \_ICESequence | Action    | N        |          |          |          |           | [Identificateur](identifier.md)     |     |             |
| \_ICESequence | Condition | O        |          |          |          |           | [Condition](condition.md)       |     |             |
| \_ICESequence | Séquence  | O        |          |          |          |           | [Integer](integer.md)           |     |             |



 

 

 



