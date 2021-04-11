---
title: TBN_GETBUTTONINFO le code de notification (commctrl. h)
description: Récupère les informations de personnalisation de la barre d’outils et avertit la fenêtre parente de la barre d’outils de toute modification apportée à la barre d’outils. Ce code de notification est envoyé sous la forme d’un \_ message WM Notify.
ms.assetid: 088527fe-5a38-4c35-ba68-d0cbfdee410c
keywords:
- Contrôles Windows de code de notification TBN_GETBUTTONINFO
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942533"
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

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** si les informations sur le bouton ont été copiées dans la structure spécifiée, ou **false** dans le cas contraire.

## <a name="remarks"></a>Notes

Le contrôle ToolBar alloue une mémoire tampon et le récepteur (fenêtre parente) doit copier le texte dans cette mémoire tampon. Le membre **cchText** contient la longueur de la mémoire tampon allouée par la barre d’outils lorsque TBN \_ GETBUTTONINFO est envoyé à la fenêtre parente.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **TBN \_ GETBUTTONINFOW** (Unicode) et **TBN \_ GETBUTTONINFOA** (ANSI)<br/>       |



 

 





