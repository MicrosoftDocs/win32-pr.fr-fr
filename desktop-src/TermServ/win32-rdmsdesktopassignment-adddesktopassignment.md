---
title: Méthode AddDesktopAssignment de la classe Win32_RDMSDesktopAssignment
description: Ajoutez une attribution de bureau.
ms.assetid: 3690f70e-d0c3-444a-a0b7-cec6994eb3b8
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode AddDesktopAssignment
- Services Bureau à distance de la méthode AddDesktopAssignment, classe Win32_RDMSDesktopAssignment
- Win32_RDMSDesktopAssignment de la classe Services Bureau à distance, méthode AddDesktopAssignment
topic_type:
- apiref
api_name:
- Win32_RDMSDesktopAssignment.AddDesktopAssignment
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 571273e76b0bb45b748f1587e5a831fcf1e36b0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843398"
---
# <a name="adddesktopassignment-method-of-the-win32_rdmsdesktopassignment-class"></a>Méthode AddDesktopAssignment de la \_ classe Win32 RDMSDesktopAssignment

Ajouter une attribution de bureau

## <a name="syntax"></a>Syntaxe


```mof
uint32 AddDesktopAssignment(
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

 

 





