---
description: Ouvre un volume spécifié et initialise son objet de contrôle de quota.
ms.assetid: 20eae2a3-f602-48a2-bf1c-65570e7a5d21
title: DiskQuotaControl.Iniméthode tialize
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.Initialize
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 0df879c626ccdac7494077f021c23a6e42b24f0df3aa780d1be8b1af8225527a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119455899"
---
# <a name="diskquotacontrolinitialize-method"></a>DiskQuotaControl.Iniméthode tialize

Ouvre un volume spécifié et initialise son objet de contrôle de quota.

## <a name="syntax"></a>Syntaxe


```JScript
DiskQuotaControl.Initialize(
  sPath,
  bReadWrite
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*sPath* 
</dt> <dd>

Type : **chaîne**

Valeur de chaîne qui contient le chemin d’accès qualifié complet du volume à initialiser.

</dd> <dt>

*bReadWrite* 
</dt> <dd>

Type : **booléen**

Valeur booléenne qui spécifie le mode d’ouverture du volume. Affectez la valeur **true** à *bReadWrite* pour l’accès en lecture/écriture ou **false** pour l’accès en lecture seule.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 5,0 ou ultérieure)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




