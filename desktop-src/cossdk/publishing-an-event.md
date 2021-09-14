---
description: Publication d'un événement
ms.assetid: b40d10aa-43bc-4c53-9e89-94c585d34238
title: Publication d'un événement
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c060d8bf67e12fc7429b2afc768794468a1c49ad
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008184"
---
# <a name="publishing-an-event"></a>Publication d'un événement

pour publier un événement, il vous suffit d’instancier un objet d’événement en appelant [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) ou la méthode Microsoft Visual Basic **CreateObject** en utilisant EventClassID ou événements comme argument. Le serveur de publication appelle [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) sur l’objet d’événement pour obtenir les interfaces prises en charge par l’objet de classe d’événements et appelle une méthode sur l’objet d’événement par le biais de l’interface pour publier l’événement. Le système d’événements publie ensuite des événements sur la classe d’événements CLSID \_ EventObjectChange avec l’ID d’interface IID \_ IEventObjectChange.

Pour prendre en charge la remise d’événements à plusieurs abonnés, les méthodes de classe d’événements doivent contenir uniquement des paramètres in.

En utilisant la propriété FireInParallel de l’objet de [classe d’événements](the-com--event-class-object.md) , les éditeurs peuvent demander que le système d’événements utilise plusieurs threads pour remettre un événement à plusieurs abonnés. La sélection d’un mécanisme de remise en parallèle ne garantit pas la remise simultanée de l’événement à plusieurs abonnés, mais il indique au service d’événements COM+ de l’autoriser à se produire.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Publication et diffusion d’événements dans COM+](publishing-and-delivering-events-in-com-.md)
</dt> </dl>

 

 
