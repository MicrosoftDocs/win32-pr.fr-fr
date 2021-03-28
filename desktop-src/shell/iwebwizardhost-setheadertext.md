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
ms.openlocfilehash: 92e23fab94cfedd8bbc62e31086759af48238a95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973499"
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

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl> |



 

 
