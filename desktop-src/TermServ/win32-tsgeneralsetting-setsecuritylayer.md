---
title: Méthode SetSecurityLayer de la classe Win32_TSGeneralSetting
description: La méthode SetSecurityLayer définit la couche de sécurité.
ms.assetid: 3b894494-2180-4f1d-8e67-a66c679d286c
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetSecurityLayer
- Services Bureau à distance de la méthode SetSecurityLayer, classe Win32_TSGeneralSetting
- Win32_TSGeneralSetting de la classe Services Bureau à distance, méthode SetSecurityLayer
topic_type:
- apiref
api_name:
- Win32_TSGeneralSetting.SetSecurityLayer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5e04c3f7e5a58ec8de345d570e36b35c7eb1e7e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942227"
---
# <a name="setsecuritylayer-method-of-the-win32_tsgeneralsetting-class"></a>Méthode SetSecurityLayer de la \_ classe Win32 TSGeneralSetting

La méthode **SetSecurityLayer** définit la couche de sécurité.

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetSecurityLayer(
  [in] uint32 SecurityLayer
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Securitylayer* \[ dans\]
</dt> <dd>

Couche de sécurité à définir. Si le niveau de chiffrement actuel est 1, la valeur 2 pour *securitylayer* n’est pas valide.

<dt>

<span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>

<span id="RDP_Security_Layer"></span><span id="rdp_security_layer"></span><span id="RDP_SECURITY_LAYER"></span>**Couche de sécurité RDP** (0)


</dt> <dd>

La communication entre le serveur et le client utilise le chiffrement RDP natif.

</dd> <dt>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>**Négocier** (1)


</dt> <dd>

La couche la plus sécurisée prise en charge par le client sera utilisée. S’il est pris en charge, SSL (TLS 1,0) sera utilisé.

</dd> <dt>

<span id="SSL"></span><span id="ssl"></span>

<span id="SSL"></span><span id="ssl"></span>**SSL** (2)


</dt> <dd>

SSL (TLS 1,0) sera utilisé pour l’authentification du serveur, ainsi que pour le chiffrement de toutes les données transférées entre le serveur et le client. Ce paramètre requiert que le serveur dispose d’un certificat compatible SSL. Ce paramètre n’est pas compatible avec une valeur **MinEncryptionLevel** de 1.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une réussite en cas de réussite, sinon retourne un code d’erreur WMI. Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .

## <a name="remarks"></a>Notes

Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TSGeneralSetting Win32**](win32-tsgeneralsetting.md)
</dt> <dt>

[**SetEncryptionLevel**](win32-tsgeneralsetting-setencryptionlevel.md)
</dt> </dl>

 

