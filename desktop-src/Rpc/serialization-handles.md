---
title: Handles de sérialisation
description: Une application utilise les procédures de sérialisation ou les routines de prise en charge de sérialisation générées par le compilateur MIDL conjointement avec un ensemble de fonctions de bibliothèque pour manipuler un handle de sérialisation.
ms.assetid: 39859846-5b94-447a-a71b-a08b8eb2c4c1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5585fc3f34b6cc826c1f8157bd59a144070ea081
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104029656"
---
# <a name="serialization-handles"></a>Handles de sérialisation

Une application utilise les procédures de sérialisation ou les routines de prise en charge de sérialisation générées par le compilateur MIDL conjointement avec un ensemble de fonctions de bibliothèque pour manipuler un handle de sérialisation. Ensemble, ces fonctions fournissent un mécanisme permettant de personnaliser la façon dont une application sérialise les données.

Un handle de sérialisation est requis pour toute opération de sérialisation, et tous les handles de sérialisation doivent être gérés explicitement par vous-même. Pour ce faire, vous devez d’abord créer un handle valide en appelant l’une des routines suivantes :

-   [**MesDecodeBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodebufferhandlecreate)
-   [**MesDecodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesdecodeincrementalhandlecreate)
-   [**MesEncodeDynBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodedynbufferhandlecreate)
-   [**MesEncodeFixedBufferHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodefixedbufferhandlecreate)
-   [**MesEncodeIncrementalHandleCreate**](/windows/desktop/api/Midles/nf-midles-mesencodeincrementalhandlecreate)

Vous publiez le handle avec un appel à [**MesHandleFree**](/windows/desktop/api/Midles/nf-midles-meshandlefree). Une fois que le handle a été créé ou réinitialisé, il représente un contexte de sérialisation valide et peut être utilisé pour encoder ou décoder, selon le type du descripteur.

Cette section décrit les descripteurs de sérialisation et leur utilisation dans les rubriques suivantes :

-   [Descripteurs implicites et explicites](implicit-versus-explicit-handles.md)
-   [Styles de sérialisation](serialization-styles.md)
-   [Obtention d’une identité d’encodage](obtaining-an-encoding-identity.md)

 

 




