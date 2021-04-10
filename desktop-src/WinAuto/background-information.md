---
title: Informations générales
description: Le composant Microsoft Active Accessibility, oleacc.dll, crée des objets proxy qui implémentent IAccessible pour le compte de contrôles Windows standard.
ms.assetid: c010af48-384c-40c0-ab52-c80b225502fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0a9b044f8035a474f02b8457dc99ec39aca73c2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100649"
---
# <a name="background-information"></a>Informations générales

Le composant Microsoft Active Accessibility, oleacc.dll, crée des objets proxy qui implémentent [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) pour le compte de contrôles Windows standard. Étant donné que ces proxies utilisent des messages Windows standard et des API spécifiques au contrôle pour collecter des informations sur chaque contrôle, il n’existe aucun mécanisme direct pour la personnalisation des informations exposées par ces proxies par le biais de **IAccessible**.

Actuellement, vous pouvez personnaliser une implémentation [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) existante à l’aide de techniques de sous-classe et d’encapsulation. Toutefois, ces techniques sont fastidieuses et sujettes aux erreurs. En fait, la majorité du code écrit pour remplacer une ou deux propriétés s’intéresse à l’implémentation de la sous-classe et de l’encapsulation. seule une petite fraction effectue la tâche réelle de remplacement des informations. L’annotation dynamique améliore la situation en fournissant des fonctionnalités similaires sans avoir à écrire du code de sous-classe ou d’habillage. Au lieu de cela, vous pouvez vous concentrer sur la fourniture de code qui fournit les informations correctes. L’annotation dynamique permet aux développeurs de passer des indications et d’autres informations utiles à OLEACC pour personnaliser les informations qu’elle expose. Cette fonctionnalité permet de réduire le coût de prise en charge de Microsoft Active Accessibility et de permettre aux développeurs d’améliorer de façon considérable l’accessibilité de leurs interfaces utilisateur.

 

 




