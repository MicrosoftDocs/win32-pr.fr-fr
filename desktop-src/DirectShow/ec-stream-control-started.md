---
description: Une commande de démarrage de flux de contrôle a pris effet.
ms.assetid: e2f8d9a2-c96c-457c-8a88-7c86d4405928
title: EC_STREAM_CONTROL_STARTED (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 984562fde9001de14067e5865d5583636b264852
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106530450"
---
# <a name="ec_stream_control_started"></a>\_le contrôle de flux EC \_ \_ a démarré

Une commande de démarrage de flux de contrôle a pris effet.

## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="pSender"></span><span id="psender"></span><span id="PSENDER"></span>*pSender*
</dt> <dd>

(**IUnknown** \* ) Pointeur vers l’interface [**IPIN**](/windows/desktop/api/Strmif/nn-strmif-ipin) du code confidentiel qui a démarré le flux.

</dd> <dt>

<span id="dwCookie"></span><span id="dwcookie"></span><span id="DWCOOKIE"></span>*dwCookie*
</dt> <dd>

(**DWORD**) Valeur définie par l’utilisateur.

</dd> </dl>

## <a name="default-action"></a>Action par défaut

Aucun.

## <a name="remarks"></a>Notes

Les filtres envoient cet événement en réponse à la méthode [**IAMStreamControl :: startat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) . Cette méthode spécifie une durée de référence pour le début de la diffusion en continu d’un code confidentiel. Lorsque la diffusion en continu commence, le filtre envoie cet événement.

Le paramètre *pSender* spécifie le code confidentiel qui exécute la commande de démarrage. En fonction de l’implémentation, il est possible qu’il ne s’agit pas du code confidentiel qui a reçu l’appel [**startat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) .

Le paramètre *dwCookie* est spécifié par l’application dans la méthode [**startat**](/windows/desktop/api/Strmif/nf-strmif-iamstreamcontrol-startat) . Ce paramètre permet à l’application d’effectuer le suivi de plusieurs appels à la méthode.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>DShow. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Codes de notification d’événement](event-notification-codes.md)
</dt> <dt>

[Notification d’événement dans DirectShow](event-notification-in-directshow.md)
</dt> </dl>

 

 




