---
title: Surcharge de IPropertyNotifySink
description: Surcharge de IPropertyNotifySink
ms.assetid: c6d52da0-7b7e-4ca8-b903-310bf988d2f7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4faca0027144498138e1a60bf3df9a29b618aeb7eb09198ff97a3dd7616be67
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118310022"
---
# <a name="overloading-ipropertynotifysink"></a>Surcharge de IPropertyNotifySink

de nombreux conteneurs de contrôle ActiveX implémentent une fenêtre de navigation des propriétés non modale. Si les propriétés d’un contrôle sont modifiées par le biais des pages de propriétés du contrôle, les propriétés du contrôle peuvent être désynchronisées avec la vue du conteneur de ces propriétés (le contrôle est toujours correct, bien sûr). pour garantir qu’il a toujours les valeurs actuelles pour les propriétés d’un contrôle, un conteneur de contrôle ActiveX peut surcharger l’interface [**IPropertyNotifySink**](/windows/desktop/api/OCIdl/nn-ocidl-ipropertynotifysink) (liaison de données) et l’utiliser également pour être averti qu’une propriété de contrôle a été modifiée. cette technique est facultative et n’est pas obligatoire pour les conteneurs de contrôle ActiveX ou les contrôles de ActiveX.

Notez qu’un contrôle doit utiliser [**OnRequestEdit**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onrequestedit) uniquement pour la liaison de données ; Il est libre d’utiliser [**OnChanged**](/windows/desktop/api/OCIdl/nf-ocidl-ipropertynotifysink-onchanged) pour l’une ou les deux opérations.

 

 




