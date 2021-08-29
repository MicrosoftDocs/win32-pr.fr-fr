---
description: cette section décrit les fonctions de gestion des chaînes de l’interpréteur de commandes Windows. Les éléments de programmation expliqués dans cette documentation sont exportés par Shlwapi.dll et définis dans Shlwapi. h et Shlwapi. lib.
title: Fonctions de gestion des chaînes de Shell
ms.topic: article
ms.date: 05/31/2018
ms.assetid: c7329e22-c9bf-4845-bc0a-a155d1bd2005
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 4f738b6dfb2f84cac387a113a001c156b892a89fbaa0093e5f9cbeee736990d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111109"
---
# <a name="shell-string-handling-functions"></a>Fonctions de gestion des chaînes de Shell

cette section décrit les fonctions de gestion des chaînes de l’interpréteur de commandes Windows. Les éléments de programmation expliqués dans cette documentation sont exportés par Shlwapi.dll et définis dans Shlwapi. h et Shlwapi. lib.

## <a name="in-this-section"></a>Contenu de cette section



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Rubrique</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-chrcmpia"><strong>ChrCmpI</strong></a><br/></td>
<td>Effectue une comparaison entre deux caractères. La comparaison ne respecte pas la casse.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-getacceptlanguagesa"><strong>GetAcceptLanguages</strong></a><br/></td>
<td>Récupère une chaîne utilisée avec des sites Web lors de la spécification des préférences linguistiques.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqna"><strong>IntlStrEqN</strong></a><br/></td>
<td>Effectue une comparaison respectant la casse d’un nombre spécifié de caractères à partir du début de deux chaînes localisées.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqnia"><strong>IntlStrEqNI</strong></a><br/></td>
<td>Effectue une comparaison ne respectant pas la casse d’un nombre spécifié de caractères à partir du début de deux chaînes localisées.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-intlstreqworkera"><strong>IntlStrEqWorker</strong></a><br/></td>
<td>Compare un nombre spécifié de caractères à partir du début de deux chaînes localisées.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-ischarspacea"><strong>IsCharSpace</strong></a><br/></td>
<td>Détermine si un caractère représente un espace.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shloadindirectstring"><strong>SHLoadIndirectString</strong></a><br/></td>
<td>Extrait une ressource de texte spécifiée lorsque cette ressource est fournie sous la forme d’une chaîne indirecte (une chaîne commençant par le symbole' @ ').<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-shstrdupa"><strong>SHStrDup</strong></a><br/></td>
<td>Effectue une copie d’une chaîne dans la mémoire nouvellement allouée.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatw"><strong>StrCat</strong></a><br/></td>
<td>Ajoute une chaîne à une autre. <br/>
<blockquote>
[!Note]<br />
Ne pas utiliser. Pour connaître les autres fonctions, consultez la section Notes.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatbuffa"><strong>StrCatBuff</strong></a><br/></td>
<td>Copie et ajoute des caractères d’une chaîne à la fin d’une autre. <br/>
<blockquote>
[!Note]<br />
Ne pas utiliser. Pour connaître les autres fonctions, consultez la section Notes.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcatchainw"><strong>StrCatChainW</strong></a><br/></td>
<td>Concatène deux chaînes Unicode. Utilisé lorsque des concaténations répétées dans la même mémoire tampon sont requises.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchra"><strong>StrChr</strong></a><br/></td>
<td>Recherche dans une chaîne la première occurrence d’un caractère qui correspond au caractère spécifié. La comparaison respecte la casse.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchria"><strong>StrChrI</strong></a><br/></td>
<td>Recherche dans une chaîne la première occurrence d’un caractère qui correspond au caractère spécifié. La comparaison ne respecte pas la casse.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchrniw"><strong>StrChrNIW</strong></a><br/></td>
<td>Recherche dans une chaîne la première occurrence d’un caractère spécifié. La comparaison ne respecte pas la casse.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strchrnw"><strong>StrChrNW</strong></a><br/></td>
<td>Recherche dans une chaîne la première occurrence d’un caractère spécifié. La comparaison respecte la casse.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpw"><strong>StrCmp</strong></a><br/></td>
<td>Compare deux chaînes pour déterminer si elles sont identiques. La comparaison respecte la casse.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpca"><strong>StrCmpC</strong></a><br/></td>
<td>Compare les chaînes à l’aide des règles de classement du runtime C (ASCII). La comparaison respecte la casse.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpiw"><strong>StrCmpI</strong></a><br/></td>
<td>Compare deux chaînes pour déterminer si elles sont identiques. La comparaison ne respecte pas la casse.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpica"><strong>StrCmpIC</strong></a><br/></td>
<td>Compare deux chaînes à l’aide de règles de classement Runtime C (ASCII). La comparaison ne respecte pas la casse.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmplogicalw"><strong>StrCmpLogicalW</strong></a><br/></td>
<td>Compare deux chaînes Unicode. Les chiffres dans les chaînes sont considérés comme du contenu numérique plutôt que du texte. Ce test ne respecte pas la casse.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpna"><strong>StrCmpN</strong></a><br/></td>
<td>Compare un nombre spécifié de caractères à partir du début de deux chaînes pour déterminer s’ils sont identiques. La comparaison respecte la casse. La macro <strong>StrNCmp</strong> diffère de cette fonction dans nom uniquement.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnca"><strong>StrCmpNC</strong></a><br/></td>
<td>Compare un nombre spécifié de caractères à partir du début de deux chaînes à l’aide des règles de classement Runtime C (ASCII). La comparaison respecte la casse.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnia"><strong>StrCmpNI</strong></a><br/></td>
<td>Compare un nombre spécifié de caractères à partir du début de deux chaînes pour déterminer s’ils sont identiques. La comparaison ne respecte pas la casse. La macro <strong>StrNCmpI</strong> diffère de cette fonction dans nom uniquement.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcmpnica"><strong>StrCmpNIC</strong></a><br/></td>
<td>Compare un nombre spécifié de caractères à partir du début de deux chaînes à l’aide des règles de classement Runtime C (ASCII). La comparaison ne respecte pas la casse.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcpyw"><strong>StrCpy</strong></a><br/></td>
<td>Copie une chaîne dans une autre. <br/>
<blockquote>
[!Note]<br />
Ne pas utiliser. Pour connaître les autres fonctions, consultez la section Notes.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcpynw"><strong>StrCpyN</strong></a><br/></td>
<td>Copie un nombre spécifié de caractères à partir du début d’une chaîne vers une autre.<br/>
<blockquote>
[!Note]<br />
N’utilisez pas cette fonction ou la macro <strong>StrNCpy</strong> . Pour connaître les autres fonctions, consultez la section Notes.
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcspna"><strong>StrCSpn</strong></a><br/></td>
<td>Recherche dans une chaîne la première occurrence d’un groupe de caractères. La méthode de recherche respecte la casse et le caractère <strong>null</strong> de fin est inclus dans la correspondance du modèle de recherche.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strcspnia"><strong>StrCSpnI</strong></a><br/></td>
<td>Recherche dans une chaîne la première occurrence d’un groupe de caractères. La méthode de recherche ne respecte pas la casse et le caractère <strong>null</strong> de fin est inclus dans la correspondance du modèle de recherche.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strdupa"><strong>StrDup</strong></a><br/></td>
<td>Duplique une chaîne.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesize64a"><strong>StrFormatByteSize64</strong></a><br/></td>
<td>Convertit une valeur numérique en une chaîne qui représente le nombre exprimé sous la forme d’une valeur de taille en octets, kilo-octets, mégaoctets ou gigaoctets, selon la taille.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizea"><strong>StrFormatByteSizeA</strong></a><br/></td>
<td>Convertit une valeur numérique en une chaîne qui représente le nombre exprimé sous la forme d’une valeur de taille en octets, kilo-octets, mégaoctets ou gigaoctets, selon la taille. Diffère de <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a> dans un type de paramètre.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizeex"><strong>StrFormatByteSizeEx</strong></a><br/></td>
<td>Convertit une valeur numérique en une chaîne qui représente le nombre en octets, en kilo-octets, en mégaoctets ou en gigaoctets, selon la taille. Étend <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a> en offrant la possibilité d’arrondir au chiffre le plus proche affiché ou de supprimer les chiffres incomplets.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizew"><strong>StrFormatByteSizeW</strong></a><br/></td>
<td>Convertit une valeur numérique en une chaîne qui représente le nombre exprimé sous la forme d’une valeur de taille en octets, kilo-octets, mégaoctets ou gigaoctets, selon la taille. Diffère de <a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatbytesizea"><strong>StrFormatByteSizeA</strong></a> dans un type de paramètre.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strformatkbsizea"><strong>StrFormatKBSize</strong></a><br/></td>
<td>Convertit une valeur numérique en une chaîne qui représente le nombre exprimé en kilo-octets comme valeur de taille.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strfromtimeintervala"><strong>StrFromTimeInterval</strong></a><br/></td>
<td>Convertit un intervalle de temps, exprimé en millisecondes, en une chaîne.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strisintlequala"><strong>StrIsIntlEqual</strong></a><br/></td>
<td>Compare un nombre spécifié de caractères à partir du début de deux chaînes pour déterminer si elles sont égales.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strncata"><strong>StrNCat</strong></a><br/></td>
<td>Ajoute un nombre spécifié de caractères à partir du début d’une chaîne à la fin d’un autre. <br/>
<blockquote>
[!Note]<br />
N’utilisez pas cette fonction ou la macro <strong>StrCatN</strong> . Pour connaître les autres fonctions, consultez la section Notes.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strpbrka"><strong>StrPBrk</strong></a><br/></td>
<td>Recherche dans une chaîne la première occurrence d’un caractère contenu dans une mémoire tampon spécifiée. Cette recherche n’inclut pas le caractère null de fin.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrchra"><strong>StrRChr</strong></a><br/></td>
<td>Recherche dans une chaîne la dernière occurrence d’un caractère spécifié. La comparaison respecte la casse.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrchria"><strong>StrRChrI</strong></a><br/></td>
<td>Recherche dans une chaîne la dernière occurrence d’un caractère spécifié. La comparaison ne respecte pas la casse.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobstr"><strong>StrRetToBSTR</strong></a><br/></td>
<td>Accepte une structure <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a> retournée par <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder :: GetDisplayNameOf</strong></a> qui contient ou pointe vers une chaîne, et retourne cette chaîne en tant que <a href="/previous-versions/windows/desktop/automat/bstr"><strong>BSTR</strong></a>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa"><strong>StrRetToBuf</strong></a><br/></td>
<td>Convertit une structure <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a> retournée par <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder :: GetDisplayNameOf</strong></a> en une chaîne, puis place le résultat dans une mémoire tampon.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrettostra"><strong>StrRetToStr</strong></a><br/></td>
<td>Prend une structure <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a> retournée par <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder :: GetDisplayNameOf</strong></a> et retourne un pointeur vers une chaîne allouée contenant le nom complet.<br/></td>
</tr>
<tr class="even">
<td><a href="strrettostrn.md"><strong>StrRetToStrN</strong></a><br/></td>
<td>Prend une structure <a href="/windows/desktop/api/Shtypes/ns-shtypes-strret"><strong>STRRET</strong></a> retournée par <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof"><strong>IShellFolder :: GetDisplayNameOf</strong></a>, le convertit en une chaîne et place le résultat dans une mémoire tampon.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strrstria"><strong>StrRStrI</strong></a><br/></td>
<td>Recherche la dernière occurrence d’une sous-chaîne spécifiée dans une chaîne. La comparaison ne respecte pas la casse.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strspna"><strong>StrSpn</strong></a><br/></td>
<td>Obtient la longueur d’une sous-chaîne dans une chaîne composée uniquement de caractères contenus dans une mémoire tampon spécifiée.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstra"><strong>StrStr</strong></a><br/></td>
<td>Recherche la première occurrence d’une sous-chaîne dans une chaîne. La comparaison respecte la casse.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strstria"><strong>StrStrI</strong></a><br/></td>
<td>Recherche la première occurrence d’une sous-chaîne dans une chaîne. La comparaison ne respecte pas la casse.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtointa"><strong>StrToInt</strong></a><br/></td>
<td>Convertit une chaîne qui représente une valeur décimale en entier. La macro <strong>StrToLong</strong> est identique à cette fonction.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtoint64exa"><strong>StrToInt64Ex</strong></a><br/></td>
<td>Convertit une chaîne représentant une valeur décimale ou hexadécimale en entier 64 bits.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtointexa"><strong>StrToIntEx</strong></a><br/></td>
<td>Convertit une chaîne représentant un nombre décimal ou hexadécimal en entier.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-strtrima"><strong>StrTrim</strong></a><br/></td>
<td>Supprime les caractères de début et de fin spécifiés d’une chaîne.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-wnsprintfa"><strong>wnsprintf</strong></a><br/></td>
<td>Prend une liste d’arguments de longueur variable et retourne les valeurs des arguments sous la forme d’une chaîne mise en forme de style <a href="https://www.microsoft.com/download/details.aspx?id=55979"><strong>printf</strong></a>. <br/>
<blockquote>
[!Note]<br />
N’utilisez pas cette fonction. Pour connaître les autres fonctions, consultez la section Notes.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Shlwapi/nf-shlwapi-wvnsprintfa"><strong>wvnsprintf</strong></a><br/></td>
<td>Prend une liste d’arguments et retourne les valeurs des arguments sous la forme d’une chaîne mise en forme de style <a href="https://www.microsoft.com/download/details.aspx?id=55979"><strong>printf</strong></a>. <br/>
<blockquote>
[!Note]<br />
N’utilisez pas cette fonction. Pour connaître les autres fonctions, consultez la section Notes.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

 

 
