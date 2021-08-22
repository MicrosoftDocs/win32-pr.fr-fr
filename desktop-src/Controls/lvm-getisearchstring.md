---
title: Message LVM_GETISEARCHSTRING (commctrl. h)
description: Récupère la chaîne de recherche incrémentielle d’un contrôle List-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView GetISearchString.
ms.assetid: e953c4a0-0556-4987-8abf-3276e787fe49
keywords:
- LVM_GETISEARCHSTRING les contrôles de Windows de message
topic_type:
- apiref
api_name:
- LVM_GETISEARCHSTRING
- LVM_GETISEARCHSTRINGA
- LVM_GETISEARCHSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d612a6c1ba303bc08b6d5067ccb4dd3802354456159e3aea4120bd122348e74f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119540819"
---
# <a name="lvm_getisearchstring-message"></a>\_Message GETISEARCHSTRING LVM

Récupère la chaîne de recherche incrémentielle d’un contrôle List-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**ListView \_ GetISearchString**](/windows/desktop/api/Commctrl/nf-commctrl-listview_getisearchstring) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une mémoire tampon qui reçoit la chaîne de recherche incrémentielle. Pour récupérer uniquement la longueur de la chaîne, affectez à *lParam* la **valeur null**.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le nombre de caractères de la chaîne de recherche incrémentielle, à l’exclusion du caractère NULL de fin, ou zéro si le contrôle de liste n’est pas en mode de recherche incrémentielle.

## <a name="remarks"></a>Remarques

**Avertissement de sécurité :** L’utilisation incorrecte de ce message peut compromettre la sécurité de votre programme. Ce message n’offre aucun moyen de connaître la taille de la mémoire tampon. Si vous utilisez ce message, appelez tout d’abord le message qui passe **null** dans *lParam*, ce qui renvoie le nombre de caractères, à l’exception de la **valeur null** requise. Ensuite, appelez le message une seconde fois pour récupérer la chaîne. vous devez examiner les [considérations relatives à la sécurité : contrôles Microsoft Windows](sec-comctls.md) avant de continuer.

La *chaîne de recherche incrémentielle* correspond à la séquence de caractères que l’utilisateur tape lorsque l’affichage de liste a le focus d’entrée. Chaque fois que l’utilisateur tape un caractère, le système ajoute le caractère à la chaîne de recherche, puis recherche un élément correspondant. Si le système trouve une correspondance, il sélectionne l’élément et, si nécessaire, le fait défiler dans la vue.

Un délai d’attente est associé à chaque caractère que l’utilisateur tape. Si le délai d’attente s’écoule avant que l’utilisateur ne tape un autre caractère, la chaîne de recherche incrémentielle est réinitialisée.

Assurez-vous que la mémoire tampon est suffisamment grande pour contenir la chaîne et le caractère NULL de fin. S’il est trop petit, une erreur de page non valide est générée immédiatement.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **LVM \_ GETISEARCHSTRINGW** (Unicode) et **LVM \_ GETISEARCHSTRINGA** (ANSI)<br/> |



 

 





