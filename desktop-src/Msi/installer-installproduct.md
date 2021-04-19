---
description: La méthode InstallProduct de l’objet installer ouvre un package d’installation et Initialise une session d’installation.
ms.assetid: 6828ca34-3cf1-4738-882d-9ff1450f1014
title: Installer. InstallProduct, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.InstallProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 08bab1081aae186b40494cff777163679847b44b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106535240"
---
# <a name="installerinstallproduct-method"></a>Installer. InstallProduct, méthode

La méthode **InstallProduct** de l’objet [**installer**](installer-object.md) ouvre un package d’installation et Initialise une session d’installation.

## <a name="syntax"></a>Syntaxe


```JScript
Installer.InstallProduct(
  packagePath,
  propertyValues
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*packagePath* 
</dt> <dd>

Chaîne obligatoire contenant le chemin d’accès au package d’installation.

</dd> <dt>

*propertyValues* 
</dt> <dd>

Chaîne facultative contenant les paires propriété = valeur séparées par un espace blanc.

Pour effectuer une installation administrative, incluez ACTION = ADMIN dans *propertyValues*. Pour plus d’informations, consultez la propriété [**action**](action.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Pour supprimer complètement un produit, définissez REMOVE = ALL dans *propertyValues*. Pour plus d’informations, consultez [**Remove**](remove.md) Property.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




