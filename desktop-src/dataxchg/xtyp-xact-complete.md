---
title: XTYP_XACT_COMPLETE transaction (Ddeml. h)
description: Une fonction de rappel client échange dynamique de données (DDE), DdeCallback, reçoit la \_ transaction XTYP XACT \_ Complete lorsqu’une transaction asynchrone, initiée par un appel à la fonction DdeClientTransaction, est terminée.
ms.assetid: d34a6fab-0e3c-44fe-b25f-7011228fe261
keywords:
- Échange de données de transaction XTYP_XACT_COMPLETE
topic_type:
- apiref
api_name:
- XTYP_XACT_COMPLETE
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 03a81869270a771836c4dd5c1a6b300f148ea13d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106512558"
---
# <a name="xtyp_xact_complete-transaction"></a>\_Transaction XTYP XACT \_ complète

Une fonction de rappel client échange dynamique de données (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), reçoit la transaction **XTYP \_ XACT \_ Complete** lorsqu’une transaction asynchrone, initiée par un appel à la fonction [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) , est terminée.


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYP_XACT_COMPLETE      (0x0080 | XCLASS_NOTIFICATION  )
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*uType* 
</dt> <dd>

Type de transaction.

</dd> <dt>

*uFmt* 
</dt> <dd>

Format des données associées à la transaction terminée (le cas échéant) ou **null** si aucune donnée n’a été échangée pendant la transaction.

</dd> <dt>

*hconv* 
</dt> <dd>

Handle de la conversation.

</dd> <dt>

*hsz1* 
</dt> <dd>

Handle vers le nom de la rubrique impliquée dans la transaction terminée.

</dd> <dt>

*hsz2* 
</dt> <dd>

Handle du nom d’élément impliqué dans la transaction terminée.

</dd> <dt>

*hdata* 
</dt> <dd>

Handle vers les données impliquées dans la transaction terminée, le cas échéant. Si la transaction a réussi, mais n’a impliqué aucune donnée, ce paramètre a la **valeur true**. Ce paramètre a la **valeur null** si la transaction a échoué.

</dd> <dt>

*dwData1* 
</dt> <dd>

Identificateur de la transaction terminée.

</dd> <dt>

*dwData2* 
</dt> <dd>

Tous les indicateurs d’état **DDE \_** applicables dans le mot de poids faible. Ce paramètre fournit la prise en charge des applications dépendantes des bits **\_ APPSTATUS DDE** . Il est recommandé que les applications n’utilisent plus ces bits. elles ne seront peut-être pas prises en charge dans les futures versions du DDEML.

</dd> </dl>

## <a name="remarks"></a>Notes

Une application ne doit pas libérer le descripteur de données obtenu pendant cette transaction. Toutefois, une application doit copier les données associées au descripteur de données si l’application doit traiter les données après le retour de la fonction de rappel. Une application peut utiliser la fonction [**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) pour copier les données.

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

[**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction)
</dt> <dt>

[**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Bibliothèque de gestion des échange dynamique de données](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

