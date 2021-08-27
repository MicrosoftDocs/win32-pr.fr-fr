---
description: La méthode OpenProduct de l’objet installer ouvre un package d’installation pour un produit installé à l’aide du code de produit et retourne un objet de session.
ms.assetid: f09c4795-19e1-4474-b7ca-68ef650b69d5
title: Installer. OpenProduct, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.OpenProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3aa6176b297261968a63b2f723a65ea14b45b8d3628b200be92df556adc5c2b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129379"
---
# <a name="installeropenproduct-method"></a>Installer. OpenProduct, méthode

La méthode **OpenProduct** de l’objet [**installer**](installer-object.md) ouvre un package d’installation pour un produit installé à l’aide du code de produit et retourne un objet de [**session**](session-object.md) .

## <a name="syntax"></a>Syntaxe


```JScript
Installer.OpenProduct(
  productCode
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*productCode* 
</dt> <dd>

Chaîne obligatoire contenant le code de produit unique ( [GUID](guid.md)) ou un descripteur d’activation écrit par le programme d’installation.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Notez qu’un seul objet de [**session**](session-object.md) peut être ouvert par un processus unique. **OpenProduct** ne peut pas être utilisé dans une action personnalisée, car l’installation active est la seule session autorisée.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




