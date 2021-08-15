---
title: Méthode SetEncryptionLevel de la classe Win32_TSGeneralSetting
description: La méthode SetEncryptionLevel définit le niveau de chiffrement.
ms.assetid: 1822c4dc-bce6-489f-b21e-f96faffd2fa5
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetEncryptionLevel
- Services Bureau à distance de la méthode SetEncryptionLevel, classe Win32_TSGeneralSetting
- Win32_TSGeneralSetting de la classe Services Bureau à distance, méthode SetEncryptionLevel
topic_type:
- apiref
api_name:
- Win32_TSGeneralSetting.SetEncryptionLevel
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a54aacf931a66d6d4bdd4daa24a6432e4caa7fb01695aebbe4324b17ab5f2bed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118348841"
---
# <a name="setencryptionlevel-method-of-the-win32_tsgeneralsetting-class"></a>Méthode SetEncryptionLevel de la \_ classe Win32 TSGeneralSetting

La méthode **SetEncryptionLevel** définit le niveau de chiffrement.

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetEncryptionLevel(
  [in] uint32 MinEncryptionLevel
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*MinEncryptionLevel* \[ dans\]
</dt> <dd>

Niveau de chiffrement minimal à définir.

<dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

Niveau de chiffrement faible. Seules les données envoyées du client au serveur sont chiffrées à l’aide du chiffrement 56 bits. Notez que les données envoyées du serveur au client ne sont pas chiffrées.

</dd> <dt>

<span id="2"></span>

<span id="2"></span>**2**


</dt> <dd>

Niveau de chiffrement compatible avec le client. Toutes les données envoyées du client au serveur et du serveur au client sont chiffrées au niveau de clé maximal pris en charge par le client.

</dd> <dt>

<span id="3"></span>

<span id="3"></span>**1,3**


</dt> <dd>

Niveau élevé de chiffrement. Toutes les données envoyées du client au serveur et du serveur au client sont chiffrées à l’aide d’un chiffrement 128 bits puissant. Les clients qui ne prennent pas en charge ce niveau de chiffrement ne peuvent pas se connecter.

</dd> <dt>

<span id="4"></span>

<span id="4"></span>**4**


</dt> <dd>

Chiffrement conforme à la norme FIPS. Toutes les données envoyées du client au serveur et du serveur au client sont chiffrées et déchiffrées avec les algorithmes de chiffrement normes FIPS (Federal Information Processing Standard) (FIPS) à l’aide des modules de chiffrement Microsoft. FIPS est une norme intitulée « exigences de sécurité pour les modules cryptographiques ». FIPS 140-1 (1994) et FIPS 140-2 (2001) décrivent les exigences gouvernementales pour les modules de chiffrement matériels et logiciels utilisés au sein du gouvernement des États-Unis.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une réussite en cas de réussite, sinon retourne un code d’erreur WMI. Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .

## <a name="remarks"></a>Remarques

les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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
</dt> </dl>

 

