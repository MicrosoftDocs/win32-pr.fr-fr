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
ms.openlocfilehash: 6a35bccad8421a47e50e6b7a39e7a259852d90af12452056a604f742ad817d36
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119987689"
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

 

 





