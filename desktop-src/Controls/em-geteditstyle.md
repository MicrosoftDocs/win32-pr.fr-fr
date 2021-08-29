---
title: Message EM_GETEDITSTYLE (RichEdit. h)
description: Récupère les indicateurs de style de modification actuels.
ms.assetid: 568e51a4-0767-4a59-bf34-bc0281b5fe65
keywords:
- EM_GETEDITSTYLE les contrôles de Windows de message
topic_type:
- apiref
api_name:
- EM_GETEDITSTYLE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 220138a63628df310e316b6042045b7ca04ccbba
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481585"
---
# <a name="em_geteditstyle-message"></a>\_Message em GETEDITSTYLE

Récupère les indicateurs de style de modification actuels.

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

## <a name="return-value"></a>Valeur de retour

Retourne les indicateurs de style de modification actuels, qui peuvent inclure une ou plusieurs des valeurs suivantes :




| Code de retour | Description | 
|-------------|-------------|
| <dl><dt><strong>SES_BEEPONMAXTEXT</strong></dt></dl> | La modification complète appellera le bip système si l’utilisateur tente d’entrer plus de caractères que le nombre maximal.<br /> | 
| <dl><dt><strong>SES_BIDI</strong></dt></dl> | Active le traitement bidirectionnel. Cela est automatiquement activé par la modification complète si l’un des styles de fenêtre suivants est actif : <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_RIGHT</strong></a>, <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_RTLREADING</strong></a> <a href="/windows/desktop/winmsg/extended-window-styles"><strong>WS_EX_LEFTSCROLLBAR</strong></a>. Toutefois, ce paramètre est utile pour gérer ces styles de fenêtre lors de l’utilisation d’une implémentation personnalisée de <a href="/windows/desktop/api/Textserv/nl-textserv-itexthost"><strong>ITextHost</strong></a> (valeur par défaut : 0).<br /> | 
| <dl><dt><strong>SES_CTFALLOWEMBED</strong></dt></dl> | <strong>Windows XP avec SP1</strong>: autorisez l’insertion d’objets incorporés à l’aide de TSF (valeur par défaut : 0).<br /> | 
| <dl><dt><strong>SES_CTFALLOWPROOFING</strong></dt></dl> | <strong>Windows XP avec SP1</strong>: autorise les conseils de vérification de la protection TSF (valeur par défaut : 0).<br /> | 
| <dl><dt><strong>SES_CTFALLOWSMARTTAG</strong></dt></dl> | <strong>Windows XP avec SP1</strong>: autorise les conseils de TSF SmartTag (valeur par défaut : 0).<br /> | 
| <dl><dt><strong>SES_CTFNOLOCK</strong></dt></dl> | <strong>Windows 8</strong>: ne pas autoriser l’accès en lecture/écriture au verrou TSF. Cela suspend l’entrée TSF. <br /> | 
| <dl><dt><strong>SES_DEFAULTLATINLIGA</strong></dt></dl> | <strong>Windows 8</strong>: les polices avec une ligature fi sont affichées avec les fonctionnalités OpenType par défaut, ce qui améliore la typographie (valeur par défaut : 0). <br /> | 
| <dl><dt><strong>SES_DRAFTMODE</strong></dt></dl> | <strong>Windows XP avec SP1</strong>: utilisez les polices en mode brouillon pour afficher le texte. Le mode brouillon est une option d’accessibilité dans laquelle le contrôle affiche le texte avec une seule police ; la police est déterminée par le paramètre système de la police utilisée dans les boîtes de message. Par exemple, les utilisateurs accessibles peuvent lire du texte plus facilement s’ils sont uniformes, au lieu d’une combinaison de polices et de styles (valeur par défaut : 0). <br /> | 
| <dl><dt><strong>SES_EMULATE10</strong></dt></dl> | <strong>Windows 8</strong>: émuler le comportement RichEdit 1,0. <br /><blockquote>[!Note]<br />si vous souhaitez vraiment ce comportement, utilisez le riched32.dll Windows au lieu de riched20.dll ou msftedit.dll. Riched32.dll possédait plus de fonctionnalités.</blockquote><br /> | 
| <dl><dt><strong>SES_EMULATESYSEDIT</strong></dt></dl> | Lorsque ce bit est activé, la modification riche tente d’émuler le contrôle d’édition système (valeur par défaut : 0).<br /> | 
| <dl><dt><strong>SES_EXTENDBACKCOLOR</strong></dt></dl> | Étend la couleur d’arrière-plan jusqu’aux bords du rectangle client (valeur par défaut : 0).<br /> | 
| <dl><dt><strong>SES_HIDEGRIDLINES</strong></dt></dl> | <strong>Windows XP avec SP1</strong>: si la largeur du quadrillage du tableau est égale à zéro, le quadrillage ne s’affiche pas. Cela équivaut à la fonctionnalité masquer le quadrillage dans le menu Tableau de Word (valeur par défaut : 0).<br /> | 
| <dl><dt><strong>SES_HYPERLINKTOOLTIPS</strong></dt></dl> | <strong>Windows 8</strong>: lorsque le curseur se trouve sur un lien, affichez une info-bulle avec l’adresse du lien cible (valeur par défaut : 0). <br /> | 
| <dl><dt><strong>SES_LOGICALCARET</strong></dt></dl> | <strong>Windows 8</strong>: fournissez des informations de signe insertion logique au lieu d’une bitmap de signe insertion, comme décrit dans <a href="/windows/desktop/api/Textserv/nf-textserv-itexthost-txsetcaretpos"><strong>ITextHost :: TxSetCaretPos</strong></a> (valeur par défaut : 0). <br /> | 
| <dl><dt><strong>SES_LOWERCASE</strong></dt></dl> | Convertit tous les caractères d’entrée en minuscules (valeur par défaut : 0).<br /> | 
| <dl><dt><strong>SES_MAPCPS</strong></dt></dl> | Obsolète. Ne pas utiliser.<br /> | 
| <dl><dt><strong>SES_MULTISELECT</strong></dt></dl> | <strong>Windows 8</strong>: activez la multisélection avec les sélections de souris individuelles effectuées pendant que la touche Ctrl est enfoncée (valeur par défaut : 0). <br /> | 
| <dl><dt><strong>SES_NOEALINEHEIGHTADJUST</strong></dt></dl> | <strong>Windows 8</strong>: ne pas ajuster la hauteur de ligne pour le texte asiatique de l’est (valeur par défaut : 0 qui ajuste la hauteur de ligne de 15%). <br /> | 
| <dl><dt><strong>SES_NOFOCUSLINKNOTIFY</strong></dt></dl> | Envoie <a href="en-link.md">EN_LINK</a> notification à partir des liens qui n’ont pas le focus.<br /> | 
| <dl><dt><strong>SES_NOIME</strong></dt></dl> | Interdit les IME pour cette instance du contrôle RichEdit (valeur par défaut : 0).<br /> | 
| <dl><dt><strong>SES_NOINPUTSEQUENCECHK</strong></dt></dl> | Lorsque ce bit est activé, Rich Edit ne vérifie pas la séquence de texte tapé. Certains langages (tels que thaï et vietnamien) requièrent la vérification de l’ordre des séquences d’entrée avant leur envoi au magasin de stockage (valeur par défaut : 0).<br /> | 
| <dl><dt><strong>SES_SCROLLONKILLFOCUS</strong></dt></dl> | Quand KillFocus se produit, fait défiler jusqu’au début du texte (position de caractère égale à 0) (valeur par défaut : 0).<br /> | 
| <dl><dt><strong>SES_SMARTDRAGDROP</strong></dt></dl> | <strong>Windows 8</strong>: ajouter ou supprimer un espace en fonction du contexte lors de la suppression du texte (valeur par défaut : 0). <br /> | 
| <dl><dt><strong>SES_USECRLF</strong></dt></dl> | Obsolète. Ne pas utiliser.<br /> | 
| <dl><dt><strong>SES_WORDDRAGDROP</strong></dt></dl> | <strong>Windows 8</strong>: si l’option sélectionner le mot est active, assurez-vous que l’emplacement cible se trouve à la limite d’un mot (valeur par défaut : 0). <br /> | 
| <dl><dt><strong>SES_UPPERCASE</strong></dt></dl> | Convertit tous les caractères d’entrée en majuscules (valeur par défaut : 0).<br /> | 
| <dl><dt><strong>SES_USEAIMM</strong></dt></dl> | Utilise le composant de méthode d’entrée IMM actif fourni avec Internet Explorer 4,0 ou une version ultérieure (valeur par défaut : 0).<br /> | 
| <dl><dt><strong>SES_USEATFONT</strong></dt></dl> | <strong>Windows XP avec SP1</strong>: utilise une police @, conçue pour le texte vertical ; utilisé avec le style de fenêtre <a href="rich-edit-control-styles.md"><strong>ES_VERTICAL</strong></a> . Le nom d’une @ font commence par le symbole @, par exemple, « @Batang » (valeur par défaut : 0, mais est activé automatiquement pour la disposition du texte vertical). <br /> | 
| <dl><dt><strong>SES_USECTF</strong></dt></dl> | <strong>Windows XP avec SP1</strong>: active la prise en charge de TSF. (valeur par défaut : 0)<br /> | 
| <dl><dt><strong>SES_XLTCRCRLFTOCR</strong></dt></dl> | Active la traduction de CRCRLFs en CRs. Lorsque ce bit est activé et qu’un fichier est lu, toutes les instances de CRCRLF sont converties en fichiers CRs en interne. Cela aura une incidence sur l’habillage du texte. Notez que si un fichier de ce type est enregistré en texte brut, le Sir sera remplacé par CRLFs. Il s’agit de la norme .txt pour le texte brut (valeur par défaut : 0, qui supprime CRCRLFs en entrée). <br /> | 




 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows \[Applications de bureau Vista uniquement\]<br/>                                        |
| Serveur minimal pris en charge<br/> | Windows Serveur 2003 \[ applications de bureau uniquement\]<br/>                                  |
| Composant redistribuable<br/>          | Édition enrichie 3,0<br/>                                                              |
| En-tête<br/>                   | <dl> <dt>RichEdit. h</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**\_SETEDITSTYLE em**](em-seteditstyle.md)
</dt> </dl>

 

