---
description: HKLM \\ Software \\ Microsoft \\ SQMClient \\ Windows \\ CEIPEnable.
ms.assetid: 68ba8219-7ed2-44a9-9fd5-f6dfa57891c0
title: CEIPEnable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef7b86a726af95e7ec9fb764d5e752057a24b3e0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104200961"
---
# <a name="ceipenable"></a>CEIPEnable

**HKLM \\ Software \\ Microsoft \\ SQMClient \\ Windows \\ CEIPEnable**



| Type de données  | Plage                     | Valeur par défaut |
|------------|---------------------------|---------------|
| \_valeur DWORD reg | 0 (désactiver) ou 1 (activer) | 0             |



 

## <a name="description"></a>Description

Active le programme d’amélioration de l’expérience utilisateur Windows.

## <a name="change-method"></a>Modifier la méthode

Pour modifier la valeur de cette entrée, dans le panneau de configuration, sélectionnez **système et maintenance**, puis **rapports et solutions aux problèmes**. Cliquez sur paramètres d’amélioration de l' **expérience utilisateur** dans la section Voir aussi.

## <a name="activation-method"></a>Méthode d’activation

Les modifications apportées à cette entrée prennent effet immédiatement. L’activation de cette clé de Registre entraîne l’activation de l’Programme d’amélioration des services Windows pour l’ensemble de l’ordinateur. La désactivation de cette clé de Registre provoque la désactivation de la Programme d’amélioration des services Windows pour l’ensemble de l’ordinateur.

Cette entrée peut être remplacée par un paramètre de stratégie de groupe sur les systèmes qui prennent en charge stratégie de groupe. Tandis que le paramètre Activer le stratégie de groupe du programme d’amélioration du produit Windows Programme d’amélioration des services est activé, le système ignore cette entrée. La configuration de ce paramètre de stratégie est stockée dans la section **stratégies** sous **HKLM \\ Software \\ Policies \\ Microsoft \\ SQMClient \\ Windows \\ CEIPEnable**.

 

 



