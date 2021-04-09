---
title: Méthode GetRedirectableAddresses de la classe Win32_TSSessionDirectory
description: Obtient la liste complète des adresses DNS éligibles.
ms.assetid: 828079e7-472c-4428-97a0-2d5dedcdae91
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode GetRedirectableAddresses
- Services Bureau à distance de la méthode GetRedirectableAddresses, classe Win32_TSSessionDirectory
- Win32_TSSessionDirectory de la classe Services Bureau à distance, méthode GetRedirectableAddresses
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.GetRedirectableAddresses
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd5348c11b5f2aba442f7f13ef06488c6d849be3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032378"
---
# <a name="getredirectableaddresses-method-of-the-win32_tssessiondirectory-class"></a>Méthode GetRedirectableAddresses de la \_ classe Win32 TSSessionDirectory

Obtient la liste complète des adresses DNS éligibles.

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetRedirectableAddresses(
  [in]  uint32 fTokenRedirection,
  [out] string IPAddresses[],
  [out] string AdapterNames[],
  [out] string NetConName[]
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*fTokenRedirection* \[ dans\]
</dt> <dd>

Type : **UInt32**

Indicateur qui signale si la redirection des jetons doit être utilisée.

</dd> <dt>

*AdressesIP* \[ à\]
</dt> <dd>

Type : **chaîne \[ \]**

Liste complète des adresses IP disponibles pour la redirection.

</dd> <dt>

*AdapterNames* \[ à\]
</dt> <dd>

Type : **chaîne \[ \]**

Liste des noms de cartes réseau qui sont associés aux adresses disponibles pour la redirection.

</dd> <dt>

*NetConName* \[ à\]
</dt> <dd>

Type : **chaîne \[ \]**

Liste des noms de connexion réseau associés aux adresses disponibles pour la redirection.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI. Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .

## <a name="remarks"></a>Notes

Les fichiers format MOF (MOF) contiennent les définitions des classes Windows Management Instrumentation (WMI). Les fichiers MOF ne sont pas installés dans le cadre du kit de développement logiciel (SDK) Microsoft Windows. Ils sont installés sur le serveur lorsque vous ajoutez le rôle associé à l’aide de l’Gestionnaire de serveur. Pour plus d’informations sur les fichiers MOF, consultez [format MOF (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

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

 

