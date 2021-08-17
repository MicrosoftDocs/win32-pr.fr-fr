---
description: Représente les paramètres d’entrée de la vidéo numérique.
ms.assetid: aa459612-db79-477b-891f-28c9d0b1b497
title: WmiMonitorDigitalVideoInputParams, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorDigitalVideoInputParams
- WmiMonitorDigitalVideoInputParams.Active
- WmiMonitorDigitalVideoInputParams.InstanceName
- WmiMonitorDigitalVideoInputParams.IsDFP1xCompatible
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: fa86add32d77a5b2838fc78eaf097c11b8a15db3f0fde9186f93046691ebc3f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117926565"
---
# <a name="wmimonitordigitalvideoinputparams-class"></a>WmiMonitorDigitalVideoInputParams, classe

**WmiMonitorDigitalVideoInputParams** représente les paramètres d’entrée de la vidéo numérique. Les données de cette classe correspondent aux données de la définition d’entrée vidéo de la norme E-EDID (Extended Display Identification Data) améliorée de l’Association Video Electronics standard Association (VESA). Une instance de cette classe est disponible uniquement lorsque la valeur de la propriété **VideoInputType** de la classe [**WmiMonitorBasicDisplayParams**](wmimonitorbasicdisplayparams.md) est « Digital ».

## <a name="syntax"></a>Syntaxe

``` syntax
class WmiMonitorDigitalVideoInputParams : MSMonitorClass
{
  boolean Active;
  string  InstanceName;
  boolean IsDFP1xCompatible;
};
```

## <a name="members"></a>Membres

La classe **WmiMonitorDigitalVideoInputParams** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **WmiMonitorDigitalVideoInputParams** possède les propriétés suivantes.

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

</dd> <dt>

**IsDFP1xCompatible**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

VESA DFP 1. x ou compatible. Si cette valeur est définie, l’interface est signalée comme étant compatible avec le panneau plat numérique (DFP) 1. x transition réduite de signal différentiel (TMDS) CRGB, 1 pixel/horloge, jusqu’à 8 bits/bit DE poids le plus significatif (MSB) aligné, DE haut actif.

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

 

 




