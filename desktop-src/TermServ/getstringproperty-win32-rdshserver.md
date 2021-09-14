---
title: Méthode GetStringProperty de la classe Win32_RDSHServer
description: Récupère une valeur de propriété de type chaîne d’un \_ objet Win32 RDSHServer.
ms.assetid: 136cd213-86a6-472a-8853-8d05f992309a
ms.tgt_platform: multiple
keywords:
- GetStringProperty, méthode Services Bureau à distance
- Méthode GetStringProperty Services Bureau à distance, classe Win32_RDSHServer
- Win32_RDSHServer de la classe Services Bureau à distance, méthode GetStringProperty
topic_type:
- apiref
api_name:
- Win32_RDSHServer.GetStringProperty
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 619a034e0a2f89270d21bf0c4fc297b4248cef59
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127324675"
---
# <a name="getstringproperty-method-of-the-win32_rdshserver-class"></a>Méthode GetStringProperty de la \_ classe RDSHServer Win32

Récupère une valeur de propriété de type chaîne d’un objet [**Win32 \_ RDSHServer**](win32-rdshserver.md) .

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetStringProperty(
  [in]  string Key,
  [out] string Value
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Clé* \[ dans\]
</dt> <dd>

Clé qui identifie la propriété à récupérer.

</dd> <dt>

*Valeur* \[ à\]
</dt> <dd>

Reçoit la valeur de la propriété récupérée.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.

## <a name="requirements"></a>Spécifications



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

 

 





