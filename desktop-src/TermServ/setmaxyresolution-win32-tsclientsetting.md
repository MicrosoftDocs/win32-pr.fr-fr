---
title: Méthode SetMaxYResolution de la classe Win32_TSClientSetting
description: Définit la propriété MaxYResolution.
ms.assetid: a8399c7c-6b3a-464f-8112-8838257ccf06
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetMaxYResolution
- Services Bureau à distance de la méthode SetMaxYResolution, classe Win32_TSClientSetting
- Win32_TSClientSetting de la classe Services Bureau à distance, méthode SetMaxYResolution
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetMaxYResolution
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c85564e075865d993552e831869979fc6227af29
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127228570"
---
# <a name="setmaxyresolution-method-of-the-win32_tsclientsetting-class"></a>Méthode SetMaxYResolution de la \_ classe Win32 TSClientSetting

Définit la propriété **MaxYResolution** .

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetMaxYResolution(
  [in] uint32 MaxYResolution
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*MaxYResolution* \[ dans\]
</dt> <dd>

Nouvelle résolution Y maximale prise en charge par le serveur. La valeur minimale est 200 et la valeur maximale est 2048.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI. Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) . La méthode retourne une erreur si les paramètres de connexion de l’utilisateur sont remplacés par le serveur.

## <a name="requirements"></a>Spécifications



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

 

 





