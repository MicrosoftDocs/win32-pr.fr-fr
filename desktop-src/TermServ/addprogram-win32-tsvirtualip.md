---
title: Méthode AddProgram de la classe Win32_TSVirtualIP (Bdaiface. h)
description: Ajoute un programme à la liste des programmes qui utilisent la virtualisation IP.
ms.assetid: 4d142774-fa7a-4cfb-9305-5a61b0ef5438
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode AddProgram
- Services Bureau à distance de la méthode AddProgram, classe Win32_TSVirtualIP
- Win32_TSVirtualIP de la classe Services Bureau à distance, méthode AddProgram
topic_type:
- apiref
api_name:
- Win32_TSVirtualIP.AddProgram
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d2f78cb461a61467867a544e954a71c23d59432e29450a7b0f35184f0edec57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117757856"
---
# <a name="addprogram-method-of-the-win32_tsvirtualip-class"></a>Méthode AddProgram de la \_ classe Win32 TSVirtualIP

Ajoute un programme à la liste des programmes qui utilisent la virtualisation IP.

## <a name="syntax"></a>Syntaxe


```mof
uint32 AddProgram(
  [in] string ProgramPath
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*ProgramPath* \[ dans\]
</dt> <dd>

Type : **chaîne**

Chemin d’accès et nom de fichier du programme à ajouter à la liste.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Type : **UInt32**

Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI. Pour obtenir la liste de ces valeurs, reportez-vous à [services Bureau à distance codes d’erreur du fournisseur WMI](terminal-services-wmi-provider-error-codes.md) . La méthode retourne une erreur si le paramètre est sous contrôle de stratégie de groupe.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2<br/>                                                       |
| Espace de noms<br/>                | Racine \\ cimv2 \\ licences TS<br/>                                                |
| En-tête<br/>                   | <dl> <dt>Bdaiface. h</dt> </dl>   |
| MOF<br/>                      | <dl> <dt>TSCfgWmi. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>TSCfgWmi.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_TSVirtualIP Win32**](win32-tsvirtualip.md)
</dt> </dl>

 

 





