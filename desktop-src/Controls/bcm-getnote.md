---
title: Message BCM_GETNOTE (commctrl. h)
description: Obtient le texte de la note associée à un bouton de lien de commande. Vous pouvez envoyer ce message de manière explicite ou utiliser le bouton \_ GetNote macro.
ms.assetid: ddaf4227-1316-49b5-abf0-00215472c46c
keywords:
- BCM_GETNOTE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- BCM_GETNOTE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 758dac90ba4c0f3087a6df90d9acf2c1321b1d73
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127120081"
---
# <a name="bcm_getnote-message"></a>\_Message GETNOTE BCM

Obtient le texte de la note associée à un bouton de lien de commande. Vous pouvez envoyer ce message de manière explicite ou utiliser le [**bouton \_ GetNote**](/windows/desktop/api/Commctrl/nf-commctrl-button_getnote) macro.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* \[ in, out\]
</dt> <dd>

**Valeur DWORD** qui spécifie la taille de la mémoire tampon vers laquelle pointe *lParam*, en caractères.

</dd> <dt>

*lParam* \[ à\]
</dt> <dd>

Mémoire tampon de chaîne devant recevoir le texte. La mémoire tampon doit être suffisamment grande pour contenir le caractère NULL de fin.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Si le message est correctement exécuté, la méthode retourne la **valeur true**. Sinon, elle retourne **false**.

## <a name="remarks"></a>Notes

Le **message \_ GETNOTE BCM** fonctionne uniquement avec les boutons qui ont le style de bouton [**BS \_ COMMANDLINK**](button-styles.md) ou [**BS \_ DEFCOMMANDLINK**](button-styles.md) .

[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) contient les éléments suivants :

-   ERREUR \_ non \_ prise en charge, si le bouton n’a pas le style [**BS \_ DEFCOMMANDLINK**](button-styles.md) ou [**BS \_ COMMANDLINK**](button-styles.md) .
-   ERREUR \_ de \_ mémoire tampon insuffisante, si la mémoire tampon *lParam* est trop petite. Le paramètre *wParam* contient la taille de mémoire tampon requise, en caractères.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2008 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[Styles de bouton](button-styles.md)
</dt> <dt>

**Conceptuel**
</dt> <dt>

[Types de bouton](button-types-and-styles.md)
</dt> </dl>

 

