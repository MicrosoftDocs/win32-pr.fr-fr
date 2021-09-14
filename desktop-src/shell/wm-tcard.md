---
description: envoyé à une application qui a initié une carte d’apprentissage avec Windows aide.
title: Message WM_TCARD (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: fdde7603-9913-4e80-9502-2142ef8a511c
api_name:
- WM_TCARD
api_type:
- HeaderDef
api_location:
- Winuser.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5eb6a3b5a4b840549b75e152f0420bfa055138c4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127196380"
---
# <a name="wm_tcard-message"></a>\_Message WM TCARD

envoyé à une application qui a initié une carte d’apprentissage avec Windows aide. Le message informe l’application lorsque l’utilisateur clique sur un bouton autorisé. Une application initie une carte d’apprentissage en spécifiant la \_ commande help TCARD dans un appel à la fonction [**WinHelp**](/windows/desktop/api/Winuser/nf-winuser-winhelpa) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*idAction* 
</dt> <dd>

Valeur qui indique l’action effectuée par l’utilisateur. Il peut s’agir de l’une des valeurs suivantes.

<dt>

<span id="IDABORT"></span><span id="idabort"></span>

<span id="IDABORT"></span><span id="idabort"></span>**IDABORT**


</dt> <dd>

L’utilisateur a cliqué sur un bouton d' **annulation** autorisé.

</dd> <dt>

<span id="IDCANCEL"></span><span id="idcancel"></span>

<span id="IDCANCEL"></span><span id="idcancel"></span>**IDCANCEL**


</dt> <dd>

L’utilisateur a cliqué sur un bouton d' **annulation** autorisé.

</dd> <dt>

<span id="IDCLOSE"></span><span id="idclose"></span>

<span id="IDCLOSE"></span><span id="idclose"></span>**IDCLOSE**


</dt> <dd>

L’utilisateur a fermé la carte de formation.

</dd> <dt>

<span id="IDHELP"></span><span id="idhelp"></span>

<span id="IDHELP"></span><span id="idhelp"></span>**IDHELP**


</dt> <dd>

l’utilisateur a cliqué sur un bouton **d’aide** Windows auteur.

</dd> <dt>

<span id="IDIGNORE"></span><span id="idignore"></span>

<span id="IDIGNORE"></span><span id="idignore"></span>**IDIGNORE**


</dt> <dd>

L’utilisateur a cliqué sur un bouton de l’autorisation autoriser **Ignorer** .

</dd> <dt>

<span id="IDOK"></span><span id="idok"></span>

<span id="IDOK"></span><span id="idok"></span>**IDOK**


</dt> <dd>

L’utilisateur a cliqué sur un bouton autorisé **OK** .

</dd> <dt>

<span id="IDNO"></span><span id="idno"></span>

<span id="IDNO"></span><span id="idno"></span>**IDNO**


</dt> <dd>

L’utilisateur a cliqué sur un bouton **sans** autorisation.

</dd> <dt>

<span id="IDRETRY"></span><span id="idretry"></span>

<span id="IDRETRY"></span><span id="idretry"></span>**IDRETRY**


</dt> <dd>

L’utilisateur a cliqué sur un bouton de **nouvelle tentative** autorisé.

</dd> <dt>

<span id="HELP_TCARD_DATA"></span><span id="help_tcard_data"></span>

<span id="HELP_TCARD_DATA"></span><span id="help_tcard_data"></span>**AIDE sur les \_ \_ données TCARD**


</dt> <dd>

L’utilisateur a cliqué sur un bouton autorisé. Le paramètre *dwActionData* contient un entier long spécifié par l’auteur de l’aide.

</dd> <dt>

<span id="HELP_TCARD_OTHER_CALLER"></span><span id="help_tcard_other_caller"></span>

<span id="HELP_TCARD_OTHER_CALLER"></span><span id="help_tcard_other_caller"></span>**AIDE \_ TCARD \_ autre \_ appelant**


</dt> <dd>

Une autre application a demandé des cartes de formation.

</dd> <dt>

<span id="IDYES"></span><span id="idyes"></span>

<span id="IDYES"></span><span id="idyes"></span>**IDYES**


</dt> <dd>

L’utilisateur a cliqué sur un bouton autoriser **Oui** .

</dd> </dl> </dd> <dt>

*dwActionData* 
</dt> <dd>

Si *idAction* spécifie Help \_ TCARD \_ Data, ce paramètre est une **valeur de type long** spécifiée par l’auteur de l’aide. Dans le cas contraire, ce paramètre est égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

La valeur de retour est ignorée ; utilisez zéro.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                 |
| En-tête<br/>                   | <dl> <dt>Winuser. h</dt> </dl> |



 

 




