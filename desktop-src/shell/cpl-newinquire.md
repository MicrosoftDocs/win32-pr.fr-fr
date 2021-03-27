---
description: Envoyé à la fonction CPlApplet d’une application du panneau de configuration pour demander des informations sur une boîte de dialogue que l’application prend en charge.
title: Message CPL_NEWINQUIRE (CPL. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: af52889c-7180-4690-8ed1-a0eb0a9dff35
api_name:
- CPL_NEWINQUIRE
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 72992d4ea867bc091c29feaa99cc1a22c2a02b2b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972046"
---
# <a name="cpl_newinquire-message"></a>\_Message NEWINQUIRE cpl

Envoyé à la fonction [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) d’une application du panneau de configuration pour demander des informations sur une boîte de dialogue que l’application prend en charge.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*uAppNum* 
</dt> <dd>

Numéro de la boîte de dialogue. Ce nombre doit être compris entre zéro et une valeur inférieure à la valeur renvoyée en réponse au message [**Cpl \_ GETCOUNT**](cpl-getcount.md) (CPL \_ GetCount – 1).

</dd> <dt>

*lpncpli* 
</dt> <dd>

Adresse d’une structure [**NEWCPLINFO**](/windows/win32/api/cpl/ns-cpl-newcplinfoa) . L’application du panneau de configuration doit remplir cette structure avec des informations sur la boîte de dialogue.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) traite ce message avec succès, elle doit retourner zéro.

## <a name="remarks"></a>Notes

Pour de meilleures performances, la plupart des applications doivent ignorer **Cpl \_ NEWINQUIRE** et traiter le message de [**\_ recherche de cpl**](cpl-inquire.md) à la place.

Le panneau de configuration envoie le message **\_ NEWINQUIRE Cpl** une fois pour chaque boîte de dialogue prise en charge par votre application. Le panneau de configuration envoie également un message de [**\_ recherche de cpl**](cpl-inquire.md) pour chaque boîte de dialogue. Ces messages sont envoyés immédiatement après le message [**Cpl \_ GETCOUNT**](cpl-getcount.md) . Toutefois, le système ne garantit **pas l’ordre \_** dans lequel les messages **\_ NEWINQUIRE et Cpl** sont envoyés.

Vous pouvez procéder à l’initialisation de la boîte de dialogue lorsque vous recevez l' [**\_ enquête Cpl**](cpl-inquire.md). Si vous devez allouer de la mémoire, faites-le en réponse au message d' [**\_ initialisation de cpl**](cpl-init.md) .

[**Cpl \_ L’interrogation**](cpl-inquire.md) est le message par défaut. Cela est dû au fait que **Cpl \_ NEWINQUIRE** retourne des informations dans un format que le système ne peut pas mettre en cache. Par conséquent, les applications qui traitent le tableau de bord **\_ NEWINQUIRE** doivent être chargées chaque fois que le panneau de configuration a besoin des informations, ce qui réduit considérablement les performances.

Les seules applications qui doivent utiliser **Cpl \_ NEWINQUIRE** sont celles qui ont besoin de modifier leur icône ou d’afficher des chaînes en fonction de l’état de l’ordinateur. Dans ce cas, votre gestionnaire de [**\_ recherche de cpl**](cpl-inquire.md) doit spécifier la \_ \_ valeur res dynamique CPL pour les membres **idIcon**, **idName** ou **idInfo** de la structure [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) , plutôt que de spécifier un identificateur de ressource valide. Cela amène le panneau de configuration à envoyer le message **\_ NEWINQUIRE Cpl** chaque fois qu’il a besoin de l’icône et des chaînes d’affichage, ce qui vous permet de spécifier des informations en fonction de l’état actuel de l’ordinateur. Bien entendu, cela est beaucoup plus lent que d’utiliser les informations mises en cache.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows XP uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>Cpl. h</dt> </dl> |



 

 
