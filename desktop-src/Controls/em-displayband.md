---
title: Message EM_DISPLAYBAND (RichEdit. h)
description: Affiche une partie du contenu d’un contrôle RichEdit, tel qu’il a été précédemment mis en forme pour un appareil à l’aide du \_ message em FormatRange.
ms.assetid: 845513d0-f32b-418c-8255-a5caf2d56215
keywords:
- EM_DISPLAYBAND les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_DISPLAYBAND
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f51896a9ba5603e799609ab52989681ecf7bcac4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103942387"
---
# <a name="em_displayband-message"></a>\_Message DISPLAYBAND em

Affiche une partie du contenu d’un contrôle RichEdit, tel qu’il a été précédemment mis en forme pour un appareil à l’aide du message [**em \_ FormatRange**](em-formatrange.md) .

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Ce paramètre n’est pas utilisé ; elle doit être égale à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Une structure [**Rect**](/previous-versions//dd162897(v=vs.85)) spécifiant la zone d’affichage de l’appareil.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Si l’opération a échoué, la valeur de retour est **true**.

Si l’opération échoue, la valeur de retour est **false**.

## <a name="remarks"></a>Notes

Les objets de texte et de modèle COM (Component Object Model) sont découpés par le rectangle. L’application n’a pas besoin de définir la zone de découpage.

La bande est le processus par lequel une seule page de sortie est générée à l’aide d’un ou de plusieurs rectangles séparés, ou de bandes. Lorsque toutes les bandes sont placées sur la page, une image complète les résultats. Cette approche est souvent utilisée par les imprimantes raster qui ne disposent pas de suffisamment de mémoire ou de capacité à effectuer une image de page entière à la fois. Les périphériques de bandes incluent la plupart des imprimantes matricielles, ainsi que certaines imprimantes laser.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Impression de contrôles RichEdit](printing-rich-edit-controls.md)
</dt> </dl>

 

