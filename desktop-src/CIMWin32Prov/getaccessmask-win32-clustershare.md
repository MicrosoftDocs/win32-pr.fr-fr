---
description: La méthode GetAccessMask de la classe Win32_ClusterShare-retourne une bitmap UInt32 avec les droits d’accès au partage détenu par l’utilisateur ou le groupe au nom duquel l’instance est retournée.
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
ms.openlocfilehash: 20c78fae9e66ad07224c96ee39ee9e99bf3b5396b4db05796feec97cc3e3db5b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120077639"
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

 

 




