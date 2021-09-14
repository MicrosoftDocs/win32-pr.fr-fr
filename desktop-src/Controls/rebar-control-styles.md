---
title: Styles de contrôle rebar (CommCtrl. h)
description: Les contrôles Rebar prennent en charge un grand nombre de styles de contrôle en plus des styles de fenêtre standard.
ms.assetid: 9690a4bd-51bd-4df9-8988-7da3ece7899f
topic_type:
- apiref
api_name:
- RBS_AUTOSIZE
- RBS_BANDBORDERS
- RBS_DBLCLKTOGGLE
- RBS_FIXEDORDER
- RBS_REGISTERDROP
- RBS_TOOLTIPS
- RBS_VARHEIGHT
- RBS_VERTICALGRIPPER
api_location:
- CommCtrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67b9f447df2cbf1bb2b956a7ec300d1f29280eef
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127117130"
---
# <a name="rebar-control-styles"></a>Styles de contrôle rebar

Les contrôles Rebar prennent en charge un grand nombre de styles de contrôle en plus des styles de fenêtre standard.



| Constante                                                                                                                                                                        | Description                                                                                                                                                                                                                                                                                                                                                 |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RBS_AUTOSIZE"></span><span id="rbs_autosize"></span><dl> <dt>**\_REdimensionnement automatique RBS**</dt> </dl>                      | [Version 4,71](common-control-versions.md). Le contrôle rebar change automatiquement la disposition des bandes lorsque la taille ou la position du contrôle change. Une notification de [ \_ redimensionnement automatique RBN](rbn-autosize.md) sera envoyée lorsque cela se produit.<br/>                                                                                              |
| <span id="RBS_BANDBORDERS"></span><span id="rbs_bandborders"></span><dl> <dt>**\_BANDBORDERS RBS**</dt> </dl>             | [Version 4,71](common-control-versions.md). Le contrôle rebar affiche des lignes étroites pour séparer les bandes adjacentes.<br/>                                                                                                                                                                                                                                 |
| <span id="RBS_DBLCLKTOGGLE"></span><span id="rbs_dblclktoggle"></span><dl> <dt>**\_DBLCLKTOGGLE RBS**</dt> </dl>          | [Version 4,71](common-control-versions.md). La bande rebar bascule son état agrandi ou réduit quand l’utilisateur double-clique sur la bande. Sans ce style, l’État agrandi ou réduit est activé ou désactivé lorsque l’utilisateur clique sur la bande.<br/>                                                                                          |
| <span id="RBS_FIXEDORDER"></span><span id="rbs_fixedorder"></span><dl> <dt>**\_FIXEDORDER RBS**</dt> </dl>                | [Version 4,70](common-control-versions.md). Le contrôle rebar affiche toujours les bandes dans le même ordre. Vous pouvez déplacer des bandes vers des lignes différentes, mais l’ordre des bandes est statique.<br/>                                                                                                                                                                      |
| <span id="RBS_REGISTERDROP"></span><span id="rbs_registerdrop"></span><dl> <dt>**\_REGISTERDROP RBS**</dt> </dl>          | [Version 4,71](common-control-versions.md). Le contrôle rebar génère des codes de notification [RBN \_ GETOBJECT](rbn-getobject.md) lorsqu’un objet est glissé sur une bande dans le contrôle. Pour recevoir les \_ notifications GETOBJECT RBN, initialisez OLE avec un appel à [**OleInitialize**](/windows/desktop/api/ole2/nf-ole2-oleinitialize) ou à [**CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize).<br/> |
| <span id="RBS_TOOLTIPS"></span><span id="rbs_tooltips"></span><dl> <dt>**\_info-bulles RBS**</dt> </dl>                      | [Version 4,71](common-control-versions.md). Pas encore pris en charge.<br/>                                                                                                                                                                                                                                                                                  |
| <span id="RBS_VARHEIGHT"></span><span id="rbs_varheight"></span><dl> <dt>**\_VARHEIGHT RBS**</dt> </dl>                   | [Version 4,71](common-control-versions.md). Le contrôle rebar affiche les bandes à la hauteur minimale requise, lorsque cela est possible. Sans ce style, le contrôle rebar affiche toutes les bandes à la même hauteur, en utilisant la hauteur de la bande visible la plus grande pour déterminer la hauteur des autres bandes.<br/>                                                   |
| <span id="RBS_VERTICALGRIPPER"></span><span id="rbs_verticalgripper"></span><dl> <dt>**\_VERTICALGRIPPER RBS**</dt> </dl> | [Version 4,71](common-control-versions.md). La poignée de dimensionnement est affichée verticalement et non horizontalement dans un contrôle rebar vertical. Ce style est ignoré pour les contrôles Rebar qui n’ont pas le style [**CCS \_ vert**](common-control-styles.md) .<br/>                                                                            |



## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------|---------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>CommCtrl. h</dt> </dl> |



 

