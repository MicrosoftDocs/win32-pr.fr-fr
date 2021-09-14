---
title: Constantes DROPEFFECT (OleIdl. h)
description: Représente des informations sur les effets d’une opération de glisser-déplacer.
ms.assetid: d8e46899-3fbf-4012-8dd3-67fa627526d5
topic_type:
- apiref
api_name:
- DROPEFFECT_NONE
- DROPEFFECT_COPY
- DROPEFFECT_MOVE
- DROPEFFECT_LINK
- DROPEFFECT_SCROLL
api_location:
- OleIdl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2b1888aa028d4e047a9a8ec1f54e2497fa28ce4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193027"
---
# <a name="dropeffect-constants"></a>Constantes DROPEFFECT

Représente des informations sur les effets d’une opération de glisser-déplacer. La fonction [**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop) et la plupart des méthodes dans [**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource) et [**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget) utilisent les valeurs de cette énumération.



| Constante/valeur                                                                                                                                                                                                                            | Description                                                                                                                         |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DROPEFFECT_NONE"></span><span id="dropeffect_none"></span><dl> <dt>**DROPEFFECT \_ AUCUN**</dt> <dt>0</dt> </dl>                | La cible de dépôt ne peut pas accepter les données.<br/>                                                                                      |
| <span id="DROPEFFECT_COPY"></span><span id="dropeffect_copy"></span><dl> <dt>**DROPEFFECT \_ COPIE**</dt> <dt>1</dt> </dl>                | Déposer les résultats dans une copie. Les données d’origine ne sont pas touchées par la source de glissement.<br/>                                               |
| <span id="DROPEFFECT_MOVE"></span><span id="dropeffect_move"></span><dl> <dt>**DROPEFFECT \_ DÉPLACER**</dt> <dt>2</dt> </dl>                | La source de glissement doit supprimer les données. <br/>                                                                                     |
| <span id="DROPEFFECT_LINK"></span><span id="dropeffect_link"></span><dl> <dt>**DROPEFFECT \_ LIEN**</dt> <dt>4</dt> </dl>                | La source de glissement doit créer un lien vers les données d’origine.<br/>                                                                   |
| <span id="DROPEFFECT_SCROLL"></span><span id="dropeffect_scroll"></span><dl> <dt>**DROPEFFECT \_ SCROLL**</dt> <dt>0x80000000</dt> </dl> | Le défilement est sur le début ou se produit actuellement dans la cible. Cette valeur est utilisée en plus des autres valeurs.<br/> |



## <a name="remarks"></a>Notes

Votre application doit toujours masquer les valeurs de l’énumération **DROPEFFECT** pour garantir la compatibilité avec les futures implémentations. Actuellement, seules certaines positions dans une valeur **DROPEFFECT** ont une signification. À l’avenir, d’autres interprétations pour le service bits seront ajoutées. Les sources de glissement et les cibles de dépôt doivent masquer soigneusement ces valeurs avant la comparaison. Ils ne doivent jamais comparer un **DROPEFFECT** à une copie DROPEFFECT, par exemple, \_ en procédant comme suit :

``` syntax
if (dwDropEffect == DROPEFFECT_COPY)... 
```

Au lieu de cela, l’application doit toujours masquer la valeur ou les valeurs recherchées en utilisant l’une des techniques suivantes :

``` syntax
if (dwDropEffect & DROPEFFECT_COPY) == DROPEFFECT_COPY)...

if (dwDropEffect & DROPEFFECT_COPY)... 
```

Cela permet de définir de nouveaux effets de suppression, tout en préservant la compatibilité descendante avec le code existant.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                          |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>OleIdl. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**DoDragDrop**](/windows/desktop/api/Ole2/nf-ole2-dodragdrop)
</dt> <dt>

[**IDropSource**](/windows/desktop/api/OleIdl/nn-oleidl-idropsource)
</dt> <dt>

[**IDropTarget**](/windows/desktop/api/OleIdl/nn-oleidl-idroptarget)
</dt> </dl>

 

 





