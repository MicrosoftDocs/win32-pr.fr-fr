---
description: La propriété FeatureState est l’état d’installation de la fonctionnalité pour l’instance de ce produit. Cette propriété appelle MsiQueryFeatureStateEx, avec le ProductCode, UserSid et le contexte de l’objet. L’ID de fonctionnalité est fourni en tant que paramètre.
ms.assetid: 6821be80-4065-465e-b4c9-4cf17856bc5f
title: Méthode Product. FeatureState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.FeatureState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3f7e602ce5d5b0a8e524f76144c7f1eff8876bb5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106541278"
---
# <a name="productfeaturestate-method"></a>Méthode Product. FeatureState

La propriété **FeatureState** est l’état d’installation de la fonctionnalité pour l’instance de ce produit.

Cette propriété appelle [**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa), avec le *ProductCode*, *UserSid* et le *contexte* de l’objet. L’ID de fonctionnalité est fourni en tant que paramètre.

## <a name="syntax"></a>Syntaxe


```JScript
Product.FeatureState(
  FeatureId
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*FeatureId* 
</dt> <dd>

ID de fonctionnalité qui apparaît dans la colonne fonctionnalité du [tableau des fonctionnalités](feature-table.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Si l’appel est effectué, la propriété contient la valeur en tant que **DWORD**.



| State                    | Signification                                      |
|--------------------------|----------------------------------------------|
| INSTALLSTATE \_ publié | Cette fonctionnalité est publiée.                  |
| INSTALLSTATE \_ local      | La fonctionnalité est installée localement.            |
| \_source INSTALLSTATE     | La fonctionnalité est installée pour s’exécuter à partir de la source. |



 

Si l’appel échoue, la propriété contient un code d’erreur de [**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa).



| Error                     | Signification                                                                                                                                    |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| ERREUR d' \_ accès \_ refusé     | Le processus appelant doit disposer de privilèges d’administrateur pour obtenir des informations sur un produit installé pour un utilisateur autre que l’utilisateur actuel. |
| ERREUR de \_ configuration incorrecte \_ | Les données de configuration sont endommagées.                                                                                                         |
| paramètre d’erreur \_ non valide \_ | Un paramètre non valide a été passé à la fonction.                                                                                           |
| ERREUR de \_ réussite            | La fonction s’est terminée avec succès.                                                                                                       |
| \_fonctionnalité inconnue d’erreur \_   | L’ID de fonctionnalité n’identifie pas une fonctionnalité connue.                                                                                          |
| ERREUR \_ de \_ produit inconnu   | Le code du produit n’identifie pas un produit connu.                                                                                        |
| échec de la fonction d’erreur \_ \_   | Une erreur interne inattendue.                                                                                                            |



 

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

[**MsiQueryFeatureStateEx**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestateexa)
</dt> <dt>

[Non pris en charge dans Windows Installer 2,0 et versions antérieures](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




