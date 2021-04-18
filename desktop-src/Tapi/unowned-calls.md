---
description: Pour empêcher les appels sans propriétaire d’être dans le système de téléphonie, TAPI supprime les appels qui ont été signalés auprès d’un fournisseur de services s’il ne peut pas identifier une application comme étant le propriétaire initial de l’appel.
ms.assetid: 6aa9ceb8-4dc7-46b9-979c-bf59a92cdf27
title: Appels sans propriétaire
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ebf07f4d109eb83fb8666728d71c1e129d6cb499
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/07/2021
ms.locfileid: "106519330"
---
# <a name="unowned-calls"></a>Appels sans propriétaire

Pour empêcher les appels sans propriétaire d’être dans le système de téléphonie, TAPI supprime les appels qui ont été signalés auprès d’un fournisseur de services s’il ne peut pas identifier une application comme étant le propriétaire initial de l’appel. Dans TAPI version 2,0 et versions ultérieures, TAPI appelle la fonction [**TSPI \_ lineDrop**](/windows/win32/api/tspi/nf-tspi-tspi_linedrop) pour supprimer l’appel.

Le fournisseur de services peut savoir à l’avance si une application est disponible pour prendre possession d’un nouvel appel. L’interface TAPI informe toujours le fournisseur de services des types de média pour lesquels une application est disponible à l’aide de la fonction [**TSPI \_ lineSetDefaultMediaDetection**](/windows/win32/api/tspi/nf-tspi-tspi_linesetdefaultmediadetection) .

Par exemple, si un fournisseur de services détermine qu’il y a un appel actif sur la ligne qui a le \_ mode INTERACTIVEVOICE LINEMEDIAMODE, il doit vérifier la détection de support par défaut avant de générer les messages de ligne [**\_ NEWCALL**](line-newcall.md) et de [**ligne \_ CALLSTATE**](/previous-versions/windows/desktop/legacy/ms725219(v=vs.85)) . Si la détection de support par défaut indique qu’aucune application n’est en train de rechercher un \_ appel LINEMEDIAMODE INTERACTIVEVOICE, le fournisseur de services ne doit pas envoyer les messages, car l’interface TAPI la supprimera immédiatement.

 

 
