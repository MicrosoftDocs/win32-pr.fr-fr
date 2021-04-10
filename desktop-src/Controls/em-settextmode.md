---
title: Message EM_SETTEXTMODE (RichEdit. h)
description: Définit le mode texte ou le niveau d’annulation d’un contrôle RichEdit. Le message échoue si le contrôle contient du texte.
ms.assetid: d6741234-0ef3-4cd2-8817-6c852f1b500d
keywords:
- EM_SETTEXTMODE les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETTEXTMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74ec5378213bdd32721ff95ae3f4505437973256
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942295"
---
# <a name="em_settextmode-message"></a>\_Message SETTEXTMODE em

Définit le mode texte ou le niveau d’annulation d’un contrôle RichEdit. Le message échoue si le contrôle contient du texte.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Une ou plusieurs valeurs du type d’énumération [**TextMode**](/windows/win32/api/richedit/ne-richedit-textmode) . Les valeurs spécifient les nouveaux paramètres pour le mode texte du contrôle et les paramètres de niveau d’annulation.

Spécifiez l’une des valeurs suivantes pour définir le paramètre de mode texte. Si vous ne spécifiez pas de valeur de mode texte, le mode texte conserve son paramètre actuel. 

| Valeur                                          | Signification                                                                                                                                                               |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_texte en clair**](/windows/win32/api/richedit/ne-richedit-textmode) | Indique le mode texte brut, dans lequel le contrôle est similaire à un contrôle d’édition standard. Pour plus d’informations sur le mode texte brut, consultez la section Notes suivante. |
| [**\_RTF TM**](/windows/win32/api/richedit/ne-richedit-textmode)   | Indique le mode texte enrichi, dans lequel le contrôle possède une fonctionnalité de modification enrichie standard. Le mode de texte enrichi est le paramètre par défaut.                                           |



 

Spécifiez l’une des valeurs suivantes pour définir le paramètre de niveau d’annulation. Si vous ne spécifiez pas de valeur de niveau d’annulation, le niveau d’annulation reste le paramètre actuel. 

| Valeur                                                      | Signification                                                                                                                                                                            |
|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_SINGLELEVELUNDO TM**](/windows/win32/api/richedit/ne-richedit-textmode) | Le contrôle permet à l’utilisateur d’annuler uniquement la dernière action qui peut être annulée.                                                                                                       |
| [**\_MULTILEVELUNDO TM**](/windows/win32/api/richedit/ne-richedit-textmode)   | Le contrôle prend en charge plusieurs opérations d’annulation. Il s'agit du paramètre par défaut. Utilisez le message [**em \_ SETUNDOLIMIT**](em-setundolimit.md) pour définir le nombre maximal d’actions d’annulation. |



 

Spécifiez l’une des valeurs suivantes pour définir le paramètre de page de codes. Si vous ne spécifiez pas de valeur de page de codes, la page de codes conserve son paramètre actuel. 

| Valeur                                                    | Signification                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**\_SINGLECODEPAGE TM**](/windows/win32/api/richedit/ne-richedit-textmode) | Le contrôle autorise uniquement le clavier anglais et un clavier correspondant au jeu de caractères par défaut. Par exemple, vous pouvez avoir des lettres grecque et anglais. Notez que cela empêche le texte Unicode d’entrer dans le contrôle. Par exemple, utilisez cette valeur si un contrôle RichEdit doit être limité au texte ANSI. |
| [**\_MULTICODEPAGE TM**](/windows/win32/api/richedit/ne-richedit-textmode)   | Le contrôle permet l’insertion de plusieurs pages de codes et de texte Unicode dans le contrôle. Il s'agit du paramètre par défaut.                                                                                                                                                                                                     |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si le message est correctement exécuté, la valeur de retour est zéro.

Si le message échoue, la valeur de retour est une valeur différente de zéro.

## <a name="remarks"></a>Notes

En mode de texte enrichi, un contrôle RichEdit offre des fonctionnalités de modification enrichies standard. Toutefois, en mode texte brut, le contrôle est similaire à un contrôle d’édition standard :

-   Le texte d’un contrôle de texte brut ne peut avoir qu’un seul format (par exemple, gras, Arial 10 PT).
-   L’utilisateur ne peut pas coller des formats de texte enrichi, tels que RTF (Rich Text Format) ou des objets incorporés dans un contrôle de texte brut.
-   Les contrôles en mode de texte enrichi ont toujours un marqueur de fin de document par défaut ou un retour chariot, pour mettre en forme des paragraphes. En revanche, les contrôles de texte brut n’ont pas besoin du marqueur de fin de document par défaut. il est donc omis.

Le contrôle ne doit pas contenir de texte lorsqu’il reçoit le message **em \_ SETTEXTMODE** . Pour garantir qu’il n’y a pas de texte, envoyez un message [**WM \_ SETTEXT**](/windows/desktop/winmsg/wm-settext) avec une chaîne vide ("").

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_GETTEXTMODE em**](em-gettextmode.md)
</dt> <dt>

[**\_SETUNDOLIMIT em**](em-setundolimit.md)
</dt> <dt>

[**TEXTMODE**](/windows/win32/api/richedit/ne-richedit-textmode)
</dt> <dt>

[**WM, \_ SETTEXT**](/windows/desktop/winmsg/wm-settext)
</dt> </dl>

 

