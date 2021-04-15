---
title: Méthode ProvisioningJobExecute de la classe Win32_RDMSVirtualDesktopCollection
description: Exécute un travail d’approvisionnement de bureau virtuel.
ms.assetid: 69f0cc6a-7eef-4cd9-94ac-f0c7e52d02d8
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode ProvisioningJobExecute
- Services Bureau à distance de la méthode ProvisioningJobExecute, classe Win32_RDMSVirtualDesktopCollection
- Win32_RDMSVirtualDesktopCollection de la classe Services Bureau à distance, méthode ProvisioningJobExecute
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.ProvisioningJobExecute
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c632a6bdc5fc5c4a128941d8a6c8b4379ddf9629
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466743"
---
# <a name="provisioningjobexecute-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Méthode ProvisioningJobExecute de la \_ classe Win32 RDMSVirtualDesktopCollection

Exécute un travail d’approvisionnement de bureau virtuel.

## <a name="syntax"></a>Syntaxe


```mof
uint32 ProvisioningJobExecute(
  [in]  string JobInputXml,
  [out] string JobGuid
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*JobInputXml* \[ dans\]
</dt> <dd>

Chaîne qui contient les informations de configuration au format XML.

</dd> <dt>

*JobGuid* \[ à\]
</dt> <dd>

**GUID** qui identifie de façon unique le travail d’approvisionnement à exécuter.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                   |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                              |
| Espace de noms<br/>                | Racine \\ cimv2 cimv2 \\<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_RDMSVirtualDesktopCollection Win32**](win32-rdmsvirtualdesktopcollection.md)
</dt> </dl>

 

 





