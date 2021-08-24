---
description: Les fonctions suivantes sont utilisées avec les jeux de caractères.
ms.assetid: 1799f5da-1391-4b6e-ac13-718017a77557
title: Unicode et fonctions de jeu de caractères
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd26edd8931b1a63887816ca07698d779bd0d4d3decceb3b53faf5d499605612
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811710"
---
# <a name="unicode-and-character-set-functions"></a>Unicode et fonctions de jeu de caractères

Les fonctions suivantes sont utilisées avec les jeux de caractères.



| Fonction                                                       | Description                                                                                                           |
|----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**GetTextCharset**](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharset)                       | Récupère un identificateur de jeu de caractères pour la police actuellement sélectionnée dans un contexte de périphérique spécifié.         |
| [**GetTextCharsetInfo**](/windows/desktop/api/Wingdi/nf-wingdi-gettextcharsetinfo)               | Récupère des informations sur le jeu de caractères de la police actuellement sélectionnée dans un contexte de périphérique spécifié. |
| [**IsDBCSLeadByte**](/windows/desktop/api/Winnls/nf-winnls-isdbcsleadbyte)                       | détermine si un caractère spécifié est un octet de tête pour le système par défaut Windows page de codes ANSI (CP \_ ACP).           |
| [**IsDBCSLeadByteEx**](/windows/desktop/api/Winnls/nf-winnls-isdbcsleadbyteex)                   | Détermine si un caractère spécifié est potentiellement un octet de tête.                                                       |
| [**IsTextUnicode**](/windows/desktop/api/Winbase/nf-winbase-istextunicode)                         | Détermine si une mémoire tampon est susceptible de contenir un formulaire de texte Unicode.                                                   |
| [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar)             | Cartes une chaîne de caractères en une chaîne UTF-16 (caractère élargi).                                                          |
| [**TranslateCharsetInfo**](/windows/desktop/api/Wingdi/nf-wingdi-translatecharsetinfo)           | Traduit les informations du jeu de caractères et définit tous les membres d’une structure de destination sur les valeurs appropriées.           |
| [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte)             | Cartes une chaîne UTF-16 (caractère élargi) à une nouvelle chaîne de caractères.                                                      |
| [**BytesToUnicode**](/previous-versions/dd317724(v=vs.85))                       | Ne pas utiliser.                                                                                                           |
| [**NlsDllCodePageTranslation**](/windows/desktop/api/Gb18030/nf-gb18030-nlsdllcodepagetranslation) | Ne pas utiliser.                                                                                                           |
| [**UnicodeToBytes**](/previous-versions/windows/desktop/legacy/dd374082(v=vs.85))                       | Ne pas utiliser.                                                                                                           |



 

 

 
