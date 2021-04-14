---
description: Définit des valeurs de chaîne constantes qui sont utilisées pour augmenter la précision de la reconnaissance en fournissant des informations contextuelles au module de reconnaissance.
ms.assetid: 247a1f7d-8205-4e4d-9cfc-daad9bd2191f
title: Constantes Factoid (Msinkaut. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1353a4989ddfb5af3865788c0fa7fdc2d377f75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526595"
---
# <a name="factoid-constants"></a>Constantes Factoid

Définit des valeurs de chaîne constantes qui sont utilisées pour augmenter la précision de la reconnaissance en fournissant des informations contextuelles au module de reconnaissance.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;">Nom</th>
<th style="text-align: left;">Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_NONE"></span><span id="factoid_none"></span><dl> <dt><strong>FACTOID_NONE</strong></dt> </dl></td>
<td style="text-align: left;">Désactive tous les autres Factoids et dictionnaires.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_DEFAULT_________"></span><span id="___________factoid_default_________"></span><dl> <dt><strong>FACTOID_DEFAULT</strong></dt> </dl></td>
<td style="text-align: left;">Le paramètre par défaut pour Factoids pour les langues occidentales comprend le dictionnaire système, le dictionnaire de l’utilisateur, les différents signes de ponctuation et le Web et le numéro Factoid. Le paramètre par défaut pour Factoids pour les langues d’Extrême-Orient comprend tous les caractères pris en charge par le module de reconnaissance. <br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_SYSTEMDICTIONARY_________"></span><span id="___________factoid_systemdictionary_________"></span><dl> <dt><strong>FACTOID_SYSTEMDICTIONARY</strong></dt> </dl></td>
<td style="text-align: left;">Indique à un module de reconnaissance pour utiliser le dictionnaire système uniquement.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_WORDLIST_________"></span><span id="___________factoid_wordlist_________"></span><dl> <dt><strong>FACTOID_WORDLIST</strong></dt> </dl></td>
<td style="text-align: left;">Indique à un module de reconnaissance pour utiliser une liste de mots définie par programmation. La liste de mots est définie par la <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_wordlist"><strong>propriété liste</strong></a> de mots d’un objet <a href="inkrecognizercontext-class.md"><strong>InkRecognizerContext</strong></a> . <br/>
<blockquote>
[!Note]<br />
Si une chaîne est ajoutée à une liste de mots, ses versions en majuscules sont également ajoutées de manière implicite. Par exemple, l’ajout de &quot; Hello &quot; ajoute implicitement Hello &quot; &quot; et &quot; Hello &quot; .
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_EMAIL_________"></span><span id="___________factoid_email_________"></span><dl> <dt><strong>FACTOID_EMAIL</strong></dt> </dl></td>
<td style="text-align: left;">Indique à un module de reconnaissance pour rechercher une adresse e-mail.<br/>
<blockquote>
[!Note]<br />
Une adresse de messagerie complète, telle que &quot; someone@example.com &quot; , doit être utilisée pour ce Factoid. Un alias solitaire, tel qu’un &quot; individu &quot; , n’est pas reconnu.
</blockquote>
<br/>
<pre class="syntax" data-space="preserve"><code>someone@example.com</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_WEB"></span><span id="factoid_web"></span><dl> <dt><strong>FACTOID_WEB</strong></dt> </dl></td>
<td style="text-align: left;">Indique à un module de reconnaissance pour rechercher une adresse Web.<br/>
<pre class="syntax" data-space="preserve"><code>`https://www.adatum.com`</code></pre></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_ONECHAR_________"></span><span id="___________factoid_onechar_________"></span><dl> <dt><strong>FACTOID_ONECHAR</strong></dt> </dl></td>
<td style="text-align: left;">Indique à un module de reconnaissance pour rechercher un caractère unique.<br/>
<blockquote>
[!Note]<br />
Ce Factoid recherche tout caractère ANSI isolé.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_NUMBER_________"></span><span id="___________factoid_number_________"></span><dl> <dt><strong>FACTOID_NUMBER</strong></dt> </dl></td>
<td style="text-align: left;">Indique à un module de reconnaissance pour rechercher un nombre.<br/>
<blockquote>
[!Note]<br />
Les valeurs numériques incluent les séparateurs, les décimales, les ordinaux et d’autres symboles numériques couramment utilisés.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_DIGIT_________"></span><span id="___________factoid_digit_________"></span><dl> <dt><strong>FACTOID_DIGIT</strong></dt> </dl></td>
<td style="text-align: left;">Indique à un module de reconnaissance pour rechercher un chiffre unique, de 0 à 9.<br/>
<pre class="syntax" data-space="preserve"><code>0, 1, 2, 3, 4, 5, 6, 7, 8, 9</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_NUMBERSIMPLE_________"></span><span id="___________factoid_numbersimple_________"></span><dl> <dt><strong>FACTOID_NUMBERSIMPLE</strong></dt> </dl></td>
<td style="text-align: left;">Fournit un contexte numérique simple à un module de reconnaissance.<br/>
<blockquote>
[!Note]<br />
Ce Factoid n’est pas pris en charge dans cette version du kit de développement logiciel (SDK) Tablet PC.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_CURRENCY_________"></span><span id="___________factoid_currency_________"></span><dl> <dt><strong>FACTOID_CURRENCY</strong></dt> </dl></td>
<td style="text-align: left;">Indique à un module de reconnaissance pour rechercher des caractères qui désignent une valeur monétaire.<br/>
<pre class="syntax" data-space="preserve"><code>$45.95,  60,  50.25,  3000</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_POSTALCODE_________"></span><span id="___________factoid_postalcode_________"></span><dl> <dt><strong>FACTOID_POSTALCODE</strong></dt> </dl></td>
<td style="text-align: left;">Indique à un module de reconnaissance pour rechercher les codes postaux.<br/>
<pre class="syntax" data-space="preserve"><code>98112</code></pre></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_PERCENT_________"></span><span id="___________factoid_percent_________"></span><dl> <dt><strong>FACTOID_PERCENT</strong></dt> </dl></td>
<td style="text-align: left;">Indique à un module de reconnaissance pour rechercher les pourcentages.<br/>
<pre class="syntax" data-space="preserve"><code>87%</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_DATE_________"></span><span id="___________factoid_date_________"></span><dl> <dt><strong>FACTOID_DATE</strong></dt> </dl></td>
<td style="text-align: left;">Indique à un module de reconnaissance pour rechercher des caractères qui désignent une date.<br/>
<pre class="syntax" data-space="preserve"><code>10/30/2001, &#39;01, 31/12, 12/99, 1999-2000</code></pre></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_TIME_________"></span><span id="___________factoid_time_________"></span><dl> <dt><strong>FACTOID_TIME</strong></dt> </dl></td>
<td style="text-align: left;">Indique à un module de reconnaissance pour rechercher des caractères qui désignent une heure.<br/>
<pre class="syntax" data-space="preserve"><code>12:23:00 PM, 12:30, 24:30, 12:23:01, 1:12 A.M.</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_TELEPHONE_________"></span><span id="___________factoid_telephone_________"></span><dl> <dt><strong>FACTOID_TELEPHONE</strong></dt> </dl></td>
<td style="text-align: left;">Indique à un module de reconnaissance pour rechercher des caractères qui désignent un numéro de téléphone.<br/>
<pre class="syntax" data-space="preserve"><code>123 555 0190, 0-123-206 555 0190, (206)555-0190</code></pre></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_FILENAME_________"></span><span id="___________factoid_filename_________"></span><dl> <dt><strong>FACTOID_FILENAME</strong></dt> </dl></td>
<td style="text-align: left;">Indique à un module de reconnaissance pour rechercher des caractères qui désignent un nom de fichier.<br/>
<pre class="syntax" data-space="preserve"><code>mydocument.doc, c:\myfolder\file.c</code></pre></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_UPPERCHAR_________"></span><span id="___________factoid_upperchar_________"></span><dl> <dt><strong>FACTOID_UPPERCHAR</strong></dt> </dl></td>
<td style="text-align: left;">Indique à un module de reconnaissance pour rechercher un caractère majuscule unique : de A à Z.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="___________FACTOID_LOWERCHAR_________"></span><span id="___________factoid_lowerchar_________"></span><dl> <dt><strong>FACTOID_LOWERCHAR</strong></dt> </dl></td>
<td style="text-align: left;">Indique à un module de reconnaissance pour rechercher un seul caractère en minuscules : de A à Z.<br/>
<blockquote>
[!Note]<br />
Ce Factoid n’est pas pris en charge dans cette version du kit de développement logiciel (SDK) Tablet PC.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="___________FACTOID_PUNCCHAR_________"></span><span id="___________factoid_puncchar_________"></span><dl> <dt><strong>FACTOID_PUNCCHAR</strong></dt> </dl></td>
<td style="text-align: left;">Indique à un module de reconnaissance pour rechercher les caractères de ponctuation.<br/>
<blockquote>
[!Note]<br />
Ce Factoid n’est pas pris en charge dans cette version du kit de développement logiciel (SDK) Tablet PC.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_JAPANESECOMMON"></span><span id="factoid_japanesecommon"></span><dl> <dt><strong>FACTOID_JAPANESECOMMON</strong></dt> </dl></td>
<td style="text-align: left;">Indique à un module de reconnaissance pour rechercher des caractères Kanji, katakana et Hiragana couramment utilisés.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_CHINESESIMPLECOMMON"></span><span id="factoid_chinesesimplecommon"></span><dl> <dt><strong>FACTOID_CHINESESIMPLECOMMON</strong></dt> </dl></td>
<td style="text-align: left;">Indique à un module de reconnaissance pour rechercher les caractères chinois simplifié couramment utilisés.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_CHINESETRADITIONALCOMMON"></span><span id="factoid_chinesetraditionalcommon"></span><dl> <dt><strong>FACTOID_CHINESETRADITIONALCOMMON</strong></dt> </dl></td>
<td style="text-align: left;">Indique à un module de reconnaissance pour rechercher les caractères chinois traditionnel couramment utilisés.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_KOREANCOMMON"></span><span id="factoid_koreancommon"></span><dl> <dt><strong>FACTOID_KOREANCOMMON</strong></dt> </dl></td>
<td style="text-align: left;">Indique à un module de reconnaissance pour rechercher les caractères coréens couramment utilisés.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_HIRAGANA"></span><span id="factoid_hiragana"></span><dl> <dt><strong>FACTOID_HIRAGANA</strong></dt> </dl></td>
<td style="text-align: left;">Indique à un module de reconnaissance pour rechercher des caractères Hiragana uniquement.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_KATAKANA"></span><span id="factoid_katakana"></span><dl> <dt><strong>FACTOID_KATAKANA</strong></dt> </dl></td>
<td style="text-align: left;">Indique à un module de reconnaissance pour rechercher des caractères katakana uniquement.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_KANJICOMMON"></span><span id="factoid_kanjicommon"></span><dl> <dt><strong>FACTOID_KANJICOMMON</strong></dt> </dl></td>
<td style="text-align: left;">Indique à un module de reconnaissance pour rechercher des caractères Kanji couramment utilisés.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_KANJIRARE"></span><span id="factoid_kanjirare"></span><dl> <dt><strong>FACTOID_KANJIRARE</strong></dt> </dl></td>
<td style="text-align: left;">Indique à un module de reconnaissance pour rechercher les caractères Kanji rarement utilisés.<br/>
<blockquote>
[!Note]<br />
Ce Factoid n’est pas pris en charge dans cette version du kit de développement logiciel (SDK) Tablet PC.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_BOPOMOFO"></span><span id="factoid_bopomofo"></span><dl> <dt><strong>FACTOID_BOPOMOFO</strong></dt> </dl></td>
<td style="text-align: left;">Indique à un module de reconnaissance pour rechercher des caractères Bopomofo.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_JAMO"></span><span id="factoid_jamo"></span><dl> <dt><strong>FACTOID_JAMO</strong></dt> </dl></td>
<td style="text-align: left;">Indique à un module de reconnaissance pour rechercher les caractères Jamos de compatibilité hangûl.<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="FACTOID_HANGULCOMMON"></span><span id="factoid_hangulcommon"></span><dl> <dt><strong>FACTOID_HANGULCOMMON</strong></dt> </dl></td>
<td style="text-align: left;">Indique à un module de reconnaissance pour rechercher des caractères Hangul couramment utilisés.<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="FACTOID_HANGULRARE"></span><span id="factoid_hangulrare"></span><dl> <dt><strong>FACTOID_HANGULRARE</strong></dt> </dl></td>
<td style="text-align: left;">Indique à un module de reconnaissance pour rechercher les caractères Hangul rarement utilisés.<br/>
<blockquote>
[!Note]<br />
Ce Factoid n’est pas pris en charge dans cette version du kit de développement logiciel (SDK) Tablet PC.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a>Notes

En C++, vous pouvez accéder à ces constantes dans le fichier d’en-tête Msinkaut. h, situé dans le <systemdrive> \\ répertoire : Program Files \\ Microsoft Tablet PC Platform SDK \\ include si vous avez installé le kit de développement logiciel (SDK) à l’emplacement par défaut.

> [!Note]  
> Ces constantes sont WCHARs, et non BSTR. Elles doivent être converties en BSTR avant d’être utilisées comme paramètres pour les méthodes d’objet. Pour plus d’informations sur le type de données BSTR, consultez [utilisation de la bibliothèque com](using-the-com-library.md).

 

> [!Note]  
> Pour les détecteurs de script latin, les Factoids définis dans cette classe sont fournis uniquement à des fins de compatibilité descendante. Pour les nouveaux développements, il est recommandé d’utiliser les valeurs définies dans la fonction [SetInputScope](/windows/desktop/api/inputscope/nf-inputscope-setinputscope) . Pour plus d’informations, consultez [utilisation du contexte pour améliorer la précision](using-context-to-improve-accuracy.md).

 

Utilisez ces identificateurs pour spécifier les Factoid à utiliser lors de la reconnaissance.

Les combinaisons de Factoids suivantes sont prises en charge uniquement pour les langues occidentales. Ils n’ont pas de définitions distinctes, mais sont des entrées de littéral de chaîne acceptables dans la propriété [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) d’objets qui utilisent Factoids. Ces constantes de chaîne Factoid permettent à l’entrée de correspondre à l’un des Factoids dans l’expression.



| Combinaison               | Définition                                                |
|---------------------------|-----------------------------------------------------------|
| « la rubrique WEB \| »           | Factoid Web ou liste de mots.                         |
| « courrier électronique \| »         | Factoid d’E-mail ou liste de mots.                       |
| « NOM du fichier \| Web \| » | Nom de fichier Factoid ou Factoid Web ou liste de mots. |



 

Si vous utilisez le contrôle [InkEdit](inkedit-control-reference.md) , Factoid peut être défini en tant que propriété du contrôle.

Si vous utilisez les API de la plateforme Tablet PC, vous pouvez définir la propriété [**Factoid**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid) sur un objet [**InkRecognizerContext**](inkrecognizercontext-class.md) .

Vous pouvez également définir cette propriété avec la constante de chaîne Factoid réelle.

> [!Note]  
> Les constantes de chaîne Factoid sont sensibles à la casse. Pour plus d’informations sur les Factoids et leur utilisation, consultez Utilisation du contexte pour [améliorer la précision](using-context-to-improve-accuracy.md). Pour déterminer si un Factoid est disponible dans un langage spécifique, consultez [Factoids pris en charge à partir de la version 1](supported-factoids-from-version-1.md).

 

## <a name="requirements"></a>Configuration requise



| Condition requise | Valeur |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Applications de bureau Windows XP Édition Tablet PC \[ uniquement\]<br/>                                                       |
| Serveur minimal pris en charge<br/> | Aucun pris en charge<br/>                                                                                           |
| En-tête<br/>                   | <dl> <dt>Msinkaut. h (nécessite également Msinkaut \_ i. c)</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[**Factoid, propriété \[ InkRecognizeContext, classe\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognizercontext-get_factoid)
</dt> <dt>

[**Factoid, propriété \[ PenInputPanel, classe\]**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-get_factoid)
</dt> <dt>

[**Propriété Factoid \[ InkEdit, contrôle\]**](/windows/desktop/api/inked/nf-inked-iinkedit-get_factoid)
</dt> <dt>

[Utilisation du contexte pour améliorer la précision](using-context-to-improve-accuracy.md)
</dt> <dt>

[Factoids pris en charge à partir de la version 1](supported-factoids-from-version-1.md)
</dt> </dl>

 

