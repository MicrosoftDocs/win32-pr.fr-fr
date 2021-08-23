---
description: Le message SENDDIALOGINSTANCEDATA de la ligne TSPI fait que l’interface \_ TAPI appelle la \_ fonction TUISPI providerGenericDialogData dans la dll de l’interface utilisateur associée à htDlgInst, en lui transmettant le bloc de paramètres vers lequel pointe lpParams, de longueur dwSize nul.
ms.assetid: d3c176ba-8b4b-4b7c-a603-130dfa761898
title: Message LINE_SENDDIALOGINSTANCEDATA (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b955d890c385894467fa0f8f3f93ec50856c746c72f0957ecbe33af203917bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140132"
---
# <a name="line_senddialoginstancedata-message"></a>\_Message SENDDIALOGINSTANCEDATA de ligne

Le message **\_ SENDDIALOGINSTANCEDATA** de la ligne TSPI fait que l’interface TAPI appelle la fonction [**TUISPI \_ providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata) dans la dll de l’interface utilisateur associée à *htDlgInst*, en lui transmettant le bloc de paramètres vers lequel pointe *lpParams, de* longueur *dwSize nul*.


```C++
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*htDlgInst* 
</dt> <dd>

HTAPIDIALOGINSTANCE retourné au fournisseur de services lorsque l’instance de la boîte de dialogue a été créée à l’aide de la [**ligne \_ CREATEDIALOGINSTANCE**](line-createdialoginstance.md).

</dd> <dt>

*lpParams* 
</dt> <dd>

Pointeur vers un bloc de paramètres spécifique au fournisseur qui est transmis à la fonction [**TUISPI \_ providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata) de la dll de l’interface utilisateur, dont la taille est spécifiée par *dwSize nul*. Si ce paramètre a la valeur **null**, il s’agit d’une demande de fermeture immédiate et de nettoyage de la boîte de dialogue (la dll de l’interface utilisateur ne doit pas appeler [**TUISPIDLLCALLBACK**](/windows/win32/api/tspi/nc-tspi-tuispidllcallback) pendant ce nettoyage).

</dd> <dt>

*dwSize nul* 
</dt> <dd>

Taille en octets du bloc de paramètres à transmettre à la DLL de l’interface utilisateur.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TSPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**TUISPIDLLCALLBACK**](/windows/win32/api/tspi/nc-tspi-tuispidllcallback)
</dt> <dt>

[**TUISPI \_ providerGenericDialogData**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialogdata)
</dt> <dt>

[**CREATEDIALOGINSTANCE de ligne \_**](line-createdialoginstance.md)
</dt> </dl>

 

