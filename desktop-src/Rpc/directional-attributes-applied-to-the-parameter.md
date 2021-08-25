---
title: Attributs directionnels appliqués au paramètre
description: Les attributs directionnels \ dans \ et \ out \ déterminent la façon dont le client et le serveur allouent et libèrent de la mémoire. Le tableau suivant résume l’effet des attributs directionnels sur l’allocation de mémoire.
ms.assetid: 21ab54c4-a707-4ee3-bea8-8ba216e25c16
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e18e34a7ea553fd5c1fd9157877a0296e403443fc490bb328f48ac4b7b2c8b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120073389"
---
# <a name="directional-attributes-applied-to-the-parameter"></a>Attributs directionnels appliqués au paramètre

Les attributs directionnels \[ [dans](/windows/desktop/Midl/in) \] et \[ [out](/windows/desktop/Midl/out-idl) \] déterminent la façon dont le client et le serveur allouent et libèrent de la mémoire. Le tableau suivant résume l’effet des attributs directionnels sur l’allocation de mémoire.



| Attribut directionnel    | Mémoire sur le client                                                                                            | Mémoire sur le serveur                                                                                                                                        |
|--------------------------|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[[dans](/windows/desktop/Midl/in)\]       | L’application cliente doit allouer avant l’appel.                                                           | Le stub serveur est alloué.                                                                                                                                  |
| \[en [sortie](/windows/desktop/Midl/out-idl)\] | Le stub client est alloué lors du retour.                                                                            | Le stub serveur alloue le pointeur de niveau supérieur uniquement. l’application serveur doit allouer tous les pointeurs incorporés. Le serveur alloue également de nouvelles données en fonction des besoins. |
| \[**in**, **out**\]      | L’application cliente doit allouer les données initiales transmises au serveur. le stub client alloue des données supplémentaires. | Le stub serveur alloue les données initiales transmises à partir du client ; l’application serveur alloue les nouvelles données en fonction des besoins.                                        |



 

Dans tous les cas, le stub client ne libère pas la mémoire. L’application cliente doit libérer la mémoire avant qu’elle ne se termine. Le stub serveur libère de la mémoire lorsque l’appel de procédure distante retourne (sous réserve de l' \[ attribut [allocate](/windows/desktop/Midl/allocate) \] ACF).

 

 