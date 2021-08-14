---
description: La propriété ComponentState est l’état d’installation du composant pour l’instance de ce produit. Cette propriété appelle MsiQueryComponentState, avec le ProductCode, UserSid et le contexte de l’objet.
ms.assetid: 2939048a-42a5-4ffb-868c-251c0f15e5ed
title: Méthode Product. ComponentState
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product.ComponentState
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: d2bc9c5c1f5325dc631f8866ba1a8c7d88ce18d624a2974974f4692bf4f7b067
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118376778"
---
# <a name="productcomponentstate-method"></a>Méthode Product. ComponentState

La propriété **ComponentState** est l’état d’installation du composant pour l’instance de ce produit.

Cette propriété appelle [**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea), avec le ProductCode, UserSid et le contexte de l’objet. Le GUID de l’ID du composant est fourni en tant que paramètre.

## <a name="syntax"></a>Syntaxe


```JScript
Product.ComponentState(
  ID
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Identifiant* 
</dt> <dd>

GUID du code du composant, tel qu’il figure dans la colonne ComponentID de la [table des composants](component-table.md).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Remarques

Si l’appel est effectué, la propriété contient la valeur en tant que **DWORD**.



| State                | Signification                                            |
|----------------------|----------------------------------------------------|
| INSTALLSTATE \_ local  | Le composant est installé localement.                |
| \_source INSTALLSTATE | Le composant est installé pour s’exécuter à partir de la source. |



 

Si l’appel échoue, la propriété contient un code d’erreur de [**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea).



| Erreur                     | Signification                                                                                                            |
|---------------------------|--------------------------------------------------------------------------------------------------------------------|
| ERREUR d' \_ accès \_ refusé     | Le processus appelant doit disposer de privilèges d’administrateur pour obtenir des informations pour un utilisateur autre que l’utilisateur actuel. |
| ERREUR de \_ configuration incorrecte \_ | Les données de configuration sont endommagées.                                                                                 |
| paramètre d’erreur \_ non valide \_ | Un paramètre non valide a été passé à la fonction.                                                                   |
| ERREUR de \_ réussite            | La fonction s’est terminée avec succès.                                                                               |
| ERREUR \_ de \_ composant inconnu | L’ID de composant n’identifie pas un composant connu.                                                              |
| ERREUR \_ de \_ produit inconnu   | Le code du produit n’identifie pas un produit connu.                                                                |
| échec de la fonction d’erreur \_ \_   | Une erreur interne inattendue.                                                                                    |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Version<br/> | Windows Installer 5,0 sur Windows Server 2012, Windows 8, Windows Server 2008 R2 ou Windows 7. Windows Installer 4,0 ou Windows Installer 4,5 sur Windows Server 2008 ou Windows Vista. Windows programme d’installation 3,0 ou version ultérieure sur Windows Server 2003, Windows XP et Windows 2000<br/> |
| DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID \_ IProduct est défini en tant que 000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Production**](product-object.md)
</dt> <dt>

[**MsiQueryComponentState**](/windows/desktop/api/Msi/nf-msi-msiquerycomponentstatea)
</dt> <dt>

[non pris en charge dans Windows Installer 2,0 et versions antérieures](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 




