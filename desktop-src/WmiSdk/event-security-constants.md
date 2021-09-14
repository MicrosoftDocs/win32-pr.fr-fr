---
description: L’exemple suivant montre les constantes de sécurité WMI utilisées pour les événements. Ils sont utilisés pour définir des entrées de contrôle d’accès (ACE) dans les descripteurs de sécurité utilisés pour les événements ou les récepteurs.
ms.assetid: 18318262-d948-4329-8d48-23664798fc58
ms.tgt_platform: multiple
title: Constantes de sécurité d’événement (Wbemcli. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4a3009b16e468a647ee96b9be365286caba2c12b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126915784"
---
# <a name="event-security-constants"></a>Constantes de sécurité d’événement

L’exemple suivant montre les constantes de sécurité WMI utilisées pour les événements. Ils sont utilisés pour définir des entrées de contrôle d’accès (ACE) dans les descripteurs de sécurité utilisés pour les événements ou les récepteurs.

<dl> <dt>

<span id="WBEM_RIGHT_PUBLISH"></span><span id="wbem_right_publish"></span>**\_publication WBEM Right \_**
</dt> <dd> <dl> <dt>

128 (0x80)
</dt> <dt>



Spécifie que le compte peut publier des événements sur l’instance de [**\_ \_ EventFilter**](--eventfilter.md) qui définit le filtre d’événement pour un consommateur permanent. Disponible dans wbemcli. h.


</dt> </dl> </dd> <dt>

<span id="WBEM_RIGHT_SUBSCRIBE"></span><span id="wbem_right_subscribe"></span>**\_ \_ s’abonner directement à WBEM**
</dt> <dd> <dl> <dt>

64 (0x40)
</dt> <dt>



Spécifie qu’un consommateur peut s’abonner aux événements remis à un récepteur. Utilisé dans [**IWbemEventSink :: SetSinkSecurity**](/windows/desktop/api/Wbemprov/nf-wbemprov-iwbemeventsink-setsinksecurity). Disponible dans wbemcli. h.


</dt> </dl> </dd> <dt>

<span id="WBEM_S_SUBJECT_TO_SDS"></span><span id="wbem_s_subject_to_sds"></span>**les \_ S WBEM sont \_ soumises \_ à \_ SDS**
</dt> <dd> <dl> <dt>

274435 (0x43003)
</dt> <dt>



Fournisseur d’événements indique que WMI vérifie la propriété du **\_ descripteur de sécurité** dans chaque événement (hérité de l' [**\_ \_ événement**](--event.md)) et envoie uniquement des événements aux consommateurs avec les autorisations d’accès appropriées. Disponible dans wbemprov. h.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                                                                                         |
| En-tête<br/>                   | <dl> <dt>Wbemcli. h ; </dt> <dt>Wbemprov. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes de sécurité WMI](wmi-security-constants.md)
</dt> <dt>

[Maintenance de la sécurité WMI](maintaining-wmi-security.md)
</dt> <dt>

[Sécurisation des événements WMI](securing-wmi-events.md)
</dt> </dl>

 

 




