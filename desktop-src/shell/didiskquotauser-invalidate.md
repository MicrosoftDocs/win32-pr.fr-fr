---
description: Efface les informations utilisateur mises en cache de l’objet.
title: DIDiskQuotaUser. Invalidate, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.Invalidate
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: e0ffd5b7-db1d-40a4-810a-ff43549b0c9b
ms.openlocfilehash: 2b07ae6fd210b8722378a771cda97c2c04572c66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525342"
---
# <a name="didiskquotauserinvalidate-method"></a>DIDiskQuotaUser. Invalidate, méthode

Efface les informations utilisateur mises en cache de l’objet.

## <a name="syntax"></a>Syntaxe


```JScript
DIDiskQuotaUser.Invalidate()
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Cette méthode efface les informations utilisateur stockées dans le cache de l’objet. La prochaine fois qu’une demande est effectuée pour obtenir des informations sur les quotas, l’objet récupère les informations à partir du volume NTFS et actualise le cache.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 5,0 ou ultérieure)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet DIDiskQuotaUser**](didiskquotauser-object.md)
</dt> </dl>

 

 




