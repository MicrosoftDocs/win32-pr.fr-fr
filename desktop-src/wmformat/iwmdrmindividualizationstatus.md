---
title: Interface IWMDRMIndividualizationStatus
description: L’interface IWMDRMIndividualizationStatus permet la récupération d’informations d’État avancées sur la progression de l’individualisation. Cette interface est fournie avec des événements MEWMDRMIndividualizationProgress.
ms.assetid: 3a148005-22fa-4495-a47c-d9463db16293
keywords:
- Format Windows Media de l’interface IWMDRMIndividualizationStatus
- Interface IWMDRMIndividualizationStatus format Windows Media, décrit
topic_type:
- apiref
api_name:
- IWMDRMIndividualizationStatus
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: fe6242d2c66b165be8c750d71c61020e9a6acc66f68654d73898fd5000ace3c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118701468"
---
# <a name="iwmdrmindividualizationstatus-interface"></a>Interface IWMDRMIndividualizationStatus

L’interface **IWMDRMIndividualizationStatus** permet la récupération d’informations d’État avancées sur la progression de l’individualisation.

Cette interface est fournie avec des événements MEWMDRMIndividualizationProgress. De nombreux événements de ce type sont générés entre un appel à [**IWMDRMSecurity ::P erformsecurityupdate**](iwmdrmsecurity-performsecurityupdate.md) et l’achèvement du processus d’individualisation, qui est signalé par la génération d’un événement **MEWMDRMIndividualizationCompleted** .

Pour récupérer un pointeur vers une instance de l’interface **IWMDRMIndividualizationStatus** , vous devez d’abord appeler la méthode **IMFMediaEvent :: GetValue** de l’événement Progress. La valeur récupérée à partir de l’événement est un pointeur vers l’interface **IUnknown** de l’objet qui implémente l’interface **IWMDRMIndividualizationStatus** .

## <a name="members"></a>Membres

L’interface **IWMDRMIndividualizationStatus** hérite de l’interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IWMDRMIndividualizationStatus** a également les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IWMDRMIndividualizationStatus** possède ces méthodes.



| Méthode                                                       | Description                                                        |
|:-------------------------------------------------------------|:-------------------------------------------------------------------|
| [**GetStatus**](iwmdrmindividualizationstatus-getstatus.md) | Récupère des informations détaillées sur l’individualisation.<br/> |



 

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Interfaces**](drm-interfaces.md)
</dt> </dl>

 

