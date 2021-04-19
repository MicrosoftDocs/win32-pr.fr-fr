---
description: La méthode AdvertiseProduct de l’objet installer publie un package d’installation.
ms.assetid: a060ccb5-353f-439b-8d48-709c81da5f2c
title: 'Installer :: AdvertiseProduct, méthode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Installer.AdvertiseProduct
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 8f8e0f92079e1eb5d2690b61acafdefb2f777b2a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528528"
---
# <a name="installeradvertiseproduct-method"></a>Installer :: AdvertiseProduct, méthode

La méthode **AdvertiseProduct** de l’objet [**installer**](installer-object.md) publie un package d’installation.

## <a name="syntax"></a>Syntaxe


```JScript
.AdvertiseProduct(
  packagePath,
  context,
  transforms,
  language,
  options
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*packagePath* 
</dt> <dd>

Chemin d’accès complet au package de Windows Installer (. msi) à publier.

</dd> <dt>

*context* 
</dt> <dd>

Contexte de la publication. Ce paramètre peut prendre les valeurs suivantes.



| Valeur                                                                                                                                                                                                                                                                                                   | Signification                                                                                                                                                                                                       |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiAdvertiseProductMachine"></span><span id="msiadvertiseproductmachine"></span><span id="MSIADVERTISEPRODUCTMACHINE"></span><dl> <dt>**msiAdvertiseProductMachine**</dt> <dt>0</dt> </dl> | Publie l’application pour une installation dans le [contexte d’installation](installation-context.md)par ordinateur. Cela rend le package disponible pour l’installation par tous les utilisateurs de l’ordinateur.<br/> |
| <span id="msiAdvertiseProductUser"></span><span id="msiadvertiseproductuser"></span><span id="MSIADVERTISEPRODUCTUSER"></span><dl> <dt>**msiAdvertiseProductUser**</dt> <dt>1</dt> </dl>             | Publie l’application pour une installation dans le [contexte d’installation](installation-context.md)par utilisateur.<br/>                                                                                   |



 

</dd> <dt>

*transformations* 
</dt> <dd>

Liste des transformations à appliquer au produit. Les transformations de la liste sont délimitées par des points-virgules. Ce paramètre est facultatif.

</dd> <dt>

*language* 
</dt> <dd>

Langue du package d’installation à utiliser. Ce paramètre est facultatif.

</dd> <dt>

*options* 
</dt> <dd>

Options de publication. Ce paramètre est facultatif. Ce paramètre peut prendre les valeurs suivantes.



| Valeur                                                                                                                                                                                                                                                                                                   | Signification                                                                                                                                                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="msiAdvertiseDefault"></span><span id="msiadvertisedefault"></span><span id="MSIADVERTISEDEFAULT"></span><dl> <dt>**msiAdvertiseDefault**</dt> <dt>0</dt> </dl>                             | Publication standard<br/>                                                                                                                                                                                                                                                                                                                 |
| <span id="msiAdvertiseSingleInstance"></span><span id="msiadvertisesingleinstance"></span><span id="MSIADVERTISESINGLEINSTANCE"></span><dl> <dt>**msiAdvertiseSingleInstance**</dt> <dt>1</dt> </dl> | Publie une nouvelle instance du produit. Requiert que la première transformation de la liste transformer du paramètre *transformations* soit la transformation d’instance qui modifie le code du produit. Pour plus d’informations, consultez [installation de plusieurs instances de produits et de correctifs](installing-multiple-instances-of-products-and-patches.md).<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

La méthode **AdvertiseProduct** utilise la fonction [**MsiAdvertiseProductEx**](/windows/desktop/api/Msi/nf-msi-msiadvertiseproductexa) .

## <a name="examples"></a>Exemples

L’exemple suivant illustre l’utilisation de la méthode **AdvertiseProduct** .


```VB
Dim installer
Set installer = CreateObject("WindowsInstaller.Installer")

'
' Perform machine advertisement of package, use transform
'

Installer.AdvertiseProduct "c:\scratch\simpletst\rtm\simple.msi", 0, "c:\scratch\simpletst\rtm\transform.mst"

'
' Verify advertised product state and registration
'
 
MsgBox Installer.ProductState("{BAE98781-CF88-4309-8E2D-3D8B347F5B53}")
MsgBox Installer.ProductInfo("{BAE98781-CF88-4309-8E2D-3D8B347F5B53}", "Transforms")

'
' Remove Product
'
Installer.InstallProduct "c:\scratch\simpletst\rtm\simple.msi", "REMOVE=ALL"
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

 

 




