---
title: Méthode AddVirtualDesktop de la classe Win32_RDMSVirtualDesktopCollection
description: Ajoute un bureau virtuel à la collection de bureaux virtuels.
ms.assetid: 31a3aa28-6e5d-4f8a-81ff-ab011f568b6a
ms.tgt_platform: multiple
keywords:
- Services Bureau à distance de la méthode AddVirtualDesktop
- Services Bureau à distance de la méthode AddVirtualDesktop, classe Win32_RDMSVirtualDesktopCollection
- Win32_RDMSVirtualDesktopCollection de la classe Services Bureau à distance, méthode AddVirtualDesktop
topic_type:
- apiref
api_name:
- Win32_RDMSVirtualDesktopCollection.AddVirtualDesktop
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4858f99f2ea4793fe0d83d06a0aaa429b7aa8f71
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508389"
---
# <a name="addvirtualdesktop-method-of-the-win32_rdmsvirtualdesktopcollection-class"></a>Méthode AddVirtualDesktop de la \_ classe Win32 RDMSVirtualDesktopCollection

Ajoute un bureau virtuel à la collection de bureaux virtuels.

## <a name="syntax"></a>Syntaxe


```mof
uint32 AddVirtualDesktop(
  [in] string VMName
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Vmname* \[ dans\]
</dt> <dd>

Nom de la machine virtuelle qui héberge le bureau virtuel.

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

 

 





