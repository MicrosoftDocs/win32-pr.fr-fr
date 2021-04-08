---
description: Représente l’aspect de pontage transparent d’un \_ objet CIM SwitchService.
ms.assetid: 24f650ab-22a1-41c8-8498-c6c30e63c83c
title: Classe CIM_TransparentBridgingService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_TransparentBridgingService
- CIM_TransparentBridgingService.AgingTime
- CIM_TransparentBridgingService.FID
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ed2c21c0f00bd89b0054667274a559ef25ce9326
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864113"
---
# <a name="cim_transparentbridgingservice-class"></a>\_Classe CIM TransparentBridgingService

Représente l’aspect de pontage transparent d’un objet [**CIM \_ SwitchService**](cim-switchservice.md) .

## <a name="syntax"></a>Syntaxe

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::SwitchingBridging"), AMENDMENT]
class CIM_TransparentBridgingService : CIM_ForwardingService
{
  uint32 AgingTime = 300;
  uint32 FID;
};
```

## <a name="members"></a>Membres

La classe **CIM \_ TransparentBridgingService** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **CIM \_ TransparentBridgingService** possède les propriétés suivantes.

<dl> <dt>

**AgingTime**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : [**unités**](/windows/desktop/WmiSdk/standard-qualifiers) (« seconds »), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) («MIB. IETF \| Bridge-MIB. dot1dTpAgingTime ")
</dt> </dl>

Délai d’attente, en secondes, pour le vieillissement des informations de transfert apprises de manière dynamique. La norme 802.1 D-1990 recommande une valeur par défaut de 300 secondes.

</dd> <dt>

**IDENTIFICATEUR manquant**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Filtrage de l’identificateur de base de données utilisé par les commutateurs sensibles aux réseaux locaux virtuels qui ont plusieurs bases de données de filtrage.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8<br/>                                                                                    |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                                          |
| Espace de noms<br/>                | \\Virtualisation racine \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_FORWARDINGSERVICE CIM**](cim-forwardingservice.md)
</dt> </dl>

 

