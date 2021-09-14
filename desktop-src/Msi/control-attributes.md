---
description: Pour plus d’informations sur les attributs de contrôle, consultez le lien vers le contrôle particulier que vous devez créer dans les contrôles, ainsi que les liens vers des attributs de contrôle particuliers dans les listes suivantes.
ms.assetid: 948ce3d3-e463-40de-8b5f-21ef18b1a0ce
title: Attributs du contrôle
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61d026e84dadefa67ce9d6e00146c6e1c2017cb9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127091981"
---
# <a name="control-attributes"></a>Attributs du contrôle

Pour plus d’informations sur les attributs de contrôle, consultez le lien vers le contrôle particulier que vous devez créer dans les [contrôles](controls.md) , ainsi que les liens vers des attributs de contrôle particuliers dans les listes suivantes.

Les méthodes suivantes sont utilisées pour spécifier les attributs d’un contrôle :

-   Utilisez la [table ControlCondition](controlcondition-table.md) pour désactiver, activer, masquer ou afficher un contrôle en fonction de la valeur d’une propriété ou d’une instruction conditionnelle. Vous pouvez également utiliser ce tableau pour remplacer le contrôle par défaut spécifié dans la [table de boîtes de dialogue](dialog-table.md).
-   Abonnez le contrôle à un ControlEvent, dans la [table EventMapping](eventmapping-table.md). Entrez l’identificateur de l’attribut dans la colonne d’attribut et l’identificateur de ControlEvent, dans la colonne d’événement de cette table.
-   Définissez les indicateurs de bits d’attribut de contrôle pour le contrôle dans la colonne attribut de la [table de contrôle](control-table.md). Cela définit les attributs lors de la création du contrôle.

Certains attributs ne peuvent pas être définis pour chaque contrôle ou être spécifiés par toutes les méthodes ci-dessus. Pour plus d’informations, consultez les rubriques de contrôle et d’attribut spécifiques.

Les valeurs initiales de certains attributs de contrôle peuvent être définies avec des bits dans la [table de contrôle](control-table.md).



| Attribut                                          | Decimal | Valeur hexadécimale | Constante                               |
|----------------------------------------------------|---------|-------------|----------------------------------------|
| [BiDi](bidi-control-attribute.md)                 | 224     | 0x000000E0  | **msidbControlAttributesBiDi**         |
| [Activé](enabled-control-attribute.md)           | 2       | 0x00000002  | **msidbControlAttributesEnabled**      |
| [Indirect](indirect-control-attribute.md)         | 8       | 0x00000008  | **msidbControlAttributesIndirect**     |
| [Contrôle entier](integer-control-attribute.md)   | 16      | 0x00000010  | **msidbControlAttributesInteger**      |
| [LeftScroll](leftscroll-control-attribute.md)     | 128     | 0x00000080  | **msidbControlAttributesLeftScroll**   |
| [RightAligned](rightaligned-control-attribute.md) | 64      | 0x00000040  | **msidbControlAttributesRightAligned** |
| [RTLRO](rtlro-control-attribute.md)               | 32      | 0x00000020  | **msidbControlAttributesRTLRO**        |
| [Sunken](sunken-control-attribute.md)             | 4       | 0x00000004  | **msidbControlAttributesSunken**       |
| [Visible](visible-control-attribute.md)           | 1       | 0x00000001  | **msidbControlAttributesVisible**      |



 

Ces attributs de contrôles de texte sont définis avec bits.



| Attribut                                            | Decimal | Valeur hexadécimale | Constante                                |
|------------------------------------------------------|---------|-------------|-----------------------------------------|
| [Formatage](formatsize-control-attribute.md)       | 524 288  | 0x00080000  | **msidbControlAttributesFormatSize**    |
| [Préfixe](noprefix-control-attribute.md)           | 131 072  | 0x00020000  | **msidbControlAttributesNoPrefix**      |
| [NoWrap](nowrap-control-attribute.md)               | 262 144  | 0x00040000  | **msidbControlAttributesNoWrap**        |
| [Mot de passe](password-control-attribute.md)           | 2 097 152 | 0x00200000  | **msidbControlAttributesPasswordInput** |
| [Transparente](transparent-control-attribute.md)     | 65536   | 0x00010000  | **msidbControlAttributesTransparent**   |
| [UsersLanguage](userslanguage-control-attribute.md) | 1 048 576 | 0x00100000  | **msidbControlAttributesUsersLanguage** |



 

Cet attribut du contrôle ProgressBar est défini avec un bit.



| Attribut                                      | Decimal | Valeur hexadécimale | Constante                             |
|------------------------------------------------|---------|-------------|--------------------------------------|
| [Progress95](progress95-control-attribute.md) | 65536   | 0x00010000  | **msidbControlAttributesProgress95** |



 

Ces attributs des contrôles SelectCombo des volumes et des répertoires sont définis avec bits.



| Attribut                                                | Decimal | Valeur hexadécimale | Constante                                  |
|----------------------------------------------------------|---------|-------------|-------------------------------------------|
| [CDROMVolume](cdromvolume-control-attribute.md)         | 524 288  | 0x00080000  | **msidbControlAttributesCDROMVolume**     |
| [FixedVolume](fixedvolume-control-attribute.md)         | 131 072  | 0x00020000  | **msidbControlAttributesFixedVolume**     |
| [FloppyVolume](floppyvolume-control-attribute.md)       | 2 097 152 | 0x00200000  | **msidbControlAttributesFloppyVolume**    |
| [RAMDiskVolume](ramdiskvolume-control-attribute.md)     | 1 048 576 | 0x00100000  | **msidbControlAttributesRAMDiskVolume**   |
| [RemoteVolume](remotevolume-control-attribute.md)       | 262 144  | 0x00040000  | **msidbControlAttributesRemoteVolume**    |
| [RemovableVolume](removablevolume-control-attribute.md) | 65536   | 0x00010000  | **msidbControlAttributesRemovableVolume** |



 

Ces attributs des contrôles ListBox et ComboBox sont définis avec bits.



| Attribut                                            | Decimal | Valeur hexadécimale | Constante                            |
|------------------------------------------------------|---------|-------------|-------------------------------------|
| [Contrôle ComboList](combolist-control-attribute.md) | 131 072  | 0x00020000  | **msidbControlAttributesComboList** |
| [Contrôle trié](sorted-control-attribute.md)       | 65536   | 0x00010000  | **msidbControlAttributesSorted**    |



 

Cet attribut du contrôle d’édition est défini avec un bit.



| Attribut                                    | Decimal | Valeur hexadécimale | Constante                            |
|----------------------------------------------|---------|-------------|-------------------------------------|
| [Lambda](multiline-control-attribute.md) | 65536   | 0x00010000  | **msidbControlAttributesMultiline** |



 

Ces attributs des contrôles PictureButton sont définis avec bits.



| Attribut                                          | Decimal | Valeur hexadécimale | Constante                             |
|----------------------------------------------------|---------|-------------|--------------------------------------|
| [Bitmap](bitmap-control-attribute.md)             | 262 144  | 0x00040000  | **msidbControlAttributesBitmap**     |
| [FixedSize](fixedsize-control-attribute.md)       | 1 048 576 | 0x00100000  | **msidbControlAttributesFixedSize**  |
| [Icône](icon-control-attribute.md)                 | 524 288  | 0x00080000  | **msidbControlAttributesIcon**       |
| [IconSize16](iconsize-control-attribute.md)       | 2 097 152 | 0x00200000  | **msidbControlAttributesIconSize16** |
| [IconSize32](iconsize-control-attribute.md)       | 4 194 304 | 0x00400000  | **msidbControlAttributesIconSize32** |
| [IconSize48](iconsize-control-attribute.md)       | 6291456 | 0x00600000  | **msidbControlAttributesIconSize48** |
| [Contrôle PushLike](pushlike-control-attribute.md) | 131 072  | 0x00020000  | **msidbControlAttributesPushLike**   |



 

Cet attribut du contrôle RadioButton est défini avec un bit.



| Attribut                                    | Decimal  | Valeur hexadécimale | Constante                            |
|----------------------------------------------|----------|-------------|-------------------------------------|
| [HasBorder](hasborder-control-attribute.md) | 16 777 216 | 0x01000000  | **msidbControlAttributesHasBorder** |



 

Cet attribut du contrôle PushButton est défini avec un bit.



| Attribut                                        | Decimal | Valeur hexadécimale | Constante                                  |
|--------------------------------------------------|---------|-------------|-------------------------------------------|
| [ElevationShield](elevationshield-attribute.md) | 8388608 | 0x00800000  | **msidbControlAttributesElevationShield** |



 

Cet attribut du contrôle VolumeCostList est défini sur un bit.



| Attribut                                                                | Decimal | Valeur hexadécimale | Constante                         |
|--------------------------------------------------------------------------|---------|-------------|----------------------------------|
| [ControlShowRollbackCost](controlshowrollbackcost-control-attribute.md) | 4 194 304 | 0x00400000  | **msidbControlShowRollbackCost** |



 

Les attributs de contrôle suivants ne sont pas définis avec bits. Ces attributs sont créés dans les tables de l’interface utilisateur ou sont définis à l’aide d' [événements de contrôle](control-events.md).

[BillboardName](billboardname-control-attribute.md)

 

[IndirectPropertyName](indirectpropertyname-control-attribute.md)

 

[Position](position-control-attribute.md)

 

[Contrôle de progression](progress-control-attribute.md)

 

[PropertyName](propertyname-control-attribute.md)

 

[PropertyValue](propertyvalue-control-attribute.md)

 

[Text Control](text-control-attribute.md)

 

[TimeRemaining](timeremaining-control-attribute.md)

Consultez [Ajout de contrôles et de texte](adding-controls-and-text.md).

 

 



