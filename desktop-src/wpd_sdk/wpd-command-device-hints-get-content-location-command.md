---
description: La commande \_ wpd \_ Device \_ Hints \_ obtenir \_ \_ l’emplacement du contenu récupère les ID d’objet des dossiers qui peuvent contenir un objet d’un type spécifié.
ms.assetid: 85de64cc-44ee-4536-b658-49d5936351e4
title: Commande WPD_COMMAND_DEVICE_HINTS_GET_CONTENT_LOCATION (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_DEVICE_HINTS_GET_CONTENT_LOCATION
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 7e893df2a67aebcbd271d6df201e7e199b3c3326371e918b02b5c574ebba5763
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118026812"
---
# <a name="wpd_command_device_hints_get_content_location-command"></a>Commande \_ wpd \_ Device \_ Hints \_ , \_ commande d’emplacement du contenu \_

La **commande \_ wpd \_ Device \_ Hints \_ obtenir \_ l' \_ emplacement du contenu** récupère les ID d’objet des dossiers qui peuvent contenir un objet d’un type spécifié. Cette commande est fournie comme un moyen plus rapide pour un client de découvrir où un appareil stocke des objets spécifiques que par l’énumération d’objets en brute.

## <a name="command-category"></a>Catégorie de commande

**indicateurs d’appareil de la \_ catégorie wpd \_ \_**

## <a name="parameters"></a>Paramètres

Le pilote attend les paramètres suivants :



| Paramètre                                   | VarType   | Description                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_type de \_ contenu des indications d’appareil \_ \_ de la propriété wpd \_ | \_CLSID VT | Obligatoire. Type d’objet pour lequel l’appelant souhaite rechercher le conteneur. Par exemple, pour rechercher les dossiers de niveau supérieur utilisés pour stocker des images sur un appareil photo numérique, l’appelant doit envoyer une \_ image de type de contenu wpd \_ \_ . pour obtenir la liste des types d’objets définis par Windows appareils mobiles, consultez [configuration requise pour les objets](requirements-for-objects.md) . |



 

## <a name="return-value"></a>Valeur renvoyée

Le pilote doit renvoyer les résultats suivants.



| Résultat                                               | VarType     | Description                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------------------------------|-------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Propriétés WPD indicateurs de l' \_ appareil de \_ \_ \_ contenu \_** | VT \_ inconnu | Obligatoire. [**IPortableDevicePropVariantCollection**](iportabledevicepropvariantcollection.md) de type VT \_ LPWStr qui spécifie les ID d’objet de dossiers contenant des objets du type indiqué par le paramètre appelant. Si aucun dossier n’est trouvé, il doit s’agir d’une liste vide. Les dossiers indiqués par le résultat peuvent ou non contenir des objets d’autres types de contenu. Pour plus d’informations sur les restrictions de dossiers, consultez la propriété [ \_ types de contenu de dossier wpd \_ \_ \_ autorisés](miscellaneous-properties.md) .<br/> |
| **\_valeur courante de la propriété wpd \_ \_ HRESULT**                   | \_erreur VT   | Obligatoire. **HRESULT** qui indique la réussite ou l’échec de la gestion de la commande. Si l’appelant effectue une demande non valide, le pilote doit retourner **HRESULT \_ à partir de \_ Win32 (erreur \_ non \_ prise en charge)** et n’est pas obligé de retourner d’autres valeurs de résultat. les codes d’erreur incluent Windows codes d’erreur des [appareils mobiles](error-constants.md) ou tout autre code d’erreur approprié.                                                                                                                                                                            |
| **\_code d' \_ \_ Erreur du pilote commun \_ \_ de la propriété wpd**       | VT \_ UI4     | Facultatif. Code d’erreur spécifique au pilote. Cela est généralement utilisé uniquement pour le test des pilotes, ou si le pilote, le périphérique et le client sont tous conçus ensemble.                                                                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="calling-methods"></a>Appel de méthodes

Peut uniquement être appelé directement à l’aide de [**IPortableDevice :: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



 

 




