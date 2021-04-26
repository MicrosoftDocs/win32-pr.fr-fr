---
description: Spécifie l’identificateur matériel PnP-X du service.
ms.assetid: aa4c935f-0d60-4603-ae96-d5cabdf9af00
title: Élément PnPXHardwareId
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0ffc389ca6df363439dd6463b3f86ca756359e8
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/26/2021
ms.locfileid: "107996526"
---
# <a name="pnpxhardwareid-element"></a>Élément PnPXHardwareId

Spécifie l’identificateur matériel PnP-X du service. PnP correspond à cet élément avec la ou les descriptions matérielles fournies dans \[ la \] section PnpxDevice du fichier INF de l’appareil. En fonction de ces informations, le service PnP sélectionne et charge le pilote de périphérique le plus approprié.

## <a name="usage"></a>Usage

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



## <a name="remarks"></a>Remarques

Pour spécifier plusieurs ID de matériel, séparez les identificateurs par un espace, par exemple, « PnPX \_ SampleService \_ HWID \_ 1 PnPX SampleService HWID \_ \_ \_ 2 PnPX SampleService1 \_ \_ HWID \_ 3 ».

## <a name="element-information"></a>Informations sur les éléments



| Étiquette | Value |
|-------------------------------------|---------------|
| Système minimal pris en charge<br/> | Windows Vista |
| Peut être vide                        | Oui           |



 

 




