---
description: Définit le titre et le sous-titre qui s’affichent dans l’en-tête de l’Assistant. En général, le client affiche l’en-tête au-dessus du code HTML et sous la barre de titre.
title: Méthode WebWizardHost. SetHeaderText (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost.SetHeaderText
api_type:
- COM
api_location:
- Shldisp.h
ms.assetid: e627de44-9929-4e08-9fd9-ca22743f434a
ms.openlocfilehash: d97bb8ac1823801257f0ad9f2a737a78bafbf6d724c0f56f3ff0607e498a61bb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117859193"
---
# <a name="webwizardhostsetheadertext-method"></a>Méthode WebWizardHost. SetHeaderText

Définit le titre et le sous-titre qui s’affichent dans l’en-tête de l’Assistant. En général, le client affiche l’en-tête au-dessus du code HTML et sous la barre de titre.

## <a name="syntax"></a>Syntaxe


```JScript
iRetVal = WebWizardHost.SetHeaderText(
  bstrHeaderTitle,
  bstrHeaderSubtitle
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*bstrHeaderTitle* \[ dans\]
</dt> <dd>

Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Chaîne contenant le titre.

</dd> <dt>

*bstrHeaderSubtitle* \[ dans\]
</dt> <dd>

Type : **[ **BSTR**](/previous-versions/windows/desktop/automat/bstr)**

Chaîne contenant le sous-titre.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl> |



 

 
