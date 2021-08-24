---
title: Message d’MM_ACM_FORMATCHOOSE (Msacm. h)
description: Le \_ message mm ACM \_ FORMATCHOOSE avertit une fonction de raccordement de boîte de dialogue acmFormatChoose avant d’ajouter un élément à l’une des trois zones de liste déroulante.
ms.assetid: f77e41c6-14e9-45c0-971e-4d6325145f1c
keywords:
- message MM_ACM_FORMATCHOOSE Windows Multimedia
topic_type:
- apiref
api_name:
- MM_ACM_FORMATCHOOSE
api_location:
- Msacm.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cceaa67bc0ce4ee922b48d1cff20eb2bf6414f93506dcc70ccd6e0e912211544
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119782959"
---
# <a name="mm_acm_formatchoose-message"></a>MM \_ \_ message FORMATCHOOSE ACM

Le message **mm \_ ACM \_ FORMATCHOOSE** avertit une fonction de raccordement de boîte de dialogue [**acmFormatChoose**](/windows/desktop/api/Msacm/nf-msacm-acmformatchoose) avant d’ajouter un élément à l’une des trois zones de liste déroulante. Ce message permet à une application de personnaliser davantage les sélections disponibles via l’interface utilisateur.


```C++
MM_ACM_FORMATCHOOSE 
wParam = (WPARAM) wDropDown 
lParam = (LONG) lCustom 
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

<span id="wDropDown"></span><span id="wdropdown"></span><span id="WDROPDOWN"></span>*wDropDown*
</dt> <dd>

Zone de liste déroulante initialisée et opération de vérification ou d’ajout.



| Condition requise | Valeur |
|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| \_vérification personnalisée \_ FORMATCHOOSE    | Le paramètre *lParam* est un pointeur vers une structure [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) à ajouter à la zone de liste déroulante nom personnalisé.                                                                                                   |
| FORMATCHOOSE \_ Ajouter au format \_       | Le paramètre *lParam* est un pointeur vers une mémoire tampon qui accepte une structure [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) à ajouter à la zone de liste déroulante format. L’application doit copier la structure de format à ajouter à cette mémoire tampon. |
| \_vérification du format de FORMATCHOOSE \_    | Le paramètre *lParam* est un pointeur vers une structure [**WAVEFORMATEX**](/windows/win32/api/mmeapi/ns-mmeapi-waveformatex) à ajouter à la zone de liste déroulante format.                                                                                                        |
| FORMATCHOOSE \_ FORMATTAG \_ Add    | Le paramètre *lParam* est un pointeur vers une variable qui accepte une balise de format audio Waveform à ajouter à la zone de liste déroulante balise de mise en forme.                                                                                             |
| FORMATCHOOSE \_ FORMATTAG \_ verify | Le paramètre *lParam* est une balise de format Waveform Audio à répertorier dans la zone de liste déroulante format de balise.                                                                                                                                     |



 

</dd> <dt>

<span id="lCustom"></span><span id="lcustom"></span><span id="LCUSTOM"></span>*lCustom*
</dt> <dd>

Valeur définie par la zone de liste spécifiée dans le paramètre **wParam** .

</dd> </dl>

## <a name="return-value"></a>Valeur renvoyée

Retourne la **valeur true** si une application gère ce message ou **false** dans le cas contraire.

## <a name="remarks"></a>Remarques

Si l’application traite l' \_ opération Add au format FILTERCHOOSE \_ , la taille de la mémoire tampon fournie dans *lParam* est déterminée à partir de la fonction [**acmMetrics**](/windows/desktop/api/Msacm/nf-msacm-acmmetrics) .

Si votre application traite une opération de vérification, elle peut empêcher la boîte de dialogue de répertorier cette sélection en appelant la fonction **SetWindowLong** avec *NINDEX* défini sur DWL \_ MSGRESULT et *lNewLong* défini sur **false** (cast en type de données **long** ). Pour autoriser la boîte de dialogue à répertorier cette sélection, appelez cette fonction avec *lNewLong* défini sur **true**.

Si votre application traite une opération d’ajout, elle peut indiquer qu’aucun ajout supplémentaire n’est requis en appelant la fonction **SetWindowLong** avec *NINDEX* défini sur DWL \_ MSGRESULT et *lNewLong* défini sur **false** (cast en type de données **long** ). Pour indiquer que des ajouts supplémentaires sont nécessaires, appelez cette fonction avec *lNewLong* défini sur **true**.

## <a name="requirements"></a>Configuration requise



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

 

