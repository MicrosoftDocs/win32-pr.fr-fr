---
title: Méthode SelectNetworkAdapterIP de la classe Win32_TSNetworkAdapterSetting
description: Sélectionne une carte réseau en fonction de l’adresse IP de la carte.
ms.assetid: 7f89fb83-8abe-421b-a48b-876c093e3a3d
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SelectNetworkAdapterIP
- Services Bureau à distance de la méthode SelectNetworkAdapterIP, classe Win32_TSNetworkAdapterSetting
- Win32_TSNetworkAdapterSetting de la classe Services Bureau à distance, méthode SelectNetworkAdapterIP
topic_type:
- apiref
api_name:
- Win32_TSNetworkAdapterSetting.SelectNetworkAdapterIP
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb4a88c4820e4537d9c0fb1833b67eb2660a7fb5618189023dfe2217f222efa1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008369"
---
# <a name="selectnetworkadapterip-method-of-the-win32_tsnetworkadaptersetting-class"></a>Méthode SelectNetworkAdapterIP de la \_ classe Win32 TSNetworkAdapterSetting

Sélectionne une carte réseau en fonction de l’adresse IP de la carte.

## <a name="syntax"></a>Syntaxe


```mof
uint32 SelectNetworkAdapterIP(
  [in] string NetworkAdapterIP
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*NetworkAdapterIP* \[ dans\]
</dt> <dd>

Adresse IP de la carte réseau à définir.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne zéro si l’adresse IP spécifiée est valide et retourne un code d’erreur WMI si l’adresse IP n’est pas valide ou n’existe pas. Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .

## <a name="remarks"></a>Remarques

Vous pouvez récupérer l’adresse IP d’une carte réseau en énumérant les propriétés de la classe [**Win32 \_ TSNetworkAdapterListSetting**](win32-tsnetworkadapterlistsetting.md) .

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

[**\_TSNetworkAdapterSetting Win32**](win32-tsnetworkadaptersetting.md)
</dt> </dl>

 

