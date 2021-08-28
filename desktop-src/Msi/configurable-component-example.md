---
description: Cet exemple permet au consommateur de module de configurer indépendamment un contrôle d’édition, l’attribut checksum et l’attribut Compressed.
ms.assetid: f0500856-18d0-45e5-992a-57e01fb2cca5
title: Exemple de composant configurable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9ff3e1567a19afd50a0ae2035893c027398816b535d5edfb233e89021ea9e59
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500739"
---
# <a name="configurable-component-example"></a>Exemple de composant configurable

Dans cet exemple, les tables ModuleConfiguration et ModuleSubstitution suivantes permettent au consommateur de module de configurer indépendamment l’attribut de mot de passe pour un contrôle d’édition, l’attribut de somme de contrôle pour un fichier et l’attribut compressé pour le même fichier.

[Table ModuleSubstitution](modulesubstitution-table.md)



| Table   | Ligne           | Colonne     | Valeur                        |
|---------|---------------|------------|------------------------------|
| Contrôler | Dialog1; Edit1 | Attributs | \[= Mot de passe\]                |
| Fichier    | Fichier1         | Attributs | \[= Checksum \] \[ = Compressed\] |



 

[Table ModuleConfiguration](moduleconfiguration-table.md)



| Name       | Format   | Type | ContextData                              | DefaultValue | Attributs | DisplayName | Description |
|------------|----------|------|------------------------------------------|--------------|------------|-------------|-------------|
| Mot de passe   | Champ |      | 2097152 ; True = 2097152 ; False = 0             | 0            | 0          |             |             |
| Somme de contrôle   | Champ |      | 1024 ; Somme de contrôle = 1024 ; Aucune somme de contrôle = 0         | 0            | 0          |             |             |
| Compressé | Champ |      | 24576 ; Compressed = 16384 ; Non compressé = 8192 | 8 192         | 0          |             |             |



 

 

 



