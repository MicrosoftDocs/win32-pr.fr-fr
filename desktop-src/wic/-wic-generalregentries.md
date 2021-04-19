---
description: Entrées de Registre générales
ms.assetid: 6a140c7f-df8c-4a8e-9e4d-dbb38901e14f
title: Entrées de Registre générales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d7c3514adcc0aeaaf9adadd2b71dfdffcd8d408
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106529293"
---
# <a name="general-registry-entries"></a>Entrées de Registre générales


Les entrées de Registre suivantes doivent être effectuées séparément pour le décodeur et l’encodeur :

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Encoder/Decoder CLSID}
         Author = Author's Name
         Description = Your Codec Description
         DeviceManufacturer = Manufacturer's Name
         DeviceModels = Device,Device
         FriendlyName = Codec Friendly Name
         Date = mm-dd-yyyy
         Vendor = {GUID_Vendor}
         ContainerFormat = {GUID_ContainerFormat}
         Version = Major.Minor.Build.Number
         SpecVersion = Major.Minor.Build.Number
         MimeTypes = Your Mime Type
         SupportAnimation = 0|1
         SupportChromakey = 0|1
         SupportLossless = 0|1
         SupportMultiframe = 0|1
         Formats
            {Supported PixelFormat GUID 1}
            {Supported PixelFormat GUID ...}
            {Supported PixelFormat GUID N}
         ArbitrationPriority  = 0-10
```

Les entrées FriendlyName, VendorGUID, ContainerFormat, MimeTypes, FileExtensions et formats sont requises. Toutes les autres sont facultatives.

Notez que les entrées DeviceManufacturer et DeviceModels sont spécifiques aux codecs bruts et font référence au fabricant de l’appareil photo et aux modèles d’appareil photo auxquels le codec est applicable. La version spec est la version de la spécification de format d’image avec laquelle le codec est conforme. L’entrée formats spécifie les formats de pixel pris en charge par le codec. Un codec peut prendre en charge plusieurs formats de pixel. Dans ce cas, vous devez entrer plusieurs clés sous HKEY \_ classes \_ racine \\ CLSID \\ {encodeur/décodeur CLSID} \\ .

## <a name="arbitrationpriority"></a>ArbitrationPriority

À compter de Windows 8, ArbitrationPriority est une nouvelle entrée de registre. Les valeurs valides sont comprises entre 0 et 10. Lorsque la clé ArbitrationPriority est présente, la valeur de cette clé indique au WIC de définir la priorité du codec associé derrière tous les autres codecs ayant une valeur ArbitrationPriority inférieure. Cette évaluation se produit avant l’arbitrage du codec WIC existant et garantit que le codec associé est classé en dessous d’un codec concurrent, même s’il est plus ou moins puissant. Tout codec qui n’a pas de valeur ArbitrationPriority explicite définie dans le registre aura par défaut la priorité 0.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Installation et inscription du CODEC](-wic-codecinstallandreg.md)
</dt> <dt>

[Entrées de Registre spécifiques à l’encodeur](-wic-encoderregentries.md)
</dt> <dt>

[Comment écrire un CODEC WIC-Enabled](-wic-howtowriteacodec.md)
</dt> <dt>

[Vue d’ensemble du composant Windows Imaging](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[**Fonctionnement du composant Windows Imaging : détection et arbitrage des codecs**](-wic-howwicworks.md)
</dt> </dl>

 

 



