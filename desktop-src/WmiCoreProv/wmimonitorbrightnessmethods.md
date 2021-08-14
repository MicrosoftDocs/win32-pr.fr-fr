---
description: Contient des méthodes qui gèrent la luminosité de l’analyse.
ms.assetid: e7e4139e-b985-4163-9c95-03008a2cc8cb
title: WmiMonitorBrightnessMethods, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBrightnessMethods
- WmiMonitorBrightnessMethods.Active
- WmiMonitorBrightnessMethods.InstanceName
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 255cfa75ab892739ce211432ef81d32da4e1cbb3205e5467045e2d81f156d102
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118321361"
---
# <a name="wmimonitorbrightnessmethods-class"></a>WmiMonitorBrightnessMethods, classe

La classe WMI **WmiMonitorBrightnessMethods** contient des méthodes qui gèrent la luminosité de l’analyse.

## <a name="syntax"></a>Syntaxe

``` syntax
class WmiMonitorBrightnessMethods
{
  boolean Active;
  string  InstanceName;
};
```

## <a name="members"></a>Membres

La classe **WmiMonitorBrightnessMethods** possède les types de membres suivants :

-   [Méthodes](#wmimonitorbrightnessmethods-class)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

La classe **WmiMonitorBrightnessMethods** possède ces méthodes.



| Méthode                                                                                                         | Description                                                    |
|:---------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------|
| [**WmiRevertToPolicyBrightness**](wmireverttopolicybrightness-method-in-class-wmimonitorbrightnessmethods.md) | Rétablit la luminosité sur le paramètre de stratégie.<br/>     |
| [**WmiSetALSBrightness**](wmisetalsbrightness-method-in-class-wmimonitorbrightnessmethods.md)                 | Définit la valeur de luminosité du capteur de lumière ambiante.<br/>     |
| [**WmiSetALSBrightnessState**](wmisetalsbrightnessstate-method-in-class-wmimonitorbrightnessmethods.md)       | Contrôle l’état de luminosité du capteur de lumière ambiante.<br/> |
| [**WmiSetBrightness**](wmisetbrightness-method-in-class-wmimonitorbrightnessmethods.md)                       | Définit la luminosité de l’analyse.<br/>                        |



 

### <a name="properties"></a>Propriétés

La classe **WmiMonitorBrightnessMethods** possède les propriétés suivantes.

<dl> <dt>

**Actif**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique le moniteur actif.

</dd> <dt>

**InstanceName**
</dt> <dd> <dl> <dt>

Type de données : **chaîne**
</dt> <dt>

Type d'accès : Lecture seule
</dt> <dt>

Qualificateurs : **clé**
</dt> </dl>

Nom de l’instance d’analyse spécifique.

</dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                         |
| Espace de noms<br/>                | \\WMI racine<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>WmiCore. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WmiProv.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**MSMonitorClass**](msmonitorclass.md)
</dt> </dl>

 

 




