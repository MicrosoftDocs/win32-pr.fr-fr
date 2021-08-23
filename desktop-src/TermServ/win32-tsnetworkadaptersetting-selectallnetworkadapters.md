---
title: Méthode SelectAllNetworkAdapters de la classe Win32_TSNetworkAdapterSetting
description: La méthode SelectAllNetworkAdapters sélectionne toutes les cartes réseau.
ms.assetid: e0bd60c3-55c3-4be9-be2d-3b97db3047d9
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SelectAllNetworkAdapters
- Services Bureau à distance de la méthode SelectAllNetworkAdapters, classe Win32_TSNetworkAdapterSetting
- Win32_TSNetworkAdapterSetting de la classe Services Bureau à distance, méthode SelectAllNetworkAdapters
topic_type:
- apiref
api_name:
- Win32_TSNetworkAdapterSetting.SelectAllNetworkAdapters
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a359e3ea87c1c2f4567e752a714741c0f2617304f8d261e0baf811794d788895
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119420519"
---
# <a name="selectallnetworkadapters-method-of-the-win32_tsnetworkadaptersetting-class"></a>Méthode SelectAllNetworkAdapters de la \_ classe Win32 TSNetworkAdapterSetting

La méthode **SelectAllNetworkAdapters** sélectionne toutes les cartes réseau.

## <a name="syntax"></a>Syntaxe


```mof
uint32 SelectAllNetworkAdapters();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI. Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .

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

[**\_TSNetworkAdapterSetting Win32**](win32-tsnetworkadaptersetting.md)
</dt> </dl>

 

