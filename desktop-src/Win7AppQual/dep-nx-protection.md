---
description: Protection DEP/NX
ms.assetid: 92F628E4-6106-42F7-B868-A3101C7A3F0A
title: Protection DEP/NX
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aec30b3758361cbe2ed20e67fe6792d6f76b58a7266c6de1d554afdba8a2519c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118329939"
---
# <a name="depnx-protection"></a>Protection DEP/NX

à compter de Windows internet Explorer 7 sur Windows Vista, l’élément du panneau de configuration internet comprend une option **activer la protection** de la mémoire pour atténuer les attaques en ligne. Cette option est également appelée prévention de *l’exécution des données* (DEP) ou *No-Execute* (NX). Quand cette option est activée, elle fonctionne avec le processeur pour empêcher les attaques par dépassement de mémoire tampon en bloquant l’exécution du code à partir de la mémoire qui est marquée comme non exécutable.

dans Windows Internet Explorer 8 sur le système d’exploitation Windows Vista avec Service Pack 1 (SP1) ou une version ultérieure, cette option est activée par défaut. DEP/NX ne protège pas contre toutes les vulnérabilités basées sur la mémoire. mais lorsqu’il est combiné à d’autres technologies telles que la randomisation du format d’espace d’adresse (ASLR), il permet d’éviter les vulnérabilités de dépassement de mémoire tampon courantes dans Windows Internet Explorer et les modules complémentaires qu’il charge. Aucune intervention supplémentaire de l’utilisateur n’est requise pour fournir cette protection et aucune nouvelle invite n’est introduite.

## <a name="related-topics"></a>Rubriques connexes

<dl> <dt>

[Résolution des problèmes de compatibilité dans les applications Web à l’aide de l’affichage de compatibilité](remediating-web-applications-and-add-ons.md)
</dt> </dl>

 

 



