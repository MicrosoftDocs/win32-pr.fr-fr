---
title: Attributs directionnels appliqués au paramètre
description: Les attributs directionnels \ dans \ et \ out \ déterminent la façon dont le client et le serveur allouent et libèrent de la mémoire. Le tableau suivant résume l’effet des attributs directionnels sur l’allocation de mémoire.
ms.assetid: 21ab54c4-a707-4ee3-bea8-8ba216e25c16
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 752432836075b319483e3a17421f691a111689b4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/20/2020
ms.locfileid: "106512119"
---
# <a name="directional-attributes-applied-to-the-parameter"></a>Attributs directionnels appliqués au paramètre

Les attributs directionnels \[ [dans](/windows/desktop/Midl/in) \] et \[ [out](/windows/desktop/Midl/out-idl) \] déterminent la façon dont le client et le serveur allouent et libèrent de la mémoire. Le tableau suivant résume l’effet des attributs directionnels sur l’allocation de mémoire.



| Attribut directionnel    | Mémoire sur le client                                                                                            | Mémoire sur le serveur                                                                                                                                        |
|--------------------------|-------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| \[[dans](/windows/desktop/Midl/in)\]       | L’application cliente doit allouer avant l’appel.                                                           | Le stub serveur est alloué.                                                                                                                                  |
| \[en [sortie](/windows/desktop/Midl/out-idl)\] | Le stub client est alloué lors du retour.                                                                            | Le stub serveur alloue le pointeur de niveau supérieur uniquement. l’application serveur doit allouer tous les pointeurs incorporés. Le serveur alloue également de nouvelles données en fonction des besoins. |
| \[**in**, **out**\]      | L’application cliente doit allouer les données initiales transmises au serveur. le stub client alloue des données supplémentaires. | Le stub serveur alloue les données initiales transmises à partir du client ; l’application serveur alloue les nouvelles données en fonction des besoins.                                        |



 

Dans tous les cas, le stub client ne libère pas la mémoire. L’application cliente doit libérer la mémoire avant qu’elle ne se termine. Le stub serveur libère de la mémoire lorsque l’appel de procédure distante retourne (sous réserve de l' \[ attribut [allocate](/windows/desktop/Midl/allocate) \] ACF).

 

 