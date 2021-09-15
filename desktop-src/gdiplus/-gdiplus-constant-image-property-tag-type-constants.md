---
description: Vous pouvez stocker et récupérer des métadonnées d’image à l’aide d’un objet PropertyItem. Le type de données membre d’un objet PropertyItem spécifie le type de données des valeurs stockées dans le membre de données de valeur de ce même objet PropertyItem.
ms.assetid: d05cdf42-4b30-45ce-85a1-025d4f4e9d13
title: Constantes de type de balise de propriété d’image (Gdiplusimaging. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b1870ad117d8c6f84af9e48f88e94f812c59467
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127525856"
---
# <a name="image-property-tag-type-constants"></a>Constantes de type de balise de propriété d’image

Vous pouvez stocker et récupérer des métadonnées d’image à l’aide d’un objet [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) . Le **type** de données membre d’un objet **PropertyItem** spécifie le type de données des valeurs stockées dans le membre de données de valeur de ce même objet **PropertyItem** .

Les constantes suivantes, définies dans Gdiplusimaging. h, peuvent être assignées au **type** de données membre d’un objet [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) .



| Constante                                                                                                                                                                                                                                 | Description                                                                                                                                                                                                                                                                                                                                                                              |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="PixelFormat4bppIndexed"></span><span id="pixelformat4bppindexed"></span><span id="PIXELFORMAT4BPPINDEXED"></span><dl> <dt>**PixelFormat4bppIndexed**</dt> </dl>         | Spécifie que le format est 4 bits par pixel, indexés.<br/>                                                                                                                                                                                                                                                                                                                       |
| <span id="PropertyTagTypeASCII"></span><span id="propertytagtypeascii"></span><span id="PROPERTYTAGTYPEASCII"></span><dl> <dt>**PropertyTagTypeASCII**</dt> </dl>                 | Spécifie que le membre de données de la **valeur** est une chaîne ASCII terminée par le caractère null. Si vous définissez le **type** de données membre d’un objet [**PropertyItem**](/windows/win32/api/gdiplusimaging/nl-gdiplusimaging-propertyitem) sur PropertyTagTypeASCII, vous devez définir **la longueur du membre de données à** la longueur de la chaîne, y compris la marque de fin null. Par exemple, la chaîne `HELLO` aurait une longueur de 6.<br/> |
| <span id="PropertyTagTypeByte"></span><span id="propertytagtypebyte"></span><span id="PROPERTYTAGTYPEBYTE"></span><dl> <dt>**PropertyTagTypeByte**</dt> </dl>                     | Spécifie que le membre de données de **valeur** est un tableau d’octets.<br/>                                                                                                                                                                                                                                                                                                                |
| <span id="PropertyTagTypeLong"></span><span id="propertytagtypelong"></span><span id="PROPERTYTAGTYPELONG"></span><dl> <dt>**PropertyTagTypeLong**</dt> </dl>                     | Spécifie que le membre de données de **valeur** est un tableau d’entiers longs non signés (32 bits).<br/>                                                                                                                                                                                                                                                                                      |
| <span id="PropertyTagTypeRational"></span><span id="propertytagtyperational"></span><span id="PROPERTYTAGTYPERATIONAL"></span><dl> <dt>**PropertyTagTypeRational**</dt> </dl>     | Spécifie que le membre de données de **valeur** est un tableau de paires d’entiers longs non signés. Chaque paire représente une fraction ; le premier entier est le numérateur et le deuxième entier est le dénominateur.<br/>                                                                                                                                                                       |
| <span id="PropertyTagTypeShort"></span><span id="propertytagtypeshort"></span><span id="PROPERTYTAGTYPESHORT"></span><dl> <dt>**PropertyTagTypeShort**</dt> </dl>                 | Spécifie que le membre de données de **valeur** est un tableau d’entiers non signés courts (16 bits).<br/>                                                                                                                                                                                                                                                                                     |
| <span id="PropertyTagTypeSLONG"></span><span id="propertytagtypeslong"></span><span id="PROPERTYTAGTYPESLONG"></span><dl> <dt>**PropertyTagTypeSLONG**</dt> </dl>                 | Spécifie que le membre de données de **valeur** est un tableau d’entiers longs signés (32 bits).<br/>                                                                                                                                                                                                                                                                                        |
| <span id="PropertyTagTypeSRational"></span><span id="propertytagtypesrational"></span><span id="PROPERTYTAGTYPESRATIONAL"></span><dl> <dt>**PropertyTagTypeSRational**</dt> </dl> | Spécifie que le membre de données de **valeur** est un tableau de paires d’entiers longs signés. Chaque paire représente une fraction ; le premier entier est le numérateur et le deuxième entier est le dénominateur.<br/>                                                                                                                                                                         |
| <span id="PropertyTagTypeUndefined"></span><span id="propertytagtypeundefined"></span><span id="PROPERTYTAGTYPEUNDEFINED"></span><dl> <dt>**PropertyTagTypeUndefined**</dt> </dl> | Spécifie que le membre de données de **valeur** est un tableau d’octets pouvant contenir des valeurs de n’importe quel type de données. <br/>                                                                                                                                                                                                                                                                         |



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Gdiplusimaging. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Constantes de balise de propriété d’image](-gdiplus-constant-image-property-tag-constants.md)
</dt> <dt>

[Spécifications des formats de fichiers image](-gdiplus-constant-image-file-format-specifications.md)
</dt> <dt>

[Lecture et écriture de métadonnées](-gdiplus-reading-and-writing-metadata-use.md)
</dt> </dl>

 

 
