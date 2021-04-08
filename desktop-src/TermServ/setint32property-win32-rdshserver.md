---
title: Méthode SetInt32Property de la classe Win32_RDSHServer
description: Met à jour une valeur de propriété entière d’un \_ objet Win32 RDSHServer.
ms.assetid: fa8df023-120d-4174-adc1-868f08fdce56
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode SetInt32Property
- Services Bureau à distance de la méthode SetInt32Property, classe Win32_RDSHServer
- Win32_RDSHServer de la classe Services Bureau à distance, méthode SetInt32Property
topic_type:
- apiref
api_name:
- Win32_RDSHServer.SetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66c22c8da9c046e0a42a6ec41f6ad5b3073c8d1f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741300"
---
# <a name="setint32property-method-of-the-win32_rdshserver-class"></a>Méthode SetInt32Property de la \_ classe Win32 RDSHServer

Met à jour une valeur de propriété entière d’un objet [**Win32 \_ RDSHServer**](win32-rdshserver.md) .

## <a name="syntax"></a>Syntaxe


```mof
uint32 SetInt32Property(
  [in] string Key,
  [in] sint32 Value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Clé* \[ dans\]
</dt> <dd>

Clé qui identifie la propriété à mettre à jour.

</dd> <dt>

*Valeur* \[ dans\]
</dt> <dd>

Nouvelle valeur de la propriété.

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

[**\_RDSHServer Win32**](win32-rdshserver.md)
</dt> </dl>

 

 





