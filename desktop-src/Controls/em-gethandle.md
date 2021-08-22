---
title: Message EM_GETHANDLE (winuser. h)
description: Obtient un handle de la mémoire actuellement allouée pour le texte d’un contrôle d’édition multiligne.
ms.assetid: 74271812-9715-4a46-96b3-0788134f8143
keywords:
- EM_GETHANDLE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_GETHANDLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f09ade5545197df2dbc9310b708cd7521334bba68f41a14329dd865e84fdee6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019647"
---
# <a name="em_gethandle-message"></a>\_Message em GETHANDLE

Obtient un handle de la mémoire actuellement allouée pour le texte d’un contrôle d’édition multiligne.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est un handle de mémoire qui identifie la mémoire tampon qui contient le contenu du contrôle d’édition. Si une erreur se produit, telle que l’envoi du message à un contrôle d’édition sur une seule ligne, la valeur de retour est zéro.

## <a name="remarks"></a>Remarques

Si la fonction réussit, l’application peut accéder au contenu du contrôle d’édition en effectuant un cast de la valeur de retour vers [**HLOCAL**](/windows/desktop/WinProg/windows-data-types) et en la passant à [**LocalLock**](/windows/desktop/api/winbase/nf-winbase-locallock). **LocalLock** retourne un pointeur vers une mémoire tampon qui est un tableau de char s ou **WCHAR** se terminant par un **caractère** null, selon qu’une fonction ANSI ou Unicode a créé le contrôle. Par exemple, si [**CreateWindowExA**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) a été utilisé, la mémoire tampon est un tableau de **char** s, mais si **CreateWindowExW** a été utilisé, la mémoire tampon est un tableau de **WCHAR** s. L’application ne peut pas modifier le contenu de la mémoire tampon. Pour déverrouiller la mémoire tampon, l’application appelle [**LocalUnlock**](/windows/desktop/api/winbase/nf-winbase-localunlock) avant d’autoriser le contrôle d’édition à recevoir de nouveaux messages.

> [!Note]  
> Pour Comctl32.dll version 6, la mémoire tampon contient toujours un tableau de **WCHAR** s, qu’une fonction ANSI ou Unicode ait créé le contrôle d’édition. Pour plus d’informations sur les versions de DLL, consultez [versions de contrôle courantes](common-control-versions.md).

 

Si votre application ne peut pas respecter les restrictions imposées par **em \_ GETHANDLE**, utilisez les fonctions [**GetWindowTextLength**](/windows/desktop/api/winuser/nf-winuser-getwindowtextlengtha) et [**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta) pour copier le contenu du contrôle d’édition dans une mémoire tampon fournie par l’application.

**Modification riche :** Le message de **em \_ GETHANDLE** n’est pas pris en charge. Les contrôles RichEdit ne stockent pas de texte sous la forme d’un simple tableau de caractères.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_SETHANDLE em**](em-sethandle.md)
</dt> <dt>

**Autres ressources**
</dt> <dt>

[**GetWindowText**](/windows/desktop/api/winuser/nf-winuser-getwindowtexta)
</dt> <dt>

[**GetWindowTextLength**](/windows/desktop/api/winuser/nf-winuser-getwindowtextlengtha)
</dt> <dt>

[**LocalLock**](/windows/desktop/api/winbase/nf-winbase-locallock)
</dt> <dt>

[**LocalUnlock**](/windows/desktop/api/winbase/nf-winbase-localunlock)
</dt> </dl>

 

