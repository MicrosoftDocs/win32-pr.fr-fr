---
title: Méthode SetProvider de la classe Win32_SessionDirectoryVMMPlugin
description: Définit le nom du fournisseur de plug-ins.
ms.assetid: fefb7c19-2bab-4ae3-b88b-20da5fd19ff3
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetProvider
- Services Bureau à distance de la méthode SetProvider, classe Win32_SessionDirectoryVMMPlugin
- Win32_SessionDirectoryVMMPlugin de la classe Services Bureau à distance, méthode SetProvider
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.SetProvider
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 205a88ecbd67dcf3b009577fa7384e074cc68487
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741477"
---
# <a name="setprovider-method-of-the-win32_sessiondirectoryvmmplugin-class"></a>Méthode SetProvider de la \_ classe Win32 SessionDirectoryVMMPlugin

Définit le nom du fournisseur de plug-ins.

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetProvider(
  [in] string sProvider
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*sProvider* \[ dans\]
</dt> <dd>

Nom du fournisseur de plug-ins.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI. Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                              |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2<br/>                                                      |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                               |
| MOF<br/>                      | <dl> <dt>TssdWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TssdWmi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SessionDirectoryVMMPlugin Win32**](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





