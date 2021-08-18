---
description: HKLM \\ Software \\ Microsoft \\ SQMClient \\ Windows \\ CEIPEnable.
ms.assetid: 68ba8219-7ed2-44a9-9fd5-f6dfa57891c0
title: CEIPEnable
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 687e17bf5438406fb7a29b954bf8a2640fc0ea5d193ba49ae7fd7bd02f1f27bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118956118"
---
# <a name="ceipenable"></a>CEIPEnable

**HKLM \\ Software \\ Microsoft \\ SQMClient \\ Windows \\ CEIPEnable**



| Type de données  | Plage                     | Valeur par défaut |
|------------|---------------------------|---------------|
| \_valeur DWORD reg | 0 (désactiver) ou 1 (activer) | 0             |



 

## <a name="description"></a>Description

active le programme d’amélioration de l’expérience utilisateur Windows.

## <a name="change-method"></a>Modifier la méthode

Pour modifier la valeur de cette entrée, dans le panneau de configuration, sélectionnez **système et maintenance**, puis **rapports et solutions aux problèmes**. cliquez sur amélioration de l' **expérience utilisateur Paramètres** dans la section voir aussi.

## <a name="activation-method"></a>Méthode d’activation

Les modifications apportées à cette entrée prennent effet immédiatement. l’activation de cette clé de registre provoque l’activation du Programme d’amélioration des services Windows pour l’ordinateur entier. la désactivation de cette clé de registre provoque la désactivation du Programme d’amélioration des services Windows pour l’ensemble de l’ordinateur.

Cette entrée peut être remplacée par un paramètre de stratégie de groupe sur les systèmes qui prennent en charge stratégie de groupe. tandis que le paramètre Windows Programme d’amélioration des services CEIP Enable stratégie de groupe est activé, le système ignore cette entrée. la configuration de ce paramètre de stratégie est stockée dans la section **stratégies** sous **HKLM \\ Software \\ policies \\ Microsoft \\ SQMClient \\ Windows \\ CEIPEnable**.

 

 



