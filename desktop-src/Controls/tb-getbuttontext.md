---
title: Message TB_GETBUTTONTEXT (commctrl. h)
description: Récupère le texte d’affichage d’un bouton dans une barre d’outils.
ms.assetid: 16dd7181-a404-4056-b084-05f49f5a4b14
keywords:
- TB_GETBUTTONTEXT les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TB_GETBUTTONTEXT
- TB_GETBUTTONTEXTA
- TB_GETBUTTONTEXTW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ec63815886ecc32f8f0b0759b9f6a8cf847bfe56e6c898fd6e3a3ae8e0f40ac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117829765"
---
# <a name="tb_getbuttontext-message"></a>TO \_ GETBUTTONTEXT message

Récupère le texte d’affichage d’un bouton dans une barre d’outils.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Identificateur de commande du bouton dont le texte doit être récupéré.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une mémoire tampon qui reçoit le texte du bouton.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la longueur, en caractères, de la chaîne désignée par *lParam*. La longueur n’inclut pas le caractère null de fin. En cas d’échec, la valeur de retour est-1.

## <a name="remarks"></a>Remarques

**Avertissement de sécurité :** L’utilisation incorrecte de ce message peut compromettre la sécurité de votre programme. Ce message n’offre aucun moyen de connaître la taille de la mémoire tampon. Si vous utilisez ce message, appelez tout d’abord le message qui passe **null** dans *lParam*, ce qui renvoie le nombre de caractères, à l’exception de la **valeur null** requise. Ensuite, appelez le message une seconde fois pour récupérer la chaîne. vous devez examiner les [considérations relatives à la sécurité : contrôles Microsoft Windows](sec-comctls.md) avant de continuer.

La chaîne retournée correspond au texte actuellement affiché par le bouton.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **To \_ GETBUTTONTEXTW** (Unicode) et **to \_ GETBUTTONTEXTA** (ANSI)<br/>         |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**TO \_ GETBUTTONINFO**](tb-getbuttoninfo.md)
</dt> <dt>

[**TO \_ GETSTRING**](tb-getstring.md)
</dt> <dt>

[**TO \_ SETBUTTONINFO**](tb-setbuttoninfo.md)
</dt> </dl>

 

 





