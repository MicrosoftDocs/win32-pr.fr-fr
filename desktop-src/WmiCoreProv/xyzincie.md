---
description: Contient les coordonnées de l’affichage dans l’espace de couleurs CIE (International Commission on illumination) XYZ.
ms.assetid: e44e8a5f-005d-4d58-84e3-135d4e396086
title: XYZinCIE, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- XYZinCIE
- XYZinCIE.X
- XYZinCIE.Y
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: ba7f781a83f3e6ba5aa4683003386a0478d65088
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106521352"
---
# <a name="xyzincie-class"></a>XYZinCIE, classe

La classe WMI **XYZinCIE** contient les coordonnées de l’affichage dans l’espace de couleurs Cie (International Commission on illumination) XYZ.

## <a name="syntax"></a>Syntaxe

``` syntax
class XYZinCIE : WmiMonitorColorCharacteristics
{
  uint16 X;
  uint16 Y;
};
```

## <a name="members"></a>Membres

La classe **XYZinCIE** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **XYZinCIE** possède les propriétés suivantes.

<dl> <dt>

**X**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Coordonnée X.

</dd> <dt>

**O**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Coordonnée Y.

</dd> </dl>

## <a name="remarks"></a>Notes

La classe [**WmiMonitorColorCharacteristics**](wmimonitorcolorcharacteristics.md) contient des instances incorporées de la classe **XYZinCIE** pour décrire les caractéristiques de couleur d’une analyse.

Pour calculer la coordonnée z, en fonction des valeurs x et y, utilisez la relation \| \| (x, y, z) \| \| = 1.

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

 

 




