---
title: Méthode SetCurrentRedirectableAddresses de la classe Win32_TSSessionDirectory
description: Définit la liste configurée des adresses DNS éligibles qui peuvent être utilisées pour la redirection.
ms.assetid: cad6a8a8-fdf1-406e-abeb-37acb396ac16
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetCurrentRedirectableAddresses
- Services Bureau à distance de la méthode SetCurrentRedirectableAddresses, classe Win32_TSSessionDirectory
- Win32_TSSessionDirectory de la classe Services Bureau à distance, méthode SetCurrentRedirectableAddresses
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetCurrentRedirectableAddresses
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1cf1e9ab7b385111ccf91af9b4e3d6ed8bed0191f2d044c02a41705dbbc4f781
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117756099"
---
# <a name="setcurrentredirectableaddresses-method-of-the-win32_tssessiondirectory-class"></a>Méthode SetCurrentRedirectableAddresses de la \_ classe Win32 TSSessionDirectory

La méthode **SetCurrentRedirectableAddresses** définit la liste configurée des adresses DNS éligibles qui peuvent être utilisées pour la redirection.

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetCurrentRedirectableAddresses(
  [in] uint32 fTokenRedirection,
  [in] string IPAddresses[]
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*fTokenRedirection* \[ dans\]
</dt> <dd>

Type : **UInt32**

Indicateur qui signale si la redirection des jetons doit être utilisée.

</dd> <dt>

*AdressesIP* \[ dans\]
</dt> <dd>

Type : **chaîne \[ \]**

Tableau de chaînes qui représente la liste des adresses IP éligibles DNS qui peuvent être utilisées pour la redirection.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Retourne 0 en cas de réussite ; Sinon, retourne un code d’erreur WMI. Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .

## <a name="remarks"></a>Remarques

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

 

