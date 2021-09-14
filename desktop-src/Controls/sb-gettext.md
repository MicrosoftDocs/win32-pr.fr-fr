---
title: Message SB_GETTEXT (commctrl. h)
description: Récupère le texte à partir de la partie spécifiée d’une fenêtre d’État.
ms.assetid: 95bef9ff-04e5-431e-bc79-06d8498fcab0
keywords:
- SB_GETTEXT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- SB_GETTEXT
- SB_GETTEXTA
- SB_GETTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e90b132c3f934188aea36afd86d53ab8f75bdadb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127117086"
---
# <a name="sb_gettext-message"></a>\_Message SB GETTEXT

Récupère le texte à partir de la partie spécifiée d’une fenêtre d’État.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de base zéro du composant à partir duquel récupérer du texte.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers la mémoire tampon qui reçoit le texte sous la forme d’une chaîne terminée par le caractère null. Utilisez le message [**SB \_ GETTEXTLENGTH**](sb-gettextlength.md) pour déterminer la taille requise pour la mémoire tampon.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne une valeur 32 bits qui se compose de valeurs 2 16 bits. Le mot de poids faible spécifie la longueur, en caractères, du texte. Le mot de poids fort spécifie le type d’opération utilisé pour dessiner le texte. Le type peut prendre l’une des valeurs suivantes.



| Code de retour                                                                                    | Description                                                                               |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| <dl> <dt>**0**</dt> </dl>               | Le texte est dessiné avec une bordure qui apparaît plus bas que le plan de la fenêtre.<br/>  |
| <dl> <dt>**SBT \_ NOfrontières**</dt> </dl>  | Le texte est dessiné sans bordures.<br/>                                             |
| <dl> <dt>**SBT \_ fenêtre indépendante**</dt> </dl>     | Le texte est dessiné avec une bordure qui doit apparaître plus haut que le plan de la fenêtre.<br/> |
| <dl> <dt>**SBT \_ RTLREADING**</dt> </dl> | Le texte s’affiche dans la direction opposée du texte dans la fenêtre parente.<br/>  |



 

## <a name="remarks"></a>Notes

**Avertissement de sécurité :** L’utilisation incorrecte de ce message peut compromettre la sécurité de votre programme. Ce message n’offre aucun moyen de connaître la taille de la mémoire tampon. Si vous utilisez ce message, appelez d’abord [**SB \_ GETTEXTLENGTH**](sb-gettextlength.md) pour obtenir le nombre de caractères requis, puis appelez le message pour récupérer la chaîne. Si vous attendez avant d’appeler SB, le texte pourrait changer, invalidant ainsi la valeur de retour de **SB \_ GETTEXTLENGTH**. **\_** vous devez examiner les [considérations relatives à la sécurité : contrôles Microsoft Windows](sec-comctls.md) avant de continuer.

Ce message retourne un maximum de 65 535 caractères. Si la chaîne de texte est plus longue, elle est tronquée.

Si le texte a le \_ type de dessin SBT OwnerDraw, ce message retourne la valeur 32 bits associée au texte au lieu de la longueur et du type d’opération.

Les fenêtres normales affichent le texte de gauche à droite (LTR). les Windows peuvent être *mis en miroir* pour afficher des langues telles que l’hébreu ou l’arabe, qui sont lues de droite à gauche (RTL). Si SBT \_ RTLREADING est défini, la chaîne *lParam* lit dans le sens opposé du texte dans la fenêtre parente.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **SB \_ GETTEXTW** (Unicode) et **SB \_ gettexta** (ANSI)<br/>                     |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**unisettext SB \_**](sb-settext.md)
</dt> </dl>

 

 





