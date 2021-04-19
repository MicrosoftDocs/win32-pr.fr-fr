---
title: XTYP_ERROR transaction (Ddeml. h)
description: Une fonction de rappel échange dynamique de données (DDE), DdeCallback, reçoit la \_ transaction d’erreur XTYP lorsqu’une erreur critique se produit.
ms.assetid: 710daa04-ed83-42e3-a55e-6ccf891a3d52
keywords:
- Échange de données de transaction XTYP_ERROR
topic_type:
- apiref
api_name:
- XTYP_ERROR
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ebbad80cb23a37881e8954dee4a80a87f253e499
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106530805"
---
# <a name="xtyp_error-transaction"></a>\_Transaction d’erreur XTYP

Une fonction de rappel échange dynamique de données (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), reçoit la transaction d' **\_ erreur XTYP** lorsqu’une erreur critique se produit.


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_ERROR              (0x0000 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK )
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*uType* 
</dt> <dd>

Type de transaction.

</dd> <dt>

*uFmt* 
</dt> <dd>

Non utilisé.

</dd> <dt>

*hconv* 
</dt> <dd>

Handle de la conversation associée à l’erreur. Ce paramètre a la **valeur null** si l’erreur n’est pas associée à une conversation.

</dd> <dt>

*hsz1* 
</dt> <dd>

Non utilisé.

</dd> <dt>

*hsz2* 
</dt> <dd>

Non utilisé.

</dd> <dt>

*hdata* 
</dt> <dd>

Non utilisé.

</dd> <dt>

*dwData1* 
</dt> <dd>

Code d’erreur dans le mot de poids faible. Actuellement, seul le code d’erreur suivant est pris en charge.



| Valeur                                                                                                                                                                      | Signification                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="DMLERR_LOW_MEMORY"></span><span id="dmlerr_low_memory"></span><dl> <dt>**\_mémoire insuffisante DMLERR \_**</dt> </dl> | La mémoire est insuffisante ; les données de notification, d’endiguement ou d’exécution peuvent être perdues ou le système peut échouer.<br/> |



 

</dd> <dt>

*dwData2* 
</dt> <dd>

Non utilisé.

</dd> </dl>

## <a name="remarks"></a>Notes

Une application ne peut pas bloquer ce type de transaction ; le code de retour de **\_ bloc CBR** est ignoré. La DDEML (échange dynamique de données Management Library) tente de libérer de la mémoire en supprimant les ressources non critiques. Une application qui a bloqué les conversations doit les débloquer.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                             |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                   |
| En-tête<br/>                   | <dl> <dt>Ddeml. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Vue d’ensemble de la bibliothèque de gestion échange dynamique de données](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

