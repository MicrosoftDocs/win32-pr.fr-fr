---
description: Spécifie l’identificateur matériel PnP-X du service.
ms.assetid: aa4c935f-0d60-4603-ae96-d5cabdf9af00
title: Élément PnPXHardwareId
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55e5e38b669a289545225df96fad05e55069b474
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106517779"
---
# <a name="pnpxhardwareid-element"></a>Élément PnPXHardwareId

Spécifie l’identificateur matériel PnP-X du service. PnP correspond à cet élément avec la ou les descriptions matérielles fournies dans \[ la \] section PnpxDevice du fichier INF de l’appareil. En fonction de ces informations, le service PnP sélectionne et charge le pilote de périphérique le plus approprié.

## <a name="usage"></a>Utilisation

``` syntax
<PnPXHardwareId/>
```

## <a name="attributes"></a>Attributs

Il n’y a pas d’attributs.

## <a name="child-elements"></a>Éléments enfants

Il n’y a pas d’éléments enfants.

## <a name="parent-elements"></a>Éléments parents



| Élément                             | Description                                                                            |
|-------------------------------------|----------------------------------------------------------------------------------------|
| [**Hébergement**](hosted.md)<br/> | Définit des éléments pour les services définis par l’hôte de service. <br/> <br/> |



## <a name="remarks"></a>Notes

Pour spécifier plusieurs ID de matériel, séparez les identificateurs par un espace, par exemple, « PnPX \_ SampleService \_ HWID \_ 1 PnPX SampleService HWID \_ \_ \_ 2 PnPX SampleService1 \_ \_ HWID \_ 3 ».

## <a name="element-information"></a>Informations sur les éléments



|                                     |               |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Oui           |



 

 




