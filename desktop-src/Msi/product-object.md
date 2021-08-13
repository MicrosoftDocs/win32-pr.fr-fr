---
description: L’objet Product représente une instance unique d’un produit qui est publié, installé ou inconnu. L’objet peut être instancié avec la propriété Product comme &\# 0034 ; WindowsInstaller. installer. Product (ProductCode, UserSid, contexte) &\# 0034 ;.
ms.assetid: 1fa89239-051a-4b3a-913a-12c7c093f35b
title: Product, objet
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: ff05a2f89244da09caa6cd3b26fc4b5d9cdbec95c0fcc3098fddf0c39dc68519
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118627672"
---
# <a name="product-object"></a>Product, objet

L’objet **Product** représente une instance unique d’un produit qui est publié, installé ou inconnu.

L’objet peut être instancié avec la propriété **Product** comme « windowsinstaller. installer. Product (*ProductCode*, *UserSid*, *Context*) ». *UserSid* doit avoir la valeur null pour le contexte par ordinateur. *UserSid* peut avoir la valeur null pour l’utilisateur actuel spécifié, lorsque le contexte n’est pas par machine. Les paramètres *ProductCode* et *Context* sont requis.

## <a name="members"></a>Membres

L’objet **Product** contient les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **Product** possède ces méthodes.



| Méthode                                                                 | Description                                                                                                        |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------|
| [**SourceListAddMediaDisk**](product-sourcelistaddmediadisk.md)       | Ajoutez un disque à l’ensemble de disques inscrits.<br/>                                                              |
| [**SourceListAddSource**](product-sourcelistaddsource.md)             | Ajoutez une source réseau ou URL à la liste source.<br/>                                                         |
| [**SourceListClearAll**](product-sourcelistclearall.md)               | Efface la liste source complète du type spécifié de sources.<br/>                                       |
| [**SourceListClearMediaDisk**](product-sourcelistclearmediadisk.md)   | Supprimer un disque de l’ensemble de disques inscrits de la liste source.<br/>                                    |
| [**SourceListClearSource**](product-sourcelistclearsource.md)         | Supprimer une source de réseau ou d’URL de la liste source.<br/>                                                    |
| [**SourceListForceResolution**](product-sourcelistforceresolution.md) | Efface la dernière source utilisée. Cela force une résolution de liste source la prochaine fois que la source est requise.<br/> |



 

### <a name="properties"></a>Propriétés

L’objet **Product** possède ces propriétés.



| Propriété                                                      | Description                                                                                 |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**ComponentState**](product-componentstate.md)<br/>   | État d’un composant spécifié pour cette instance de produit. <br/>                   |
| [**Contexte**](product-context.md)<br/>                 | Contexte de cette instance de produit en tant que valeur MSIINSTALLCONTEXT. <br/>                 |
| [**FeatureState**](product-featurestate.md)<br/>       | État d’une fonctionnalité spécifiée pour cette instance de produit. <br/>                     |
| [**InstallProperty**](product-installproperty.md)<br/> | Valeur d’une propriété spécifiée. <br/>                                              |
| [**MediaDisks**](product-mediadisks.md)<br/>           | Énumère tous les disques multimédias pour cette instance de produit.<br/>                        |
| [**ProductCode**](product-productcode.md)<br/>         | Retourne le code du produit. <br/>                                                       |
| [**SourceListInfo**](product-sourcelistinfo.md)<br/>   | Obtient et définit les propriétés des informations sur la source. Il s’agit d’une propriété de lecture ou d’écriture.<br/> |
| [**Sources**](product-sources.md)<br/>                 | Énumère toutes les sources pour cette instance de produit.<br/>                            |
| [**State**](product-state.md)<br/>                     | État d’installation du produit.<br/>                                               |
| [**UserSid**](product-usersid.md)<br/>                 | Retourne le SID de l’utilisateur, sous quel compte cette instance de produit est disponible.<br/>    |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows programme d’installation 3,0 ou version ultérieure sur Windows Server 2003, Windows XP et Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IProduct est défini en tant que 000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Windows Exemples de scripts d’installation](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




