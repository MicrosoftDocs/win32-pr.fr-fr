---
title: Message EM_SETLANGOPTIONS (RichEdit. h)
description: Définit les options de l’éditeur de méthode d’entrée (IME) et de la prise en charge des langues asiatiques dans un contrôle RichEdit.
ms.assetid: d42d0512-3339-471d-a91a-114151554799
keywords:
- EM_SETLANGOPTIONS les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_SETLANGOPTIONS
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e5095c599dfa78740ce4cb081e4d52c33b2debd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127006384"
---
# <a name="em_setlangoptions-message"></a>\_Message SETLANGOPTIONS em

Définit les options de l’éditeur de méthode d’entrée (IME) et de la prise en charge des langues asiatiques dans un contrôle RichEdit.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Spécifie les options de langue. Pour obtenir la liste des valeurs possibles, consultez [**em \_ GETLANGOPTIONS**](em-getlangoptions.md).

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Ce message retourne la valeur 1.

## <a name="remarks"></a>Notes

Le message **em \_ SETLANGOPTIONS** contrôle les éléments suivants :

-   Liaison de police automatique.
-   Basculement automatique du clavier.
-   Ajustement automatique de la taille de la police.
-   Utilisation des polices par défaut de l’interface utilisateur au lieu des polices par défaut du document.
-   Notifications au client lors de la composition de l’IME.
-   Abandon du mode de composition par l’IME.
-   Vérification de l’orthographe, correction automatique et prédiction du clavier tactile.

Ce message définit les valeurs de tous les indicateurs d’option de langage. Pour modifier un sous-ensemble des indicateurs, envoyez le message [**em \_ GETLANGOPTIONS**](em-getlangoptions.md) pour obtenir les indicateurs d’option actuels, modifiez les indicateurs que vous devez modifier, puis envoyez le **message \_ SETLANGOPTIONS em** avec le résultat.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_GETLANGOPTIONS em**](em-getlangoptions.md)
</dt> </dl>

 

 





