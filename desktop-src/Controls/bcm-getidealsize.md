---
title: Message BCM_GETIDEALSIZE (commctrl. h)
description: Obtient la taille du bouton qui correspond le mieux à son texte et à son image, si une liste d’images est présente. Vous pouvez envoyer ce message de manière explicite ou utiliser le bouton \_ GetIdealSize macro.
ms.assetid: c1bc2043-bf1a-4129-a005-f04048c4c1db
keywords:
- BCM_GETIDEALSIZE les contrôles de message Windows
topic_type:
- apiref
api_name:
- BCM_GETIDEALSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 446f4acba39b8b9722ef1a01a223f671b56ae845
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "106510139"
---
# <a name="bcm_getidealsize-message"></a>\_Message GETIDEALSIZE BCM

Obtient la taille du bouton qui correspond le mieux à son texte et à son image, si une liste d’images est présente. Vous pouvez envoyer ce message de manière explicite ou utiliser le [**bouton \_ GetIdealSize**](/windows/desktop/api/Commctrl/nf-commctrl-button_getidealsize) macro.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Pointeur vers une structure de [**taille**](/previous-versions//dd145106(v=vs.85)) qui reçoit la taille souhaitée du bouton, y compris le texte et la liste d’images, le cas échéant. L’application appelante est chargée d’allouer cette structure. Définissez les membres **CX** et **CY** sur zéro pour que la hauteur et la largeur idéales soient retournées dans la structure **Size** . Pour spécifier une largeur de bouton, définissez le membre **CX** sur la largeur de bouton souhaitée. Le système calcule la hauteur idéale pour cette largeur et le retourne dans le membre **CY** .

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si le message est correctement exécuté, la méthode retourne la **valeur true**. Sinon, elle retourne **false**.

## <a name="remarks"></a>Notes

> [!Note]  
> Si aucune largeur de bouton spéciale n’est souhaitée, vous devez définir les deux membres de [**Size**](/previous-versions//dd145106(v=vs.85)) sur zéro pour calculer et retourner la hauteur et la largeur idéales. Si la valeur du membre **CX** est supérieure à zéro, cette valeur est considérée comme la largeur de bouton souhaitée et la hauteur idéale pour cette largeur est calculée et retournée dans le membre **CY** .

 

Ce message s’applique aux boutons de bouton. Lorsqu’il est envoyé à un PushButton, le message récupère le rectangle englobant requis pour afficher le texte du bouton. En outre, si le PushButton a une liste d’images, le rectangle englobant est également dimensionné pour inclure l’image du bouton.

Lorsqu’elle est envoyée à un bouton de tout autre type, la taille du rectangle de fenêtre du contrôle est récupérée.

> [!Note]  
> Pour utiliser ce message, vous devez fournir un manifeste spécifiant Comclt32.dll version 6,0. Pour plus d’informations sur les manifestes, consultez [activation des styles visuels](cookbook-overview.md).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

