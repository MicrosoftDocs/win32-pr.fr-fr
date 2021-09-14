---
title: Utilisation de macros pour la gestion des erreurs
description: COM définit un certain nombre de macros qui facilitent l’utilisation des valeurs HRESULT.
ms.assetid: ad28eb80-cab9-4bec-9601-34660f6dcad4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2f31280ec2076f8ece1fcf15dd6e27629a3016e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "126923055"
---
# <a name="using-macros-for-error-handling"></a>Utilisation de macros pour la gestion des erreurs

COM définit un certain nombre de macros qui facilitent l’utilisation des valeurs **HRESULT** .

Les macros de gestion des erreurs sont décrites dans le tableau suivant.




| Macro | Description | 
|-------|-------------|
| <a href="/windows/desktop/api/dmerror/nf-dmerror-make_hresult"><strong>MAKE_HRESULT</strong></a><br /> | Retourne un <strong>HRESULT</strong> en fonction du bit de gravité, du code d’installation et du code d’erreur qui composent le <strong>HRESULT</strong>.<br /><blockquote>[!Note]<br />L’appel de <a href="/windows/desktop/api/dmerror/nf-dmerror-make_hresult"><strong>MAKE_HRESULT</strong></a> pour la vérification de S_OK entraîne une baisse des performances. Vous ne devez pas utiliser régulièrement <strong>MAKE_HRESULT</strong> pour obtenir des résultats corrects.</blockquote><br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-make_scode"><strong>MAKE_SCODE</strong></a><br /> | Retourne un <strong>SCODE</strong> en fonction du bit de gravité, du code d’installation et du code d’erreur qui composent le <strong>SCODE</strong>.<br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-hresult_code"><strong>HRESULT_CODE</strong></a><br /> | Extrait la partie du code d’erreur de <strong>HRESULT</strong>.<br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-hresult_facility"><strong>HRESULT_FACILITY</strong></a><br /> | Extrait le code d’installation de la valeur <strong>HRESULT</strong>.<br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-hresult_severity"><strong>HRESULT_SEVERITY</strong></a><br /> | Extrait le bit de gravité de <strong>HRESULT</strong>.<br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-scode_code"><strong>SCODE_CODE</strong></a><br /> | Extrait la partie du code d’erreur du <strong>SCODE</strong>.<br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-scode_facility"><strong>SCODE_FACILITY</strong></a><br /> | Extrait le code d’installation du <strong>SCODE</strong>.<br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-scode_severity"><strong>SCODE_SEVERITY</strong></a><br /> | Extrait le champ de gravité du <strong>SCODE</strong>.<br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-succeeded"><strong>A réussi</strong></a><br /> | Teste le bit de gravité de <strong>SCODE</strong> ou <strong>HRESULT</strong>; retourne la <strong>valeur true</strong> si la gravité est égale à zéro et la <strong>valeur false</strong> si c’est un.<br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-failed"><strong>DÉFECTUEUX</strong></a><br /> | Teste le bit de gravité de <strong>SCODE</strong> ou <strong>HRESULT</strong>; retourne la <strong>valeur true</strong> si la gravité est égale à 1 et <strong>false</strong> si elle est égale à zéro.<br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-is_error"><strong>IS_ERROR</strong></a><br /> | Fournit un test générique des erreurs sur toute valeur d’État. <br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-hresult_from_win32"><strong>HRESULT_FROM_WIN32</strong></a><br /> | Cartes un <a href="/windows/desktop/Debug/system-error-codes">code d’erreur système</a> à une valeur <strong>HRESULT</strong> . <br /> | 
| <a href="/windows/desktop/api/Winerror/nf-winerror-hresult_from_nt"><strong>HRESULT_FROM_NT</strong></a><br /> | Cartes une valeur d’état NT à une valeur <strong>HRESULT</strong> .<br /> | 




 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestion des erreurs dans COM](error-handling-in-com.md)
</dt> </dl>

 

