---
description: Windows permet la définition locale de caractères non standard dans les jeux de caractères codés sur deux octets (dbcs) et Unicode.
ms.assetid: 32d0ddab-4b3f-473e-bf92-3230b3746079
title: Jeux de caractères et polices
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eeee925f55887ac8120474f14b727ea244dc02c3b1e7908f424c0dbf09d502b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068279"
---
# <a name="character-sets-and-fonts"></a>Jeux de caractères et polices

Windows permet la définition locale de caractères non standard dans les [jeux de caractères codés sur deux octets](double-byte-character-sets.md) (dbcs) et [Unicode](unicode.md). Pour un DBCS, ces caractères non standard sont connus sous le nom de caractères définis par l’utilisateur final (EUDC). Unicode offre une fonctionnalité similaire par le biais de sa zone d’utilisation privée (PUA). Les applications identifient un caractère spécifié à l’aide de la valeur de caractère DBCS ou Unicode associée.

Les valeurs de caractères DBCS qui peuvent être assignées dépendent du jeu de caractères spécifié. chaque [page de codes](code-pages.md) Windows d’extrême-orient a au moins une plage de valeurs réservées à utiliser comme EUDCs. Les plages sont définies par la clé de Registre [EUDCCodeRange](eudccoderange.md) . Les valeurs Unicode à cet effet proviennent toujours des PUA Unicode, des valeurs U + E000 à U + F8FF, U + F0000 à U + FFFFD et de U + 100000 à U + 10FFFD.

Pour créer un caractère EUDC ou PUA, l’utilisateur choisit une valeur de caractère comprise dans la plage spécifiée et ajoute le [glyphe](uniscribe-glossary.md) à la police de l’entrée qui correspond à cette valeur de caractère. L’utilisateur crée le glyphe à l’aide d’un éditeur EUDC ou à l’aide d’un package de polices acheté auprès d’un fournisseur de polices. Toute police DBCS peut contenir EUDCs et toute police Unicode peut contenir des caractères PUA. La police est appelée une police EUDC/PUA « distincte » si elle contient uniquement des EUDCs. La police est une police EUDC/PUA « intégrée » si elle contient des caractères standard et EUDCs.

La police EUDC/PUA par défaut du système est une police que le système d’exploitation associe automatiquement à toutes les polices DBCS et Unicode, à l’exception des polices qui ont des polices EUDC/PUA explicitement associées. Les applications définissent la police EUDC/PUA par défaut du système en définissant la valeur du nom de SystemDefaultEUDCFont sous la clé de Registre [EUDC](eudc.md) . De même, les applications peuvent associer des polices EUDC/PUA distinctes aux polices correspondantes en spécifiant un nom de police et un fichier de police associé sous la clé EUDC. Le système d’exploitation tente toujours d’abord de trouver le EUDC/PUA dans la police actuellement sélectionnée. Si la police est introuvable, le système d’exploitation recherche le caractère dans la police EUDC/PUA associée, s’il a été défini pour la police actuellement sélectionnée. S’il ne parvient toujours pas à trouver le caractère, le système d’exploitation le recherche dans la police EUDC/PUA par défaut du système.

Les polices TrueType peuvent être installées sous forme de fichiers. ttf ou de fichiers. TTE. Étant donné que le système d’exploitation masque les fichiers. TTE, les applications ne peuvent pas énumérer ou examiner les polices installées à l’aide des fonctions de l’API GDI. Sur de nombreux systèmes d’exploitation, la police par défaut EUDC/PUA et les polices EUDC/PUA distinctes sont installées en tant que fichiers. TTE. Les applications telles que les éditeurs EUDC et le panneau de configuration doivent utiliser des entrées de Registre pour ajouter, modifier et supprimer ces polices.

L’utilisation de caractères EUDC et PUA ne permet pas de conserver une signification fiable sur différents ordinateurs ou jeux de caractères. Pour plus d’informations sur l’utilisation des caractères EUDC et PUA, consultez [caractères de zone d’utilisation privée et définie](end-user-defined-characters.md) par l’utilisateur.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Caractères de zone d’utilisation privée et définis par l’utilisateur](end-user-defined-characters.md)
</dt> </dl>

 

 



