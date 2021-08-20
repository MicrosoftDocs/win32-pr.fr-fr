---
title: Message SB_SETTEXT (commctrl. h)
description: Définit le texte dans la partie spécifiée d’une fenêtre d’État.
ms.assetid: 6039a61c-6ec6-42cd-94d5-5f1cf2998586
keywords:
- SB_SETTEXT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- SB_SETTEXT
- SB_SETTEXTA
- SB_SETTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fcf0a7928e87cbc614a59dc64b433223afa97bbdac3f45f1635cb8cfe7b34a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118408882"
---
# <a name="sb_settext-message"></a>\_Message SB SETTEXT

Définit le texte dans la partie spécifiée d’une fenêtre d’État.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Le [**LOBYTE**](/previous-versions/windows/desktop/legacy/ms632658(v=vs.85)) du mot de poids faible spécifie l’index de base zéro du composant à définir. Si **LOBYTE** a la valeur SB \_ SIMPLEID, la fenêtre d’État est supposée être une barre d’état de mode simple ; autrement dit, une barre d’État avec une seule partie.

Le [**HIBYTE**](/previous-versions/windows/desktop/legacy/ms632656(v=vs.85)) du mot de poids faible spécifie le type de l’opération de dessin. Ce paramètre peut prendre les valeurs suivantes.

Le mot de poids fort de *wParam* est ignoré.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Valeur</th>
<th>Signification</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span id="0"></span><dl> <dt><strong>entre</strong></dt> </dl></td>
<td>Le texte est dessiné avec une bordure qui apparaît plus bas que le plan de la fenêtre.<br/></td>
</tr>
<tr class="even">
<td><span id="SBT_NOBORDERS"></span><span id="sbt_noborders"></span><dl> <dt><strong>SBT_NOBORDERS</strong></dt> </dl></td>
<td>Le texte est dessiné sans bordures.<br/></td>
</tr>
<tr class="odd">
<td><span id="SBT_OWNERDRAW"></span><span id="sbt_ownerdraw"></span><dl> <dt><strong>SBT_OWNERDRAW</strong></dt> </dl></td>
<td>Le texte est dessiné par la fenêtre parente. <br/>
<blockquote>
[!Note]<br />
Une barre d’état de mode simple ne prend pas en charge le dessin owner-drawn.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span id="SBT_POPOUT"></span><span id="sbt_popout"></span><dl> <dt><strong>SBT_POPOUT</strong></dt> </dl></td>
<td>Le texte est dessiné avec une bordure qui doit apparaître plus haut que le plan de la fenêtre.<br/></td>
</tr>
<tr class="odd">
<td><span id="SBT_RTLREADING"></span><span id="sbt_rtlreading"></span><dl> <dt><strong>SBT_RTLREADING</strong></dt> </dl></td>
<td>Le texte s’affiche dans le sens inverse du texte de la fenêtre parente.<br/></td>
</tr>
<tr class="even">
<td><span id="SBT_NOTABPARSING"></span><span id="sbt_notabparsing"></span><dl> <dt><strong>SBT_NOTABPARSING</strong></dt> </dl></td>
<td>Les caractères de tabulation sont ignorés.<br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une chaîne se terminant par un caractère null qui spécifie le texte à définir. Si *wParam* est SBT \_ OwnerDraw, ce paramètre représente 32 bits de données. La fenêtre parente doit interpréter les données et dessiner le texte lorsqu’il reçoit le message [**WM \_ DRAWITEM**](wm-drawitem.md) .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="remarks"></a>Remarques

Le message invalide la partie de la fenêtre qui a changé, provoquant l’affichage du nouveau texte lorsque la fenêtre reçoit le message de [**\_ peinture WM**](/windows/desktop/gdi/wm-paint) .

Les fenêtres normales affichent le texte de gauche à droite (LTR). les Windows peuvent être *mis en miroir* pour afficher des langues telles que l’hébreu ou l’arabe, qui sont lues de droite à gauche (RTL). Si SBT \_ RTLREADING est défini, la chaîne *lParam* lira dans le sens inverse du texte de la fenêtre parente.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **SB \_ SETTEXTW** (Unicode) et **SB \_ SETTEXTA** (ANSI)<br/>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**SB \_ GETTEXT**](sb-gettext.md)
</dt> </dl>

 

