---
title: Message EM_SETHANDLE (winuser. h)
description: Définit le handle de la mémoire qui sera utilisée par un contrôle d’édition multiligne.
ms.assetid: 0eae9365-62af-4040-8a51-273997a00b81
keywords:
- EM_SETHANDLE les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETHANDLE
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac8f918d056db1000c6018f55d89095a73a15109
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105574"
---
# <a name="em_sethandle-message"></a>\_Message SETHANDLE em

Définit le handle de la mémoire qui sera utilisée par un contrôle d’édition multiligne.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Handle vers la mémoire tampon que le contrôle d’édition utilise pour stocker le texte actuellement affiché au lieu d’allouer sa propre mémoire. Si nécessaire, le contrôle réalloue cette mémoire.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Ce message ne retourne pas de valeur.

## <a name="remarks"></a>Notes

Avant qu’une application ne définisse un nouveau descripteur de mémoire, elle doit envoyer un message [**em \_ GETHANDLE**](em-gethandle.md) pour récupérer le handle de la mémoire tampon actuelle et libérer cette mémoire.

Un contrôle d’édition réalloue automatiquement la mémoire tampon donnée à chaque fois qu’elle a besoin d’espace supplémentaire pour le texte, ou elle supprime suffisamment de texte afin que de l’espace supplémentaire ne soit plus nécessaire.

L’envoi d’un message **em \_ SETHANDLE** efface le tampon d’annulation ([**em \_ CANUNDO**](em-canundo.md) retourne zéro) et l’indicateur de modification interne ([**em \_ GETMODIFY**](em-getmodify.md) retourne zéro). La fenêtre Modifier le contrôle est redessinée.

**Modification riche :** Le **message \_ SETHANDLE em** n’est pas pris en charge. Les contrôles RichEdit ne stockent pas de texte sous la forme d’un simple tableau de caractères.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**EM \_ CANUNDO**](em-canundo.md)
</dt> <dt>

[**EM \_ GETHANDLE**](em-gethandle.md)
</dt> <dt>

[**\_GETMODIFY em**](em-getmodify.md)
</dt> </dl>

 

 





