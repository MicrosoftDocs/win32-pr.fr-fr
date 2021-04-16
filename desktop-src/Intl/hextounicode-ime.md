---
description: La modification enrichie 3,0 prend en charge l’IME HexToUnicode, qui permet à un utilisateur d’effectuer une conversion entre des caractères hexadécimaux et Unicode à l’aide de touches d’accès rapide de l’une des deux manières suivantes.
ms.assetid: 4b8c4de4-9c1c-459c-a640-367e86a9b9cc
title: IME HexToUnicode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 88042ce276082755613b28a7e4d070c8b3d695f5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104530315"
---
# <a name="hextounicode-ime"></a>IME HexToUnicode

La modification enrichie 3,0 prend en charge l’IME HexToUnicode, qui permet à un utilisateur d’effectuer une conversion entre des caractères hexadécimaux et Unicode à l’aide de touches d’accès rapide de l’une des deux manières suivantes.

À l’aide de la première méthode de conversion, l’utilisateur tape le code de caractère au format hexadécimal, puis entre ALT + X. L’IME remplace les chiffres hexadécimaux précédant le point d’insertion par le caractère Unicode. Si la police actuelle ne prend pas en charge le code de caractère, une police appropriée qui la prend en charge est sélectionnée. Pour convertir du format Unicode au format hexadécimal, l’utilisateur entre MAJ + ALT + X. Cette entrée remplace le caractère Unicode qui précède le point d’insertion par les chiffres hexadécimaux. En particulier, cette méthode permet à l’utilisateur de déterminer le caractère indiqué par un indicateur « glyphe manquant ». Si le code de caractère hexadécimal suit immédiatement certains caractères hexadécimaux (non caractères) légitimes, l’utilisateur sélectionne les chiffres spécifiques à convertir avant de taper ALT + X. L’un des problèmes de cette première méthode est que ALT + X est parfois utilisé comme combinaison de touches pour la commande Exit (autrement dit, eXit). Par exemple, dans Microsoft Office, cette commande s’affiche uniquement sous la forme d’une option du menu **fichier** .

La deuxième méthode de conversion entre les caractères hexadécimal et Unicode implique le pavé numérique. À l’aide de cette méthode, l’utilisateur tape des nombres ALT + pavé numérique (avec des valeurs supérieures à 255) pour entrer des caractères Unicode à l’aide de valeurs décimales. Cette méthode n’est pas aussi utile que la première car l’utilisateur ne peut pas voir les chiffres hexadécimaux qui ont été tapés. En outre, l’utilisateur ne peut pas corriger les chiffres hexadécimaux, sauf en entrant à nouveau tous les chiffres.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[À propos du gestionnaire de méthode d’entrée](about-input-method-manager.md)
</dt> </dl>

 

 



