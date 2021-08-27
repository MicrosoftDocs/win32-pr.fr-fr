---
title: Identificateurs des droits d’accès (Fwpmu. h)
description: Windows La plateforme de filtrage (WFP) utilise les droits d’accès Win32 standard, ainsi qu’un ensemble de droits d’accès spécifiques à la plateforme WFP intégrés à la plateforme de filtrage.
ms.assetid: 77f0a1ac-3e99-4cba-a7c6-b8747f35cd0c
topic_type:
- apiref
api_name:
- FWPM_ACTRL_ADD
- FWPM_ACTRL_ADD_LINK
- FWPM_ACTRL_BEGIN_READ_TXN
- FWPM_ACTRL_BEGIN_WRITE_TXN
- FWPM_ACTRL_CLASSIFY
- FWPM_ACTRL_ENUM
- FWPM_ACTRL_OPEN
- FWPM_ACTRL_READ
- FWPM_ACTRL_READ_STATS
- FWPM_ACTRL_SUBSCRIBE
- FWPM_ACTRL_WRITE
- FWPM_GENERIC_READ
- FWPM_GENERIC_EXECUTE
- FWPM_GENERIC_WRITE
- FWPM_GENERIC_ALL
api_location:
- fwpmu.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6deee82b792f525814ac4c841da8a848e4f7b978720755c82f93a9569ba21ca7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118951377"
---
# <a name="access-right-identifiers"></a>Identificateurs des droits d’accès

Windows La plateforme de filtrage (WFP) utilise les [droits d’accès Win32 standard](/windows/desktop/SecAuthZ/standard-access-rights) , ainsi qu’un ensemble de droits d’accès spécifiques à la plateforme WFP intégrés à la plateforme de filtrage. Ces droits d’accès sont utilisés pour sécuriser les objets en mode utilisateur uniquement. Les appelants en mode noyau contournent toutes les vérifications d’accès.

Les identificateurs de droits d’accès spécifiques à WFP sont les suivants.

<dl> <dt>

<span id="FWPM_ACTRL_ADD"></span><span id="fwpm_actrl_add"></span>**FWPM \_ ACTRL \_ Add**
</dt> <dd> <dl> <dt>



Ajoutez un objet au moteur de filtrage de base (BFE). Ce droit d’accès est nécessaire pour appeler les fonctions [**Fwpm \* Add0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmipsectunneladd0) .


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_ADD_LINK"></span><span id="fwpm_actrl_add_link"></span>**FWPM \_ ACTRL \_ Ajouter un \_ lien**
</dt> <dd> <dl> <dt>



Ajoutez un objet référencé via un lien. Par exemple, ce droit d’accès est nécessaire pour les légendes référencées par le biais de GUID.


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_BEGIN_READ_TXN"></span><span id="fwpm_actrl_begin_read_txn"></span>**FWPM \_ ACTRL \_ Begin \_ Read \_ TXN**
</dt> <dd> <dl> <dt>



Commencez une transaction en lecture seule. Ce droit d’accès est nécessaire pour appeler [**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0).


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_BEGIN_WRITE_TXN"></span><span id="fwpm_actrl_begin_write_txn"></span>**FWPM \_ ACTRL \_ Begin \_ Write \_ TXN**
</dt> <dd> <dl> <dt>



Commencer une transaction en lecture/écriture. Ce droit d’accès est nécessaire pour appeler [**FwpmTransactionBegin0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmtransactionbegin0) pour une transaction en lecture/écriture.


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_CLASSIFY"></span><span id="fwpm_actrl_classify"></span>**\_classification FWPM ACTRL \_**
</dt> <dd> <dl> <dt>



Classer l’appel de procédure distante (RPC). Ce droit d’accès est requis par le runtime RPC afin d’appliquer les filtres RPC.


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_ENUM"></span><span id="fwpm_actrl_enum"></span>**FWPM \_ ACTRL, \_ énumération**
</dt> <dd> <dl> <dt>



Énumérer. Ce droit d’accès est nécessaire pour appeler les fonctions [**Fwpm \* CreateEnumHandle0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutcreateenumhandle0) . Pour énumérer un objet, l’appelant a également besoin \_ \_ d’un accès en lecture FWPM ACTRL à l’objet.


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_OPEN"></span><span id="fwpm_actrl_open"></span>**FWPM \_ ACTRL \_ Open**
</dt> <dd> <dl> <dt>



Ouvrez une session sur le moteur de filtre. Ce droit d’accès est nécessaire pour appeler [**FwpmEngineOpen0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmengineopen0).


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_READ"></span><span id="fwpm_actrl_read"></span>**FWPM \_ ACTRL \_ lecture**
</dt> <dd> <dl> <dt>



Lecture. Ce droit d’accès est nécessaire pour appeler les fonctions [**Fwpm \* GetById0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutgetbyid0) et [**Fwpm \* GetByKey0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmcalloutgetbykey0) .


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_READ_STATS"></span><span id="fwpm_actrl_read_stats"></span>**\_statistiques de \_ lecture FWPM ACTRL \_**
</dt> <dd> <dl> <dt>



Lire les statistiques. Ce droit d’accès est nécessaire pour appeler [**IPsecGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ipsecgetstatistics0) et [**IkeextGetStatistics0**](/windows/desktop/api/Fwpmu/nf-fwpmu-ikeextgetstatistics0).


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_SUBSCRIBE"></span><span id="fwpm_actrl_subscribe"></span>**abonnement à FWPM \_ ACTRL \_**
</dt> <dd> <dl> <dt>



Abonnez-vous. Ce droit d’accès est nécessaire pour appeler les fonctions [**Fwpm \* SubscribeChanges0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidersubscribechanges0) . Pour recevoir une notification pour un objet, un abonné a également besoin d’un \_ \_ accès en lecture FWPM ACTRL à l’objet.


</dt> </dl> </dd> <dt>

<span id="FWPM_ACTRL_WRITE"></span><span id="fwpm_actrl_write"></span>**FWPM \_ ACTRL \_ Write**
</dt> <dd> <dl> <dt>



Options du moteur d’écriture. Ce droit d’accès est nécessaire pour appeler [**FwpmEngineSetOption0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmenginesetoption0).


</dt> </dl> </dd> <dt>

<span id="FWPM_GENERIC_READ"></span><span id="fwpm_generic_read"></span>**\_lecture générique \_ FWPM**
</dt> <dd> <dl> <dt>



\_droits standard \_ lire \| FWPM \_ ACTRL \_ Démarrer \_ lire \_ TXN \| FWPM \_ ACTRL \_ classer \| FWPM \_ ACTRL \_ ouvrir \| FWPM \_ ACTRL \_ lire \| FWPM ACTRL \_ lire les \_ \_ statistiques


</dt> </dl> </dd> <dt>

<span id="FWPM_GENERIC_EXECUTE"></span><span id="fwpm_generic_execute"></span>**\_Exécution générique \_ FWPM**
</dt> <dd> <dl> <dt>



\_droits standard \_ exécuter \| FWPM \_ ACTRL \_ enum \| FWPM \_ ACTRL \_ subscribe


</dt> </dl> </dd> <dt>

<span id="FWPM_GENERIC_WRITE"></span><span id="fwpm_generic_write"></span>**\_écriture générique \_ FWPM**
</dt> <dd> <dl> <dt>



droits d’écriture de la \_ \_ \| suppression \| FWPM \_ ACTRL \_ Add \| FWPM \_ ACTRL \_ Ajouter un \_ lien \| FWPM \_ ACTRL \_ commencer l' \_ écriture TXN FWPM \_ \| \_ ACTRL \_ écrire


</dt> </dl> </dd> <dt>

<span id="FWPM_GENERIC_ALL"></span><span id="fwpm_generic_all"></span>**FWPM \_ générique \_ tout**
</dt> <dd> <dl> <dt>



\_droits standard \_ requis \| FWPM \_ ACTRL \_ Add \| FWPM \_ ACTRL \_ Add \_ Link \| FWPM \_ ACTRL \_ Begin \_ Read \_ TXN FWPM ACTRL \| \_ \_ Begin \_ Write \_ TXN \| FWPM \_ ACTRL \_ classifie FWPM \| \_ ACTRL \_ enum \| FWPM \_ ACTRL \_ Open \| FWPM \_ ACTRL \_ lecture FWPM ACTRL lire les \| \_ \_ \_ statistiques \| FWPM \_ ACTRL \_ s’abonner FWPM \| \_ ACTRL \_ Write


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                     |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Fwpmu. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Windows Modèle de Access Control de la plateforme de filtrage](access-control.md)
</dt> <dt>

[Droits d’accès standard](/windows/desktop/SecAuthZ/standard-access-rights)
</dt> </dl>

 

