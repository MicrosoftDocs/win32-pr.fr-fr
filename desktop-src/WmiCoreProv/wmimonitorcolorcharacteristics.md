---
description: Représente les caractéristiques de couleur CIE (International Commission on illumination) d’un moniteur d’ordinateur.
ms.assetid: 476aefae-11c0-46be-a2bb-83fbafd70421
title: WmiMonitorColorCharacteristics, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorColorCharacteristics
- WmiMonitorColorCharacteristics.Active
- WmiMonitorColorCharacteristics.Blue
- WmiMonitorColorCharacteristics.DefaultWhite
- WmiMonitorColorCharacteristics.Green
- WmiMonitorColorCharacteristics.InstanceName
- WmiMonitorColorCharacteristics.Red
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 9fbb7d56e56519576d257b077311a144e923d6bb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013080"
---
# <a name="wmimonitorcolorcharacteristics-class"></a>WmiMonitorColorCharacteristics, classe

La classe **WmiMonitorColorCharacteristics** représente les caractéristiques de couleur Cie (International Commission on illumination) d’un moniteur d’ordinateur. Les données correspondent aux données dans le bloc des caractéristiques de couleur de la structure E-EDID (Extended Display Identification Data) améliorée de l’Association Video Electronics standard Association (VESA).

## <a name="syntax"></a>Syntaxe

``` syntax
class WmiMonitorColorCharacteristics : MSMonitorClass
{
  boolean  Active;
  XYZinCIE Blue;
  XYZinCIE DefaultWhite;
  XYZinCIE Green;
  string   InstanceName;
  XYZinCIE Red;
};
```

## <a name="members"></a>Membres

La classe **WmiMonitorColorCharacteristics** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **WmiMonitorColorCharacteristics** possède les propriétés suivantes.

<dl> <dt>

**Actif**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique le moniteur actif.

</dd> <dt>

**Bleu**
</dt> <dd> <dl> <dt>

Type de données : **[ **XYZinCIE**](xyzincie.md)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Coordonnées CIE pour le bleu, représentées par une instance de la classe [**XYZinCIE**](xyzincie.md) .

</dd> <dt>

**DefaultWhite**
</dt> <dd> <dl> <dt>

Type de données : **[ **XYZinCIE**](xyzincie.md)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Coordonnées CIE blanches par défaut.

</dd> <dt>

**Vert**
</dt> <dd> <dl> <dt>

Type de données : **[ **XYZinCIE**](xyzincie.md)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Coordonnées CIE pour le vert, représentées par une instance de la classe [**XYZinCIE**](xyzincie.md) .

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

**Rouge**
</dt> <dd> <dl> <dt>

Type de données : **[ **XYZinCIE**](xyzincie.md)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Coordonnées CIE pour le rouge, représentées par une instance de la classe [**XYZinCIE**](xyzincie.md) .

</dd> </dl>

## <a name="remarks"></a>Notes

Les valeurs de la chromatique et du point blanc sont exprimées sous forme de nombres fractionnaires à l’aide d’un format d’encodage. Ce format est précis à l’emplacement du millième, ce qui correspond à une longueur de 10 bits. Le bit le plus significatif (MSB) représente 2 ^-1 et le bit le moins significatif (LSB) représente respectivement 2 ^-10 coefficients. La précision des valeurs stockées dans la structure E-EDID v1. x doit être précise à +/-0,005 de la valeur réelle.

## <a name="requirements"></a>Spécifications



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

 

 




