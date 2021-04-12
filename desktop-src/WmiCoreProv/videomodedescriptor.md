---
description: Contient des éléments de descripteur de mode pour le tableau MonitorSourceModes dans la classe WmiMonitorListedSupportedSourceModes.
ms.assetid: 6d6c846d-caec-41a8-8a88-1c1e14bc0473
title: VideoModeDescriptor, classe
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- VideoModeDescriptor
- VideoModeDescriptor.CompositePolarityType
- VideoModeDescriptor.HorizontalActivePixels
- VideoModeDescriptor.HorizontalBlankingPixels
- VideoModeDescriptor.HorizontalBorder
- VideoModeDescriptor.HorizontalImageSize
- VideoModeDescriptor.HorizontalPolarityType
- VideoModeDescriptor.HorizontalRefreshRateDenominator
- VideoModeDescriptor.HorizontalRefreshRateNumerator
- VideoModeDescriptor.HorizontalSyncOffset
- VideoModeDescriptor.HorizontalSyncPulseWidth
- VideoModeDescriptor.IsInterlaced
- VideoModeDescriptor.IsSerrationRequired
- VideoModeDescriptor.IsSyncOnRGB
- VideoModeDescriptor.PixelClockRate
- VideoModeDescriptor.StereoModeType
- VideoModeDescriptor.SyncSignalType
- VideoModeDescriptor.VerticalActivePixels
- VideoModeDescriptor.VerticalBlankingPixels
- VideoModeDescriptor.VerticalBorder
- VideoModeDescriptor.VerticalImageSize
- VideoModeDescriptor.VerticalRefreshRateDenominator
- VideoModeDescriptor.VerticalRefreshRateNumerator
- VideoModeDescriptor.VerticalSyncOffset
- VideoModeDescriptor.VerticalPolarityType
- VideoModeDescriptor.VerticalSyncPulseWidth
- VideoModeDescriptor.VideoStandardType
api_type:
- DllExport
api_location:
- WmiProv.dll
ms.openlocfilehash: 06094b24b6b8197eab89b65cd5a9a83f46b39f95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320346"
---
# <a name="videomodedescriptor-class"></a>VideoModeDescriptor, classe

La classe WMI **VideoModeDescriptorVideo** contient des éléments de descripteur de mode pour le tableau **MonitorSourceModes** dans la classe [**WmiMonitorListedSupportedSourceModes**](wmimonitorlistedsupportedsourcemodes.md) . Ces éléments incluent des fonctionnalités de surveillance telles que la fréquence de rafraîchissement, les caractéristiques des pixels ou la taille de l’image. La classe **VideoModeDescriptorVideo** contient des informations qui sont un sur-ensemble des données disponibles à partir de blocs de synchronisation établis, standard et détaillés.

## <a name="syntax"></a>Syntaxe

``` syntax
class VideoModeDescriptor : WmiMonitorSupportedVideoModes
{
  uint8   CompositePolarityType;
  uint16  HorizontalActivePixels;
  uint16  HorizontalBlankingPixels;
  uint16  HorizontalBorder;
  uint16  HorizontalImageSize;
  uint8   HorizontalPolarityType;
  uint16  HorizontalRefreshRateDenominator;
  uint16  HorizontalRefreshRateNumerator;
  uint16  HorizontalSyncOffset;
  uint16  HorizontalSyncPulseWidth;
  boolean IsInterlaced;
  uint8   IsSerrationRequired;
  uint8   IsSyncOnRGB;
  uint32  PixelClockRate;
  uint8   StereoModeType;
  uint8   SyncSignalType;
  uint16  VerticalActivePixels;
  uint16  VerticalBlankingPixels;
  uint16  VerticalBorder;
  uint16  VerticalImageSize;
  uint16  VerticalRefreshRateDenominator;
  uint16  VerticalRefreshRateNumerator;
  uint16  VerticalSyncOffset;
  uint8   VerticalPolarityType;
  uint16  VerticalSyncPulseWidth;
  uint8   VideoStandardType;
};
```

## <a name="members"></a>Membres

La classe **VideoModeDescriptor** possède les types de membres suivants :

-   [Propriétés](#properties)

### <a name="properties"></a>Propriétés

La classe **VideoModeDescriptor** possède les propriétés suivantes.

<dl> <dt>

**CompositePolarityType**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Type de polarité composite. Il s’agit de la polarité des impulsions de synchronisation horizontale en dehors de la synchronisation verticale.



| Valeur                                                                              | Signification                                                                    |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | La polarité composite est positive.<br/>                                 |
| <dl> <dt>1 (0x1)</dt> </dl> | La polarité composite est négative.<br/>                                 |
| <dl> <dt>2 (0X2)</dt> </dl> | Non applicable. Le type de synchronisation de signal doit être numérique composite.<br/> |



 

</dd> <dt>

**HorizontalActivePixels**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre de pixels actifs horizontalement.

</dd> <dt>

**HorizontalBlankingPixels**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre de pixels à blanc horizontal

</dd> <dt>

**HorizontalBorder**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Bordure horizontale.

</dd> <dt>

**HorizontalImageSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Taille de l’image horizontale en millimètres (mm).

</dd> <dt>

**HorizontalPolarityType**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Type de polarité horizontale.



| Valeur                                                                              | Signification                                                                   |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | La polarité horizontale est positive.<br/>                               |
| <dl> <dt>1 (0x1)</dt> </dl> | La polarité horizontale est négative.<br/>                               |
| <dl> <dt>2 (0X2)</dt> </dl> | Non applicable. Le type de synchronisation de signal doit être séparé par un numérique.<br/> |



 

</dd> <dt>

**HorizontalRefreshRateDenominator**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Dénominateur du taux de rafraîchissement horizontal.

</dd> <dt>

**HorizontalRefreshRateNumerator**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Numérateur du taux de rafraîchissement horizontal en Hertz (Hz).

</dd> <dt>

**HorizontalSyncOffset**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Décalage de synchronisation horizontale.

</dd> <dt>

**HorizontalSyncPulseWidth**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Largeur d’impulsion de synchronisation horizontale.

</dd> <dt>

**IsInterlaced**
</dt> <dd> <dl> <dt>

Type de données : **booléen**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique si le mode d’affichage est entrelacé.

</dd> <dt>

**IsSerrationRequired**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique le type de serration requis, le cas échéant.



| Valeur                                                                              | Signification                                                                                                  |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | Le contrôleur doit fournir une synchronisation horizontale pendant la synchronisation verticale.<br/>                                 |
| <dl> <dt>1 (0x1)</dt> </dl> | Le contrôleur ne doit pas fournir de synchronisation horizontale pendant la synchronisation verticale.<br/>                             |
| <dl> <dt>2 (0X2)</dt> </dl> | Non applicable. Le type de synchronisation de signal doit être bipolaire, composite analogique ou composite numérique.<br/> |



 

</dd> <dt>

**IsSyncOnRGB**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Indique les lignes de signal vidéo à synchroniser, le cas échéant.



| Valeur                                                                              | Signification                                                                           |
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | L’impulsion de synchronisation doit apparaître sur les 3 lignes de signal vidéo.<br/>                  |
| <dl> <dt>1 (0x1)</dt> </dl> | L’impulsion de synchronisation doit apparaître uniquement sur la ligne de signal vidéo verte.<br/>          |
| <dl> <dt>2 (0X2)</dt> </dl> | Non applicable. Le type de synchronisation de signal doit être composite analogique bipolaire.<br/> |



 

</dd> <dt>

**PixelClockRate**
</dt> <dd> <dl> <dt>

Type de données : **UInt32**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Fréquence d’horloge en Hertz (Hz).

</dd> <dt>

**StereoModeType**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Type de mode stéréo. Le tableau suivant répertorie les valeurs possibles.



| Valeur                                                                              | Signification                                                             |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | Pas de stéréo.<br/>                                               |
| <dl> <dt>1 (0x1)</dt> </dl> | Champ stéréo séquentiel avec image de droite sur synchronisation stéréo.<br/> |
| <dl> <dt>2 (0X2)</dt> </dl> | Champ stéréo séquentiel avec image de gauche sur synchronisation stéréo.<br/>  |
| <dl> <dt>3 (0x3)</dt> </dl> | Stéréo entrelacée bidirectionnelle avec image de droite sur les lignes paires.<br/> |
| <dl> <dt>4 (0x4)</dt> </dl> | Stéréo entrelacée bidirectionnelle avec image de gauche sur les lignes paires.<br/>  |
| <dl> <dt>5 (0x5)</dt> </dl> | Stéréo entrelacée à 4 voies.<br/>                                |
| <dl> <dt>6 (0x6)</dt> </dl> | Stéréo entrelacée côte à côte.<br/>                         |



 

</dd> <dt>

**SyncSignalType**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Type de synchronisation de signal. Le tableau suivant répertorie les valeurs possibles.



| Valeur                                                                              | Signification                             |
|------------------------------------------------------------------------------------|-------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | Composite analogique<br/>         |
| <dl> <dt>1 (0x1)</dt> </dl> | Composite analogique bipolaire<br/> |
| <dl> <dt>2 (0X2)</dt> </dl> | Composite numérique<br/>        |
| <dl> <dt>3 (0x3)</dt> </dl> | Séparation numérique<br/>         |



 

</dd> <dt>

**VerticalActivePixels**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre de pixels actifs verticalement.

</dd> <dt>

**VerticalBlankingPixels**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Nombre de pixels à espacement horizontal.

</dd> <dt>

**VerticalBorder**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Bordure verticale.

</dd> <dt>

**VerticalImageSize**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Taille de l’image verticale en millimètres (mm).

</dd> <dt>

**VerticalPolarityType**
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Type de polarité verticale.



| Valeur                                                                              | Signification                                                                   |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl> | La polarité verticale est positive.<br/>                                 |
| <dl> <dt>1 (0x1)</dt> </dl> | La polarité verticale est négative<br/>                                  |
| <dl> <dt>2 (0X2)</dt> </dl> | Non applicable. Le type de synchronisation de signal doit être séparé par un numérique.<br/> |



 

</dd> <dt>

**VerticalRefreshRateDenominator**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Dénominateur de la fréquence d’actualisation verticale.

</dd> <dt>

**VerticalRefreshRateNumerator**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Numérateur de fréquence d’actualisation verticale en Hertz (Hz).

</dd> <dt>

**VerticalSyncOffset**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Décalage de synchronisation verticale.

</dd> <dt>

**VerticalSyncPulseWidth**
</dt> <dd> <dl> <dt>

Type de données : **UInt16**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Largeur d’impulsion de synchronisation verticale.

</dd> <dt>

VideoStandardType
</dt> <dd> <dl> <dt>

Type de données : **UInt8**
</dt> <dt>

Type d'accès : Lecture seule
</dt> </dl>

Type de vidéo standard.



| Valeur                                                                                | Signification                                                                                                        |
|--------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <dl> <dt>0 (0x0)</dt> </dl>   | Autres<br/>                                                                                               |
| <dl> <dt>1 (0x1)</dt> </dl>   | VESA DMT. À partir de Video Electronics standard Association (VESA), affichez la spécification des minutages de moniteur.<br/> |
| <dl> <dt>2 (0X2)</dt> </dl>   | GTF VESA. À partir de la norme de formule de minutage généralisée VESA.<br/>                                            |
| <dl> <dt>3 (0x3)</dt> </dl>   | VESA CVT/à partir de la norme des minutages vidéo coordonné VESA.<br/>                                             |
| <dl> <dt>4 (0x4)</dt> </dl>   | IBM<br/>                                                                                                 |
| <dl> <dt>5 (0x5)</dt> </dl>   | pomme<br/>                                                                                               |
| <dl> <dt>6 (0x6)</dt> </dl>   | NTSC M<br/>                                                                                              |
| <dl> <dt>7 (0x7)</dt> </dl>   | NTSC J<br/>                                                                                              |
| <dl> <dt>8 (0x8)</dt> </dl>   | NTSC 433<br/>                                                                                            |
| <dl> <dt>9 (0x9)</dt> </dl>   | PAL B<br/>                                                                                               |
| <dl> <dt>10 (0xA)</dt> </dl>  | PAL B1<br/>                                                                                              |
| <dl> <dt>11 (0xB)</dt> </dl>  | PAL G<br/>                                                                                               |
| <dl> <dt>12 (0xC)</dt> </dl>  | PAL H<br/>                                                                                               |
| <dl> <dt>13 (0xD)</dt> </dl>  | PAL I<br/>                                                                                               |
| <dl> <dt>14 (0xE)</dt> </dl>  | PAL D<br/>                                                                                               |
| <dl> <dt>15 (0xF)</dt> </dl>  | PAL N<br/>                                                                                               |
| <dl> <dt>16 (0x10)</dt> </dl> | CONTEXTE DE NOMMAGE PAL<br/>                                                                                              |
| <dl> <dt>17 (0x11)</dt> </dl> | SECAM B<br/>                                                                                             |
| <dl> <dt>18 (0x12)</dt> </dl> | SECAM D<br/>                                                                                             |
| <dl> <dt>19 (0x13)</dt> </dl> | SECAM G<br/>                                                                                             |
| <dl> <dt>20 (0x14)</dt> </dl> | SECAM H<br/>                                                                                             |
| <dl> <dt>21 (0x15)</dt> </dl> | SECAM K<br/>                                                                                             |
| <dl> <dt>22 (0x16)</dt> </dl> | SECAM K1<br/>                                                                                            |
| <dl> <dt>23 (0x17)</dt> </dl> | SECAM L<br/>                                                                                             |
| <dl> <dt>24 (0x18)</dt> </dl> | SECAM L1<br/>                                                                                            |
| <dl> <dt>25 (0x19)</dt> </dl> | EIA861<br/>                                                                                              |
| <dl> <dt>26 (0x1A)</dt> </dl> | EIA861A<br/>                                                                                             |
| <dl> <dt>27 (0x1B)</dt> </dl> | EIA861B<br/>                                                                                             |



 

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

 

 




