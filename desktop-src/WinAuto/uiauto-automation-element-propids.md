---
title: Identificateurs de propriété d’élément Automation (UIAutomationClient. h)
description: Cette rubrique décrit les constantes nommées qui identifient les propriétés des éléments de Microsoft UI Automation.
ms.assetid: f7613ad1-0b75-46fb-b9ac-b1ae9eea4193
topic_type:
- apiref
api_name:
- UIA_AcceleratorKeyPropertyId
- UIA_AccessKeyPropertyId
- UIA_AnnotationObjectsPropertyId
- UIA_AnnotationTypesPropertyId
- UIA_AriaPropertiesPropertyId
- UIA_AriaRolePropertyId
- UIA_AutomationIdPropertyId
- UIA_BoundingRectanglePropertyId
- UIA_CenterPointPropertyId
- UIA_ClassNamePropertyId
- UIA_ClickablePointPropertyId
- UIA_ControllerForPropertyId
- UIA_ControlTypePropertyId
- UIA_CulturePropertyId
- UIA_DescribedByPropertyId
- UIA_FillColorPropertyId
- UIA_FillTypePropertyId
- UIA_FlowsFromPropertyId
- UIA_FlowsToPropertyId
- UIA_FrameworkIdPropertyId
- UIA_FullDescriptionPropertyId
- UIA_HasKeyboardFocusPropertyId
- UIA_HeadingLevelPropertyId
- UIA_HelpTextPropertyId
- UIA_IsContentElementPropertyId
- UIA_IsControlElementPropertyId
- UIA_IsDataValidForFormPropertyId
- UIA_IsEnabledPropertyId
- UIA_IsKeyboardFocusablePropertyId
- UIA_IsOffscreenPropertyId
- UIA_IsPasswordPropertyId
- UIA_IsPeripheralPropertyId
- UIA_IsRequiredForFormPropertyId
- UIA_ItemStatusPropertyId
- UIA_ItemTypePropertyId
- UIA_LabeledByPropertyId
- UIA_LandmarkTypePropertyId
- UIA_LevelPropertyId
- UIA_LiveSettingPropertyId
- UIA_LocalizedControlTypePropertyId
- UIA_LocalizedLandmarkTypePropertyId
- UIA_NamePropertyId
- UIA_NativeWindowHandlePropertyId
- UIA_OptimizeForVisualContentPropertyId
- UIA_OrientationPropertyId
- UIA_OutlineColorPropertyId
- UIA_OutlineThicknessPropertyId
- UIA_PositionInSetPropertyId
- UIA_ProcessIdPropertyId
- UIA_ProviderDescriptionPropertyId
- UIA_RotationPropertyId
- UIA_RuntimeIdPropertyId
- UIA_SizePropertyId
- UIA_SizeOfSetPropertyId
- UIA_VisualEffectsPropertyId
api_location:
- UIAutomationClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b373091ec34e71afbac32fca962ec380513acfcd
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627695"
---
# <a name="automation-element-property-identifiers"></a>Identificateurs de propriété d’élément Automation

Cette rubrique décrit les constantes nommées qui identifient les propriétés des éléments de Microsoft UI Automation.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th >Constante/valeur</th>
<th >Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td ><span id="UIA_AcceleratorKeyPropertyId"></span><span id="uia_acceleratorkeypropertyid"></span><span id="UIA_ACCELERATORKEYPROPERTYID"></span><dl> <dt><strong>UIA_AcceleratorKeyPropertyId</strong></dt> <dt>30006</dt> </dl></td>
<td >Identifie la propriété <strong>AcceleratorKey</strong> , qui est une chaîne contenant les combinaisons touche accélérateur (également appelée touche de raccourci) pour l’élément Automation. <br/> Les combinaisons de touches de raccourci appellent une action. Par exemple, la combinaison de touches CTRL + O est souvent utilisée pour appeler la boîte de dialogue Ouvrir un fichier commun. Un élément Automation qui a la propriété <strong>AcceleratorKey</strong> peut implémenter le modèle de contrôle <a href="uiauto-implementinginvoke.md">Invoke</a> pour l’action qui est équivalente à la commande de raccourci.<br/> Type Variant : <strong>VT_BSTR</strong><br/> Valeur par défaut : chaîne vide<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_AccessKeyPropertyId"></span><span id="uia_accesskeypropertyid"></span><span id="UIA_ACCESSKEYPROPERTYID"></span><dl> <dt><strong>UIA_AccessKeyPropertyId</strong></dt> <dt>30007</dt> </dl></td>
<td >Identifie la propriété <strong>AccessKey</strong> , qui est une chaîne contenant le caractère clé d’accès de l’élément Automation.<br/> Une clé d’accès (parfois appelée mnémonique) est un caractère dans le texte d’un menu, un élément de menu ou une étiquette d’un contrôle tel qu’un bouton, qui active la fonction de menu associée. Par exemple, pour ouvrir le menu fichier, pour lequel la touche d’accès est généralement F, l’utilisateur appuie sur ALT + F.<br/> Type Variant : <strong>VT_BSTR</strong><br/> Valeur par défaut : chaîne vide<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_AnnotationObjectsPropertyId"></span><span id="uia_annotationobjectspropertyid"></span><span id="UIA_ANNOTATIONOBJECTSPROPERTYID"></span><dl> <dt><strong>UIA_AnnotationObjectsPropertyId</strong></dt> <dt>30156</dt> </dl></td>
<td >Identifie la propriété <strong>AnnotationObjects</strong> , qui est une liste d’objets annotation dans un document, comme un commentaire, un en-tête, un pied de page, etc.<br/> Type Variant : <strong>VT_I4</strong>  |  <strong>VT_ARRAY</strong><br/> Valeur par défaut : tableau vide<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_AnnotationTypesPropertyId"></span><span id="uia_annotationtypespropertyid"></span><span id="UIA_ANNOTATIONTYPESPROPERTYID"></span><dl> <dt><strong>UIA_AnnotationTypesPropertyId</strong></dt> <dt>30155</dt> </dl></td>
<td >Identifie la propriété <strong>AnnotationTypes</strong> , qui est une liste des types d’annotations dans un document, tels que le commentaire, l’en-tête, le pied de page, etc.<br/> Type Variant : <strong>VT_I4</strong>  |  <strong>VT_ARRAY</strong><br/> Valeur par défaut : tableau vide<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_AriaPropertiesPropertyId"></span><span id="uia_ariapropertiespropertyid"></span><span id="UIA_ARIAPROPERTIESPROPERTYID"></span><dl> <dt><strong>UIA_AriaPropertiesPropertyId</strong></dt> <dt>30102</dt> </dl></td>
<td >Identifie la propriété <strong>AriaProperties</strong> , qui est une chaîne mise en forme contenant les informations de propriété d’application Internet riche (ARIA) accessibles pour l’élément Automation. Pour plus d’informations sur le mappage des États et des propriétés ARIA aux propriétés et fonctions UI Automation, consultez <a href="uiauto-ariaspecification.md">UI Automation pour la spécification des applications Internet riches accessibles par le W3C</a>.<br/> <strong>AriaProperties</strong> est une collection de paires nom/valeur avec des délimiteurs de <strong>=</strong> (égal à) et <strong>;</strong> (point-virgule), par exemple, &quot; Checked = True ; Disabled = false &quot; . La <strong>\</strong> barre oblique inverse () est utilisée comme caractère d’échappement lorsque ces caractères délimitent ou <strong>\</strong> s’affichent dans les valeurs. Pour des raisons de sécurité et autres, l’implémentation du fournisseur de cette propriété peut prendre des mesures pour valider les propriétés ARIA d’origine. Toutefois, ce n’est pas obligatoire.<br/> Type Variant : <strong>VT_BSTR</strong><br/> Valeur par défaut : chaîne vide<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_AriaRolePropertyId"></span><span id="uia_ariarolepropertyid"></span><span id="UIA_ARIAROLEPROPERTYID"></span><dl> <dt><strong>UIA_AriaRolePropertyId</strong></dt> <dt>30101</dt> </dl></td>
<td >Identifie la propriété <strong>AriaRole</strong> , qui est une chaîne contenant les informations de rôle Aria (Rich Internet application) accessibles pour l’élément Automation. Pour plus d’informations sur le mappage des rôles ARIA à des types de contrôle UI Automation, consultez <a href="uiauto-ariaspecification.md">UI Automation pour la spécification des applications Internet riches accessibles par le W3C</a>.<br/>
<blockquote>
[!Note]<br />
En guise d’option, l’agent utilisateur peut également fournir une description localisée du rôle ARIA du W3C dans la propriété <strong>LocalizedControlType</strong> . Lorsque la chaîne localisée n’est pas spécifiée, le système fournit la chaîne <strong>LocalizedControlType</strong> par défaut pour l’élément.
</blockquote>
<br/> <br/> Type Variant : <strong>VT_BSTR</strong><br/> Valeur par défaut : chaîne vide<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_AutomationIdPropertyId"></span><span id="uia_automationidpropertyid"></span><span id="UIA_AUTOMATIONIDPROPERTYID"></span><dl> <dt><strong>UIA_AutomationIdPropertyId</strong></dt> <dt>30011</dt> </dl></td>
<td >Identifie la propriété <strong>AutomationId</strong> , qui est une chaîne contenant l’identificateur UI Automation (ID) de l’élément Automation.<br/> Lorsqu’il est disponible, le <strong>AutomationId</strong> d’un élément doit être le même dans n’importe quelle instance de l’application, quelle que soit la langue locale. La valeur doit être unique parmi les éléments frères, mais elle n’est pas nécessairement unique sur l’ensemble du bureau. par exemple, plusieurs instances d’une application, ou plusieurs affichages de dossiers dans l’explorateur de Windows Microsoft, peuvent contenir des éléments avec la même propriété <strong>AutomationId</strong> , par exemple &quot; SystemMenuBar &quot; .<br/> Bien que la prise en charge de <strong>AutomationId</strong> soit toujours recommandée pour une meilleure prise en charge des tests automatisés, cette propriété n’est pas obligatoire. Lorsqu’il est pris en charge, <strong>AutomationId</strong> est utile pour créer un script d’automatisation des tests qui s’exécute indépendamment de la langue de l’interface utilisateur. Les clients ne doivent pas faire d’hypothèses concernant les valeurs <strong>AutomationId</strong> exposées par d’autres applications. Il n’est pas garanti que <strong>AutomationId</strong> soit stable dans les différentes versions ou les versions d’une application.<br/> Type Variant : <strong>VT_BSTR</strong><br/> Valeur par défaut : chaîne vide<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_BoundingRectanglePropertyId"></span><span id="uia_boundingrectanglepropertyid"></span><span id="UIA_BOUNDINGRECTANGLEPROPERTYID"></span><dl> <dt><strong>UIA_BoundingRectanglePropertyId</strong></dt> <dt>30001</dt> </dl></td>
<td >Identifie la propriété <strong>BoundingRectangle</strong> , qui spécifie les coordonnées du rectangle qui englobe complètement l’élément Automation. Le rectangle est exprimé en coordonnées d’écran physiques. Elle peut contenir des points qui ne sont pas interdépendants si la forme ou la zone de l’élément de l’interface utilisateur cliquable est irrégulière, ou si l’élément est masqué par d’autres éléments de l’interface utilisateur.<br/> Type Variant : <strong>VT_R8</strong>  |  <strong>VT_ARRAY</strong><br/> Valeur par défaut : [0, 0, 0, 0]<br/>
<blockquote>
[!Note]<br />
Cette propriété a la <strong>valeur null</strong> si l’élément n’affiche pas actuellement une interface utilisateur.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_CenterPointPropertyId"></span><span id="uia_centerpointpropertyid"></span><span id="UIA_CENTERPOINTPROPERTYID"></span><dl> <dt><strong>UIA_CenterPointPropertyId</strong></dt> <dt>30165</dt> </dl></td>
<td >Identifie la propriété <strong>Centerpoint</strong> , qui spécifie les coordonnées du centre X et Y de l’élément Automation. L’espace de coordonnées est ce que le fournisseur considère logiquement comme une page.<br/> Type Variant : <strong>VT_R8</strong>  |  <strong>VT_ARRAY</strong><br/> Valeur par défaut : <strong>VT_EMPTY</strong><br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_ClassNamePropertyId"></span><span id="uia_classnamepropertyid"></span><span id="UIA_CLASSNAMEPROPERTYID"></span><dl> <dt><strong>UIA_ClassNamePropertyId</strong></dt> <dt>30012</dt> </dl></td>
<td >Identifie la propriété <strong>className</strong> , qui est une chaîne contenant le nom de classe de l’élément Automation tel qu’assigné par le développeur de contrôle.<br/> Le nom de la classe dépend de l’implémentation du fournisseur UI Automation et, par conséquent, n’est pas toujours dans un format standard. Toutefois, si le nom de la classe est connu, il peut être utilisé pour vérifier qu’une application fonctionne avec l’élément Automation attendu.<br/> Type Variant : <strong>VT_BSTR</strong><br/> Valeur par défaut : chaîne vide<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_ClickablePointPropertyId"></span><span id="uia_clickablepointpropertyid"></span><span id="UIA_CLICKABLEPOINTPROPERTYID"></span><dl> <dt><strong>UIA_ClickablePointPropertyId</strong></dt> <dt>30014</dt> </dl></td>
<td >Identifie la propriété <strong>ClickablePoint</strong> , qui est un point de l’élément Automation sur lequel vous pouvez cliquer. Un élément ne peut pas être cliqué s’il est totalement ou partiellement masqué par une autre fenêtre.<br/> Type Variant : <strong>VT_R8</strong>  |  <strong>VT_ARRAY</strong><br/> Valeur par défaut : <strong>VT_EMPTY</strong><br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_ControllerForPropertyId"></span><span id="uia_controllerforpropertyid"></span><span id="UIA_CONTROLLERFORPROPERTYID"></span><dl> <dt><strong>UIA_ControllerForPropertyId</strong></dt> <dt>30104</dt> </dl></td>
<td >Identifie la propriété <strong>ControllerFor</strong> , qui est un tableau d’éléments Automation manipulés par l’élément Automation qui prend en charge cette propriété.<br/> <strong>ControllerFor</strong> est utilisé lorsqu’un élément Automation affecte un ou plusieurs segments de l’interface utilisateur de l’application ou du bureau. dans le cas contraire, il est difficile d’associer l’impact de l’opération de contrôle aux éléments d’interface utilisateur.<br/> Cet identificateur est couramment utilisé pour l' <a href="/windows/uwp/design/accessibility/accessible-text-requirements">accessibilité de suggestion automatique</a>.<br/> Type Variant pour les fournisseurs : <strong>VT_UNKNOWN</strong>  |  <strong>VT_ARRAY</strong><br/> Type Variant pour les clients : <strong>VT_UNKNOWN</strong> (<a href="/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray"><strong>IUIAutomationElementArray</strong></a> )<br/> Valeur par défaut : tableau vide<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_ControlTypePropertyId"></span><span id="uia_controltypepropertyid"></span><span id="UIA_CONTROLTYPEPROPERTYID"></span><dl> <dt><strong>UIA_ControlTypePropertyId</strong></dt> <dt>30003</dt> </dl></td>
<td >Identifie la propriété <strong>ControlType</strong> , qui est une classe qui identifie le type de l’élément Automation. <strong>ControlType</strong> définit les caractéristiques des éléments d’interface utilisateur par le biais de primitives de contrôle d’interface utilisateur connues comme Button ou case à cocher. <br/> Type Variant : <strong>VT_I4</strong><br/> Valeur par défaut : <a href="uiauto-controltype-ids.md"> <strong>UIA_CustomControlTypeId</strong></a><br/>
<blockquote>
[!Note]<br />
Utilisez la valeur par défaut uniquement si l’élément Automation représente un nouveau type de contrôle.
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_CulturePropertyId"></span><span id="uia_culturepropertyid"></span><span id="UIA_CULTUREPROPERTYID"></span><dl> <dt><strong>UIA_CulturePropertyId</strong></dt> <dt>30015</dt> </dl></td>
<td >Identifie la propriété de <strong>culture</strong> , qui contient un identificateur de paramètres régionaux pour l’élément Automation (par exemple, <code>0x0409</code> pour &quot; en-US &quot; ou anglais (États-Unis)).<br/> Chaque paramètre régional a un identificateur unique, une valeur de 32 bits qui se compose d’un identificateur de langue et d’un identificateur d’ordre de tri. L’identificateur de paramètres régionaux est une abréviation numérique internationale standard et contient les composants nécessaires pour identifier de manière unique l’un des paramètres régionaux définis par le système d’exploitation installés. Pour plus d’informations, consultez <a href="/windows/desktop/Intl/language-identifier-constants-and-strings">constantes et chaînes</a>de l’identificateur de langue.<br/> Cette propriété peut exister pour chaque contrôle, mais elle est généralement disponible uniquement au niveau de l’application.<br/> Type Variant : <strong>VT_I4</strong><br/> Valeur par défaut : 0<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_DescribedByPropertyId"></span><span id="uia_describedbypropertyid"></span><span id="UIA_DESCRIBEDBYPROPERTYID"></span><dl> <dt><strong>UIA_DescribedByPropertyId</strong></dt> <dt>30105</dt> </dl></td>
<td >Identifie la propriété <strong>DescribedBy</strong> , qui est un tableau d’éléments qui fournissent plus d’informations sur l’élément Automation.<br/> <strong>DescribedBy</strong> est utilisé lorsqu’un élément Automation est expliqué par un autre segment de l’interface utilisateur de l’application. Par exemple, la propriété peut pointer vers un élément de texte de &quot; 2 529 éléments dans 85 groupes, 10 éléments sélectionnés &quot; à partir d’un objet de liste personnalisée complexe. Au lieu d’utiliser le modèle objet pour les clients afin de condenser des informations similaires, la propriété <strong>DescribedBy</strong> peut offrir un accès rapide à l’élément d’interface utilisateur qui peut déjà offrir des informations utiles à l’utilisateur final qui décrivent l’élément d’interface utilisateur.<br/> Type Variant pour les fournisseurs : <strong>VT_UNKNOWN</strong>  |  <strong>VT_ARRAY</strong><br/> Type Variant pour les clients : <strong>VT_UNKNOWN</strong> (<a href="/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray"><strong>IUIAutomationElementArray</strong></a>)<br/> Valeur par défaut : tableau vide<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_FillColorPropertyId"></span><span id="uia_fillcolorpropertyid"></span><span id="UIA_FILLCOLORPROPERTYID"></span><dl> <dt><strong>UIA_FillColorPropertyId</strong></dt> <dt>30160</dt> </dl></td>
<td >Identifie la propriété <strong>FillColor</strong> , qui spécifie la couleur utilisée pour remplir l’élément Automation. Cet attribut est spécifié en tant que COLORREF, valeur 32 bits utilisée pour spécifier une couleur RVB ou RVBA.<br/> Type Variant : <strong>VT_I4</strong><br/> Valeur par défaut : 0<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_FillTypePropertyId"></span><span id="uia_filltypepropertyid"></span><span id="UIA_FILLTYPEPROPERTYID"></span><dl> <dt><strong>UIA_FillTypePropertyId</strong></dt> <dt>30162</dt> </dl></td>
<td >Identifie la propriété <strong>fillType</strong> , qui spécifie le modèle utilisé pour remplir l’élément Automation, tel que None, Color, gradient, image, pattern, et ainsi de suite.<br/> Type Variant : <strong>VT_I4</strong><br/> Valeur par défaut : 0<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_FlowsFromPropertyId"></span><span id="uia_flowsfrompropertyid"></span><span id="UIA_FLOWSFROMPROPERTYID"></span><dl> <dt><strong>UIA_FlowsFromPropertyId</strong></dt> <dt>30148</dt> </dl></td>
<td >Identifie la propriété <strong>FlowsFrom</strong> , qui est un tableau d’éléments Automation qui suggère l’ordre de lecture avant l’élément Automation actuel. Pris en charge à partir de Windows 8.<br/> La propriété <strong>FlowsFrom</strong> spécifie l’ordre de lecture lorsque les éléments Automation ne sont pas exposés ou structurés dans le même ordre de lecture que celui perçu par l’utilisateur. Alors que la propriété <strong>FlowsFrom</strong> peut spécifier plusieurs éléments précédents, elle contient généralement uniquement l’élément précédent dans l’ordre de lecture.<br/> Type Variant pour les fournisseurs : <strong>VT_UNKNOWN</strong>  |  <strong>VT_ARRAY</strong><br/> Type Variant pour les clients : <strong>VT_UNKNOWN</strong> (<a href="/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray"><strong>IUIAutomationElementArray</strong></a>)<br/> Valeur par défaut : tableau vide<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_FlowsToPropertyId"></span><span id="uia_flowstopropertyid"></span><span id="UIA_FLOWSTOPROPERTYID"></span><dl> <dt><strong>UIA_FlowsToPropertyId</strong></dt> <dt>30106</dt> </dl></td>
<td >Identifie la propriété <strong>FlowsTo</strong> , qui est un tableau d’éléments Automation qui suggère l’ordre de lecture après l’élément Automation actuel.<br/> La propriété <strong>FlowsTo</strong> spécifie l’ordre de lecture lorsque les éléments Automation ne sont pas exposés ou structurés dans le même ordre de lecture que celui perçu par l’utilisateur. Alors que la propriété <strong>FlowsTo</strong> peut spécifier plusieurs éléments suivants, elle contient généralement uniquement l’élément suivant dans l’ordre de lecture.<br/> Type Variant pour les fournisseurs : <strong>VT_UNKNOWN</strong>  |  <strong>VT_ARRAY</strong><br/> Type Variant pour les clients : <strong>VT_UNKNOWN</strong> (<a href="/windows/desktop/api/UIAutomationClient/nn-uiautomationclient-iuiautomationelementarray"><strong>IUIAutomationElementArray</strong></a>)<br/> Valeur par défaut : tableau vide<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_FrameworkIdPropertyId"></span><span id="uia_frameworkidpropertyid"></span><span id="UIA_FRAMEWORKIDPROPERTYID"></span><dl> <dt><strong>UIA_FrameworkIdPropertyId</strong></dt> <dt>30024</dt> </dl></td>
<td >Identifie la propriété <strong>FrameworkId</strong> , qui est une chaîne contenant le nom de l’infrastructure d’interface utilisateur sous-jacente à laquelle l’élément Automation appartient.<br/> Le <strong>FrameworkId</strong> permet aux applications clientes de traiter les éléments d’automatisation différemment en fonction de l’infrastructure d’interface utilisateur particulière. Les exemples de valeurs de propriété incluent &quot; Win32 &quot; , &quot; WinForm &quot; et &quot; directui &quot; .<br/> Type Variant : <strong>VT_BSTR</strong><br/> Valeur par défaut : chaîne vide<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_FullDescriptionPropertyId"></span><span id="uia_fulldescriptionpropertyid"></span><span id="UIA_FULLDESCRIPTIONPROPERTYID"></span><dl> <dt><strong>UIA_FullDescriptionPropertyId</strong></dt> <dt>30159</dt> </dl></td>
<td >La propriété <strong>FullDescription</strong> expose une chaîne localisée qui peut contenir un texte de description étendu pour un élément. <strong>FullDescription</strong> peut contenir une description plus complète d’un élément que celle qui peut être appropriée pour le <strong>nom</strong>de l’élément.<br/> Type Variant : <strong>VT_BSTR</strong><br/> Valeur par défaut : chaîne vide<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_HasKeyboardFocusPropertyId"></span><span id="uia_haskeyboardfocuspropertyid"></span><span id="UIA_HASKEYBOARDFOCUSPROPERTYID"></span><dl> <dt><strong>UIA_HasKeyboardFocusPropertyId</strong></dt> <dt>30008</dt> </dl></td>
<td >Identifie la propriété <strong>HasKeyboardFocus</strong> , qui est une valeur booléenne qui indique si l’élément Automation a le focus clavier.<br/> Type Variant : <strong>VT_BOOL</strong><br/> Valeur par défaut : <strong>false</strong><br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_HeadingLevelPropertyId"></span><span id="uia_headinglevelpropertyid"></span><span id="UIA_HEADINGLEVELPROPERTYID"></span><dl> <dt><strong>UIA_HeadingLevelPropertyId</strong></dt> <dt>30173</dt> </dl></td>
<td >Identifie la propriété <strong>HeadingLevel</strong> , qui indique le niveau de titre d’un élément UI Automation.<br/> Type Variant : <strong>VT_I4</strong><br/> Valeur par défaut : <strong>HeadingLevel_None</strong><br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_HelpTextPropertyId"></span><span id="uia_helptextpropertyid"></span><span id="UIA_HELPTEXTPROPERTYID"></span><dl> <dt><strong>UIA_HelpTextPropertyId</strong></dt> <dt>30013</dt> </dl></td>
<td >Identifie la propriété <strong>HelpText</strong> , qui est une chaîne de texte d’aide associée à l’élément Automation.<br/> La propriété <strong>HelpText</strong> peut être prise en charge avec le texte de l’espace réservé apparaissant dans les contrôles d’édition ou de liste. Par exemple, &quot; tapez le texte ici pour &quot; la recherche est un bon candidat à la propriété <strong>HelpText</strong> pour un contrôle d’édition qui place le texte avant l’entrée réelle de l’utilisateur. Toutefois, il n’est pas approprié pour la propriété Name du contrôle Edit.<br/> Quand <strong>HelpText</strong> est pris en charge, la chaîne doit correspondre à la langue de l’interface utilisateur de l’application ou à la langue d’interface utilisateur par défaut du système d’exploitation.<br/> Type Variant : <strong>VT_BSTR</strong><br/> Valeur par défaut : chaîne vide<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_IsContentElementPropertyId"></span><span id="uia_iscontentelementpropertyid"></span><span id="UIA_ISCONTENTELEMENTPROPERTYID"></span><dl> <dt><strong>UIA_IsContentElementPropertyId</strong></dt> <dt>30017</dt> </dl></td>
<td >Identifie la propriété <strong>IsContentElement</strong> , qui est une valeur booléenne qui spécifie si l’élément apparaît dans l’affichage de contenu de l’arborescence des éléments Automation. Pour plus d’informations, consultez <a href="uiauto-treeoverview.md">UI Automation Tree Overview</a>.<br/>
<blockquote>
[!Note]<br />
Pour qu’un élément apparaisse dans l’affichage de contenu, la propriété <strong>IsContentElement</strong> et la propriété <strong>IsControlElement</strong> doivent avoir la <strong>valeur true</strong>.
</blockquote>
<br/> <br/> Type Variant : <strong>VT_BOOL</strong><br/> Valeur par défaut : <strong>true</strong><br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_IsControlElementPropertyId"></span><span id="uia_iscontrolelementpropertyid"></span><span id="UIA_ISCONTROLELEMENTPROPERTYID"></span><dl> <dt><strong>UIA_IsControlElementPropertyId</strong></dt> <dt>30016</dt> </dl></td>
<td >Identifie la propriété <strong>IsControlElement</strong> , qui est une valeur booléenne qui spécifie si l’élément apparaît dans la vue de contrôle de l’arborescence des éléments Automation. Pour plus d’informations, consultez <a href="uiauto-treeoverview.md">UI Automation Tree Overview</a>.<br/> Type Variant : <strong>VT_BOOL</strong><br/> Valeur par défaut : <strong>true</strong><br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_IsDataValidForFormPropertyId"></span><span id="uia_isdatavalidforformpropertyid"></span><span id="UIA_ISDATAVALIDFORFORMPROPERTYID"></span><dl> <dt><strong>UIA_IsDataValidForFormPropertyId</strong></dt> <dt>30103</dt> </dl></td>
<td >Identifie la propriété <strong>IsDataValidForForm</strong> , qui est une valeur booléenne qui indique si la valeur entrée ou sélectionnée est valide pour la règle de formulaire associée à l’élément Automation. Par exemple, si l’utilisateur &quot; a entré 425-555-5555 &quot; pour un champ Code postal qui requiert 5 ou 9 chiffres, la propriété <strong>IsDataValidForForm</strong> peut avoir la valeur <strong>false</strong> pour indiquer que les données ne sont pas valides.<br/> Type Variant : <strong>VT_BOOL</strong><br/> Valeur par défaut : <strong>false</strong><br/></td>
</tr>

<tr class="odd">
<td ><span id="UIA_IsDialogPropertyId"></span><span id="uia_isdialogpropertyid"></span><span id="UIA_ISDIALOGPROPERTYID"></span><dl> <dt><strong>UIA_IsDialogPropertyId</strong></dt> <dt>30174</dt> </dl></td>
<td >Identifie la propriété <strong>IsDialog</strong> , qui est une valeur booléenne qui indique si l’élément Automation est une fenêtre de boîte de dialogue. Par exemple, les technologies d’assistance comme les lecteurs d’écran parlent généralement le titre de la boîte de dialogue, le contrôle ayant le focus dans la boîte de dialogue, puis le contenu de la boîte de dialogue jusqu’au contrôle ayant le focus (voulez &quot; -vous enregistrer vos modifications avant de fermer &quot; ). Pour les fenêtres standard, un lecteur d’écran parle généralement le titre de la fenêtre, suivi du contrôle ayant le focus. La propriété <strong>IsDialog</strong> peut avoir la valeur <strong>true</strong> pour indiquer que l’application cliente doit traiter l’élément comme une fenêtre de dialogue.<br/> Type Variant : <strong>VT_BOOL</strong><br/> Valeur par défaut : <strong>false</strong><br/></td>
</tr>

<tr class="even">
<td ><span id="UIA_IsEnabledPropertyId"></span><span id="uia_isenabledpropertyid"></span><span id="UIA_ISENABLEDPROPERTYID"></span><dl> <dt><strong>UIA_IsEnabledPropertyId</strong></dt> <dt>30010</dt> </dl></td>
<td >Identifie la propriété <strong>IsEnabled</strong> , qui est une valeur booléenne qui indique si l’élément d’interface utilisateur référencé par l’élément Automation est activé et peut être interagi avec.<br/> Lorsque l’état activé d’un contrôle a la <strong>valeur false</strong>, il est supposé que les contrôles enfants ne sont pas activés. Les clients ne doivent pas s’attendre à des événements de modification de propriété à partir d’éléments enfants lorsque l’état du contrôle parent change.<br/> Type Variant : <strong>VT_BOOL</strong><br/> Valeur par défaut : <strong>false</strong><br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_IsKeyboardFocusablePropertyId"></span><span id="uia_iskeyboardfocusablepropertyid"></span><span id="UIA_ISKEYBOARDFOCUSABLEPROPERTYID"></span><dl> <dt><strong>UIA_IsKeyboardFocusablePropertyId</strong></dt> <dt>30009</dt> </dl></td>
<td >Identifie la propriété <strong>IsKeyboardFocusable</strong> , qui est une valeur booléenne qui indique si l’élément Automation peut accepter le focus clavier.<br/> Type Variant : <strong>VT_BOOL</strong><br/> Valeur par défaut : <strong>false</strong><br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_IsOffscreenPropertyId"></span><span id="uia_isoffscreenpropertyid"></span><span id="UIA_ISOFFSCREENPROPERTYID"></span><dl> <dt><strong>UIA_IsOffscreenPropertyId</strong></dt> <dt>30022</dt> </dl></td>
<td >Identifie la propriété <strong>IsOffscreen</strong> , qui est une valeur booléenne qui indique si l’élément Automation est entièrement défilant de l’affichage (par exemple, un élément d’une zone de liste qui se trouve en dehors de la fenêtre d’affichage de l’objet conteneur) ou s’il est réduit hors de l’affichage (par exemple, un élément dans une arborescence ou un menu ou dans une fenêtre réduite). Si l’élément a un point de clic qui peut provoquer le focus, l’élément est considéré comme étant à l’écran alors qu’une partie de l’élément est hors écran.<br/> La valeur de la propriété n’est pas affectée par l’occlusion par d’autres fenêtres ou si l’élément est visible sur une analyse spécifique.<br/> Si la propriété <strong>IsOffscreen</strong> a la <strong>valeur true</strong>, l’élément d’interface utilisateur est défilant hors de l’écran ou réduit. L’élément est temporairement masqué, mais il reste dans la perception de l’utilisateur final et continue à être inclus dans le modèle d’interface utilisateur. L’objet peut être rétabli en mode de défilement, en cliquant sur une liste déroulante, et ainsi de suite.<br/> Les objets que l’utilisateur final ne perçoivent pas du tout, ou qui sont &quot; masqués par programmation &quot; (par exemple, une boîte de dialogue qui a été fermée, mais l’objet sous-jacent est toujours mis en cache par l’application) ne doivent pas figurer dans l’arborescence des éléments Automation (au lieu de définir l’état de <strong>IsOffscreen</strong> sur <strong>true</strong>).<br/> Type Variant : <strong>VT_BOOL</strong><br/> Valeur par défaut : <strong>false</strong><br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_IsPasswordPropertyId"></span><span id="uia_ispasswordpropertyid"></span><span id="UIA_ISPASSWORDPROPERTYID"></span><dl> <dt><strong>UIA_IsPasswordPropertyId</strong></dt> <dt>30019</dt> </dl></td>
<td >Identifie la propriété <strong>IsPassword</strong> , qui est une valeur booléenne qui indique si l’élément Automation contient du contenu protégé ou un mot de passe.<br/> Lorsque la propriété <strong>IsPassword</strong> a la <strong>valeur true</strong> et que l’élément a le focus clavier, une application cliente doit désactiver l’écho du clavier ou les commentaires d’entrée au clavier qui peuvent exposer les informations protégées de l’utilisateur. Toute tentative d’accès à la propriété <strong>value</strong> de l’élément protégé (contrôle d’édition) peut provoquer une erreur.<br/> Type Variant : <strong>VT_BOOL</strong><br/> Valeur par défaut : <strong>false</strong><br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_IsPeripheralPropertyId"></span><span id="uia_isperipheralpropertyid"></span><span id="UIA_ISPERIPHERALPROPERTYID"></span><dl> <dt><strong>UIA_IsPeripheralPropertyId</strong></dt> <dt>30150</dt> </dl></td>
<td >Identifie la propriété <strong>IsPeripheral</strong> , qui est une valeur booléenne qui indique si l’élément Automation représente l’interface utilisateur périphérique. L’interface utilisateur du périphérique apparaît et prend en charge l’interaction de l’utilisateur, mais ne prend pas le focus clavier lorsqu’il apparaît. Les fenêtres contextuelles, les lanceurs, les menus contextuels ou les notifications flottantes sont des exemples d’interface utilisateur. Pris en charge à partir de Windows 8.1.<br/> Lorsque la propriété <strong>IsPeripheral</strong> a la <strong>valeur true</strong>, une application cliente ne peut pas supposer que le focus a été pris par l’élément même s’il est actuellement interactif au clavier.<br/> Cette propriété s’applique à ces types de contrôles :<br/>
<ul>
<li><strong>UIA_GroupControlTypeId</strong></li>
<li><strong>UIA_MenuControlTypeId</strong></li>
<li><strong>UIA_PaneControlTypeId</strong></li>
<li><strong>UIA_ToolBarControlTypeId</strong></li>
<li><strong>UIA_ToolTipControlTypeId</strong></li>
<li><strong>UIA_WindowControlTypeId</strong></li>
<li><strong>UIA_CustomControlTypeId</strong></li>
</ul>
Type Variant : <strong>VT_BOOL</strong><br/> Valeur par défaut : <strong>false</strong><br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_IsRequiredForFormPropertyId"></span><span id="uia_isrequiredforformpropertyid"></span><span id="UIA_ISREQUIREDFORFORMPROPERTYID"></span><dl> <dt><strong>UIA_IsRequiredForFormPropertyId</strong></dt> <dt>30025</dt> </dl></td>
<td >Identifie la propriété <strong>IsRequiredForForm</strong> , qui est une valeur booléenne qui indique si l’élément Automation doit obligatoirement être renseigné sur un formulaire.<br/> Type Variant : <strong>VT_BOOL</strong><br/> Valeur par défaut : <strong>false</strong><br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_ItemStatusPropertyId"></span><span id="uia_itemstatuspropertyid"></span><span id="UIA_ITEMSTATUSPROPERTYID"></span><dl> <dt><strong>UIA_ItemStatusPropertyId</strong></dt> <dt>30026</dt> </dl></td>
<td >Identifie la propriété <strong>ItemStatus</strong> , qui est une chaîne de texte décrivant l’état d’un élément de l’élément Automation.<br/> <strong>ItemStatus</strong> permet à un client de déterminer si un élément communique l’état d’un élément, ainsi que l’État. Par exemple, un élément associé à un contact dans une application de messagerie peut être &quot; occupé &quot; ou &quot; connecté &quot; .<br/> Lorsque <strong>ItemStatus</strong> est pris en charge, la chaîne doit correspondre à la langue de l’interface utilisateur de l’application ou à la langue d’interface utilisateur par défaut du système d’exploitation.<br/> Type Variant : <strong>VT_BSTR</strong><br/> Valeur par défaut : chaîne vide<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_ItemTypePropertyId"></span><span id="uia_itemtypepropertyid"></span><span id="UIA_ITEMTYPEPROPERTYID"></span><dl> <dt><strong>UIA_ItemTypePropertyId</strong></dt> <dt>300021</dt> </dl></td>
<td >Identifie la propriété <strong>ItemType</strong> , qui est une chaîne de texte décrivant le type de l’élément Automation.<br/> <strong>ItemType</strong> est utilisé pour obtenir des informations sur les éléments d’une liste, d’une arborescence ou d’une grille de données. Par exemple, un élément d’une vue de répertoire de fichiers peut être un &quot; fichier de document &quot; ou un &quot; dossier &quot; .<br/> Quand <strong>ItemType</strong> est pris en charge, la chaîne doit correspondre à la langue de l’interface utilisateur de l’application ou à la langue d’interface utilisateur par défaut du système d’exploitation.<br/> Type Variant : <strong>VT_BSTR</strong><br/> Valeur par défaut : chaîne vide<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_LabeledByPropertyId"></span><span id="uia_labeledbypropertyid"></span><span id="UIA_LABELEDBYPROPERTYID"></span><dl> <dt><strong>UIA_LabeledByPropertyId</strong></dt> <dt>30018</dt> </dl></td>
<td >Identifie la propriété <strong>LabeledBy</strong> , qui est un élément Automation qui contient l’étiquette de texte pour cet élément.<br/> Cette propriété peut être utilisée pour récupérer, par exemple, l’étiquette de texte statique pour une zone de liste déroulante.<br/> Type Variant : <strong>VT_UNKNOWN</strong><br/> Valeur par défaut : <strong>null</strong><br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_LandmarkTypePropertyId"></span><span id="uia_landmarktypepropertyid"></span><span id="UIA_LANDMARKTYPEPROPERTYID"></span><dl> <dt><strong>UIA_LandmarkTypePropertyId</strong></dt> <dt>30157</dt> </dl></td>
<td >Identifie la propriété <strong>LandmarkType</strong> , qui est un <a href="landmark-type-identifiers.md"><strong>identificateur de type repère</strong></a> associé à un élément.<br/> La propriété <strong>LandmarkType</strong> décrit un élément qui représente un groupe d’éléments. Par exemple, un repère de recherche peut représenter un ensemble de contrôles associés pour la recherche.<br/> Si <a href="landmark-type-identifiers.md"><strong>UIA_CustomLandmarkTypeId</strong></a> est utilisé, <strong>UIA_LocalizedLandmarkTypePropertyId</strong> est requis pour décrire le repère personnalisé.<br/> Type Variant : <strong>VT_I4</strong><br/> Valeur par défaut : 0<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_LevelPropertyId"></span><span id="uia_levelpropertyid"></span><span id="UIA_LEVELPROPERTYID"></span><dl> <dt><strong>UIA_LevelPropertyId</strong></dt> <dt>30154</dt> </dl></td>
<td >Identifie la propriété de <strong>niveau</strong> , qui est un entier de base 1 associé à un élément Automation.<br/> La propriété <strong>Level</strong> décrit l’emplacement d’un élément à l’intérieur d’une structure hiérarchique ou de structures hiérarchiques rompues. Par exemple, une liste à puces/numérotées, des en-têtes ou d’autres éléments de données structurées peuvent avoir plusieurs relations parent/enfant. Le <strong>niveau</strong> décrit l’emplacement de l’élément dans la structure.<br/> Il est recommandé d’utiliser le <a href="/windows/desktop/WinAuto/uiauto-implementingcustomnavigation">modèle de contrôle CustomNavigation</a> en tandem avec <strong>Level</strong>.<br/> Type Variant : <strong>VT_I4</strong><br/> Valeur par défaut : 0<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_LiveSettingPropertyId"></span><span id="uia_livesettingpropertyid"></span><span id="UIA_LIVESETTINGPROPERTYID"></span><dl> <dt><strong>UIA_LiveSettingPropertyId</strong></dt> <dt>30135</dt> </dl></td>
<td >Identifie la propriété <strong>LiveSetting</strong> , qui est prise en charge par un élément Automation qui représente une zone dynamique. La propriété <strong>LiveSetting</strong> indique le &quot; niveau de poli &quot; qu’un client doit utiliser pour informer l’utilisateur des modifications apportées à la zone dynamique. Cette propriété peut être l’une des valeurs de l’énumération <a href="/windows/desktop/api/uiautomationcore/ne-uiautomationcore-livesetting"><strong>LiveSetting</strong></a> . Pris en charge à partir de Windows 8.<br/> Type Variant : <strong>VT_I4</strong><br/> Valeur par défaut : 0<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_LocalizedControlTypePropertyId"></span><span id="uia_localizedcontroltypepropertyid"></span><span id="UIA_LOCALIZEDCONTROLTYPEPROPERTYID"></span><dl> <dt><strong>UIA_LocalizedControlTypePropertyId</strong></dt> <dt>30004</dt> </dl></td>
<td >Identifie la propriété <strong>LocalizedControlType</strong> , qui est une chaîne de texte décrivant le type de contrôle représenté par l’élément Automation. La chaîne ne doit contenir que des caractères minuscules :
<ul>
<li>Correct : &quot; bouton&quot;</li>
<li>Incorrect : &quot; Button&quot;</li>
</ul>
<br/> Quand <strong>LocalizedControlType</strong> n’est pas spécifié par le fournisseur d’éléments, la chaîne localisée par défaut est fournie par l’infrastructure, en fonction du type de contrôle de l’élément (par exemple, &quot; Button &quot; pour le type de contrôle <a href="uiauto-supportbuttoncontroltype.md">Button</a> ). Un élément Automation avec le type de contrôle <strong>personnalisé</strong> doit prendre en charge une chaîne de type de contrôle localisée qui représente le rôle de l’élément (par exemple, un &quot; Sélecteur &quot; de couleurs pour un contrôle personnalisé qui permet aux utilisateurs de choisir et de spécifier des couleurs).<br/> Quand une valeur personnalisée est fournie, la chaîne doit correspondre à la langue de l’interface utilisateur de l’application ou à la langue de l’interface utilisateur par défaut du système d’exploitation.<br/> Type Variant : <strong>VT_BSTR</strong><br/> Valeur par défaut : chaîne vide<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_LocalizedLandmarkTypePropertyId"></span><span id="uia_localizedlandmarktypepropertyid"></span><span id="UIA_LOCALIZEDLANDMARKTYPEPROPERTYID"></span><dl> <dt><strong>UIA_LocalizedLandmarkTypePropertyId</strong></dt> <dt>30158</dt> </dl></td>
<td >Identifie le <strong>LocalizedLandmarkType</strong>, qui est une chaîne de texte décrivant le type d’élément géographique représenté par l’élément Automation.<br/> Cela doit être utilisé en tandem avec <a href="landmark-type-identifiers.md"><strong>UIA_CustomLandmarkTypeId</strong></a> Toutefois, <strong>LocalizedLandmarkType</strong> doit toujours avoir la priorité sur <strong>LandmarkType</strong> et être utilisé pour décrire le repère avant <strong>LandmarkType</strong>.<br/> La chaîne doit correspondre à la langue de l’interface utilisateur de l’application ou à la langue de l’interface utilisateur par défaut du système d’exploitation.<br/> Type Variant : <strong>VT_BSTR</strong><br/> Valeur par défaut : chaîne vide<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_NamePropertyId"></span><span id="uia_namepropertyid"></span><span id="UIA_NAMEPROPERTYID"></span><dl> <dt><strong>UIA_NamePropertyId</strong></dt> <dt>30005</dt> </dl></td>
<td >Identifie la propriété <strong>Name</strong> , qui est une chaîne qui contient le nom de l’élément Automation.<br/> La propriété <strong>Name</strong> doit être la même que le texte de l’étiquette à l’écran. Par exemple, le <strong>nom</strong> doit être &quot; Rechercher &quot; un élément Button avec l’étiquette &quot; Browse &quot; . La propriété <strong>Name</strong> ne doit pas inclure le caractère mnémonique pour les touches d’accès (autrement dit, &quot; & &quot; ), qui est souligné dans la présentation texte de l’interface utilisateur. En outre, la propriété <strong>Name</strong> ne doit pas être une version étendue ou modifiée de l’étiquette à l’écran, car l’incohérence entre le nom et l’étiquette peut entraîner une confusion entre les utilisateurs et les applications clientes.<br/> Lorsque le texte de l’étiquette correspondant n’est pas visible à l’écran ou lorsqu’il est remplacé par des graphiques, vous devez choisir le texte de remplacement. Le texte de remplacement doit être concis, intuitif et localisé dans la langue de l’interface utilisateur de l’application, ou dans la langue de l’interface utilisateur par défaut du système d’exploitation. Le texte de remplacement ne doit pas être une description détaillée des détails visuels, mais une description concise de la fonction ou de la fonctionnalité de l’interface utilisateur comme si elle était étiquetée par du texte simple. par exemple, le bouton menu Démarrer Windows s’intitule &quot; démarrer &quot; (bouton) au lieu de &quot; Windows Logo dans le bouton bleu round sphere graphics &quot; (button). Pour plus d’informations, consultez <a href="/previous-versions/windows/desktop/dnacc/creating-text-equivalents-for-images">création d’équivalents de texte pour les images</a>.<br/> Quand une étiquette d’interface utilisateur utilise des graphiques de texte (par exemple, à l’aide &quot; >> &quot; d’un bouton qui ajoute un élément de gauche à droite), la propriété <strong>Name</strong> doit être remplacée par une alternative textuelle appropriée (par exemple, &quot; Add &quot; ). Toutefois, la pratique consistant à utiliser des graphiques de texte comme étiquette d’interface utilisateur est déconseillée en raison des problèmes de localisation et d’accessibilité.<br/> La propriété <strong>Name</strong> ne doit pas inclure les informations de rôle ou de type de contrôle, telles que &quot; Button &quot; ou &quot; List &quot; ; sinon, elle est en conflit avec le texte de la propriété <strong>LocalizedControlType</strong> lorsque ces deux propriétés sont ajoutées (de nombreuses technologies d’assistance existantes le font).<br/> La propriété <strong>Name</strong> ne peut pas être utilisée en tant qu’identificateur unique parmi les frères. Toutefois, tant qu’il est cohérent avec la présentation de l’interface utilisateur, la même valeur de <strong>nom</strong> peut être prise en charge parmi les homologues. Pour l’automatisation des tests, les clients doivent envisager d’utiliser la propriété <strong>AutomationId</strong> ou <strong>RuntimeId</strong> .<br/> Les contrôles de texte n’ont pas toujours la même propriété <strong>Name</strong> que le texte affiché dans le contrôle, tant que le modèle de <strong>texte</strong> est également pris en charge.<br/> Type Variant : <strong>VT_BSTR</strong><br/> Valeur par défaut : chaîne vide<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_NativeWindowHandlePropertyId"></span><span id="uia_nativewindowhandlepropertyid"></span><span id="UIA_NATIVEWINDOWHANDLEPROPERTYID"></span><dl> <dt><strong>UIA_NativeWindowHandlePropertyId</strong></dt> <dt>30020</dt> </dl></td>
<td >Identifie la propriété <strong>NativeWindowHandle</strong> , qui est un entier qui représente le handle (<strong>HWND</strong>) de la fenêtre de l’élément Automation, le cas échéant ; dans le cas contraire, cette propriété a la valeur 0.<br/> Type Variant : <strong>VT_I4</strong><br/> Valeur par défaut : 0<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_OptimizeForVisualContentPropertyId"></span><span id="uia_optimizeforvisualcontentpropertyid"></span><span id="UIA_OPTIMIZEFORVISUALCONTENTPROPERTYID"></span><dl> <dt><strong>UIA_OptimizeForVisualContentPropertyId</strong></dt> <dt>30111</dt> </dl></td>
<td >Identifie la propriété <strong>OptimizeForVisualContent</strong> , qui est une valeur booléenne qui indique si le fournisseur expose uniquement les éléments qui sont visibles. Un fournisseur peut utiliser cette propriété pour optimiser les performances lors de l’utilisation de très grands éléments de contenu. Par exemple, à mesure que l’utilisateur parcourt une grande partie du contenu, le fournisseur peut détruire les éléments de contenu qui ne sont plus visibles. Lorsqu’un élément de contenu est détruit, le fournisseur doit retourner le <strong>UIA_E_ELEMENTNOTAVAILABLE</strong> code d’erreur. Pris en charge à partir de Windows 8.<br/> Type Variant : <strong>VT_BOOL</strong><br/> Valeur par défaut : <strong>false</strong><br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_OrientationPropertyId"></span><span id="uia_orientationpropertyid"></span><span id="UIA_ORIENTATIONPROPERTYID"></span><dl> <dt><strong>UIA_OrientationPropertyId</strong></dt> <dt>300023</dt> </dl></td>
<td >Identifie la propriété d' <strong>orientation</strong> , qui indique l’orientation du contrôle représenté par l’élément Automation. La propriété est exprimée sous la forme d’une valeur du type énuméré <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-orientationtype"><strong>OrientationType</strong></a> .<br/> La propriété <strong>orientation</strong> est prise en charge par les contrôles, tels que les barres de défilement et les curseurs, qui peuvent avoir une orientation verticale ou horizontale. Dans le cas contraire, il peut toujours être <a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-orientationtype"><strong>OrientationType_None</strong></a>, ce qui signifie que le contrôle n’a pas d’orientation.<br/> Type Variant : <strong>VT_I4</strong><br/> Valeur par défaut : 0 (<a href="/windows/desktop/api/UIAutomationCore/ne-uiautomationcore-orientationtype"><strong>OrientationType_None</strong></a>)<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_OutlineColorPropertyId"></span><span id="uia_outlinecolorpropertyid"></span><span id="UIA_OUTLINECOLORPROPERTYID"></span><dl> <dt><strong>UIA_OutlineColorPropertyId</strong></dt> <dt>30161</dt> </dl></td>
<td >Identifie la propriété <strong>OutlineColor</strong> , qui spécifie la couleur utilisée pour le contour de l’élément Automation. Cet attribut est spécifié en tant que <strong>COLORREF</strong>, valeur 32 bits utilisée pour spécifier une couleur RVB ou RVBA.<br/> Type Variant : <strong>VT_I4</strong>  |  <strong>VT_ARRAY</strong><br/> Valeur par défaut : 0<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_OutlineThicknessPropertyId"></span><span id="uia_outlinethicknesspropertyid"></span><span id="UIA_OUTLINETHICKNESSPROPERTYID"></span><dl> <dt><strong>UIA_OutlineThicknessPropertyId</strong></dt> <dt>30164</dt> </dl></td>
<td >Identifie la propriété <strong>OutlineThickness</strong> , qui spécifie la largeur du contour de l’élément Automation.<br/> Type Variant : <strong>VT_R8</strong>  |  <strong>VT_ARRAY</strong><br/> Valeur par défaut : <strong>VT_EMPTY</strong><br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_PositionInSetPropertyId"></span><span id="uia_positioninsetpropertyid"></span><span id="UIA_POSITIONINSETPROPERTYID"></span><dl> <dt><strong>UIA_PositionInSetPropertyId</strong></dt> <dt>30152</dt> </dl></td>
<td >Identifie la propriété <strong>PositionInSet</strong> , qui est un entier de base 1 associé à un élément Automation. <strong>PositionInSet</strong> décrit l’emplacement ordinal de l’élément dans un ensemble d’éléments qui sont considérés comme des frères.<br/> <strong>PositionInSet</strong> fonctionne en coordination avec la propriété <strong>SizeOfSet</strong> pour décrire l’emplacement ordinal dans le jeu.<br/> Type Variant : <strong>VT_I4</strong><br/> Valeur par défaut : 0<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_ProcessIdPropertyId"></span><span id="uia_processidpropertyid"></span><span id="UIA_PROCESSIDPROPERTYID"></span><dl> <dt><strong>UIA_ProcessIdPropertyId</strong></dt> <dt>30002</dt> </dl></td>
<td >Identifie la propriété <strong>ProcessID</strong> , qui est un entier représentant l’identificateur de processus (ID) de l’élément Automation.<br/> L’identificateur de processus (ID) est assigné par le système d’exploitation. Vous pouvez le voir dans la colonne <strong>PID</strong> de l’onglet <strong>processus</strong> du gestionnaire des tâches.<br/> Type Variant : <strong>VT_I4</strong><br/> Valeur par défaut : 0<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_ProviderDescriptionPropertyId"></span><span id="uia_providerdescriptionpropertyid"></span><span id="UIA_PROVIDERDESCRIPTIONPROPERTYID"></span><dl> <dt><strong>UIA_ProviderDescriptionPropertyId</strong></dt> <dt>30107</dt> </dl></td>
<td >Identifie la propriété <strong>ProviderDescription</strong> , qui est une chaîne mise en forme contenant les informations sources du fournisseur UI Automation pour l’élément Automation, y compris les informations de proxy.<br/> Type Variant : <strong>VT_BSTR</strong><br/> Valeur par défaut : chaîne vide<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_RotationPropertyId"></span><span id="uia_rotationpropertyid"></span><span id="UIA_ROTATIONPROPERTYID"></span><dl> <dt><strong>UIA_RotationPropertyId</strong></dt> <dt>30166</dt> </dl></td>
<td >Identifie la propriété de <strong>rotation</strong> , qui spécifie l’angle de rotation en unités non spécifiées.<br/> Type Variant : <strong>VT_R8</strong><br/> Valeur par défaut : 0<br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_RuntimeIdPropertyId"></span><span id="uia_runtimeidpropertyid"></span><span id="UIA_RUNTIMEIDPROPERTYID"></span><dl> <dt><strong>UIA_RuntimeIdPropertyId</strong></dt> <dt>30000</dt> </dl></td>
<td >Identifie la propriété <strong>RuntimeId</strong> , qui est un tableau d’entiers représentant l’identificateur d’un élément Automation.<br/> L’identificateur est unique sur le bureau, mais il est garanti qu’il est unique dans l’interface utilisateur du Bureau sur lequel il a été généré. Les identificateurs peuvent être réutilisés au fil du temps.<br/> Le format de <strong>RuntimeId</strong> peut changer. L’identificateur retourné doit être traité comme une valeur opaque et utilisé uniquement pour la comparaison ; par exemple, pour déterminer si un élément Automation se trouve dans le cache.<br/> Type Variant : <strong>VT_I4</strong>  |  <strong>VT_ARRAY</strong><br/> Valeur par défaut : <strong>VT_EMPTY</strong><br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_SizePropertyId"></span><span id="uia_sizepropertyid"></span><span id="UIA_SIZEPROPERTYID"></span><dl> <dt><strong>UIA_SizePropertyId</strong></dt> <dt>30167</dt> </dl></td>
<td >Identifie la propriété <strong>Size</strong> , qui spécifie la largeur et la hauteur de l’élément Automation.<br/> Type Variant : <strong>VT_R8</strong>  |  <strong>VT_ARRAY</strong><br/> Valeur par défaut : <strong>VT_EMPTY</strong><br/></td>
</tr>
<tr class="even">
<td ><span id="UIA_SizeOfSetPropertyId"></span><span id="uia_sizeofsetpropertyid"></span><span id="UIA_SIZEOFSETPROPERTYID"></span><dl> <dt><strong>UIA_SizeOfSetPropertyId</strong></dt> <dt>30153</dt> </dl></td>
<td >Identifie la propriété <strong>SizeOfSet</strong> , qui est un entier de base 1 associé à un élément Automation. <strong>SizeOfSet</strong> décrit le nombre d’éléments Automation d’un groupe ou d’un ensemble qui sont considérés comme des frères.<br/> <strong>SizeOfSet</strong> fonctionne en coordination avec la propriété <strong>PositionInSet</strong> pour décrire le nombre d’éléments dans le jeu.<br/> Type Variant : <strong>VT_I4</strong><br/> Valeur par défaut : 0<br/></td>
</tr>
<tr class="odd">
<td ><span id="UIA_VisualEffectsPropertyId"></span><span id="uia_visualeffectspropertyid"></span><span id="UIA_VISUALEFFECTSPROPERTYID"></span><dl> <dt><strong>UIA_VisualEffectsPropertyId</strong></dt> <dt>30163</dt> </dl></td>
<td >Identifie la propriété <strong>VisualEffects</strong> , qui est un champ de bits qui spécifie les effets sur l’élément Automation, tels que l’ombre, la réflexion, la lueur, les bords adoucis ou le biseau.<br/> VisualEffects:<br/>
<ul>
<li>VisualEffects_Shadow : 0x1</li>
<li>VisualEffects_Reflection : 0X2</li>
<li>VisualEffects_Glow : 0x4</li>
<li>VisualEffects_SoftEdges : 0x8</li>
<li>VisualEffects_Bevel : 0x10</li>
</ul>
Type Variant : <strong>VT_I4</strong><br/> Valeur par défaut : 0<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows Applications de bureau XP pour applications \[ \| UWP\]<br/>                                              |
| Serveur minimal pris en charge<br/> | Windows Applications de bureau du serveur 2003 \[ \| applications UWP\]<br/>                                     |
| En-tête<br/>                   | <dl> <dt>UIAutomationClient. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

**Méthodologique**
</dt> <dt>

[Vue d'ensemble des propriétés UI Automation](uiauto-propertiesoverview.md)
</dt> <dt>

[Récupération de propriétés à partir d’éléments UI Automation](uiauto-propertiesforclients.md)
</dt> </dl>
