---
title: Exposition d’une interface de modèle objet natif
description: Si un élément d’interface utilisateur prend en charge un modèle d’objet natif autre que Microsoft Active Accessibility ou UI Automation, il peut exposer l’interface personnalisée en répondant aux \_ messages WM GETOBJECT qui incluent l' \_ identificateur d’objet objid NATIVEOM.
ms.assetid: 430abeaf-e5ca-48c4-aa35-8d52a8cee2f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 701ed721e8259aa3b707fa1d7a6f2e80b9da13a3760b9850edef22b169d772e1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119644919"
---
# <a name="exposing-a-native-object-model-interface"></a>Exposition d’une interface de modèle objet natif

Si un élément d’interface utilisateur prend en charge un modèle d’objet natif autre que Microsoft Active Accessibility ou UI Automation, il peut exposer l’interface personnalisée en répondant aux messages [**WM \_ GETOBJECT**](wm-getobject.md) qui incluent l’identificateur d’objet [**objID \_ NATIVEOM**](object-identifiers.md) . Pour répondre, l’élément d’interface utilisateur doit retourner la valeur récupérée par un appel à la fonction [**LresultFromObject**](/windows/desktop/api/Oleacc/nf-oleacc-lresultfromobject) .

Un client peut récupérer une interface à partir d’un élément d’interface utilisateur qui prend en charge un modèle objet natif en appelant la fonction [**AccessibleObjectFromWindow**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromwindow) et en spécifiant [**objID \_ NATIVEOM**](object-identifiers.md) comme deuxième paramètre.

 

 




