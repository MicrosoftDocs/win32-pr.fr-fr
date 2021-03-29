---
description: Met à jour les boutons précédent, suivant et terminer dans le frame de l’Assistant du client.
title: Méthode WebWizardHost. SetWizardButtons (shldisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WebWizardHost.SetWizardButtons
api_type:
- COM
api_location:
- Shldisp.h
ms.assetid: 863aa667-454c-40cd-8091-9bb456047b6c
ms.openlocfilehash: 18af31eac1042e84a41e5651c517279869f03697
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973498"
---
# <a name="webwizardhostsetwizardbuttons-method"></a>Méthode WebWizardHost. SetWizardButtons

Met à jour les boutons **précédent**, **suivant** et **Terminer** dans le frame de l’Assistant du client.

## <a name="syntax"></a>Syntaxe


```JScript
iRetVal = WebWizardHost.SetWizardButtons(
  vbEnableBack,
  vbEnableNext,
  vbLastPage
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*vbEnableBack* \[ dans\]
</dt> <dd>

Type : **booléen**

Active le bouton **précédent** .

</dd> <dt>

*vbEnableNext* \[ dans\]
</dt> <dd>

Type : **booléen**

Active le bouton **Suivant**.

</dd> <dt>

*vbLastPage* \[ dans\]
</dt> <dd>

Type : **booléen**

Active le bouton **Terminer** . Indique qu’il s’agit de la dernière page côté serveur.

</dd> </dl>

## <a name="remarks"></a>Notes

Veillez à implémenter des fonctions de gestionnaire dans chaque page côté serveur pour OnBack () et OnNext (), correspondant aux boutons d’Assistant **précédent** et **suivant**. Les fonctions OnBack () et OnNext () répondent à **SetWizardButtons**. Au moment opportun, la fonction OnNext () appelle **SetWizardButtons** avec *vbLastPage* = **true**, qui peut activer un bouton **Terminer** . OnNext () appelle également [**FinalNext**](iwebwizardhost-finalnext.md) quand un utilisateur clique sur le bouton **Terminer** .

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                   |
| En-tête<br/>                   | <dl> <dt>Shldisp. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Shldisp. idl</dt> </dl> |



 

 




