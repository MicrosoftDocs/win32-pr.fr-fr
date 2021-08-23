---
title: Informations générales
description: le composant Microsoft Active Accessibility, oleacc.dll, crée des objets proxy qui implémentent IAccessible pour le compte de contrôles Windows standard.
ms.assetid: c010af48-384c-40c0-ab52-c80b225502fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17d154beb5d824bc722e713346129258c2d294d678a92c1b66d12035ce390f44
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052957"
---
# <a name="background-information"></a>Informations générales

le composant Microsoft Active Accessibility, oleacc.dll, crée des objets proxy qui implémentent [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) pour le compte de contrôles Windows standard. étant donné que ces proxies utilisent des messages de Windows standard et des api spécifiques au contrôle pour collecter des informations sur chaque contrôle, il n’existe aucun mécanisme direct pour la personnalisation des informations exposées par ces proxies par le biais de **IAccessible**.

Actuellement, vous pouvez personnaliser une implémentation [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) existante à l’aide de techniques de sous-classe et d’encapsulation. Toutefois, ces techniques sont fastidieuses et sujettes aux erreurs. En fait, la majorité du code écrit pour remplacer une ou deux propriétés s’intéresse à l’implémentation de la sous-classe et de l’encapsulation. seule une petite fraction effectue la tâche réelle de remplacement des informations. L’annotation dynamique améliore la situation en fournissant des fonctionnalités similaires sans avoir à écrire du code de sous-classe ou d’habillage. Au lieu de cela, vous pouvez vous concentrer sur la fourniture de code qui fournit les informations correctes. L’annotation dynamique permet aux développeurs de passer des indications et d’autres informations utiles à OLEACC pour personnaliser les informations qu’elle expose. Cette fonctionnalité permet de réduire le coût de prise en charge de Microsoft Active Accessibility et de permettre aux développeurs d’améliorer de façon considérable l’accessibilité de leurs interfaces utilisateur.

 

 




