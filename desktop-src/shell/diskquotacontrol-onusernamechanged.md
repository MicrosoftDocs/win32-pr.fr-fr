---
description: Se produit lorsque les informations de nom d’un objet DIDiskQuotaUser ont été résolues.
ms.assetid: df32cb17-ad90-4535-a36b-60c5b4e9999f
title: OnUserNameChanged, fonction (dskquota. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OnUserNameChanged
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 02e4227e06d9c9303a5fe9b799afff6e452843bbb7c0dac096b39f925e568d25
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118459892"
---
# <a name="onusernamechanged-function"></a>OnUserNameChanged fonction)

Se produit lorsque les informations de nom d’un objet [**DIDiskQuotaUser**](didiskquotauser-object.md) ont été résolues.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*oUser* 
</dt> <dd>

**Objet** qui prend la valeur de l’objet [**DIDiskQuotaUser**](didiskquotauser-object.md) associé à l’utilisateur dont le nom a été résolu.

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Cette fonction ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Lorsqu’un client [**énumère des utilisateurs**](didiskquotauser-object.md)ou appelle la méthode [**adduser**](diskquotacontrol-adduser.md) ou [**FindUser**](diskquotacontrol-finduser.md) , le nom d’utilisateur doit être résolu à l’ID de sécurité (SID) associé. Étant donné que cette procédure peut prendre du temps, la résolution de noms peut être effectuée de façon asynchrone sur un thread d’arrière-plan. Lorsque le nom d’un utilisateur est résolu, l’objet [**DiskQuotaControl**](diskquotacontrol-object.md) avertit son client en déclenchant l’événement **OnUserNameChanged** . Un objet **DIDiskQuotaUser** associé à l’utilisateur est passé en tant que paramètre. Cet objet permet au client de modifier les paramètres de quota de l’utilisateur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Dskquota. h</dt> </dl>                         |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 5,0 ou ultérieure)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




