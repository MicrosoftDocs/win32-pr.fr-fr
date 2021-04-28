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
ms.openlocfilehash: aae44918b51331363c6750e269019b5c4d6d6883
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108089557"
---
# <a name="getaccessmask-method-of-the-win32_clustershare-class"></a>Méthode GetAccessMask de la \_ classe Win32 ClusterShare

Retourne une bitmap **UInt32** avec les droits d’accès au partage détenu par l’utilisateur ou le groupe au nom duquel l’instance est retournée.

## <a name="syntax"></a>Syntaxe


```mof
uint32 GetAccessMask();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur renvoyée

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

 

 




