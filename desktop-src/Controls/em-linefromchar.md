---
title: Message EM_LINEFROMCHAR (winuser. h)
description: Obtient l’index de la ligne qui contient l’index de caractère spécifié dans un contrôle d’édition multiligne.
ms.assetid: e8e9217b-3f0c-478d-b44d-2a51868dbc5a
keywords:
- EM_LINEFROMCHAR les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_LINEFROMCHAR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f0dfe0c6c2ed0f9d77817fddde75fa18b64d485f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103373"
---
# <a name="em_linefromchar-message"></a>\_Message LINEFROMCHAR em

Obtient l’index de la ligne qui contient l’index de caractère spécifié dans un contrôle d’édition multiligne. Un index de caractère est l’index de base zéro du caractère à partir du début du contrôle d’édition. Vous pouvez envoyer ce message à un contrôle d’édition ou à un contrôle d’édition enrichi.

## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Index de caractère du caractère contenu dans la ligne dont le nombre doit être récupéré. Si ce paramètre a la valeur-1, **em \_ LINEFROMCHAR** récupère le numéro de ligne de la ligne active (la ligne qui contient le signe insertion) ou, s’il y a une sélection, le numéro de ligne de la ligne contenant le début de la sélection.

</dd> <dt>

*lParam* 
</dt> <dd>

Ce paramètre n'est pas utilisé.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

La valeur de retour est le numéro de ligne de base zéro de la ligne contenant l’index de caractère spécifié par *wParam*.

## <a name="remarks"></a>Notes

**Modification riche :** Pris en charge dans Microsoft Rich Edit 1,0 et versions ultérieures. Si l’index de caractère est supérieur à 64 000, utilisez le message [**em \_ EXLINEFROMCHAR**](em-exlinefromchar.md) . Pour plus d’informations sur la compatibilité des versions RichEdit avec les différentes versions du système, consultez [à propos des contrôles](about-rich-edit-controls.md)RichEdit.

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows Vista uniquement\]<br/>                                                           |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2003 \[ uniquement\]<br/>                                                     |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**\_EXLINEFROMCHAR em**](em-exlinefromchar.md)
</dt> <dt>

[**\_LINEINDEX em**](em-lineindex.md)
</dt> </dl>

 

 





