---
title: Méthode SetMaxXResolution de la classe Win32_TSClientSetting
description: Définit la propriété MaxXResolution.
ms.assetid: c1e00bab-ab32-4cf6-8121-950184bd8a01
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetMaxXResolution
- Services Bureau à distance de la méthode SetMaxXResolution, classe Win32_TSClientSetting
- Win32_TSClientSetting de la classe Services Bureau à distance, méthode SetMaxXResolution
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetMaxXResolution
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 759a674e2b283d18caf1cc4d1b2f3e3ecae786dc76f9acc222f47dd8daf385de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000509"
---
# <a name="setmaxxresolution-method-of-the-win32_tsclientsetting-class"></a>Méthode SetMaxXResolution de la \_ classe Win32 TSClientSetting

Définit la propriété **MaxXResolution** .

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetMaxXResolution(
  [in] uint32 MaxXResolution
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*MaxXResolution* \[ dans\]
</dt> <dd>

Nouvelle résolution X maximale prise en charge par le serveur. La valeur minimale est 200 et la valeur maximale est 4096.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI. Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) . La méthode retourne une erreur si les paramètres de connexion de l’utilisateur sont remplacés par le serveur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2<br/>                                                       |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                                |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TSClientSetting Win32**](win32-tsclientsetting.md)
</dt> </dl>

 

 





