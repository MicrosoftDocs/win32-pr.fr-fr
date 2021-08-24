---
description: La méthode Reset de la \_ classe CIM CurrentSensor demande une réinitialisation de l’unité logique.
ms.assetid: 4c1f500b-bc8b-428f-8f4e-cbf5a18f9405
ms.tgt_platform: multiple
title: Méthode Reset de la classe CIM_CurrentSensor
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CurrentSensor.Reset
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d6ebccfb75abd55a9bf3df69051195a1ca73204a578321d91e5c7cfae433f923
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119701519"
---
# <a name="reset-method-of-the-cim_currentsensor-class"></a>Méthode Reset de la \_ classe CIM CurrentSensor

La méthode **Reset** de la \_ classe CIM CurrentSensor demande une réinitialisation de l’unité logique. Cette méthode est héritée de [**CIM \_ LogicalDevice**](cim-logicaldevice.md).

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

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                                |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                          |
| Espace de noms<br/>                | \\Cimv2 racine<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[\_CURRENTSENSOR CIM](reset-method-in-class-cim-currentsensor.md)
</dt> <dt>

[**\_CURRENTSENSOR CIM**](cim-currentsensor.md)
</dt> </dl>

 

 




