---
title: Méthode RemoveDesktopAssignment de la classe Win32_RDMSDesktopAssignment
description: Supprime une attribution de bureau.
ms.assetid: e1a8cf03-1d21-4bf4-a868-3da4d5bbf43b
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode RemoveDesktopAssignment
- Services Bureau à distance de la méthode RemoveDesktopAssignment, classe Win32_RDMSDesktopAssignment
- Win32_RDMSDesktopAssignment de la classe Services Bureau à distance, méthode RemoveDesktopAssignment
topic_type:
- apiref
api_name:
- Win32_RDMSDesktopAssignment.RemoveDesktopAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6645a79efc970cf7c3288d0765e9aac8cac68a89
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106513830"
---
# <a name="removedesktopassignment-method-of-the-win32_rdmsdesktopassignment-class"></a>Méthode RemoveDesktopAssignment de la \_ classe Win32 RDMSDesktopAssignment

Supprime une attribution de bureau.

## <a name="syntax"></a>Syntaxe


```mof
uint32 RemoveDesktopAssignment(
  [in] string CollectionAlias,
  [in] string DesktopName,
  [in] string UserDomain,
  [in] string UserName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*CollectionAlias* \[ dans\]
</dt> <dd>

Alias de collection.

</dd> <dt>

*DesktopName* \[ dans\]
</dt> <dd>

Nom du bureau.

</dd> <dt>

*UserDomain* \[ dans\]
</dt> <dd>

Nom de domaine du compte d’utilisateur.

</dd> <dt>

*Nom d’utilisateur* \[ dans\]
</dt> <dd>

Nom du compte d’utilisateur.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                   |
| Serveur minimal pris en charge<br/> | Windows Server 2016<br/>                                                              |
| Espace de noms<br/>                | Racine \\ cimv2 cimv2 \\<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_RDMSDesktopAssignment Win32**](win32-rdmsdesktopassignment.md)
</dt> </dl>

 

 





