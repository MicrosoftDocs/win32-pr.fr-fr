---
title: XTYP_ADVDATA transaction (Ddeml. h)
description: Informe le client que la valeur de l’élément de données a changé. la fonction de rappel du client échange dynamique de données (DDE), DdeCallback, reçoit cette transaction après avoir établi une boucle de notification avec un serveur.
ms.assetid: c6e61785-b98c-4ffa-9d23-339e1c66cb4d
keywords:
- XTYP_ADVDATA Exchange de données de transaction
topic_type:
- apiref
api_name:
- XTYP_ADVDATA
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8359e34388d185200b5f30c4554e138cc1f6b94a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126852351"
---
# <a name="xtyp_advdata-transaction"></a>\_Transaction ADVDATA XTYP

Informe le client que la valeur de l’élément de données a changé. la fonction de rappel du client échange dynamique de données (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), reçoit cette transaction après avoir établi une boucle de notification avec un serveur.


```C++
#define     XCLASS_FLAGS             0x4000
#define     XTYP_ADVDATA            (0x0010 | XCLASS_FLAGS         )
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*uType* 
</dt> <dd>

Type de transaction.

</dd> <dt>

*uFmt* 
</dt> <dd>

Format Atom des données envoyées à partir du serveur.

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

Handle du nom de l’élément.

</dd> <dt>

*hdata* 
</dt> <dd>

Handle vers les données associées au nom de la rubrique et à la paire de noms d’éléments. Ce paramètre a la **valeur null** si le client a spécifié l’indicateur **\_ NoData XTYPF** lors de la demande de la boucle de notification.

</dd> <dt>

*dwData1* 
</dt> <dd>

Non utilisé.

</dd> <dt>

*dwData2* 
</dt> <dd>

Non utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Une fonction de rappel DDE doit retourner le **\_ Fack DDE** si elle traite cette transaction, **DDE \_ FBUSY** si elle est trop occupée pour traiter cette transaction, ou **DDE \_ FNOTPROCESSED** si elle rejette cette transaction.

## <a name="remarks"></a>Notes

Une application ne doit pas libérer le descripteur de données obtenu pendant cette transaction. Toutefois, une application doit copier les données associées au descripteur de données si l’application doit traiter les données après le retour de la fonction de rappel. Une application peut utiliser la fonction [**DdeGetData**](/windows/desktop/api/Ddeml/nf-ddeml-ddegetdata) pour copier les données.

## <a name="requirements"></a>Spécifications



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

[**DdePostAdvise**](/windows/desktop/api/Ddeml/nf-ddeml-ddepostadvise)
</dt> <dt>

**Conceptuel**
</dt> <dt>

[bibliothèque de gestion des échange dynamique de données](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

