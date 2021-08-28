---
title: Fonctions RichEdit
description: Fonctions RichEdit
ms.assetid: 5e913cb6-d561-447f-b33e-9160a8f46cda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df1b74069b63220a07bfb1bd5e3f5a1ad99a6c6c
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122482455"
---
# <a name="rich-edit-functions"></a>Fonctions RichEdit

## <a name="in-this-section"></a>Contenu de cette section




| Rubrique | Description | 
|-------|-------------|
| <a href="/windows/desktop/api/Richedit/nc-richedit-autocorrectproc"><em>AutoCorrectProc</em></a><br /> | La fonction <a href="/windows/desktop/api/Richedit/nc-richedit-autocorrectproc"><em>AutoCorrectProc</em></a> est une fonction de rappel définie par l’application qui est utilisée avec le message <a href="em-setautocorrectproc.md"><strong>EM_SETAUTOCORRECTPROC</strong></a> .<br /> | 
| <a href="/windows/desktop/api/Richedit/nc-richedit-editstreamcallback"><em>EditStreamCallback</em></a><br /> | La fonction <a href="/windows/desktop/api/Richedit/nc-richedit-editstreamcallback"><em>EditStreamCallback</em></a> est une fonction de rappel définie par l’application utilisée avec les messages <a href="em-streamin.md"><strong>EM_STREAMIN</strong></a> et <a href="em-streamout.md"><strong>EM_STREAMOUT</strong></a> . Il est utilisé pour transférer un flux de données vers ou à partir d’un contrôle RichEdit. Le type <strong>EDITSTREAMCALLBACK</strong> définit un pointeur vers cette fonction de rappel. <em>EditStreamCallback</em> est un espace réservé pour le nom de la fonction définie par l’application. <br /> | 
| <a href="/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex"><em>EditWordBreakProcEx</em></a><br /> | La fonction <a href="/windows/desktop/api/Richedit/nc-richedit-editwordbreakprocex"><em>EditWordBreakProcEx</em></a> est une fonction de rappel définie par l’application utilisée avec le message <a href="em-setwordbreakprocex.md"><strong>EM_SETWORDBREAKPROCEX</strong></a> . Il détermine l’index de caractère de l’arrêt de mot ou la classe de caractères et les indicateurs de césure lexicale des caractères du texte spécifié. Le type <strong>EDITWORDBREAKPROCEX</strong> définit un pointeur vers cette fonction de rappel. <em>EditWordBreakProcEx</em> est un espace réservé pour le nom de la fonction définie par l’application. <br /> | 
| <a href="/previous-versions/windows/desktop/legacy/hh780353(v=vs.85)"><strong>GetMathAlphanumeric</strong></a><br /> | Récupère le caractère alphanumérique de transformation UTF (Unicode Transformation Format)-32 qui correspond au caractère BMP (Basic Multilingual Plane) et au style mathématique spécifiés. <br /> | 
| <a href="/previous-versions/windows/desktop/legacy/hh780354(v=vs.85)"><strong>GetMathAlphanumericCode</strong></a><br /> | Récupère le style mathématique et le code de caractère BMP (Basic Multilingual Plane) qui correspond à l’octet de fin spécifié d’une paire de substitution mathématique.<br /> | 
| <a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>HyphenateProc</em></a><br /> | La fonction <a href="/windows/desktop/api/Richedit/nf-richedit-hyphenateproc"><em>HyphenateProc</em></a> est une fonction de rappel définie par l’application utilisée avec le message <a href="em-sethyphenateinfo.md"><strong>EM_SETHYPHENATEINFO</strong></a> . Elle détermine la façon dont la césure est effectuée dans un contrôle Rich Edit Microsoft.<br /> | 
| <a href="/previous-versions/windows/desktop/legacy/hh780443(v=vs.85)"><strong>MathBuildDown</strong></a><br /> | Traduit les objets incorporés Math, Ruby et other inclus dans la plage spécifiée au format linéaire.<br /> | 
| <a href="/previous-versions/windows/desktop/legacy/hh780445(v=vs.85)"><strong>MathBuildUp</strong></a><br /> | Convertit les maths de format linéaire d’une plage en un formulaire intégré, ou modifie le formulaire de création actuel. <br /> | 
| <a href="/previous-versions/windows/desktop/legacy/hh780446(v=vs.85)"><strong>MathTranslate</strong></a><br /> | Traduit les caractères mathématiques dans la plage spécifiée.<br /> | 
| <a href="reextendedregisterclass.md"><strong>REExtendedRegisterClass</strong></a><br /> | Inscrit deux noms de classe, REListBox20W et RECombobox20W, qui peuvent être utilisés pour créer des fenêtres modifiables RichEdit ou de zone de liste déroulante. <br /><blockquote>[!Note]<br />Destiné à un usage interne ; non recommandé pour une utilisation dans les applications. Cette fonction peut ne pas être prise en charge dans les versions ultérieures.</blockquote><br /> | 




 

 

