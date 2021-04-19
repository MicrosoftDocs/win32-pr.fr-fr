---
description: La propriété ProductElevated de l’objet installer retourne la valeur true si le produit est managé ou false si le produit n’est pas géré.
ms.assetid: 8126f5a0-751f-46c3-9014-208e9c2db34c
title: Programme d’installation ::P propriété roductElevated
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.ProductElevated
- Installer.get_ProductElevated
- Installer.ProductElevated
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 22591c20cbabfda2eb052e4746e87739b9681804
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106537675"
---
# <a name="installerproductelevated-property"></a>Programme d’installation ::P propriété roductElevated

La propriété **ProductElevated** de l’objet [**installer**](installer-object.md) retourne la valeur true si le produit est managé ou false si le produit n’est pas géré.

Cette propriété est en lecture seule.

## <a name="syntax"></a>Syntaxe


```JScript
propVal = Installer.ProductElevated
```



## <a name="property-value"></a>Valeur de la propriété

GUID du code du produit complet du produit. Ce paramètre est obligatoire.

## <a name="remarks"></a>Notes

La propriété **ProductElevated** utilise la fonction [**MsiIsProductElevated**](/windows/desktop/api/Msi/nf-msi-msiisproductelevateda) . Le retour de la propriété ne prend pas en compte la stratégie [AlwaysInstallElevated a](alwaysinstallelevated.md) .

## <a name="examples"></a>Exemples

L’exemple de script suivant illustre l’utilisation de la propriété **ProductElevated** .


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

' 
' Install Orca tool per-machine
'
installer.InstallProduct "\\products\public\orca\orca.msi", "ALLUSERS=1"

'
' Verify Orca is managed
'

Dim bManaged
bManaged = installer.ProductElevated("{85F4CBCB-9BBC-4B50-A7D8-E1106771498D}")

If bManaged Then
    MsgBox "Success - Product Is Managed"
Else
    MsgBox "Failure - Product Is Not Managed"
End If
```



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer 4,5 sur Windows Server 2003 et Windows XP<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                           |
| IID<br/>     | IID \_ IInstaller est défini en tant que 000C1090-0000-0000-C000-000000000046<br/>                                                                                                                                                                                |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Programme d’installation**](installer-object.md)
</dt> <dt>

[Non pris en charge dans Windows Installer 3,1 et versions antérieures](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 




