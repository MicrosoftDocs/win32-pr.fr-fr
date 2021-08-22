---
title: Annexes E text attributes for Active Accessibility Text Services dictionary
description: Cette annexe fournit des informations sur les attributs de texte définis dans IAccDictionary.
ms.assetid: 9e405140-c151-4f00-91c5-777c84c41806
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 539583f05e5140d96594490b0038b1a629f7760b13e4de223f6a8a3304c3901b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134062"
---
# <a name="appendix-e-text-attributes-for-active-accessibility-text-services-dictionary"></a>Annexe E : attributs de texte pour Active Accessibility dictionnaire des services de texte

Cette annexe fournit des informations sur les attributs de texte définis dans [**IAccDictionary**](/windows/desktop/api/msaatext/nn-msaatext-iaccdictionary). Il est organisé sous la forme d’une série de tables. Chaque table contient des informations sur une catégorie spécifique d’attributs. Ces catégories sont réellement imbriquées, mais sont séparées ci-dessous afin que vous puissiez voir les attributs.

> [!Note]  
> Active Accessibility Text services est déconseillé. pour plus d’informations sur l’entrée de texte avancée et les technologies de langage naturel, consultez [Microsoft Windows text Services Framework](../tsf/text-services-framework.md) .

 

Chaque entrée d’une table fournit un nom d’attribut et un nom convivial, un type, un feuilles de style en cascade (CSS) équivalent, un modèle d’objet de texte (TOM) équivalent, ainsi que des commentaires supplémentaires, le cas échéant. La colonne TOM équivalente fournit des informations sur la méthode TOM utilisée avec l’attribut (partie des interfaces [**ITextFont**](/windows/desktop/api/tom/nn-tom-itextfont), [**ITextRange**](/windows/desktop/api/tom/nn-tom-itextrange)ou [**ITextPara**](/windows/desktop/api/tom/nn-tom-itextpara) ). Les informations antérieures à chaque table indiquent l’interface qui prend en charge les attributs. les informations contenues dans la table équivalente TOM indiquent le nom de la méthode. Chaque entrée de la colonne équivalente TOM est associée à deux méthodes. Par exemple, l’entrée de nom est associée aux méthodes **GetName** et **SetName** .

pour plus d’informations sur ces interfaces, consultez la documentation du [modèle d’objet de texte](../controls/text-object-model.md) dans le kit de développement logiciel (SDK) Windows.

## <a name="font"></a>Police

Les attributs du tableau suivant sont associés à des attributs de police généraux. L’équivalent TOM est l’interface [**ITextFont**](/windows/desktop/api/tom/nn-tom-itextfont) .



| Nom de l’attribut, nom convivial       | Type     | Équivalent CSS       | Équivalent TOM | Commentaire           |
|-------------------------------------|----------|----------------------|----------------|-------------------|
| \_FaceName de police, FaceName<br/> | VT \_ BSTR | Famille de polices : Verdana | Nom           |                   |
| \_SizePts de police, SizePts<br/>   | VT \_   | Font-size : XPT       | Taille           | La taille est en points |



 

## <a name="font_style"></a>Style de police \_

Les attributs du tableau suivant regroupent les attributs de style de police (par exemple, si le texte est défini en gras ou en italique). L’équivalent TOM est l’interface [**ITextFont**](/windows/desktop/api/tom/nn-tom-itextfont) .



| Nom de l’attribut, nom convivial                             | Type     | Équivalent CSS              | Équivalent TOM                                            | Commentaire                   |
|-----------------------------------------------------------|----------|-----------------------------|-----------------------------------------------------------|---------------------------|
| \_Style \_ de police gras, gras<br/>                        | VT \_ bool | Font-weight : gras           | Gras                                                      |                           |
| \_Style \_ de police italique, italique<br/>                    | VT \_ bool | Font-style : italique          | Italique                                                    |                           |
| \_Style \_ de police SmallCaps, SmallCaps<br/>              | VT \_ bool | Font-variant : petites majuscules    | SmallCaps                                                 |                           |
| \_Style \_ de police majuscule, majuscule<br/>             | VT \_ bool | Text-transform : majuscule  | Non pris en charge                                             |                           |
| \_Style \_ de police majuscule, majuscules<br/>               | VT \_ bool | Text-transform : majuscules   | AllCaps                                                   |                           |
| \_Style \_ de police minuscules, minuscules<br/>               | VT \_ bool | Text-transform : minuscules   | Non pris en charge                                             |                           |
| \_Style \_ de police relief, relief<br/>                     | VT \_ bool | Non pris en charge               | Relief                                                    |                           |
| \_Style \_ de police Engrave, empreinte<br/>                   | VT \_ bool | Non pris en charge               | Empreinte                                                   |                           |
| Style de police \_ \_ masqué                                       | VT \_ bool | Non pris en charge               | Hidden                                                    |                           |
| \_ \_ Crénage de style de police, crénage<br/>                   | VT \_ R4   | Non pris en charge               | Le crénage                                                   | Mêmes valeurs que GetKerning |
| \_Style \_ de police souligné, contour<br/>                 | VT \_ bool | Non pris en charge               | Indiquée                                                  |                           |
| \_Position du style \_ de police, position<br/>                 | VT \_ R4   | Non pris en charge               | Position                                                  |                           |
| Style de police \_ \_ protégé                                    | VT \_ bool | Non pris en charge               | Protected                                                 |                           |
| \_Ombre du style \_ de police, ombre<br/>                     | VT \_ bool | Hauteur de la ligne (moins de nombres) | Shadow                                                    |                           |
| \_ \_ Espacement du style de police, espacement<br/>                   | VT \_ R4   | Espacement des lettres              | Espacement                                                   | En points                 |
| \_Épaisseur du style \_ de police, poids<br/>                     | VT \_   | Police-Weight                 | WeightSame les valeurs comme police-Weight et GetWeight<br/> |                           |
| \_ \_ Hauteur de style de police, hauteur<br/>                     | VT \_ R4   | Line-height                 | Non pris en charge                                             | En points                 |
| \_ \_ Clignotement du style de police, clignotant<br/>                       | VT \_ bool | Texte-décoration : clignoter      | Non pris en charge                                             |                           |
| \_ \_ Indice de police, indice<br/>               | VT \_ bool | Vertical-align : Sub         | Indice (position également)                                 |                           |
| \_ \_ Exposant de style de police, exposant<br/>           | VT \_ bool | Alignement vertical : Super       | Exposant (position également)                               |                           |
| \_Couleur du style \_ de police, couleur<br/>                       | VT \_   | Couleur                       | CouleurTexte                                                 | Style COLORREF RBG        |
| \_Style \_ de police BackgroundColor, couleur d’arrière-plan \_<br/> | VT \_   | Background-couleur            | CouleurFond                                                 | Style COLORREF RBG        |



 

## <a name="font_style_animation"></a>\_Animation de style de police \_

Les attributs de l’animation de police d’adresse du tableau suivant. L’équivalent TOM est l’interface [**ITextFont**](/windows/desktop/api/tom/nn-tom-itextfont) .



| Nom de l’attribut, nom convivial                                              | Type     | Équivalent CSS | Équivalent TOM |
|----------------------------------------------------------------------------|----------|----------------|----------------|
| \_ \_ Animation de style \_ de police LasVegasLights, \_ lumières LasVegas<br/>         | VT \_ bool | Non pris en charge  | Animation      |
| \_ \_ Animation de style \_ de police BlinkingBackground, \_ arrière-plan clignotant<br/> | VT \_ bool | Non pris en charge  | Animation      |
| \_Animation style \_ de police \_ SparkleText, \_ texte Spark<br/>               | VT \_ bool | Non pris en charge  | Animation      |
| \_ \_ Animation de style \_ de police MarchingBlackAnts, défilé \_ noir \_ ants<br/> | VT \_ bool | Non pris en charge  | Animation      |
| \_ \_ Animation de style \_ de police MarchingRedAnts, défilé de \_ \_ ants rouge<br/>     | VT \_ bool | Non pris en charge  | Animation      |
| \_ \_ Animation de style \_ de police vibrations, scintillement<br/>                         | VT \_ bool | Non pris en charge  | Animation      |
| \_ \_ Animation de style \_ de police WipeDown, WipeDown<br/>                       | VT \_ bool | Non pris en charge  | Animation      |
| \_ \_ Animation de style \_ de police WipeRight, WipeRight<br/>                     | VT \_ bool | Non pris en charge  | Animation      |



 

## <a name="font_style_underline"></a>\_Souligner le style de police \_

Les attributs du tableau suivant définissent les styles de soulignement pour les polices. L’équivalent TOM est l’interface [**ITextFont**](/windows/desktop/api/tom/nn-tom-itextfont) .



| Nom de l’attribut, nom convivial                     | Type     | Équivalent CSS                | Équivalent TOM |
|---------------------------------------------------|----------|-------------------------------|----------------|
| \_Style \_ de police souligné \_ unique, unique<br/>  | VT \_ bool | Texte-décoration : souligné    | Souligner      |
| \_Style \_ de police souligné \_ double, double<br/> | VT \_ bool | Texte-décoration : ligne par ligne | Barre  |



 

## <a name="font_style_strikethrough"></a>Style de police \_ \_ barré

Les attributs du tableau suivant définissent les styles de texte barré pour les polices.



| Nom de l’attribut, nom convivial                                         | Type     | Équivalent CSS | Équivalent TOM |
|-----------------------------------------------------------------------|----------|----------------|----------------|
| \_Style \_ de police barré \_ simple, barré \_ \_ simple<br/> | VT \_ bool | Non pris en charge  | Non pris en charge  |
| \_Style \_ de police barré \_ double, barré \_ \_ double<br/> | VT \_ bool | Non pris en charge  | Non pris en charge  |



 

## <a name="font_style_overline"></a>Style de police \_ \_ souligné

Les attributs du tableau suivant définissent les styles de police de surlignage pour les polices.



| Nom de l’attribut, nom convivial                             | Type     | Équivalent CSS            | Équivalent TOM |
|-----------------------------------------------------------|----------|---------------------------|----------------|
| \_Style \_ de police \_ simple, surligne \_ simple<br/> | VT \_ bool | Text-decoration : trait de soulignement | Non pris en charge  |
| \_ \_ Trait de soulignement \_ double, superligne \_ double<br/> | VT \_ bool | Text-decoration : trait de soulignement | Non pris en charge  |



 

## <a name="text"></a>Texte

Les attributs du tableau suivant traitent des attributs de mise en forme générale du texte.



| Nom de l’attribut, nom convivial                     | Type        | Équivalent CSS | Équivalent TOM                                       | Commentaire                                                                               |
|---------------------------------------------------|-------------|----------------|------------------------------------------------------|---------------------------------------------------------------------------------------|
| Texte \_ VerticalWriting, écriture verticale<br/> | VT \_ bool    | Non pris en charge  | non pris en charge                                        | Utilisé par le chinois/japonais                                                           |
| Texte \_ RightToLeft, RightToLeft<br/>          | VT \_ bool    | Sens      | Non pris en charge                                        |                                                                                       |
| Texte \_ en lecture seule, lecture seule<br/>               | VT \_ bool    | Non pris en charge  | ITextFont :: CanChange, ITextRange :: CanEdit            | La propriété modifiable du document est prioritaire                                     |
| Langue du texte \_ , langue<br/>                | VT \_      | Non pris en charge  | ITextFont::GetLanguageID, ITextFont::SetLanguageID   | LANGID                                                                                |
| Orientation du texte \_ , orientation<br/>          | VT \_      | Non pris en charge  | Non pris en charge                                        | 10 ??? d’un degré                                                                     |
| Texte \_ EmbeddedObject, objet incorporé \_<br/>  | VT \_ bool    | Non pris en charge  | Non pris en charge                                        | Permet de rechercher des objets incorporés                                                 |
| \_Lien de texte, lien<br/>                        | VT \_ inconnu | Lien           | Non pris en charge                                        | Pointeur d’interface vers l’objet ; appeler QueryInterface pour toute interface digne d’intérêt |
| \_Césure de texte, césure<br/>          | VT \_ bool    | Non pris en charge  | ITextPara::GetHyphenation, ITextPara::SetHyphenation |                                                                                       |



 

## <a name="text_alignment"></a>Alignement du texte \_

Les attributs figurant dans le tableau suivant démontrent l’alignement du texte. L’équivalent TOM est l’interface [**ITextPara**](/windows/desktop/api/tom/nn-tom-itextpara) .



| Nom de l’attribut, nom convivial               | Type     | Équivalent CSS | Équivalent TOM |
|---------------------------------------------|----------|----------------|----------------|
| Alignement du texte à \_ \_ gauche, à gauche<br/>       | VT \_ bool | Aligner le texte     | Alignment      |
| Alignement du texte à droite \_ \_ , droite<br/>     | VT \_ bool | Aligner le texte     | Alignment      |
| \_Centre d’alignement \_ de texte, Centre<br/>   | VT \_ bool | Aligner le texte     | Alignment      |
| Alignement du texte \_ \_ , justifier<br/> | VT \_ bool | Aligner le texte     | Alignment      |



 

## <a name="text_para"></a>Paragraphe de texte \_

Les attributs du tableau suivant déforment l’adresse des paragraphes. L’équivalent TOM est l’interface [**ITextPara**](/windows/desktop/api/tom/nn-tom-itextpara) .



| Nom de l’attribut, nom convivial                              | Type   | Équivalent CSS | Équivalent TOM  | Commentaire |
|------------------------------------------------------------|--------|----------------|-----------------|---------|
| \_FirstLineIndent paragraphe \_ de texte, retrait de la première \_ ligne \_<br/> | VT \_ R4 | Non pris en charge  | FirstLineIndent | Dans pts  |
| Texte \_ para \_ LeftIndent, retrait à gauche \_<br/>             | VT \_ R4 | Non pris en charge  | LeftIndent      | Dans pts  |
| Texte- \_ paragraphe \_ RightIndent, \_ retrait à droite<br/>           | VT \_ R4 | Non pris en charge  | RightIndent     | Dans pts  |
| \_Paragraphe \_ de texte SpaceAfter, espace \_ après<br/>             | VT \_ R4 | Non pris en charge  | SpaceAfter      | Dans pts  |
| Texte \_ paragraphe \_ SpaceBefore, espace \_ après<br/>            | VT \_ R4 | Non pris en charge  | SpaceAfter      | Dans pts  |



 

## <a name="text_para_linespacing"></a>Texte des paragraphes de texte \_ \_

Les attributs figurant dans le tableau suivant traitent l’interligne des paragraphes. L’équivalent TOM est l’interface [**ITextPara**](/windows/desktop/api/tom/nn-tom-itextpara) .



| Nom de l’attribut, nom convivial                               | Type     | Équivalent CSS | Équivalent TOM | Commentaire  |
|-------------------------------------------------------------|----------|----------------|----------------|----------|
| Texte \_ para-description \_ \_ simple, unique<br/>           | VT \_ bool | Non pris en charge  | Interligne    |          |
| Text \_ para \_ \_ baOnePtFive, One \_ PT \_ cinq<br/> | VT \_ bool | Non pris en charge  | Interligne    |          |
| Texte \_ paragraphe \_ LineSpacing \_ double, double<br/>           | VT \_ bool | Non pris en charge  | Interligne    |          |
| Texte \_ \_ des paragraphes \_ interversions au \_ moins<br/>       | VT \_ R4   | Non pris en charge  | Interligne    | Dans les lignes |
| Description \_ \_ des paragraphes \_ de texte exactement, exactement<br/>         | VT \_ R4   | Non pris en charge  | Interligne    | Dans les lignes |
| Text \_ para \_ \_ multiples, multiple<br/>        | VT \_ R4   | Non pris en charge  | Interligne    | Dans les lignes |



 

## <a name="text_list"></a>Liste de texte \_

Les attributs du tableau suivant répertorient les listes d’adresses et les niveaux de texte. L’équivalent TOM est l’interface [**ITextPara**](/windows/desktop/api/tom/nn-tom-itextpara) .



| Nom de l’attribut, nom convivial | Type   | Équivalent CSS | Équivalent TOM | Commentaire                                                       |
|-------------------------------|--------|----------------|----------------|---------------------------------------------------------------|
| \_Liste \_ de texte LevelIndex,       | VT \_ | Non pris en charge  | ListLevelIndex | Où 1 est la liste la plus à l’extérieur, 2 le niveau suivant, et ainsi de suite |



 

## <a name="text_list_type"></a>\_Type de liste de texte \_

Les attributs du tableau suivant répertorient les styles de liste d’adresses pour le texte. L’équivalent TOM est l’interface [**ITextPara**](/windows/desktop/api/tom/nn-tom-itextpara) .



| Nom de l’attribut, nom convivial                          | Type     | Équivalent CSS  | Équivalent TOM |
|--------------------------------------------------------|----------|-----------------|----------------|
| \_ \_ Type de liste \_ de texte puce, puce<br/>             | VT \_ bool | Type de liste       | ListType       |
| \_ \_ Type de liste \_ de texte arabe, arabe<br/>             | VT \_ bool | Type de liste-style | ListType       |
| \_ \_ Type de liste \_ de texte LowerLetter, \_ lettre inférieure<br/> | VT \_ bool | Type de liste-style | ListType       |
| \_ \_ Type de liste \_ de texte UpperLetter, \_ lettre majuscule<br/> | VT \_ bool | Type de liste-style | ListType       |
| \_ \_ Type de liste \_ de texte LowerRoman, \_ chiffre romain inférieur<br/>   | VT \_ bool | Type de liste-style | ListType       |
| \_ \_ Type de liste \_ de texte UpperRoman, \_ chiffre romain majuscule<br/>   | VT \_ bool | Type de liste-style | ListType       |



 

## <a name="app"></a>Application



| Nom de l’attribut, nom convivial                         | Type     | Équivalent CSS | Équivalent TOM |
|-------------------------------------------------------|----------|----------------|----------------|
| \_IncorrectSpelling de l’application, orthographe incorrecte \_<br/> | VT \_ bool |                | Non pris en charge  |
| \_IncorrectGrammar de l’application, grammaire incorrecte \_<br/>   | VT \_ bool |                | Non pris en charge  |



 

 

