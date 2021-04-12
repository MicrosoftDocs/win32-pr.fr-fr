---
title: Message EM_SETTABSTOPS (winuser. h)
description: Le \_ message em SETTABSTOPS définit les taquets de tabulation dans un contrôle d’édition multiligne.
ms.assetid: d6fe2828-4ae9-4652-ace0-2f71e146f777
keywords:
- EM_SETTABSTOPS les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_SETTABSTOPS
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48d076dea415f169eff46101fd7cfe632d73d976
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104212"
---
# <a name="em_settabstops-message"></a>\_Message SETTABSTOPS em

Le message **em \_ SETTABSTOPS** définit les taquets de tabulation dans un contrôle d’édition multiligne. Lorsque du texte est copié dans le contrôle, tout caractère de tabulation dans le texte entraîne la génération de l’espace jusqu’au taquet de tabulation suivant.

Ce message est traité uniquement par les contrôles d’édition multiligne. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Nombre de taquets de tabulation contenus dans le tableau. Si ce paramètre est égal à zéro, le paramètre *lParam* est ignoré et les taquets de tabulation par défaut sont définis à chaque unité de modèle de boîte de dialogue 32. Si ce paramètre a la valeur 1, les taquets de tabulation sont définis à toutes les *n* unités de modèle de boîte de dialogue, où *n* est la distance vers laquelle pointe le paramètre *lParam* . Si ce paramètre est supérieur à 1, *lParam* est un pointeur vers un tableau de taquets de tabulation.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers un tableau d’entiers non signés qui spécifie les taquets de tabulation dans les unités du modèle de boîte de dialogue. Si le paramètre *wParam* est 1, ce paramètre est un pointeur vers un entier non signé qui contient la distance entre tous les taquets de tabulation, dans les unités de modèle de boîte de dialogue.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si tous les onglets sont définis, la valeur de retour est **true**.

Si tous les onglets ne sont pas définis, la valeur de retour est **false**.

## <a name="remarks"></a>Notes

Le **message \_ SETTABSTOPS em** ne redessine pas automatiquement la fenêtre de contrôle d’édition. Si l’application modifie les taquets de tabulation pour le texte déjà présent dans le contrôle d’édition, elle doit appeler la fonction [**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect) pour redessiner la fenêtre de contrôle d’édition.

Les valeurs spécifiées dans le tableau se trouvent dans les unités de modèle de boîte de dialogue, qui sont les unités indépendantes du périphérique utilisées dans les modèles de boîte de dialogue. Pour convertir des mesures à partir d’unités de modèle de boîte de dialogue en unités d’écran (pixels), utilisez la fonction [**MapDialogRect**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect) .

**Modification riche :** Pris en charge dans Microsoft Rich Edit 3,0 et versions ultérieures. Un contrôle RichEdit peut avoir le nombre maximal de taquets de tabulation spécifiés par les \_ taquets de tabulation Max \_ . Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Autres ressources**
</dt> <dt>

[**InvalidateRect**](/windows/desktop/api/winuser/nf-winuser-invalidaterect)
</dt> <dt>

[**MapDialogRect**](/windows/desktop/api/winuser/nf-winuser-mapdialogrect)
</dt> </dl>

 

