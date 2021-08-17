---
description: 'Le gestionnaire de mémoire crée les pools de mémoire suivants utilisés par le système pour allouer de la mémoire : pool non paginé et pool paginé.'
ms.assetid: 68ee9c72-f3a3-4f1f-a827-ed4210a665e4
title: Pools de mémoire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08a49597cf90324395c50a4e44aac03815426f0c1de8ea2c7ca7aa85b5cdac95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117808996"
---
# <a name="memory-pools"></a>Pools de mémoire

Le gestionnaire de mémoire crée les pools de mémoire suivants utilisés par le système pour allouer de la mémoire : pool non paginé et pool paginé. Les deux pools de mémoire sont situés dans la région de l’espace d’adressage réservée pour le système et mappés à l’espace d’adressage virtuel de chaque processus. Le pool non paginé se compose d’adresses mémoire virtuelles qui sont garanties de résider dans la mémoire physique tant que les objets de noyau correspondants sont alloués. La réserve paginée se compose d’une mémoire virtuelle qui peut être paginée et déverrouillée du système. Pour améliorer les performances, les systèmes avec un seul processeur ont trois pools paginés et les systèmes multiprocesseurs ont cinq pools paginés.

Les descripteurs des [objets de noyau](../sysinfo/kernel-objects.md) sont stockés dans la réserve paginée, donc le nombre de handles que vous pouvez créer est basé sur la mémoire disponible.

Le système enregistre les limites et les valeurs actuelles de la réserve non paginée, de la réserve paginée et de l’utilisation du fichier d’échange. Pour plus d’informations, consultez [informations sur les performances](memory-performance-information.md)de la mémoire.

 

 
