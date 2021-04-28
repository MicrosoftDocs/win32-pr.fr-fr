---
description: Protection DEP/NX
ms.assetid: 92F628E4-6106-42F7-B868-A3101C7A3F0A
title: Protection DEP/NX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3565460cbfd2e6b13c3c5ba6b1f0693a3d5b25ba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108088567"
---
# <a name="depnx-protection"></a>Protection DEP/NX

À compter de Windows Internet Explorer 7 sur Windows Vista, l’élément du panneau de configuration Internet comprend une option **activer la protection** de la mémoire pour atténuer les attaques en ligne. Cette option est également appelée prévention de *l’exécution des données* (DEP) ou *No-Execute* (NX). Quand cette option est activée, elle fonctionne avec le processeur pour empêcher les attaques par dépassement de mémoire tampon en bloquant l’exécution du code à partir de la mémoire qui est marquée comme non exécutable.

Dans Windows Internet Explorer 8 sur le système d’exploitation Windows Vista avec Service Pack 1 (SP1) ou une version ultérieure, cette option est activée par défaut. DEP/NX ne protège pas contre toutes les vulnérabilités basées sur la mémoire. Mais lorsqu’il est combiné à d’autres technologies telles que la randomisation du format d’espace d’adresse (ASLR), il permet d’éviter les vulnérabilités de dépassement de mémoire tampon courantes dans Windows Internet Explorer et les modules complémentaires qu’il charge. Aucune intervention supplémentaire de l’utilisateur n’est requise pour fournir cette protection et aucune nouvelle invite n’est introduite.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Résolution des problèmes de compatibilité dans les applications Web à l’aide de l’affichage de compatibilité](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



