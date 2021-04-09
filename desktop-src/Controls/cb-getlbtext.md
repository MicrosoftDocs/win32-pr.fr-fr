---
title: Message CB_GETLBTEXT (winuser. h)
description: Obtient une chaîne à partir de la liste d’une zone de liste déroulante.
ms.assetid: f84e302a-65bb-45c8-958b-1cb438fb5a7a
keywords:
- CB_GETLBTEXT les contrôles de message Windows
topic_type:
- apiref
api_name:
- CB_GETLBTEXT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d26a964b463daedab1ad5d9f50888b3e0c1e0db
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104032853"
---
# <a name="cb_getlbtext-message"></a>\_Message GETLBTEXT CB

Obtient une chaîne à partir de la liste d’une zone de liste déroulante.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de base zéro de la chaîne à récupérer.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers la mémoire tampon qui reçoit la chaîne. La mémoire tampon doit avoir suffisamment d’espace pour la chaîne et un caractère null de fin. Vous pouvez envoyer un message [**CB \_ GETLBTEXTLEN**](cb-getlbtextlen.md) avant le message **\_ GETLBTEXT CB** pour récupérer la longueur, dans **TCHAR** s, de la chaîne. S’il s’agit d’une chaîne ANSI, il s’agit du nombre d’octets, mais s’il s’agit d’une chaîne Unicode, il s’agit du nombre de caractères.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est la longueur de la chaîne, dans **TCHAR** s, à l’exclusion du caractère null de fin. Si *wParam* ne spécifie pas d’index valide, la valeur de retour est CB \_ Err.

## <a name="remarks"></a>Notes

**Avertissement de sécurité :** L’utilisation incorrecte de ce message peut compromettre la sécurité de votre programme. Ce message n’offre aucun moyen de connaître la taille de la mémoire tampon. Si vous utilisez ce message, appelez d’abord [**CB \_ GETLBTEXTLEN**](cb-getlbtextlen.md) pour obtenir le nombre de caractères requis, puis appelez le message pour récupérer la chaîne. Vous devez examiner les [considérations relatives à la sécurité : contrôles Microsoft Windows](sec-comctls.md) avant de continuer.

Si vous créez la zone de liste déroulante avec un style owner-drawn mais sans le style [**CBS \_ HASSTRINGS**](combo-box-styles.md) , la mémoire tampon vers laquelle pointe *lParam* reçoit les données associées à l’élément.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_GETLBTEXTLEN CB**](cb-getlbtextlen.md)
</dt> </dl>

 

 





