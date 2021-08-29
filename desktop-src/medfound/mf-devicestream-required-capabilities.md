---
description: Spécifie une liste de chaînes Unicode représentant les fonctionnalités de l’appareil requises par la transformation du capteur.
ms.assetid: 4A129FEB-E650-47C9-ABC0-9A512EE4121D
title: Attribut MF_DEVICESTREAM_REQUIRED_CAPABILITIES (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9cb7947f97b76d558fffac23742cf3728028d47eb60133e8a805862165454e0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956619"
---
# <a name="mf_devicestream_required_capabilities-attribute"></a>\_Attribut des \_ fonctionnalités requises DEVICESTREAM \_ MF

Spécifie une liste de chaînes Unicode représentant les fonctionnalités de l’appareil requises par la transformation du capteur.

## <a name="data-type"></a>Type de données

**WCHAR\***

## <a name="remarks"></a>Remarques

Cet attribut est facultatif et n’est requis que si la transformation du capteur accède à une ressource protégée. La valeur doit être une liste délimitée par des points-virgules de jetons de chaîne définis dans [**DeviceCapability**](/uwp/schemas/appxpackage/appxmanifestschema/element-devicecapability).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 10, les applications de bureau version 1703 \[ uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



 

 
