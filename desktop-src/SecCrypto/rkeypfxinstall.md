---
description: La fonction RKeyPFXInstall n’est pas prise en charge.
ms.assetid: 061e3d9d-fc92-4204-92f3-f3425afdbe27
title: RKeyPFXInstall, fonction (Rkeysvcc. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RKeyPFXInstall
api_type:
- HeaderDef
api_location:
- Rkeysvcc.h
ms.openlocfilehash: 4908b7224a02f5a28b876b1ff67cbcec7d23df5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103951193"
---
# <a name="rkeypfxinstall-function"></a>RKeyPFXInstall fonction)

La fonction **RKeyPFXInstall** n’est pas prise en charge.

**Windows Server 2003 :** La fonction **RKeyPFXInstall** installe un certificat sur un ordinateur distant. Notez que ce comportement a changé avec Windows Server 2003 avec Service Pack 1 (SP1).

## <a name="syntax"></a>Syntaxe


```C++
ULONG RKeyPFXInstall(
  _In_ KEYSVCC_HANDLE         hKeySvcCli,
  _In_ PKEYSVC_BLOB           pPFX,
  _In_ PKEYSVC_UNICODE_STRING pPassword,
  _In_ ULONG                  ulFlags
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hKeySvcCli* \[ dans\]
</dt> <dd>

Handle [**de \_ handle KEYSVCC**](keysvcc-handle.md) précédemment ouvert par [**RKeyOpenKeyService**](rkeyopenkeyservice.md). Le descripteur représente l’ordinateur distant qui recevra le certificat. Cette valeur ne peut pas être **null**.

</dd> <dt>

*pPFX* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**d' \_ objet BLOB KEYSVC**](keysvc-blob.md) qui représente le certificat à installer. L’objet BLOB est au format [*PKCS \# 12*](../secgloss/p-gly.md) .

</dd> <dt>

*pPassword* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**de \_ \_ chaîne Unicode KEYSVC**](keysvc-unicode-string.md) qui représente le mot de passe pour l’objet BLOB. Lorsque vous avez fini d’utiliser le mot de passe, effacez le mot de passe de la mémoire en appelant la fonction [**SecureZeroMemory**](/previous-versions/windows/desktop/legacy/aa366877(v=vs.85)) . Pour plus d’informations sur la protection des mots de passe, consultez [gestion des mots de passe](../secbp/handling-passwords.md).

</dd> <dt>

*ulFlags* \[ dans\]
</dt> <dd>

Indicateurs qui spécifient les options d’installation du certificat. Ce paramètre peut avoir la valeur zéro ou une combinaison des valeurs suivantes.



| Valeur                                                                                                                                                                                                                                     | Signification                                                                                      |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="CRYPT_EXPORTABLE"></span><span id="crypt_exportable"></span><dl> <dt>**Crypt \_ Exportable**</dt><dt></dt> </dl>              | Les clés importées sont marquées comme étant exportables.<br/>                                           |
| <span id="CRYPT_MACHINE_KEYSET"></span><span id="crypt_machine_keyset"></span><dl> <dt>**Crypt \_ \_jeu de clés**</dt> de l’ordinateur <dt></dt> </dl> | Les clés privées sont stockées sous l’ordinateur distant et non sous l’utilisateur actuel.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction réussit, la valeur de retour est S \_ OK.

Si la fonction échoue, la valeur de retour est un **ULong** qui indique l’erreur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                             |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Rkeysvcc. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**RKeyCloseKeyService**](rkeyclosekeyservice.md)
</dt> <dt>

[**RKeyOpenKeyService**](rkeyopenkeyservice.md)
</dt> </dl>

 

 
