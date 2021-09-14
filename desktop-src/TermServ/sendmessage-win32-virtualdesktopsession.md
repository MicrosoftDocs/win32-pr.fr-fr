---
title: Méthode SendMessage de la classe Win32_VirtualDesktopSession
description: Envoyer un message à l’utilisateur via la session de bureau virtuel.
ms.assetid: 4bb9183e-c016-48f2-8e8c-0d5fb395c435
ms.tgt_platform: multiple
keywords:
- SendMessage, méthode Services Bureau à distance
- SendMessage, méthode Services Bureau à distance, classe Win32_VirtualDesktopSession
- Win32_VirtualDesktopSession de la classe Services Bureau à distance, SendMessage, méthode
topic_type:
- apiref
api_name:
- Win32_VirtualDesktopSession.SendMessage
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1e3e72f5c401b8cbb0e5e5de45f594d61af6275
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127324490"
---
# <a name="sendmessage-method-of-the-win32_virtualdesktopsession-class"></a>Méthode SendMessage de la \_ classe VirtualDesktopSession Win32

Envoyer un message à l’utilisateur via la session de bureau virtuel.

## <a name="syntax"></a>Syntaxe


```mof
uint32 SendMessage(
  [in] string Title,
  [in] string Message
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Titre* \[ dans\]
</dt> <dd>

Titre du messages.

</dd> <dt>

*Message* \[ dans\]
</dt> <dd>

Contenu du message.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne 0 en cas de réussite, sinon retourne un code d’erreur WMI.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                   |
| Serveur minimal pris en charge<br/> | Windows Server 2012<br/>                                                              |
| Espace de noms<br/>                | Racine \\ cimv2 cimv2 \\<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_VirtualDesktopSession Win32**](win32-virtualdesktopsession.md)
</dt> </dl>

 

 





