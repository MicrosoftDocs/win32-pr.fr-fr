---
title: Méthode PingSessionDirectory de la classe Win32_TSSessionDirectory
description: Vérifie si le serveur Connexion Bureau à distance Broker (Service Broker pour les connexions Bureau à distance) est disponible.
ms.assetid: 89243998-5ab2-4ea6-aa31-95ec63289055
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode PingSessionDirectory
- Services Bureau à distance de la méthode PingSessionDirectory, classe Win32_TSSessionDirectory
- Win32_TSSessionDirectory de la classe Services Bureau à distance, méthode PingSessionDirectory
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.PingSessionDirectory
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4022a0c34094a19651522c3f8153038c6d9df503
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127008607"
---
# <a name="pingsessiondirectory-method-of-the-win32_tssessiondirectory-class"></a>Méthode PingSessionDirectory de la \_ classe Win32 TSSessionDirectory

Vérifie si le serveur Connexion Bureau à distance Broker (Service Broker pour les connexions Bureau à distance) est disponible.

## <a name="syntax"></a>Syntaxe


```mof
uint32 PingSessionDirectory(
  [in] string ServerName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Nom du serveur* \[ dans\]
</dt> <dd>

Type : **chaîne**

Nom du serveur du Service Broker pour les connexions Bureau à distance.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Type : **UInt32**

Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI. Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .

## <a name="remarks"></a>Notes

les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TSSessionDirectory Win32**](win32-tssessiondirectory.md)
</dt> </dl>

 

