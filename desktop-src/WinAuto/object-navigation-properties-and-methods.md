---
title: Propriétés et méthodes de navigation entre les objets
description: Les clients naviguent d’un objet à un autre à l’aide de méthodes telles que IAccessible accNavigate et IAccessible accHitTest.
ms.assetid: c6bcd044-bf70-4eec-92ae-66f9bd836c33
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80631c78e42d9a480992bb40f14d12c0fca8b7c0085ec259daa5550c834d200a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119133752"
---
# <a name="object-navigation-properties-and-methods"></a>Propriétés et méthodes de navigation entre les objets

Les clients *naviguent* d’un objet à un autre à l’aide de méthodes telles que [**IAccessible :: accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) et [**IAccessible :: accHitTest**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-acchittest). Ces méthodes permettent aux clients de récupérer un ID enfant ou l’adresse de l’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) d’un autre objet. La navigation permet aux clients d’explorer les relations entre les objets. Notez que la navigation vers un autre objet ne modifie pas la sélection ou le focus.

L’interface [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) fournit des propriétés et des méthodes qui prennent en charge les types de navigation suivants :

-   [Navigation hiérarchique](hierarchical-navigation.md)
-   [Navigation spatiale et logique](spatial-and-logical-navigation.md)
-   [Navigation via le test de positionnement et l’emplacement à l’écran](navigation-through-hit-testing-and-screen-location.md)

 

 




