---
description: effectue l’initialisation nécessaire pour permettre à l’application appelante d’être un récepteur d’affichage Miracast.
ms.assetid: D87B427B-0B7F-44BB-BC34-726FDF87CCCC
title: WFDDisplaySinkStart, fonction (Wfdsink. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WFDStartDisplaySink
api_type:
- DllExport
api_location:
- wifidisplay.dll
ms.openlocfilehash: 423ca68364fbe7c4beb89ab3b1d9f8e8fdb891be
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127413739"
---
# <a name="wfddisplaysinkstart-function"></a>WFDDisplaySinkStart fonction)

effectue l’initialisation nécessaire pour permettre à l’application appelante d’être un récepteur d’affichage Miracast. Votre application doit l’appeler une fois au démarrage.

## <a name="syntax"></a>Syntaxe


```C++
DWORD WINAPI WFDStartDisplaySink(
  _In_     USHORT                                 uDeviceCategory,
  _In_     USHORT                                 uSubCategory,
  _In_opt_ PVOID                                  pCallbackContext,
  _In_     WFD_DISPLAY_SINK_NOTIFICATION_CALLBACK *pfnCallback
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*uDeviceCategory* \[ dans\]
</dt> <dd>

Catégorie de l’appareil.

</dd> <dt>

*uSubCategory* \[ dans\]
</dt> <dd>

Sous-catégorie d’appareil.

</dd> <dt>

*pCallbackContext* \[ dans, facultatif\]
</dt> <dd>

Pointeur de contexte facultatif qui est passé à la fonction de rappel spécifiée dans le paramètre *pfnCallback* .

</dd> <dt>

*pfnCallback* \[ dans\]
</dt> <dd>

Pointeur vers la fonction de rappel à appeler à chaque fois qu’une notification est envoyée à l’application. Les notifications qui peuvent être envoyées sont décrites dans le [**rappel de notification du \_ récepteur d’affichage \_ \_ \_ WFD**](wfd-display-sink-notification-callback.md).

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si la fonction réussit, la valeur de retour est une erreur de \_ réussite.

Si la fonction échoue, la valeur de retour peut être l’un des codes de retour suivants.



| Code de retour                                                                                          | Description                                                    |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <dt>**ERREUR \_ non \_ prise en charge**</dt> </dl> | Le récepteur d’affichage n’est pas pris en charge sur ce matériel.<br/> |



 

## <a name="remarks"></a>Notes

Cette fonction effectue les tâches suivantes :

-   Rend le PC détectable
-   Définit les informations de l’appareil P2P pour refléter la catégorie et la sous-catégorie spécifiées
-   définit le Miracast IEs sur toutes les Wi-Fi frames directs dont le type d’appareil est le récepteur
-   Inscrit le rappel spécifié à appeler à chaque fois qu’il existe une connexion entrante.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8.1 les \[ applications de bureau uniquement\]<br/>                                               |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[Applications de bureau R2 uniquement\]<br/>                                    |
| Fin de la prise en charge des clients<br/>    | Windows 10<br/>                                                                      |
| Fin de la prise en charge des serveurs<br/>    | Windows Server 2016<br/>                                                             |
| En-tête<br/>                   | <dl> <dt>Wfdsink. h</dt> </dl>       |
| Bibliothèque<br/>                  | <dl> <dt>Wifidisplay. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wifidisplay.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_rappel de \_ notification du récepteur d’affichage WFD \_ \_**](wfd-display-sink-notification-callback.md)
</dt> </dl>

 

 




