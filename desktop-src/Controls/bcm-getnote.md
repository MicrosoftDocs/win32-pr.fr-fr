---
title: Message BCM_GETNOTE (commctrl. h)
description: Obtient le texte de la note associée à un bouton de lien de commande. Vous pouvez envoyer ce message de manière explicite ou utiliser le bouton \_ GetNote macro.
ms.assetid: ddaf4227-1316-49b5-abf0-00215472c46c
keywords:
- BCM_GETNOTE les contrôles de message Windows
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106527571"
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

## <a name="return-value"></a>Valeur retournée

Si le message est correctement exécuté, la méthode retourne la **valeur true**. Sinon, elle retourne **false**.

## <a name="remarks"></a>Notes

Le **message \_ GETNOTE BCM** fonctionne uniquement avec les boutons qui ont le style de bouton [**BS \_ COMMANDLINK**](button-styles.md) ou [**BS \_ DEFCOMMANDLINK**](button-styles.md) .

[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) contient les éléments suivants :

-   ERREUR \_ non \_ prise en charge, si le bouton n’a pas le style [**BS \_ DEFCOMMANDLINK**](button-styles.md) ou [**BS \_ COMMANDLINK**](button-styles.md) .
-   ERREUR \_ de \_ mémoire tampon insuffisante, si la mémoire tampon *lParam* est trop petite. Le paramètre *wParam* contient la taille de mémoire tampon requise, en caractères.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2008 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[Styles de bouton](button-styles.md)
</dt> <dt>

**Méthodologique**
</dt> <dt>

[Types de bouton](button-types-and-styles.md)
</dt> </dl>

 

