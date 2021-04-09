---
title: Message TB_CHANGEBITMAP (commctrl. h)
description: Modifie l’image bitmap d’un bouton dans une barre d’outils.
ms.assetid: 112b6f4e-6034-4e13-8b2f-b8411a351fbd
keywords:
- TB_CHANGEBITMAP les contrôles de message Windows
topic_type:
- apiref
api_name:
- TB_CHANGEBITMAP
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1367a2a1b4e35d6f52bf1e7a0be42f1e75daa7ac
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844454"
---
# <a name="tb_changebitmap-message"></a>TO \_ CHANGEBITMAP message

Modifie l’image bitmap d’un bouton dans une barre d’outils.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Identificateur de commande du bouton qui doit recevoir une nouvelle image bitmap.

</dd> <dt>

*lParam* 
</dt> <dd>

Index de base zéro d’une image dans la liste d’images de la barre d’outils. Le système affiche l’image spécifiée dans le bouton. Affectez à ce paramètre la valeur I \_ IMAGECALLBACK et la barre d’outils enverra la notification [**\_ GETDISPINFO TBN**](tbn-getdispinfo.md) pour récupérer l’index d’image quand il est nécessaire.

[Version 5,81](common-control-versions.md). Affectez à ce paramètre \_ la valeur I IMAGENONE pour indiquer que le bouton n’a pas d’image. La disposition du bouton n’inclut pas d’espace pour une image bitmap, uniquement du texte.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne la **valeur true** en cas de réussite, ou **false** dans le cas contraire.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





