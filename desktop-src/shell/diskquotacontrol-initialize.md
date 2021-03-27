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
ms.openlocfilehash: 919720f01c67b6df3189b760aa8cefbb29615179
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104971959"
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

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                    |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Shell32.dll (version 5,0 ou ultérieure)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet DiskQuotaControl**](diskquotacontrol-object.md)
</dt> </dl>

 

 




