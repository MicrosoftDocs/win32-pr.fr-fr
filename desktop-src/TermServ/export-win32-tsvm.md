---
title: Méthode Export de la classe Win32_TSVm
description: Récupère les informations de surveillance de session de l’ordinateur virtuel.
ms.assetid: 7996651c-aa7c-4fde-84a6-928b27c8c5b8
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode d’exportation
- Méthode d’exportation Services Bureau à distance, classe Win32_TSVm
- Services Bureau à distance de la classe Win32_TSVm, méthode d’exportation
topic_type:
- apiref
api_name:
- Win32_TSVm.Export
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c72d94b24af5563f9cdb668e269c260e8fe19049
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106511933"
---
# <a name="export-method-of-the-win32_tsvm-class"></a>Méthode Export de la \_ classe TSVm Win32

Récupère les informations de surveillance de session de l’ordinateur virtuel.

## <a name="syntax"></a>Syntaxe


```mof
uint32 Export(
  [in]  string ExportFolderPath,
  [out] string ExportJobObjectPath
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ExportFolderPath* \[ dans\]
</dt> <dd>

Chemin d’accès à l’emplacement où l’ordinateur virtuel sera exporté.

</dd> <dt>

*ExportJobObjectPath* \[ à\]
</dt> <dd>

En cas de réussite, retourne le chemin d’accès de l’objet ConcreteJob HyperV.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI. Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) .

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                  |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                             |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                                   |
| MOF<br/>                      | <dl> <dt>TSVmHost. mof</dt> </dl>    |
| DLL<br/>                      | <dl> <dt>TSVmHostWmi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TSVm Win32**](win32-tsvm.md)
</dt> </dl>

 

 





