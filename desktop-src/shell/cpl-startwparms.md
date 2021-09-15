---
description: Envoyé pour notifier à CPlApplet que l’utilisateur a choisi l’icône associée à une boîte de dialogue donnée. CPlApplet doit afficher la boîte de dialogue correspondante et effectuer toutes les tâches spécifiées par l’utilisateur.
title: Message CPL_STARTWPARMS (CPL. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 04ac5117-39c9-4d3f-b32d-8f8d2b515be1
api_name:
- CPL_STARTWPARMS
api_type:
- HeaderDef
api_location:
- Cpl.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 790779c1c45acbc211fe36e28b2e55d5ae2e60da
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127412565"
---
# <a name="cpl_startwparms-message"></a>\_Message STARTWPARMS cpl

Envoyé pour notifier à [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) que l’utilisateur a choisi l’icône associée à une boîte de dialogue donnée. **CPlApplet** doit afficher la boîte de dialogue correspondante et effectuer toutes les tâches spécifiées par l’utilisateur.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*uAppNum* 
</dt> <dd>

Numéro de la boîte de dialogue. Ce nombre doit être compris entre zéro et une valeur inférieure à la valeur renvoyée en réponse au message [**Cpl \_ GETCOUNT**](cpl-getcount.md) (CPL \_ GetCount – 1).

</dd> <dt>

*lpszExtra* 
</dt> <dd>

Chaîne avec des instructions supplémentaires pour l’exécution.

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Retourne la **valeur true** si le message a été géré, ou **false** dans le cas contraire.

## <a name="remarks"></a>Notes

**Cpl \_ STARTWPARMS** est similaire à [**Cpl \_ DBLCLK**](cpl-dblclk.md) , mais vous permet de passer une chaîne à [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) au lieu d’un **int**. Vous pouvez utiliser cette chaîne comme une méthode flexible pour fournir des instructions détaillées pour l’exécution.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professional, Windows XP \[ desktop apps uniquement\]<br/>           |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                             |
| En-tête<br/>                   | <dl> <dt>Cpl. h</dt> </dl> |



 

 
