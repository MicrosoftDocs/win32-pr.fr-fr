---
description: Lance la communication avec un fournisseur d’événements à l’aide d’un ensemble restreint de requêtes.
ms.assetid: dd076dd0-ed39-47a2-86fb-a595baf3f464
ms.tgt_platform: multiple
title: Interface IWbemEventSink (wbemprov. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemEventSink
api_type:
- COM
api_location:
- Wbemsvc.dll
ms.openlocfilehash: 10c5fa56a96db3e46ce2c4c7941fd7a1d6fb27a1730dc3741890935782e4ace7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118318095"
---
# <a name="iwbemeventsink-interface"></a>Interface IWbemEventSink

L’interface **IWbemEventSink** initie la communication avec un fournisseur d’événements à l’aide d’un ensemble restreint de requêtes. Cette interface étend [**IWbemObjectSink**](iwbemobjectsink.md), en fournissant de nouvelles méthodes pour la sécurité et les performances. Pour plus d’informations sur l’utilisation de cette interface, consultez [écriture d’un fournisseur d’événements](writing-an-event-provider.md) et [sécurisation des événements WMI](securing-wmi-events.md).

## <a name="members"></a>Membres

L’interface **IWbemEventSink** possède les types de membres suivants :

-   [Méthodes](#methods)

### <a name="methods"></a>Méthodes

L’interface **IWbemEventSink** possède ces méthodes.



| Méthode                                                                | Description                                                           |
|:----------------------------------------------------------------------|:----------------------------------------------------------------------|
| [**GetRestrictedSink**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-getrestrictedsink)         | Appelée par le consommateur pour configurer des requêtes d’événement restreintes.<br/> |
| [**IsActive**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-isactive)                           | Vérifie l’état du récepteur d’événements.<br/>                               |
| [**SetBatchingParameters**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setbatchingparameters) | Appelé par le consommateur pour définir les paramètres de traitement par lot.<br/>         |
| [**SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity)             | Utilisé pour mettre à jour le descripteur de sécurité sur un récepteur d’événements.<br/>   |



 

## <a name="remarks"></a>Remarques

Lors de l’implémentation d’un récepteur d’abonnement aux événements ([**IWbemObjectSink**](iwbemobjectsink.md) ou **IWbemEventSink**), n’appelez pas WMI à partir des méthodes sur l’objet récepteur. Par exemple, l’appel de [**IWbemServices :: CancelAsyncCall**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-cancelasynccall) pour annuler le récepteur dans une implémentation de [**IWbemEventSink :: SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity) peut interférer avec l’État WMI. Pour annuler un abonnement à un événement, définissez un indicateur et appelez **IWbemServices :: CancelAsyncCall** à partir d’un autre thread ou objet. Pour les implémentations qui ne sont pas liées à un récepteur d’événements, telles que les récupérations d’objets, d’enum et de requêtes, vous pouvez rappeler dans WMI.

Les implémentations de récepteur doivent traiter la notification d’événement dans un délai de 100 ms car le thread WMI qui remet la notification d’événement ne peut pas effectuer d’autres tâches tant que le traitement de l’objet récepteur n’est pas terminé. Si la notification nécessite une grande quantité de traitement, le récepteur peut utiliser une file d’attente interne pour qu’un autre thread gère le traitement.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                                            |
| En-tête<br/>                   | <dl> <dt>Wbemprov. h (inclure Wbemidl. h)</dt> </dl> |
| Bibliothèque<br/>                  | <dl> <dt>Wbemuuid. lib</dt> </dl>                   |
| DLL<br/>                      | <dl> <dt>Wbemsvc.dll</dt> </dl>                    |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[API COM pour WMI](com-api-for-wmi.md)
</dt> </dl>

 

 




