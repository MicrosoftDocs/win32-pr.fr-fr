---
description: CPL_INQUIRE message-envoyé à la fonction CPlApplet d’une application du panneau de configuration pour demander des informations sur une boîte de dialogue que l’application prend en charge.
title: Message CPL_INQUIRE (CPL. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: daca87b7-f1ee-40f4-95d2-3150b595151e
api_name:
- CPL_INQUIRE
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5998e26eab79d3e5f0b9e3628614e1cc2ecbfb7040e866a898a09ad54fa49f10
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119710719"
---
# <a name="cpl_inquire-message"></a>\_Message de recherche cpl

Envoyé à la fonction [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) d’une application du panneau de configuration pour demander des informations sur une boîte de dialogue que l’application prend en charge.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*uAppNum* 
</dt> <dd>

Numéro de la boîte de dialogue. Ce nombre doit être compris entre zéro et une valeur inférieure à la valeur renvoyée en réponse au message [**Cpl \_ GETCOUNT**](cpl-getcount.md) (CPL \_ GetCount – 1).

</dd> <dt>

*lpcpli* 
</dt> <dd>

Adresse d’une structure [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) . L’application doit remplir cette structure avec des identificateurs de ressource pour l’icône, le nom abrégé, la description et toute valeur définie par l’utilisateur associée à la boîte de dialogue.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si la fonction [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) traite ce message avec succès, elle doit retourner zéro.

## <a name="remarks"></a>Remarques

Le panneau de configuration envoie le message de **\_ recherche Cpl** une fois pour chaque boîte de dialogue prise en charge par votre application. Le panneau de configuration envoie également un message [**\_ NEWINQUIRE Cpl**](cpl-newinquire.md) pour chaque boîte de dialogue. Ces messages sont envoyés immédiatement après le message [**Cpl \_ GETCOUNT**](cpl-getcount.md) . Toutefois, le système ne garantit **pas l’ordre \_** dans lequel les messages **\_ NEWINQUIRE et Cpl** sont envoyés.

Vous pouvez procéder à l’initialisation de la boîte de dialogue lorsque vous recevez l' **\_ enquête Cpl**. Si vous devez allouer de la mémoire, faites-le en réponse au message d' [**\_ initialisation de cpl**](cpl-init.md) .

Le [**message \_ NEWINQUIRE de cpl**](cpl-newinquire.md) retourne des informations dans un format que le système ne peut pas mettre en cache. Pour cette raison, la plupart des fonctions [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) doivent traiter le **panneau de \_ recherche** et ignorer **Cpl \_ NEWINQUIRE**.

Les seules applications qui doivent utiliser [**Cpl \_ NEWINQUIRE**](cpl-newinquire.md) sont celles qui ont besoin de modifier leur icône ou d’afficher des chaînes en fonction de l’état de l’ordinateur. Dans ce cas, votre gestionnaire de **\_ recherche de cpl** doit spécifier la \_ \_ valeur res dynamique CPL pour les membres **idIcon**, **idName** ou **idInfo** de la structure [**CPLINFO**](/windows/win32/api/cpl/ns-cpl-cplinfo) , plutôt que de spécifier un identificateur de ressource valide. Cela amène le panneau de configuration à envoyer le message **\_ NEWINQUIRE Cpl** chaque fois qu’il a besoin de l’icône et des chaînes d’affichage, ce qui vous permet de spécifier des informations en fonction de l’état actuel de l’ordinateur. Cela est beaucoup plus lent que d’utiliser les informations mises en cache.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau XP uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>Cpl. h</dt> </dl> |



 

 
