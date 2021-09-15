---
title: Codes d’erreur DirectComposition (Dcomp. h)
description: Cette section décrit les codes d’erreur spécifiques à DirectComposition.
ms.assetid: 8DFBFC34-DBD0-4731-8305-B33E90C96C54
topic_type:
- apiref
api_name:
- DCOMPOSITION_ERROR_ACCESS_DENIED
- DCOMPOSITION_ERROR_SURFACE_BEING_RENDERED
- DCOMPOSITION_ERROR_SURFACE_NOT_BEING_RENDERED
- DCOMPOSITION_ERROR_WINDOW_ALREADY_COMPOSED
api_location:
- Dcomp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96a76a7527bacf8caa756a0fad75ca70f4bf9a77
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127524449"
---
# <a name="directcomposition-error-codes"></a>Codes d’erreur DirectComposition

Si une erreur se produit, Microsoft DirectComposition retourne un code en tant que valeur **HRESULT** . Cette section décrit les codes d’erreur spécifiques à DirectComposition. Pour obtenir la liste des codes d’erreur COM (Component Object Model) généraux, consultez [codes d’erreur com](/windows/desktop/com/com-error-codes).

<dl> <dt>

<span id="DCOMPOSITION_ERROR_ACCESS_DENIED"></span><span id="dcomposition_error_access_denied"></span>**\_ \_ accès à l’erreur DCOMPOSITION \_ refusé**
</dt> <dd> <dl> <dt>


</dt> <dt>



Le handle de fenêtre qui a été spécifié dans un appel à la méthode [**IDCompositionDevice :: CreateTargetForHwnd**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtargetforhwnd) appartient à un processus différent de celui qui a créé l’objet appareil.


</dt> </dl> </dd> <dt>

<span id="DCOMPOSITION_ERROR_SURFACE_BEING_RENDERED"></span><span id="dcomposition_error_surface_being_rendered"></span>**\_surface d’erreur DCOMPOSITION \_ \_ \_ rendue**
</dt> <dd> <dl> <dt>


</dt> <dt>



La surface était déjà rendue lorsque l’application a appelé la méthode [**IDCompositionSurface :: BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw), [**IDCompositionSurface :: SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw)ou [**IDCompositionSurface :: ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) . Pour plus d'informations, consultez la section Notes.


</dt> </dl> </dd> <dt>

<span id="DCOMPOSITION_ERROR_SURFACE_NOT_BEING_RENDERED"></span><span id="dcomposition_error_surface_not_being_rendered"></span>**la \_ surface d’erreur DCOMPOSITION \_ \_ n' \_ est pas \_ rendue**
</dt> <dd> <dl> <dt>


</dt> <dt>



L’application a appelé la méthode [**IDCompositionSurface :: SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw), [**IDCompositionSurface :: ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)ou [**IDCompositionSurface :: EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) pour une surface qui n’est pas rendue. Pour plus d'informations, consultez la section Notes.


</dt> </dl> </dd> <dt>

<span id="DCOMPOSITION_ERROR_WINDOW_ALREADY_COMPOSED"></span><span id="dcomposition_error_window_already_composed"></span>**\_fenêtre d’erreur DCOMPOSITION \_ \_ déjà \_ composée**
</dt> <dd> <dl> <dt>


</dt> <dt>



La méthode [**IDCompositionDevice :: CreateTargetForHwnd**](/windows/win32/api/dcomp/nf-dcomp-idcompositiondevice-createtargetforhwnd) a été appelée avec *HWND* et les paramètres de niveau *supérieur* pour lesquels une arborescence d’éléments visuels existe déjà.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Remarques

Si un appel à [**IDCompositionSurface :: BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw) était l’action la plus récente :



| Appel de cette méthode :                                    | Retourne cette valeur :                               |
|---------------------------------------------------------|---------------------------------------------------|
| [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | **\_surface d’erreur DCOMPOSITION \_ \_ \_ rendue** |
| [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | \_OK                                             |
| [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | \_OK                                             |
| [**ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | **\_surface d’erreur DCOMPOSITION \_ \_ \_ rendue** |



 

Si un appel à [**IDCompositionSurface :: SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) était l’action la plus récente :



| Appel de cette méthode :                                    | Retourne cette valeur :                               |
|---------------------------------------------------------|---------------------------------------------------|
| [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | **\_surface d’erreur DCOMPOSITION \_ \_ \_ rendue** |
| [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | \_OK                                             |
| [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | **\_surface d’erreur DCOMPOSITION \_ \_ \_ rendue** |
| [**ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | \_OK                                             |



 

Si un appel à [**IDCompositionSurface :: ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw) était l’action la plus récente :



| Appel de cette méthode :                                    | Retourne cette valeur :                                |
|---------------------------------------------------------|----------------------------------------------------|
| [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | **\_surface d’erreur DCOMPOSITION \_ \_ \_ rendue**  |
| [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | \_OK                                              |
| [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | \_OK                                              |
| [**ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | **\_surface d’erreur DCOMPOSITION \_ \_ \_ rendue.** |



 

Si un appel à [**IDCompositionSurface :: EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw) était l’action la plus récente :



| Appel de cette méthode :                                    | Retourne cette valeur :                                     |
|---------------------------------------------------------|---------------------------------------------------------|
| [**BeginDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-begindraw)     | \_OK                                                   |
| [**EndDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-enddraw)         | **la \_ surface d’erreur DCOMPOSITION \_ \_ n' \_ est pas \_ rendue.** |
| [**SuspendDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-suspenddraw) | **la \_ surface d’erreur DCOMPOSITION \_ \_ n' \_ est pas \_ rendue.** |
| [**ResumeDraw**](/windows/win32/api/dcomp/nf-dcomp-idcompositionsurface-resumedraw)   | **la \_ surface d’erreur DCOMPOSITION \_ \_ n' \_ est pas \_ rendue.** |



 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 8 \[ applications de bureau uniquement\]<br/>                                         |
| Serveur minimal pris en charge<br/> | Windows Server 2012 \[ applications de bureau uniquement\]<br/>                               |
| En-tête<br/>                   | <dl> <dt>Dcomp. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Référence DirectComposition](reference.md)
</dt> </dl>

 

