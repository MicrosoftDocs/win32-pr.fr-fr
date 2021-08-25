---
description: Une commande d’arrêt de contrôle de flux a pris effet.
ms.assetid: a2f7a959-fafd-47ff-9b3d-1a898fdb1f81
title: EC_STREAM_CONTROL_STOPPED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 69884ecc573b2bb775092529cb81e1b33a1514d4799af9f55c7bcebb5ebd2b24
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928419"
---
# <a name="ec_stream_control_stopped"></a>\_le contrôle de flux EC s' \_ \_ est arrêté

Une commande d’arrêt de contrôle de flux a pris effet.

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="pSender"></span><span id="psender"></span><span id="PSENDER"></span>*pSender*
</dt> <dd>

(**IUnknown** \* ) Pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) du code confidentiel qui a arrêté le flux.

</dd> <dt>

<span id="dwCookie"></span><span id="dwcookie"></span><span id="DWCOOKIE"></span>*dwCookie*
</dt> <dd>

(**DWORD**) Valeur définie par l’utilisateur.

</dd> </dl>

## <a name="default-action"></a>Action par défaut

Aucun.

## <a name="remarks"></a>Notes

Les filtres envoient cet événement en réponse à la méthode [**IAMStreamControl :: STOPAT**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) . La méthode **STOPAT** spécifie un temps de référence pour un code confidentiel pour arrêter la diffusion en continu. Lorsque la diffusion en continu s’arrête, le filtre envoie cet événement.

Le paramètre *pSender* spécifie le code confidentiel qui exécute la commande Stop. En fonction de l’implémentation, il est possible qu’il ne s’agit pas du code confidentiel qui a reçu l’appel [**STOPAT**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) .

Le paramètre *dwCookie* est spécifié par l’application dans la méthode [**STOPAT**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-stopat) . Ce paramètre permet à l’application d’effectuer le suivi de plusieurs appels à la méthode.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Codes de notification d’événement](event-notification-codes.md)
</dt> <dt>

[Notification d’événements dans DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




