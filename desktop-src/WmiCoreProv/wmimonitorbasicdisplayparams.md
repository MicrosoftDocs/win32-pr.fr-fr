---
description: Représente les fonctionnalités d’affichage de base d’un moniteur d’ordinateur.
ms.assetid: 08405e7f-7824-4e44-9f37-da9bb5619cd6
title: WmiMonitorBasicDisplayParams, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorBasicDisplayParams
- WmiMonitorBasicDisplayParams.Active
- WmiMonitorBasicDisplayParams.DisplayTransferCharacteristic
- WmiMonitorBasicDisplayParams.InstanceName
- WmiMonitorBasicDisplayParams.MaxHorizontalImageSize
- WmiMonitorBasicDisplayParams.MaxVerticalImageSize
- WmiMonitorBasicDisplayParams.SupportedDisplayFeatures
- WmiMonitorBasicDisplayParams.VideoInputType
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: e457757a3542bbfc8ded7536396458ef3e592714
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013091"
---
# <a name="wmimonitorbasicdisplayparams-class"></a>WmiMonitorBasicDisplayParams, classe

La classe WMI **WmiMonitorBasicDisplayParams** représente les fonctionnalités d’affichage de base d’un moniteur d’ordinateur. La valeur de la propriété **VideoInputType** indique si l’analyse est analogique ou numérique. Les données de cette classe correspondent aux données dans le bloc paramètres d’affichage de base/fonctionnalités de la norme E-EDID (Enhanced Display Identification Data) améliorée de l’Association Video Electronics standard Association (VESA).

## <a name="syntax"></a>Syntaxe

``` syntax
class WmiMonitorBasicDisplayParams : MSMonitorClass
{
  boolean                            Active;
  uint8                              DisplayTransferCharacteristic;
  string                             InstanceName;
  uint8                              MaxHorizontalImageSize;
  uint8                              MaxVerticalImageSize;
  SupportedDisplayFeaturesDescriptor SupportedDisplayFeatures;
  uint8                              VideoInputType;
};
```

## <a name="members"></a>Membres

La classe **WmiMonitorBasicDisplayParams** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **WmiMonitorBasicDisplayParams** possède les propriétés suivantes.

<dl> <dt>

**Actif**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique le moniteur actif.

</dd> <dt>

**DisplayTransferCharacteristic**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Affichez les caractéristiques de transfert (100 \* gamma-100).

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

**MaxHorizontalImageSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Taille maximale de l’image horizontale en centimètres. Pour plus d'informations, consultez la section Notes.

</dd> <dt>

**MaxVerticalImageSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Taille d’image verticale maximale en centimètres. Pour plus d'informations, consultez la section Notes.

</dd> <dt>

**SupportedDisplayFeatures**
</dt> <dd> <dl> <dt>

Type de données : **[ **SupportedDisplayFeaturesDescriptor**](supporteddisplayfeaturesdescriptor.md)**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Affichez les fonctionnalités prises en charge par l’analyse.

</dd> <dt>

**VideoInputType**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Type d’entrée vidéo.



| Valeur                                                                              | Signification            |
|------------------------------------------------------------------------------------|--------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | Analogique<br/>  |
| <dl> <dt>1 (0x1)</dt> </dl> | Digital<br/> |



 

</dd> </dl>

## <a name="remarks"></a>Notes

**MaxHorizontalImageSize** et **MaxVerticalImageSize** représentent les dimensions d’image maximales que le moniteur peut afficher correctement pour l’ensemble des combinaisons de mise en forme et de minutage prises en charge. La dimension image maximale est définie par la norme VESA Video image image Definition (VIAD) et est arrondie au centimètre le plus proche. Le système de l’ordinateur hôte peut utiliser ces données pour sélectionner la taille de l’image et les proportions qui permettront un texte correctement mis à l’échelle. Sachez que, si l’un des champs ou les deux sont nuls, le système n’émet aucune supposition quant à la taille d’affichage. Par exemple, la taille d’un affichage de projection peut être indéterminée.

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

 

 




