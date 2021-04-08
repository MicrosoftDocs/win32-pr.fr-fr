---
title: Message EM_GETEDITSTYLEEX (RichEdit. h)
description: Récupère les indicateurs de style de modification étendus actuels.
ms.assetid: 3E81F7BB-404D-4465-982A-3CF6FD9359DA
keywords:
- EM_GETEDITSTYLEEX les contrôles de message Windows
topic_type:
- apiref
api_name:
- EM_GETEDITSTYLEEX
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb4077abaedd0c5ec720603d6b23e77950fd5307
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843685"
---
# <a name="em_geteditstyleex-message"></a>\_Message GETEDITSTYLEEX em

Récupère les indicateurs de style de modification étendus actuels.


```C++
#define EM_GETEDITSTYLEEX       (WM_USER + 276)
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*wParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> <dt>

*lParam* 
</dt> <dd>

Non utilisé ; doit être égal à zéro.

</dd> </dl>

## <a name="return-value"></a>Valeur retournée

Retourne les indicateurs de style de modification étendus, qui peuvent inclure une ou plusieurs des valeurs suivantes.



| Code de retour                                                                                                | Description                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**SES \_ ex \_ HANDLEFRIENDLYURL**</dt> </dl>  | Affichez des liens de nom convivial avec la même couleur de texte et le soulignement que les liens automatiques, à condition que la mise en forme temporaire n’utilise pas ou utilise la couleur automatique de texte (valeur par défaut : 0).<br/>                                                                       |
| <dl> <dt>**SES \_ par \_ multipoint**</dt> </dl>         | Activez la prise en charge tactile en Rich Edit. Cela comprend la sélection, le positionnement du signe insertion et l’appel du menu contextuel. Lorsque cet indicateur n’est pas défini, la fonction tactile est émulée par les commandes de la souris, qui ne prennent pas en compte les spécificités en mode tactile (valeur par défaut : 0). <br/>      |
| <dl> <dt>**SES \_ ex \_ NOACETATESELECTION**</dt> </dl> | Affichez le texte sélectionné à l’aide de la sélection Windows classique texte et couleurs d’arrière-plan au lieu de couleur d’acétate d’arrière-plan (par défaut : 0). <br/>                                                                                                               |
| <dl> <dt>**SES \_ ex \_ maths**</dt> </dl>             | Désactivez l’insertion de zones mathématiques (valeur par défaut : 1). Pour activer la modification et l’affichage des mathématiques, envoyez le message [**em \_ SETEDITSTYLEEX**](em-seteditstyleex.md) avec *wParam* défini sur 0, et *lParam* défini sur **ses \_ ex \_ maths**. <br/>                              |
| <dl> <dt>**SES \_ ex \_ table**</dt> </dl>            | Désactive l’insertion de tables. Le message [**em \_ INSERTTABLE**](em-inserttable.md) retourne **E \_ Fail** et les tables RTF sont ignorées (valeur par défaut : 0). <br/>                                                                                                  |
| <dl> <dt>**SES \_ ex \_ USESINGLELINE**</dt> </dl>      | Permet à un contrôle multiligne d’agir comme un contrôle sur une seule ligne, avec la possibilité de faire défiler verticalement lorsque la hauteur d’une seule ligne est supérieure à la hauteur de la fenêtre (valeur par défaut : 0). <br/>                                                                   |
| <dl> <dt>**\_HIDETEMPFORMAT ses**</dt> </dl>         | Masquer la mise en forme temporaire qui est créée quand [**ITextFont. Reset**](/windows/desktop/api/Tom/nf-tom-itextfont-reset) est appelé avec **tomApplyTmp**. Par exemple, une telle mise en forme est utilisée par les vérificateurs d’orthographe pour afficher un soulignement ondulé sous des mots éventuellement mal orthographiés.<br/> |
| <dl> <dt>**SES \_ ex \_ USEMOUSEWPARAM**</dt> </dl>     | Utilisez *wParam* lors du traitement du message [**WM \_ MOUSEMOVE**](/windows/desktop/inputdev/wm-mousemove) et n’appelez pas [**GetAsyncKeyState**](/windows/desktop/api/winuser/nf-winuser-getasynckeystate).<br/>                                                                                              |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de \[ Bureau Windows 8 uniquement\]<br/>                                            |
| Serveur minimal pris en charge<br/> | Applications de bureau Windows Server 2012 \[ uniquement\]<br/>                                  |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETEDITSTYLEEX em**](em-seteditstyleex.md)
</dt> </dl>

 

