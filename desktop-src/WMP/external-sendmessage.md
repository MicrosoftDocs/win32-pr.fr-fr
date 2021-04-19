---
title: External. sendMessage, méthode
description: Remarque Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge. La méthode sendMessage envoie un message au plug-in du magasin en ligne.
ms.assetid: 72d34dcc-3284-4446-804f-0fc93a7d8dab
keywords:
- méthode sendMessage lecteur Windows Media
- méthode sendMessage lecteur Windows Media, classe externe
- Classe externe lecteur Windows Media, sendMessage, méthode
topic_type:
- apiref
api_name:
- External.sendMessage
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4648f3cf433a2828d3c97604ebf9ee6e7223b7f1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106525491"
---
# <a name="externalsendmessage-method"></a>External. sendMessage, méthode

> [!Note]  
> Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

La méthode **SendMessage** envoie un message au plug-in du magasin en ligne.

## <a name="syntax"></a>Syntaxe


```JScript
External.sendMessage(
  Msg,
  Param
)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*Message* \[ dans\]
</dt> <dd>

**Chaîne** contenant le message.

</dd> <dt>

*Param* \[ dans\]
</dt> <dd>

**Chaîne** contenant les paramètres associés au message.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Cette méthode ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Le message est envoyé de manière asynchrone. Autrement dit, cette méthode retourne immédiatement au lieu d’attendre que le message soit traité. Lorsque le plug-in termine le traitement du message, il appelle la méthode [IWMPContentPartnerCallback :: SendMessageComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete) , qui à son tour appelle le gestionnaire d’événements [OnSendMessageComplete](external-onsendmessagecomplete-event.md) du script.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media 11.<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet externe pour les magasins de type 1 en ligne**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. OnSendMessageComplete**](external-onsendmessagecomplete-event.md)
</dt> <dt>

[**IWMPContentPartner :: SendMessage**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage)
</dt> <dt>

[**IWMPContentPartnerCallback::SendMessageComplete**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete)
</dt> </dl>

 

 





