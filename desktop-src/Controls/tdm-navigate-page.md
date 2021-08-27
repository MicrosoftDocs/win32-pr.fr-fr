---
title: Message TDM_NAVIGATE_PAGE (commctrl. h)
description: Recrée une boîte de dialogue de tâches avec le nouveau contenu, en simulant la fonctionnalité d’un Assistant multipage.
ms.assetid: e0eefd08-e279-47db-97e9-7ca86b41e22f
keywords:
- TDM_NAVIGATE_PAGE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TDM_NAVIGATE_PAGE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c7894bdc5831af2c1fe2e779679aaab38eab94f976cf9c586dfe64d26a051b8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104629"
---
# <a name="tdm_navigate_page-message"></a>Message de page de \_ navigation TDM \_

Recrée une boîte de dialogue de tâches avec le nouveau contenu, en simulant la fonctionnalité d’un Assistant multipage.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* \[ dans\]
</dt> <dd>

Non utilisé. Doit être zéro.

</dd> <dt>

*lParam* \[ dans\]
</dt> <dd>

Pointeur vers une structure [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) qui décrit la boîte de dialogue de tâche à créer. L’application appelante doit allouer cette structure et définir ses membres. Les valeurs des membres varient en fonction du type de page vers lequel l’utilisateur accède.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est ignorée.

## <a name="remarks"></a>Remarques

Pour lancer une boîte de dialogue de tâche de l’Assistant, utilisez la fonction [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) . Lorsque l’utilisateur navigue à l’aide de l’Assistant, envoyez ce message à la boîte de dialogue de tâche pour afficher la page suivante. Une nouvelle boîte de dialogue de tâches (qui ressemble à une nouvelle page) est créée avec les éléments spécifiés dans la structure vers laquelle pointe *lParam*. Au moment de la création, le contenu entier du cadre de la boîte de dialogue est détruit et reconstruit. Par conséquent, toutes les informations d’État détenues par les contrôles (par exemple, une barre de progression, un bouton de développement ou un bouton de vérification) dans la boîte de dialogue sont perdues.

La disposition de la boîte de dialogue de tâche peut échouer et cela peut ne pas être reflété dans la valeur de retour. Une valeur de retour de S \_ OK reflète uniquement que la boîte de dialogue de tâche a reçu le message et a tenté de le traiter. Si la disposition de la boîte de dialogue de tâche échoue (la boîte de dialogue de tâche ne peut pas être affichée), la boîte de dialogue se ferme et un code **HRESULT** est retourné au niveau de la fonction de rappel enregistrée. Pour plus d’informations sur la syntaxe de la fonction de rappel, consultez [*TaskDialogCallbackProc*](/windows/win32/api/commctrl/nc-commctrl-pftaskdialogcallback).

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

