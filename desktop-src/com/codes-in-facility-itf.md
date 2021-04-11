---
title: Codes dans FACILITY_ITF
description: Codes dans ITF d’usine \_
ms.assetid: 1f9f7b2c-a4e4-41c0-9ba5-b8bbf722e077
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fc4375b5956502dbaee97057d347aff1da77e3a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103939799"
---
# <a name="codes-in-facility_itf"></a>Codes dans ITF d’usine \_

Les **HRESULT** s avec des fonctionnalités telles que la \_ valeur null de la base de connaissances et le RPC de la fonction \_ ont une signification universelle, car ils sont définis au niveau d’une seule source : Microsoft. Toutefois, **HRESULT** s dans ITF d’installation \_ sont déterminés par la fonction ou la méthode d’interface à partir de laquelle ils sont retournés. Cela signifie que la même valeur 32 bits dans ITF d’installation \_ retournée à partir de deux méthodes d’interface différentes peut avoir des significations différentes.

La raison pour laquelle les savesets **HRESULT** dans \_ ITF peuvent avoir des significations différentes dans des interfaces différentes est que les **HRESULT** s sont conservés à une taille de type de données efficace de 32 bits. Malheureusement, 32 bits n’est pas assez grand pour le développement d’un système d’allocation de code d’erreur qui évite les codes conflictuels alloués par différents programmeurs à des moments différents (contrairement à la gestion des identificateurs d’interface et des CLSID). Par conséquent, la valeur **HRESULT** 32 bits est structurée de sorte que Microsoft peut définir plusieurs codes d’erreur universels, tout en permettant à d’autres programmeurs de définir de nouveaux codes d’erreur sans crainte de conflit. La Convention du code d’État est la suivante :

-   Les codes d’État dans des services autres que les ITF de service \_ ne peuvent être définis que par Microsoft.
-   Les codes d’État dans les ITF d’installation de service \_ sont définis uniquement par le développeur de l’interface ou de la fonction qui retourne le code d’État. Pour éviter les codes d’erreur conflictuels, toute personne qui définit l’interface est chargée de coordonner et de publier les \_ codes d’État ITF d’installation associés à cette interface.

Tous les codes ITF de l’infrastructure définie par COM \_ ont une valeur de code comprise dans la plage 0x0000-0x01FF. Bien qu’il soit légal d’utiliser des codes dans \_ ITF d’installation, il est recommandé d’utiliser uniquement des valeurs de code dans la plage de 0x0200-0xFFFF. Cette recommandation est un moyen de réduire la confusion avec les erreurs définies par COM.

Il est également recommandé que les développeurs définissent de nouvelles fonctions et interfaces pour retourner des codes d’erreur tels que définis par COM et dans des installations autres que \_ ITF. En particulier, les interfaces qui ont des chances d’être à distance à l’aide de RPC dans le futur doivent définir les codes RPC de l’installation \_ comme valides. E \_ inattendue est un code d’erreur spécifique que la plupart des développeurs souhaitent rendre universellement légaux.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Gestion des erreurs dans COM](error-handling-in-com.md)
</dt> </dl>

 

 




