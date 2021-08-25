---
title: Message ACM_OPEN (commctrl. h)
description: Ouvre un clip AVI et affiche sa première image dans un contrôle d’animation. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro animer \_ ouvrir ou animer \_ OpenEx. Nous vous recommandons d’utiliser la version Unicode de ce message, ACM \_ OPENW.
ms.assetid: 87f476ce-bb27-4b5f-bfdf-dff84bd7e4f4
keywords:
- ACM_OPEN les contrôles de Windows de message
topic_type:
- apiref
api_name:
- ACM_OPEN
- ACM_OPENA
- ACM_OPENW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c5af2bd996af159217c92d78102a97e5c530d34cf445d5ad34186cecb93ab85
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922169"
---
# <a name="acm_open-message"></a>\_Message d’ouverture ACM

Ouvre un clip AVI et affiche sa première image dans un contrôle d’animation. Vous pouvez envoyer ce message de manière explicite ou utiliser la macro [**animer \_ ouvrir**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) ou [**animer \_ OpenEx**](/windows/desktop/api/Commctrl/nf-commctrl-animate_openex) . Nous vous recommandons d’utiliser la version Unicode de ce message, ACM \_ OPENW.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

[Version 4,71](common-control-versions.md) et versions ultérieures. Handle d’instance du module à partir duquel la ressource doit être chargée. Définissez cette valeur sur **null** pour que le contrôle utilise la valeur HINSTANCE utilisée pour créer la fenêtre. Notez que si la fenêtre est créée par une DLL, la valeur par défaut de *wParam* est la valeur HINSTANCE de la dll, et non celle de l’application qui appelle la dll.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une mémoire tampon qui contient le chemin d’accès du fichier AVI ou le nom d’une ressource AVI. Ce paramètre peut également être constitué de l’identificateur de ressource AVI dans [**LOWORD**](/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)) et de zéro dans le [**HIWORD**](/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)). Pour créer cette valeur, utilisez la macro [**MAKEINTRESOURCE**](/windows/desktop/api/winuser/nf-winuser-makeintresourcea) . Le contrôle charge la ressource AVI à partir du module spécifié par le handle d’instance passé à la fonction [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) , à la macro de création d' [**animation \_**](/windows/desktop/api/Commctrl/nf-commctrl-animate_create) ou à la fonction de création de boîte de dialogue qui a créé le contrôle. Dans la [Version 4,71](common-control-versions.md) et les versions ultérieures, la ressource est chargée à partir du module spécifié par *wParam*. Une ressource AVI doit avoir le type « AVI ». Si ce paramètre a la **valeur null**, le système ferme le fichier AVI précédemment ouvert pour le contrôle d’animation spécifié, le cas échéant.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne une valeur différente de zéro en cas de réussite, ou zéro dans le cas contraire.

## <a name="remarks"></a>Remarques

Le fichier ou la ressource AVI spécifié par *lpszName* ne doit pas contenir de données audio.

Nous vous recommandons d’utiliser la version Unicode de ce message, ACM \_ OPENW.

Vous ne pouvez ouvrir que des clips AVI en mode silencieux. Le composant ACM \_ Open et [**Animate \_ Open**](/windows/desktop/api/Commctrl/nf-commctrl-animate_open) échoue si *lParam* spécifie un clip AVI contenant du son.

Vous pouvez utiliser l' [**animation \_ Fermer**](/windows/desktop/api/Commctrl/nf-commctrl-animate_close) pour fermer un fichier AVI ou une ressource AVI précédemment ouverte pour le contrôle d’animation spécifié.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **ACM \_ OPENW** (Unicode) et **ACM \_ Opena** (ANSI)<br/>                         |



 

