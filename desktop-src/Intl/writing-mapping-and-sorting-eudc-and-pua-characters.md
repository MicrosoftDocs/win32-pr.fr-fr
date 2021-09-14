---
description: Les applications écrivent des caractères définis par l’utilisateur (EUDCs) et des caractères de zone d’utilisation privée (PUA) sur l’écran ou l’imprimante, tout comme ils écrivent d’autres caractères, à l’aide de fonctions de sortie telles que TextOut et ExtTextOut.
ms.assetid: c975c70d-4231-4a69-bec2-d51d6993fdd4
title: Écriture, mappage et tri des caractères EUDC et PUA
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6c34264d956bb6a87407e249f68b2bc03fb2c99
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/13/2021
ms.locfileid: "127009799"
---
# <a name="writing-mapping-and-sorting-eudc-and-pua-characters"></a>Écriture, mappage et tri des caractères EUDC et PUA

Les applications écrivent des caractères définis par l’utilisateur (EUDCs) et des caractères de zone d’utilisation privée (PUA) sur l’écran ou l’imprimante, tout comme ils écrivent d’autres caractères, à l’aide de fonctions de sortie telles que [TextOut](/windows/win32/api/wingdi/nf-wingdi-textouta) et [ExtTextOut](/windows/win32/api/wingdi/nf-wingdi-exttextouta). Ces fonctions récupèrent automatiquement les informations de caractères à partir des polices de caractères EUDC ou PUA si EUDC est activé. Pour plus d’informations, consultez [caractères de \_ zone d’utilisation privée et définis par l’utilisateur final](end-user-defined-characters.md).

Lors de l’écriture de caractères EUDCs ou PUA, l’opération de la fonction Text output dépend de la police actuellement sélectionnée. Si la police sélectionnée est une police de caractères EUDC ou PUA intégrée, la fonction extrait les informations de caractères de cette police. Si la police sélectionnée est un [jeu de caractères codés sur deux octets](double-byte-character-sets.md) (DBCS) TrueType auquel est associée une police EUDC distincte, la fonction récupère les informations de la police EUDC spécifiée. De même, si la police sélectionnée est une police TrueType [Unicode](unicode.md) associée à une police de caractères PUA distincte, la fonction récupère les informations de la police de caractères PUA. Si la police sélectionnée n’est pas associée à une police de caractères EUDC ou PUA, la fonction récupère les informations à partir de la police EUDC par défaut du système. Si le caractère n’est pas dans la police EUDC par défaut du système ou qu’il n’existe aucune police EUDC par défaut du système, la fonction écrit le caractère par défaut défini par la police sélectionnée.

Les applications peuvent mapper des EUDCs vers et depuis Unicode à l’aide des fonctions [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) et [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) . La fonction **MultiByteToWideChar** mappe la plupart des EUDCs à des caractères dans le PUA Unicode. Toutefois, pour prendre en charge certaines normes nationales ou régionales, certaines EUDCs peuvent être mappées à des points de code Unicode non PUA. La fonction **WideCharToMultiByte** mappe un caractère dans PUA à son équivalent EUDC, si un mappage de ce type existe et si le point de code n’a pas de mappage non-PUA valide dans Unicode. Toutes les pages de codes n’ont pas une plage EUDC. La page de codes spécifiée dans un appel à **WideCharToMultiByte** doit contenir une plage de code EUDC pour le mappage à la plage EUDC. Si la page de codes ne contient pas de plage de code EUDC, la fonction récupère le caractère par défaut pour tous les caractères de la PUA Unicode.

[**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar) et [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte) ne garantissent pas le mappage aller-retour. En d’autres termes, il est possible de commencer avec une chaîne multioctet particulière contenant EUDCs, de mapper la chaîne à Unicode avec **MultiByteToWideChar** et de la mapper à nouveau sur le DBCS d’origine avec **WideCharToMultiByte**, et de finir par un résultat qui n’est pas identique à la chaîne d’origine. Les applications qui reposent sur le mappage de EUDCs à Unicode doivent s’assurer que tous les caractères nécessaires peuvent aller-retour entre la zone EUDC de la page de codes appropriée et les PUA Unicode.

Les applications ne doivent pas essayer de mapper EUDCs d’une page de codes à une autre. Si une application démarre avec un EUDC à partir d’une page de codes, la mappe à Unicode avec [**MultiByteToWideChar**](/windows/desktop/api/Stringapiset/nf-stringapiset-multibytetowidechar)et est mappée à un autre DBCS avec [**WideCharToMultiByte**](/windows/desktop/api/Stringapiset/nf-stringapiset-widechartomultibyte), il n’existe aucune garantie quant aux résultats. Le caractère d’origine peut être mappé à un autre EUDC dans la page de codes de destination, ou il peut être mappé en tant que caractère non défini. De même, le mappage d’une chaîne Unicode à une page de codes qui a une plage EUDC peut avoir des résultats inattendus. Si la chaîne Unicode contient un point de code PUA, il est possible que le point de code soit mappé à un EUDC qui ne représente pas le même caractère.

Les applications peuvent comparer des chaînes DBCS qui contiennent des EUDCs à l’aide de la version ANSI de la fonction [CompareString](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) . La fonction mappe effectivement les caractères au format Unicode avant de comparer les valeurs de caractères. Les applications peuvent créer une clé de tri pour la chaîne à l’aide de la version ANSI de la fonction [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa) et de la \_ valeur SortKey LCMAP. Cette fonction mappe en premier les caractères au format Unicode. Tous les caractères du PUA sont triés après tous les autres caractères Unicode. Dans la zone, les caractères sont triés par ordre numérique. Si une application tente de récupérer des informations CTYPE pour un EUDC à l’aide de la fonction [GetStringTypeA](/windows/desktop/api/Winnls/nf-winnls-getstringtypea) , la fonction récupère la **valeur null** pour chaque caractère.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Utilisation d’Unicode et de jeux de caractères](using-unicode-and-character-sets.md)
</dt> </dl>

 

 
