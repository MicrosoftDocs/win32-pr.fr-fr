---
title: Surcharge de IPropertyNotifySink
description: Surcharge de IPropertyNotifySink
ms.assetid: c6d52da0-7b7e-4ca8-b903-310bf988d2f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 037b27650ae68f355962454ae154d7c332c73518
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104380273"
---
# <a name="overloading-ipropertynotifysink"></a>Surcharge de IPropertyNotifySink

De nombreux conteneurs de contrôles ActiveX implémentent une fenêtre de navigation des propriétés non modale. Si les propriétés d’un contrôle sont modifiées par le biais des pages de propriétés du contrôle, les propriétés du contrôle peuvent être désynchronisées avec la vue du conteneur de ces propriétés (le contrôle est toujours correct, bien sûr). Pour garantir qu’il a toujours les valeurs actuelles pour les propriétés d’un contrôle, un conteneur de contrôles ActiveX peut surcharger l’interface [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) (liaison de données) et l’utiliser pour être informé qu’une propriété de contrôle a été modifiée. Cette technique est facultative et n’est pas requise pour les conteneurs de contrôles ActiveX ou les contrôles ActiveX.

Notez qu’un contrôle doit utiliser [**OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit) uniquement pour la liaison de données ; Il est libre d’utiliser [**OnChanged**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onchanged) pour l’une ou les deux opérations.

 

 




