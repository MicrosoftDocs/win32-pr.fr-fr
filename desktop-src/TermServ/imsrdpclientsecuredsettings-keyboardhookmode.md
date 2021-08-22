---
title: IMsRdpClientSecuredSettings propriété KeyboardHookMode
description: spécifie les paramètres de redirection du clavier, qui spécifient comment et quand appliquer Windows raccourci clavier (par exemple, ALT + TAB).
ms.assetid: 16734580-9be9-476b-b8e7-1eca3ba24d61
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la propriété KeyboardHookMode
- Services Bureau à distance de la propriété KeyboardHookMode, interface IMsRdpClientSecuredSettings
- Services Bureau à distance de l’interface IMsRdpClientSecuredSettings, propriété KeyboardHookMode
topic_type:
- apiref
api_name:
- IMsRdpClientSecuredSettings.KeyboardHookMode
- IMsRdpClientSecuredSettings.get_KeyboardHookMode
- IMsRdpClientSecuredSettings.put_KeyboardHookMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a291eeb26f8011440b8629ed46e1bb12c8b9cfb7adb937d33f80afe60a4d5cd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657589"
---
# <a name="imsrdpclientsecuredsettingskeyboardhookmode-property"></a>IMsRdpClientSecuredSettings :: KeyboardHookMode, propriété

spécifie les paramètres de redirection du clavier, qui spécifient comment et quand appliquer Windows raccourci clavier (par exemple, ALT + TAB).

Cette propriété est en lecture/écriture.

## <a name="syntax"></a>Syntaxe


```C++
HRESULT put_KeyboardHookMode(
  [in]  LONG keyboardHookMode
);

HRESULT get_KeyboardHookMode(
  [out] LONG *pkeyboardHookMode
);
```



## <a name="property-value"></a>Valeur de la propriété

Nouveaux paramètres. Ce paramètre peut prendre les valeurs suivantes.

<dt>

0
</dt> <dd>

Appliquez les combinaisons de touches uniquement localement sur l’ordinateur client.

</dd> <dt>

1
</dt> <dd>

Appliquez des combinaisons de touches au serveur distant.

</dd> <dt>

2
</dt> <dd>

Appliquez des combinaisons de touches au serveur distant uniquement lorsque le client s’exécute en mode plein écran. Il s'agit de la valeur par défaut.

</dd> </dl>

## <a name="error-codes"></a>Codes d’erreur

Retourne **S \_ OK** en cas de réussite.

## <a name="remarks"></a>Remarques

Ces propriétés ne peuvent pas être définies lorsque le contrôle est connecté.

Pour plus d’informations, consultez la rubrique [fourniture de la sécurité du client RDP](providing-for-rdp-client-security.md) .

Pour plus d’informations sur la Connexion Bureau à distance par le Web, consultez [Requirements for connexion Bureau à distance par le Web](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                       |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                                 |
| Bibliothèque de types<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| IID<br/>                      | IID \_ IMsRdpClientSecuredSettings est défini en tant que 605befcf-39c1-45cc-A811-068fb7be346d<br/> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**IMsRdpClientSecuredSettings**](imsrdpclientsecuredsettings-interface.md)
</dt> </dl>

 

 





