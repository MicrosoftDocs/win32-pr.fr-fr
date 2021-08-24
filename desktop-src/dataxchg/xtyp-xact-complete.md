---
title: XTYP_XACT_COMPLETE transaction (Ddeml. h)
description: une fonction de rappel client échange dynamique de données (DDE), DdeCallback, reçoit la \_ transaction XTYP XACT \_ complete lorsqu’une transaction asynchrone, initiée par un appel à la fonction DdeClientTransaction, est terminée.
ms.assetid: d34a6fab-0e3c-44fe-b25f-7011228fe261
keywords:
- XTYP_XACT_COMPLETE Exchange de données de transaction
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
ms.openlocfilehash: 2d3833207371bbfab059f67ecb5bdb72b77334ef3ffc73618e013ce137835c6d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119678009"
---
# <a name="xtyp_xact_complete-transaction"></a>\_Transaction XTYP XACT \_ complète

une fonction de rappel client échange dynamique de données (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), reçoit la transaction **XTYP \_ XACT \_ complete** lorsqu’une transaction asynchrone, initiée par un appel à la fonction [**DdeClientTransaction**](/windows/desktop/api/Ddeml/nf-ddeml-ddeclienttransaction) , est terminée.


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

## <a name="remarks"></a>Remarques

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

[bibliothèque de gestion des échange dynamique de données](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

