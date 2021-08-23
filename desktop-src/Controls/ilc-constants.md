---
title: Indicateurs de création de la liste d’images (shlobj. h)
description: Jeu d’indicateurs de bits qui spécifie le type de liste d’images à créer. Ce paramètre peut être une combinaison des valeurs suivantes, mais il ne peut inclure qu’une seule des \_ valeurs de couleur ILC. Utilisé par ImageList \_ Create et IImageList2 Initialize.
ms.assetid: DFEB1934-DB7F-4151-97F9-DDB2BCCC782A
topic_type:
- apiref
api_name:
- ILC_MASK
- ILC_COLOR
- ILC_COLORDDB
- ILC_COLOR4
- ILC_COLOR8
- ILC_COLOR16
- ILC_COLOR24
- ILC_COLOR32
- ILC_PALETTE
- ILC_MIRROR
- ILC_PERITEMMIRROR
- ILC_ORIGINALSIZE
- ILC_HIGHQUALITYSCALE
api_location:
- Shlobj.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac1197604750e5da9248200b2dbcf37e53611d83842a401aafc3d2ded70c9179
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118958688"
---
# <a name="image-list-creation-flags"></a>Indicateurs de création de la liste d’images

Jeu d’indicateurs de bits qui spécifie le type de liste d’images à créer. Ce paramètre peut être une combinaison des valeurs suivantes, mais il ne peut inclure qu’une seule des \_ valeurs de couleur ILC. Utilisé par [**ImageList \_ Create**](/windows/desktop/api/Commctrl/nf-commctrl-imagelist_create) et [**IImageList2 :: Initialize**](/windows/desktop/api/Commoncontrols/nf-commoncontrols-iimagelist2-initialize).



| Constante/valeur                                                                                                                                                                                                                                     | Description                                                                                                                                                                                  |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ILC_MASK"></span><span id="ilc_mask"></span><dl> <dt>**ILC \_ Masquer**</dt> <dt>0x00000001</dt> </dl>                                     | Utilisez un masque. La liste d’images contient deux bitmaps, dont l’un est une bitmap monochrome utilisée comme masque. Si cette valeur n’est pas incluse, la liste d’images contient une seule bitmap.<br/>      |
| <span id="ILC_COLOR"></span><span id="ilc_color"></span><dl> <dt>**ILC \_ COULEUR**</dt> <dt>0x00000000</dt> </dl>                                  | Utilisez le comportement par défaut si aucun des autres \_ indicateurs ILC COLORx n’est spécifié. En règle générale, la valeur par défaut est ILC \_ color4, mais pour les anciens pilotes d’affichage, la valeur par défaut est ILC \_ COLORDDB.<br/> |
| <span id="ILC_COLORDDB"></span><span id="ilc_colorddb"></span><dl> <dt>**ILC \_ COLORDDB**</dt> <dt>0x000000FE</dt> </dl>                         | Utilisez une image bitmap dépendante de l’appareil.<br/>                                                                                                                                                    |
| <span id="ILC_COLOR4"></span><span id="ilc_color4"></span><dl> <dt>**ILC \_ COLOR4**</dt> <dt>0x00000004</dt> </dl>                               | Utilisez une section DIB (Device-Independent Bitmap) 4 bits (16 couleurs) comme bitmap de la liste d’images.<br/>                                                                                  |
| <span id="ILC_COLOR8"></span><span id="ilc_color8"></span><dl> <dt>**ILC \_ COLOR8**</dt> <dt>0x00000008</dt> </dl>                               | Utilisez une section DIB 8 bits. Les couleurs utilisées pour la table de couleurs sont les mêmes que celles de la palette de demi-teintes.<br/>                                                                        |
| <span id="ILC_COLOR16"></span><span id="ilc_color16"></span><dl> <dt>**ILC \_ COLOR16**</dt> <dt>0x00000010</dt> </dl>                            | Utilisez une section DIB 16 bits (32/64 bits).<br/>                                                                                                                                          |
| <span id="ILC_COLOR24"></span><span id="ilc_color24"></span><dl> <dt>**ILC \_ COLOR24**</dt> <dt>0x00000018</dt> </dl>                            | Utilisez une section DIB de 24 bits.<br/>                                                                                                                                                         |
| <span id="ILC_COLOR32"></span><span id="ilc_color32"></span><dl> <dt>**ILC \_ COLOR32**</dt> <dt>0x00000020</dt> </dl>                            | Utilisez une section DIB 32 bits.<br/>                                                                                                                                                         |
| <span id="ILC_PALETTE"></span><span id="ilc_palette"></span><dl> <dt>**ILC \_ PALETTE**</dt> <dt>0x00000800</dt> </dl>                            | Non implémenté.<br/>                                                                                                                                                                  |
| <span id="ILC_MIRROR"></span><span id="ilc_mirror"></span><dl> <dt>**ILC \_ MIROIR**</dt> <dt>0x00002000</dt> </dl>                               | Mettre en miroir les icônes contenues si le processus est mis en miroir<br/>                                                                                                                            |
| <span id="ILC_PERITEMMIRROR"></span><span id="ilc_peritemmirror"></span><dl> <dt>**ILC \_ PERITEMMIRROR**</dt> <dt>0x00008000</dt> </dl>          | Fait en sorte que le code de mise en miroir reflète chaque élément lors de l’insertion d’un ensemble d’images, par opposition à la bande entière.<br/>                                                                             |
| <span id="ILC_ORIGINALSIZE"></span><span id="ilc_originalsize"></span><dl> <dt>**ILC \_ ORIGINALSIZE**</dt> <dt>0x00010000</dt> </dl>             | **Windows Vista et versions ultérieures.** ImageList doit accepter des images Set plus petites et appliquer la taille d’origine en fonction de l’image ajoutée.<br/>                                                        |
| <span id="ILC_HIGHQUALITYSCALE"></span><span id="ilc_highqualityscale"></span><dl> <dt>**ILC \_ HIGHQUALITYSCALE**</dt> <dt>0x00020000</dt> </dl> | **Windows Vista et versions ultérieures.** Réservé.<br/>                                                                                                                                            |



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                      |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                |
| En-tête<br/>                   | <dl> <dt>Shlobj. h</dt> </dl> |



 

 





