---
description: Windows l’Acquisition d’images (WIA) fournit des objets d’automatisation pour une utilisation dans des langages de script, tels que microsoft JScript et microsoft Visual Basic scripting Edition (VBScript), ainsi que des langages de programmation de haut niveau tels que le système de développement microsoft Visual Basic.
ms.assetid: 3d294db3-3349-4b26-aae1-1e3f588a0f0e
title: Modèle de script WIA
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b558e84dd4095fd0d5dc3f1f14a7de76d9108c488cf3fc3613e3a09bc4830714
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119812849"
---
# <a name="wia-scripting-model"></a>Modèle de script WIA

Windows l’Acquisition d’images (WIA) fournit des objets d’automatisation pour une utilisation dans des langages de script, tels que microsoft JScript et microsoft Visual Basic scripting Edition (VBScript), ainsi que des langages de programmation de haut niveau tels que le système de développement microsoft Visual Basic.

> [!Note]  
> ce système de script a été remplacé par la couche d’automatisation d’acquisition d’images Windows (WIA). consultez [Windows couche automatisation](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage)de l’Acquisition d’images.

 

Le tableau suivant décrit les objets de script WIA et leur utilisation. 

| Object                                | Description                                                                                                                                                                                  |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WIA**](-wia-wia.md)               | Objet de script WIA de niveau supérieur. Utilisez l’objet [**WIA**](-wia-wia.md) pour énumérer et vous connecter à des appareils, et pour gérer des événements de périphérique matériel.                                        |
| [**DeviceInfo**](-wia-deviceinfo.md) | L’objet [**DeviceInfo**](-wia-deviceinfo.md) fournit l’accès aux informations sur les propriétés de l’appareil.                                                                                     |
| [**Élément**](-wia-item.md)             | Cet objet représente les éléments de périphérique, de fichier et de dossier WIA. Un périphérique matériel WIA et ses images ou lits d’analyse sont représentés sous la forme d’une arborescence hiérarchique d’objets [**Item**](-wia-item.md) . |



 

L’objet [**DeviceInfo**](-wia-deviceinfo.md) et l’objet [**Item**](-wia-item.md) sont associés à des objets de collection. Pour plus d’informations sur l’utilisation des objets de collection, consultez Utilisation des objets de collection WIA.

Les rubriques suivantes couvrent des informations générales sur l’utilisation du modèle de script WIA :

-   [Conventions de syntaxe](-wia-syntax-conventions.md)
-   [Utilisation d’objets de collection WIA](-wia-using-wia-collection-objects.md)
-   [Définitions de constantes de propriété WIA](-wia-wia-property-constant-definitions.md)

 

 
