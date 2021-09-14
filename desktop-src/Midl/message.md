---
title: attribut de message
description: L’attribut \ message \ indique que l’appel de procédure distante doit être traité comme un message du client au serveur.
ms.assetid: ec616bf5-a845-4e7e-9f39-20947d2074f7
keywords:
- MIDL (attribut de message)
topic_type:
- apiref
api_name:
- message
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 964f8dfd8652547bdf5bef25d1abe9acde8189a2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127093421"
---
# <a name="message-attribute"></a>attribut de message

L’attribut de **\[ message \]** indique que l’appel de procédure distante doit être traité comme un message du client au serveur.

``` syntax
[message, optional-attribute-list] void function-name(
    [in, optional-parameter-attributes] param-name,. . .);
```

## <a name="parameters"></a>Paramètres

<dl> <dt>

*Optional-attribute-List* 
</dt> <dd>

Autres attributs qui s’appliquent à la fonction. Seuls les **\[** attributs [**local**](local.md) **\]** , **\[** [**nocode**](nocode.md) **\]** , **\[** [**code**](code.md)**\]** et **\[** [**optimize**](optimize.md) **\]** peuvent être utilisés avec l’attribut de **\[ message \]** .

</dd> <dt>

*nom de fonction* 
</dt> <dd>

Nom de la fonction tel qu’il est défini dans le fichier IDL.

</dd> <dt>

*facultatif-Parameter-Attributes* 
</dt> <dd>

Zéro, un ou plusieurs attributs MIDL qui seront appliqués au paramètre.

</dd> <dt>

*nom du paramètre* 
</dt> <dd>

Nom du paramètre tel que défini dans le fichier IDL.

</dd> </dl>

## <a name="remarks"></a>Notes

En tant que messages du client, les appels de procédure distante avec l’attribut de **\[ message \]** sont remis au serveur de façon asynchrone via le transport [**ncadg \_ MQ**](ncadg-mq.md) Message-Queuing. Vous pouvez indiquer une messagerie en mode synchrone en spécifiant le protocole de transport **ncadg \_ MQ** sans utiliser l’attribut de **\[ \] message** .

En spécifiant une messagerie en mode asynchrone, l’attribut de **\[ message \]** permet au client d’effectuer l’appel de procédure distante et de retourner immédiatement, même lorsque l’application serveur ne répond pas. Si le serveur cible n’est pas disponible, l’appel est stocké jusqu’à ce que le serveur soit disponible.

En outre, la messagerie en mode asynchrone vous permet de contrôler les propriétés de file d’attente de messages de la file d’attente de réception pour le serveur. Consultez [**RpcBindingSetOption**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetoption) pour plus d’informations sur la sélection de la qualité de service, la priorité d’appel et la durée de vie des appels pour le processus serveur.

Les restrictions suivantes s’appliquent également à l’attribut de **\[ message \]** :

-   Microsoft Message Queuing doit être implémenté dans les systèmes client et serveur et les systèmes doivent être visibles les uns avec les autres, comme déterminé par l’étendue de l’installation de la file d’attente de messages.
-   La liaison doit utiliser des points de terminaison connus et le protocole de transport [**\_ MQ ncadg**](ncadg-mq.md) .
-   La fonction ne peut pas contenir de paramètres de sortie ou de type de retour autre que [**void**](void.md). Notez que la dernière restriction rend l’attribut de **\[ message \]** inapproprié pour les méthodes d’interface com (objet), à l’heure actuelle. La prochaine version de MIDL permettra aux fonctions de **\[ message \]** de retourner l’état d’erreur \_ \_ t ou HRESULT.
-   Toute interface contenant au moins un appel de **\[ \] message** doit être inscrite en appelant [**RpcServerRegisterIf**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterif) ou [**RpcServerRegisterIfEx**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserverregisterifex) avant d’appeler [**RpcServerUseProtseqEpEx (ncadg \_ mq)**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcserveruseprotseqepex). Dans le cas contraire, les appels qui étaient en attente sur la file d’attente du serveur sont lus avant l’inscription de l’interface et les appels échouent.

## <a name="examples"></a>Exemples

``` syntax
[message] void DisplayString(
    [in, string] char * p1);
 
[message] void VarDataArray(
    [in, size_is(iSize)] ARRAY_TYPE lpMyArray,
    [in] int iSize,
    [in] unsigned long ulChksum);
```

## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**code**](code.md)
</dt> <dt>

[**localisé**](local.md)
</dt> <dt>

[**ncadg \_ MQ**](ncadg-mq.md)
</dt> <dt>

[**SansCode**](nocode.md)
</dt> <dt>

[**requêtes**](optimize.md)
</dt> <dt>

[Message Queuing RPC](/windows/desktop/Rpc/rpc-message-queuing)
</dt> <dt>

[**RpcBindingSetOption**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindingsetoption)
</dt> <dt>

[**RpcBindingInqOption**](/windows/desktop/api/rpcdce/nf-rpcdce-rpcbindinginqoption)
</dt> <dt>

[**nullité**](void.md)
</dt> </dl>

 

 