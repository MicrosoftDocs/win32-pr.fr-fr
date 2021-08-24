---
description: Les \_ constantes LINEADDRFEATURE répertorient les opérations qui peuvent être appelées sur une adresse.
ms.assetid: dedeee7b-578b-4b19-8b99-5cd23779d661
title: Constantes LINEADDRFEATURE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bb545bdf0195d9fd8ed35833150b9cfd1f6b10bfbd3d1ead7e8ebff65c93132
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682218"
---
# <a name="lineaddrfeature_-constants"></a>\_Constantes LINEADDRFEATURE

Les constantes **LINEADDRFEATURE \_** répertorient les opérations qui peuvent être appelées sur une adresse.

<dl> <dt>

<span id="LINEADDRFEATURE_FORWARD"></span><span id="lineaddrfeature_forward"></span>**LINEADDRFEATURE \_ vers l’avant**
</dt> <dd> <dl> <dt>



L’adresse peut être transférée.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_MAKECALL"></span><span id="lineaddrfeature_makecall"></span>**LINEADDRFEATURE \_ MAKECALL**
</dt> <dd> <dl> <dt>



Un appel sortant peut être placé sur l’adresse.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_PICKUP"></span><span id="lineaddrfeature_pickup"></span>**\_collecte LINEADDRFEATURE**
</dt> <dd> <dl> <dt>



Un appel peut être récupéré à l’adresse.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_PICKUPDIRECT"></span><span id="lineaddrfeature_pickupdirect"></span>**LINEADDRFEATURE \_ PICKUPDIRECT**
</dt> <dd> <dl> <dt>



La fonction [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) peut être utilisée pour récupérer un appel sur une adresse spécifique.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_PICKUPGROUP"></span><span id="lineaddrfeature_pickupgroup"></span>**LINEADDRFEATURE \_ PICKUPGROUP**
</dt> <dd> <dl> <dt>



La fonction [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) peut être utilisée pour récupérer un appel dans le groupe.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_PICKUPHELD"></span><span id="lineaddrfeature_pickupheld"></span>**LINEADDRFEATURE \_ PICKUPHELD**
</dt> <dd> <dl> <dt>



La fonction [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) (avec une adresse de destination **null** ) peut être utilisée pour récupérer un appel détenu sur l’adresse. Cela est normalement utilisé uniquement dans une organisation avec pontage exclusive.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_PICKUPWAITING"></span><span id="lineaddrfeature_pickupwaiting"></span>**LINEADDRFEATURE \_ PICKUPWAITING**
</dt> <dd> <dl> <dt>



La fonction [**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup) (avec une adresse de destination **null** ) peut être utilisée pour récupérer un appel d’appel en attente. Notez que cela n’indique pas nécessairement qu’un appel en attente est réellement présent, car il est souvent impossible pour un appareil de téléphonie de détecter automatiquement un tel appel ; Toutefois, il indique que la fonction de raccordement-Flash sera appelée pour tenter de basculer vers ce type d’appel.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_SETMEDIACONTROL"></span><span id="lineaddrfeature_setmediacontrol"></span>**LINEADDRFEATURE \_ SETMEDIACONTROL**
</dt> <dd> <dl> <dt>



Le contrôle de média peut être défini sur cette adresse.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_SETTERMINAL"></span><span id="lineaddrfeature_setterminal"></span>**LINEADDRFEATURE \_ SETTERMINAL**
</dt> <dd> <dl> <dt>



Les modes de terminal pour cette adresse peuvent être définis.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_SETUPCONF"></span><span id="lineaddrfeature_setupconf"></span>**LINEADDRFEATURE \_ SETUPCONF**
</dt> <dd> <dl> <dt>



Un appel de conférence avec un appel initial **null** peut être configuré à cette adresse.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_UNCOMPLETECALL"></span><span id="lineaddrfeature_uncompletecall"></span>**LINEADDRFEATURE \_ UNCOMPLETECALL**
</dt> <dd> <dl> <dt>



Les demandes d’achèvement d’appel peuvent être annulées à cette adresse.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_UNPARK"></span><span id="lineaddrfeature_unpark"></span>**déspark LINEADDRFEATURE \_**
</dt> <dd> <dl> <dt>



Les appels peuvent être désimmobilisés à l’aide de cette adresse.

> [!Note]  
> Si aucun des nouveaux bits modifiés « PICKUP » n’est défini dans le membre **dwAddressFeatures** dans [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) , mais que le \_ bit de collecte LINEADDRFEATURE est défini, alors l’un des modes de collecte peut fonctionner ; le fournisseur de services n’a simplement pas spécifié les uns des autres.

 


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_FORWARDDND"></span><span id="lineaddrfeature_forwarddnd"></span>**LINEADDRFEATURE \_ FORWARDDND**
</dt> <dd> <dl> <dt>



La fonction [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) (avec une adresse de destination vide) peut être utilisée pour activer la fonctionnalité ne pas déranger sur l’adresse. LINEADDRFEATURE \_ Forward sera également défini.


</dt> </dl> </dd> <dt>

<span id="LINEADDRFEATURE_FORWARDFWD"></span><span id="lineaddrfeature_forwardfwd"></span>**LINEADDRFEATURE \_ FORWARDFWD**
</dt> <dd> <dl> <dt>



La fonction [**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward) peut être utilisée pour transférer des appels sur l’adresse à d’autres nombres. LINEADDRFEATURE \_ Forward sera également défini.

> [!Note]  
> Si aucun des nouveaux bits « FORWARD » modifiés n’est défini dans le membre **dwAddressFeatures** dans [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) , mais que le \_ bit de transfert LINEADDRFEATURE est défini, alors l’un des modes de transfert peut fonctionner ; le fournisseur de services n’a simplement pas spécifié les uns des autres.

 


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Remarques

Aucune extensibilité. Tous les 32 bits sont réservés.

Cette constante est utilisée à la fois dans [**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps) (retournée par [**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)) et dans [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) (retournée par [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)). **LINEADDRESSCAPS** signale la disponibilité des fonctionnalités d’adresse par le fournisseur de services (principalement le commutateur) pour une adresse donnée. Une application effectue cette détermination lors de son initialisation. La structure [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) signale, pour une adresse donnée, les fonctionnalités d’adresse qui peuvent être appelées alors que l’adresse est dans l’état actuel. Une application effectue cette détermination de manière dynamique après modification de l’état de l’adresse, généralement provoquée par les activités liées aux appels sur l’adresse.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**LINEADDRESSCAPS**](/windows/desktop/api/Tapi/ns-tapi-lineaddresscaps)
</dt> <dt>

[**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)
</dt> <dt>

[**lineForward**](/windows/desktop/api/Tapi/nf-tapi-lineforward)
</dt> <dt>

[**lineGetAddressCaps**](/windows/desktop/api/Tapi/nf-tapi-linegetaddresscaps)
</dt> <dt>

[**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)
</dt> <dt>

[**linePickup**](/windows/desktop/api/Tapi/nf-tapi-linepickup)
</dt> </dl>

 

 




