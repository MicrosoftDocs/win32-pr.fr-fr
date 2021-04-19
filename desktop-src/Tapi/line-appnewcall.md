---
description: Le \_ message APPNEWCALL de ligne TAPI est envoyé pour informer une application lorsqu’un nouveau handle d’appel a été créé spontanément en son nom.
ms.assetid: 0c263025-e719-453e-91c4-a9f2d9321db3
title: Message LINE_APPNEWCALL (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33d24ca816fb69384e90e4215edbc90b9410b887
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106542686"
---
# <a name="line_appnewcall-message"></a>\_Message APPNEWCALL de ligne

Le message **\_ APPNEWCALL de ligne** TAPI est envoyé pour informer une application lorsqu’un nouveau handle d’appel a été créé spontanément en son nom (à l’exception d’un appel d’API de l’application, auquel cas le handle aurait été retourné via un paramètre de pointeur transmis à la fonction).


```C++
        
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*hDevice* 
</dt> <dd>

Handle de l’application sur le périphérique de ligne sur lequel l’appel a été créé.

</dd> <dt>

*dwCallbackInstance* 
</dt> <dd>

Instance de rappel fournie lors de l’ouverture de la ligne de l’appel.

</dd> <dt>

*dwParam1* 
</dt> <dd>

Identificateur de l’adresse sur la ligne sur laquelle l’appel s’affiche. Un identificateur d’adresse est associé de manière permanente à une adresse ; l’identificateur reste constant entre les mises à niveau du système d’exploitation.

</dd> <dt>

*dwParam2* 
</dt> <dd>

Handle de l’application vers le nouvel appel.

</dd> <dt>

*dwParam3* 
</dt> <dd>

Privilège des applications au nouvel appel (LINECALLPRIVILEGE \_ owner ou LINECALLPRIVILEGE \_ Monitor).

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Pas de valeur de retour.

## <a name="remarks"></a>Notes

Les applications prenant en charge TAPI version 2,0 ou ultérieure reçoivent un message de **ligne \_ APPNEWCALL** chaque fois que l’application reçoit spontanément un handle vers un nouvel appel. Étant donné que le message comprend les paramètres *hLine* et *dwAddressID* sur lesquels l’appel existe, l’application peut facilement créer un nouvel objet d’appel dans le contexte approprié. Le message de **ligne \_ APPNEWCALL** est toujours immédiatement suivi d’un message de [**ligne \_ CALLSTATE**](line-callstate.md) indiquant l’état initial de l’appel.

Les applications plus anciennes (qui ont négocié une version d’API antérieure à 2,0) sont envoyées uniquement à un message [**\_ CALLSTATE de ligne**](line-callstate.md) , comme indiqué dans les versions précédentes de l’API. De telles applications créeraient un nouvel objet d’appel lors de la réception d’un message [**\_ CALLSTATE de ligne**](line-callstate.md) dont *dwParam3* a une valeur différente de zéro et qui contient un handle d’appel non connu actuellement par l’application. Les inconvénients sont que (a) l’application doit appeler [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo) pour déterminer les paramètres *hLine* et *dwAddressID* associés à l’appel. (b) l’application doit analyser tous les handles d’appel connus pour déterminer que l’appel est un nouvel appel ; et (c) c’est possible, dans certaines conditions, pour que l’application considère qu’elle reçoit un nouveau descripteur d’appel alors qu’en réalité elle vient de libérer son handle à l’appel (par exemple, l’application vient de libérer un handle d’appel, mais un message de [**ligne \_ CALLSTATE**](line-callstate.md) indiquant à l’application la propriété de l’appel en raison d’un [**lineHandoff**](/windows/desktop/api/Tapi/nf-tapi-linehandoff) d’une autre application était déjà dans la file d’attente de messages TAPI

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------|-----------------------------------------------------------------------------------|
| Version TAPI<br/> | Nécessite TAPI 2,0 ou une version ultérieure<br/>                                             |
| En-tête<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**CALLSTATE de ligne \_**](line-callstate.md)
</dt> <dt>

[**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo)
</dt> <dt>

[**lineHandoff**](/windows/desktop/api/Tapi/nf-tapi-linehandoff)
</dt> </dl>

 

 




