---
description: L’arabe et de nombreuses autres langues ont des formes classiques pour les nombres qui diffèrent des chiffres occidentaux conventionnels les plus souvent utilisés sur les ordinateurs.
ms.assetid: 6b5267d8-b102-410c-bdc9-831555ca2f84
title: Formes de chiffres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 03fa63f26cceb3c3e819e754461330bb190a260013211c4a37e05eb0c816164d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120083019"
---
# <a name="digit-shapes"></a>Formes de chiffres

L’arabe et de nombreuses autres langues ont des formes classiques pour les nombres qui diffèrent des chiffres occidentaux conventionnels les plus souvent utilisés sur les ordinateurs. Pour éviter toute ambiguïté lors de l’attribution d’un nom à ces formes, ce document utilise les noms suivants de la norme Unicode.



| Nom Unicode des chiffres                                     | Pays/région utilisé (e)                                    |
|----------------------------------------------------------------|--------------------------------------------------------------|
| Chiffres européens                                                | Europe, Amérique et dans de nombreux autres pays/régions       |
| Chiffres Arabic-Indic                                            | Pays/régions arabes (bien que beaucoup utilisent des chiffres européens) |
| Autres chiffres nationaux : chiffres indo-aryens, chiffres thaïs et similaires | Différents pays/régions                                    |



 

Unicode fournit des points de code distincts pour chaque forme de chiffre. Ainsi, pour accéder à des formes de chiffres de langue spéciales, votre application peut utiliser les codes de caractères Unicode appropriés pour les chiffres ci-dessus, U + 0030 à U + 0039. Ces codes sont toujours affichés avec la forme appropriée, selon la disponibilité de la police.

Les codes de caractères Unicode U + 0030 à U + 0039 représentent les chiffres européens de 0 à 9, mais leur forme de chiffres peut être modifiée. les api de texte GDI et DirectWrite fournissent des mécanismes permettant aux applications de contrôler ce comportement. (Voir, par exemple, [**ScriptApplyDigitSubstitution**](/windows/desktop/api/Usp10/nf-usp10-scriptapplydigitsubstitution) ou [**IDWriteTextAnalysisSink :: SetNumberSubstitution**](/windows/win32/api/dwrite/nf-dwrite-idwritetextanalysissink-setnumbersubstitution).) Le comportement dans certains contrôles de l’interpréteur de commandes et les infrastructures d’interface utilisateur peut répondre aux paramètres régionaux de l’utilisateur pour la substitution de chiffres ; les paramètres [régionaux \_ IDIGITSUBSTITUTION](locale-idigitsubstitution.md) LCTYPE peuvent être utilisés pour obtenir les paramètres de substitution de chiffres par défaut pour différents paramètres régionaux ou les paramètres de bureau de l’utilisateur actuel pour la substitution de chiffres.

## <a name="native-digits"></a>Chiffres natifs

Les chiffres natifs sont les formes de chiffres choisies par l’utilisateur dans la feuille de propriétés **nombre** dans la partie Options régionales et linguistiques du panneau de configuration. Pour trouver la présentation de chiffres préférée par l’utilisateur, votre application utilise la fonction [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa) ou [**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex) avec la constante [ \_ SNATIVEDIGITS locale](locale-snative-constants.md) qui représente les informations de paramètres régionaux.

> [!Note]  
> En règle générale, les codes numériques Unicode sont générés dans les routines du système d’exploitation du Runtime. Par conséquent, les systèmes d’exploitation Common Runtime doivent être mis à niveau pour que l’application inspecte les [paramètres régionaux \_ SNATIVEDIGITS](locale-snative-constants.md) de manière appropriée.

 

## <a name="digit-substitution"></a>Substitution de chiffres

L’application peut utiliser la substitution de chiffres pour indiquer au système d’exploitation comment imprimer les chiffres U + 0030 à U + 0039. La constante [ \_ IDIGITSUBSTITUTION de paramètres régionaux](locale-idigitsubstitution.md) contrôle cette opération.

## <a name="digit-shaping-for-a-single-function"></a>Mise en forme des chiffres pour une fonction unique

Les fonctions de [ \_ résultats](/windows/win32/api/wingdi/ns-wingdi-gcp_resultsa) [ExtTextOut](/windows/win32/api/wingdi/nf-wingdi-exttextouta), [GetCharacterPlacement](/windows/win32/api/wingdi/nf-wingdi-getcharacterplacementa)et GCP ont des indicateurs qui régissent la substitution des codes Unicode U + 0030 à u + 0039 pour la durée de l’appel de fonction. Ces indicateurs remplacent les paramètres régionaux dans le panneau de configuration, mais ne réinitialisent pas les paramètres. En outre, ils ne remplacent pas les codes Unicode NADS et nœuds. Les indicateurs suivants sont disponibles.



| Indicateurs                 | Chiffres utilisés                      | Utilisé dans                   |
|-----------------------|----------------------------------|---------------------------|
| \_NUMERICSLATIN ETO    | Chiffres européens                  | **ExtTextOut**            |
| \_NUMERICSLOCAL ETO    | Chiffres appropriés aux paramètres régionaux | **ExtTextOut**            |
| GCP \_ NUMERICSLATIN    | Chiffres européens                  | **GetCharacterPlacement** |
| GCP \_ NUMERICSLOCAL    | Chiffres appropriés aux paramètres régionaux | **GetCharacterPlacement** |
| GCPCLASS \_ LATINNUMBER | Chiffres européens                  | **résultats de GCP \_**          |
| GCPCLASS \_ LOCALNUMBER | Chiffres appropriés aux paramètres régionaux | **résultats de GCP \_**          |



 

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos de la prise en charge linguistique nationale](about-national-language-support.md)
</dt> <dt>

[**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)
</dt> <dt>

[**GetLocaleInfoEx**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoex)
</dt> </dl>

 

 
