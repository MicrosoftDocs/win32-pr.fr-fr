---
title: TBN_GETBUTTONINFO le code de notification (commctrl. h)
description: Récupère les informations de personnalisation de la barre d’outils et avertit la fenêtre parente de la barre d’outils de toute modification apportée à la barre d’outils. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 088527fe-5a38-4c35-ba68-d0cbfdee410c
keywords:
- TBN_GETBUTTONINFO les contrôles de Windows de code de notification
topic_type:
- apiref
api_name:
- TBN_GETBUTTONINFO
- TBN_GETBUTTONINFOA
- TBN_GETBUTTONINFOW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 409297306901980fa8b831e5c1129a13c596ef0c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127116310"
---
# <a name="tbn_getbuttoninfo-notification-code"></a>\_Code de notification TBN GETBUTTONINFO

Récupère les informations de personnalisation de la barre d’outils et avertit la fenêtre parente de la barre d’outils de toute modification apportée à la barre d’outils. Ce code de notification est envoyé sous la forme d’un message [**WM \_ Notify**](wm-notify.md) .


```C++
TBN_GETBUTTONINFO 

    lpnmtb = (LPNMTOOLBAR) lParam; 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure [**NMTOOLBAR**](/windows/win32/api/commctrl/ns-commctrl-nmtoolbara) . Le membre **iItem** spécifie un index de base zéro qui fournit le nombre de boutons que la boîte de dialogue Personnaliser la barre d’outils affiche comme étant disponible et présente dans la barre d’outils. Le membre **pszText** spécifie l’adresse du texte du bouton actuel et **cchText** spécifie sa longueur en caractères. L’application doit remplir la structure avec des informations sur le bouton.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la **valeur true** si les informations sur le bouton ont été copiées dans la structure spécifiée, ou **false** dans le cas contraire.

## <a name="remarks"></a>Notes

Le contrôle ToolBar alloue une mémoire tampon et le récepteur (fenêtre parente) doit copier le texte dans cette mémoire tampon. Le membre **cchText** contient la longueur de la mémoire tampon allouée par la barre d’outils lorsque TBN \_ GETBUTTONINFO est envoyé à la fenêtre parente.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **TBN \_ GETBUTTONINFOW** (Unicode) et **TBN \_ GETBUTTONINFOA** (ANSI)<br/>       |



 

 





