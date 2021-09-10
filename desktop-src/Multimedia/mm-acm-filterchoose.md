---
title: Message d’MM_ACM_FILTERCHOOSE (Msacm. h)
description: Le \_ \_ message FILTERCHOOSE ACM mm avertit une fonction de raccordement de boîte de dialogue acmFilterChoose avant d’ajouter un élément à l’une des trois zones de liste déroulante.
ms.assetid: f3c68240-a9aa-4771-96b9-1cb3bb5ea906
keywords:
- message MM_ACM_FILTERCHOOSE Windows Multimedia
topic_type:
- apiref
api_name:
- MM_ACM_FILTERCHOOSE
api_location:
- Msacm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1df28ad7f950b8ce995fd308622db8c429393cb8
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/10/2021
ms.locfileid: "124364035"
---
# <a name="mm_acm_filterchoose-message"></a>MM \_ \_ message FILTERCHOOSE ACM

Le **message \_ \_ FILTERCHOOSE ACM mm** avertit une fonction de raccordement de boîte de dialogue [**acmFilterChoose**](/windows/desktop/api/Msacm/nf-msacm-acmfilterchoose) avant d’ajouter un élément à l’une des trois zones de liste déroulante. Ce message permet à une application de personnaliser davantage les sélections disponibles via l’interface utilisateur.


```C++
        MM_ACM_FILTERCHOOSE
        wParam = (WPARAM) wDropDown
        lParam = (LONG) lCustom
      
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="wDropDown"></span><span id="wdropdown"></span><span id="WDROPDOWN"></span>*wDropDown*
</dt> <dd>

Zone de liste déroulante initialisée et opération de vérification ou d’ajout.



| Condition requise | Valeur |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_vérification personnalisée \_ FILTERCHOOSE    | Le paramètre *lParam* est un pointeur vers une structure [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) à ajouter à la zone de liste déroulante nom personnalisé.                                                                                                   |
| \_Ajouter un filtre FILTERCHOOSE \_       | Le paramètre *lParam* est un pointeur vers une mémoire tampon qui accepte une structure [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) à ajouter à la zone de liste déroulante de filtre. L’application doit copier la structure de filtre à ajouter à cette mémoire tampon. |
| \_vérification du filtre FILTERCHOOSE \_    | Le paramètre *lParam* est un pointeur vers une structure [**WAVEFILTER**](/windows/desktop/api/Mmreg/ns-mmreg-wavefilter) à ajouter à la zone de liste déroulante de filtre.                                                                                                        |
| FILTERCHOOSE \_ FILTERTAG \_ Add    | Le paramètre *lParam* est un pointeur vers une **valeur DWORD** qui accepte une balise de filtre audio Waveform à ajouter à la zone de liste déroulante balise de filtre.                                                                                        |
| FILTERCHOOSE \_ FILTERTAG \_ verify | Le paramètre *lParam* est une balise de filtre de forme d’onde audio à répertorier dans la zone de liste déroulante balise de filtre.                                                                                                                                 |



 

</dd> <dt>

<span id="lCustom"></span><span id="lcustom"></span><span id="LCUSTOM"></span>*lCustom*
</dt> <dd>

Valeur définie par la zone de liste spécifiée dans le paramètre **wParam** .

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne la **valeur true** si une application gère ce message ou **false** dans le cas contraire.

## <a name="remarks"></a>Remarques

Si l’application traite l' \_ \_ opération d’ajout de filtre FILTERCHOOSE, la taille de la mémoire tampon fournie dans *lParam* est déterminée à partir de la fonction [**acmMetrics**](/windows/desktop/api/Msacm/nf-msacm-acmmetrics) .

Si l’application traite une opération de vérification, l’application doit précéder la valeur de retour avec **SetWindowLong** (HWND, DWL \_ MSGRESULT, (long) **false**) pour empêcher la boîte de dialogue de répertorier cette sélection ou avec **SetWindowLong** (HWND, DWL \_ MSGRESULT, (long)**true**) pour permettre à la boîte de dialogue de répertorier cette sélection. En cas de traitement d’une opération d’ajout, l’application doit précéder le retour avec **SetWindowLong** (HWND, DWL \_ MSGRESULT, (long)**false**) pour indiquer qu’aucun ajout supplémentaire n’est nécessaire ou avec **SetWindowLong** (HWND, DWL \_ MSGRESULT, (long)**true**) si d’autres ajouts sont nécessaires.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                         |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Msacm. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Gestionnaire de compression audio](audio-compression-manager.md)
</dt> <dt>

[Messages de compression audio](audio-compression-messages.md)
</dt> </dl>

 

 





