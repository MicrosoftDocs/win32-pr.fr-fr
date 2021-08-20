---
description: La méthode Reset de la \_ classe CIM CDROMDrive demande une réinitialisation de l’unité logique.
ms.assetid: 9d422fb3-8332-4be5-8e90-0e782640748a
ms.tgt_platform: multiple
title: Méthode Reset de la classe CIM_CDROMDrive
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CDROMDrive.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9ab872ac313c6a60cd3d47715a5b4bbb9872d0ed8d7bdc7b203928c4d3a1c24d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118009467"
---
# <a name="reset-method-of-the-cim_cdromdrive-class"></a>Méthode Reset de la \_ classe CIM CDROMDrive

La méthode **Reset** de la \_ classe CIM CDROMDrive demande une réinitialisation de l’unité logique. Cette méthode est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

> [!IMPORTANT]
> Les classes de la DMTF (Distributed Management Task Force) CIM (Common Information Model) sont les classes parentes sur lesquelles les classes WMI sont générées. WMI ne prend actuellement en charge que les [schémas de version CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

## <a name="syntax"></a>Syntaxe


```mof
uint32 Reset();
```



## <a name="parameters"></a>Paramètres

Cette méthode n’a aucun paramètre.

## <a name="return-value"></a>Valeur retournée

Retourne 0 (zéro) si la requête a été exécutée avec succès, 1 (un) si la demande n’est pas prise en charge, et une autre valeur si une erreur s’est produite.

## <a name="remarks"></a>Remarques

Actuellement, cette méthode n’est pas implémentée par WMI. Pour utiliser cette méthode, vous devez l’implémenter dans votre propre fournisseur.

Cette documentation est dérivée des descriptions de classe CIM publiées par le DMTF. Microsoft peut avoir apporté des modifications pour corriger les erreurs mineures, se conformer aux normes de documentation du kit de développement logiciel (SDK) Microsoft ou fournir plus d’informations.

## <a name="requirements"></a>Conditions requises



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[\_CDROMDRIVE CIM](reset-method-in-class-cim-cdromdrive.md)
</dt> <dt>

[**\_CDROMDRIVE CIM**](cim-cdromdrive.md)
</dt> </dl>

 

 




