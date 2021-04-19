---
description: La méthode OpenPackage de l’objet installer ouvre un package d’installation à utiliser avec les fonctions qui accèdent à la base de données du produit et au moteur d’installation, en retournant un objet de session.
ms.assetid: 22b03bde-29ae-4dd4-a41c-d55b3a4f424c
title: Installer. OpenPackage, méthode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.OpenPackage
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 621fac51155b2ac89eba40d39da6d5af6c305e67
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106523478"
---
# <a name="installeropenpackage-method"></a>Installer. OpenPackage, méthode

La méthode **OpenPackage** de l’objet [**installer**](installer-object.md) ouvre un package d’installation à utiliser avec les fonctions qui accèdent à la base de données du produit et au moteur d’installation, en retournant un objet de [**session**](session-object.md) .

## <a name="syntax"></a>Syntaxe


```JScript
Installer.OpenPackage(
  packagePath,
  options
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*packagePath* 
</dt> <dd>

Chaîne obligatoire contenant le nom du chemin d’accès du package.

</dd> <dt>

*options* 
</dt> <dd>

Valeur entière facultative qui spécifie si **OpenPackage** doit ignorer l’état actuel de l’ordinateur lors de la création de l’objet de session. Aucune valeur ou valeur de 0 pour les options par défaut est le comportement d’origine. Lorsque l’option Options est 1, la méthode **OpenPackage** ignore l’état actuel de l’ordinateur lors de l’ouverture du package. La valeur 1 empêche toute modification de l’état actuel de l’ordinateur. Pour plus d’informations, consultez [**MsiOpenPackageEx**](/windows/desktop/api/Msi/nf-msi-msiopenpackageexa).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

La méthode **OpenPackage** peut accepter directement le handle de base de données au lieu de la chaîne pour le chemin d’accès au package.

Notez qu’un seul objet de [**session**](session-object.md) peut être ouvert par un processus unique. **OpenPackage** ne peut pas être utilisé dans une action personnalisée, car l’installation active est la seule session autorisée.

Un objet de [**session**](session-object.md) sécurisé ignore l’état actuel de l’ordinateur lors de l’ouverture du package et empêche toute modification de l’état actuel de l’ordinateur. Pour plus d’informations, consultez [**MsiOpenPackageEx**](/windows/desktop/api/Msi/nf-msi-msiopenpackageexa).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer sur Windows Server 2003 ou Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                           |



 

 




