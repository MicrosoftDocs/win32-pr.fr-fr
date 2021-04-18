---
description: L’acquisition d’images Windows (WIA) fournit des objets d’automatisation pour une utilisation dans les langages de script, tels que les logiciels de développement Microsoft JScript et Microsoft Visual Basic Scripting Edition (VBScript), ainsi que des langages de programmation de haut niveau tels que le système de développement Microsoft Visual Basic.
ms.assetid: 3d294db3-3349-4b26-aae1-1e3f588a0f0e
title: Modèle de script WIA
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e70863e60e0d7aa6172bd9c93240f38cac27c6be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519310"
---
# <a name="wia-scripting-model"></a>Modèle de script WIA

L’acquisition d’images Windows (WIA) fournit des objets d’automatisation pour une utilisation dans les langages de script, tels que les logiciels de développement Microsoft JScript et Microsoft Visual Basic Scripting Edition (VBScript), ainsi que des langages de programmation de haut niveau tels que le système de développement Microsoft Visual Basic.

> [!Note]  
> Ce système de script a été remplacé par la couche d’automatisation de l’acquisition d’images Windows (WIA). Voir [couche d’automatisation de l’acquisition d’image Windows](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage).

 

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

 

 
