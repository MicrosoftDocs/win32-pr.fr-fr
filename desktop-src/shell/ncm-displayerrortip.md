---
description: Affiche un message d’erreur dans l’info-bulle associée au contrôle d’adresse réseau.
title: Message NCM_DISPLAYERRORTIP (shellapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 5ECAB6C3-69FC-4f2a-A9E6-80BC37ED3119
api_name:
- NCM_DISPLAYERRORTIP
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 8a3968b9001d74721938190369e6b52cf2368835
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104991112"
---
# <a name="ncm_displayerrortip-message"></a>\_Message NCM DISPLAYERRORTIP

Affiche un message d’erreur dans l’info-bulle associée au contrôle d’adresse réseau.


```C++
NCM_DISPLAYERRORTIP

    wParam = 0;

    lParam = 0;            

            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>Doit être zéro.</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si ce message est correctement exécuté, il renvoie la valeur **\_ OK**. Sinon, elle retourne un code d’erreur **HRESULT** .

## <a name="remarks"></a>Notes

Envoyer ce message pour afficher un message d’erreur quand une adresse tapée dans le contrôle n’est pas validée par rapport aux types d’adresses réseau autorisés définis avec le message [**NCM \_ SETALLOWTYPE**](ncm-setallowtype.md) . Utilisez le message [**NCM \_ GETADDRESS**](ncm-getaddress.md) pour valider l’adresse.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Shellapi. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**DisplayErrorTip NETADDR \_**](/windows/desktop/api/Shellapi/nf-shellapi-netaddr_displayerrortip)
</dt> </dl>

 

 




