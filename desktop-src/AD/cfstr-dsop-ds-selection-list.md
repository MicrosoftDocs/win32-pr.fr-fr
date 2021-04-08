---
title: CFSTR_DSOP_DS_SELECTION_LIST (objsel. h)
description: Le \_ format de \_ presse-papiers de la liste de sélection DS CFSTR DSOP \_ \_ fournit un HGLOBAL qui contient une structure de liste de sélection des services d’annuaire \_ \_ . La structure de la liste de sélection des services \_ \_ d’annuaire contient des données sur les éléments sélectionnés dans la boîte de dialogue Sélecteur d’objets d’annuaire.
ms.assetid: cd634e3b-0eb7-4144-b9e1-1d27a322f72c
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- CFSTR_DSOP_DS_SELECTION_LIST
api_location:
- Objsel.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b783b0790ed87a292cd171cb8283333d5b9bd5b3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103941967"
---
# <a name="cfstr_dsop_ds_selection_list"></a>liste de sélection de CFSTR \_ DSOP \_ DS \_ \_

<dl> <dt>

<span id="CFSTR_DSOP_DS_SELECTION_LIST"></span><span id="cfstr_dsop_ds_selection_list"></span>**liste de sélection de CFSTR \_ DSOP \_ DS \_ \_**
</dt> <dd> <dl> <dt>

« \_ liste de sélection CFSTR DSOP \_ DS \_ \_ »
</dt> <dt>



Le format de presse-papiers de la **\_ \_ \_ \_ liste de sélection DS CFSTR DSOP** est fourni par l' [**IDataObject**](/windows/win32/api/objidl/nn-objidl-idataobject) obtenu en appelant [**IDsObjectPicker :: InvokeDialog**](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-invokedialog). Le format de presse-papiers de la **\_ \_ \_ \_ liste de sélection DS CFSTR DSOP** fournit un **HGLOBAL** qui contient une structure de [**\_ \_ liste de sélection des services d’annuaire**](/windows/desktop/api/Objsel/ns-objsel-ds_selection_list) . La structure de la **\_ \_ liste de sélection des services** d’annuaire contient des données sur les éléments sélectionnés dans la boîte de dialogue Sélecteur d’objets d' [Annuaire](directory-object-picker.md) .


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Vista<br/>                                                            |
| Serveur minimal pris en charge<br/> | Windows Server 2008<br/>                                                      |
| En-tête<br/>                   | <dl> <dt>Objsel. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_liste de sélection DS \_**](/windows/desktop/api/Objsel/ns-objsel-ds_selection_list)
</dt> <dt>

[**IDsObjectPicker::InvokeDialog**](/windows/desktop/api/Objsel/nf-objsel-idsobjectpicker-invokedialog)
</dt> <dt>

[Sélecteur d’objets d’annuaire](directory-object-picker.md)
</dt> </dl>

 

