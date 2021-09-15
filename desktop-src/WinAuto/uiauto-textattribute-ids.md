---
title: Identificateurs d’attribut de texte (UIAutomationClient. h)
description: Cette rubrique décrit les constantes nommées utilisées pour identifier les attributs de texte d’une plage de texte Microsoft UI Automation.
ms.assetid: 67d86817-6a3f-4047-88d9-34f33f52a563
topic_type:
- apiref
api_name:
- UIA_AfterParagraphSpacingAttributeId
- UIA_AnimationStyleAttributeId
- UIA_AnnotationObjectsAttributeId
- UIA_AnnotationTypesAttributeId
- UIA_BackgroundColorAttributeId
- UIA_BeforeParagraphSpacingAttributeId
- UIA_BulletStyleAttributeId
- UIA_CapStyleAttributeId
- UIA_CaretBidiModeAttributeId
- UIA_CaretPositionAttributeId
- UIA_CultureAttributeId
- UIA_FontNameAttributeId
- UIA_FontSizeAttributeId
- UIA_FontWeightAttributeId
- UIA_ForegroundColorAttributeId
- UIA_HorizontalTextAlignmentAttributeId
- UIA_IndentationFirstLineAttributeId
- UIA_IndentationLeadingAttributeId
- UIA_IndentationTrailingAttributeId
- UIA_IsActiveAttributeId
- UIA_IsHiddenAttributeId
- UIA_IsItalicAttributeId
- UIA_IsReadOnlyAttributeId
- UIA_IsSubscriptAttributeId
- UIA_IsSuperscriptAttributeId
- UIA_LineSpacingAttributeId
- UIA_LinkAttributeId
- UIA_MarginBottomAttributeId
- UIA_MarginLeadingAttributeId
- UIA_MarginTopAttributeId
- UIA_MarginTrailingAttributeId
- UIA_OutlineStylesAttributeId
- UIA_OverlineColorAttributeId
- UIA_OverlineStyleAttributeId
- UIA_SelectionActiveEndAttributeId
- UIA_StrikethroughColorAttributeId
- UIA_StrikethroughStyleAttributeId
- UIA_StyleIdAttributeId
- UIA_StyleNameAttributeId
- UIA_TabsAttributeId
- UIA_TextFlowDirectionsAttributeId
- UIA_UnderlineColorAttributeId
- UIA_UnderlineStyleAttributeId
api_location:
- UIAutomationClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e84ba97b387097233b7a838fbe192585b9676b6
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127403974"
---
# <a name="text-attribute-identifiers"></a>Identificateurs d’attribut de texte

Cette rubrique décrit les constantes nommées utilisées pour identifier les attributs de texte d’une plage de texte Microsoft UI Automation. Ces constantes sont utilisées avec les méthodes suivantes :

-   [**ITextRangeProvider::FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute)
-   [**ITextRangeProvider :: GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue)
-   [**IUIAutomationTextRange::FindAttribute**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findattribute)
-   [**IUIAutomationTextRange :: GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue)




| Constante/valeur | Description | 
|----------------|-------------|
| <span id="UIA_AfterParagraphSpacingAttributeId"></span><span id="uia_afterparagraphspacingattributeid"></span><span id="UIA_AFTERPARAGRAPHSPACINGATTRIBUTEID"></span><dl><dt><strong>UIA_AfterParagraphSpacingAttributeId</strong></dt><dt>40042</dt></dl> | Identifie l’attribut de texte <strong>AfterParagraphSpacing</strong> , qui spécifie la taille de l’espacement après le paragraphe.<br /> Type Variant : <strong>VT_R8</strong><br /> Valeur par défaut : 0<br /> | 
| <span id="UIA_AnimationStyleAttributeId"></span><span id="uia_animationstyleattributeid"></span><span id="UIA_ANIMATIONSTYLEATTRIBUTEID"></span><dl><dt><strong>UIA_AnimationStyleAttributeId</strong></dt><dt>40000</dt></dl> | Identifie l’attribut de texte <strong>AnimationStyle</strong> , qui spécifie le type d’animation appliqué au texte. Cet attribut est spécifié en tant que valeur du type énuméré <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-animationstyle"><strong>AnimationStyle</strong></a> . <br /> Type Variant : <strong>VT_I4</strong><br /> Valeur par défaut : <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-animationstyle"> <strong>AnimationStyle_None</strong></a><br /> | 
| <span id="UIA_AnnotationObjectsAttributeId"></span><span id="uia_annotationobjectsattributeid"></span><span id="UIA_ANNOTATIONOBJECTSATTRIBUTEID"></span><dl><dt><strong>UIA_AnnotationObjectsAttributeId</strong></dt><dt>40032</dt></dl> | Identifie l’attribut de texte <strong>AnnotationObjects</strong> , qui gère un tableau d’interfaces <a href="/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelement2"><strong>IUIAutomationElement2</strong></a> , un pour chaque élément de la plage de texte actuelle qui implémente le modèle de contrôle d' <a href="uiauto-implementingannotation.md">annotation</a> . Chaque élément peut également implémenter d’autres modèles de contrôle en fonction des besoins pour décrire l’annotation. Par exemple, une annotation qui est un commentaire prendrait également en charge le modèle de contrôle <a href="uiauto-implementingtextandtextrange.md">Text</a> . Pris en charge à partir de Windows 8.<br /> Type Variant : <strong>VT_UNKNOWN</strong><br /> Valeur par défaut : tableau vide <br /> | 
| <span id="UIA_AnnotationTypesAttributeId"></span><span id="uia_annotationtypesattributeid"></span><span id="UIA_ANNOTATIONTYPESATTRIBUTEID"></span><dl><dt><strong>UIA_AnnotationTypesAttributeId</strong></dt><dt>40031</dt></dl> | Identifie l’attribut de texte <strong>AnnotationTypes</strong> , qui gère une liste d’identificateurs de type d’annotation pour une plage de texte. Pour obtenir la liste des valeurs possibles, consultez <a href="uiauto-annotation-type-identifiers.md"><strong>identificateurs de type d’annotation</strong></a>. Pris en charge à partir de Windows 8.<br /> Type Variant : <strong>VT_ARRAY</strong> | <strong>VT_I4</strong><br /> Valeur par défaut : tableau vide <br /> | 
| <span id="UIA_BackgroundColorAttributeId"></span><span id="uia_backgroundcolorattributeid"></span><span id="UIA_BACKGROUNDCOLORATTRIBUTEID"></span><dl><dt><strong>UIA_BackgroundColorAttributeId</strong></dt><dt>40001</dt></dl> | Identifie l’attribut de texte <strong>backgroundColor</strong> , qui spécifie la couleur d’arrière-plan du texte. Cet attribut est spécifié en tant que <a href="/windows/win32/gdi/colorref">COLORREF</a>; valeur 32 bits utilisée pour spécifier une couleur RVB ou RVBA. <br /> Type Variant : <strong>VT_I4</strong><br /> Valeur par défaut : 0 <br /> | 
| <span id="UIA_BeforeParagraphSpacingAttributeId"></span><span id="uia_beforeparagraphspacingattributeid"></span><span id="UIA_BEFOREPARAGRAPHSPACINGATTRIBUTEID"></span><dl><dt><strong>UIA_BeforeParagraphSpacingAttributeId</strong></dt><dt>40041</dt></dl> | Identifie l’attribut de texte <strong>BeforeParagraphSpacing</strong> , qui spécifie la taille de l’espacement avant le paragraphe.<br /> Type Variant : <strong>VT_R8</strong><br /> Valeur par défaut : 0<br /> | 
| <span id="UIA_BulletStyleAttributeId"></span><span id="uia_bulletstyleattributeid"></span><span id="UIA_BULLETSTYLEATTRIBUTEID"></span><dl><dt><strong>UIA_BulletStyleAttributeId</strong></dt><dt>40002</dt></dl> | Identifie l’attribut de texte <strong>BulletStyle</strong> , qui spécifie le style de puces utilisé dans la plage de texte. Cet attribut est spécifié en tant que valeur du type énuméré <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-bulletstyle"><strong>BulletStyle</strong></a> .<br /> Type Variant : <strong>VT_I4</strong><br /> Valeur par défaut : <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-bulletstyle"> <strong>BulletStyle_None</strong></a><br /> | 
| <span id="UIA_CapStyleAttributeId"></span><span id="uia_capstyleattributeid"></span><span id="UIA_CAPSTYLEATTRIBUTEID"></span><dl><dt><strong>UIA_CapStyleAttributeId</strong></dt><dt>40003</dt></dl> | Identifie l’attribut de texte <strong>CapStyle</strong> , qui spécifie le style de mise en majuscules du texte. Cet attribut est spécifié en tant que valeur du type énuméré <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-capstyle"><strong>CapStyle</strong></a> . <br /> Type Variant : <strong>VT_I4</strong><br /> Valeur par défaut : <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-capstyle"> <strong>CapStyle_None</strong></a><br /> | 
| <span id="UIA_CaretBidiModeAttributeId"></span><span id="uia_caretbidimodeattributeid"></span><span id="UIA_CARETBIDIMODEATTRIBUTEID"></span><dl><dt><strong>UIA_CaretBidiModeAttributeId</strong></dt><dt>40039</dt></dl> | Identifie l’attribut de texte <strong>CaretBidiMode</strong> , qui indique le sens du déroulement du texte dans la plage de texte. Cet attribut est spécifié en tant que valeur du type énuméré <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-caretbidimode"><strong>CaretBidiMode</strong></a> . Pris en charge à partir de Windows 8.<br /> Type Variant : <strong>VT_I4</strong><br /> Valeur par défaut : <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-caretbidimode"> <strong>CaretBidiMode_LTR</strong></a><br /> | 
| <span id="UIA_CaretPositionAttributeId"></span><span id="uia_caretpositionattributeid"></span><span id="UIA_CARETPOSITIONATTRIBUTEID"></span><dl><dt><strong>UIA_CaretPositionAttributeId</strong></dt><dt>40038</dt></dl> | Identifie l’attribut de texte <strong>CaretPosition</strong> , qui indique si le signe insertion se trouve au début ou à la fin d’une ligne de texte dans la plage de texte. Cet attribut est spécifié en tant que valeur du type énuméré <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-caretposition"><strong>CaretPosition</strong></a> . Pris en charge à partir de Windows 8.<br /> Type Variant : <strong>VT_I4</strong><br /> Valeur par défaut : <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-caretposition"> <strong>CaretPosition_Unknown</strong></a><br /> | 
| <span id="UIA_CultureAttributeId"></span><span id="uia_cultureattributeid"></span><span id="UIA_CULTUREATTRIBUTEID"></span><dl><dt><strong>UIA_CultureAttributeId</strong></dt><dt>40004</dt></dl> | Identifie l’attribut de texte de <strong>culture</strong> , qui spécifie les paramètres régionaux du texte par identificateur de paramètres régionaux (LCID). <br /> Type Variant : <strong>VT_I4</strong><br /> Valeur par défaut : paramètres régionaux de l’interface utilisateur de l’application<br /> | 
| <span id="UIA_FontNameAttributeId"></span><span id="uia_fontnameattributeid"></span><span id="UIA_FONTNAMEATTRIBUTEID"></span><dl><dt><strong>UIA_FontNameAttributeId</strong></dt><dt>40005</dt></dl> | Identifie l’attribut de texte <strong>FontName</strong> , qui spécifie le nom de la police. Exemples : « Arial Black »; « Arial Narrow ». La chaîne de nom de police n’est pas localisée. <br /> Type Variant : <strong>VT_BSTR</strong><br /> Valeur par défaut : chaîne vide<br /> | 
| <span id="UIA_FontSizeAttributeId"></span><span id="uia_fontsizeattributeid"></span><span id="UIA_FONTSIZEATTRIBUTEID"></span><dl><dt><strong>UIA_FontSizeAttributeId</strong></dt><dt>40006</dt></dl> | Identifie l’attribut de texte <strong>FontSize</strong> , qui spécifie la taille en points de la police. <br /> Type Variant : <strong>VT_R8</strong><br /> Valeur par défaut : 0<br /> | 
| <span id="UIA_FontWeightAttributeId"></span><span id="uia_fontweightattributeid"></span><span id="UIA_FONTWEIGHTATTRIBUTEID"></span><dl><dt><strong>UIA_FontWeightAttributeId</strong></dt><dt>40007</dt></dl> | Identifie l’attribut de texte <strong>FontWeight</strong> , qui spécifie le trait, l’épaisseur ou le gras de la police relatifs. L’attribut <strong>FontWeight</strong> est modélisé après le membre <strong>lfWeight</strong> de la structure GDI <a href="/windows/win32/api/wingdi/ns-wingdi-logfonta">LOGFONT</a> , et les normes associées, et peut prendre l’une des valeurs suivantes :<ul><li>0 = <strong>DontCare</strong></li><li>100 = <strong>fin</strong></li><li>200 = <strong>« extralight »</strong> ou <strong>Ultralight</strong></li><li>300 = <strong>clair</strong></li><li>400 = <strong>normal</strong> ou <strong>normal</strong></li><li>500 = <strong>moyenne</strong></li><li>600 = <strong>SemiBold</strong></li><li>700 = <strong>gras</strong></li><li>800 = <strong>ExtraBold</strong> ou <strong>« UltraBold »</strong></li><li>900 = <strong>épais</strong> ou <strong>noir</strong></li></ul><br /> Type Variant : <strong>VT_I4</strong><br /> Valeur par défaut : 0<br /> | 
| <span id="UIA_ForegroundColorAttributeId"></span><span id="uia_foregroundcolorattributeid"></span><span id="UIA_FOREGROUNDCOLORATTRIBUTEID"></span><dl><dt><strong>UIA_ForegroundColorAttributeId</strong></dt><dt>40008</dt></dl> | Identifie l’attribut de texte <strong>ForegroundColor</strong> , qui spécifie la couleur de premier plan du texte. Cet attribut est spécifié en tant que <a href="/windows/win32/gdi/colorref">COLORREF</a>, valeur 32 bits utilisée pour spécifier une couleur RVB ou RVBA. <br /> Type Variant : <strong>VT_I4</strong><br /> Valeur par défaut : 0<br /> | 
| <span id="UIA_HorizontalTextAlignmentAttributeId"></span><span id="uia_horizontaltextalignmentattributeid"></span><span id="UIA_HORIZONTALTEXTALIGNMENTATTRIBUTEID"></span><dl><dt><strong>UIA_HorizontalTextAlignmentAttributeId</strong></dt><dt>40009</dt></dl> | Identifie l’attribut de texte <strong>HorizontalTextAlignment</strong> , qui spécifie la façon dont le texte est aligné horizontalement. Cet attribut est spécifié en tant que valeur du type énuméré <a href="/previous-versions/windows/desktop/legacy/ee671233(v=vs.85)"><strong>HorizontalTextAlignmentEnum</strong></a> . <br /> Type Variant : <strong>VT_I4</strong><br /> Valeur par défaut : <a href="/previous-versions/windows/desktop/legacy/ee671233(v=vs.85)"> <strong>HorizontalTextAlignment_Left</strong></a><br /> | 
| <span id="UIA_IndentationFirstLineAttributeId"></span><span id="uia_indentationfirstlineattributeid"></span><span id="UIA_INDENTATIONFIRSTLINEATTRIBUTEID"></span><dl><dt><strong>UIA_IndentationFirstLineAttributeId</strong></dt><dt>40010</dt></dl> | Identifie l’attribut de texte <strong>IndentationFirstLine</strong> , qui spécifie la distance, en points, de mise en retrait de la première ligne d’un paragraphe. <br /> Type Variant : <strong>VT_R8</strong><br /> Valeur par défaut : 0<br /> | 
| <span id="UIA_IndentationLeadingAttributeId"></span><span id="uia_indentationleadingattributeid"></span><span id="UIA_INDENTATIONLEADINGATTRIBUTEID"></span><dl><dt><strong>UIA_IndentationLeadingAttributeId</strong></dt><dt>40011</dt></dl> | Identifie l’attribut de texte <strong>IndentationLeading</strong> , qui spécifie la mise en retrait de début, en points. <br /> Type Variant : <strong>VT_R8</strong><br /> Valeur par défaut : 0<br /> | 
| <span id="UIA_IndentationTrailingAttributeId"></span><span id="uia_indentationtrailingattributeid"></span><span id="UIA_INDENTATIONTRAILINGATTRIBUTEID"></span><dl><dt><strong>UIA_IndentationTrailingAttributeId</strong></dt><dt>40012</dt></dl> | Identifie l’attribut de texte <strong>IndentationTrailing</strong> , qui spécifie la mise en retrait de fin, en points. <br /> Type Variant : <strong>VT_R8</strong><br /> Valeur par défaut : 0<br /> | 
| <span id="UIA_IsActiveAttributeId"></span><span id="uia_isactiveattributeid"></span><span id="UIA_ISACTIVEATTRIBUTEID"></span><dl><dt><strong>UIA_IsActiveAttributeId</strong></dt><dt>40036</dt></dl> | Identifie l’attribut de texte <strong>IsActive</strong> , qui indique si le contrôle qui contient la plage de texte a le focus clavier (<strong>true</strong>) ou non (<strong>false</strong>). Pris en charge à partir de Windows 8.<br /> Type Variant : <strong>VT_BOOL</strong><br /> Valeur par défaut : <strong>false</strong><br /> | 
| <span id="UIA_IsHiddenAttributeId"></span><span id="uia_ishiddenattributeid"></span><span id="UIA_ISHIDDENATTRIBUTEID"></span><dl><dt><strong>UIA_IsHiddenAttributeId</strong></dt><dt>40013</dt></dl> | Identifie l’attribut de texte <strong>IsHidden</strong> , qui indique si le texte est masqué (<strong>true</strong>) ou visible (<strong>false</strong>). <br /> Type Variant : <strong>VT_BOOL</strong><br /> Valeur par défaut : <strong>false</strong><br /> | 
| <span id="UIA_IsItalicAttributeId"></span><span id="uia_isitalicattributeid"></span><span id="UIA_ISITALICATTRIBUTEID"></span><dl><dt><strong>UIA_IsItalicAttributeId</strong></dt><dt>40014</dt></dl> | Identifie l’attribut de texte <strong>IsItalic</strong> , qui indique si le texte est en italique (<strong>true</strong>) ou non (<strong>false</strong>). <br /> Type Variant : <strong>VT_BOOL</strong><br /> Valeur par défaut : <strong>false</strong><br /> | 
| <span id="UIA_IsReadOnlyAttributeId"></span><span id="uia_isreadonlyattributeid"></span><span id="UIA_ISREADONLYATTRIBUTEID"></span><dl><dt><strong>UIA_IsReadOnlyAttributeId</strong></dt><dt>40015</dt></dl> | Identifie l’attribut de texte <strong>IsReadOnly</strong> , qui indique si le texte est en lecture seule (<strong>true</strong>) ou s’il peut être modifié (<strong>false</strong>). <br /> Type Variant : <strong>VT_BOOL</strong><br /> Valeur par défaut : <strong>false</strong><br /> | 
| <span id="UIA_IsSubscriptAttributeId"></span><span id="uia_issubscriptattributeid"></span><span id="UIA_ISSUBSCRIPTATTRIBUTEID"></span><dl><dt><strong>UIA_IsSubscriptAttributeId</strong></dt><dt>40016</dt></dl> | Identifie l’attribut de texte <strong>IsSubscript</strong> , qui indique si le texte est un indice (<strong>true</strong>) ou non (<strong>false</strong>). <br /> Type Variant : <strong>VT_BOOL</strong><br /> Valeur par défaut : <strong>false</strong><br /> | 
| <span id="UIA_IsSuperscriptAttributeId"></span><span id="uia_issuperscriptattributeid"></span><span id="UIA_ISSUPERSCRIPTATTRIBUTEID"></span><dl><dt><strong>UIA_IsSuperscriptAttributeId</strong></dt><dt>40017</dt></dl> | Identifie l’attribut de texte <strong>IsSuperscript</strong> , qui indique si le texte est un indice (<strong>true</strong>) ou non (<strong>false</strong>). <br /> Type Variant : <strong>VT_BOOL</strong><br /> Valeur par défaut : <strong>false</strong><br /> | 
| <span id="UIA_LineSpacingAttributeId"></span><span id="uia_linespacingattributeid"></span><span id="UIA_LINESPACINGATTRIBUTEID"></span><dl><dt><strong>UIA_LineSpacingAttributeId</strong></dt><dt>40040</dt></dl> | Identifie l’attribut de texte <strong>LineSpacing</strong> , qui spécifie l’espacement entre les lignes de texte.<br /> Type Variant : <strong>VT_BSTR</strong><br /> Valeur par défaut : « LineSpacingAttributeDefault »<br /> | 
| <span id="UIA_LinkAttributeId"></span><span id="uia_linkattributeid"></span><span id="UIA_LINKATTRIBUTEID"></span><dl><dt><strong>UIA_LinkAttributeId</strong></dt><dt>40035</dt></dl> | Identifie l’attribut de texte de <strong>lien</strong> , qui contient l’interface <a href="/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationtextrange"><strong>IUIAutomationTextRange</strong></a> de la plage de texte qui est la cible d’un lien interne dans un document. Pris en charge à partir de Windows 8.<br /> Type Variant : <strong>VT_UNKNOWN</strong><br /> Valeur par défaut : <strong>null</strong><br /> | 
| <span id="UIA_MarginBottomAttributeId"></span><span id="uia_marginbottomattributeid"></span><span id="UIA_MARGINBOTTOMATTRIBUTEID"></span><dl><dt><strong>UIA_MarginBottomAttributeId</strong></dt><dt>40018</dt></dl> | Identifie l’attribut de texte <strong>marginBottom</strong> , qui spécifie la taille, en points, de la marge inférieure appliquée à la page associée à la plage de texte. <br /> Type Variant : <strong>VT_R8</strong><br /> Valeur par défaut : 0<br /> | 
| <span id="UIA_MarginLeadingAttributeId"></span><span id="uia_marginleadingattributeid"></span><span id="UIA_MARGINLEADINGATTRIBUTEID"></span><dl><dt><strong>UIA_MarginLeadingAttributeId</strong></dt><dt>40019</dt></dl> | Identifie l’attribut de texte <strong>MarginLeading</strong> , qui spécifie la taille, en points, de la marge de début appliquée à la page associée à la plage de texte. <br /> Type Variant : <strong>VT_R8</strong><br /> Valeur par défaut : 0<br /> | 
| <span id="UIA_MarginTopAttributeId"></span><span id="uia_margintopattributeid"></span><span id="UIA_MARGINTOPATTRIBUTEID"></span><dl><dt><strong>UIA_MarginTopAttributeId</strong></dt><dt>40020</dt></dl> | Identifie l’attribut de texte <strong>marginTop</strong> , qui spécifie la taille, en points, de la marge supérieure appliquée à la page associée à la plage de texte. <br /> Type Variant : <strong>VT_R8</strong><br /> Valeur Ddefault : 0<br /> | 
| <span id="UIA_MarginTrailingAttributeId"></span><span id="uia_margintrailingattributeid"></span><span id="UIA_MARGINTRAILINGATTRIBUTEID"></span><dl><dt><strong>UIA_MarginTrailingAttributeId</strong></dt><dt>40021</dt></dl> | Identifie l’attribut de texte <strong>MarginTrailing</strong> , qui spécifie la taille, en points, de la marge de fin appliquée à la page associée à la plage de texte. <br /> Type Variant : <strong>VT_R8</strong><br /> Valeur par défaut : 0<br /> | 
| <span id="UIA_OutlineStylesAttributeId"></span><span id="uia_outlinestylesattributeid"></span><span id="UIA_OUTLINESTYLESATTRIBUTEID"></span><dl><dt><strong>UIA_OutlineStylesAttributeId</strong></dt><dt>40022</dt></dl> | Identifie l’attribut de texte <strong>OutlineStyles</strong> , qui spécifie le style de contour du texte. Cet attribut est spécifié en tant que valeur du type énuméré <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-outlinestyles"><strong>OutlineStyles</strong></a> . <br /> Type Variant : <strong>VT_I4</strong><br /> Valeur par défaut : <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-outlinestyles"> <strong>OutlineStyles_None</strong></a><br /> | 
| <span id="UIA_OverlineColorAttributeId"></span><span id="uia_overlinecolorattributeid"></span><span id="UIA_OVERLINECOLORATTRIBUTEID"></span><dl><dt><strong>UIA_OverlineColorAttributeId</strong></dt><dt>40023</dt></dl> | Identifie l’attribut de texte <strong>OverlineColor</strong> , qui spécifie la couleur de la décoration du texte de la ligne. Cet attribut est spécifié en tant que <a href="/windows/win32/gdi/colorref">COLORREF</a>, valeur 32 bits utilisée pour spécifier une couleur RVB ou RVBA. <br /> Type Variant : <strong>VT_I4</strong><br /> Valeur par défaut : 0<br /> | 
| <span id="UIA_OverlineStyleAttributeId"></span><span id="uia_overlinestyleattributeid"></span><span id="UIA_OVERLINESTYLEATTRIBUTEID"></span><dl><dt><strong>UIA_OverlineStyleAttributeId</strong></dt><dt>40024</dt></dl> | Identifie l’attribut de texte <strong>OverlineStyle</strong> , qui spécifie le style de la décoration de texte en surligne. Cet attribut est spécifié en tant que valeur du type énuméré <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textdecorationlinestyle"><strong>TextDecorationLineStyleEnum</strong></a> . <br /> Type Variant : <strong>VT_I4</strong><br /> Valeur par défaut : <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textdecorationlinestyle"> <strong>TextDecorationLineStyle_None</strong></a><br /> | 
| <span id="UIA_SelectionActiveEndAttributeId"></span><span id="uia_selectionactiveendattributeid"></span><span id="UIA_SELECTIONACTIVEENDATTRIBUTEID"></span><dl><dt><strong>UIA_SelectionActiveEndAttributeId</strong></dt><dt>40037</dt></dl> | Identifie l’attribut de texte <strong>SelectionActiveEnd</strong> , qui indique l’emplacement du signe insertion par rapport à une plage de texte qui représente le texte actuellement sélectionné. Cet attribut est spécifié en tant que valeur de l’énumération <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-activeend"><strong>ActiveEnd</strong></a> . Pris en charge à partir de Windows 8.<br /> Type Variant : <strong>VT_I4</strong><br /> Valeur par défaut : <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-activeend"> <strong>ActiveEnd_None</strong></a><br /> | 
| <span id="UIA_StrikethroughColorAttributeId"></span><span id="uia_strikethroughcolorattributeid"></span><span id="UIA_STRIKETHROUGHCOLORATTRIBUTEID"></span><dl><dt><strong>UIA_StrikethroughColorAttributeId</strong></dt><dt>40025</dt></dl> | Identifie l’attribut de texte <strong>StrikethroughColor</strong> , qui spécifie la couleur de la décoration du texte barré. Cet attribut est spécifié en tant que <a href="/windows/win32/gdi/colorref">COLORREF</a>, valeur 32 bits utilisée pour spécifier une couleur RVB ou RVBA. <br /> Type Variant : <strong>VT_I4</strong><br /> Valeur par défaut : 0<br /> | 
| <span id="UIA_StrikethroughStyleAttributeId"></span><span id="uia_strikethroughstyleattributeid"></span><span id="UIA_STRIKETHROUGHSTYLEATTRIBUTEID"></span><dl><dt><strong>UIA_StrikethroughStyleAttributeId</strong></dt><dt>40026</dt></dl> | Identifie l’attribut de texte <strong>StrikethroughStyle</strong> , qui spécifie le style de la décoration du texte barré. Cet attribut est spécifié en tant que valeur du type énuméré <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textdecorationlinestyle"><strong>TextDecorationLineStyleEnum</strong></a> . <br /> Type Variant : <strong>VT_I4</strong><br /> Valeur par défaut : <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textdecorationlinestyle"> <strong>TextDecorationLineStyle_None</strong></a><br /> | 
| <span id="UIA_StyleIdAttributeId"></span><span id="uia_styleidattributeid"></span><span id="UIA_STYLEIDATTRIBUTEID"></span><dl><dt><strong>UIA_StyleIdAttributeId</strong></dt><dt>40034</dt></dl> | Identifie l’attribut de texte <strong>StyleId</strong> , qui indique les styles de texte en cours d’utilisation pour une plage de texte. Pour obtenir la liste des valeurs possibles, consultez <a href="uiauto-style-identifiers.md"><strong>identificateurs de style</strong></a>. Pris en charge à partir de Windows 8.<br /> Type Variant : <strong>VT_I4</strong><br /> Valeur par défaut : 0 <br /> | 
| <span id="UIA_StyleNameAttributeId"></span><span id="uia_stylenameattributeid"></span><span id="UIA_STYLENAMEATTRIBUTEID"></span><dl><dt><strong>UIA_StyleNameAttributeId</strong></dt><dt>40033</dt></dl> | Identifie l’attribut de texte <strong>styleName</strong> , qui identifie le nom localisé du style de texte utilisé pour une plage de texte. Pris en charge à partir de Windows 8.<br /> Type Variant : <strong>VT_BSTR</strong><br /> Valeur par défaut : chaîne vide<br /> | 
| <span id="UIA_TabsAttributeId"></span><span id="uia_tabsattributeid"></span><span id="UIA_TABSATTRIBUTEID"></span><dl><dt><strong>UIA_TabsAttributeId</strong></dt><dt>40027</dt></dl> | Identifie l’attribut de texte <strong>Tabs</strong> , qui est un tableau spécifiant les taquets de tabulation de la plage de texte. Chaque élément de tableau spécifie une distance, en points, à partir de la marge de début. <br /> Type Variant : <strong> VT_ARRAY | VT_R8</strong><br /> Valeur par défaut : tableau vide<br /> | 
| <span id="UIA_TextFlowDirectionsAttributeId"></span><span id="uia_textflowdirectionsattributeid"></span><span id="UIA_TEXTFLOWDIRECTIONSATTRIBUTEID"></span><dl><dt><strong>UIA_TextFlowDirectionsAttributeId</strong></dt><dt>40028</dt></dl> | Identifie l’attribut de texte <strong>TextFlowDirections</strong> , qui spécifie le sens du déroulement du texte. Cet attribut est spécifié sous la forme d’une combinaison de valeurs du type énuméré <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-flowdirections"><strong>FlowDirections</strong></a> . <br /> Type Variant : <strong>VT_I4</strong><br /> Valeur par défaut : <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-flowdirections"> <strong>FlowDirections_Default</strong></a><br /> | 
| <span id="UIA_UnderlineColorAttributeId"></span><span id="uia_underlinecolorattributeid"></span><span id="UIA_UNDERLINECOLORATTRIBUTEID"></span><dl><dt><strong>UIA_UnderlineColorAttributeId</strong></dt><dt>40029</dt></dl> | Identifie l’attribut de texte <strong>UnderlineColor</strong> , qui spécifie la couleur de la décoration de texte souligné. Cet attribut est spécifié en tant que <a href="/windows/win32/gdi/colorref">COLORREF</a>, valeur 32 bits utilisée pour spécifier une couleur RVB ou RVBA. <br /> Type Variant : <strong>VT_I4</strong><br /> Valeur par défaut : 0<br /> | 
| <span id="UIA_UnderlineStyleAttributeId"></span><span id="uia_underlinestyleattributeid"></span><span id="UIA_UNDERLINESTYLEATTRIBUTEID"></span><dl><dt><strong>UIA_UnderlineStyleAttributeId</strong></dt><dt>40030</dt></dl> | Identifie l’attribut de texte <strong>UnderlineStyle</strong> , qui spécifie le style de la décoration de texte souligné. Cet attribut est spécifié en tant que valeur du type énuméré <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textdecorationlinestyle"><strong>TextDecorationLineStyleEnum</strong></a> . <br /> Type Variant : <strong>VT_I4</strong><br /> Valeur par défaut : <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-textdecorationlinestyle"> <strong>TextDecorationLineStyle_None</strong></a><br /> | 




## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP pour applications \[ \| UWP\]<br/>                                              |
| Serveur minimal pris en charge<br/> | Windows Applications de bureau du serveur 2003 \[ \| applications UWP\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>UIAutomationClient. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Référence**
</dt> <dt>

[**ITextRangeProvider::FindAttribute**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-findattribute)
</dt> <dt>

[**ITextRangeProvider :: GetAttributeValue**](/windows/desktop/api/UIAutomationCore/nf-uiautomationcore-itextrangeprovider-getattributevalue)
</dt> <dt>

[**IUIAutomation::FindAttribute**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-findattribute)
</dt> <dt>

[**IUIAutomation :: GetAttributeValue**](/windows/desktop/api/UIAutomationClient/nf-uiautomationclient-iuiautomationtextrange-getattributevalue)
</dt> <dt>

**Conceptuel**
</dt> <dt>

[Prise en charge d’UI Automation pour le contenu textuel](uiauto-ui-automation-textpattern-overview.md)
</dt> </dl>
