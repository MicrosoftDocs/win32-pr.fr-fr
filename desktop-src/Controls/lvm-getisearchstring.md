---
title: Message LVM_GETISEARCHSTRING (commctrl. h)
description: Récupère la chaîne de recherche incrémentielle d’un contrôle List-View. Vous pouvez envoyer ce message explicitement ou à l’aide de la \_ macro ListView GetISearchString.
ms.assetid: e953c4a0-0556-4987-8abf-3276e787fe49
keywords:
- LVM_GETISEARCHSTRING les contrôles de message Windows
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
ms.openlocfilehash: 9040cf96c5c483b29764b1ccfb67e0e4fff3f897
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466514"
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

## <a name="remarks"></a>Notes

**Avertissement de sécurité :** L’utilisation incorrecte de ce message peut compromettre la sécurité de votre programme. Ce message n’offre aucun moyen de connaître la taille de la mémoire tampon. Si vous utilisez ce message, appelez tout d’abord le message qui passe **null** dans *lParam*, ce qui renvoie le nombre de caractères, à l’exception de la **valeur null** requise. Ensuite, appelez le message une seconde fois pour récupérer la chaîne. Vous devez examiner les [considérations relatives à la sécurité : contrôles Microsoft Windows](sec-comctls.md) avant de continuer.

La *chaîne de recherche incrémentielle* correspond à la séquence de caractères que l’utilisateur tape lorsque l’affichage de liste a le focus d’entrée. Chaque fois que l’utilisateur tape un caractère, le système ajoute le caractère à la chaîne de recherche, puis recherche un élément correspondant. Si le système trouve une correspondance, il sélectionne l’élément et, si nécessaire, le fait défiler dans la vue.

Un délai d’attente est associé à chaque caractère que l’utilisateur tape. Si le délai d’attente s’écoule avant que l’utilisateur ne tape un autre caractère, la chaîne de recherche incrémentielle est réinitialisée.

Assurez-vous que la mémoire tampon est suffisamment grande pour contenir la chaîne et le caractère NULL de fin. S’il est trop petit, une erreur de page non valide est générée immédiatement.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **LVM \_ GETISEARCHSTRINGW** (Unicode) et **LVM \_ GETISEARCHSTRINGA** (ANSI)<br/> |



 

 





