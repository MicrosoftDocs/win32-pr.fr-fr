---
title: Message TVM_GETISEARCHSTRING (commctrl. h)
description: Récupère la chaîne de recherche incrémentielle pour un contrôle Tree-View.
ms.assetid: 71f9a9b6-e124-4655-80fc-dd23f441496d
keywords:
- TVM_GETISEARCHSTRING les contrôles de Windows de message
topic_type:
- apiref
api_name:
- TVM_GETISEARCHSTRING
- TVM_GETISEARCHSTRINGA
- TVM_GETISEARCHSTRINGW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79838b2b0d2f109216caf970d33d51b4a3c1369da7b1fc47f5a53e45c3ee82fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120060239"
---
# <a name="tvm_getisearchstring-message"></a>TVM \_ GETISEARCHSTRING message

Récupère la chaîne de recherche incrémentielle pour un contrôle Tree-View. Le contrôle Tree-View utilise la chaîne de recherche incrémentielle pour sélectionner un élément en fonction des caractères tapés par l’utilisateur. Vous pouvez envoyer ce message explicitement ou à l’aide de la macro [**\_ GetISearchString TreeView**](/windows/desktop/api/Commctrl/nf-commctrl-treeview_getisearchstring) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>Doit être zéro.</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers la mémoire tampon qui reçoit la chaîne de recherche incrémentielle.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne le nombre de caractères dans la chaîne de recherche incrémentielle.

## <a name="remarks"></a>Remarques

**Avertissement de sécurité :** L’utilisation incorrecte de ce message peut compromettre la sécurité de votre programme. Vous devez allouer une mémoire tampon suffisamment grande pour contenir la chaîne. Appelez tout d’abord le message qui passe **null** dans *lParam*. Cela retourne le nombre de caractères, à l’exception de **null**, qui sont requis. Ensuite, appelez le message une seconde fois pour récupérer la chaîne. vous devez examiner les [considérations relatives à la sécurité : contrôles Microsoft Windows](sec-comctls.md) avant de continuer.

Si le contrôle Tree-View n’est pas en mode de recherche incrémentielle, la valeur de retour est zéro.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Noms Unicode et ANSI<br/>   | **TVM \_ GETISEARCHSTRINGW** (Unicode) et **TVM \_ GETISEARCHSTRINGA** (ANSI)<br/> |



 

 





