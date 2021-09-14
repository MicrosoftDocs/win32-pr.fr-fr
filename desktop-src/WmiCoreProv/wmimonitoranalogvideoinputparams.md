---
description: Représente les paramètres d’entrée de vidéo analogique d’un moniteur d’ordinateur.
ms.assetid: 87d4260d-06c7-4a76-a3a1-8f6e51e23d92
title: WmiMonitorAnalogVideoInputParams, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WmiMonitorAnalogVideoInputParams
- WmiMonitorAnalogVideoInputParams.Active
- WmiMonitorAnalogVideoInputParams.CompositeSyncSupported
- WmiMonitorAnalogVideoInputParams.InstanceName
- WmiMonitorAnalogVideoInputParams.SeparateSyncsSupported
- WmiMonitorAnalogVideoInputParams.SerrationOfVsyncRequired
- WmiMonitorAnalogVideoInputParams.SetupExpected
- WmiMonitorAnalogVideoInputParams.SignalLevelStandard
- WmiMonitorAnalogVideoInputParams.SyncOnGreenVideoSupported
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 900bf4353de0c81acb5aa2c69578256b0212a2c0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127013092"
---
# <a name="wmimonitoranalogvideoinputparams-class"></a>WmiMonitorAnalogVideoInputParams, classe

La classe WMI **WmiMonitorAnalogVideoInputParams** représente les paramètres d’entrée de vidéo analogique d’un moniteur d’ordinateur. Les données de cette classe correspondent aux données de la définition d’entrée vidéo de la norme E-EDID (Extended Display Identification Data) améliorée de l’Association Video Electronics standard Association (VESA). Une instance de cette classe est disponible uniquement lorsque la valeur de la propriété **VideoInputType** de la classe [**WmiMonitorBasicDisplayParams**](wmimonitorbasicdisplayparams.md) est « Analog ».

## <a name="syntax"></a>Syntaxe

``` syntax
class WmiMonitorAnalogVideoInputParams : MSMonitorClass
{
  boolean Active;
  uint8   CompositeSyncSupported;
  string  InstanceName;
  uint8   SeparateSyncsSupported;
  uint8   SerrationOfVsyncRequired;
  uint8   SetupExpected;
  uint8   SignalLevelStandard;
  uint8   SyncOnGreenVideoSupported;
};
```

## <a name="members"></a>Membres

La classe **WmiMonitorAnalogVideoInputParams** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **WmiMonitorAnalogVideoInputParams** possède les propriétés suivantes.

<dl> <dt>

**Actif**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique le moniteur actif.

</dd> <dt>

**CompositeSyncSupported**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la synchronisation composite est prise en charge.



| Valeur                                                                              | Signification                                                             |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | La synchronisation composite sur la ligne de synchronisation horizontale est prise en charge.<br/>     |
| <dl> <dt>1 (0x1)</dt> </dl> | La synchronisation composite sur la ligne de synchronisation horizontale n’est pas prise en charge.<br/> |



 

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

**SeparateSyncsSupported**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si les synchronisations distinctes sont prises en charge.



| Valeur                                                                              | Signification                                      |
|------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | Les synchronisations distinctes sont prises en charge.<br/>     |
| <dl> <dt>1 (0x1)</dt> </dl> | Les synchronisations distinctes ne sont pas prises en charge.<br/> |



 

</dd> <dt>

**SerrationOfVsyncRequired**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si l’impulsion de synchronisation verticale serration est requise.



| Valeur                                                                              | Signification                                                                                                             |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | Serration de l’impulsion de synchronisation verticale est nécessaire lors de l’utilisation d’une synchronisation composite ou d’une vidéo en vert.<br/>     |
| <dl> <dt>1 (0x1)</dt> </dl> | Le serration de l’impulsion de synchronisation verticale n’est pas requis lorsque la synchronisation composite ou la vidéo de synchronisation en vert est utilisée.<br/> |



 

</dd> <dt>

**SetupExpected**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si l’installation est attendue.



| Valeur                                                                              | Signification                                                                                                                   |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | Le moniteur attend une installation vide ou un socle pour chaque niveau de signal approprié.<br/>                      |
| <dl> <dt>1 (0x1)</dt> </dl> | Le moniteur ne s’attend pas à une installation vide ou à un socle en fonction de la norme de niveau de signal appropriée.<br/> |



 

</dd> <dt>

**SignalLevelStandard**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Norme de niveau de signal pour les connexions EVC (Enhanced Video Connector).



| Valeur                                                                              | Signification                     |
|------------------------------------------------------------------------------------|-----------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | 0,7, 0.3 \[ V\]<br/>     |
| <dl> <dt>1 (0x1)</dt> </dl> | 0.714, 0.286 \[ V\]<br/> |
| <dl> <dt>2 (0X2)</dt> </dl> | 1,0, 0,4 \[ V\]<br/>     |
| <dl> <dt>3 (0x3)</dt> </dl> | 0,7, 0.0 \[ V\]<br/>     |



 

</dd> <dt>

**SyncOnGreenVideoSupported**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si la synchronisation sur le vert est prise en charge.



| Valeur                                                                              | Signification                                          |
|------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | La synchronisation sur Green Video est prise en charge.<br/>     |
| <dl> <dt>1 (0x1)</dt> </dl> | La synchronisation sur une vidéo verte n’est pas prise en charge.<br/> |



 

</dd> </dl>

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

 

 




