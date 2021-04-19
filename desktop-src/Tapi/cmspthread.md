---
description: La classe CMSPThread implémente le thread de travail MSP.
ms.assetid: 9dc2373a-cdcf-4e60-95fa-56cb68bda15b
title: CMSPThread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17a12b71668e81688b5de7f41e188a51b88944d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/08/2021
ms.locfileid: "106520738"
---
# <a name="cmspthread"></a>CMSPThread

La classe **CMSPThread** implémente le thread de travail du MSP. Les classes de base utilisent ce thread de travail à différentes fins. Un mécanisme d’élément de travail générique et léger est fourni pour permettre au MSP dérivé d’utiliser ce thread pour ses propres éléments de travail synchrones ou asynchrones, quel que soit le cas. Le thread pompe également les messages et prend en charge la gestion des APC (bien que les APC ne soient pas utilisés dans les classes de base).

Lorsque plusieurs adresses similaires sont présentes (autrement dit, lorsque la même implémentation MSP de la même DLL est instanciée plusieurs fois), la classe thread garantit l’évolutivité en utilisant automatiquement un thread unique pour toutes les adresses. L’interface à la classe thread est telle que l’implémentation MSP peut considérer la classe thread comme un thread privé et n’a pas besoin de se soucier des autres adresses qui peuvent la partager.

Défini dans MSPthrd. h.

 

 



