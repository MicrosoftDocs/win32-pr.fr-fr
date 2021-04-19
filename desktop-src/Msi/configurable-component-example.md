---
description: Cet exemple permet au consommateur de module de configurer indépendamment un contrôle d’édition, l’attribut checksum et l’attribut Compressed.
ms.assetid: f0500856-18d0-45e5-992a-57e01fb2cca5
title: Exemple de composant configurable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 971b2a7c442acb96d7ba00a444c8c3a038c339f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106533759"
---
# <a name="configurable-component-example"></a>Exemple de composant configurable

Dans cet exemple, les tables ModuleConfiguration et ModuleSubstitution suivantes permettent au consommateur de module de configurer indépendamment l’attribut de mot de passe pour un contrôle d’édition, l’attribut de somme de contrôle pour un fichier et l’attribut compressé pour le même fichier.

[Table ModuleSubstitution](modulesubstitution-table.md)



| Table de charge de travail   | Ligne           | Colonne     | Valeur                        |
|---------|---------------|------------|------------------------------|
| Contrôler | Dialog1; Edit1 | Attributs | \[= Mot de passe\]                |
| Fichier    | Fichier1         | Attributs | \[= Checksum \] \[ = Compressed\] |



 

[Table ModuleConfiguration](moduleconfiguration-table.md)



| Nom       | Format   | Type | ContextData                              | DefaultValue | Attributs | DisplayName | Description |
|------------|----------|------|------------------------------------------|--------------|------------|-------------|-------------|
| Mot de passe   | Champ |      | 2097152 ; True = 2097152 ; False = 0             | 0            | 0          |             |             |
| Somme de contrôle   | Champ |      | 1024 ; Somme de contrôle = 1024 ; Aucune somme de contrôle = 0         | 0            | 0          |             |             |
| Compressé | Champ |      | 24576 ; Compressed = 16384 ; Non compressé = 8192 | 8 192         | 0          |             |             |



 

 

 



