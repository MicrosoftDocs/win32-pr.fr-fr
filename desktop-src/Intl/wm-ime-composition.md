---
description: Envoyé à une application lorsque l’IME modifie l’état de la composition à la suite d’une séquence de touches. Une fenêtre reçoit ce message par le biais de sa fonction WindowProc.
ms.assetid: 6de1c4c2-d910-487c-8b82-408cb6e02c44
title: Message WM_IME_COMPOSITION (winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8d795c1e270be978927e3b93743de5fece7021b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127223972"
---
# <a name="wm_ime_composition-message"></a>Message de composition du WM \_ IME \_

Envoyé à une application lorsque l’IME modifie l’état de la composition à la suite d’une séquence de touches. Une fenêtre reçoit ce message par le biais de sa fonction [*WindowProc*](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
LRESULT CALLBACK WindowProc(
  HWND  hwnd,     
  WM_IME_COMPOSITION,   
  WPARAM wParam,
  LPARAM lParam          
);
```



## <a name="parameters"></a>Paramètres

<dl> <dt>

*HWND* 
</dt> <dd>

Handle de fenêtre.

</dd> <dt>

*wParam* 
</dt> <dd>

Caractère DBCS représentant la dernière modification apportée à la chaîne de composition.

</dd> <dt>

*lParam* 
</dt> <dd>

Valeur spécifiant le mode de modification de la chaîne ou du caractère de composition. Ce paramètre peut être une ou plusieurs des valeurs suivantes. Pour plus d’informations sur ces valeurs, consultez [valeurs de chaîne de composition IME](ime-composition-string-values.md).

<dl><span id="GCS_COMPATTR"></span><span id="gcs_compattr"></span><dt>

**comfromateurs \_ gc**
</dt><span id="GCS_COMPCLAUSE"></span><span id="gcs_compclause"></span><dt>

**catalogues globaux \_ COMPCLAUSE**
</dt><span id="GCS_COMPREADSTR"></span><span id="gcs_compreadstr"></span><dt>

**catalogues globaux \_ COMPREADSTR**
</dt><span id="GCS_COMPREADATTR"></span><span id="gcs_compreadattr"></span><dt>

**catalogues globaux \_ COMPREADATTR**
</dt><span id="GCS_COMPREADCLAUSE"></span><span id="gcs_compreadclause"></span><dt>

**catalogues globaux \_ COMPREADCLAUSE**
</dt><span id="GCS_COMPSTR"></span><span id="gcs_compstr"></span><dt>

**catalogues globaux \_ COMPSTR**
</dt><span id="GCS_CURSORPOS"></span><span id="gcs_cursorpos"></span><dt>

**catalogues globaux \_ CURSORPOS**
</dt><span id="GCS_DELTASTART"></span><span id="gcs_deltastart"></span><dt>

**catalogues globaux \_ DELTASTART**
</dt><span id="GCS_RESULTCLAUSE"></span><span id="gcs_resultclause"></span><dt>

**catalogues globaux \_ RESULTCLAUSE**
</dt><span id="GCS_RESULTREADCLAUSE"></span><span id="gcs_resultreadclause"></span><dt>

**catalogues globaux \_ RESULTREADCLAUSE**
</dt><span id="GCS_RESULTREADSTR"></span><span id="gcs_resultreadstr"></span><dt>

**catalogues globaux \_ RESULTREADSTR**
</dt><span id="GCS_RESULTSTR"></span><span id="gcs_resultstr"></span><dt>

**GC \_ RESULTSTR**
</dt> </dl>

Le paramètre *lParam* peut également avoir une ou plusieurs des valeurs suivantes.



| Valeur                                                                                                                                                            | Signification                                                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CS_INSERTCHAR"></span><span id="cs_insertchar"></span><dl> <dt>**\_INSERTCHAR CS**</dt> </dl>    | Insérez le caractère de composition *wParam* au niveau du point d’insertion actuel. Une application doit afficher le caractère de composition s’il traite ce message.<br/>                                                                                                                                                                                                                                |
| <span id="CS_NOMOVECARET"></span><span id="cs_nomovecaret"></span><dl> <dt>**\_NOMOVECARET CS**</dt> </dl> | Ne pas déplacer l’emplacement du signe insertion à la suite du traitement du message. Par exemple, si un IME spécifie une combinaison de CS \_ INSERTCHAR et CS \_ NOMOVECARET, l’application doit insérer le caractère spécifié à la position actuelle du point d’insertion, mais ne doit pas déplacer le signe insertion à la position suivante. Un message de \_ composition de l’IME WM ultérieur \_ avec GC \_ RESULTSTR remplace ce caractère.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valeur de retour

Ce message n’a pas de valeur de retour.

## <a name="remarks"></a>Notes

Une application doit traiter ce message si elle affiche lui-même des caractères de composition. Dans le cas contraire, il doit envoyer le message à la fenêtre IME.

Si l’application a créé une fenêtre IME, elle doit transmettre ce message à cette fenêtre. La fonction [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)  traite ce message en le passant à la fenêtre IME par défaut. La fenêtre IME traite ce message en mettant à jour son apparence en fonction de l’indicateur de modification spécifié. Une application peut appeler [**ImmGetCompositionString**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa) pour récupérer l’état de la nouvelle composition.

Si aucune des valeurs de catalogues globaux \_ n’est définie, le message indique que la composition actuelle a été annulée et que les applications qui dessinent la chaîne de composition doivent supprimer la chaîne.

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                                                                                                                                |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                                                                                                                      |
| En-tête<br/>                   | <dl> <dt>Winuser. h (inclure Windows. h);</dt> <dt>Imm. h (inclure Windows. h)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Gestionnaire de méthode d’entrée](input-method-manager.md)
</dt> <dt>

[Messages du gestionnaire de méthode d’entrée](input-method-manager-messages.md)
</dt> <dt>

[**ImmGetCompositionString**](/windows/desktop/api/Imm/nf-imm-immgetcompositionstringa)
</dt> </dl>

 

 
