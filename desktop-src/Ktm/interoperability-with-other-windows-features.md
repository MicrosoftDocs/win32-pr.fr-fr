---
description: Le Distributed Transaction Coordinator (DTC) active les transactions distribuées ou les transactions qui sont sous le contrôle de plusieurs gestionnaires de ressources sur un ou plusieurs systèmes. KTM et DTC fonctionnent étroitement ensemble pour y parvenir.
ms.assetid: 468379e2-c5f6-479f-9d5d-42afb395ec9b
title: interopérabilité avec d’autres fonctionnalités de Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a18595140676539c6e5acaa5fc62835ac279215d068834e3e56dffe50d01e0e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119265069"
---
# <a name="interoperability-with-other-windows-features"></a>interopérabilité avec d’autres fonctionnalités de Windows

Le [Distributed Transaction Coordinator](/previous-versions/windows/desktop/ms684146(v=vs.85)) (DTC) active les *transactions distribuées* ou les transactions qui sont sous le contrôle de plusieurs gestionnaires de ressources sur un ou plusieurs systèmes. KTM et DTC fonctionnent étroitement ensemble pour y parvenir.

COM+ expose un modèle déclaratif pour la programmation transactionnelle. En d’autres termes, le programmeur déclare dans quelle mesure un objet peut tirer parti des transactions et le runtime COM+ gère les transactions au nom de l’objet. Par exemple, un objet peut être déclaré pour participer à une transaction uniquement s’il en existe déjà un, pour exiger une transaction (une transaction est créée si elle n’existe pas déjà), pour exiger une nouvelle transaction (créée, qu’il en existe déjà une) ou non transactionnelle. Ces transactions gérées de façon déclarative sont automatiquement utilisées sur les connexions de base de données créées par des objets COM+ qui s’exécutent dans le contexte d’une transaction.

 

 
