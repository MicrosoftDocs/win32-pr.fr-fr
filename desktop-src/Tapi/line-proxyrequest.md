---
description: Le message PROXYREQUEST de ligne TAPI \_ envoie une requête à un gestionnaire de fonctions proxy inscrit.
ms.assetid: 7f33de55-2482-4558-bd86-ee2ac1e31269
title: Message LINE_PROXYREQUEST (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d536e85a9c773626bb5aacc4745d9d82817fe3c0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127217668"
---
# <a name="line_proxyrequest-message"></a>\_Message PROXYREQUEST de ligne

Le message **\_ PROXYREQUEST de ligne** TAPI envoie une requête à un gestionnaire de fonctions proxy inscrit.


```C++
            
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hDevice* 
</dt> <dd>

Handle de l’application sur le périphérique de ligne sur lequel l’état de l’agent a changé.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Instance de rappel fournie lors de l’ouverture de la ligne de l’appel.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Pointeur vers une structure [**LINEPROXYREQUEST**](/windows/desktop/api/Tapi/ns-tapi-lineproxyrequest) contenant la demande à traiter par l’application du gestionnaire de proxy.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Réservé.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Réservé.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Le message de **ligne \_ PROXYREQUEST** est envoyé uniquement à la première application inscrite pour gérer les demandes de proxy du type remis.

L’application doit traiter la requête contenue dans la mémoire tampon du proxy et appeler [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) pour retourner des données ou fournir des résultats. Le traitement de la requête doit être effectué dans le contexte de la fonction de rappel TAPI de l’application uniquement si elle peut être exécutée immédiatement, sans attendre la réponse d’une autre entité. Si l’application doit communiquer avec d’autres entités (par exemple, un fournisseur de services pour gérer les ACD basés sur PBX, ou tout autre service système qui peut entraîner un blocage), la demande doit être mise en file d’attente dans l’application et la fonction de rappel s’est arrêtée pour éviter de retarder la réception de messages TAPI supplémentaires par l’application.

Au moment où la **ligne \_ PROXYREQUEST** est remise au gestionnaire proxy, TAPI a déjà retourné un résultat de fonction *dwRequestID* positif à l’application d’origine et a débloqué le thread appelant pour poursuivre l’exécution. L’application attend un message de [**\_ réponse de ligne**](line-reply.md) , qui est généré automatiquement lorsque l’application de gestionnaire proxy appelle [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse).

L’application ne libère pas la mémoire vers laquelle pointe *lpProxyRequest*. L’interface TAPI libère de la mémoire pendant l’exécution de [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse). L’application peut appeler [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) exactement une fois pour chaque message de **\_ PROXYREQUEST de ligne** .

Si l’application reçoit un message de [**\_ fermeture de ligne**](line-close.md) alors qu’elle a des requêtes proxy en attente, elle doit appeler [**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse) pour chaque demande en attente, en transmettant une valeur *dwResult* appropriée (telle que LINEERR \_ OPERATIONFAILED).

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**fermeture de ligne \_**](line-close.md)
</dt> <dt>

[**réponse de ligne \_**](line-reply.md)
</dt> <dt>

[**LINEPROXYREQUEST**](/windows/desktop/api/Tapi/ns-tapi-lineproxyrequest)
</dt> <dt>

[**lineProxyResponse**](/windows/desktop/api/Tapi/nf-tapi-lineproxyresponse)
</dt> </dl>

 

 




