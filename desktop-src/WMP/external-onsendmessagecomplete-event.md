---
title: External. OnSendMessageComplete, événement
description: Remarque Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. | External. OnSendMessageComplete, événement
ms.assetid: 9ae60aa5-4ecd-41dd-aeb0-afb1a3686982
keywords:
- Événement External. OnSendMessageComplete lecteur Windows Media
topic_type:
- apiref
api_name:
- External.OnSendMessageComplete Event
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 05d4de69a753811537f60ae8a3244cfaf012f60d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106539513"
---
# <a name="externalonsendmessagecomplete-event"></a>External. OnSendMessageComplete, événement

> [!Note]  
> Cette rubrique décrit les fonctionnalités conçues pour être utilisées par les magasins en ligne. L’utilisation de cette fonctionnalité en dehors du contexte d’un magasin en ligne n’est pas prise en charge.

 

L’événement **OnSendMessageComplete** se produit lorsque le magasin en ligne a terminé le traitement d’un message. Le script sur la page de découverte a précédemment envoyé le message en appelant [External. SendMessage](external-sendmessage.md).

``` syntax
window.external.OnSendMessageComplete = FunctionName
```

## <a name="possible-values"></a>Valeurs possibles

Il s’agit d’une propriété en écriture seule qui spécifie le nom de la fonction dans le script que le lecteur Windows Media appelle lorsque l’événement se produit.

## <a name="parameters"></a>Paramètres

La fonction qui gère cet événement a les paramètres suivants.

<dl> <dt>

<span id="Msg"></span><span id="msg"></span><span id="MSG"></span>*Fragment*
</dt> <dd>

La même chaîne qui a été passée dans le paramètre **MSG** de **SendMessage**.

</dd> <dt>

<span id="Param"></span><span id="param"></span><span id="PARAM"></span>*Envoyés*
</dt> <dd>

La même chaîne qui a été passée dans le paramètre **param** de **SendMessage**.

</dd> <dt>

<span id="Result"></span><span id="result"></span><span id="RESULT"></span>*Venir*
</dt> <dd>

**Chaîne** qui contient le résultat de la gestion des messages. Consultez la section Notes.

</dd> </dl>

## <a name="remarks"></a>Notes

La méthode **SendMessage** appelle [IWMPContentPartner :: SendMessage](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage), qui retourne de manière asynchrone. Autrement dit, il retourne avant que le magasin en ligne ne termine le traitement du message. Lorsque le magasin en ligne a terminé le traitement du message, il appelle [IWMPContentPartnerCallback :: SendMessageComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete), qui à son tour appelle le gestionnaire d’événements **OnSendMessageComplete** du script.

Lorsque le magasin en ligne appelle **IWMPContentPartnerCallback :: SendMessageComplete**, il fournit un code de résultat dans le paramètre *bstrResult* . Le lecteur Windows Media n’interprète pas ce code de résultat. Au lieu de cela, le lecteur Windows Media transmet le code de résultat au gestionnaire d’événements **OnSendMessageComplete** dans le paramètre de *résultat* .

Aucun des paramètres (*MSG*, *param*, *result*) du gestionnaire d’événements **OnSendMessageComplete** n’est interprété par le lecteur Windows Media. Les paramètres n’ont de sens que dans le magasin en ligne.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|--------------------|------------------------------------------------------------------------------------|
| Version<br/> | Lecteur Windows Media 11<br/>                                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Objet externe pour les magasins de type 1 en ligne**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**External. sendMessage**](external-sendmessage.md)
</dt> <dt>

[**IWMPContentPartner :: SendMessage**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-sendmessage)
</dt> <dt>

[**IWMPContentPartnerCallback::SendMessageComplete**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-sendmessagecomplete)
</dt> </dl>

 

 





