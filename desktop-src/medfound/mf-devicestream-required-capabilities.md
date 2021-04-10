---
description: Spécifie une liste de chaînes Unicode représentant les fonctionnalités de l’appareil requises par la transformation du capteur.
ms.assetid: 4A129FEB-E650-47C9-ABC0-9A512EE4121D
title: Attribut MF_DEVICESTREAM_REQUIRED_CAPABILITIES (Mfidl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cac47d60c38e41d44ecf0776ea8bf7588559dfe1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113674"
---
# <a name="mf_devicestream_required_capabilities-attribute"></a>\_Attribut des \_ fonctionnalités requises DEVICESTREAM \_ MF

Spécifie une liste de chaînes Unicode représentant les fonctionnalités de l’appareil requises par la transformation du capteur.

## <a name="data-type"></a>Type de données

**WCHAR \** _

## <a name="remarks"></a>Notes

Cet attribut est facultatif et n’est requis que si la transformation du capteur accède à une ressource protégée. La valeur doit être une liste délimitée par des points-virgules de jetons de chaîne définis dans [_ *DeviceCapability* *](/uwp/schemas/appxpackage/appxmanifestschema/element-devicecapability).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows 10, version 1703 \[ uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                          |
| En-tête<br/>                   | <dl> <dt>Mfidl. h</dt> </dl> |



 

 
