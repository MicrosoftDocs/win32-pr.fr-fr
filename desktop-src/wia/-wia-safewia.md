---
description: L’objet SafeWia est un &\# 0034 ; Safe pour les scripts&\# 0034 ; point d’entrée pour toutes les fonctionnalités de script WIA (Windows Image Acquisition).
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
ms.openlocfilehash: 1f227180b7420f5c70ef64d7d1d3feb0f13ae164
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106514442"
---
# <a name="safewia-object"></a>Objet SafeWia

L’objet **SafeWia** est un point d’entrée « sécurisé pour le script » pour toutes les fonctionnalités de script WIA (Windows Image Acquisition). Toute application qui utilise le modèle de script WIA doit créer un objet **SafeWia** ou [**WIA**](-wia-wia.md) . Utilisez cet objet pour énumérer et créer des appareils et recevoir des notifications d’événements matériels.

## <a name="members"></a>Membres

L’objet **SafeWia** possède les types de membres suivants :

-   [Méthodes](#methods)
-   [Propriétés](#properties)

### <a name="methods"></a>Méthodes

L’objet **SafeWia** a ces méthodes.



| Méthode                             | Description                                                                                                                                                                                                                |
|:-----------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Créés**](-wia-iwia-create.md) | La méthode [**Create**](-wia-iwia-create.md) de l’objet [**WIA**](-wia-wia.md) établit une connexion à l’appareil WIA spécifié et retourne un objet [**Item**](-wia-item.md) qui représente l’appareil.<br/> |



 

### <a name="properties"></a>Propriétés

L’objet **SafeWia** a ces propriétés.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Propriété</th>
<th style="text-align: left;">Type d’accès</th>
<th style="text-align: left;">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><a href="-wia-iwia-devices.md"><strong>Appareils</strong></a><br/></td>
<td style="text-align: left;">Lecture seule<br/></td>
<td style="text-align: left;">Collection d’objets <a href="-wia-deviceinfo.md"><strong>DeviceInfo</strong></a> qui représentent tous les périphériques installés sur l’ordinateur. Lecture seule. <br/>
<blockquote>
[!Note]<br />
Cette collection est de base 0.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 professionnel, applications de \[ Bureau Windows XP uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                          |
| DLL<br/>                      | <dl> <dt>Wiascr.dll (version 4,90 ou ultérieure)</dt> </dl> |
| IID<br/>                      | CLSID \_ SafeWia<br/>                                                                                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**WIA**](-wia-wia.md)
</dt> </dl>

 

 




