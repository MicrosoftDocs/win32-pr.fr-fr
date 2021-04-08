---
description: Événement de traçage réseau Winsock pour l’opération de fermeture du Socket.
ms.assetid: C59B2B51-288A-46C9-B390-26A18DB0C2FB
title: Événement AFD_EVENT_CLOSE
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AFD_EVENT_CLOSE
api_type:
- NA
api_location: ''
ms.openlocfilehash: fbc6c63a3084db6a9be0a4b4ea7672d84881a29a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751485"
---
# <a name="afd_event_close-event"></a>Événement de fermeture d' \_ événement AFD \_

L’événement de **\_ \_ fermeture d’événement AFD** est un événement de traçage réseau Winsock pour l’opération de fermeture de Socket.


```C++
const EVENT_DESCRIPTOR AFD_EVENT_CLOSE = {0x3e9, 0x0, 0x10, 0x4, 0xf, 0x3e9, 0x8000000000000004};
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*EnterExit* 
</dt> <dd>

Informations sur cet événement.

Le tableau suivant répertorie les valeurs possibles pour le paramètre *EnterExit* :



| Valeur                                                                        | Signification                                                                                              |
|------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>0</dt> </dl> | Début d’une demande Winsock.<br/>                                                           |
| <dl> <dt>1</dt> </dl> | La demande Winsock est terminée.<br/>                                                            |
| <dl> <dt>2</dt> </dl> | Le pilote AFD Winsock a effectué une action interne (en abandonnant une connexion, par exemple).<br/>      |
| <dl> <dt>3</dt> </dl> | Le pilote TCP/IP a entraîné l’apparition de cet événement. Cela indique généralement une notification de données.<br/> |
| <dl> <dt>4</dt> </dl> | Le pilote AFD Winsock a entraîné l’apparition de cet événement (par exemple, la définition d’une option de socket).<br/> |



 

</dd> <dt>

*Lieu* 
</dt> <dd>

Champ privé utilisé en interne.

</dd> <dt>

*Processus* 
</dt> <dd>

Adresse [EPROCESS](/windows-hardware/drivers/kernel/eprocess) du processus qui possède le socket associé. Il s’agit d’une structure opaque qui sert d’objet de processus pour un processus. Pour plus d’informations, consultez la documentation du kit de pilotes Windows pour la structure [EPROCESS](/windows-hardware/drivers/kernel/eprocess) .

</dd> <dt>

*Point de terminaison* 
</dt> <dd>

\_Adresse du point de terminaison AFD du Socket.

</dd> <dt>

*État* 
</dt> <dd>

Code NTSTATUS pour l’opération.

</dd> </dl>

## <a name="remarks"></a>Notes

L’événement de **\_ \_ fermeture d’événement AFD** est suivi pour qu’une opération réseau Winsock ferme un Socket. Le canal de cet événement est Winsock-AFD. Le niveau de cet événement est informatif.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 7 uniquement\]<br/>              |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 R2 \[ uniquement\]<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Contrôle du suivi Winsock](control-of-winsock-tracing.md)
</dt> <dt>

[**descripteur d’événement \_**](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor)
</dt> <dt>

[Suivi Winsock](winsock-tracing.md)
</dt> <dt>

[Niveaux de suivi Winsock](winsock-tracing-levels.md)
</dt> <dt>

[Détails du suivi de modification du catalogue Winsock](winsock-layered-service-provider-tracing-event-details.md)
</dt> </dl>

 

