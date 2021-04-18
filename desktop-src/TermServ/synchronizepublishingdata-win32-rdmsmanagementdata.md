---
title: Méthode SynchronizePublishingData de la classe Win32_RDMSManagementData
description: Synchronise l’ensemble spécifié de données de publication pour Bureau à distance services de gestion (RDMS).
ms.assetid: 0476ce12-9b08-418c-83c2-208275574f5b
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SynchronizePublishingData
- Services Bureau à distance de la méthode SynchronizePublishingData, classe Win32_RDMSManagementData
- Win32_RDMSManagementData de la classe Services Bureau à distance, méthode SynchronizePublishingData
topic_type:
- apiref
api_name:
- Win32_RDMSManagementData.SynchronizePublishingData
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d389ad08d81f39cab45502a42f4ebd95e16f36c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384556"
---
# <a name="synchronizepublishingdata-method-of-the-win32_rdmsmanagementdata-class"></a>Méthode SynchronizePublishingData de la \_ classe Win32 RDMSManagementData

Synchronise l’ensemble spécifié de données de publication pour Bureau à distance services de gestion (RDMS).

## <a name="syntax"></a>Syntaxe


```mof
uint32 SynchronizePublishingData(
  [in] string Context
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Contexte* \[ dans\]
</dt> <dd>

Informations de contexte des données de publication à synchroniser.

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

[**\_RDMSManagementData Win32**](win32-rdmsmanagementdata.md)
</dt> </dl>

 

 





