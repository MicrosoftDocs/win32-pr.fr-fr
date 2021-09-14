---
title: Indicateurs pour le mode de conversion (Ctffunc. h)
description: Les indicateurs suivants sont utilisés comme valeur de la \_ conversion de \_ INPUTMODE clavier de compartiment de GUID \_ \_ . Cela équivaut aux \_ valeurs CMODE IME pour imm32.
ms.assetid: 6e545af5-5fdb-49de-b24e-aaee82b51326
keywords:
- Indicateurs pour le mode de conversion Text Services Framework
topic_type:
- apiref
api_name:
- Flags for Conversion Mode
api_location:
- Ctffunc.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 022712ff45f213992bf3d40bd0149959e4864faa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127193523"
---
# <a name="flags-for-conversion-mode"></a>Indicateurs pour le mode de conversion

Les indicateurs suivants sont utilisés comme valeur de la [ \_ conversion de \_ \_ INPUTMODE clavier \_ de compartiment de GUID](predefined-compartments.md). Cela équivaut aux valeurs [ \_ CMODE IME](../intl/ime-conversion-mode-values.md) pour imm32.



| Indicateur                             | Valeur  | Description                                                     |
|----------------------------------|--------|-----------------------------------------------------------------|
| \_CONVERSIONMODE TF \_ | 0x0000 | Affectez la valeur 1 à en mode alphanumérique.                                  |
| CONVERSIONMODE TF en \_ \_ mode natif       | 0x0001 | Défini sur 1 en mode natif ; 0 si le mode est alphanumérique.                |
| TF \_ CONVERSIONMODE \_ Katakana     | 0x0002 | Défini sur 1 si le mode KATAKANA ; 0 en mode HIRAGANA.                  |
| TF \_ CONVERSIONMODE \_ FULLSHAPE    | 0x0008 | Défini sur 1 en mode de forme complète ; 0 s’il s’agit du mode demi-forme.              |
| TF \_ CONVERSIONMODE \_ roman        | 0x0010 | Défini sur 1 pour empêcher le traitement des conversions par l’IME ; 0 dans le cas contraire. |
| TF \_ CONVERSIONMODE \_ CHARCODE     | 0x0020 | Défini sur 1 si le mode de saisie du code du caractère ; 0 dans le cas contraire.                |
| TF \_ CONVERSIONMODE \_ | 0x0080 | Défini sur 1 si le mode de clavier logiciel est activé ; 0 dans le cas contraire.                       |
| TF \_ CONVERSIONMODE \_ noconversion | 0x0100 | Défini sur 1 pour empêcher le traitement des conversions par l’IME ; 0 dans le cas contraire. |
| \_symbole TF CONVERSIONMODE \_       | 0x0400 | Défini sur 1 si le mode de conversion des symboles ; 0 dans le cas contraire.                   |
| \_CONVERSIONMODE TF \_ fixe        | 0x0800 | Défini sur 1 si le mode de conversion est fixe ; 0 dans le cas contraire.                    |



 

Les valeurs suivantes sont utilisées comme valeur de la [ \_ \_ \_ \_ phrase INPUTMODE du clavier du compartiment GUID](predefined-compartments.md). Cela équivaut aux valeurs [ \_ SMODE IME](../intl/ime-composition-string-values.md) pour imm32.



| Indicateur                            | Valeur  | Description                                                                |
|---------------------------------|--------|----------------------------------------------------------------------------|
| TF \_ SENTENCEMODE \_ aucun          | 0x0000 | Aucune information pour la phrase.                                               |
| TF \_ SENTENCEMODE \_ PLAURALCLAUSE | 0x0001 | L’IME utilise des informations de clause pluriel pour effectuer le traitement de la conversion. |
| TF \_ SENTENCEMODE \_ SINGLECONVERT | 0x0002 | L’IME effectue le traitement de la conversion en mode à un seul caractère.        |
| \_SENTENCEMODE TF \_ automatique     | 0x0004 | L’IME effectue le traitement de la conversion en mode automatique.               |
| TF \_ SENTENCEMODE \_ PHRASEPREDICT | 0x0008 | L’IME utilise les informations d’expression pour prédire le caractère suivant.             |
| \_conversation TF SENTENCEMODE \_  | 0x0010 | L’IME utilise le mode conversation. Cela est utile pour les applications de conversation.      |



 

## <a name="requirements"></a>Spécifications



| Condition requise | Valeur |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Client minimal pris en charge<br/> | Windows 2000 Professionnel - \[Applications de bureau uniquement\]<br/>                             |
| Serveur minimal pris en charge<br/> | Windows 2000 Server - \[Applications de bureau uniquement\]<br/>                                   |
| Composant redistribuable<br/>          | TSF 1,0 onWindows NT 4,0, Windows 2000 ProfessionalandWindows MeWindows 98<br/>   |
| En-tête<br/>                   | <dl> <dt>Ctffunc. h</dt> </dl>   |
| MIDL<br/>                      | <dl> <dt>Ctffunc. idl</dt> </dl> |



## <a name="see-also"></a>Voir aussi

<dl> <dt>

[Compartiments prédéfinis](predefined-compartments.md)
</dt> </dl>

 

