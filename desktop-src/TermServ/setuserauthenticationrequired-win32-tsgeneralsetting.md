---
title: Méthode SetUserAuthenticationRequired de la classe Win32_TSGeneralSetting
description: Active ou désactive l’exigence selon laquelle les utilisateurs doivent être authentifiés au moment de la connexion en définissant la valeur de la propriété UserAuthenticationRequired.
ms.assetid: a0581326-fecc-4d23-87bf-3696c93366e8
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetUserAuthenticationRequired
- Services Bureau à distance de la méthode SetUserAuthenticationRequired, classe Win32_TSGeneralSetting
- Win32_TSGeneralSetting de la classe Services Bureau à distance, méthode SetUserAuthenticationRequired
topic_type:
- apiref
api_name:
- Win32_TSGeneralSetting.SetUserAuthenticationRequired
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b39c0eb711d2146130ff0fd879953fc71fcba965
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317429"
---
# <a name="setuserauthenticationrequired-method-of-the-win32_tsgeneralsetting-class"></a>Méthode SetUserAuthenticationRequired de la \_ classe Win32 TSGeneralSetting

Active ou désactive la spécification selon laquelle les utilisateurs doivent être authentifiés au moment de la connexion en définissant la valeur de la propriété **UserAuthenticationRequired** dans la classe [**\_ TSGeneralSetting Win32**](win32-tsgeneralsetting.md) . Si la **valeur est true**, ce qui signifie qu’elle est activée, **UserAuthenticationRequired** nécessite l’authentification de l’utilisateur au moment de la connexion pour augmenter la protection du serveur contre les attaques réseau. Seuls les clients protocole RDP (Remote Desktop Protocol) (RDP) qui prennent en charge le protocole RDP version 6,0 ou une version ultérieure sont en mesure de se connecter. Pour éviter les interruptions pour les utilisateurs distants, il est recommandé de déployer les clients RDP qui prennent en charge la version de protocole appropriée avant d’activer la propriété.

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetUserAuthenticationRequired(
  [in] uint32 UserAuthenticationRequired
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*UserAuthenticationRequired* \[ dans\]
</dt> <dd>

Indique si l’authentification de l’utilisateur est requise.

<dt>

0 (0x0)
</dt> <dd>

Désactiver l’exigence selon laquelle l’utilisateur doit être authentifié

</dd> <dt>

1 (0x1)
</dt> <dd>

Permet d’exiger l’authentification de l’utilisateur.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI. Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .

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
</dt> </dl>

 

