---
description: Les fonctions suivantes vous permettent d’énumérer les ressources protégées.
ms.assetid: 6806c320-6071-4075-9003-2469089a9cc4
title: Fonctions WRP
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de4a2639d6796bd083c8f4df6a4952941cfa9e0426af6494229c7a3eddd5c7be
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999199"
---
# <a name="wrp-functions"></a>Fonctions WRP

Les fonctions suivantes vous permettent d’énumérer les ressources protégées.



| Fonction                                         | Description                                                 |
|--------------------------------------------------|-------------------------------------------------------------|
| [**SfcIsFileProtected**](/windows/desktop/api/Sfc/nf-sfc-sfcisfileprotected) | Détermine si le fichier spécifié est protégé.         |
| [**SfcIsKeyProtected**](/windows/desktop/api/Sfc/nf-sfc-sfciskeyprotected)   | Détermine si la clé de Registre spécifiée est protégée. |



 

S’il est disponible pour le système d’exploitation, les fonctions de cette table doivent être utilisées à la place des fonctions déconseillées : [**SfcGetNextProtectedFile**](/windows/desktop/api/Sfc/nf-sfc-sfcgetnextprotectedfile) et [**SfcGetFiles**](sfcgetfiles.md).

 

 



