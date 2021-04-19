---
description: La propriété InstallProperty est la valeur de la propriété pour l’instance de ce produit. Cette propriété appelle la fonction MsiGetProductInfoEx, avec le ProductCode, le UserSid et le contexte de l’objet Product et la propriété demandée en tant que paramètre.
ms.assetid: 945c11fe-39da-43b7-a19f-e6364d5e715c
title: Méthode Product. InstallProperty
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.InstallProperty
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 12949997363fce8073c15f7ca6b7312c211fa0f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525178"
---
# <a name="productinstallproperty-method"></a>Méthode Product. InstallProperty

La propriété **InstallProperty** est la valeur de la propriété pour l’instance de ce produit.

Cette propriété appelle la fonction [**MsiGetProductInfoEx**](/windows/desktop/api/Msi/nf-msi-msigetproductinfoexa) , avec le *ProductCode*, le *UserSid* et le *contexte* de l’objet [**Product**](product-object.md) et la propriété demandée en tant que paramètre.

## <a name="syntax"></a>Syntaxe


```JScript
Product.InstallProperty(
  property
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*property* 
</dt> <dd>

Spécifie la propriété à récupérer. Les propriétés de la liste suivante peuvent uniquement être récupérées à partir d’applications déjà installées. Notez que les propriétés [requises](required-properties.md) sont toujours disponibles, mais que d’autres propriétés ne sont disponibles que si cette propriété a été définie. Pour plus d’informations sur la façon dont chaque propriété est définie, consultez les liens indiqués vers les [Propriétés](properties.md) du programme d’installation.



| Propriétés installées                                                                                                                                                                                                               | Signification                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="INSTALLPROPERTY_PRODUCTSTATE"></span><span id="installproperty_productstate"></span><dl> <dt>**INSTALLPROPERTY \_ PRODUCTSTATE**</dt> </dl>                         | État du produit retourné sous forme de chaîne « 1 » pour publié et « 5 » pour installé.<br/>                                                                                                                                                                                                                                                                            |
| <span id="INSTALLPROPERTY_HELPLINK"></span><span id="installproperty_helplink"></span><dl> <dt>**INSTALLPROPERTY \_ HELPLINK**</dt> </dl>                                     | Lien de support. Pour plus d’informations, consultez la propriété [**ARPHELPLINK**](arphelplink.md) .<br/>                                                                                                                                                                                                                                                                             |
| <span id="INSTALLPROPERTY_HELPTELEPHONE"></span><span id="installproperty_helptelephone"></span><dl> <dt>**INSTALLPROPERTY \_ HELPTELEPHONE**</dt> </dl>                      | Téléphone de support. Pour plus d’informations, consultez la propriété [**ARPHELPTELEPHONE**](arphelptelephone.md) .<br/>                                                                                                                                                                                                                                                              |
| <span id="INSTALLPROPERTY_INSTALLDATE"></span><span id="installproperty_installdate"></span><dl> <dt>**INSTALLPROPERTY \_ INSTALLDATE**</dt> </dl>                            | Heure de la dernière réception du service par ce produit. La valeur de cette propriété est remplacée chaque fois qu’un correctif est appliqué ou supprimé du produit ou lorsque l' [option de ligne de commande](command-line-options.md) /v est utilisée pour réparer le produit. Si le produit n’a pas reçu de réparation ou de correctifs, cette propriété contient l’heure à laquelle le produit a été installé sur cet ordinateur.<br/> |
| <span id="INSTALLPROPERTY_INSTALLEDPRODUCTNAME"></span><span id="installproperty_installedproductname"></span><dl> <dt>**INSTALLPROPERTY \_ INSTALLEDPRODUCTNAME**</dt> </dl> | Nom du produit installé. Pour plus d’informations, consultez la propriété [**ProductName**](productname.md) .<br/>                                                                                                                                                                                                                                                                   |
| <span id="INSTALLPROPERTY_INSTALLLOCATION"></span><span id="installproperty_installlocation"></span><dl> <dt>**INSTALLPROPERTY \_ InstallLocation**</dt> </dl>                | Emplacement d’installation. Pour plus d’informations, consultez la propriété [**ARPINSTALLLOCATION**](arpinstalllocation.md) .<br/>                                                                                                                                                                                                                                                      |
| <span id="INSTALLPROPERTY_INSTALLSOURCE"></span><span id="installproperty_installsource"></span><dl> <dt>**INSTALLPROPERTY \_ INSTALLSOURCE**</dt> </dl>                      | Source d’installation. Pour plus d’informations, consultez la propriété [**SourceDir**](sourcedir.md) .<br/>                                                                                                                                                                                                                                                                          |
| <span id="INSTALLPROPERTY_LOCALPACKAGE"></span><span id="installproperty_localpackage"></span><dl> <dt>**INSTALLPROPERTY \_ LOCALPACKAGE**</dt> </dl>                         | Package local mis en cache.<br/>                                                                                                                                                                                                                                                                                                                                                |
| <span id="INSTALLPROPERTY_PUBLISHER"></span><span id="installproperty_publisher"></span><dl> <dt>**serveur de \_ publication INSTALLPROPERTY**</dt> </dl>                                  | Publication. Pour plus d’informations, consultez la propriété [**Manufacturer**](manufacturer.md) .<br/>                                                                                                                                                                                                                                                                              |
| <span id="INSTALLPROPERTY_URLINFOABOUT"></span><span id="installproperty_urlinfoabout"></span><dl> <dt>**INSTALLPROPERTY \_ URLINFOABOUT**</dt> </dl>                         | Informations sur l’URL. Pour plus d’informations, consultez la propriété [**ARPURLINFOABOUT**](arpurlinfoabout.md) .<br/>                                                                                                                                                                                                                                                                  |
| <span id="INSTALLPROPERTY_URLUPDATEINFO"></span><span id="installproperty_urlupdateinfo"></span><dl> <dt>**INSTALLPROPERTY \_ URLUPDATEINFO**</dt> </dl>                      | Informations de mise à jour d’URL. Pour plus d’informations, consultez la propriété [**ARPURLUPDATEINFO**](arpurlupdateinfo.md) .<br/>                                                                                                                                                                                                                                                         |
| <span id="INSTALLPROPERTY_VERSIONMINOR"></span><span id="installproperty_versionminor"></span><dl> <dt>**INSTALLPROPERTY \_ VERSIONMINOR**</dt> </dl>                         | Version mineure du produit dérivée de la propriété [**ProductVersion**](productversion.md) .<br/>                                                                                                                                                                                                                                                                            |
| <span id="INSTALLPROPERTY_VERSIONMAJOR"></span><span id="installproperty_versionmajor"></span><dl> <dt>**INSTALLPROPERTY \_ VERSIONMAJOR**</dt> </dl>                         | Version du produit principale dérivée de la propriété [**ProductVersion**](productversion.md) .<br/>                                                                                                                                                                                                                                                                            |
| <span id="INSTALLPROPERTY_VERSIONSTRING"></span><span id="installproperty_versionstring"></span><dl> <dt>**INSTALLPROPERTY, \_ VERSIONSTRING**</dt> </dl>                      | Version du produit. Pour plus d’informations, consultez la propriété [**ProductVersion**](productversion.md) .<br/>                                                                                                                                                                                                                                                                    |



 

Pour récupérer l’ID de produit, le propriétaire inscrit ou une société inscrite à partir d’applications déjà installées, définissez la *propriété* sur l’une des valeurs de chaîne de texte suivantes.



| Valeur      | Description                                                                                    |
|------------|------------------------------------------------------------------------------------------------|
| ProductID  | Identificateur du produit. Pour plus d’informations, consultez la propriété [**ProductID**](productid.md) . |
| RegCompany | La société inscrite pour utiliser ce produit.                                                    |
| RegOwner   | Propriétaire inscrit pour utiliser ce produit.                                                      |



 

Pour récupérer le type d’instance du produit, affectez à la *propriété* la valeur suivante. Cette propriété est disponible pour les produits publiés ou installés.



| Valeur        | Description                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| InstanceType | Une valeur manquante ou une valeur de 0 indique une installation normale du produit. La valeur 1 indique un produit installé à l’aide d’une transformation à plusieurs instances et de la propriété [**MSINEWINSTANCE**](msinewinstance.md) . Disponible avec le programme d’installation exécutant Windows Server 2003 ou Windows XP avec SP1. Pour plus d’informations, consultez [installation de plusieurs instances de produits et de correctifs](installing-multiple-instances-of-products-and-patches.md). |



 

Les propriétés de la liste suivante peuvent également être récupérées à partir d’applications publiées. Ces propriétés ne peuvent pas être récupérées pour les instances de produit installées dans un contexte non géré par utilisateur pour les comptes d’utilisateurs autres que le compte d’utilisateur actuel.



| Propriétés publiées                 | Description                                                                                                                                                                                                                                                                                          |
|---------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_TRANSformations INSTALLPROPERTY           | Transformations :                                                                                                                                                                                                                                                                                          |
| \_langue INSTALLPROPERTY             | Langue du produit.                                                                                                                                                                                                                                                                                    |
| INSTALLPROPERTY \_ ProductName          | Lisible par l’utilisateur : nom du produit. Pour plus d’informations, consultez la propriété [**ProductName**](productname.md) .                                                                                                                                                                                              |
| INSTALLPROPERTY \_ ASSIGNMENTTYPE       | Est égal à zéro (0) si le produit est publié ou installé par utilisateur. Est égal à un (1) si le produit est publié ou installé par ordinateur pour tous les utilisateurs.<br/>                                                                                                                                  |
| INSTALLPROPERTY \_ PACKAGECODE          | Identificateur du package à partir duquel ce produit a été installé. Pour plus d’informations, consultez [codes de package](package-codes.md).                                                                                                                                                                                      |
| VERSION de INSTALLPROPERTY \_              | Version du produit dérivée de la propriété [**ProductVersion**](productversion.md) .                                                                                                                                                                                                                  |
| INSTALLPROPERTY \_ PRODUCTICON          | Icône principale du package. Pour plus d’informations, consultez la propriété [**ARPPRODUCTICON**](arpproducticon.md) .                                                                                                                                                                                       |
| INSTALLPROPERTY \_ PackageName          | Nom du package d’installation d’origine.                                                                                                                                                                                                                                                           |
| \_ \_ application Lua autorisée \_ INSTALLPROPERTY | La valeur 1 indique un produit qui peut être desservi par des non-administrateurs à l’aide de la mise à [jour corrective du contrôle de compte d’utilisateur](user-account-control--uac--patching.md). Une valeur manquante ou une valeur de 0 indique que la mise à jour corrective des privilèges minimum n’est pas activée. Disponible avec Windows Installer 3,0 et versions ultérieures. |



 

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Si l’appel a échoué, la propriété contient la valeur sous forme de chaîne.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows Installer 3,0 ou version ultérieure sur Windows Server 2003, Windows XP et Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IProduct est défini en tant que 000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Production**](product-object.md)
</dt> <dt>

[Non pris en charge dans Windows Installer 2,0 et versions antérieures](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




