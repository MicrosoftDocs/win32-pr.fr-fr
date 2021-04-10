---
description: Les modules de fusion fonctionnent uniquement avec les composants et non avec les fonctionnalités. Toutefois, certaines tables dans les modules de fusion, telles que la table PublishComponent, contiennent des champs qui font référence à des fonctionnalités.
ms.assetid: f2891457-efef-4319-bd09-5de7fcf32d21
title: Référencement des fonctionnalités dans les modules de fusion
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01640902912aae7d2ca3c6519c92bbdb563a9473
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951906"
---
# <a name="referencing-features-in-merge-modules"></a>Référencement des fonctionnalités dans les modules de fusion

Les modules de fusion fonctionnent uniquement avec les composants et non avec les fonctionnalités. Toutefois, certaines tables dans les modules de fusion, telles que la [table PublishComponent](publishcomponent-table.md), contiennent des champs qui font référence à des fonctionnalités.

Un GUID NULL : {00000000-0000-0000-0000-000000000000} doit être créé dans n’importe quel champ d’une base de données de module de fusion qui fait référence à une fonctionnalité. Lorsque le module de fusion est fusionné dans un package d’installation, l’outil de fusion remplace le GUID NULL par la fonctionnalité spécifiée dans le package d’installation, à l’exception des tables qui nécessitent un traitement spécial, par exemple la [table ModuleSignature](modulesignature-table.md) et les tables ModuleSequence.

Notez que si un GUID null est utilisé comme clé primaire, il n’est pas garanti que la valeur substituée par l’outil de fusion est unique. Les auteurs de modules de fusion sont chargés de s’assurer qu’aucune clé primaire existante dans l’interface de l’utilisateur n’est dupliquée lorsque l’outil de fusion remplace des GUID null avec des fonctionnalités.

 

 



