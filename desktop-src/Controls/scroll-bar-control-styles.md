---
title: Styles de contrôle de barre de défilement (winuser. h)
description: Pour créer un contrôle de barre de défilement à l’aide de la fonction CreateWindow ou CreateWindowEx, spécifiez la classe SCROLLBAR, les constantes de style de fenêtre appropriées et une combinaison des styles de contrôle de barre de défilement suivants.
ms.assetid: 07195a95-eff8-4a47-926a-9d503fa7b299
topic_type:
- apiref
api_name:
- SBS_BOTTOMALIGN
- SBS_HORZ
- SBS_LEFTALIGN
- SBS_RIGHTALIGN
- SBS_SIZEBOX
- SBS_SIZEBOXBOTTOMRIGHTALIGN
- SBS_SIZEBOXTOPLEFTALIGN
- SBS_SIZEGRIP
- SBS_TOPALIGN
- SBS_VERT
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cc5de721fd4cc44867fca0dbe1b35dcaf58c6dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 03/22/2021
ms.locfileid: "106528508"
---
# <a name="scroll-bar-control-styles"></a>Styles de contrôle de barre de défilement

Pour créer un contrôle de barre de défilement à l’aide de la fonction [**CreateWindow**](/windows/desktop/api/winuser/nf-winuser-createwindowa) ou [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , spécifiez la classe ScrollBar, les constantes de style de fenêtre appropriées et une combinaison des styles de contrôle de barre de défilement suivants. Certains styles créent un contrôle de barre de défilement qui utilise une largeur ou une hauteur par défaut. Toutefois, vous devez toujours spécifier les coordonnées x et y et les autres dimensions de la barre de défilement lorsque vous appelez **CreateWindow** ou **CreateWindowEx**.



| Constante                                                                                                                                                                                                | Description                                                                                                                                                                                                                                                                                                                                |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SBS_BOTTOMALIGN"></span><span id="sbs_bottomalign"></span><dl> <dt>**\_BOTTOMALIGN SBS**</dt> </dl>                                     | Aligne le bord inférieur de la barre de défilement avec le bord inférieur du rectangle défini par les paramètres *x*, *y*, *nWidth* et *nHeight* de la fonction [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) . La barre de défilement a la hauteur par défaut pour les barres de défilement système. Utilisez ce style avec le style de ligne \_ Horiz SBS.<br/>                      |
| <span id="SBS_HORZ"></span><span id="sbs_horz"></span><dl> <dt>**\_Horiz SBS**</dt> </dl>                                                          | Désigne une barre de défilement horizontale. Si ni le \_ style SBS BOTTOMALIGN ni le style d’alignement de la \_ liste SBS ne sont spécifiés, la barre de défilement a la hauteur, la largeur et la position spécifiées par les paramètres *x*, *y*, *nWidth* et *nHeight* de [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).<br/>                                                      |
| <span id="SBS_LEFTALIGN"></span><span id="sbs_leftalign"></span><dl> <dt>**\_LEFTALIGN SBS**</dt> </dl>                                           | Aligne le bord gauche de la barre de défilement sur le bord gauche du rectangle défini par les paramètres *x*, *y*, *nWidth* et *nHeight* de [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa). La barre de défilement a la largeur par défaut pour les barres de défilement système. Utilisez ce style avec le \_ style de bascule SBS.<br/>                                    |
| <span id="SBS_RIGHTALIGN"></span><span id="sbs_rightalign"></span><dl> <dt>**\_RIGHTALIGN SBS**</dt> </dl>                                        | Aligne le bord droit de la barre de défilement sur le bord droit du rectangle défini par les paramètres *x*, *y*, *nWidth* et *nHeight* de [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa). La barre de défilement a la largeur par défaut pour les barres de défilement système. Utilisez ce style avec le \_ style de bascule SBS.<br/>                                  |
| <span id="SBS_SIZEBOX"></span><span id="sbs_sizebox"></span><dl> <dt>**\_SIZEBOX SBS**</dt> </dl>                                                 | Désigne une zone de taille. Si vous ne spécifiez ni le \_ style SBS SIZEBOXBOTTOMRIGHTALIGN \_ , ni le style SIZEBOXTOPLEFTALIGN SBS, la zone taille a la hauteur, la largeur et la position spécifiées par les paramètres *x*, *y*, *nWidth* et *nHeight* de [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa). <br/>                                          |
| <span id="SBS_SIZEBOXBOTTOMRIGHTALIGN"></span><span id="sbs_sizeboxbottomrightalign"></span><dl> <dt>**\_SIZEBOXBOTTOMRIGHTALIGN SBS**</dt> </dl> | Aligne le coin inférieur droit de la zone taille avec le coin inférieur droit du rectangle spécifié par les paramètres *x*, *y*, *nWidth* et *nHeight* de [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa). La zone Taille contient la taille par défaut des zones taille du système. Utilisez ce style avec les \_ styles SBS SIZEBOX ou SBS \_ SIZEGRIP.<br/> |
| <span id="SBS_SIZEBOXTOPLEFTALIGN"></span><span id="sbs_sizeboxtopleftalign"></span><dl> <dt>**\_SIZEBOXTOPLEFTALIGN SBS**</dt> </dl>             | Aligne l’angle supérieur gauche de la zone taille avec l’angle supérieur gauche du rectangle spécifié par les paramètres *x*, *y*, *nWidth* et *nHeight* de [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa). La zone Taille contient la taille par défaut des zones taille du système. Utilisez ce style avec les \_ styles SBS SIZEBOX ou SBS \_ SIZEGRIP.<br/>   |
| <span id="SBS_SIZEGRIP"></span><span id="sbs_sizegrip"></span><dl> <dt>**\_SIZEGRIP SBS**</dt> </dl>                                              | Identique à SBS \_ SIZEBOX, mais avec un bord en relief. <br/>                                                                                                                                                                                                                                                                                  |
| <span id="SBS_TOPALIGN"></span><span id="sbs_topalign"></span><dl> <dt>**alignement de la \_ réalignement SBS**</dt> </dl>                                              | Aligne le bord supérieur de la barre de défilement sur le bord supérieur du rectangle défini par les paramètres *x*, *y*, *nWidth* et *nHeight* de [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa). La barre de défilement a la hauteur par défaut pour les barres de défilement système. Utilisez ce style avec le style de ligne \_ Horiz SBS.<br/>                                     |
| <span id="SBS_VERT"></span><span id="sbs_vert"></span><dl> <dt>**bascule vers le SBS \_**</dt> </dl>                                                          | Désigne une barre de défilement verticale. Si vous ne spécifiez ni le \_ style SBS RIGHTALIGN, ni le \_ style LEFTALIGN SBS, la barre de défilement a la hauteur, la largeur et la position spécifiées par les paramètres *x*, *y*, *nWidth* et *nHeight* de [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa).<br/>                                                     |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------|--------------------------------------------------------------------------------------|
| En-tête<br/> | <dl> <dt>Winuser. h</dt> </dl> |



 

