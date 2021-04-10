---
title: Utilisation de macros pour la gestion des erreurs
description: COM définit un certain nombre de macros qui facilitent l’utilisation des valeurs HRESULT.
ms.assetid: ad28eb80-cab9-4bec-9601-34660f6dcad4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6605ecc05f2d24d3671d28becd770b15d56e1413
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/21/2020
ms.locfileid: "103730421"
---
# <a name="using-macros-for-error-handling"></a>Utilisation de macros pour la gestion des erreurs

COM définit un certain nombre de macros qui facilitent l’utilisation des valeurs **HRESULT** .

Les macros de gestion des erreurs sont décrites dans le tableau suivant.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Macro</th>
<th>Description</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/dmerror/nf-dmerror-make_hresult"><strong>MAKE_HRESULT</strong></a><br/></td>
<td>Retourne un <strong>HRESULT</strong> en fonction du bit de gravité, du code d’installation et du code d’erreur qui composent le <strong>HRESULT</strong>.<br/>
<blockquote>
[!Note]<br />
L’appel de <a href="/windows/desktop/api/dmerror/nf-dmerror-make_hresult"><strong>MAKE_HRESULT</strong></a> pour la vérification de S_OK entraîne une baisse des performances. Vous ne devez pas utiliser régulièrement <strong>MAKE_HRESULT</strong> pour obtenir des résultats corrects.
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-make_scode"><strong>MAKE_SCODE</strong></a><br/></td>
<td>Retourne un <strong>SCODE</strong> en fonction du bit de gravité, du code d’installation et du code d’erreur qui composent le <strong>SCODE</strong>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_code"><strong>HRESULT_CODE</strong></a><br/></td>
<td>Extrait la partie du code d’erreur de <strong>HRESULT</strong>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_facility"><strong>HRESULT_FACILITY</strong></a><br/></td>
<td>Extrait le code d’installation de la valeur <strong>HRESULT</strong>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_severity"><strong>HRESULT_SEVERITY</strong></a><br/></td>
<td>Extrait le bit de gravité de <strong>HRESULT</strong>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-scode_code"><strong>SCODE_CODE</strong></a><br/></td>
<td>Extrait la partie du code d’erreur du <strong>SCODE</strong>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-scode_facility"><strong>SCODE_FACILITY</strong></a><br/></td>
<td>Extrait le code d’installation du <strong>SCODE</strong>.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-scode_severity"><strong>SCODE_SEVERITY</strong></a><br/></td>
<td>Extrait le champ de gravité du <strong>SCODE</strong>.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-succeeded"><strong>A réussi</strong></a><br/></td>
<td>Teste le bit de gravité de <strong>SCODE</strong> ou <strong>HRESULT</strong>; retourne la <strong>valeur true</strong> si la gravité est égale à zéro et la <strong>valeur false</strong> si c’est un.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-failed"><strong>DÉFECTUEUX</strong></a><br/></td>
<td>Teste le bit de gravité de <strong>SCODE</strong> ou <strong>HRESULT</strong>; retourne la <strong>valeur true</strong> si la gravité est égale à 1 et <strong>false</strong> si elle est égale à zéro.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-is_error"><strong>IS_ERROR</strong></a><br/></td>
<td>Fournit un test générique des erreurs sur toute valeur d’État. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_from_win32"><strong>HRESULT_FROM_WIN32</strong></a><br/></td>
<td>Mappe un <a href="/windows/desktop/Debug/system-error-codes">code d’erreur système</a> à une valeur <strong>HRESULT</strong> . <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Winerror/nf-winerror-hresult_from_nt"><strong>HRESULT_FROM_NT</strong></a><br/></td>
<td>Mappe une valeur d’état NT à une valeur <strong>HRESULT</strong> .<br/></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestion des erreurs dans COM](error-handling-in-com.md)
</dt> </dl>

 

