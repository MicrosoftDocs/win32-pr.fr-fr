---
description: Appareils mobiles Windows prend en charge les propriétés d’événement suivantes.
ms.assetid: 672b75ac-cd47-4212-a505-c220ecdf98e3
title: Propriétés de l’événement (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Event
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 54c7aefeaf1170b7a8b8e3e79a62288f2d14dad2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537701"
---
# <a name="event-properties"></a>Propriétés de l’événement

Appareils mobiles Windows prend en charge les propriétés d’événement suivantes.



<table>
<thead>
<tr class="header">
<th>Propriété</th>
<th>VarType</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>WPD_EVENT_OPTION_IS_AUTOPLAY_EVENT</strong></td>
<td><strong>VT_BOOL</strong></td>
<td>Réservé pour un usage futur.</td>
</tr>
<tr class="even">
<td><strong>WPD_EVENT_OPTION_IS_BROADCAST_EVENT</strong></td>
<td><strong>VT_BOOL</strong></td>
<td>Valeur booléenne qui spécifie si l’événement est diffusé à tous les clients. Les clients peuvent recevoir cet événement en inscrivant leur rappel avec <strong>IPortableDevice :: Advise</strong>.<br/></td>
</tr>
<tr class="odd">
<td><strong>WPD_EVENT_PARAMETER_CHILD_HIERARCHY_CHANGED</strong></td>
<td><strong>VT_BOOL</strong></td>
<td>Valeur booléenne qui spécifie si la hiérarchie enfant de l’objet a changé. Ce paramètre est utilisé pour informer l’appelant que certains enfants de l’objet spécifié ont été ajoutés ou supprimés. En général, la modification de la hiérarchie est lancée côté appareil. Les clients devront peut-être réénumérer les enfants de ce dossier pour maintenir à jour leurs vues.<br/></td>
</tr>
<tr class="even">
<td><strong>WPD_EVENT_PARAMETER_EVENT_ID</strong></td>
<td><strong>VT_CLSID</strong></td>
<td>Valeur qui identifie un événement.</td>
</tr>
<tr class="odd">
<td><strong>WPD_EVENT_PARAMETER_OBJECT_CREATION_COOKIE</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Le cookie est remis à un client lorsqu’il demande la création d’un objet en appelant la méthode <a href="/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevicecontent-createobjectwithpropertiesanddata"><strong>IPortableDeviceContent :: CreateObjectWithPropertiesAndData</strong></a> . Ce paramètre est ajouté pour aider l’appelant à lier un événement ajouté à l’objet à la demande qu’il a envoyée pour créer l’objet. Le pilote rétablit ce cookie comme valeur de retour <strong>WPD_PROPERTY_OBJECT_MANAGEMENT_CONTEXT</strong> lors du traitement de la commande <strong>WPD_COMMAND_OBJECT_MANAGEMENT_CREATE_OBJECT_WITH_PROPERTIES_AND_DATA</strong> .<br/></td>
</tr>
<tr class="even">
<td><strong>WPD_EVENT_PARAMETER_OBJECT_PARENT_PERSISTENT_UNIQUE_ID</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Valeur qui identifie de façon unique l’objet parent. Cette propriété est similaire à <strong>WPD_OBJECT_PARENT_ID</strong>, mais cet ID ne change pas entre les sessions.</td>
</tr>
<tr class="odd">
<td><strong>WPD_EVENT_PARAMETER_OPERATION_PROGRESS</strong></td>
<td><strong>VT_UI4</strong></td>
<td>Valeur qui spécifie la progression d’une opération en cours d’exécution. La valeur de cette propriété peut être comprise entre 0 et 100, avec 100 indiquant que l’opération est terminée.</td>
</tr>
<tr class="even">
<td><strong>WPD_EVENT_PARAMETER_OPERATION_STATE</strong></td>
<td><strong>VT_UI4</strong></td>
<td>Valeur qui indique l’état actuel de l’opération, par exemple, démarrée, en cours d’exécution, arrêtée, etc. Les valeurs possibles de ce paramètre proviennent de l’énumération <strong>WPD_OPERATION_STATES</strong> définie dans PortableDevice. h. Les valeurs possibles sont les suivantes :<br/> <dl> <strong>WPD_OPERATION_STATE_UNSPECIFIED</strong><br />
<strong>WPD_OPERATION_STATE_STARTED</strong><br />
<strong>WPD_OPERATION_STATE_RUNNING</strong><br />
<strong>WPD_OPERATION_STATE_PAUSED</strong><br />
<strong>WPD_OPERATION_STATE_CANCELLED</strong><br />
<strong>WPD_OPERATION_STATE_FINISHED</strong><br />
<strong>WPD_OPERATION_STATE_ABORTED</strong><br />
</dl></td>
</tr>
<tr class="odd">
<td><strong>WPD_EVENT_PARAMETER_PNP_DEVICE_ID</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Valeur qui spécifie le périphérique à l’origine de l’événement. Il s’agit de l’identificateur de périphérique ou de service fourni par le système plug-and-Play (PnP). il s’agit de la même chaîne que celle utilisée dans les méthodes <strong>IPortableDevice :: Open</strong>ou <a href="/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservice-open"><strong>IPortableDeviceService :: Open</strong></a> .<br/></td>
</tr>
<tr class="even">
<td><strong>WPD_EVENT_PARAMETER_SERVICE_METHOD_CONTEXT</strong></td>
<td><strong>VT_LPWSTR</strong></td>
<td>Chaîne utilisée par un pilote WPD pour identifier l’opération d’une méthode de service d’appareil. Les applications ne doivent pas utiliser ce paramètre directement.</td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Propriétés et attributs WPD**](properties-and-attributes.md)
</dt> </dl>

 

 




