---
description: Retourne une bitmap UInt32 avec les droits d’accès au partage détenu par l’utilisateur ou le groupe au nom duquel l’instance est retournée.
ms.assetid: 1f656c63-f5ee-4b14-845a-0eb34a0e7a64
ms.tgt_platform: multiple
title: Méthode GetAccessMask de la classe Win32_ClusterShare
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ClusterShare.GetAccessMask
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: db27998c362e3df350dd12b6b91f3966cfc152ae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110510"
---
# <a name="getaccessmask-method-of-the-win32_clustershare-class"></a>Méthode GetAccessMask de la \_ classe Win32 ClusterShare

Retourne une bitmap **UInt32** avec les droits d’accès au partage détenu par l’utilisateur ou le groupe au nom duquel l’instance est retournée.

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetAccessMask();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Droits d’accès au partage détenu par l’utilisateur ou le groupe.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 7<br/>                                                                    |
| Serveur minimal pris en charge<br/> | Windows Server 2008 R2<br/>                                                       |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>Cimwin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_ClusterShare Win32**](win32-clustershare.md)
</dt> </dl>

 

 




