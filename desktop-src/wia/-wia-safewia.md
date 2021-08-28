---
description: l’objet SafeWia est un &\# 0034 ; safe pour les scripts&\# 0034 ; point d’entrée pour toutes les fonctionnalités de script de l’acquisition d’images Windows (WIA).
ms.assetid: 6b10bb8e-8500-4f2c-ae18-5db78ef75f74
title: Objet SafeWia
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SafeWia
api_type:
- COM
api_location:
- Wiascr.dll
ms.openlocfilehash: ef324934abee38e2581b6e05c0fdac92145e4f43
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473845"
---
# <a name="safewia-object"></a>Objet SafeWia

l’objet **SafeWia** est un point d’entrée « sécurisé pour le script » pour toutes les fonctionnalités de script de l’acquisition d’images (WIA) Windows. Toute application qui utilise le modèle de script WIA doit créer un objet **SafeWia** ou [**WIA**](-wia-wia.md) . Utilisez cet objet pour énumérer et créer des appareils et recevoir des notifications d’événements matériels.

## <a name="members"></a>Membres

L’objet **SafeWia** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **SafeWia** a ces méthodes.



| Méthode                             | Description                                                                                                                                                                                                                |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Créer**](-wia-iwia-create.md) | La méthode [**Create**](-wia-iwia-create.md) de l’objet [**WIA**](-wia-wia.md) établit une connexion à l’appareil WIA spécifié et retourne un objet [**Item**](-wia-item.md) qui représente l’appareil.<br/> |



 

### <a name="properties"></a>Propriétés

L’objet **SafeWia** a ces propriétés.




| Propriété | Type d’accès | Description | 
|----------|-------------|-------------|
| <a href="-wia-iwia-devices.md"><strong>Appareils</strong></a><br /> | Lecture seule<br /> | Collection d’objets <a href="-wia-deviceinfo.md"><strong>DeviceInfo</strong></a> qui représentent tous les périphériques installés sur l’ordinateur. Lecture seule. <br /><blockquote>[!Note]<br />Cette collection est de base 0.</blockquote><br /> | 




 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (version 4,90 ou ultérieure)</dt> </dl> |
| IID<br/>                      | CLSID \_ SafeWia<br/>                                                                                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**WIA**](-wia-wia.md)
</dt> </dl>

 

 




