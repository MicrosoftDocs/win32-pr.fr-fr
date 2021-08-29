---
description: La propriété ProductInfoFromScript de l’objet installer retourne la valeur de l’attribut spécifié qui est stocké dans un script de publication.
ms.assetid: 92aa479b-2b4c-482c-a186-a290461bc6d8
title: Programme d’installation ::P propriété roductInfoFromScript
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductInfoFromScript
- Installer.put_ProductInfoFromScript
- Installer.ProductInfoFromScript
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 7b0319c83cc981f36bc4d744bb34e96a684adf8d203bdf4f4dc6ab8472033639
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129369"
---
# <a name="installerproductinfofromscript-property"></a>Programme d’installation ::P propriété roductInfoFromScript

La propriété **ProductInfoFromScript** de l’objet [**installer**](installer-object.md) retourne la valeur de l’attribut spécifié qui est stocké dans un script de publication.

Cette propriété est en écriture seule.

## <a name="syntax"></a>Syntaxe


```JScript
Installer.ProductInfoFromScript = propVal 
```



## <a name="property-value"></a>Valeur de la propriété

## <a name="error-codes"></a>Codes d’erreur

Valeur de chaîne ou d’entier en fonction de l’attribut demandé.

## <a name="remarks"></a>Remarques

La propriété **ProductInfoFromScript** utilise la fonction [**MsiGetProductInfoFromScript**](/windows/desktop/api/Msi/nf-msi-msigetproductinfofromscripta) .

## <a name="examples"></a>Exemples

L’exemple de script suivant illustre l’utilisation de la propriété **ProductInfoFromScript** .


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

' 
' Create an advertise script for Orca
'

installer.CreateAdvertiseScript "\\products\public\orca\orca.msi", "c:\scratch\orca.aas"

' 
' Output ProductName Information From Script
'

MsgBox  installer.ProductInfoFromScript("c:\scratch\orca.aas", 3)
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows programme d’installation 4,5 sur Windows Server 2003 et Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                           |
| IID<br/>     | IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Programme d’installation**](installer-object.md)
</dt> <dt>

[non pris en charge dans Windows Installer 3,1 et versions antérieures](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




