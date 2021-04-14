---
title: XTYP_ADVREQ transaction (Ddeml. h)
description: La \_ transaction XTYP ADVREQ informe le serveur qu’une transaction de notification est en suspens sur le nom de rubrique et la paire de noms d’éléments spécifiés et que les données correspondant à la paire nom de la rubrique et nom de l’élément ont changé.
ms.assetid: 9bd43e61-cbd6-4d53-bab3-90e85819b16b
keywords:
- Échange de données de transaction XTYP_ADVREQ
topic_type:
- apiref
api_name:
- XTYP_ADVREQ
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2884e838268342ab10c556c6ae3cfc8349ed5d2c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384783"
---
# <a name="xtyp_advreq-transaction"></a>\_Transaction ADVREQ XTYP

La transaction **XTYP \_ ADVREQ** informe le serveur qu’une transaction de notification est en suspens sur le nom de rubrique et la paire de noms d’éléments spécifiés et que les données correspondant à la paire nom de la rubrique et nom de l’élément ont changé. Le système envoie cette transaction à la fonction de rappel échange dynamique de données (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), une fois que le serveur a appelé la fonction [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) .


```C++
#define     XCLASS_DATA              0x2000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_ADVREQ             (0x0020 | XCLASS_DATA | XTYPF_NOBLOCK )
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*uType* 
</dt> <dd>

Type de transaction.

</dd> <dt>

*uFmt* 
</dt> <dd>

Format dans lequel les données doivent être envoyées au client.

</dd> <dt>

*hconv* 
</dt> <dd>

Handle de la conversation.

</dd> <dt>

*hsz1* 
</dt> <dd>

Handle vers le nom de la rubrique.

</dd> <dt>

*hsz2* 
</dt> <dd>

Handle du nom de l’élément qui a changé.

</dd> <dt>

*hdata* 
</dt> <dd>

Non utilisé.

</dd> <dt>

*dwData1* 
</dt> <dd>

Nombre, dans le mot de poids faible, des transactions **XTYP \_ ADVREQ** qui restent à traiter sur la même rubrique, le même élément et le même nom de format définis dans le contexte de l’appel actuel à la fonction [**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise) . Le nombre est égal à zéro si la transaction **XTYP \_ ADVREQ** actuelle est la dernière. Un serveur peut utiliser ce nombre pour déterminer s’il faut créer un descripteur de données **HDATA \_ APPOWNED** pour les données de notification.

Le mot de poids faible est défini sur **CADV \_ LATEACK** si le Ddeml a émis la transaction **XTYP \_ ADVREQ** en raison d’un message d’accusé de réception DDE \_ d’un client Outrun par le serveur.

Le mot de poids fort n’est pas utilisé.

</dd> <dt>

*dwData2* 
</dt> <dd>

Non utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Le serveur doit d’abord appeler la fonction [**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle) pour créer un handle de données qui identifie les données modifiées, puis retourner le descripteur. Le serveur doit retourner la **valeur null** s’il ne parvient pas à terminer la transaction.

## <a name="remarks"></a>Notes

Un serveur ne peut pas bloquer ce type de transaction ; le code de retour de **\_ bloc CBR** est ignoré.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                   |
| En-tête<br/>                   | <dl> <dt>Ddeml. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**DdeCreateDataHandle**](/windows/desktop/api/Ddeml/nf-ddeml-ddecreatedatahandle)
</dt> <dt>

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Bibliothèque de gestion des échange dynamique de données](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

