---
description: La \_ commande wpd \_ SMS \_ Send lance l’envoi d’un message SMS (Short Message Service) par un objet fonctionnel SMS.
ms.assetid: 507d3237-f2dd-499c-85e4-3c6857a15f6f
title: Commande WPD_COMMAND_SMS_SEND (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_COMMAND_SMS_SEND
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 2378ae2b17102fc2bbee568b7f5baa82da554bbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106526004"
---
# <a name="wpd_command_sms_send-command"></a>Commande \_ wpd \_ SMS \_ Send, commande

La **commande \_ wpd \_ SMS \_ Send** lance l’envoi d’un message SMS (Short Message Service) par un objet fonctionnel SMS.

## <a name="command-category"></a>Catégorie de commande

**\_SMS de catégorie wpd \_**

## <a name="parameters"></a>Paramètres

Le pilote attend les paramètres suivants :



| Paramètre                              | VarType             | Description                                                                                                                                                                                                                          |
|----------------------------------------|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_cible de \_ la \_ commande \_ commune de la propriété wpd | \_LPWStr VT          | Obligatoire. ID d’objet de l’objet fonctionnel SMS qui doit envoyer le message. Différents objets fonctionnels SMS peuvent avoir des paramètres différents.                                                                                     |
| \_propriété wpd \_ \_ destinataire SMS          | \_LPWStr VT          | Obligatoire. URI du destinataire.                                                                                                                                                                                                  |
| \_type de \_ \_ message SMS \_ de la propriété wpd      | VT \_ UI4             | Obligatoire. Énumérateur [**de \_ \_ types de messages SMS**](sms-message-types.md) qui indique le type de message (texte ou binaire).                                                                                                        |
| \_ \_ \_ message texte SMS de la propriété wpd \_      | \_LPWStr VT          | Optionnel. Si **la \_ propriété \_ wpd \_ \_ type de message SMS** indique un message texte, il s’agit de la chaîne de message ; sinon, ce paramètre n’est pas inclus.                                                                                  |
| \_propriété wpd \_ \_ message binaire \_ SMS    | VT \_ UI1 VT Vector \| \_ | Optionnel. Si **la \_ propriété \_ wpd \_ \_ type de message SMS** indique un message binaire, il s’agit d’un pointeur vers un tableau d’octets ; sinon, ce paramètre n’est pas inclus. Le premier DWORD de la valeur est la longueur du tableau, en octets. |



 

## <a name="return-value"></a>Valeur renvoyée

Le pilote doit renvoyer les résultats suivants.



| Résultats                                         | VarType   | Description                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **\_valeur courante de la propriété wpd \_ \_ HRESULT**             | \_erreur VT | Obligatoire. **HRESULT** qui indique la réussite ou l’échec de l’exécution de la commande. Si l’appelant effectue une demande non valide, le pilote doit retourner **HRESULT \_ à partir de \_ Win32 (erreur \_ non \_ prise en charge)** et n’est pas obligé de retourner d’autres valeurs de résultat. Les codes d’erreur incluent les codes d’erreur des [appareils mobiles Windows](error-constants.md) ou tout autre code d’erreur approprié. |
| **\_code d' \_ \_ Erreur du pilote commun \_ \_ de la propriété wpd** | VT \_ UI4   | Optionnel. Code d’erreur spécifique au pilote. Cela est généralement utilisé uniquement pour le test des pilotes, ou si le pilote, le périphérique et le client sont tous conçus ensemble.                                                                                                                                                                                                                                |



 

## <a name="calling-methods"></a>Appel de méthodes

Peut uniquement être appelé directement à l’aide de [**IPortableDevice :: SendCommand**](/windows/desktop/api/PortableDeviceApi/nf-portabledeviceapi-iportabledevice-sendcommand).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Commandes**](commands.md)
</dt> </dl>

 

 




